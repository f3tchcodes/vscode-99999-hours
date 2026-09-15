# vscode-99999-hours

Modify or spoof Discord VSCode RPC using Discord Presence extension by iCrawl.

## Steps to reproduce
1. Install the extension "Discord Presence" by iCrawl on VSCode.
  <img width="527" height="156" alt="image" src="https://github.com/user-attachments/assets/7baee253-e73c-4176-810a-e9660c78cacc" />

2. Find and open extension folder on your operating system:
  - **Windows:** Press `Win + R` to open Run window, paste `%USERPROFILE%\.vscode\extensions` and hit enter.
  - **Linux and macOS:** Open terminal and run `cd ~/.vscode/extensions`.

3. Find iCrawl's Discord Presence extension folder, it should be named something along the lines of `icrawl.discord-vscode-<version>`.

4. Inside the folder, navigate to `dist/extension.cjs` and open the file via VSCode.

5. Search and replace:

Search: 
```
startTimestamp: config2["removeTimestamp" /* RemoveTimestamp */] ? void 0 : previous.startTimestamp ?? Date.now()
```
Replace with: 
```
startTimestamp: config2["removeTimestamp" /* RemoveTimestamp */] ? void 0 : previous.startTimestamp ?? Date.now() - 359996401000
```

6. Reload window or restart VSCode and confirm the modified rich presence:
  <img width="665" height="550" alt="image" src="https://github.com/user-attachments/assets/fe0c03f9-c40e-4847-9895-bbe6c2ea2056" />

## License

This work is licensed under the Creative Commons Attribution 4.0 International License.
https://creativecommons.org/licenses/by/4.0/
