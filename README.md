# SuperMemoAssistant.Services.HTML.dll

Compatible with JetBrains Rider IDE

Simply hit Build to generate SuperMemoAssistant.Services.HTML.dll

## Changed
- Removed dependency SuperMemoAssistant.Interop from Nuget Manager, replaced by local copy. 
- Add a relative path ```<ProjectReference Include="..\SuperMemoAssistant.Interop\SuperMemoAssistant.Interop.csproj" />```, so that IDE is now able to detect it. 
- For example, ```using SuperMemoAssistant.Extensions;``` in SuperMemoAssistant.Services.HTML show errors like "Cannot resolve symbol 'Extensions'", is actually referenced from SuperMemoAssistant.Interop.dll
- Both SuperMemoAssistant.Interop.dll and SuperMemoAssistant.Serivces.HTML.dll will be generated locally in the same directory, after a simple "Build Solution"
- Lock SuperMemoAssistant.Interop.dll to version 2.0.5.10, where git commit is 10/25/2020
- Recreate and tidy up the SuperMemoAssistant.Services.HTML.csproj to use consistent and dependable package versions from Nuget
- Set configuration to Debug/x86 only