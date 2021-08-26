---
description: Método Shell.ShowBrowserBar – exibe uma barra de navegador.
ms.assetid: 203636D2-54D3-4163-B9AC-39213D6F4203
title: Método Shell.ShowBrowserBar (Shldisp.h)
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
ms.openlocfilehash: 21bafde8c148ea8249672dd26a244dec152ed0e9fc5ce5fbb769e5cae6c92b74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008886"
---
# <a name="shellshowbrowserbar-method"></a>Método Shell.ShowBrowserBar

Exibe uma barra do navegador.

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

*sCLSID* \[ Em\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Uma **Cadeia de** caracteres que contém a forma de cadeia de caracteres do CLSID da barra do navegador a ser exibida. O objeto deve ser registrado como um objeto Da Barra do Explorer com uma categoria de componente \_ INFOBand CATID. Para obter mais informações, consulte [Criando barras personalizadas do Explorer, faixas de ferramentas e bandas de mesa.](band-objects.md)

</dd> <dt>

*vShow* \[ Em\]
</dt> <dd>

Tipo: **Variante**

De definido **como true** para mostrar a barra do navegador ou **false para** o ocultar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

### <a name="jscript"></a>JScript

Tipo: **\* Variante**

Retornará **true se** for bem-sucedido; caso contrário, **false.**

### <a name="vb"></a>VB

Tipo: **\* Variante**

Retornará **true se** for bem-sucedido; caso contrário, **false.**

## <a name="remarks"></a>Comentários

Você pode exibir uma das Barras do Explorer padrão definindo o parâmetro *sCLSID* como o CLSID dessa Barra do Explorer. As barras padrão do Explorer e suas cadeias de caracteres CLSID são as seguinte:



| Barra do Explorer | Cadeia de caracteres CLSID                           |
|--------------|----------------------------------------|
| Favoritos    | {EFA24E61-B078-11d0-89E4-00C04FC9E26E} |
| Pastas      | {EFA24E64-B078-11d0-89E4-00C04FC9E26E} |
| Histórico      | {EFA24E62-B078-11d0-89E4-00C04FC9E26E} |
| Search       | {30D02401-6A81-11d0-8274-00C04FD5AE38} |



 

Esse método não está disponível atualmente no Microsoft Visual Basic.

## <a name="examples"></a>Exemplos

Os exemplos a seguir mostram o uso **de Shell.ShowBrowserBar** para exibir a barra do navegador **Favoritos.** O uso é mostrado para JScript e VBScript.

JScript:


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



Vbscript:


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
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows aplicativos da área de \[ trabalho XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5.0 ou posterior)</dt> </dl> |



 

 
