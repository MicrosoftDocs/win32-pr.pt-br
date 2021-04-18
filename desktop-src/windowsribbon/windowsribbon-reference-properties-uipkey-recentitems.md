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
# <a name="ui_pkey_recentitems"></a><span data-ttu-id="e274c-103">\_RecentItems PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="e274c-103">UI\_PKEY\_RecentItems</span></span>

<span data-ttu-id="e274c-104">Identifica a \_ Propriedade PKEY RecentItems da interface do usuário \_ .</span><span class="sxs-lookup"><span data-stu-id="e274c-104">Identifies the UI\_PKEY\_RecentItems property.</span></span>

```
propertyDescription
   name = UI_PKEY_RecentItems
   shellPKey = UI_PKEY_RecentItems
   formatID = 00000350-7363-696e-8441798acf5aebb7
   propID = 350
   typeInfo
      type = VT_ARRAY | VT_UNKNOWN
```

## <a name="remarks"></a><span data-ttu-id="e274c-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="e274c-105">Remarks</span></span>

<span data-ttu-id="e274c-106">[Interface do usuário \_ PKEY \_ fixado](windowsribbon-reference-properties-uipkey-pinned.md) é usado por um aplicativo para consultar a matriz de itens na coleção de itens usados mais recentemente (MRU) do [menu do aplicativo](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="e274c-106">[UI\_PKEY\_Pinned](windowsribbon-reference-properties-uipkey-pinned.md) is used by an application to query the array of items in the most recently used (MRU) items collection of the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span> <span data-ttu-id="e274c-107">As informações para cada item MRU são encapsuladas em um objeto [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) e incluem as três seguintes chaves de propriedade:</span><span class="sxs-lookup"><span data-stu-id="e274c-107">The information for each MRU item is encapsulated in an [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) object and includes the following three property keys:</span></span>

-   [<span data-ttu-id="e274c-108">\_Rótulo de PKEY da interface do usuário \_</span><span class="sxs-lookup"><span data-stu-id="e274c-108">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)
-   [<span data-ttu-id="e274c-109">\_LabelDescription PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="e274c-109">UI\_PKEY\_LabelDescription</span></span>](windowsribbon-reference-properties-uipkey-labeldescription.md)
-   [<span data-ttu-id="e274c-110">Interface do usuário \_ PKEY \_ fixada</span><span class="sxs-lookup"><span data-stu-id="e274c-110">UI\_PKEY\_Pinned</span></span>](windowsribbon-reference-properties-uipkey-pinned.md)

<span data-ttu-id="e274c-111">A lista de itens MRU é passada para o aplicativo host da faixa de lista como um **SafeArray** de ponteiros [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) para as respectivas implementações no aplicativo host.</span><span class="sxs-lookup"><span data-stu-id="e274c-111">The list of MRU items is passed to the Ribbon host application as a **SAFEARRAY** of [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) pointers to respective implementations in the host application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e274c-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e274c-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e274c-113">Propriedades de estado</span><span class="sxs-lookup"><span data-stu-id="e274c-113">State Properties</span></span>](windowsribbon-reference-properties-state.md)
</dt> </dl>

 

 