---
description: Obtém o valor de uma política especificada do Windows Internet Explorer.
ms.assetid: 490c3e18-b606-456a-9016-dc4f7bad2bc3
title: Método IShellDispatch4. ExplorerPolicy (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.ExplorerPolicy
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 57247ad328c647cf9cdde32ac1a2951dd8e364ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827397"
---
# <a name="ishelldispatch4explorerpolicy-method"></a>Método IShellDispatch4. ExplorerPolicy

Obtém o valor de uma política especificada do Windows Internet Explorer.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = IShellDispatch4.ExplorerPolicy(
  bstrPolicyName
)
```


```VB

IShellDispatch4.ExplorerPolicy( _
  ByVal bstrPolicyName As BSTR _
) As Variant
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrPolicyName* \[ no\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Uma **cadeia de caracteres** que especifica o nome da política.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

### <a name="jscript"></a>JScript

Tipo: **Variant \** _

O valor associado ao nome de política especificado.

### <a name="vb"></a>VB

Tipo: _*variante \**_

O valor associado ao nome de política especificado.

## <a name="remarks"></a>Comentários

Os administradores de rede podem controlar e gerenciar o ambiente computacional de seus usuários definindo políticas.

O nome do valor especificado deve estar na subchave _ *HKEY \_ \_ **\\** software do usuário atual **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** Policies **\\** Explorer**. Se o nome do valor não existir, o método retornará **NULL**.

## <a name="examples"></a>Exemplos

Os exemplos a seguir mostram o uso apropriado de **ExplorerPolicy** para JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnIShellDispatch4ExplorerPolicyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;
        
        vReturn = objshell.ExplorerPolicy("ValueName");
        alert(vReturn);
    }
</script>
```



VBScript


```VB
<script language="VBScript">
     function fnIShellDispatch4ExplorerPolicyVB()
        dim objShell
        dim vReturn
        
        set objShell = CreateObject("shell.application")
            vReturn = objshell.ExplorerPolicy("ValueName")
            alert(vReturn)
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnIShellDispatch4ExplorerPolicyVB()
    Dim objShell As Shell
    Dim vReturn  As Variant
    
    Set objShell = New Shell
        vReturn = objshell.ExplorerPolicy("ValueName")
        Debug.Print vReturn
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                                   |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 6,0 ou posterior)</dt> </dl> |



 

 
