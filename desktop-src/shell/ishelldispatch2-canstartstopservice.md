---
description: Determina se o usuário atual pode iniciar e parar o serviço nomeado.
ms.assetid: cbb54ae9-02e6-4243-a782-e9f125c21c0d
title: Método IShellDispatch2. CanStartStopService (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.CanStartStopService
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 92655c2c561284f00204826e1848a75f00f4a04d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502081"
---
# <a name="ishelldispatch2canstartstopservice-method"></a>Método IShellDispatch2. CanStartStopService

Determina se o usuário atual pode iniciar e parar o serviço nomeado.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = IShellDispatch2.CanStartStopService(
  sServiceName
)
```


```VB

IShellDispatch2.CanStartStopService( _
  ByVal sServiceName As String _
) As Variant
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sServiceName* \[ no\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Uma **cadeia de caracteres** que contém o nome do serviço.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

### <a name="jscript"></a>JScript

Tipo: **Variant \** _

Retorna _ *true** se o usuário puder iniciar e parar o serviço; caso contrário, **false**.

### <a name="vb"></a>VB

Tipo: **Variant \** _

Retorna _ *true** se o usuário puder iniciar e parar o serviço; caso contrário, **false**.

## <a name="remarks"></a>Comentários

Esse método é implementado e acessado por meio do método [**shell. CanStartStopService**](./shell-canstartstopservice.md) .

Este método não está disponível atualmente no Microsoft Visual Basic.

## <a name="examples"></a>Exemplos

Os exemplos a seguir mostram o uso de **CanStartStopService** para JScript e VBScript.

JScript


```JScript
<script language="JScript">
    function fnCanStartStopServiceJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;

        bReturn = objShell.CanStartStopService("service name");
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnCanStartStopServiceVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.CanStartStopService("service name")

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



 

 
