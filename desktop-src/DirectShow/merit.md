---
description: Os valores de mérito definem a ordem na qual o Gerenciador do grafo de filtro tenta adicionar filtros durante a criação do grafo.
ms.assetid: 9e026675-e0a9-4c82-9b57-ab0e7d9592ea
title: Mérito (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 947a13d78f58c12c236ec31f0eeee1dc6d44f1d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758462"
---
# <a name="merit"></a><span data-ttu-id="7bfba-103">Núcleo</span><span class="sxs-lookup"><span data-stu-id="7bfba-103">Merit</span></span>

<span data-ttu-id="7bfba-104">Os valores de mérito definem a ordem na qual o Gerenciador do grafo de filtro tenta adicionar filtros durante a criação do grafo.</span><span class="sxs-lookup"><span data-stu-id="7bfba-104">Merit values define the order in which the Filter Graph Manager tries to add filters during graph building.</span></span>

<dl> <span data-ttu-id="7bfba-105"><span id="MERIT_PREFERRED"></span><span id="merit_preferred"></span>**Mérito \_ Preferível** (0x800000) <span id="MERIT_NORMAL"></span> <span id="merit_normal"></span> **mérito \_ normal** (0x600000) mérito <span id="MERIT_UNLIKELY"></span> <span id="merit_unlikely"></span> **\_ improvável** (0x400000) <span id="MERIT_DO_NOT_USE"></span> <span id="merit_do_not_use"></span> **mérito \_ \_ não \_ usa** (0x200000) ( <span id="MERIT_SW_COMPRESSOR"></span> <span id="merit_sw_compressor"></span> **mérito \_ SW \_ compressor** <span id="MERIT_HW_COMPRESSOR"></span> <span id="merit_hw_compressor"></span> **\_ \_** ) (0x100000) (núcleo de HW)</span><span class="sxs-lookup"><span data-stu-id="7bfba-105"><span id="MERIT_PREFERRED"></span><span id="merit_preferred"></span>**MERIT\_PREFERRED** (0x800000) <span id="MERIT_NORMAL"></span><span id="merit_normal"></span>**MERIT\_NORMAL** (0x600000) <span id="MERIT_UNLIKELY"></span><span id="merit_unlikely"></span>**MERIT\_UNLIKELY** (0x400000) <span id="MERIT_DO_NOT_USE"></span><span id="merit_do_not_use"></span>**MERIT\_DO\_NOT\_USE** (0x200000) <span id="MERIT_SW_COMPRESSOR"></span><span id="merit_sw_compressor"></span>**MERIT\_SW\_COMPRESSOR** (0x100000) <span id="MERIT_HW_COMPRESSOR"></span><span id="merit_hw_compressor"></span>**MERIT\_HW\_COMPRESSOR** (0x100050)</span></span>
</dl>

## <a name="remarks"></a><span data-ttu-id="7bfba-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="7bfba-106">Remarks</span></span>

<span data-ttu-id="7bfba-107">Cada filtro é registrado com um valor de mérito.</span><span class="sxs-lookup"><span data-stu-id="7bfba-107">Each filter is registered with a merit value.</span></span> <span data-ttu-id="7bfba-108">Quando o Gerenciador de gráfico de filtro cria um grafo, ele enumera todos os filtros registrados com o tipo de mídia correto.</span><span class="sxs-lookup"><span data-stu-id="7bfba-108">When the filter graph manager builds a graph, it enumerates all the filters registered with the correct media type.</span></span> <span data-ttu-id="7bfba-109">Em seguida, ele os tenta em ordem de mérito, do mais alto para o mais baixo.</span><span class="sxs-lookup"><span data-stu-id="7bfba-109">Then it tries them in order of merit, from highest to lowest.</span></span> <span data-ttu-id="7bfba-110">(Ele usa critérios adicionais para escolher entre os filtros com o mesmo mérito.) Ele nunca tenta filtros com um valor de mérito menor ou igual a **mérito \_ não \_ é \_ usado**.</span><span class="sxs-lookup"><span data-stu-id="7bfba-110">(It uses additional criteria to choose between filters with equal merit.) It never tries filters with a merit value less than or equal to **MERIT\_DO\_NOT\_USE**.</span></span>

<span data-ttu-id="7bfba-111">Um filtro que nunca deve ser considerado para reprodução comum deve ter um mérito de **mérito \_ \_ não \_ usar** ou menos.</span><span class="sxs-lookup"><span data-stu-id="7bfba-111">A filter that should never be considered for ordinary playback should have a merit of **MERIT\_DO\_NOT\_USE** or less.</span></span> <span data-ttu-id="7bfba-112">Os filtros podem ser registrados com valores intermediários não definidos por essa enumeração, como **mérito \_ normal** + 1.</span><span class="sxs-lookup"><span data-stu-id="7bfba-112">Filters can be registered with intermediate values not defined by this enumeration, such as **MERIT\_NORMAL** + 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bfba-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7bfba-113">Requirements</span></span>



| <span data-ttu-id="7bfba-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bfba-114">Requirement</span></span> | <span data-ttu-id="7bfba-115">Valor</span><span class="sxs-lookup"><span data-stu-id="7bfba-115">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7bfba-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7bfba-116">Header</span></span><br/> | <dl> <span data-ttu-id="7bfba-117"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="7bfba-117"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bfba-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="7bfba-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bfba-119">Constantes e GUIDs</span><span class="sxs-lookup"><span data-stu-id="7bfba-119">Constants and GUIDs</span></span>](constants-and-guids.md)
</dt> <dt>

[<span data-ttu-id="7bfba-120">Diretrizes para o registro de filtros</span><span class="sxs-lookup"><span data-stu-id="7bfba-120">Guidelines for Registering Filters</span></span>](guidelines-for-registering-filters.md)
</dt> <dt>

[<span data-ttu-id="7bfba-121">Conexão inteligente</span><span class="sxs-lookup"><span data-stu-id="7bfba-121">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> </dl>

 

 




