---
title: IDXCoreAdapterList::IsStale
description: Determina se as alterações feitas neste sistema resultaram no desatualização deste objeto da lista de adaptadores DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 68b4e4ba6f3434f76ea5b4a2a98ae4e83486f61e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105793751"
---
# <a name="idxcoreadapterlistisstale-method"></a><span data-ttu-id="76a40-103">Método IDXCoreAdapterList:: isobsoleto</span><span class="sxs-lookup"><span data-stu-id="76a40-103">IDXCoreAdapterList::IsStale method</span></span>

<span data-ttu-id="76a40-104">Determina se as alterações feitas neste sistema resultaram no desatualização deste objeto da lista de adaptadores DXCore.</span><span class="sxs-lookup"><span data-stu-id="76a40-104">Determines whether changes to this system have resulted in this DXCore adapter list object becoming out of date.</span></span> <span data-ttu-id="76a40-105">Para obter diretrizes de programação e exemplos de código, consulte [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="76a40-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="76a40-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="76a40-106">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsStale() = 0;
```

## <a name="returns"></a><span data-ttu-id="76a40-107">Retornos</span><span class="sxs-lookup"><span data-stu-id="76a40-107">Returns</span></span>

<span data-ttu-id="76a40-108">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="76a40-108">Type: **bool**</span></span>

<span data-ttu-id="76a40-109">Retorna  `true`   se, desde a geração da lista, ocorreram alterações nas condições do sistema que poderiam fazer com que essa lista de adaptadores se torne obsoleta.</span><span class="sxs-lookup"><span data-stu-id="76a40-109">Returns `true` if, since generating the list, changes to system conditions have occurred that would cause this adapter list to become stale.</span></span> <span data-ttu-id="76a40-110">Caso contrário, retorna  `false` .</span><span class="sxs-lookup"><span data-stu-id="76a40-110">Otherwise, returns `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="76a40-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="76a40-111">Remarks</span></span>

<span data-ttu-id="76a40-112">Você pode sondar **isobsoleta** para determinar se as condições de alteração do sistema levaram a esta lista ficando desatualizadas.</span><span class="sxs-lookup"><span data-stu-id="76a40-112">You can poll **IsStale** to determine whether changing system conditions have led to this list becoming out of date.</span></span> <span data-ttu-id="76a40-113">Se **isobsoleto** retornar `true` uma vez, ele retornará `true` para o tempo de vida restante do objeto de lista do adaptador DXCore.</span><span class="sxs-lookup"><span data-stu-id="76a40-113">If **IsStale** returns `true` once, then it returns `true` for the remaining lifetime of the DXCore adapter list object.</span></span> <span data-ttu-id="76a40-114">Um objeto de lista obsoleto ainda é considerado obsoleto mesmo que as condições do sistema retornem a um estado que corresponda à lista (as mesmas condições obtêm-se agora como era quando a lista foi gerada pela primeira vez).</span><span class="sxs-lookup"><span data-stu-id="76a40-114">A stale list object is still considered stale even if system conditions return to a state that matches the list (the same conditions obtain now as did when the list was first generated).</span></span>

## <a name="see-also"></a><span data-ttu-id="76a40-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="76a40-115">See also</span></span>

<span data-ttu-id="76a40-116">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="76a40-116">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>