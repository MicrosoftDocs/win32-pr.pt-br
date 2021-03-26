---
description: Exibe a barra de tarefas e a caixa de diálogo Propriedades do menu iniciar. Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar Propriedades.
ms.assetid: 0d82d847-9e6f-461e-b938-fe8fd49a636f
title: Método Shell. Trayproperties (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.TrayProperties
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: da3fbfdb2b6aa2517b275041856920c6b2cd1bb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968163"
---
# <a name="shelltrayproperties-method"></a>Método Shell. Trayproperties

Exibe a **barra de tarefas e a caixa de diálogo Propriedades do menu iniciar** . Esse método tem o mesmo efeito que clicar com o botão direito do mouse na barra de tarefas e selecionar **Propriedades**.

## <a name="syntax"></a>Sintaxe


```JScript
iRetVal = Shell.TrayProperties()
```


```VB

Shell.TrayProperties() As Integer
```





## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra **trayproperties** em uso. O uso adequado é mostrado para JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnShellTrayPropertiesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.TrayProperties();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellTrayPropertiesVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.TrayProperties

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellTrayPropertiesVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.TrayProperties

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



 

 




