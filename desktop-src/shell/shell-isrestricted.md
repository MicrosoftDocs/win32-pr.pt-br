---
description: Método Shell. IsRestricted-recupera a configuração de restrição de um grupo do registro.
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
ms.openlocfilehash: 40e6c23f14b3c09a6cfe4885cc7b7bf877e3e4bfbf538645cf96b99ea451776f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968545"
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

## <a name="return-value"></a>Valor retornado

### <a name="jscript"></a>JScript

Tipo: **inteiro \***

O valor da restrição. Se a restrição especificada não for encontrada, o valor de retorno será 0.

### <a name="vb"></a>VB

Tipo: **inteiro \***

O valor da restrição. Se a restrição especificada não for encontrada, o valor de retorno será 0.

## <a name="remarks"></a>Comentários

**IsRestricted** primeiro procura por um nome de subchave que corresponda a *sGroup* sob a chave a seguir.

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

Os exemplos a seguir mostram o uso de **IsRestricted** para recuperar o valor de dados da restrição **undockwithoutlogon** da subchave do **sistema** . o uso é mostrado para JScript e VBScript.

JScript:


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
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos de área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



 

 
