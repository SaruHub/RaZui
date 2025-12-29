loadstring(game:HttpGet("https://raw.githubusercontent.com/anurajsaru/RaZui/refs/heads/main/1"))()

-- Define functions for each game
local function GameA()
    print("Running Game A script...")
    -- Your Game A specific WindUI setup or autofarm logic here
end

local function GameB()
    print("Running Game B script...")
    -- Your Game B specific WindUI setup or combat aura logic here
end

local function GameC()
    print("Running Game C script...")
    -- Your Game C specific WindUI setup or teleport logic here
end

-- Dispatcher
local scripts = {
    [1234567890] = GameA,  -- PlaceId for Game A
    [9876543210] = GameB,  -- PlaceId for Game B
    [5555555555] = GameC,  -- PlaceId for Game C
}

-- Run the correct script if available
local runner = scripts[game.PlaceId]
if runner then
    runner()
else
    warn("No script defined for this game.")
end
