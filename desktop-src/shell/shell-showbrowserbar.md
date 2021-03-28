---
description: Exibe uma barra de navegador.
ms.assetid: 203636D2-54D3-4163-B9AC-39213D6F4203
title: Método Shell. ShowBrowserBar (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ShowBrowserBar
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d112399e62825714b4c060aeddcb8618ff73d478
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967952"
---
# <a name="shellshowbrowserbar-method"></a>Método Shell. ShowBrowserBar

Exibe uma barra de navegador.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = Shell.ShowBrowserBar(
  sCLSID,
  vShow
)
```


```VB

Shell.ShowBrowserBar( _
  ByVal sCLSID As BSTR, _
  ByVal vShow As Variant _
) As Variant
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sCLSID* \[ no\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Uma **cadeia de caracteres** que contém a forma de cadeia de caracteres do CLSID da barra do navegador a ser exibida. O objeto deve ser registrado como um objeto de barra do Explorer com uma \_ categoria de componente InfoBand de CATID. Para obter mais informações, consulte [Criando barras personalizadas do Explorer, faixas de ferramentas e faixas de escrivaninha](band-objects.md).

</dd> <dt>

*vShow* \[ no\]
</dt> <dd>

Tipo: **variante**

Defina como **true** para mostrar a barra de navegador ou **false** para ocultá-la.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

### <a name="jscript"></a>JScript

Tipo: **Variant \** _

Retorna _ *true** se for bem-sucedido; caso contrário, **false**.

### <a name="vb"></a>VB

Tipo: **Variant \** _

Retorna _ *true** se for bem-sucedido; caso contrário, **false**.

## <a name="remarks"></a>Comentários

Você pode exibir uma das barras padrão do Explorer definindo o parâmetro *sCLSID* como o CLSID da barra do Gerenciador. As barras padrão do Explorer e suas cadeias de caracteres CLSID são as seguintes:



| Barra do Explorer | Cadeia de caracteres CLSID                           |
|--------------|----------------------------------------|
| Favoritos    | {EFA24E61-B078-11d0-89E4-00C04FC9E26E} |
| Pastas      | {EFA24E64-B078-11d0-89E4-00C04FC9E26E} |
| Histórico      | {EFA24E62-B078-11d0-89E4-00C04FC9E26E} |
| Pesquisar       | {30D02401-6A81-11d0-8274-00C04FD5AE38} |



 

Este método não está disponível atualmente no Microsoft Visual Basic.

## <a name="examples"></a>Exemplos

Os exemplos a seguir mostram o uso de **shell. ShowBrowserBar** para exibir a barra de navegador de **favoritos** . O uso é mostrado para JScript e VBScript.

JScript


```JScript
<script language="JavaScript">
    function fnShowBrowserBarJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ShowBrowserBar("{EFA24E61-B078-11d0-89E4-00C04FC9E26E}", true);
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShowBrowserBarVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ShowBrowserBar("{EFA24E61-B078-11d0-89E4-00C04FC9E26E}", true)

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



 

 
