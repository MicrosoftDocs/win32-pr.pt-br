---
description: Essa propriedade consulta o decodificador quanto à taxa máxima de quadro completo que o decodificador dá suporte. O tipo de dados para essa propriedade é uma \_ estrutura am QueryRate.
ms.assetid: 98808ed4-6d34-437b-9729-9cc805bc81f0
title: Propriedade AM_RATE_QueryFullFrameRate (DVDMedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab2c99564caa09253198b101a3e2467ec88c7e34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785507"
---
# <a name="am_rate_queryfullframerate-property"></a><span data-ttu-id="e4987-104">Propriedade de QueryFullFrameRate da \_ taxa de am \_</span><span class="sxs-lookup"><span data-stu-id="e4987-104">AM\_RATE\_QueryFullFrameRate Property</span></span>

<span data-ttu-id="e4987-105">Essa propriedade consulta o decodificador quanto à taxa máxima de quadro completo que o decodificador dá suporte.</span><span class="sxs-lookup"><span data-stu-id="e4987-105">This property queries the decoder for the maximum full-frame rate that the decoder supports.</span></span> <span data-ttu-id="e4987-106">O tipo de dados para essa propriedade é uma estrutura **am \_ QueryRate** .</span><span class="sxs-lookup"><span data-stu-id="e4987-106">The data type for this property is an **AM\_QueryRate** structure.</span></span>

<span data-ttu-id="e4987-107">Esta propriedade é definida para a versão 1,1 deste conjunto de propriedades; consulte [**a \_ taxa de \_ UseRateVersion**](am-rate-userateversion-property.md).</span><span class="sxs-lookup"><span data-stu-id="e4987-107">This property is defined for version 1.1 of this property set; see [**AM\_RATE\_UseRateVersion**](am-rate-userateversion-property.md).</span></span>



|                   |                                       |
|-------------------|---------------------------------------|
| <span data-ttu-id="e4987-108">GUID do Conjunto de Propriedades</span><span class="sxs-lookup"><span data-stu-id="e4987-108">Property Set GUID</span></span> | <span data-ttu-id="e4987-109">\_KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="e4987-109">AM\_KSPROPSETID\_TSRateChange</span></span>         |
| <span data-ttu-id="e4987-110">ID da propriedade</span><span class="sxs-lookup"><span data-stu-id="e4987-110">Property ID</span></span>       | <span data-ttu-id="e4987-111">Propriedade de QueryFullFrameRate da \_ taxa de am \_</span><span class="sxs-lookup"><span data-stu-id="e4987-111">AM\_RATE\_QueryFullFrameRate Property</span></span> |
| <span data-ttu-id="e4987-112">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="e4987-112">Data Type</span></span>         | [<span data-ttu-id="e4987-113">**AM \_ QueryRate**</span><span class="sxs-lookup"><span data-stu-id="e4987-113">**AM\_QueryRate**</span></span>](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_queryrate) |



 

## <a name="remarks"></a><span data-ttu-id="e4987-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4987-114">Remarks</span></span>

<span data-ttu-id="e4987-115">Se a taxa de reprodução exceder a taxa máxima do decodificador, o filtro de origem enviará grupos de amostras contínuas separadas por descontinuidades.</span><span class="sxs-lookup"><span data-stu-id="e4987-115">If the playback rate exceeds the decoder's maximum rate, the source filter sends groups of continuous samples separated by discontinuities.</span></span> <span data-ttu-id="e4987-116">Os carimbos de data/hora saltam pelo descontinuidades.</span><span class="sxs-lookup"><span data-stu-id="e4987-116">The time stamps jump across the discontinuities.</span></span> <span data-ttu-id="e4987-117">O filtro de origem pode fazer isso mesmo se a taxa de reprodução estiver dentro da taxa máxima do decodificador, porque pode haver outros fatores, como e/s de disco, que limitam a taxa de reprodução completa.</span><span class="sxs-lookup"><span data-stu-id="e4987-117">The source filter might do this even if the playback rate is within the decoder's maximum rate, because there may be other factors, such as disk IO, that limit the full playback rate.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4987-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4987-118">Requirements</span></span>



| <span data-ttu-id="e4987-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4987-119">Requirement</span></span> | <span data-ttu-id="e4987-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e4987-120">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4987-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e4987-121">Header</span></span><br/> | <dl> <span data-ttu-id="e4987-122"><dt>DVDMedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4987-122"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4987-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4987-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4987-124">**Conjunto de propriedades de alteração de taxa**</span><span class="sxs-lookup"><span data-stu-id="e4987-124">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




