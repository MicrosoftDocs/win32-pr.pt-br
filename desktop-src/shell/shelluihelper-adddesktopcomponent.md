---
description: Adiciona um item ao microsoft Active Desktop.
title: Método ShellUIHelper.AddDesktopComponent (Exdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddDesktopComponent
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 41634a89-15b9-41c8-ba3f-4bf19b786f6f
ms.openlocfilehash: 5141b35b9fb71b09b9b269016d0b38cdb0b9f01ec88a02070a0f936934159930
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941496"
---
# <a name="shelluihelperadddesktopcomponent-method"></a>Método ShellUIHelper.AddDesktopComponent

Adiciona um item ao microsoft Active Desktop.

## <a name="syntax"></a>Sintaxe


```JScript
iRetVal = ShellUIHelper.AddDesktopComponent(
  sURL,
  sType,
  [ Left ],
  [ Top ],
  [ Width ],
  [ Height ]
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sURL* \[ Em\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Um **valor string** que especifica a URL do novo item favorito.

</dd> <dt>

*sType* \[ Em\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Um **valor string** que especifica o tipo de item que está sendo adicionado. Esse pode ser um dos valores a seguir.

<dt>



 (imagem)


</dt> <dd>

O componente é uma imagem.

</dd> <dt>



 (site)


</dt> <dd>

O componente é um site.

</dd> </dl> </dd> <dt>

*Esquerda* \[ in, opcional\]
</dt> <dd>

Tipo: **Variante**

A posição da borda esquerda do componente, em coordenadas de tela.

</dd> <dt>

*Superior* \[ in, opcional\]
</dt> <dd>

Tipo: **Variante**

A posição da borda superior do componente, em coordenadas de tela.

</dd> <dt>

*Largura* \[ in, opcional\]
</dt> <dd>

Tipo: **Variante**

A largura do componente, em unidades de tela.

</dd> <dt>

*Altura* \[ in, opcional\]
</dt> <dd>

Tipo: **Variante**

A altura do componente, em unidades de tela.

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
    function fnShellUIHelperAddDesktopComponentJ()
    {
        ShellUIHelper.AddDesktopComponent("https://www.microsoft.com/", "website");
    }
</script>

</head>
<body onload=fnShellUIHelperAddDesktopComponentJ()>
</body>
</html>
```



Visual Basic:


```VB
Private Sub fnShellUIHelperAddDesktopComponentVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddDesktopComponent "https://www.microsoft.com/", "website"
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows aplicativos da área de \[ trabalho XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Exdisp.h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4.71 ou posterior)</dt> </dl> |



 

 
