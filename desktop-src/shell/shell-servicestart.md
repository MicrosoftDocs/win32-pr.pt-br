---
description: Método Shell.ServiceStart – inicia um serviço nomeado.
ms.assetid: 72214E80-38A2-4a57-B555-942902BAFC3D
title: Método Shell.ServiceStart (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ServiceStart
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: afdc1e7cac8d50de08e21cfad5cb492b5b51dcb647e963b4c003e9600a924244
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709546"
---
# <a name="shellservicestart-method"></a>Método Shell.ServiceStart

Inicia um serviço nomeado.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = Shell.ServiceStart(
  sServiceName,
  vPersistent
)
```


```VB

Shell.ServiceStart( _
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

Definido como **true para** que o serviço seja iniciado automaticamente pelo gerenciador de controle de serviço durante a inicialização do sistema. De definido **como false** para deixar a configuração do serviço inalterada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

### <a name="jscript"></a>JScript

Tipo: **\* Variante**

Retornará **true se** for bem-sucedido; caso contrário, **false.**

### <a name="vb"></a>VB

Tipo: **\* Variante**

Retornará **true se** for bem-sucedido; caso contrário, **false.**

## <a name="remarks"></a>Comentários

O método **retornará false** se o serviço já tiver sido iniciado. Antes de chamar esse método, você pode chamar [**Shell.IsServiceRunning**](./shell-isservicerunning.md) para determinar o status do serviço.

Esse método não está disponível atualmente no Microsoft Visual Basic.

## <a name="examples"></a>Exemplos

Os exemplos a seguir mostram o uso de **ServiceStart** para iniciar o serviço Messenger. O uso é mostrado para JScript e VBScript.

JScript:


```JScript
<script language="JScript">
    function fnServiceStartJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStart("Messenger", true);
    }
```



Vbscript:


```VB
<script language="VBScript">
    function fnServiceStartVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ServiceStart("Messenger", true)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows aplicativos da área de \[ trabalho XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5.0 ou posterior)</dt> </dl> |



 

 
