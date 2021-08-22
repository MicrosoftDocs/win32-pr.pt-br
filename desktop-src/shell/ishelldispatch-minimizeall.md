---
description: Minimiza todas as janelas na área de trabalho. Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar Minimizar Todos os Windows sistemas mais antigos ou clicar no ícone Mostrar Área de Trabalho na barra de tarefas.
ms.assetid: 25DD56B0-221E-44a2-9FAD-FB358ADD7FF1
title: Método IShellDispatch.MinimizeAll (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.MinimizeAll
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 18f1256f93c9cd18d0c904f090716641b466e91319dbef323ee5107b802f82ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452981"
---
# <a name="ishelldispatchminimizeall-method"></a>Método IShellDispatch.MinimizeAll

Minimiza todas as janelas na área de trabalho. Esse método tem o mesmo efeito que clicar com o botão direito do mouse na  barra de tarefas e selecionar Minimizar Todos **os** Windows em sistemas mais antigos ou clicar no ícone Mostrar Área de Trabalho na barra de tarefas.

## <a name="syntax"></a>Sintaxe


```JScript
IShellDispatch.MinimizeAll()
```


```VB

IShellDispatch.MinimizeAll()
```





## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

### <a name="jscript"></a>JScript

Esse método não retorna um valor.

### <a name="vb"></a>VB

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método é implementado e acessado por meio do [**método Shell.MinimizeAll.**](shell-minimizeall.md)

## <a name="examples"></a>Exemplos

Os exemplos a seguir mostram o uso de **MinimizeAll** em uso para JScript, VBScript e Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellMinimizeAllJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.MinimizeAll();
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellMinimizeAllVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.MinimizeAll

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellMinimizeAllVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.MinimizeAll

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows somente aplicativos da \[ área de trabalho XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4.71 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IShellDispatch**](ishelldispatch.md)
</dt> <dt>

[**UndoMinimizeALL**](shell-undominimizeall.md)
</dt> </dl>

 

 




