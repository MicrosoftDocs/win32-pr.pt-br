---
description: Obtém ou define o diretório de trabalho especificado no link.
ms.assetid: c3820deb-9f00-42a9-ab0e-c0f6389e9f29
title: Propriedade ShellLinkObject. WorkingDirectory (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.WorkingDirectory
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d8788899a06179056cd871b68e4e64566bcd5ee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296874"
---
# <a name="shelllinkobjectworkingdirectory-property"></a>Propriedade ShellLinkObject. WorkingDirectory

Obtém ou define o diretório de trabalho especificado no link.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```JScript
strWorkingDirectory = ShellLinkObject.WorkingDirectory
ShellLinkObject.WorkingDirectory(sWorkingDirectory) = strWorkingDirectory
```



## <a name="property-value"></a>Valor da propriedade

o caminho totalmente qualificado do diretório de trabalho do link.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra o uso apropriado dessa propriedade em JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnShellShellLinkObjectWorkingDirectoryJ()
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
                    var szDirectory;
                    
                    // Get the working directory for the ShellLinkObject.
                    szDirectory = objShellLink.WorkingDirectory;
                    alert(szDirectory);
                    
                    // Set the working directory for the ShellLinkObject.
                    objShellLink.WorkingDirectory = "";
                }
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellLinkObjectWorkingDirectoryVB()
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
                                dim szDirectory
                                
                                'Get the working directory.
                                szDirectory = objShellLink.WorkingDirectory
                                alert(szDirectory)
                                
                                'Set the working directory.
                                objShellLink.WorkingDirectory = ""
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
Private Sub fnShellLinkObjectWorkingDirectoryVB()
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
                            Dim szDirectory As String
                            
                            'Get the working directory.
                            szDirectory = objShellLink.WorkingDirectory
                            Debug.Print szDirectory
                            
                            'Set the working directory.
                            objShellLink.WorkingDirectory = ""
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows 2000 Professional com SP3 \[\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



 

 




