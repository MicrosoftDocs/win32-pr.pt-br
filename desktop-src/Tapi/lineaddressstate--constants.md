---
description: As \_ constantes de sinalizador de bit LINEADDRESSSTATE descrevem vários itens de status de endereço.
ms.assetid: f06140d0-f41a-4228-93c5-21d609af5473
title: Constantes de LINEADDRESSSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 483ac665c41989c65b43419442601dfb70667dc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788052"
---
# <a name="lineaddressstate_-constants"></a><span data-ttu-id="40766-103">\_Constantes LINEADDRESSSTATE</span><span class="sxs-lookup"><span data-stu-id="40766-103">LINEADDRESSSTATE\_ Constants</span></span>

<span data-ttu-id="40766-104">As constantes de sinalizador de bit **LINEADDRESSSTATE \_** descrevem vários itens de status de endereço.</span><span class="sxs-lookup"><span data-stu-id="40766-104">The **LINEADDRESSSTATE\_** bit-flag constants describe various address status items.</span></span>

<dl> <dt>

<span data-ttu-id="40766-105"><span id="LINEADDRESSSTATE_CAPSCHANGE"></span><span id="lineaddressstate_capschange"></span>**LINEADDRESSSTATE \_ CAPSCHANGE**</span><span class="sxs-lookup"><span data-stu-id="40766-105"><span id="LINEADDRESSSTATE_CAPSCHANGE"></span><span id="lineaddressstate_capschange"></span>**LINEADDRESSSTATE\_CAPSCHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="40766-106">Indica que, devido a alterações de configuração feitas pelo usuário ou outras circunstâncias, um ou mais dos membros na estrutura [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) para o endereço foram alterados.</span><span class="sxs-lookup"><span data-stu-id="40766-106">Indicates that, due to configuration changes made by the user or other circumstances, one or more of the members in the [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) structure for the address have changed.</span></span> <span data-ttu-id="40766-107">O aplicativo deve usar [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps) para ler a estrutura atualizada.</span><span class="sxs-lookup"><span data-stu-id="40766-107">The application should use [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps) to read the updated structure.</span></span> <span data-ttu-id="40766-108">Se um provedor de serviços enviar uma mensagem [**\_ addressstate de linha**](line-addressstate.md) que contém esse valor para TAPI, a TAPI a passará para aplicativos que negociaram a TAPI versão 1,4 ou posterior; os aplicativos que negociam uma versão de API anterior receberão mensagens [**\_ LINEDEVSTATE de linha**](line-linedevstate.md) especificando LINEDEVSTATE \_ REINIT, exigindo que eles desliguem e reinicialize sua conexão com a TAPI para obter as informações atualizadas</span><span class="sxs-lookup"><span data-stu-id="40766-108">If a service provider sends a [**LINE\_ADDRESSSTATE**](line-addressstate.md) message containing this value to TAPI, TAPI will pass it along to applications that have negotiated TAPI version 1.4 or later; applications negotiating a previous API version will receive [**LINE\_LINEDEVSTATE**](line-linedevstate.md) messages specifying LINEDEVSTATE\_REINIT, requiring them to shut down and reinitialize their connection to TAPI to obtain the updated information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40766-109"><span id="LINEADDRESSSTATE_DEVSPECIFIC"></span><span id="lineaddressstate_devspecific"></span>**LINEADDRESSSTATE \_ DEVSPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="40766-109"><span id="LINEADDRESSSTATE_DEVSPECIFIC"></span><span id="lineaddressstate_devspecific"></span>**LINEADDRESSSTATE\_DEVSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="40766-110">O item específico do dispositivo do status do endereço foi alterado.</span><span class="sxs-lookup"><span data-stu-id="40766-110">The device-specific item of the address status has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40766-111"><span id="LINEADDRESSSTATE_FORWARD"></span><span id="lineaddressstate_forward"></span>**encaminhar LINEADDRESSSTATE \_**</span><span class="sxs-lookup"><span data-stu-id="40766-111"><span id="LINEADDRESSSTATE_FORWARD"></span><span id="lineaddressstate_forward"></span>**LINEADDRESSSTATE\_FORWARD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="40766-112">O status de encaminhamento do endereço foi alterado, incluindo possivelmente o número de anéis para determinar uma condição de não resposta.</span><span class="sxs-lookup"><span data-stu-id="40766-112">The forwarding status of the address has changed, including possibly the number of rings for determining a no-answer condition.</span></span> <span data-ttu-id="40766-113">O aplicativo deve verificar o status do endereço para determinar os detalhes sobre o status de encaminhamento atual do endereço.</span><span class="sxs-lookup"><span data-stu-id="40766-113">The application should check the address status to determine details about the address's current forwarding status.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40766-114"><span id="LINEADDRESSSTATE_INUSEMANY"></span><span id="lineaddressstate_inusemany"></span>**LINEADDRESSSTATE \_ INUSEMANY**</span><span class="sxs-lookup"><span data-stu-id="40766-114"><span id="LINEADDRESSSTATE_INUSEMANY"></span><span id="lineaddressstate_inusemany"></span>**LINEADDRESSSTATE\_INUSEMANY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="40766-115">O endereço monitorado ou com ponte mudou de sendo usado por uma estação para estar em uso por mais de uma estação.</span><span class="sxs-lookup"><span data-stu-id="40766-115">The monitored or bridged address has changed from being in use by one station to being in use by more than one station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40766-116"><span id="LINEADDRESSSTATE_INUSEONE"></span><span id="lineaddressstate_inuseone"></span>**LINEADDRESSSTATE \_ INUSEONE**</span><span class="sxs-lookup"><span data-stu-id="40766-116"><span id="LINEADDRESSSTATE_INUSEONE"></span><span id="lineaddressstate_inuseone"></span>**LINEADDRESSSTATE\_INUSEONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="40766-117">O endereço mudou de ocioso ou em uso por muitas estações de ponte para estar em uso por apenas uma estação.</span><span class="sxs-lookup"><span data-stu-id="40766-117">The address has changed from idle or in use by many bridged stations to being in use by just one station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40766-118"><span id="LINEADDRESSSTATE_INUSEZERO"></span><span id="lineaddressstate_inusezero"></span>**LINEADDRESSSTATE \_ INUSEZERO**</span><span class="sxs-lookup"><span data-stu-id="40766-118"><span id="LINEADDRESSSTATE_INUSEZERO"></span><span id="lineaddressstate_inusezero"></span>**LINEADDRESSSTATE\_INUSEZERO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="40766-119">O endereço foi alterado para ocioso (ele não está em uso por nenhuma estação).</span><span class="sxs-lookup"><span data-stu-id="40766-119">The address has changed to idle (it is not in use by any stations).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40766-120"><span id="LINEADDRESSSTATE_NUMCALLS"></span><span id="lineaddressstate_numcalls"></span>**LINEADDRESSSTATE \_ NUMCALLS**</span><span class="sxs-lookup"><span data-stu-id="40766-120"><span id="LINEADDRESSSTATE_NUMCALLS"></span><span id="lineaddressstate_numcalls"></span>**LINEADDRESSSTATE\_NUMCALLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="40766-121">O número de chamadas no endereço foi alterado.</span><span class="sxs-lookup"><span data-stu-id="40766-121">The number of calls on the address has changed.</span></span> <span data-ttu-id="40766-122">Esse é o resultado de eventos como uma nova chamada de entrada, uma chamada de saída no endereço ou uma chamada que altera seu status de espera.</span><span class="sxs-lookup"><span data-stu-id="40766-122">This is the result of events such as a new incoming call, an outgoing call on the address, or a call changing its hold status.</span></span> <span data-ttu-id="40766-123">Esse sinalizador aborda as alterações em qualquer um dos membros **dwNumActiveCalls**, **dwNumOnHoldCalls** e **dwNumOnHoldPendingCalls** na estrutura [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) .</span><span class="sxs-lookup"><span data-stu-id="40766-123">This flag covers changes in any of the members **dwNumActiveCalls**, **dwNumOnHoldCalls** and **dwNumOnHoldPendingCalls** in the [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) structure.</span></span> <span data-ttu-id="40766-124">O aplicativo deve verificar todos esses três membros ao receber uma mensagem de [**\_ endereço de linhastate**](line-addressstate.md) (numCalls).</span><span class="sxs-lookup"><span data-stu-id="40766-124">The application should check all three of these members when it receives a [**LINE\_ADDRESSSTATE**](line-addressstate.md) (numCalls) message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40766-125"><span id="LINEADDRESSSTATE_OTHER"></span><span id="lineaddressstate_other"></span>**LINEADDRESSSTATE \_ outros**</span><span class="sxs-lookup"><span data-stu-id="40766-125"><span id="LINEADDRESSSTATE_OTHER"></span><span id="lineaddressstate_other"></span>**LINEADDRESSSTATE\_OTHER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="40766-126">Os itens de status de endereço diferentes daqueles listados abaixo foram alterados.</span><span class="sxs-lookup"><span data-stu-id="40766-126">Address-status items other than those listed below have changed.</span></span> <span data-ttu-id="40766-127">O aplicativo deve verificar o status do endereço atual para determinar quais itens foram alterados.</span><span class="sxs-lookup"><span data-stu-id="40766-127">The application should check the current address status to determine which items have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40766-128"><span id="LINEADDRESSSTATE_TERMINALS"></span><span id="lineaddressstate_terminals"></span>**\_terminais LINEADDRESSSTATE**</span><span class="sxs-lookup"><span data-stu-id="40766-128"><span id="LINEADDRESSSTATE_TERMINALS"></span><span id="lineaddressstate_terminals"></span>**LINEADDRESSSTATE\_TERMINALS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="40766-129">As configurações de terminal para o endereço foram alteradas.</span><span class="sxs-lookup"><span data-stu-id="40766-129">The terminal settings for the address have changed.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="40766-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="40766-130">Remarks</span></span>

<span data-ttu-id="40766-131">Sem extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="40766-131">No extensibility.</span></span> <span data-ttu-id="40766-132">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="40766-132">All 32 bits are reserved.</span></span>

<span data-ttu-id="40766-133">Um aplicativo é notificado sobre alterações nesses itens de status na [**mensagem \_ addressstate de linha**](line-addressstate.md) .</span><span class="sxs-lookup"><span data-stu-id="40766-133">An application is notified about changes to these status items in the [**LINE\_ADDRESSSTATE**](line-addressstate.md) message.</span></span> <span data-ttu-id="40766-134">Os recursos do dispositivo do endereço indicam quais alterações de estado de endereço podem possivelmente ser relatadas para esse endereço.</span><span class="sxs-lookup"><span data-stu-id="40766-134">The address's device capabilities indicate which address state changes can possibly be reported for this address.</span></span>

## <a name="requirements"></a><span data-ttu-id="40766-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40766-135">Requirements</span></span>



| <span data-ttu-id="40766-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="40766-136">Requirement</span></span> | <span data-ttu-id="40766-137">Valor</span><span class="sxs-lookup"><span data-stu-id="40766-137">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="40766-138">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="40766-138">TAPI version</span></span><br/> | <span data-ttu-id="40766-139">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="40766-139">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="40766-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="40766-140">Header</span></span><br/>       | <dl> <span data-ttu-id="40766-141"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="40766-141"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40766-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="40766-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40766-143">**Endereço de LINHAstate \_**</span><span class="sxs-lookup"><span data-stu-id="40766-143">**LINE\_ADDRESSSTATE**</span></span>](line-addressstate.md)
</dt> <dt>

[<span data-ttu-id="40766-144">**LINEDEVSTATE de linha \_**</span><span class="sxs-lookup"><span data-stu-id="40766-144">**LINE\_LINEDEVSTATE**</span></span>](line-linedevstate.md)
</dt> <dt>

[<span data-ttu-id="40766-145">**LINEADDRESSCAPS**</span><span class="sxs-lookup"><span data-stu-id="40766-145">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="40766-146">**LINEADDRESSSTATUS**</span><span class="sxs-lookup"><span data-stu-id="40766-146">**LINEADDRESSSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[<span data-ttu-id="40766-147">**lineGetAddressCaps**</span><span class="sxs-lookup"><span data-stu-id="40766-147">**lineGetAddressCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> </dl>

 

 




