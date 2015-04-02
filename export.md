1. IE内核浏览器，使用ActiveX技术   
`var exportData = ['1,2,3,4,5,6', 'a,b,c,d,e,f'];`
`var wshShell = new ActiveXObject('WScript.Shell'),`
`    desktop = wshShell.SpecialFolders('Desktop'), // 获取用户的桌面路径`
`    sheet = new ActiveXObject('Excel.Sheet');`
`sheet.Application.Visible = true;`
`for (var i = 0; i < exportData.length; i++) {`
`    var currArr = exportData[i].split(separator);`
`    for (var j = 0; j < currArr.length; j++) {`
`        sheet.ActiveSheet.Cells(i + 1, j + 1).Value = currArr[j];`
`    }`
`}`

`sheet.SaveAs(desktop + '\\' + 'test.csv'); // 将文件导出到用户桌面`
`sheet.Application.Quit(); `