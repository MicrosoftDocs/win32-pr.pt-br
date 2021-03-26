---
description: 'Exibe a caixa de diálogo localizar: todos os arquivos. Isso é o mesmo que clicar no menu iniciar e Selecionar Pesquisar.'
ms.assetid: 6F588D5E-5B6E-4000-BAD5-B557FB975FCA
title: Método IShellDispatch. FindFiles (shldisp. h)
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
ms.openlocfilehash: 9a9ea407d0ceccfe7706ed481aa80bcda9405ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827403"
---
# <a name="ishelldispatchfindfiles-method"></a>Método IShellDispatch. FindFiles

Exibe a caixa de diálogo **localizar: todos os arquivos** . Isso é o mesmo que clicar no menu **Iniciar** e selecionar **Pesquisar**.

## <a name="syntax"></a>Sintaxe


```JScript
IShellDispatch.FindFiles()
```


```VB

IShellDispatch.FindFiles()
```





## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

### <a name="jscript"></a>JScript

Esse método não retorna um valor.

### <a name="vb"></a>VB

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método é implementado e acessado por meio do método [**shell. findfiles**](shell-findfiles.md) .

## <a name="examples"></a>Exemplos

Os exemplos a seguir mostram o uso de **FindFiles** em JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnShellFindFilesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindFiles();
    }
</script>
```



VBScript


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
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4,71 ou posterior)</dt> </dl> |



 

 




