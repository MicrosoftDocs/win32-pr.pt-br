---
description: As \_ constantes LINECALLTREATMENT listam tratamentos para chamadas que não são respondidas ou estão em espera. Exceto para a validação básica de parâmetros, o tratamento de chamadas é uma passagem direta pela TAPI para o provedor de serviços.
ms.assetid: c28c9200-dd51-48b2-905c-fbe37c83b00f
title: Constantes de LINECALLTREATMENT_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e25a19b5db4525550047c468b496cce2363f6ee2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761953"
---
# <a name="linecalltreatment_-constants"></a><span data-ttu-id="c3691-104">\_Constantes LINECALLTREATMENT</span><span class="sxs-lookup"><span data-stu-id="c3691-104">LINECALLTREATMENT\_ Constants</span></span>

<span data-ttu-id="c3691-105">As **constantes \_ LINECALLTREATMENT** listam tratamentos para chamadas que não são respondidas ou estão em espera.</span><span class="sxs-lookup"><span data-stu-id="c3691-105">The **LINECALLTREATMENT\_** constants list treatments for calls that are unanswered or on hold.</span></span> <span data-ttu-id="c3691-106">Exceto para a validação básica de parâmetros, o tratamento de chamadas é uma passagem direta pela TAPI para o provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="c3691-106">Except for basic parameter validation, call treatment is a straight pass-through by TAPI to the service provider.</span></span>

<dl> <dt>

<span data-ttu-id="c3691-107"><span id="LINECALLTREATMENT_BUSY"></span><span id="linecalltreatment_busy"></span>**LINECALLTREATMENT \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="c3691-107"><span id="LINECALLTREATMENT_BUSY"></span><span id="linecalltreatment_busy"></span>**LINECALLTREATMENT\_BUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c3691-108">Quando a chamada não está ativamente conectada a um dispositivo (oferta ou onhold), a parte ouve o sinal ocupado.</span><span class="sxs-lookup"><span data-stu-id="c3691-108">When the call is not actively connected to a device (offering or onhold), the party hears busy signal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c3691-109"><span id="LINECALLTREATMENT_MUSIC"></span><span id="linecalltreatment_music"></span>**\_música LINECALLTREATMENT**</span><span class="sxs-lookup"><span data-stu-id="c3691-109"><span id="LINECALLTREATMENT_MUSIC"></span><span id="linecalltreatment_music"></span>**LINECALLTREATMENT\_MUSIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c3691-110">Quando a chamada não está ativamente conectada a um dispositivo (oferta ou onhold), a parte ouve música.</span><span class="sxs-lookup"><span data-stu-id="c3691-110">When the call is not actively connected to a device (offering or onhold), the party hears music.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c3691-111"><span id="LINECALLTREATMENT_RINGBACK"></span><span id="linecalltreatment_ringback"></span>**LINECALLTREATMENT de \_ toque**</span><span class="sxs-lookup"><span data-stu-id="c3691-111"><span id="LINECALLTREATMENT_RINGBACK"></span><span id="linecalltreatment_ringback"></span>**LINECALLTREATMENT\_RINGBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c3691-112">Quando a chamada não está ativamente conectada a um dispositivo (oferta ou onhold), a parte ouve o tom de toque.</span><span class="sxs-lookup"><span data-stu-id="c3691-112">When the call is not actively connected to a device (offering or onhold), the party hears ringback tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c3691-113"><span id="LINECALLTREATMENT_SILENCE"></span><span id="linecalltreatment_silence"></span>**\_silêncio LINECALLTREATMENT**</span><span class="sxs-lookup"><span data-stu-id="c3691-113"><span id="LINECALLTREATMENT_SILENCE"></span><span id="linecalltreatment_silence"></span>**LINECALLTREATMENT\_SILENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c3691-114">Quando a chamada não está ativamente conectada a um dispositivo (oferta ou onhold), a parte ouve silêncio.</span><span class="sxs-lookup"><span data-stu-id="c3691-114">When the call is not actively connected to a device (offering or onhold), the party hears silence.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3691-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3691-115">Remarks</span></span>

<span data-ttu-id="c3691-116">O valor 0x00000000 é reservado para indicar que o provedor de serviços não dá suporte a tratamentos de chamada.</span><span class="sxs-lookup"><span data-stu-id="c3691-116">The value 0x00000000 is reserved to indicate that the service provider does not support call treatments.</span></span> <span data-ttu-id="c3691-117">Os valores no intervalo de 0x00000005 a 0x000000FF são reservados para a definição futura.</span><span class="sxs-lookup"><span data-stu-id="c3691-117">Values in the range 0x00000005 through 0x000000FF are reserved for future definition.</span></span> <span data-ttu-id="c3691-118">Os valores no intervalo de 0x00000100 a 0xFFFFFFFF são reservados para atribuição por provedores de serviço e podem incluir a identificação de seleções musicais específicas ou anúncios gravados.</span><span class="sxs-lookup"><span data-stu-id="c3691-118">Values in the range 0x00000100 through 0xFFFFFFFF are reserved for assignment by service providers, and may include identification of specific musical selections or recorded announcements.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3691-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3691-119">Requirements</span></span>



| <span data-ttu-id="c3691-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3691-120">Requirement</span></span> | <span data-ttu-id="c3691-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c3691-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c3691-122">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="c3691-122">TAPI version</span></span><br/> | <span data-ttu-id="c3691-123">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="c3691-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="c3691-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c3691-124">Header</span></span><br/>       | <dl> <span data-ttu-id="c3691-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3691-125"><dt>Tapi.h</dt></span></span> </dl> |



 

 




