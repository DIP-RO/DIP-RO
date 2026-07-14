# GitHub Profile Setup

Upload the full contents of this folder to your public GitHub profile repository:

```text
DIP-RO/DIP-RO
```

The repository name must exactly match your GitHub username.

## 1. Upload the files

Your profile repository should contain:

```text
README.md
assets/header.svg
.github/workflows/profile-summary.yml
.github/workflows/snake.yml
```

## 2. Enable workflow write permission

Open:

```text
Repository Settings → Actions → General → Workflow permissions
```

Choose:

```text
Read and write permissions
```

Save the setting.

## 3. Add the summary-card token

The profile summary workflow needs a GitHub token to generate complete cards.

1. Create a fine-grained personal access token.
2. Give it read access to the repositories you want counted.
3. Open the profile repository:
   `Settings → Secrets and variables → Actions`.
4. Create a repository secret named:

```text
SUMMARY_GITHUB_TOKEN
```

5. Paste the token as the value.

Never put the token directly inside a workflow or README file.

## 4. Include private contribution totals

To count private activity without displaying private repository names:

1. Open GitHub profile settings.
2. Find **Contribution settings**.
3. Enable **Include private contributions on my profile**.
4. Ensure the token can read the selected private repositories.

## 5. Run both workflows once

Open the repository's **Actions** tab.

Run manually:

1. **Generate GitHub Profile Summary Cards**
2. **Generate Contribution Snake**

After both workflows finish, refresh your profile README.

## Notes

- The locally generated summary cards are committed to:
  `profile-summary-card-output/tokyonight/`
- The snake SVGs are pushed to the:
  `output` branch
- Most-used-language cards represent repository and commit data; they are not a measure of skill level.
- Some dynamic external cards can occasionally be delayed by service caching.
