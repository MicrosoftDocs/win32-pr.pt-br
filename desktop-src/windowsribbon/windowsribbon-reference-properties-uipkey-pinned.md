---
title: UI_PKEY_Pinned
description: Identifica a \_ Propriedade fixada PKEY da interface do usuário \_ .
ms.assetid: 906b2ab9-1ed7-46a6-88bc-e8f9160ab60c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8637f11404090313751647058ee41acbad3d9bf8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160121"
---
# <a name="ui_pkey_pinned"></a>Interface do usuário \_ PKEY \_ fixada

Identifica a \_ Propriedade fixada PKEY da interface do usuário \_ .

```
propertyDescription
   name = UI_PKEY_Pinned
   shellPKey = UI_PKEY_Pinned
   formatID = 00000351-7363-696e-8441798acf5aebb7
   propID = 351
   typeInfo
      type = VT_BOOL
   booleanFormat
      formatAs = VARIANT_TRUE=-1, VARIANT_FALSE=0
```

## <a name="remarks"></a>Comentários

A interface do usuário \_ PKEY \_ fixada é usada por um aplicativo para consultar se um item no [menu do aplicativo](windowsribbon-controls-applicationmenu.md) é "fixado" ou persistente, entre instâncias do aplicativo. Por exemplo, um item na lista de itens usados mais recentemente (MRU) é acessível e não descarta a lista de itens MRU até que seja "desafixado".

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades de estado](windowsribbon-reference-properties-state.md)
</dt> <dt>

[\_RecentItems PKEY \_ UI](windowsribbon-reference-properties-uipkey-recentitems.md)
</dt> <dt>

[Itens recentes](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 




