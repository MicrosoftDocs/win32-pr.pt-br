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
# <a name="ui_pkey_pinned"></a><span data-ttu-id="118aa-103">Interface do usuário \_ PKEY \_ fixada</span><span class="sxs-lookup"><span data-stu-id="118aa-103">UI\_PKEY\_Pinned</span></span>

<span data-ttu-id="118aa-104">Identifica a \_ Propriedade fixada PKEY da interface do usuário \_ .</span><span class="sxs-lookup"><span data-stu-id="118aa-104">Identifies the UI\_PKEY\_Pinned property.</span></span>

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

## <a name="remarks"></a><span data-ttu-id="118aa-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="118aa-105">Remarks</span></span>

<span data-ttu-id="118aa-106">A interface do usuário \_ PKEY \_ fixada é usada por um aplicativo para consultar se um item no [menu do aplicativo](windowsribbon-controls-applicationmenu.md) é "fixado" ou persistente, entre instâncias do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="118aa-106">UI\_PKEY\_Pinned is used by an application to query whether an item in the [Application Menu](windowsribbon-controls-applicationmenu.md) is "pinned", or persistent, across application instances.</span></span> <span data-ttu-id="118aa-107">Por exemplo, um item na lista de itens usados mais recentemente (MRU) é acessível e não descarta a lista de itens MRU até que seja "desafixado".</span><span class="sxs-lookup"><span data-stu-id="118aa-107">For example, an item in the most recently used (MRU) items list is accessible and does not drop off the MRU items list until it is "unpinned".</span></span>

## <a name="related-topics"></a><span data-ttu-id="118aa-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="118aa-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="118aa-109">Propriedades de estado</span><span class="sxs-lookup"><span data-stu-id="118aa-109">State Properties</span></span>](windowsribbon-reference-properties-state.md)
</dt> <dt>

[<span data-ttu-id="118aa-110">\_RecentItems PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="118aa-110">UI\_PKEY\_RecentItems</span></span>](windowsribbon-reference-properties-uipkey-recentitems.md)
</dt> <dt>

[<span data-ttu-id="118aa-111">Itens recentes</span><span class="sxs-lookup"><span data-stu-id="118aa-111">Recent Items</span></span>](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 




