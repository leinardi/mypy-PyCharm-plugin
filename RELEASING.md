# Releasing

1. Bump the `version` property in `gradle.properties` based on Major.Minor.Patch naming scheme
2. Update `CHANGELOG.md` for the impending release.
3. Update the `README.md` with the new changes (if necessary).
4. `./gradlew clean buildPlugin` 
5. `git commit -am "Prepare for release x.y.z"` (where x.y.z is the version you set in step 1)
6. `git push`
7. Create a new release on Github
    1. Tag version `x.y.z` (`git tag -s x.y.z && git push --tags`)
    2. Release title `x.y.z`
    3. Paste the content from `CHANGELOG.md` as the description
    4. Upload the `build/distributions/pylint-plugin-x.y.z.zip`
8. Create a PR from [master](../../tree/master) to [release](../../tree/release)
9. `./gradlew publishPlugin`
