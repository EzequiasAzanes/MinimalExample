# Bug Report: Minimal Example for @expo/cli 

## Steps to Reproduce

1. Create a new Expo project:

```bash
   npx create-expo-app MinimalExample
```

2. Start the app

```bash
   npx expo start
```

## Expected Behaviour

The project should start without any errors as it is fresh install.

## Actual Behaviour

I received a fetch error when trying to start the project.

```Error Logs
      Starting Metro Bundler
TypeError: fetch failed
TypeError: fetch failed
    at node:internal/deps/undici/undici:12618:11
    at processTicksAndRejections (node:internal/process/task_queues:95:5)
    at fetchWithCredentials (C:\Users\azane\OneDrive\Documents\Expo\MinimalExample\node_modules\@expo\cli\src\api\rest\client.ts:91:24)
    at cachedFetch (C:\Users\azane\OneDrive\Documents\Expo\MinimalExample\node_modules\@expo\cli\src\api\re    at getNativeModuleVersionsAsync (C:\Users\azane\OneDrive\Documents\Expo\MinimalExample\node_modules\@expo\cli\src\api\getNativeModuleVersions.ts:39:20)
    at getVersionedNativeModulesAsync (C:\Users\azane\OneDrive\Documents\Expo\MinimalExample\node_modules\@expo\cli\src\start\doctor\dependencies\bundledNativeModules.ts:33:14)
    at getCombinedKnownVersionsAsync (C:\Users\azane\OneDrive\Documents\Expo\MinimalExample\node_modules\@expo\cli\src\start\doctor\dependencies\getVersionedPackages.ts:58:7)
    at getVersionedDependenciesAsync (C:\Users\azane\OneDrive\Documents\Expo\MinimalExample\node_modules\@expo\cli\src\start\doctor\dependencies\validateDependenciesVersions.ts:97:33)
    at validateDependenciesVersionsAsync (C:\Users\azane\OneDrive\Documents\Expo\MinimalExample\node_modules\@expo\cli\src\start\doctor\dependencies\validateDependenciesVersions.ts:46:25)
    at startAsync (C:\Users\azane\OneDrive\Documents\Expo\MinimalExample\node_modules\@expo\cli\src\start\startAsync.ts:112:5)
   ```

## Environment

- OS: Windows 10
- Node.js version: 18.20.5
- Code Editor: VS Code
- Test App: Expo Go and Android Studio Virtual Device Manager

## Other details

- Firewall allowed Nodejs
- Can access expo.dev
- Stable internet connection
- Tested to different nodejs version (18.18.0, 18.20.5, 20.11.0, 22.11.0)

Note: 
I have 2 working project which were working till November 13, 2024. Opened the project on November 14, 2024 and 2 projects display the same error.
I created Expo project to check if the error will not display on newly installed project and got the same error.

```bash
   npx create-expo-app@latest projectName --template blank
```