---
description: Exibe a janela de ajuda e suporte do Windows. Esse método tem o mesmo efeito que clicar no menu iniciar e selecionar ajuda e suporte.
ms.assetid: 9460C87E-6703-4df6-A84C-8D394E0E6703
title: Método IShellDispatch. Help (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Help
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b58bcc97748cecf6ab4064ecccf3ba5bbe190b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967537"
---
# <a name="ishelldispatchhelp-method"></a>Método IShellDispatch. Help

Exibe a janela de ajuda e suporte do Windows. Esse método tem o mesmo efeito que clicar no menu **Iniciar** e selecionar **ajuda e suporte**.

## <a name="syntax"></a>Sintaxe


```JScript
IShellDispatch.Help()
```


```VB

IShellDispatch.Help()
```





## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

### <a name="jscript"></a>JScript

Esse método não retorna um valor.

### <a name="vb"></a>VB

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método é implementado e acessado por meio do método [**shell. Help**](shell-help.md) .

## <a name="examples"></a>Exemplos

Os exemplos a seguir mostram o uso da **ajuda** no JScript, no VBScript e no Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnShellHelpJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Help();
    }
</script>
```



VBScript


```VB
 <script language="VBScript">
    function fnShellHelpVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.Help

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellHelpVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.Help

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



 

 




