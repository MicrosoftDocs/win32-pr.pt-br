---
title: UI_PKEY_StandardColors
description: Identifica a \_ Propriedade PKEY StandardColors da interface do usuário \_ .
ms.assetid: fbdce7ba-4417-4f7f-928b-fba6af6eb396
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2dd46462e9a123b0a8c64c3fd06fdfbc6ccbe3aa35274505dc4722dd2a40e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117850067"
---
# <a name="ui_pkey_standardcolors"></a>\_StandardColors PKEY \_ UI

Identifica a \_ Propriedade PKEY StandardColors da interface do usuário \_ .

```
propertyDescription
   name = UI_PKEY_StandardColors
   shellPKey = UI_PKEY_StandardColors
   formatID = 00000410-7363-696e-8441798acf5aebb7
   propID = 410
   typeInfo
      type = VT_VECTOR | VT_UI4
```

## <a name="remarks"></a>Comentários

A interface do usuário \_ PKEY \_ StandardColors é usada por um aplicativo para consultar os valores de amostra de cor de um [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).

Cada valor de [COLORREF](../gdi/colorref.md) corresponde a uma amostra de cor em um [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) , independentemente do valor especificado para o atributo **colortemplate** .

O valor da propriedade é uma matriz de valores [COLORREF](../gdi/colorref.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades do seletor de cores](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 