> [!WARNING]
> This package is deprecated. The content is moved to the [@teamleader/ahoy](https://www.npmjs.com/package/@teamleader/ahoy) package. 
> The further development of the project will be closed-source but the package will be published under the new name.

# UI Utilities

## How to make a release

1.  Pull the `next-release` branch to make sure you have all the latest code on your local machine.
2.  Make a new branch, starting from `next-release` and give it the name of the next version you want to release (`release/new.version.number`).
3.  Bump the version in `package.json` and commit with message `Version bump` and push.
4.  Update `CHANGELOG.md`

    - Replace `[unreleased]` with the `[new.version.number]` and add the release `date next to it, like this`- yyyy-mm-dd`.
    - Clean up the unused titles.
    - Prepare for next release by adding the following content on top of the file:

      ```
      ## [unreleased]

      ### Added

      ### Changed

      ### Deprecated

      ### Removed

      ### Fixed
      ```

    - Commit with message `Update changelog` and push.

5.  Make a `pull request` on Github where you add the `changelog items` as the description and wait for approval.
6.  Make a `draft release` on Github and fill in the following fields:
    - **Tag version:** `new.version.number` @ `target: next-release`
    - **Release title:** `new.version.number`
    - **Description:** add the `changelog items`
7.  Once the pull request has the needed amount of approvals, merge it into the `next-release` branch.
8.  `Publish` the earlier created `draft release` on Github.
9.  In your `console`, pull the `next-release` branch.
10. `Publish` to `npm` using the `npm publish --access=public` command.
11. `Merge` the `next-release` branch into `master` and push to Github
