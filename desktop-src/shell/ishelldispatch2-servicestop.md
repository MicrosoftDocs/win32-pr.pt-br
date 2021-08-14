---
description: Método IShellDispatch2.ServiceStop – interrompe um serviço nomeado.
ms.assetid: f4cd0e2c-4ecc-4e9f-a0b5-d2a8a739f0e2
title: Método IShellDispatch2.ServiceStop (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ServiceStop
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 71bc0502d45e4092decfe1b712ed11f75a02bf50d112436ad1d21f9e02c17e72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118221017"
---
# <a name="ishelldispatch2servicestop-method"></a>Método IShellDispatch2.ServiceStop

Interrompe um serviço nomeado.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = IShellDispatch2.ServiceStop(
  sServiceName,
  vPersistent
)
```


```VB

IShellDispatch2.ServiceStop( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sServiceName* \[ Em\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Uma **Cadeia de** caracteres que contém o nome do serviço.

</dd> <dt>

*vPersistent* \[ Em\]
</dt> <dd>

Tipo: **Variante**

Definido como **true** para que o serviço seja iniciado pelo gerenciador de controle de serviço [**quando ServiceStart**](ishelldispatch2-servicestart.md) for chamado. Para deixar a configuração do serviço inalterada, de *acordo com vPersistent* como **false.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

### <a name="jscript"></a>JScript

Tipo: **\* Variante**

Retornará **true se** for bem-sucedido; caso contrário, **false.**

### <a name="vb"></a>VB

Tipo: **\* Variante**

Retornará **true se** for bem-sucedido; caso contrário, **false.**

## <a name="remarks"></a>Comentários

Esse método é implementado e acessado por meio do [**método Shell.ServiceStop.**](./shell-servicestop.md)

O método **retornará false** se o serviço já tiver sido interrompido. Antes de chamar esse método, você pode chamar [**Shell.IsServiceRunning**](./shell-isservicerunning.md) para determinar o status do serviço.

Esse método não está disponível atualmente no Microsoft Visual Basic.

## <a name="examples"></a>Exemplos

Os exemplos a seguir mostram o uso de **ServiceStop** para interromper o serviço Messenger. O uso é mostrado para JScript e VBScript.

JScript:


```JScript
<script language="JScript">
    function fnServiceStopJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStop("Messenger", true);
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnServiceStopVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ServiceStop("Messenger", true)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows aplicativos da área de \[ trabalho XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5.0 ou posterior)</dt> </dl> |



 

 
