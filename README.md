# devtools

Common tools and configs used in rom-rb projects

## Keeping CHANGELOG.md up to date

Use the following syntax in your **commit messages** to have `CHANGELOG.md` automatically updated in rom-rb repos:

#### Updating latest version that already exists in the CHANGELOG.md

```
I added a feature

[changelog]

added: "New feature was added (@gh-handle)"
```

#### Targetting a specific version in the CHANGELOG.md

```
I added a feature

[changelog]

version: 3.1.2
added: "New feature was added (@gh-handle)"
```

> if the version doesn't exist, it will be added for you

### Adding multiple entries

```
Bump to 3.1.2

[changelog]

version: 3.1.2
added: "New feature was added (@gh-handle)"
fixed: "Something was broken and it was fixed (@gh-handle)"
changed: "Something else was changed too (@gh-handle)"
```

### Adding many items under the same entry

```
Bump to 3.1.2

[changelog]

version: 3.1.2
fixed:
- "this bug (@gh-handle)"
- "that bug (@gh-handle)"
```

### Adding release date and summary

```
Bump to 3.1.2

[changelog]

version: 3.1.2
summary: "This release is great"
```

### Adding `unreleased` version

To add or update `unreleased` version simply set `version: unreleased` ie:

```
Add a feature

[changelog]

version: unreleased
summary: "This release will be great"
added: a feature!
```

## Cherry-pick doc patches

When a doc patch is sent the bot can cherry-pick it into version branches. Use the following syntax in merge commits:

```
docsite:release-1.2
docsite:release-1.3
```

The example above patches `release-1.2` and `release-1.3` branches. Don't forget the PR should be based on `master`.
