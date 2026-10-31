# Guardian News for Android

A Kotlin news reader using the Guardian API, Paging 3, Room, Retrofit, and MVVM.

## Highlights

- Fetch articles from the Guardian Content API with Retrofit.
- Load paginated results with Paging 3 and a remote mediator.
- Cache article data and pagination keys in Room.
- Keep settings in DataStore and separate UI state with ViewModels.

**Stack:** Kotlin · Android Views · MVVM · Retrofit · Room · Paging 3 · Coil

## Getting started

Use Android Studio with JDK 17, Android SDK 33, and a device or emulator running Android API 29 or newer.

```bash
git clone https://github.com/imhmdrz/guardian-news-android.git
cd guardian-news-android
./gradlew :app:assembleDebug
```

Open the repository in Android Studio, let Gradle sync, and run the `app` configuration. On Windows, use `gradlew.bat` in place of `./gradlew`.

### Guardian API access

Obtain your own key from [Guardian Open Platform](https://open-platform.theguardian.com/access/). The current request declares its API key directly in `GuardianApiService.kt`; configure your own key there before running. Keep personal credentials out of published commits. The project does not currently expose a `local.properties` API-key setting.

## Code map

Paths below are relative to `app/src/main/java/com/example/myproj/`.

| Directory | Responsibility |
| --- | --- |
| `loadDataFromInternet/` | API interface and Retrofit client |
| `pagingMediator/` | Network and database pagination |
| `roomDataBase/` | Article cache and remote keys |
| `repository/` | Data access |
| `uiHolder/` | Article UI, adapters, and ViewModels |
| `dataStore/` | User preferences |
