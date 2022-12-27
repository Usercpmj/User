function START()
menu = gg.multiChoice({
'ঔৣ͜͡➳『BUG START ON』',
'ঔৣ͜͡➳『BUG START OFF』',
'『ᴇxɪᴛ』',
}, nil, os.date ("y\n\n              •PANDU CPM•\ny\n\n\n╭╾•Tanggal : %Y , %m %d\n╰╾•Jam : %X , %p \n"))
if menu == nil then else
if menu[1] == true then BUGSTARTON() end
if menu[2] == true then BUGSTARTOFF() end
if menu[3] == true then EXIT() end end

Cradel = -1
end
keluar = 1

function BUGSTARTON()
gg.setVisible(false)
gg.setRanges(gg.REGION_CODE_APP)
gg.processResume()
gg.searchNumber("0D;1D;2D;3D;4D;5D;6D;7D;8D;9D;16D;17D;18D;19D;20D;21D;22D;23D;24D;25D:77", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
gg.processResume()
gg.refineNumber("0;1;2;3;4;5;6;7;8;9;16;17;18;19;20;21;22;23;24;25", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
gg.processResume()
revert = gg.getResults(100, nil, nil, nil, nil, nil, nil, nil, nil)
gg.editAll("0;0;0;0", gg.TYPE_DWORD)
gg.processResume()
gg.toast("i")
end

function BUGSTARTOFF()
gg.setVisible(false)
gg.setRanges(gg.REGION_CODE_APP)
gg.processResume()
gg.searchNumber("0D;1D;2D;3D;4D;5D;6D;7D;8D;9D;16D;17D;18D;19D;20D;21D;22D;23D;24D;25D:77", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
gg.processResume()
gg.refineNumber("0;1;2;3;4;5;6;7;8;9;16;17;18;19;20;21;22;23;24;25", gg.TYPE_DWORD, false, gg.SIGN_EQUAL, 0, -1, 0)
gg.processResume()
revert = gg.getResults(100, nil, nil, nil, nil, nil, nil, nil, nil)
gg.editAll("0;0;0;0", gg.TYPE_DWORD)
gg.processResume()
gg.toast("o")
end

keluar = 4
function EXIT()
gg.alert("SCRIPT PANDU CPM")
print("TERIMAKASIH")
gg.sleep(1000)
os.exit()
end

while true do
if gg.isVisible(true) then
Cradel = 1
gg.setVisible(false)
end
if Cradel == 1 then START() end
end
