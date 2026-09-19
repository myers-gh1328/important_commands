# important_commands

Keep windows awake temporarily
```ps
while ($true) { (New-Object -ComObject WScript.Shell).SendKeys('{F15}'); Start-Sleep -Seconds 60 }
```

Enable Windows Sandbox
```
Enable-WindowsOptionalFeature -FeatureName "Containers-DisposableClientVM" -All -Online
```

winget install command
```
winget install -e --id Microsoft.VisualStudioCode;winget install -e --id Kubernetes.kubectl;winget install -e --id RedHat.Podman;winget install -e --id Insomnia.Insomnia; -e --id Notepad++.Notepad++; -e --id Hashicorp.Terraform;
```

Purge all branches except main
```
git branch | %{ $_.Trim() } | ?{ $_ -ne 'main'} | %{ git branch -D $_ }
```

remove remotes
```
git fetch --prune
```

Check vulnerable packages
```
dotnet list package --include-transitive --vulnerable
```

MSSQL Impersonation
```sql
USE {DATABASE}
EXECUTE AS USER = '{USERACCOUNT}';
GO

-- add code to run here

REVERT;
GO
```
