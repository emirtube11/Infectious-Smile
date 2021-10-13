local b = game:GetService("Players").LocalPlayer
local c = game:GetService("RunService")
while wait() do
   if b.Character and b.Character:FindFirstChild("Humanoid") ~= nil then
       if
           b.Character:FindFirstChild("Bat") == nil and b.Backpack:FindFirstChild("Bat") == nil and
               b.Character.Humanoid.Health ~= 0
        then
           local d = b.Character.HumanoidRootPart.CFrame
           repeat
               b.Character.HumanoidRootPart.CFrame =
                   CFrame.new(
                   -19.8717194,
                   4.56999779,
                   -22.1750679,
                   -0.093234241,
                   -9.18765934e-08,
                   0.995644212,
                   -2.4196261e-08,
                   1,
                   9.00127475e-08,
                   -0.995644212,
                   -1.5698598e-08,
                   -0.093234241
               )
               if syn then
                   fireclickdetector(game:GetService("Workspace").Map.Terrain.Vendor.BatCollection.ClickDetector)
               end
               c.RenderStepped:Wait()
           until b.Backpack:FindFirstChild("Bat") ~= nil
           b.Character:FindFirstChild("Humanoid"):UnequipTools()
           local e = b.Backpack:FindFirstChild("Bat")
           a = Instance.new("SelectionBox", e.BodyAttach)
           a.Adornee = e.BodyAttach
           e.Parent = b.Backpack
           e.BodyAttach.Size = Vector3.new(25, 25, 25) -- here you can change
           e.BodyAttach.Massless = true
           e.Parent = b.Character
           for f = 1, 10 do
               b.Character.HumanoidRootPart.CFrame = d
               c.RenderStepped:Wait()
           end
       end
   end
end
