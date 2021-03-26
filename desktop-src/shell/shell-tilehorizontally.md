---
description: Organiza todas as janelas na área de trabalho horizontalmente. Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar janelas de bloco horizontalmente.
ms.assetid: b0e06766-1bd4-4744-81f3-139b018aa72c
title: Método Shell. TileHorizontally (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.TileHorizontally
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e295d0a7847afc0cb405f3ab9141e54ae424e9e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170084"
---
# <a name="shelltilehorizontally-method"></a>Método Shell. TileHorizontally

Organiza todas as janelas na área de trabalho horizontalmente. Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar **janelas de bloco horizontalmente**.

## <a name="syntax"></a>Sintaxe


```JScript
iRetVal = Shell.TileHorizontally()
```


```VB

Shell.TileHorizontally() As Integer
```





## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra **TileHorizontally** em uso. O uso adequado é mostrado para JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnShellTileHorizontallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.TileHorizontally();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellTileHorizontallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.TileHorizontally

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellTileHorizontallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.TileHorizontally

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



 

 




