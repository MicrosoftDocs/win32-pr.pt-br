---
description: Método IShellDispatch2. IsServiceRunning – retorna um valor que indica se um serviço específico está em execução.
ms.assetid: 91f3fba1-7aa5-423a-bc37-49db230c79db
title: Método IShellDispatch2. IsServiceRunning (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.IsServiceRunning
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e8ad792f1669a8ebcfa411c58b34da214ccf69a7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117084"
---
# <a name="ishelldispatch2isservicerunning-method"></a>Método IShellDispatch2. IsServiceRunning

Retorna um valor que indica se um serviço específico está em execução.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = IShellDispatch2.IsServiceRunning(
  sServiceName
)
```


```VB

IShellDispatch2.IsServiceRunning( _
  ByVal sServiceName As BSTR _
) As Variant
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sServiceName* \[ no\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Uma **cadeia de caracteres** que contém o nome do serviço.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

### <a name="jscript"></a>JScript

Tipo: **variante \***

Retornará **true** se o serviço especificado por *sServiceName* estiver em execução; caso contrário, **false**.

### <a name="vb"></a>VB

Tipo: **variante \***

Retornará **true** se o serviço especificado por *sServiceName* estiver em execução; caso contrário, **false**.

## <a name="remarks"></a>Comentários

Esse método é implementado e acessado por meio do método [**shell. IsServiceRunning**](./shell-isservicerunning.md) .

Este método não está disponível atualmente no Microsoft Visual Basic.

## <a name="examples"></a>Exemplos

Os exemplos a seguir mostram o uso de **IsServiceRunning** para determinar se o serviço de temas está em execução para um aplicativo. O uso é mostrado para JScript e VBScript.

JScript


```JScript
<script language="JScript">
    function fnIsServiceRunningJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
    
        bReturn = objShell.IsServiceRunning("Themes");
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnIsServiceRunningVB()
        dim objShell
        dim bReturn
    
        set objShell = CreateObject("shell.application")
    
        bReturn = objShell.IsServiceRunning("Themes")
    
        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



 

 
