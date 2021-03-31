---
title: UI_PKEY_RecentColorsCategoryLabel
description: Identifica a \_ Propriedade PKEY RecentColorsCategoryLabel da interface do usuário \_ .
ms.assetid: e9336b98-59ae-4118-8535-009fc0fda4b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62bcb2e3f5df1ba66204a8df6b088ca3a2808ced
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636412"
---
# <a name="ui_pkey_recentcolorscategorylabel"></a>\_RecentColorsCategoryLabel PKEY \_ UI

Identifica a \_ Propriedade PKEY RecentColorsCategoryLabel da interface do usuário \_ .

```
propertyDescription
   name = UI_PKEY_RecentColorsCategoryLabel
   shellPKey = UI_PKEY_RecentColorsCategoryLabel
   formatID = 00000405-7363-696e-8441798acf5aebb7
   propID = 405
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Comentários

A interface do usuário \_ PKEY \_ RecentColorsCategoryLabel é usada por um aplicativo para consultar o valor do rótulo associado à categoria **cores recentes** de um [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).

A interface do usuário \_ PKEY \_ RecentColorsCategoryLabel é válida somente para um [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) em que `ThemeColors` é especificado como o valor do atributo **colortemplate** (esse é o único modelo que contém categorias rotuladas).

A captura de tela a seguir mostra um `ThemeColors`  [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).

![captura de tela do elemento dropdowncolorpicker com o atributo colortemplate definido como themecolors.](images/markup/colortemplate.themedcolors.recentcolors.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades do seletor de cores](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 




