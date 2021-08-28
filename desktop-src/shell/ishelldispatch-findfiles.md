---
description: 'Exibe a caixa de diálogo Encontrar: Todos os Arquivos. Isso é o mesmo que clicar no menu Iniciar e, em seguida, selecionar Pesquisar.'
ms.assetid: 6F588D5E-5B6E-4000-BAD5-B557FB975FCA
title: Método IShellDispatch.FindFiles (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.FindFiles
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 6cc390ea0ff4ba328bd0061ed03d973bff9e32054713a793ebe29ef9be2650ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942376"
---
# <a name="ishelldispatchfindfiles-method"></a>Método IShellDispatch.FindFiles

Exibe a caixa **de diálogo Encontrar: Todos os** Arquivos. Isso é o mesmo que clicar no menu **Iniciar** e, em seguida, selecionar **Pesquisar**.

## <a name="syntax"></a>Sintaxe


```JScript
IShellDispatch.FindFiles()
```


```VB

IShellDispatch.FindFiles()
```





## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

### <a name="jscript"></a>JScript

Esse método não retorna um valor.

### <a name="vb"></a>VB

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método é implementado e acessado por meio [**do método Shell.FindFiles.**](shell-findfiles.md)

## <a name="examples"></a>Exemplos

Os exemplos a seguir mostram o uso de **FindFiles** JScript, VBScript e Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellFindFilesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindFiles();
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
   function fnShellFindFilesVB()
       dim objShell
       
       set objShell = CreateObject("shell.application")
       objshell.FindFiles

       set objShell = nothing
   end function
</script>
```



Visual Basic:


```VB
Private Sub fnShellFindFilesVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindFiles

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows aplicativos da área de \[ trabalho XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4.71 ou posterior)</dt> </dl> |



 

 




