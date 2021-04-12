---
title: UI_PKEY_ThemeColors
description: Identifica a \_ Propriedade PKEY ThemeColors da interface do usuário \_ .
ms.assetid: d539cbaa-45dc-4f9e-830e-e81fb289b4ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f5991ce5058de5a6f49ca8929de02e19657a610
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294134"
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

 

 