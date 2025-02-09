local Fluent = loadstring(game:HttpGet("https://github.com/dawid-scripts/Fluent/releases/latest/download/main.lua"))()
local SaveManager = loadstring(game:HttpGet("https://raw.githubusercontent.com/dawid-scripts/Fluent/master/Addons/SaveManager.lua"))()
local InterfaceManager = loadstring(game:HttpGet("https://raw.githubusercontent.com/dawid-scripts/Fluent/master/Addons/InterfaceManager.lua"))()

-- Criar janela Fluent
local Window = Fluent:CreateWindow({
    Title = "Japa Cheat",
    SubTitle = "Powered by Japa",
    TabWidth = 160,
    Size = UDim2.fromOffset(1000, 500),
    Acrylic = false,
    transparency = false,
    Theme = "Light",
    MinimizeKey = Enum.KeyCode.RightShift -- Used when theres no MinimizeKeybind
})

-- Criar Tabs
local Tabs = {
    ini = Window:AddTab({ Title = "Japa Cheats", Icon = "user" }),
}

Tabs.ini:AddButton({ 
    Title = "Executar Japa Cheat Sem Time", 
    Callback = function() 
        loadstring(game:HttpGet("https://raw.githubusercontent.com/japa777666/JapaHub1/refs/heads/main/README.md"))() 
    end 
})

Tabs.ini:AddButton({ 
    Title = "Executar Japa Cheat Com Time", 
    Callback = function() 
        loadstring(game:HttpGet("https://raw.githubusercontent.com/japa777666/Japahub2/refs/heads/main/README.md"))() 
    end 
})


-- Notificação inicial
Fluent:Notify({
    Title = "Japa Cheat",
    Content = "Japa Cheat Injected Successfully!",
    Duration = 15
})

Window:SelectTab(Tabs.ini)
