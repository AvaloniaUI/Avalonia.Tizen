# Release instructions

## Branch and Tag

1. Create a branch named `release/<version>` (e.g. `release/11.2.6`) for a specific version.
2. Update the version in `SharedVersion.props`, e.g. `<Version>11.2.6</Version>`
3. Commit the file.
4. Add a matching tag for this version, e.g. `git tag 11.2.6`
5. Push the release branch and the tag.

## CI Build

6. Wait for Azure Pipelines to finish the build. A matching build in the `nuget-feed-all` feed should be released soon after.
7. Using the build, run a due diligence test to make sure you're happy with the package.
8. On Azure Pipelines, on the build for your release, click on the badge for *NuGet (Release!)* then click on *Deploy*.

## GitHub Release

9. Make a new release on GitHub releases.
10. Select the tag matching the version, then click on *Generate release notes*. 
11. Review the release information, then click on *Publish release*.
