---
title: Atribuição de peso de filtro
description: Cada filtro na WFP (Windows Filtering Platform) tem um peso associado, que é usado durante a arbitragem de filtro.
ms.assetid: c78854c2-9aa1-408f-82d6-4b9e52f38e84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c77982258bb9c8ef14e22b20e28b6a3039456ae
ms.sourcegitcommit: 013de6f5280f28a9b04c3cce9387e629b07d70fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/26/2020
ms.locfileid: "104365763"
---
# <a name="filter-weight-assignment"></a><span data-ttu-id="7b150-103">Atribuição de peso de filtro</span><span class="sxs-lookup"><span data-stu-id="7b150-103">Filter Weight Assignment</span></span>

<span data-ttu-id="7b150-104">Cada filtro na WFP (Windows Filtering Platform) tem um peso associado, que é usado durante a [arbitragem de filtro](filter-arbitration.md).</span><span class="sxs-lookup"><span data-stu-id="7b150-104">Every filter in the Windows Filtering Platform (WFP) has an associated weight, which is used during [filter arbitration](filter-arbitration.md).</span></span>

<span data-ttu-id="7b150-105">O peso do filtro usado pelo mecanismo de filtragem base (BFE) é do tipo [**fwp \_ UINT64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span><span class="sxs-lookup"><span data-stu-id="7b150-105">The filter weight used by the Base Filtering Engine (BFE) is of type [**FWP\_UINT64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span></span> <span data-ttu-id="7b150-106">Os chamadores têm três opções ao adicionar filtros.</span><span class="sxs-lookup"><span data-stu-id="7b150-106">Callers have three options when adding filters.</span></span>

-   <span data-ttu-id="7b150-107">Defina o peso para um [**fwp \_ UINT64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span><span class="sxs-lookup"><span data-stu-id="7b150-107">Set the weight to an [**FWP\_UINT64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span></span> <span data-ttu-id="7b150-108">O BFE usa o peso fornecido como está.</span><span class="sxs-lookup"><span data-stu-id="7b150-108">BFE uses the supplied weight as is.</span></span>
-   <span data-ttu-id="7b150-109">Defina o peso como [**fwp \_ vazio**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span><span class="sxs-lookup"><span data-stu-id="7b150-109">Set the weight to [**FWP\_EMPTY**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span></span> <span data-ttu-id="7b150-110">O BFE gera automaticamente um peso no intervalo de \[ 0, 2 ⁶ ⁰).</span><span class="sxs-lookup"><span data-stu-id="7b150-110">BFE automatically generates a weight in the range \[0, 2⁶⁰).</span></span>
-   <span data-ttu-id="7b150-111">Defina o peso para um [**fwp \_ UINT8**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) no intervalo de \[ 0, 15 \] .</span><span class="sxs-lookup"><span data-stu-id="7b150-111">Set the weight to an [**FWP\_UINT8**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) in the range \[0, 15\].</span></span> <span data-ttu-id="7b150-112">O BFE usa o peso fornecido como um identificador de intervalo de peso.</span><span class="sxs-lookup"><span data-stu-id="7b150-112">BFE uses the supplied weight as a weight range identifier.</span></span>

    <span data-ttu-id="7b150-113">O BFE gera automaticamente os bits 60 de ordem inferior (exatamente como se o peso tivesse sido definido como [**fwp \_ vazio**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)) e, em seguida, usa o valor fornecido para definir os 4 bits de ordem superior.</span><span class="sxs-lookup"><span data-stu-id="7b150-113">BFE automatically generates the low-order 60 bits (exactly as if the weight had been set to [**FWP\_EMPTY**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)), and then uses the supplied value to set the 4 high-order bits.</span></span> <span data-ttu-id="7b150-114">Isso permite que os chamadores dividam manualmente o espaço de peso em 16 intervalos, enquanto ainda usam o peso automático em um intervalo.</span><span class="sxs-lookup"><span data-stu-id="7b150-114">This allows callers to manually divide the weight space into 16 ranges, while still using automatic weighting within a range.</span></span>

> [!Note]  
> <span data-ttu-id="7b150-115">Quando dois ou mais textos explicativos são registrados na mesma subcamada, podem ocorrer problemas quando o mesmo peso é atribuído aos filtros.</span><span class="sxs-lookup"><span data-stu-id="7b150-115">When two or more callouts are registered at the same sublayer, problems may occur when the same weight is assigned to the filters.</span></span> <span data-ttu-id="7b150-116">Esse problema pode ser evitado fazendo com que os textos explicativos criem sua própria subcamada usando [**FwpmSubLayerAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayeradd0).</span><span class="sxs-lookup"><span data-stu-id="7b150-116">This issue can be prevented by having callouts create their own sublayer by using [**FwpmSubLayerAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayeradd0).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="7b150-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7b150-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b150-118">**Identificadores de peso de filtro**</span><span class="sxs-lookup"><span data-stu-id="7b150-118">**Filter Weight Identifiers**</span></span>](filter-weight-identifiers.md)
</dt> </dl>

 

 




