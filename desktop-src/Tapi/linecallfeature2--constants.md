---
description: As \_ constantes LINECALLFEATURE2 listam os recursos complementares disponíveis para conferência, transferência e chamadas de estacionamento.
ms.assetid: 67a3b587-dd5b-4ccf-ab69-2137604706b8
title: Constantes de LINECALLFEATURE2_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 977e71f722fba34da6b2ecbd6a3e914c34a0aae5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767744"
---
# <a name="linecallfeature2_-constants"></a><span data-ttu-id="bb923-103">\_Constantes LINECALLFEATURE2</span><span class="sxs-lookup"><span data-stu-id="bb923-103">LINECALLFEATURE2\_ Constants</span></span>

<span data-ttu-id="bb923-104">As **constantes \_ LINECALLFEATURE2** listam os recursos complementares disponíveis para conferência, transferência e chamadas de estacionamento.</span><span class="sxs-lookup"><span data-stu-id="bb923-104">The **LINECALLFEATURE2\_** constants list the supplemental features available for conferencing, transferring, and parking calls.</span></span>

<dl> <dt>

<span data-ttu-id="bb923-105"><span id="LINECALLFEATURE2_COMPLCALLBACK"></span><span id="linecallfeature2_complcallback"></span>**LINECALLFEATURE2 \_ COMPLCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="bb923-105"><span id="LINECALLFEATURE2_COMPLCALLBACK"></span><span id="linecallfeature2_complcallback"></span>**LINECALLFEATURE2\_COMPLCALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bb923-106">Se esse bit estiver ativado, o recurso de "retorno de chamada" poderá ser invocado usando a \_ opção de retorno de chamada LINECOMPLMODE com [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span><span class="sxs-lookup"><span data-stu-id="bb923-106">If this bit is on, the "callback" feature can be invoked by using the LINECOMPLMODE\_CALLBACK option with [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span></span> <span data-ttu-id="bb923-107">O LINECALLFEATURE \_ COMPLETECALL bit também estará ativado no membro **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="bb923-107">The LINECALLFEATURE\_COMPLETECALL bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bb923-108"><span id="LINECALLFEATURE2_COMPLCAMPON"></span><span id="linecallfeature2_complcampon"></span>**LINECALLFEATURE2 \_ COMPLCAMPON**</span><span class="sxs-lookup"><span data-stu-id="bb923-108"><span id="LINECALLFEATURE2_COMPLCAMPON"></span><span id="linecallfeature2_complcampon"></span>**LINECALLFEATURE2\_COMPLCAMPON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bb923-109">Se esse bit for on, o recurso "Camp on" poderá ser invocado usando a \_ opção LINECOMPLMODE Camp com [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span><span class="sxs-lookup"><span data-stu-id="bb923-109">If this bit is on, the "camp on" feature can be invoked by using the LINECOMPLMODE\_CAMPON option with [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span></span> <span data-ttu-id="bb923-110">O LINECALLFEATURE \_ COMPLETECALL bit também estará ativado no membro **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="bb923-110">The LINECALLFEATURE\_COMPLETECALL bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bb923-111"><span id="LINECALLFEATURE2_COMPLINTRUDE"></span><span id="linecallfeature2_complintrude"></span>**LINECALLFEATURE2 \_ COMPLINTRUDE**</span><span class="sxs-lookup"><span data-stu-id="bb923-111"><span id="LINECALLFEATURE2_COMPLINTRUDE"></span><span id="linecallfeature2_complintrude"></span>**LINECALLFEATURE2\_COMPLINTRUDE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bb923-112">Se esse bit for on, o recurso "intrusão" poderá ser invocado usando a \_ opção LINECOMPLMODE intruso com [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span><span class="sxs-lookup"><span data-stu-id="bb923-112">If this bit is on, the "intrude" feature can be invoked by using the LINECOMPLMODE\_INTRUDE option with [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span></span> <span data-ttu-id="bb923-113">O LINECALLFEATURE \_ COMPLETECALL bit também estará ativado no membro **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="bb923-113">The LINECALLFEATURE\_COMPLETECALL bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bb923-114"><span id="LINECALLFEATURE2_COMPLMESSAGE"></span><span id="linecallfeature2_complmessage"></span>**LINECALLFEATURE2 \_ COMPLMESSAGE**</span><span class="sxs-lookup"><span data-stu-id="bb923-114"><span id="LINECALLFEATURE2_COMPLMESSAGE"></span><span id="linecallfeature2_complmessage"></span>**LINECALLFEATURE2\_COMPLMESSAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bb923-115">Se esse bit estiver ativado, o recurso "deixar mensagem" poderá ser invocado usando a \_ opção de mensagem LINECOMPLMODE com [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span><span class="sxs-lookup"><span data-stu-id="bb923-115">If this bit is on, the "leave message" feature can be invoked by using the LINECOMPLMODE\_MESSAGE option with [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall).</span></span> <span data-ttu-id="bb923-116">O LINECALLFEATURE \_ COMPLETECALL bit também estará ativado no membro **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="bb923-116">The LINECALLFEATURE\_COMPLETECALL bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bb923-117"><span id="LINECALLFEATURE2_NOHOLDCONFERENCE"></span><span id="linecallfeature2_noholdconference"></span>**LINECALLFEATURE2 \_ NOHOLDCONFERENCE**</span><span class="sxs-lookup"><span data-stu-id="bb923-117"><span id="LINECALLFEATURE2_NOHOLDCONFERENCE"></span><span id="linecallfeature2_noholdconference"></span>**LINECALLFEATURE2\_NOHOLDCONFERENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bb923-118">Se esse bit estiver ativado, uma "nenhuma conferência de retenção" poderá ser criada usando a \_ opção LINECALLPARAMFLAGS NOHOLDCONFERENCE com [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference).</span><span class="sxs-lookup"><span data-stu-id="bb923-118">If this bit is on, a "no hold conference" can be created by using the LINECALLPARAMFLAGS\_NOHOLDCONFERENCE option with [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference).</span></span> <span data-ttu-id="bb923-119">O LINECALLFEATURE \_ SETUPCONF bit também estará ativado no membro **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="bb923-119">The LINECALLFEATURE\_SETUPCONF bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bb923-120"><span id="LINECALLFEATURE2_ONESTEPTRANSFER"></span><span id="linecallfeature2_onesteptransfer"></span>**LINECALLFEATURE2 \_ ONESTEPTRANSFER**</span><span class="sxs-lookup"><span data-stu-id="bb923-120"><span id="LINECALLFEATURE2_ONESTEPTRANSFER"></span><span id="linecallfeature2_onesteptransfer"></span>**LINECALLFEATURE2\_ONESTEPTRANSFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bb923-121">Se esse bit estiver ativado, a "transferência de uma etapa" poderá ser criada usando a \_ opção LINECALLPARAMFLAGS ONESTEPTRANSFER com [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer).</span><span class="sxs-lookup"><span data-stu-id="bb923-121">If this bit is on, "one step transfer" can be created by using the LINECALLPARAMFLAGS\_ONESTEPTRANSFER option with [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer).</span></span> <span data-ttu-id="bb923-122">O LINECALLFEATURE \_ SETUPTRANSFER bit também estará ativado no membro **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="bb923-122">The LINECALLFEATURE\_SETUPTRANSFER bit will also be on in the **dwCallFeatures** member.</span></span>

> [!Note]  
> <span data-ttu-id="bb923-123">Se nenhum dos bits "COMPr" for especificado no membro **dwCallFeatures2** em [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) , mas LINECALLFEATURE \_ COMPLETECALL for especificado, será possível que qualquer um deles funcione, mas o provedor de serviços não especificou que.</span><span class="sxs-lookup"><span data-stu-id="bb923-123">If none of the "COMPL" bits is specified in the **dwCallFeatures2** member in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) but LINECALLFEATURE\_COMPLETECALL is specified, then it is possible that any of them will work, but the service provider has not specified which.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="bb923-124"><span id="LINECALLFEATURE2_TRANSFERCONF"></span><span id="linecallfeature2_transferconf"></span>**LINECALLFEATURE2 \_ TRANSFERCONF**</span><span class="sxs-lookup"><span data-stu-id="bb923-124"><span id="LINECALLFEATURE2_TRANSFERCONF"></span><span id="linecallfeature2_transferconf"></span>**LINECALLFEATURE2\_TRANSFERCONF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bb923-125">Se esse bit for on, a função [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) poderá ser usada para resolver a transferência como uma conferência de três vias.</span><span class="sxs-lookup"><span data-stu-id="bb923-125">If this bit is on, the [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) function can be used to resolve the transfer as a three-way conference.</span></span> <span data-ttu-id="bb923-126">O LINECALLFEATURE \_ COMPLETETRANSF bit também estará ativado no membro **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="bb923-126">The LINECALLFEATURE\_COMPLETETRANSF bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bb923-127"><span id="LINECALLFEATURE2_TRANSFERNORM"></span><span id="linecallfeature2_transfernorm"></span>**LINECALLFEATURE2 \_ TRANSFERNORM**</span><span class="sxs-lookup"><span data-stu-id="bb923-127"><span id="LINECALLFEATURE2_TRANSFERNORM"></span><span id="linecallfeature2_transfernorm"></span>**LINECALLFEATURE2\_TRANSFERNORM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bb923-128">Se esse bit for on, a função [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) poderá ser usada para resolver a transferência como uma transferência normal.</span><span class="sxs-lookup"><span data-stu-id="bb923-128">If this bit is on, the [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) function can be used to resolve the transfer as a normal transfer.</span></span> <span data-ttu-id="bb923-129">O LINECALLFEATURE \_ COMPLETETRANSF bit também estará ativado no membro **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="bb923-129">The LINECALLFEATURE\_COMPLETETRANSF bit will also be on in the **dwCallFeatures** member.</span></span>

> [!Note]  
> <span data-ttu-id="bb923-130">Se nem TRANSFERNORM nem TRANSFERCONF forem especificados no membro **dwCallFeatures2** em [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) , mas LINECALLFEATURE \_ COMPLETETRANSF for especificado, será possível que ele funcione, mas o provedor de serviços não especificou que.</span><span class="sxs-lookup"><span data-stu-id="bb923-130">If neither TRANSFERNORM nor TRANSFERCONF is specified in the **dwCallFeatures2** member in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) but LINECALLFEATURE\_COMPLETETRANSF is specified, then it is possible that either will work, but the service provider has not specified which.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="bb923-131"><span id="LINECALLFEATURE2_PARKDIRECT"></span><span id="linecallfeature2_parkdirect"></span>**LINECALLFEATURE2 \_ PARKDIRECT**</span><span class="sxs-lookup"><span data-stu-id="bb923-131"><span id="LINECALLFEATURE2_PARKDIRECT"></span><span id="linecallfeature2_parkdirect"></span>**LINECALLFEATURE2\_PARKDIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bb923-132">Se esse bit estiver ativado, o recurso "Parque direcionado" poderá ser invocado usando a \_ opção direcionada LINEPARKMODE com [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark).</span><span class="sxs-lookup"><span data-stu-id="bb923-132">If this bit is on, the "directed park" feature can be invoked by using the LINEPARKMODE\_DIRECTED option with [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark).</span></span> <span data-ttu-id="bb923-133">O \_ bit LINECALLFEATURE Park também estará ativado no membro **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="bb923-133">The LINECALLFEATURE\_PARK bit will also be on in the **dwCallFeatures** member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bb923-134"><span id="LINECALLFEATURE2_PARKNONDIRECT"></span><span id="linecallfeature2_parknondirect"></span>**LINECALLFEATURE2 \_ PARKNONDIRECT**</span><span class="sxs-lookup"><span data-stu-id="bb923-134"><span id="LINECALLFEATURE2_PARKNONDIRECT"></span><span id="linecallfeature2_parknondirect"></span>**LINECALLFEATURE2\_PARKNONDIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bb923-135">Se esse bit estiver ativado, o recurso "Parque não direcionado" poderá ser invocado usando a \_ opção não direcionada LINEPARKMODE com [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark).</span><span class="sxs-lookup"><span data-stu-id="bb923-135">If this bit is on, the "non-directed park" feature can be invoked by using the LINEPARKMODE\_NONDIRECTED option with [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark).</span></span> <span data-ttu-id="bb923-136">O \_ bit LINECALLFEATURE Park também estará ativado no membro **dwCallFeatures** .</span><span class="sxs-lookup"><span data-stu-id="bb923-136">The LINECALLFEATURE\_PARK bit will also be on in the **dwCallFeatures** member.</span></span>

> [!Note]  
> <span data-ttu-id="bb923-137">Se nem PARKDIRECT nem PARKNONDIRECT forem especificados no membro **dwCallFeatures2** em [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) , mas \_ o parque LINECALLFEATURE for especificado, será possível que ele funcione, mas o provedor de serviços não especificou que.</span><span class="sxs-lookup"><span data-stu-id="bb923-137">If neither PARKDIRECT nor PARKNONDIRECT is specified in the **dwCallFeatures2** member in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) but LINECALLFEATURE\_PARK is specified, then it is possible that either will work, but the service provider has not specified which.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bb923-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb923-138">Requirements</span></span>



| <span data-ttu-id="bb923-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb923-139">Requirement</span></span> | <span data-ttu-id="bb923-140">Valor</span><span class="sxs-lookup"><span data-stu-id="bb923-140">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="bb923-141">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="bb923-141">TAPI version</span></span><br/> | <span data-ttu-id="bb923-142">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="bb923-142">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="bb923-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bb923-143">Header</span></span><br/>       | <dl> <span data-ttu-id="bb923-144"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb923-144"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb923-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb923-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb923-146">**LINECALLSTATUS**</span><span class="sxs-lookup"><span data-stu-id="bb923-146">**LINECALLSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[<span data-ttu-id="bb923-147">**lineCompleteCall**</span><span class="sxs-lookup"><span data-stu-id="bb923-147">**lineCompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)
</dt> <dt>

[<span data-ttu-id="bb923-148">**lineCompleteTransfer**</span><span class="sxs-lookup"><span data-stu-id="bb923-148">**lineCompleteTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[<span data-ttu-id="bb923-149">**linePark**</span><span class="sxs-lookup"><span data-stu-id="bb923-149">**linePark**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepark)
</dt> <dt>

[<span data-ttu-id="bb923-150">**lineSetupConference**</span><span class="sxs-lookup"><span data-stu-id="bb923-150">**lineSetupConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)
</dt> <dt>

[<span data-ttu-id="bb923-151">**lineSetupTransfer**</span><span class="sxs-lookup"><span data-stu-id="bb923-151">**lineSetupTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> </dl>

 

 




