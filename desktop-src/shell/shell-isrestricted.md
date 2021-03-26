---
description: Recupera a configuração de restrição de um grupo do registro.
ms.assetid: C4B3B5C0-7445-483a-885F-5283BD4D4B39
title: Método Shell. IsRestricted (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.IsRestricted
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 2224a3ea4ea26cf39f2e15486de4f96afe5448d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170091"
---
# <a name="shellisrestricted-method"></a>Método de Shell. IsRestricted

Recupera a configuração de restrição de um grupo do registro.

## <a name="syntax"></a>Sintaxe


```JScript
iRetVal = Shell.IsRestricted(
  sGroup,
  sRestriction
)
```


```VB

Shell.IsRestricted( _
  ByVal sGroup As BSTR, _
  ByVal sRestriction As BSTR _
) As Integer
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sGroup* \[ no\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Uma **cadeia de caracteres** que contém o nome do grupo. Esse valor é o nome de uma subchave do registro sob a qual verificar a restrição.

</dd> <dt>

*sRestriction* \[ no\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Uma **cadeia de caracteres** que contém a restrição cujo valor deve ser recuperado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

### <a name="jscript"></a>JScript

Tipo: **inteiro \** _

O valor da restrição. Se a restrição especificada não for encontrada, o valor de retorno será 0.

### <a name="vb"></a>VB

Tipo: _*inteiro \**_

O valor da restrição. Se a restrição especificada não for encontrada, o valor de retorno será 0.

## <a name="remarks"></a>Comentários

_ *IsRestricted** primeiro procura um nome de subchave que corresponda a *sGroup* sob a chave a seguir.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
```

As restrições são declaradas como valores das subchaves de política individuais. Se a restrição nomeada em *sRestriction* for encontrada na subchave nomeada em *SGroup*, **IsRestricted** retornará o valor atual da restrição. Se a restrição não for encontrada em **HKEY \_ local \_ Machine**, a mesma subchave será verificada em **HKEY \_ Current \_ User**.

Este método não está disponível atualmente no Microsoft Visual Basic.

## <a name="examples"></a>Exemplos

Os exemplos a seguir mostram o uso de **IsRestricted** para recuperar o valor de dados da restrição **undockwithoutlogon** da subchave do **sistema** . O uso é mostrado para JScript e VBScript.

JScript


```JScript
<script language="JScript">
    function fnIsRestricedJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var lReturn;
        
        lReturn = objShell.IsRestricted("system", "undockwithoutlogon");
        document.write(lReturn);
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnIsRestricedVB()
        dim objShell
        dim lReturn

        set objShell = CreateObject("shell.application")

        lReturn = objShell.IsRestricted("system", "undockwithoutlogon")
        document.write(lReturn)

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



 

 
