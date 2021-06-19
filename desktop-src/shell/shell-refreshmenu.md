---
description: Saiba mais sobre o método Shell. RefreshMenu, que atualiza o conteúdo do menu iniciar. Usado apenas com sistemas anteriores ao Windows XP.
ms.assetid: 1269c66d-61df-432d-9220-5ac975e3ad58
title: Método Shell. RefreshMenu (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.RefreshMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 90020cd128f5cbc585bd7bc9ab33a8a81c745f8e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404529"
---
# <a name="shellrefreshmenu-method"></a>Método Shell. RefreshMenu

Atualiza o conteúdo do menu **Iniciar** . Usado apenas com sistemas anteriores ao Windows XP.

## <a name="syntax"></a>Sintaxe


```JScript
iRetVal = Shell.RefreshMenu()
```


```VB

Shell.RefreshMenu() As Integer
```





## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="remarks"></a>Comentários

A funcionalidade que o **RefreshMenu** fornece é tratada automaticamente no Windows XP ou posterior. Não chame esse método nesse sistema operacional.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra **RefreshMenu** em uso. O uso adequado é mostrado para JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnShellRefreshMenuJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.RefreshMenu();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellRefreshMenuVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.RefreshMenu

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellRefreshMenuVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.RefreshMenu

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



 

 




