---
description: Adiciona um item ao Microsoft Active Desktop.
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
ms.openlocfilehash: 2edaa79bd62dcee40e4f197700d2128cb0b2070d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842457"
---
# <a name="shelluihelperadddesktopcomponent-method"></a>Método ShellUIHelper.AddDesktopComponent

Adiciona um item ao Microsoft Active Desktop.

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

A posição da borda superior do componente, em coordenadas da tela.

</dd> <dt>

*Largura* \[ em, opcional\]
</dt> <dd>

Tipo: **variante**

A largura do componente, em unidades da tela.

</dd> <dt>

*Altura* \[ em, opcional\]
</dt> <dd>

Tipo: **variante**

A altura do componente, em unidades da tela.

</dd> </dl>

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra o uso correto desse método para JScript Embedded em HTML e Visual Basic.

JScript


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
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>O textdisp. h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4,71 ou posterior)</dt> </dl> |



 

 
