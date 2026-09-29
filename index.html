# Fresh Windows machine, one line in PowerShell:  irm gutslfo.github.io/restore | iex
# Installs git + GitHub CLI, signs in (browser + 2FA), pulls the private config repo and runs the real restore.
foreach ($id in 'Git.Git', 'GitHub.cli') {
    winget install -e --id $id --silent --accept-source-agreements --accept-package-agreements
}
$env:Path = [Environment]::GetEnvironmentVariable('Path', 'Machine') + ';' + [Environment]::GetEnvironmentVariable('Path', 'User')
gh auth status *> $null
if ($LASTEXITCODE -ne 0) { gh auth login --web --git-protocol https }
gh auth setup-git
$cfg = Join-Path $env:TEMP 'claude-config'
if (Test-Path $cfg) { Remove-Item -Recurse -Force $cfg }
gh repo clone gutslfo/claude-config $cfg
powershell -NoProfile -ExecutionPolicy Bypass -File "$cfg\restore\restore.ps1" -ConfigClone $cfg
