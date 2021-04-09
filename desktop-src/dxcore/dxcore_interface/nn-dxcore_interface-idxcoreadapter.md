---
title: IDXCoreAdapter
description: A interface **IDXCoreAdapter**   implementa métodos para recuperar detalhes sobre um item de adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 0930ce76353d556f7839f476ec8979823eac3a6c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084820"
---
# <a name="idxcoreadapter-interface"></a><span data-ttu-id="e7e5b-103">Interface IDXCoreAdapter</span><span class="sxs-lookup"><span data-stu-id="e7e5b-103">IDXCoreAdapter interface</span></span>

<span data-ttu-id="e7e5b-104">A interface **IDXCoreAdapter**   implementa métodos para recuperar detalhes sobre um item de adaptador.</span><span class="sxs-lookup"><span data-stu-id="e7e5b-104">The **IDXCoreAdapter** interface implements methods for retrieving details about an adapter item.</span></span> <span data-ttu-id="e7e5b-105">**IDXCoreAdapter** herda da interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e7e5b-105">**IDXCoreAdapter** inherits from the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e7e5b-106">Para obter diretrizes de programação e exemplos de código, consulte [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="e7e5b-106">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e7e5b-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7e5b-107">Remarks</span></span>

<span data-ttu-id="e7e5b-108">As propriedades de um adaptador são estabelecidas no momento em que o adaptador é iniciado e são imutáveis durante o tempo de vida do adaptador.</span><span class="sxs-lookup"><span data-stu-id="e7e5b-108">An adapter's properties are established at the time the adapter starts, and they're immutable for the lifetime of the adapter.</span></span> <span data-ttu-id="e7e5b-109">Isso é diferente do estado de um adaptador, que pode ser consultado ou definido, e os valores que podem ser alterados ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="e7e5b-109">This is in contrast to an adapter's state, which can be queried or set, and the values of which can change over time.</span></span>

## <a name="see-also"></a><span data-ttu-id="e7e5b-110">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7e5b-110">See also</span></span>

<span data-ttu-id="e7e5b-111">[Referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="e7e5b-111">[DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>