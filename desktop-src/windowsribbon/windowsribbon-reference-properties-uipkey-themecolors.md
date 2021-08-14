---
title: UI_PKEY_ThemeColors
description: Identifica a \_ Propriedade PKEY ThemeColors da interface do usuário \_ .
ms.assetid: d539cbaa-45dc-4f9e-830e-e81fb289b4ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab5c4582561e3c86ba19b2821cf600d0a1da614cfc9fc7144b935665c8af7f14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437791"
---
# <a name="ui_pkey_themecolors"></a>\_ThemeColors PKEY \_ UI

Identifica a \_ Propriedade PKEY ThemeColors da interface do usuário \_ .

```
propertyDescription
   name = UI_PKEY_ThemeColors
   shellPKey = UI_PKEY_ThemeColors
   formatID = 00000409-7363-696e-8441798acf5aebb7
   propID = 409
   typeInfo
      type = VT_VECTOR | VT_UI4
```

## <a name="remarks"></a>Comentários

A interface do usuário \_ PKEY \_ ThemeColors é usada por um aplicativo para consultar os valores de amostra de cor de um [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).

Cada valor de [COLORREF](../gdi/colorref.md) corresponde a uma amostra de cor em um [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) em que `ThemeColors` é especificado como o valor do atributo **colortemplate** .

O valor da propriedade é uma matriz de valores [COLORREF](../gdi/colorref.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades do seletor de cores](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 