# Change Log Documentation

To trigger the pipeline, create a new tag and push it to your repository:

```sh
git tag v1.0.0
git push origin v1.0.0
```

**Explanation**:

1. Workflow Trigger: The workflow triggers on pushes to tags that match the pattern v*.*.*.
2. Checkout Code: The code is checked out from the repository.
3. Set Up Go: The Go environment is set up because git-chglog is a Go application.
4. Install git-chglog: git-chglog is installed.
5. Generate Changelog: The changelog is generated and output to CHANGELOG.md.
6. Commit Changelog: The generated changelog is committed and pushed back to the repository.

This setup ensures that every time you push a new version tag, the changelog is generated and updated automatically.