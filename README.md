# AutoComplete


# Tech Stack
.Net Core 7.0 Web API, C#

# Environment Setup

Install dotnet 7.0 
  mac - brew install dotnet (should install the latest version
  
  Direct Download Link - https://dotnet.microsoft.com/en-us/download/dotnet/7.0

# API Project Setup

1. Download / UnCompress the Zip 
2. On your Terminal, Navigate to AutoCompleteAPI/AutoCompleteAPI (you should see AutoCOmpleteAPI.csproj)
3. Run command `dotnet build`
4. Run command `dotnet run`
5. You should see the service listening on port 5000

# UI

1. Find index.html inside /AutoCompleteAPI/AutoCompleteAPI/index.html
2. Open it and start typing 

# Input (input.json)

1. I am using Trie DS for this purpose. I didn't get much time to prepare a larger dataset. 
2. Available Words:
      - aim / aid
      - apple / app / append / appear / appeal /ape / apex / apartment 
      - pat / pie / piece / pine / pint / pineapple / pierce / ping / pinch / piper / piano
      
# Features

1. Trie DataStructure (Idea is to potentially use a MongoDB Repository
2. REST Routes
   /Suggestions/GetSuggestions?prefix=ap
   /Suggestions/IncreaseFrequency?word=apple
3. In Memory Caching (Idea is to use Redis or Distributed Cache in future)
   - Auto expires in few seconds
