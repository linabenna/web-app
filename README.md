# Wrap public website into a mobile app (Android- for now)

Instructions below will use Capacitor to wrap a public website into a mobile app.

## Project Structure
You may start with the following file structure.
```
my-mobile-app/
├── front/
│   ├── index.html
│   ├── styles.css
├── mobile/ 
```
Below is the complete project file structure for reference.
```
my-mobile-app/
├── front/
│   ├── index.html
│   ├── styles.css
├── mobile/
│   ├── capacitor.config.json 
│   ├── package.json
│   ├── node_modules/
│   └── www/
│       └── index.html  
```

### 1. Install NVM
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash
```

Restart your terminal using below:

```bash
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
```

### 2. Install Node.js version 18
I had to downgrade because of compatibility issues, but you can start with the latest version- up to you.
```bash
nvm install 18
nvm use 18
```

### 3. Set up the Capacitor project

Navigate into the mobile folder:

```bash
cd mobile
```

Copy the index.html file into mobile/wwww:

```bash
cp my-mobile-app/front/index.html ./www/
```

Install the required packages:
I am also using an older version of capacitor.

```bash
npm install
npm install @capacitor/cli@4 @capacitor/core@4
npm install @capacitor/android@4
```

### 4. Build the Android project

```bash
npx cap add android
npx cap copy
```

The command below will open the Android project in Android Studio where you can build and run your mobile app.

```bash
npx cap open android
```
