BasePanel:subClass("MainPanel")
MainPanel.name = "MainPanel"

function MainPanel:Init()
    self.base.Init(self)
    -- 避免重复向UI控件添加监听事件
    if self.isInitEvent == false then
        self:GetControl("btnRole", "Button").onClick:AddListener(function()
            self:BtnRoleClick()
        end)
        self.isInitEvent = true
    end
end

function MainPanel:BtnRoleClick()
    BagPanel:ShowMe()
end