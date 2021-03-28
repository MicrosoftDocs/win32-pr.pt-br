---
description: Obtém ou define o caminho para o objeto de link.
ms.assetid: ddb5be91-7c21-46c8-949e-bdd973e11b6c
title: Propriedade ShellLinkObject. Path (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.Path
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ac6b6f1168724f3808462088dc7e5907ec0cec58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172194"
---
# <a name="shelllinkobjectpath-property"></a>Propriedade ShellLinkObject. Path

Obtém ou define o caminho para o objeto de link.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```JScript
strPath = ShellLinkObject.Path
ShellLinkObject.Path(sPath) = strPath
```



## <a name="property-value"></a>Valor da propriedade

o caminho totalmente qualificado do objeto de link.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra o uso apropriado dessa propriedade em JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnShellShellLinkObjectPathJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.ParseName("Internet Explorer.lnk");
            if (objFolderItem != null)
            {
                var objShellLink;
                
                objShellLink = objFolderItem.GetLink;
                if (objShellLink != null)
                {
                    var szPath;
                    
                    // Get the path for the ShellLinkObject.
                    szPath = objShellLink.Path;
                    alert(szPath);
                    
                    // Set the path for the ShellLinkObject.
                    objShellLink.Path = "C:\\Program Files\\IE\\IEXPLORE.EXE";
                }
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellLinkObjectPathVB()
        dim objShell
        dim objFolder
        dim ssfPROGRAMS
        
        ssfPROGRAMS = 2
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objFolderItem
                
                set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                    if (not objFolderItem is nothing) then
                        dim objShellLink
                        
                        set objShellLink = objFolderItem.GetLink
                            if (not objShellLink is nothing) then
                                dim szPath
                                
                                'Get the path for the ShellLinkObject..
                                szPath = objShellLink.Path
                                alert(szPath)
                                
                                'Set the path for the ShellLinkObject
                                objShellLink.Path = "C:\Program Files\IE\IEXPLORE.EXE"
                            end if
                        set objShellLink = nothing
                    end if
                set objFolderItem = nothing
            end if
        set objFolder = nothing
        set objShell = nothing
    end function

 </script>
```



Visual Basic:


```VB
Private Sub fnShellLinkObjectPathVB()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                If (Not objFolderItem Is Nothing) Then
                    Dim objShellLink As ShellLinkObject
                    
                    Set objShellLink = objFolderItem.GetLink
                        If (Not objShellLink Is Nothing) Then
                            Dim szPath As String
                            
                            'Get the path for the ShellLinkObject.
                            szPath = objShellLink.Path
                            Debug.Print szPath
                            
                            'Set the path for the ShellLinkObject.
                            objShellLink.Path = "C:\Program Files\IE\IEXPLORE.EXE"
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows 2000 Professional com SP3 \[\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



 

 




