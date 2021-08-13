---
title: UI_PKEY_RecentItems
description: Identifica a propriedade \_ PKEY \_ RecentItems da interface do usuário.
ms.assetid: 54e7ad1f-86b3-45e0-a0f4-5ee0d08e9d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04e18400f297edae1f9a1eda54bccbcd6c31c9f1d9b40408e243b6c275a83ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437952"
---
# <a name="ui_pkey_recentitems"></a>PKEY \_ \_ RecentItems da interface do usuário

Identifica a propriedade \_ PKEY \_ RecentItems da interface do usuário.

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

[Interface do usuário \_ PKEY \_ Fixado](windowsribbon-reference-properties-uipkey-pinned.md) é usado por um aplicativo para consultar a matriz de itens na coleção de itens usados mais recentemente (MRU) do [Menu do Aplicativo](windowsribbon-controls-applicationmenu.md). As informações de cada item MRU são encapsuladas em um objeto [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) e incluem as três chaves de propriedade a seguir:

-   [Rótulo \_ PKEY da interface do \_ usuário](windowsribbon-reference-properties-uipkey-label.md)
-   [IU \_ PKEY \_ LabelDescription](windowsribbon-reference-properties-uipkey-labeldescription.md)
-   [PKEY \_ da interface do usuário \_ fixada](windowsribbon-reference-properties-uipkey-pinned.md)

A lista de itens do MRU é passada para o aplicativo host da Faixa de Opções como **uma SAFEARRAY** de [**ponteiros IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) para as respectivas implementações no aplicativo host.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades de estado](windowsribbon-reference-properties-state.md)
</dt> </dl>

 

 