---
description: As \_ constantes LINEADDRFEATURE listam as operações que podem ser invocadas em um endereço.
ms.assetid: dedeee7b-578b-4b19-8b99-5cd23779d661
title: Constantes de LINEADDRFEATURE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 825902c2943806d1d495e14a0f0a5042f2949796
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764760"
---
# <a name="lineaddrfeature_-constants"></a><span data-ttu-id="45d91-103">\_Constantes LINEADDRFEATURE</span><span class="sxs-lookup"><span data-stu-id="45d91-103">LINEADDRFEATURE\_ Constants</span></span>

<span data-ttu-id="45d91-104">As **constantes \_ LINEADDRFEATURE** listam as operações que podem ser invocadas em um endereço.</span><span class="sxs-lookup"><span data-stu-id="45d91-104">The **LINEADDRFEATURE\_** constants list the operations that can be invoked on an address.</span></span>

<dl> <dt>

<span data-ttu-id="45d91-105"><span id="LINEADDRFEATURE_FORWARD"></span><span id="lineaddrfeature_forward"></span>**encaminhar LINEADDRFEATURE \_**</span><span class="sxs-lookup"><span data-stu-id="45d91-105"><span id="LINEADDRFEATURE_FORWARD"></span><span id="lineaddrfeature_forward"></span>**LINEADDRFEATURE\_FORWARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="45d91-106">O endereço pode ser encaminhado.</span><span class="sxs-lookup"><span data-stu-id="45d91-106">The address can be forwarded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45d91-107"><span id="LINEADDRFEATURE_MAKECALL"></span><span id="lineaddrfeature_makecall"></span>**LINEADDRFEATURE \_ MAKECALL**</span><span class="sxs-lookup"><span data-stu-id="45d91-107"><span id="LINEADDRFEATURE_MAKECALL"></span><span id="lineaddrfeature_makecall"></span>**LINEADDRFEATURE\_MAKECALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="45d91-108">Uma chamada de saída pode ser colocada no endereço.</span><span class="sxs-lookup"><span data-stu-id="45d91-108">An outgoing call can be placed on the address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45d91-109"><span id="LINEADDRFEATURE_PICKUP"></span><span id="lineaddrfeature_pickup"></span>**retirada de LINEADDRFEATURE \_**</span><span class="sxs-lookup"><span data-stu-id="45d91-109"><span id="LINEADDRFEATURE_PICKUP"></span><span id="lineaddrfeature_pickup"></span>**LINEADDRFEATURE\_PICKUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="45d91-110">Uma chamada pode ser selecionada no endereço.</span><span class="sxs-lookup"><span data-stu-id="45d91-110">A call can be picked up at the address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45d91-111"><span id="LINEADDRFEATURE_PICKUPDIRECT"></span><span id="lineaddrfeature_pickupdirect"></span>**LINEADDRFEATURE \_ PICKUPDIRECT**</span><span class="sxs-lookup"><span data-stu-id="45d91-111"><span id="LINEADDRFEATURE_PICKUPDIRECT"></span><span id="lineaddrfeature_pickupdirect"></span>**LINEADDRFEATURE\_PICKUPDIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="45d91-112">A função [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) pode ser usada para pegar uma chamada em um endereço específico.</span><span class="sxs-lookup"><span data-stu-id="45d91-112">The [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) function can be used to pick up a call on a specific address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45d91-113"><span id="LINEADDRFEATURE_PICKUPGROUP"></span><span id="lineaddrfeature_pickupgroup"></span>**LINEADDRFEATURE \_ pickup**</span><span class="sxs-lookup"><span data-stu-id="45d91-113"><span id="LINEADDRFEATURE_PICKUPGROUP"></span><span id="lineaddrfeature_pickupgroup"></span>**LINEADDRFEATURE\_PICKUPGROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="45d91-114">A função [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) pode ser usada para pegar uma chamada no grupo.</span><span class="sxs-lookup"><span data-stu-id="45d91-114">The [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) function can be used to pick up a call in the group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45d91-115"><span id="LINEADDRFEATURE_PICKUPHELD"></span><span id="lineaddrfeature_pickupheld"></span>**LINEADDRFEATURE \_ PICKUPHELD**</span><span class="sxs-lookup"><span data-stu-id="45d91-115"><span id="LINEADDRFEATURE_PICKUPHELD"></span><span id="lineaddrfeature_pickupheld"></span>**LINEADDRFEATURE\_PICKUPHELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="45d91-116">A função [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) (com um endereço de destino **nulo** ) pode ser usada para pegar uma chamada que é mantida no endereço.</span><span class="sxs-lookup"><span data-stu-id="45d91-116">The [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) function (with a **null** destination address) can be used to pick up a call that is held on the address.</span></span> <span data-ttu-id="45d91-117">Isso normalmente é usado apenas em uma organização exclusivamente em ponte.</span><span class="sxs-lookup"><span data-stu-id="45d91-117">This is normally used only in a bridged-exclusive arrangement.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45d91-118"><span id="LINEADDRFEATURE_PICKUPWAITING"></span><span id="lineaddrfeature_pickupwaiting"></span>**LINEADDRFEATURE \_ PICKUPWAITING**</span><span class="sxs-lookup"><span data-stu-id="45d91-118"><span id="LINEADDRFEATURE_PICKUPWAITING"></span><span id="lineaddrfeature_pickupwaiting"></span>**LINEADDRFEATURE\_PICKUPWAITING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="45d91-119">A função [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) (com um endereço de destino **nulo** ) pode ser usada para pegar uma chamada em espera de chamada.</span><span class="sxs-lookup"><span data-stu-id="45d91-119">The [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) function (with a **null** destination address) can be used to pick up a call waiting call.</span></span> <span data-ttu-id="45d91-120">Observe que isso não indica necessariamente que uma chamada em espera está realmente presente, porque geralmente é impossível para um dispositivo de telefonia detectar automaticamente tal chamada; no entanto, ele indica que a função Hook-flash será invocada para tentar alternar para tal chamada.</span><span class="sxs-lookup"><span data-stu-id="45d91-120">Note that this does not necessarily indicate that a waiting call is actually present, because it is often impossible for a telephony device to automatically detect such a call; it does, however, indicate that the hook-flash function will be invoked to attempt to switch to such a call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45d91-121"><span id="LINEADDRFEATURE_SETMEDIACONTROL"></span><span id="lineaddrfeature_setmediacontrol"></span>**LINEADDRFEATURE \_ SETMEDIACONTROL**</span><span class="sxs-lookup"><span data-stu-id="45d91-121"><span id="LINEADDRFEATURE_SETMEDIACONTROL"></span><span id="lineaddrfeature_setmediacontrol"></span>**LINEADDRFEATURE\_SETMEDIACONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="45d91-122">O controle de mídia pode ser definido nesse endereço.</span><span class="sxs-lookup"><span data-stu-id="45d91-122">Media control can be set on this address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45d91-123"><span id="LINEADDRFEATURE_SETTERMINAL"></span><span id="lineaddrfeature_setterminal"></span>**LINEADDRFEATURE \_ SETterminal**</span><span class="sxs-lookup"><span data-stu-id="45d91-123"><span id="LINEADDRFEATURE_SETTERMINAL"></span><span id="lineaddrfeature_setterminal"></span>**LINEADDRFEATURE\_SETTERMINAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="45d91-124">Os modos de terminal para esse endereço podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="45d91-124">The terminal modes for this address can be set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45d91-125"><span id="LINEADDRFEATURE_SETUPCONF"></span><span id="lineaddrfeature_setupconf"></span>**LINEADDRFEATURE \_ SETUPCONF**</span><span class="sxs-lookup"><span data-stu-id="45d91-125"><span id="LINEADDRFEATURE_SETUPCONF"></span><span id="lineaddrfeature_setupconf"></span>**LINEADDRFEATURE\_SETUPCONF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="45d91-126">Uma chamada de conferência com uma chamada inicial **nula** pode ser configurada nesse endereço.</span><span class="sxs-lookup"><span data-stu-id="45d91-126">A conference call with a **NULL** initial call can be set up at this address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45d91-127"><span id="LINEADDRFEATURE_UNCOMPLETECALL"></span><span id="lineaddrfeature_uncompletecall"></span>**LINEADDRFEATURE \_ UNCOMPLETECALL**</span><span class="sxs-lookup"><span data-stu-id="45d91-127"><span id="LINEADDRFEATURE_UNCOMPLETECALL"></span><span id="lineaddrfeature_uncompletecall"></span>**LINEADDRFEATURE\_UNCOMPLETECALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="45d91-128">As solicitações de conclusão de chamada podem ser canceladas neste endereço.</span><span class="sxs-lookup"><span data-stu-id="45d91-128">Call completion requests can be canceled at this address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45d91-129"><span id="LINEADDRFEATURE_UNPARK"></span><span id="lineaddrfeature_unpark"></span>**LINEADDRFEATURE o \_ estacionamento**</span><span class="sxs-lookup"><span data-stu-id="45d91-129"><span id="LINEADDRFEATURE_UNPARK"></span><span id="lineaddrfeature_unpark"></span>**LINEADDRFEATURE\_UNPARK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="45d91-130">As chamadas podem ter o estacionamento anulado usando esse endereço.</span><span class="sxs-lookup"><span data-stu-id="45d91-130">Calls can be unparked using this address.</span></span>

> [!Note]  
> <span data-ttu-id="45d91-131">Se nenhum dos novos bits "PICKUP" modificados for definido no membro **dwAddressFeatures** em [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) , mas o \_ bit de retirada LINEADDRFEATURE estiver definido, então qualquer um dos modos de retirada poderá funcionar; o provedor de serviços simplesmente não especificou quais deles.</span><span class="sxs-lookup"><span data-stu-id="45d91-131">If none of the new modified "PICKUP" bits is set in the **dwAddressFeatures** member in [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) but the LINEADDRFEATURE\_PICKUP bit is set, then any of the pickup modes may work; the service provider has simply not specified which ones.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="45d91-132"><span id="LINEADDRFEATURE_FORWARDDND"></span><span id="lineaddrfeature_forwarddnd"></span>**LINEADDRFEATURE \_ FORWARDDND**</span><span class="sxs-lookup"><span data-stu-id="45d91-132"><span id="LINEADDRFEATURE_FORWARDDND"></span><span id="lineaddrfeature_forwarddnd"></span>**LINEADDRFEATURE\_FORWARDDND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="45d91-133">A função [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) (com um endereço de destino vazio) pode ser usada para ativar o recurso não incomodar no endereço.</span><span class="sxs-lookup"><span data-stu-id="45d91-133">The [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) function (with an empty destination address) can be used to turn on the Do Not Disturb feature on the address.</span></span> <span data-ttu-id="45d91-134">O LINEADDRFEATURE \_ Forward também será definido.</span><span class="sxs-lookup"><span data-stu-id="45d91-134">LINEADDRFEATURE\_FORWARD will also be set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45d91-135"><span id="LINEADDRFEATURE_FORWARDFWD"></span><span id="lineaddrfeature_forwardfwd"></span>**LINEADDRFEATURE \_ FORWARDFWD**</span><span class="sxs-lookup"><span data-stu-id="45d91-135"><span id="LINEADDRFEATURE_FORWARDFWD"></span><span id="lineaddrfeature_forwardfwd"></span>**LINEADDRFEATURE\_FORWARDFWD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="45d91-136">A função [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) pode ser usada para encaminhar chamadas no endereço para outros números.</span><span class="sxs-lookup"><span data-stu-id="45d91-136">The [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) function can be used to forward calls on the address to other numbers.</span></span> <span data-ttu-id="45d91-137">O LINEADDRFEATURE \_ Forward também será definido.</span><span class="sxs-lookup"><span data-stu-id="45d91-137">LINEADDRFEATURE\_FORWARD will also be set.</span></span>

> [!Note]  
> <span data-ttu-id="45d91-138">Se nenhum dos novos bits "encaminhar" modificados estiver definido no membro **dwAddressFeatures** em [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) , mas o \_ bit de encaminhamento LINEADDRFEATURE estiver definido, qualquer um dos modos de encaminhamento poderá funcionar; o provedor de serviços simplesmente não especificou quais deles.</span><span class="sxs-lookup"><span data-stu-id="45d91-138">If neither of the new modified "FORWARD" bits is set in the **dwAddressFeatures** member in [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) but the LINEADDRFEATURE\_FORWARD bit is set, then any of the forward modes may work; the service provider has simply not specified which ones.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45d91-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="45d91-139">Remarks</span></span>

<span data-ttu-id="45d91-140">Sem extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="45d91-140">No extensibility.</span></span> <span data-ttu-id="45d91-141">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="45d91-141">All 32 bits are reserved.</span></span>

<span data-ttu-id="45d91-142">Essa constante é usada em [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) (retornada por [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)) e em [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) (retornada por [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)).</span><span class="sxs-lookup"><span data-stu-id="45d91-142">This constant is used both in [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) (returned by [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)) and in [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) (returned by [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)).</span></span> <span data-ttu-id="45d91-143">O **LINEADDRESSCAPS** relata a disponibilidade dos recursos de endereço pelo provedor de serviços (principalmente a opção) para um determinado endereço.</span><span class="sxs-lookup"><span data-stu-id="45d91-143">**LINEADDRESSCAPS** reports the availability of the address features by the service provider (mainly the switch) for a given address.</span></span> <span data-ttu-id="45d91-144">Um aplicativo tornaria essa determinação quando ele for inicializado.</span><span class="sxs-lookup"><span data-stu-id="45d91-144">An application would make this determination when it initializes.</span></span> <span data-ttu-id="45d91-145">Os relatórios de estrutura [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) , para um determinado endereço, que os recursos de endereço podem realmente ser invocados enquanto o endereço está no estado atual.</span><span class="sxs-lookup"><span data-stu-id="45d91-145">The [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) structure reports, for a given address, which address features can actually be invoked while the address is in the current state.</span></span> <span data-ttu-id="45d91-146">Um aplicativo tornaria essa determinação dinamicamente após as alterações de estado do endereço, geralmente causadas por atividades relacionadas à chamada no endereço.</span><span class="sxs-lookup"><span data-stu-id="45d91-146">An application would make this determination dynamically after address-state changes, typically caused by call-related activities on the address.</span></span>

## <a name="requirements"></a><span data-ttu-id="45d91-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45d91-147">Requirements</span></span>



| <span data-ttu-id="45d91-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="45d91-148">Requirement</span></span> | <span data-ttu-id="45d91-149">Valor</span><span class="sxs-lookup"><span data-stu-id="45d91-149">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="45d91-150">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="45d91-150">TAPI version</span></span><br/> | <span data-ttu-id="45d91-151">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="45d91-151">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="45d91-152">parâmetro</span><span class="sxs-lookup"><span data-stu-id="45d91-152">Header</span></span><br/>       | <dl> <span data-ttu-id="45d91-153"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="45d91-153"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45d91-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="45d91-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45d91-155">**LINEADDRESSCAPS**</span><span class="sxs-lookup"><span data-stu-id="45d91-155">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="45d91-156">**LINEADDRESSSTATUS**</span><span class="sxs-lookup"><span data-stu-id="45d91-156">**LINEADDRESSSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[<span data-ttu-id="45d91-157">**lineForward**</span><span class="sxs-lookup"><span data-stu-id="45d91-157">**lineForward**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[<span data-ttu-id="45d91-158">**lineGetAddressCaps**</span><span class="sxs-lookup"><span data-stu-id="45d91-158">**lineGetAddressCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> <dt>

[<span data-ttu-id="45d91-159">**lineGetAddressStatus**</span><span class="sxs-lookup"><span data-stu-id="45d91-159">**lineGetAddressStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)
</dt> <dt>

[<span data-ttu-id="45d91-160">**linePickup**</span><span class="sxs-lookup"><span data-stu-id="45d91-160">**linePickup**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> </dl>

 

 




