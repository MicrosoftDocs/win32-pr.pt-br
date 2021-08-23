---
description: Método IShellDispatch2. CanStartStopService – determina se o usuário atual pode iniciar e parar o serviço nomeado.
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
ms.openlocfilehash: bae0ed1a6f60a363a360c8824d5b41f17b89f9040d3354b9e3011e0269e9d9e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032234"
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

## <a name="return-value"></a>Valor retornado

### <a name="jscript"></a>JScript

Tipo: **variante \***

Retornará **true** se o usuário puder iniciar e parar o serviço; caso contrário, **false**.

### <a name="vb"></a>VB

Tipo: **variante \***

Retornará **true** se o usuário puder iniciar e parar o serviço; caso contrário, **false**.

## <a name="remarks"></a>Comentários

Esse método é implementado e acessado por meio do método [**shell. CanStartStopService**](./shell-canstartstopservice.md) .

Este método não está disponível atualmente no Microsoft Visual Basic.

## <a name="examples"></a>Exemplos

os exemplos a seguir mostram o uso de **CanStartStopService** para JScript e VBScript.

JScript:


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
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos de área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



 

 
