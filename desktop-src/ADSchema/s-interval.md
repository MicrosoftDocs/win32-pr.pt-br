---
title: Sintaxe de intervalo
description: Representa um valor de intervalo de tempo.
ms.assetid: e41b71da-cd05-4a4a-8b97-9210dbe314de
ms.tgt_platform: multiple
keywords:
- Esquema de sintaxe do intervalo do AD
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59b92961deecde7faa879dbbda6bfd24560ad705
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104369946"
---
# <a name="interval-syntax"></a><span data-ttu-id="9bb50-104">Sintaxe de intervalo</span><span class="sxs-lookup"><span data-stu-id="9bb50-104">Interval syntax</span></span>

<span data-ttu-id="9bb50-105">Representa um valor de intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="9bb50-105">Represents a time interval value.</span></span> <span data-ttu-id="9bb50-106">As unidades de tempo reais dependem de qual atributo está usando essa sintaxe.</span><span class="sxs-lookup"><span data-stu-id="9bb50-106">The actual time units depend on which attribute is using this syntax.</span></span> <span data-ttu-id="9bb50-107">Essa sintaxe é idêntica à sintaxe [**LargeInteger**](s-largeinteger.md) , exceto que os valores alto e baixo são inteiros sem sinal.</span><span class="sxs-lookup"><span data-stu-id="9bb50-107">This syntax is identical to the [**LargeInteger**](s-largeinteger.md) syntax, except the high and low values are unsigned integers.</span></span>



| <span data-ttu-id="9bb50-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="9bb50-108">Entry</span></span> | <span data-ttu-id="9bb50-109">Valor</span><span class="sxs-lookup"><span data-stu-id="9bb50-109">Value</span></span> |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9bb50-110">Nome</span><span class="sxs-lookup"><span data-stu-id="9bb50-110">Name</span></span>         | <span data-ttu-id="9bb50-111">Intervalo</span><span class="sxs-lookup"><span data-stu-id="9bb50-111">Interval</span></span>                                                                           |
| <span data-ttu-id="9bb50-112">ID da sintaxe</span><span class="sxs-lookup"><span data-stu-id="9bb50-112">Syntax ID</span></span>    | <span data-ttu-id="9bb50-113">2.5.5.16</span><span class="sxs-lookup"><span data-stu-id="9bb50-113">2.5.5.16</span></span>                                                                           |
| <span data-ttu-id="9bb50-114">ID DO OM</span><span class="sxs-lookup"><span data-stu-id="9bb50-114">OM ID</span></span>        | <span data-ttu-id="9bb50-115">65</span><span class="sxs-lookup"><span data-stu-id="9bb50-115">65</span></span>                                                                                 |
| <span data-ttu-id="9bb50-116">Tipo de MAPI</span><span class="sxs-lookup"><span data-stu-id="9bb50-116">MAPI Type</span></span>    | \-                                                                                 |
| <span data-ttu-id="9bb50-117">Tipo de ADS</span><span class="sxs-lookup"><span data-stu-id="9bb50-117">ADS Type</span></span>     | <span data-ttu-id="9bb50-118">\_inteiro grande \_ ADSTYPE</span><span class="sxs-lookup"><span data-stu-id="9bb50-118">ADSTYPE\_LARGE\_INTEGER</span></span>                                                            |
| <span data-ttu-id="9bb50-119">Tipo de variante</span><span class="sxs-lookup"><span data-stu-id="9bb50-119">Variant Type</span></span> | <span data-ttu-id="9bb50-120">expedição de VT \_</span><span class="sxs-lookup"><span data-stu-id="9bb50-120">VT\_DISPATCH</span></span>                                                                       |
| <span data-ttu-id="9bb50-121">Tipo SDS</span><span class="sxs-lookup"><span data-stu-id="9bb50-121">SDS Type</span></span>     | <span data-ttu-id="9bb50-122">Um objeto COM que pode ser convertido em um [**IADsLargeInteger**](/windows/desktop/api/iads/nn-iads-iadslargeinteger).</span><span class="sxs-lookup"><span data-stu-id="9bb50-122">A COM object that can be cast to an [**IADsLargeInteger**](/windows/desktop/api/iads/nn-iads-iadslargeinteger).</span></span> |



## <a name="see-also"></a><span data-ttu-id="9bb50-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="9bb50-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bb50-124">**IADsLargeInteger**</span><span class="sxs-lookup"><span data-stu-id="9bb50-124">**IADsLargeInteger**</span></span>](/windows/desktop/api/iads/nn-iads-iadslargeinteger)
</dt> <dt>

[<span data-ttu-id="9bb50-125">**LargeInteger**</span><span class="sxs-lookup"><span data-stu-id="9bb50-125">**LargeInteger**</span></span>](s-largeinteger.md)
</dt> </dl>

 

 
