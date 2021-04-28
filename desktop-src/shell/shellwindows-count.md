---
description: Propriedade ShellWindows. Count – contém o número de itens na coleção.
ms.assetid: 0113cc32-2197-4004-99a1-89fe10828e5f
title: Propriedade ShellWindows. Count (textdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows.Count
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b2b33dc11e6bf909043ac5391965e1ebd225d376
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103934"
---
# <a name="shellwindowscount-property"></a>Propriedade ShellWindows. Count

Contém o número de itens na coleção.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
iCount = ShellWindows.Count
```



## <a name="property-value"></a>Valor da propriedade

Um **inteiro** que contém um valor para a propriedade **Count** .

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra a **contagem** em uso. O uso adequado é mostrado para JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnShellWindowsCountJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objshell.Shell_Windows();
        if (objShellWindows != null)
        {
            var nCount;
            
            nCount = objShellWindows.Count;
            alert(nCount);
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellWindowsCountVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Shell_Windows

        if (not objShellWindows is nothing) then
            dim nCount
            nCount = objShellWindows.Count

            alert(nCount)
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellWindowsCountVB()
    Dim objShell         As Shell
    Dim objShellWindows  As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Shell_Windows

    If (Not objShellWindows Is Nothing) Then
        Debug.Print objShellWindows.Count
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>O textdisp. h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4,71 ou posterior)</dt> </dl> |



 

 




