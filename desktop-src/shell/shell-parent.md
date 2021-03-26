---
description: Obtém um objeto que representa o pai do objeto atual.
ms.assetid: 76c2f72c-5ef6-4f2c-bdfc-62ced6dbc504
title: Propriedade Shell. Parent (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Parent
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a121e4f87be1163429156f22dfe7bd55f1345f43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967955"
---
# <a name="shellparent-property"></a>Propriedade Shell. Parent

Obtém um objeto que representa o pai do objeto atual.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
objParent = Shell.Parent
```


```VB

Property Parent As Object
```





## <a name="property-value"></a>Valor da propriedade

Uma variável do tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que recebe o objeto pai.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra o uso apropriado do **pai** para JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnShellParentJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objParent;

        objParent = objShell.Parent;
        if (objParent != null)
        {
            alert("Got parent property");
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellParentVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            if (not objShell is nothing) then
                dim objParent

                set objParent = objShell.Parent
                    if (not objParent is nothing) then
                        alert("Got parent property")
                    end if
                set objParent = nothing
            end if
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellParentVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        If (Not objShell Is Nothing) Then
            Dim objParent As Object
            
            Set objParent = objShell.Parent
                If (Not objParent Is Nothing) Then
                    Debug.Print "Got parent object"
                End If
            Set objParent = Nothing
        End If
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4,71 ou posterior)</dt> </dl> |



 

 
