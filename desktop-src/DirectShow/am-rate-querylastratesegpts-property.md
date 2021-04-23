---
description: Essa propriedade consulta o decodificador para a hora de início da alteração de taxa que foi enfileirada mais recentemente, independentemente de sua posição na fila de alteração de taxa.
ms.assetid: 3c7006e7-48fd-4df8-b446-8ee2b024278b
title: Propriedade AM_RATE_QueryLastRateSegPTS (DVDMedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c6e3e00985ba6e714bf48d349fd5af5c9593b9
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910264"
---
# <a name="am_rate_querylastratesegpts-property"></a><span data-ttu-id="df814-103">Propriedade de QueryLastRateSegPTS da \_ taxa de am \_</span><span class="sxs-lookup"><span data-stu-id="df814-103">AM\_RATE\_QueryLastRateSegPTS Property</span></span>

<span data-ttu-id="df814-104">Essa propriedade consulta o decodificador para a hora de início da alteração de taxa que foi enfileirada mais recentemente, independentemente de sua posição na fila de alteração de taxa.</span><span class="sxs-lookup"><span data-stu-id="df814-104">This property queries the decoder for the start time of the rate change that was queued most recently, regardless of its position in the rate-change queue.</span></span>

<span data-ttu-id="df814-105">Esta propriedade é definida para a versão 1,1 deste conjunto de propriedades; consulte [**a \_ taxa de \_ UseRateVersion**](am-rate-userateversion-property.md).</span><span class="sxs-lookup"><span data-stu-id="df814-105">This property is defined for version 1.1 of this property set; see [**AM\_RATE\_UseRateVersion**](am-rate-userateversion-property.md).</span></span>



| <span data-ttu-id="df814-106">Label</span><span class="sxs-lookup"><span data-stu-id="df814-106">Label</span></span> | <span data-ttu-id="df814-107">Valor</span><span class="sxs-lookup"><span data-stu-id="df814-107">Value</span></span> |
|-------------------|-------------------------------|
| <span data-ttu-id="df814-108">GUID do Conjunto de Propriedades</span><span class="sxs-lookup"><span data-stu-id="df814-108">Property Set GUID</span></span> | <span data-ttu-id="df814-109">\_KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="df814-109">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="df814-110">ID da propriedade</span><span class="sxs-lookup"><span data-stu-id="df814-110">Property ID</span></span>       | <span data-ttu-id="df814-111">\_QueryLastRateSegPTS de taxa de am \_</span><span class="sxs-lookup"><span data-stu-id="df814-111">AM\_RATE\_QueryLastRateSegPTS</span></span> |
| <span data-ttu-id="df814-112">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="df814-112">Data Type</span></span>         | <span data-ttu-id="df814-113">**hora de referência \_**</span><span class="sxs-lookup"><span data-stu-id="df814-113">**REFERENCE\_TIME**</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="df814-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="df814-114">Remarks</span></span>

<span data-ttu-id="df814-115">O filtro de origem pode usar essa propriedade para sincronizar as alterações de taxa em vários fluxos de áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="df814-115">The source filter can use this property to synchronize rate changes across several audio and video streams.</span></span>

## <a name="requirements"></a><span data-ttu-id="df814-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df814-116">Requirements</span></span>



| <span data-ttu-id="df814-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="df814-117">Requirement</span></span> | <span data-ttu-id="df814-118">Valor</span><span class="sxs-lookup"><span data-stu-id="df814-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df814-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="df814-119">Header</span></span><br/> | <dl> <span data-ttu-id="df814-120"><dt>DVDMedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="df814-120"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df814-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="df814-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df814-122">**Conjunto de propriedades de alteração de taxa**</span><span class="sxs-lookup"><span data-stu-id="df814-122">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




