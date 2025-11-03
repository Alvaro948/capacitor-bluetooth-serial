# Release Process

## Prerequisites

Before making a release, ensure the following tools are installed:

- **Java (JDK 11 or newer)**
- **Gradle**
- **CocoaPods**

## Steps to make a new release

1. **Verify the project:**

```sh
npm run verify
npm run lint
```

2. **Update the version:**
   Bump the version in `package.json` and `CapacitorBluetoothSerial.podspec` as needed.

3. **Build the plugin:**

```sh
npm run build
```

4. **Commit and tag the release:**

```sh
git add .
git commit -m "feat: 🎸 <message>"
# Optionally, use npx git-cz for a guided commit message
# npx git-cz

# Tag the commit (this will tag the latest commit, which includes all changes)
git tag <version>

# Push the commit and the tag in one go
git push && git push --tags
```

5. **Publish to npm:**

```sh
npm publish
```

6. **Publish to CocoaPods:**

```sh
npm run publish:cocoapod
```

7. **Verify release:**
   Check npm and CocoaPods for the new version.

Repeat these steps for each new release. Update this section if the process changes.
