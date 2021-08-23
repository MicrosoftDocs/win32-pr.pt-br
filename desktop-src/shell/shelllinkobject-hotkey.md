---
description: Obtém ou define o atalho de teclado para o link.
ms.assetid: edc65fe8-c7f3-46d0-86ca-1c0c93e7ca64
title: Propriedade ShellLinkObject.Hotkey (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.Hotkey
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5b741b40d0947119109d3496a214ccdd75c59272fd7c5f4d0eac569a5b24c3a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119591896"
---
# <a name="shelllinkobjecthotkey-property"></a>Propriedade ShellLinkObject.Hotkey

Obtém ou define o atalho de teclado para o link.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```JScript
iHotkey = ShellLinkObject.Hotkey
ShellLinkObject.Hotkey(iHotkey) = iHotkey
```



## <a name="property-value"></a>Valor da propriedade

o atalho de teclado do link. O atalho de teclado virtual está no byte de ordem baixa e os sinalizadores modificador estão no byte de ordem alta. Os sinalizadores modificador podem ser uma combinação dos valores a seguir.

<dt>



 (1)


</dt> <dd>

Tecla SHIFT

</dd> <dt>



 (2)


</dt> <dd>

Tecla CTRL

</dd> <dt>



 (4)


</dt> <dd>

tecla ALT

</dd> <dt>



 (8)


</dt> <dd>

Chave estendida

</dd> </dl>

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra o uso adequado dessa propriedade em JScript, VBScript e Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellShellLinkObjectHotkeyJ()
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
                    var nHotkey;
                    
                    // Get the keyboard shortcut for the ShellLinkObject.
                    nHotkey = objShellLink.Hotkey;
                    alert(nHotkey);
                    
                    // Set the keyboard shortcut for the ShellLinkObject.
                    objShellLink.Hotkey = 4;
                }
            }
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
     function fnShellLinkObjectHotkeyVB()
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
                                dim nHotkey
                                
                                'Get the keyboard shortcut for the ShellLinkObject.
                                nHotkey = objShellLink.Hotkey
                                alert(nHotkey)
                                
                                'Set the keyboard shortcut for the ShellLinkObject.
                                objShellLink.Hotkey = 4
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
Private Sub fnShellLinkObjectHotkeyVB()
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
                            Dim nHotkey As Integer
                            
                            'Get the keyboard shortcut for the ShellLinkObject.
                            nHotkey = objShellLink.Hotkey
                            Debug.Print nHotkey
                            
                            'Set the keyboard shortcut for the ShellLinkObject.
                            objShellLink.Hotkey = 4
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
| Cliente mínimo com suporte<br/> | Windows 2000 Professional somente com aplicativos da área de trabalho SP3 \[\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5.0 ou posterior)</dt> </dl> |



 

 




