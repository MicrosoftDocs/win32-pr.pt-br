---
title: Interfaces duplas (COM)
description: Interfaces duplas
ms.assetid: 6e4dc529-8a25-4ae5-b868-28cb17e0db52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da95c77a307c40721b909eceb1e6d29bab23bc14
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008476"
---
# <a name="dual-interfaces"></a><span data-ttu-id="179c7-103">Interfaces duplas</span><span class="sxs-lookup"><span data-stu-id="179c7-103">Dual Interfaces</span></span>

<span data-ttu-id="179c7-104">A automação OLE permite que um objeto exponha um conjunto de métodos de duas maneiras: por meio da interface **IDispatch** e por meio da associação direta de OLE vtable.</span><span class="sxs-lookup"><span data-stu-id="179c7-104">OLE Automation enables an object to expose a set of methods in two ways: via the **IDispatch** interface, and through direct OLE VTable binding.</span></span> <span data-ttu-id="179c7-105">O **IDispatch** é usado pela maioria das ferramentas disponíveis hoje e oferece suporte para associação tardia a propriedades e métodos.</span><span class="sxs-lookup"><span data-stu-id="179c7-105">**IDispatch** is used by most tools available today, and offers support for late binding to properties and methods.</span></span>

<span data-ttu-id="179c7-106">A associação VTable oferece um desempenho muito maior porque esse método é chamado diretamente, em vez de **IDispatch:: Invoke**.</span><span class="sxs-lookup"><span data-stu-id="179c7-106">VTable binding offers much higher performance because this method is called directly instead of through **IDispatch::Invoke**.</span></span> <span data-ttu-id="179c7-107">O **IDispatch** oferece suporte de associação tardia, em que a ligação Direct vtable oferece um lucro significativo de desempenho; ambas as técnicas são valiosas e importantes em cenários diferentes.</span><span class="sxs-lookup"><span data-stu-id="179c7-107">**IDispatch** offers late bound support, where direct VTable binding offers a significant performance gain; both techniques are valuable and important in different scenarios.</span></span> <span data-ttu-id="179c7-108">Ao rotular uma interface como \[ [**dupla**](/windows/desktop/Midl/dual) \] na biblioteca de tipos, uma interface de automação OLE pode ser usada por meio de **IDispatch** ou pode ser associada diretamente.</span><span class="sxs-lookup"><span data-stu-id="179c7-108">By labeling an interface as \[[**dual**](/windows/desktop/Midl/dual)\] in the type library, an OLE Automation interface can be used either via **IDispatch**, or it can be bound to directly.</span></span> <span data-ttu-id="179c7-109">Os contêineres podem, portanto, escolher a técnica mais apropriada.</span><span class="sxs-lookup"><span data-stu-id="179c7-109">Containers can thus choose the most appropriate technique.</span></span> <span data-ttu-id="179c7-110">O suporte para interfaces duplas é altamente recomendável para controles e contêineres.</span><span class="sxs-lookup"><span data-stu-id="179c7-110">Support for dual interfaces is strongly recommended for both controls and containers.</span></span>

 

 