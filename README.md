# important_commands

Purge all branches except main
```
git branch | %{ $_.Trim() } | ?{ $_ -ne 'main'} | %{ git branch -D $_ }
```
