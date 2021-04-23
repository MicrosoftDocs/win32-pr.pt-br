---
description: Essa propriedade consulta o decodificador quanto à taxa máxima de quadro completo que o decodificador dá suporte. O tipo de dados para essa propriedade é uma \_ estrutura am QueryRate.
ms.assetid: 98808ed4-6d34-437b-9729-9cc805bc81f0
title: Propriedade AM_RATE_QueryFullFrameRate (DVDMedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70bc096e5b68737ca877a037571223d673284dab
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910274"
---
# <a name="am_rate_queryfullframerate-property"></a><span data-ttu-id="500c5-104">Propriedade de QueryFullFrameRate da \_ taxa de am \_</span><span class="sxs-lookup"><span data-stu-id="500c5-104">AM\_RATE\_QueryFullFrameRate Property</span></span>

<span data-ttu-id="500c5-105">Essa propriedade consulta o decodificador quanto à taxa máxima de quadro completo que o decodificador dá suporte.</span><span class="sxs-lookup"><span data-stu-id="500c5-105">This property queries the decoder for the maximum full-frame rate that the decoder supports.</span></span> <span data-ttu-id="500c5-106">O tipo de dados para essa propriedade é uma estrutura **am \_ QueryRate** .</span><span class="sxs-lookup"><span data-stu-id="500c5-106">The data type for this property is an **AM\_QueryRate** structure.</span></span>

<span data-ttu-id="500c5-107">Esta propriedade é definida para a versão 1,1 deste conjunto de propriedades; consulte [**a \_ taxa de \_ UseRateVersion**](am-rate-userateversion-property.md).</span><span class="sxs-lookup"><span data-stu-id="500c5-107">This property is defined for version 1.1 of this property set; see [**AM\_RATE\_UseRateVersion**](am-rate-userateversion-property.md).</span></span>



| <span data-ttu-id="500c5-108">Label</span><span class="sxs-lookup"><span data-stu-id="500c5-108">Label</span></span> | <span data-ttu-id="500c5-109">Valor</span><span class="sxs-lookup"><span data-stu-id="500c5-109">Value</span></span> |
|-------------------|---------------------------------------|
| <span data-ttu-id="500c5-110">GUID do Conjunto de Propriedades</span><span class="sxs-lookup"><span data-stu-id="500c5-110">Property Set GUID</span></span> | <span data-ttu-id="500c5-111">\_KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="500c5-111">AM\_KSPROPSETID\_TSRateChange</span></span>         |
| <span data-ttu-id="500c5-112">ID da propriedade</span><span class="sxs-lookup"><span data-stu-id="500c5-112">Property ID</span></span>       | <span data-ttu-id="500c5-113">Propriedade de QueryFullFrameRate da \_ taxa de am \_</span><span class="sxs-lookup"><span data-stu-id="500c5-113">AM\_RATE\_QueryFullFrameRate Property</span></span> |
| <span data-ttu-id="500c5-114">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="500c5-114">Data Type</span></span>         | [<span data-ttu-id="500c5-115">**AM \_ QueryRate**</span><span class="sxs-lookup"><span data-stu-id="500c5-115">**AM\_QueryRate**</span></span>](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_queryrate) |



 

## <a name="remarks"></a><span data-ttu-id="500c5-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="500c5-116">Remarks</span></span>

<span data-ttu-id="500c5-117">Se a taxa de reprodução exceder a taxa máxima do decodificador, o filtro de origem enviará grupos de amostras contínuas separadas por descontinuidades.</span><span class="sxs-lookup"><span data-stu-id="500c5-117">If the playback rate exceeds the decoder's maximum rate, the source filter sends groups of continuous samples separated by discontinuities.</span></span> <span data-ttu-id="500c5-118">Os carimbos de data/hora saltam pelo descontinuidades.</span><span class="sxs-lookup"><span data-stu-id="500c5-118">The time stamps jump across the discontinuities.</span></span> <span data-ttu-id="500c5-119">O filtro de origem pode fazer isso mesmo se a taxa de reprodução estiver dentro da taxa máxima do decodificador, porque pode haver outros fatores, como e/s de disco, que limitam a taxa de reprodução completa.</span><span class="sxs-lookup"><span data-stu-id="500c5-119">The source filter might do this even if the playback rate is within the decoder's maximum rate, because there may be other factors, such as disk IO, that limit the full playback rate.</span></span>

## <a name="requirements"></a><span data-ttu-id="500c5-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="500c5-120">Requirements</span></span>



| <span data-ttu-id="500c5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="500c5-121">Requirement</span></span> | <span data-ttu-id="500c5-122">Valor</span><span class="sxs-lookup"><span data-stu-id="500c5-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="500c5-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="500c5-123">Header</span></span><br/> | <dl> <span data-ttu-id="500c5-124"><dt>DVDMedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="500c5-124"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="500c5-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="500c5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="500c5-126">**Conjunto de propriedades de alteração de taxa**</span><span class="sxs-lookup"><span data-stu-id="500c5-126">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




