local Players = game:GetService("Players")
local player = Players.LocalPlayer

local ScreenGui = Instance.new("ScreenGui")
ScreenGui.Name = "LeoUI"
ScreenGui.ResetOnSpawn = false
ScreenGui.Parent = player.PlayerGui

-- 主視窗
local Main = Instance.new("Frame")
Main.Size = UDim2.new(0, 1000, 0, 620)
Main.Position = UDim2.new(0.5,-500,0.5,-310)
Main.BackgroundColor3 = Color3.fromRGB(10,15,25)
Main.BorderSizePixel = 0
Main.Parent = ScreenGui

Instance.new("UICorner",Main).CornerRadius = UDim.new(0,12)

-- 側邊欄
local Sidebar = Instance.new("Frame")
Sidebar.Size = UDim2.new(0,180,1,0)
Sidebar.BackgroundColor3 = Color3.fromRGB(7,10,18)
Sidebar.BorderSizePixel = 0
Sidebar.Parent = Main

-- Logo
local Logo = Instance.new("TextLabel")
Logo.Size = UDim2.new(1,0,0,60)
Logo.BackgroundTransparency = 1
Logo.Text = "Leo"
Logo.Font = Enum.Font.GothamBold
Logo.TextSize = 28
Logo.TextColor3 = Color3.fromRGB(0,255,170)
Logo.Parent = Sidebar

-- 內容區
local Content = Instance.new("Frame")
Content.Size = UDim2.new(1,-180,1,0)
Content.Position = UDim2.new(0,180,0,0)
Content.BackgroundTransparency = 1
Content.Parent = Main

-- 搜尋框
local Search = Instance.new("TextBox")
Search.Size = UDim2.new(0,250,0,36)
Search.Position = UDim2.new(0,20,0,20)
Search.PlaceholderText = "Search..."
Search.Text = ""
Search.BackgroundColor3 = Color3.fromRGB(18,24,35)
Search.TextColor3 = Color3.new(1,1,1)
Search.Parent = Content

Instance.new("UICorner",Search).CornerRadius = UDim.new(0,8)

-- Inventory頁面
local InventoryPage = Instance.new("Frame")
InventoryPage.Size = UDim2.new(1,-40,1,-80)
InventoryPage.Position = UDim2.new(0,20,0,70)
InventoryPage.BackgroundTransparency = 1
InventoryPage.Parent = Content

local Grid = Instance.new("UIGridLayout")
Grid.CellSize = UDim2.new(0,180,0,220)
Grid.CellPadding = UDim2.new(0,15,0,15)
Grid.Parent = InventoryPage

local function CreateCard(Name, Rarity)
    local Card = Instance.new("TextButton")
    Card.BackgroundColor3 = Color3.fromRGB(15,20,30)
    Card.Text = ""
    Card.AutoButtonColor = false

    Instance.new("UICorner", Card).CornerRadius = UDim.new(0,10)

    local Title = Instance.new("TextLabel")
    Title.Size = UDim2.new(1,0,0,40)
    Title.BackgroundTransparency = 1
    Title.Text = Name
    Title.TextColor3 = Color3.new(1,1,1)
    Title.Font = Enum.Font.GothamBold
    Title.Parent = Card

    local Tag = Instance.new("TextLabel")
    Tag.Size = UDim2.new(0,80,0,25)
    Tag.Position = UDim2.new(0,10,1,-35)
    Tag.Text = Rarity
    Tag.BackgroundColor3 = Color3.fromRGB(160,40,80)
    Tag.TextColor3 = Color3.new(1,1,1)
    Tag.Parent = Card

    Instance.new("UICorner", Tag).CornerRadius = UDim.new(0,6)

    Card.Activated:Connect(function()
        print("Selected skin:", Name)
    end)

    return Card
end
CreateCard("Prototype","Covert").Parent = InventoryPage
CreateCard("Mindspill","Covert").Parent = InventoryPage
CreateCard("Labyrinth","Restricted").Parent = InventoryPage
CreateCard("Desert Strike","Mil-Spec").Parent = InventoryPage
