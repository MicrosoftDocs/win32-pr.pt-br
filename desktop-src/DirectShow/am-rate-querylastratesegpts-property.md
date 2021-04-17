---
description: Essa propriedade consulta o decodificador para a hora de início da alteração de taxa que foi enfileirada mais recentemente, independentemente de sua posição na fila de alteração de taxa.
ms.assetid: 3c7006e7-48fd-4df8-b446-8ee2b024278b
title: Propriedade AM_RATE_QueryLastRateSegPTS (DVDMedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 024ac26d8307dc9b8ff8e16603dfcc61b0704390
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754781"
---
# <a name="am_rate_querylastratesegpts-property"></a><span data-ttu-id="582ff-103">Propriedade de QueryLastRateSegPTS da \_ taxa de am \_</span><span class="sxs-lookup"><span data-stu-id="582ff-103">AM\_RATE\_QueryLastRateSegPTS Property</span></span>

<span data-ttu-id="582ff-104">Essa propriedade consulta o decodificador para a hora de início da alteração de taxa que foi enfileirada mais recentemente, independentemente de sua posição na fila de alteração de taxa.</span><span class="sxs-lookup"><span data-stu-id="582ff-104">This property queries the decoder for the start time of the rate change that was queued most recently, regardless of its position in the rate-change queue.</span></span>

<span data-ttu-id="582ff-105">Esta propriedade é definida para a versão 1,1 deste conjunto de propriedades; consulte [**a \_ taxa de \_ UseRateVersion**](am-rate-userateversion-property.md).</span><span class="sxs-lookup"><span data-stu-id="582ff-105">This property is defined for version 1.1 of this property set; see [**AM\_RATE\_UseRateVersion**](am-rate-userateversion-property.md).</span></span>



|                   |                               |
|-------------------|-------------------------------|
| <span data-ttu-id="582ff-106">GUID do Conjunto de Propriedades</span><span class="sxs-lookup"><span data-stu-id="582ff-106">Property Set GUID</span></span> | <span data-ttu-id="582ff-107">\_KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="582ff-107">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="582ff-108">ID da propriedade</span><span class="sxs-lookup"><span data-stu-id="582ff-108">Property ID</span></span>       | <span data-ttu-id="582ff-109">\_QueryLastRateSegPTS de taxa de am \_</span><span class="sxs-lookup"><span data-stu-id="582ff-109">AM\_RATE\_QueryLastRateSegPTS</span></span> |
| <span data-ttu-id="582ff-110">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="582ff-110">Data Type</span></span>         | <span data-ttu-id="582ff-111">**hora de referência \_**</span><span class="sxs-lookup"><span data-stu-id="582ff-111">**REFERENCE\_TIME**</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="582ff-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="582ff-112">Remarks</span></span>

<span data-ttu-id="582ff-113">O filtro de origem pode usar essa propriedade para sincronizar as alterações de taxa em vários fluxos de áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="582ff-113">The source filter can use this property to synchronize rate changes across several audio and video streams.</span></span>

## <a name="requirements"></a><span data-ttu-id="582ff-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="582ff-114">Requirements</span></span>



| <span data-ttu-id="582ff-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="582ff-115">Requirement</span></span> | <span data-ttu-id="582ff-116">Valor</span><span class="sxs-lookup"><span data-stu-id="582ff-116">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="582ff-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="582ff-117">Header</span></span><br/> | <dl> <span data-ttu-id="582ff-118"><dt>DVDMedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="582ff-118"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="582ff-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="582ff-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="582ff-120">**Conjunto de propriedades de alteração de taxa**</span><span class="sxs-lookup"><span data-stu-id="582ff-120">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




