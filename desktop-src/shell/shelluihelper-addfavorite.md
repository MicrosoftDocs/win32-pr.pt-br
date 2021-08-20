---
description: Exibe a interface do usuário padrão para criar um item favorito. A interface do usuário é inicializada para os parâmetros especificados.
title: Método ShellUIHelper.AddFavorite (Exdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddFavorite
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b30e776e-642c-4599-b83f-ef15bc0b23d2
ms.openlocfilehash: f106b9860dcfa87cad9a69763731b47aeb4f9b0c7d4698f72dfc7210498e9234
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117676617"
---
# <a name="shelluihelperaddfavorite-method"></a>Método ShellUIHelper.AddFavorite

Exibe a interface do usuário padrão para criar um item favorito. A interface do usuário é inicializada para os parâmetros especificados.

## <a name="syntax"></a>Sintaxe


```JScript
iRetVal = ShellUIHelper.AddFavorite(
  sURL,
  [ vTitle ]
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sURL* \[ Em\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Um **valor string** que especifica a URL do item a ser adicionado à pasta **Favoritos.**

</dd> <dt>

*vTitle* \[ in, opcional\]
</dt> <dd>

Tipo: **\* Variante**

Um **valor** Variant que especifica o nome do item.

</dd> </dl>

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra o uso adequado desse método para JScript inserido em HTML e Visual Basic.

JScript:


```JScript
<html>
<head>
<title></title>

<object id="ShellUIHelper"
        classid="CLSID:64AB4BB7-111E-11d1-8F79-00C04FC2FBE1"
        width=0
        height=0
        VIEWASTEXT>
</object>

<script language="JavaScript">
    function fnShellUIHelperAddFavoriteJ()
    {
        ShellUIHelper.AddFavorite("https://www.msn.com", "MSN Home Page");
    }
</script>

</head>
<body onload=fnShellUIHelperAddFavoriteJ()>
</body>
</html>
```



Visual Basic:


```VB
Private Sub fnShellUIHelperAddFavoriteVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddFavorite "https://www.msn.com", "MSN Home Page"
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows somente aplicativos da \[ área de trabalho XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Exdisp.h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4.71 ou posterior)</dt> </dl> |



 

 
