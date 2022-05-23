# Test Details
## .github/workflows/push.yml
```YAML
|
  name: Bump Version (Custom Wording)
  'on':
    push: null
  jobs:
    bump-version:
      runs-on: ubuntu-latest
      steps:
        - uses: actions/checkout@v2
        - id: version-bump
          uses: ./action
          env:
            GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
          with:
            minor-wording: custom-minor
            major-wording: custom-major
            rc-wording: custom-pre

```
## Message
custom-major
## Expectation
- **Version:** 4.0.0