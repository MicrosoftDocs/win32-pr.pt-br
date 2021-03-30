---
description: Adiciona um item ao Microsoft Active Desktop.
title: Método ShellUIHelper. AddDesktopComponent (exdisp. h)
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
ms.openlocfilehash: d5234a0b43ea25c8ac931dc14ec90f7a6696ddfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968160"
---
# <a name="shelluihelperadddesktopcomponent-method"></a>Método ShellUIHelper. AddDesktopComponent

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

*sUrl* \[ no\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Um valor de **cadeia de caracteres** que especifica a URL do novo item favorito.

</dd> <dt>

*stype* \[ no\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Um valor de **cadeia de caracteres** que especifica o tipo de item que está sendo adicionado. Isso pode ser um dos valores a seguir.

<dt>



 imagem


</dt> <dd>

O componente é uma imagem.

</dd> <dt>



 site


</dt> <dd>

O componente é um site.

</dd> </dl> </dd> <dt>

*À esquerda* \[ em, opcional\]
</dt> <dd>

Tipo: **variante**

A posição da borda esquerda do componente, em coordenadas da tela.

</dd> <dt>

*Superior* \[ em, opcional\]
</dt> <dd>

Tipo: **variante**

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



 

 
