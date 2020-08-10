# React Native CallKeep (fork with additional improvements)

Improvements:
- take control over permissions, no more obtrusive alerts. You can redirect to phone account settings from your app.

API (Android only)
```
static checkPhoneAccountEnabled(): Promise<boolean>
static registerPhoneAccount(): void
```

- 0 crashes when you call `backToForeground()` in headless mode

- new, better headless mode. You can wake killed app on Android and pass parameters like `callUUID`
API (Android only)
```
static openAppFromHeadlessMode(callUUID: string): void
static getExtrasFromHeadlessMode(): Promise<HeadlessExtras>
```

- render custom UI over locked screen (you don't need to unlock your phone)

API (Android only):
```
static showOnLockedScreen(): void
static hideFromLockedScreen(): void
```

- better TypeScript typings - no more `@ts-ignore`

## Credits
Full credits goes to original maintainers of `react-native-callkeep` repo

## License

This work is dual-licensed under ISC and MIT.
Previous work done by @ianlin on iOS is on ISC Licence.
We choose MIT for the rest of the project.

