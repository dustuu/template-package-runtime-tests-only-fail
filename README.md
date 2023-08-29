* [template-package-runtime-tests-only-fail](https://github.com/dustuu/template-package-runtime-tests-only-fail) shows what happens when all repository variables and secrets are configured properly, but Unit Tests are only present for testing the package's Editor Scripts.
  * Because `REQUIRED_COVERAGE` is still set to `100`, the `Build Release` workflow will fail due to the Unit Tests no longer covering the Editor Scripts:
  * ![image](https://github.com/vrchat-community/template-package/assets/101824882/2b4f2d9c-45a4-4f88-8ff1-b063798b5f80)
  * The `Build Repo Listing` workflow will fail as expected because there are no published releases.
  * Both badges will be broken because there are no releases:
    * [![VPM Package Version](https://img.shields.io/vpm/v/com.vrchat.demo-template?repository_url=https%3A%2F%2Fdustuu.github.io%2Ftemplate-package-runtime-tests-only-fail%2Findex.json)](https://dustuu.github.io/template-package-runtime-tests-only-fail)
    * [![Code Coverage](https://dustuu.github.io/template-package-runtime-tests-only-fail/coverage/badge_linecoverage.svg)](https://dustuu.github.io/template-package-runtime-tests-only-fail/coverage)
