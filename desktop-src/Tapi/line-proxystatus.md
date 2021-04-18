---
description: A mensagem de linha \_ PROXYSTATUS é enviada quando os proxies disponíveis são alterados em uma linha que o aplicativo abriu atualmente.
ms.assetid: e20d4b48-a72a-4a83-ae04-a608791a1a3a
title: Mensagem de LINE_PROXYSTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb00c5df4f531309bdd1311fb7c34c3e9967a8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753343"
---
# <a name="line_proxystatus-message"></a><span data-ttu-id="bf164-103">Mensagem de PROXYSTATUS de linha \_</span><span class="sxs-lookup"><span data-stu-id="bf164-103">LINE\_PROXYSTATUS message</span></span>

<span data-ttu-id="bf164-104">A mensagem de **linha \_ PROXYSTATUS** é enviada quando os proxies disponíveis são alterados em uma linha que o aplicativo abriu atualmente.</span><span class="sxs-lookup"><span data-stu-id="bf164-104">The **LINE\_PROXYSTATUS** message is sent when the available proxies change on a line that the application currently has open.</span></span>

<span data-ttu-id="bf164-105">TAPISRV gera essa mensagem durante uma função [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) usando LINEPROXYSTATUS \_ Open e LINEPROXYSTATUS \_ ALLOPENFORACD ou uma função [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose) usando LINEPROXYSTATUS \_ Close (todas as [**\_ constantes LINEPROXYSTATUS**](lineproxystatus--constants.md)).</span><span class="sxs-lookup"><span data-stu-id="bf164-105">TAPISRV generates this message during a [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) function using LINEPROXYSTATUS\_OPEN and LINEPROXYSTATUS\_ALLOPENFORACD or a [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose) function using LINEPROXYSTATUS\_CLOSE (all [**LINEPROXYSTATUS\_ Constants**](lineproxystatus--constants.md)).</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="bf164-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bf164-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf164-107">*dwDevice*</span><span class="sxs-lookup"><span data-stu-id="bf164-107">*dwDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="bf164-108">O identificador do aplicativo para o dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="bf164-108">The application's handle to the line device.</span></span> <span data-ttu-id="bf164-109">Isso está relacionado ao manipulador do agente.</span><span class="sxs-lookup"><span data-stu-id="bf164-109">This relates to the agent handler.</span></span>

</dd> <dt>

<span data-ttu-id="bf164-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="bf164-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="bf164-111">A instância de retorno de chamada fornecida ao abrir a linha.</span><span class="sxs-lookup"><span data-stu-id="bf164-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="bf164-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="bf164-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="bf164-113">Especifica o status da fila que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="bf164-113">Specifies the queue status that has changed.</span></span> <span data-ttu-id="bf164-114">Pode ser uma ou mais das [**\_ constantes LINEPROXYSTATUS**](lineproxystatus--constants.md).</span><span class="sxs-lookup"><span data-stu-id="bf164-114">Can be one or more of the [**LINEPROXYSTATUS\_ constants**](lineproxystatus--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf164-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="bf164-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="bf164-116">Se *dwParam1* for definido como LINEPROXYSTATUS \_ Open ou LINEPROXYSTATUS \_ Close, *dwParam2* indicará o tipo de solicitação de proxy relacionado, que é um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="bf164-116">If *dwParam1* is set to LINEPROXYSTATUS\_OPEN or LINEPROXYSTATUS\_CLOSE, *dwParam2* indicates the related proxy request type, which is one of the following:</span></span>

-   <span data-ttu-id="bf164-117">LINEPROXYREQUEST \_ SETagent</span><span class="sxs-lookup"><span data-stu-id="bf164-117">LINEPROXYREQUEST\_SETAGENTGROUP</span></span>
-   <span data-ttu-id="bf164-118">LINEPROXYREQUEST \_ SETagentstate</span><span class="sxs-lookup"><span data-stu-id="bf164-118">LINEPROXYREQUEST\_SETAGENTSTATE</span></span>
-   <span data-ttu-id="bf164-119">LINEPROXYREQUEST \_ SETAGENTACTIVITY</span><span class="sxs-lookup"><span data-stu-id="bf164-119">LINEPROXYREQUEST\_SETAGENTACTIVITY</span></span>
-   <span data-ttu-id="bf164-120">LINEPROXYREQUEST \_ GETAGENTCAPS</span><span class="sxs-lookup"><span data-stu-id="bf164-120">LINEPROXYREQUEST\_GETAGENTCAPS</span></span>
-   <span data-ttu-id="bf164-121">LINEPROXYREQUEST \_ GETAGENTSTATUS</span><span class="sxs-lookup"><span data-stu-id="bf164-121">LINEPROXYREQUEST\_GETAGENTSTATUS</span></span>
-   <span data-ttu-id="bf164-122">LINEPROXYREQUEST \_ AGENTSPECIFIC</span><span class="sxs-lookup"><span data-stu-id="bf164-122">LINEPROXYREQUEST\_AGENTSPECIFIC</span></span>
-   <span data-ttu-id="bf164-123">LINEPROXYREQUEST \_ GETAGENTACTIVITYLIST</span><span class="sxs-lookup"><span data-stu-id="bf164-123">LINEPROXYREQUEST\_GETAGENTACTIVITYLIST</span></span>
-   <span data-ttu-id="bf164-124">LINEPROXYREQUEST \_ GETAGENTGROUPLIST</span><span class="sxs-lookup"><span data-stu-id="bf164-124">LINEPROXYREQUEST\_GETAGENTGROUPLIST</span></span>
-   <span data-ttu-id="bf164-125">CreateAgent do LINEPROXYREQUEST \_</span><span class="sxs-lookup"><span data-stu-id="bf164-125">LINEPROXYREQUEST\_CREATEAGENT</span></span>
-   <span data-ttu-id="bf164-126">LINEPROXYREQUEST \_ SETAGENTMEASUREMENTPERIOD</span><span class="sxs-lookup"><span data-stu-id="bf164-126">LINEPROXYREQUEST\_SETAGENTMEASUREMENTPERIOD</span></span>
-   <span data-ttu-id="bf164-127">LINEPROXYREQUEST \_ GETAGENTINFO</span><span class="sxs-lookup"><span data-stu-id="bf164-127">LINEPROXYREQUEST\_GETAGENTINFO</span></span>
-   <span data-ttu-id="bf164-128">LINEPROXYREQUEST \_ CREATEAGENTSESSION</span><span class="sxs-lookup"><span data-stu-id="bf164-128">LINEPROXYREQUEST\_CREATEAGENTSESSION</span></span>
-   <span data-ttu-id="bf164-129">LINEPROXYREQUEST \_ GETAGENTSESSIONLIST</span><span class="sxs-lookup"><span data-stu-id="bf164-129">LINEPROXYREQUEST\_GETAGENTSESSIONLIST</span></span>
-   <span data-ttu-id="bf164-130">LINEPROXYREQUEST \_ SETAGENTSESSIONSTATE</span><span class="sxs-lookup"><span data-stu-id="bf164-130">LINEPROXYREQUEST\_SETAGENTSESSIONSTATE</span></span>
-   <span data-ttu-id="bf164-131">LINEPROXYREQUEST \_ GETAGENTSESSIONINFO</span><span class="sxs-lookup"><span data-stu-id="bf164-131">LINEPROXYREQUEST\_GETAGENTSESSIONINFO</span></span>
-   <span data-ttu-id="bf164-132">LINEPROXYREQUEST \_ GETqueuelist</span><span class="sxs-lookup"><span data-stu-id="bf164-132">LINEPROXYREQUEST\_GETQUEUELIST</span></span>
-   <span data-ttu-id="bf164-133">LINEPROXYREQUEST \_ SETQUEUEMEASUREMENTPERIOD</span><span class="sxs-lookup"><span data-stu-id="bf164-133">LINEPROXYREQUEST\_SETQUEUEMEASUREMENTPERIOD</span></span>
-   <span data-ttu-id="bf164-134">LINEPROXYREQUEST \_ GETQUEUEINFO</span><span class="sxs-lookup"><span data-stu-id="bf164-134">LINEPROXYREQUEST\_GETQUEUEINFO</span></span>
-   <span data-ttu-id="bf164-135">LINEPROXYREQUEST \_ GETgrouplist</span><span class="sxs-lookup"><span data-stu-id="bf164-135">LINEPROXYREQUEST\_GETGROUPLIST</span></span>
-   <span data-ttu-id="bf164-136">LINEPROXYREQUEST \_ SETAGENTSTATEEX</span><span class="sxs-lookup"><span data-stu-id="bf164-136">LINEPROXYREQUEST\_SETAGENTSTATEEX</span></span>

<span data-ttu-id="bf164-137">Caso contrário, *dwParam2* será definido como zero.</span><span class="sxs-lookup"><span data-stu-id="bf164-137">Otherwise, *dwParam2* is set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="bf164-138">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="bf164-138">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="bf164-139">Reservado.</span><span class="sxs-lookup"><span data-stu-id="bf164-139">Reserved.</span></span> <span data-ttu-id="bf164-140">Definido como zero.</span><span class="sxs-lookup"><span data-stu-id="bf164-140">Set to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bf164-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf164-141">Requirements</span></span>



| <span data-ttu-id="bf164-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf164-142">Requirement</span></span> | <span data-ttu-id="bf164-143">Valor</span><span class="sxs-lookup"><span data-stu-id="bf164-143">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="bf164-144">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="bf164-144">TAPI version</span></span><br/> | <span data-ttu-id="bf164-145">Requer TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="bf164-145">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="bf164-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bf164-146">Header</span></span><br/>       | <dl> <span data-ttu-id="bf164-147"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf164-147"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf164-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf164-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf164-149">**lineOpen**</span><span class="sxs-lookup"><span data-stu-id="bf164-149">**lineOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[<span data-ttu-id="bf164-150">**lineClose**</span><span class="sxs-lookup"><span data-stu-id="bf164-150">**lineClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[<span data-ttu-id="bf164-151">**PROXYREQUEST de linha \_**</span><span class="sxs-lookup"><span data-stu-id="bf164-151">**LINE\_PROXYREQUEST**</span></span>](line-proxyrequest.md)
</dt> <dt>

[<span data-ttu-id="bf164-152">**\_Constantes LINEPROXYREQUEST**</span><span class="sxs-lookup"><span data-stu-id="bf164-152">**LINEPROXYREQUEST\_ Constants**</span></span>](lineproxyrequest--constants.md)
</dt> </dl>

 

 




