<img src="./screenshot.jpg" alt="theme-screenshot" width="45%"/>


```powershell
# Install Oh-My-Posh
winget install JanDeDobbeleer.OhMyPosh

# Copy the theme file to 
"C:\Users\{username}\AppData\Local\Programs\oh-my-posh\themes"

# Set the theme file path to the environment variable
notepad $PROFILE

# If error occurs, run the following command 
new-item -type file -path $profile -force

# Add the following lines to the profile file
oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH\theme.omp.json" | Invoke-Expression

# Reload the profile
. $PROFILE

# If script error occurs, run the following command
Set-ExecutionPolicy -ExecutionPolicy Unrestricted
```