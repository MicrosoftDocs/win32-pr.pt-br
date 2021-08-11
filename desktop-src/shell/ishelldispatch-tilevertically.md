---
description: Organiza todas as janelas na área de trabalho verticalmente. Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar Mostrar janelas lado a lado.
ms.assetid: 63CB7E20-48E6-4cfe-B0BA-0D28A7B151BD
title: Método IShellDispatch. TileVertically (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.TileVertically
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 0863db300f18e0231143b4f3aaa28cf4fcdb9ff1a46f4c92bd99d2092fdc088d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118221493"
---
# <a name="ishelldispatchtilevertically-method"></a>Método IShellDispatch. TileVertically

Organiza todas as janelas na área de trabalho verticalmente. Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar **Mostrar janelas lado a lado**.

## <a name="syntax"></a>Sintaxe


```JScript
IShellDispatch.TileVertically()
```


```VB

IShellDispatch.TileVertically()
```





## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

### <a name="jscript"></a>JScript

Esse método não retorna um valor.

### <a name="vb"></a>VB

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método é implementado e acessado por meio do método [**shell. TileVertically**](shell-tilevertically.md) .

## <a name="examples"></a>Exemplos

os exemplos a seguir mostram o uso de **TileVertically** em JScript, VBScript e Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellTileVerticallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TileVertically();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellTileVerticallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.TileVertically

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellTileVerticallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TileVertically

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos de área de trabalho do Windows XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4,71 ou posterior)</dt> </dl> |



 

 




