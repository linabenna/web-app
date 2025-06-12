# Wrap public website into a mobile app (Android- for now)

Instructions below will use Capacitor to wrap a public website into a mobile app.

## Project Structure
You may start with the following file structure.
```
my-mobile-app/
├── front/
│   ├── index.html
├── mobile/ 
```
Below is the complete project file structure for reference.
```
my-mobile-app/
├── front/
│   ├── index.html
├── mobile/
│   ├── capacitor.config.json 
│   ├── package.json
│   ├── node_modules/
│   ├── android/
│   ├── ios/
│   └── www/
│       └── index.html  
```

### 1. Install Capacitor

```bash
cd mobile
npm init -y
npm install @capacitor/core @capacitor/cli
npx cap init "MyMobileApp" "com.lina.myapp"
```

Press Enter.

### 2. Copy index to www

```bash
cp ../front/* www/
```

### 3. Install Android Platform

```bash
npm install @capacitor/android
```

### 4. Build Android project

```bash
npx cap add android  
```

You can view the android project in your mobile/ directory and open it through Android Studio.

---

## As for ios, these steps work only on Mac
Following from the steps above:

### 1. Install ios platform:

```bash
npm install @capacitor/ios
```

### 2. Build ios project

```bash
npx cap add ios
```
