---
title: UI_PKEY_RecentItems
description: Identifica a \_ Propriedade PKEY RecentItems da interface do usuário \_ .
ms.assetid: 54e7ad1f-86b3-45e0-a0f4-5ee0d08e9d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a07410d3152fb49b55460ec15c6914c53f3b6850
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105815586"
---
# <a name="ui_pkey_recentitems"></a>\_RecentItems PKEY \_ UI

Identifica a \_ Propriedade PKEY RecentItems da interface do usuário \_ .

```
propertyDescription
   name = UI_PKEY_RecentItems
   shellPKey = UI_PKEY_RecentItems
   formatID = 00000350-7363-696e-8441798acf5aebb7
   propID = 350
   typeInfo
      type = VT_ARRAY | VT_UNKNOWN
```

## <a name="remarks"></a>Comentários

[Interface do usuário \_ PKEY \_ fixado](windowsribbon-reference-properties-uipkey-pinned.md) é usado por um aplicativo para consultar a matriz de itens na coleção de itens usados mais recentemente (MRU) do [menu do aplicativo](windowsribbon-controls-applicationmenu.md). As informações para cada item MRU são encapsuladas em um objeto [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) e incluem as três seguintes chaves de propriedade:

-   [\_Rótulo de PKEY da interface do usuário \_](windowsribbon-reference-properties-uipkey-label.md)
-   [\_LabelDescription PKEY \_ UI](windowsribbon-reference-properties-uipkey-labeldescription.md)
-   [Interface do usuário \_ PKEY \_ fixada](windowsribbon-reference-properties-uipkey-pinned.md)

A lista de itens MRU é passada para o aplicativo host da faixa de lista como um **SafeArray** de ponteiros [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) para as respectivas implementações no aplicativo host.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades de estado](windowsribbon-reference-properties-state.md)
</dt> </dl>

 

 