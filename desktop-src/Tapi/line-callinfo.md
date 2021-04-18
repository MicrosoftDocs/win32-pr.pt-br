---
description: A mensagem de CALLINFO de linha TAPI \_ é enviada quando as informações de chamada sobre a chamada especificada foram alteradas. O aplicativo pode invocar lineGetCallInfo para determinar as informações de chamada atuais.
ms.assetid: eb882409-6842-434e-9f93-61cf0c11d1d0
title: Mensagem de LINE_CALLINFO (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6005ab5383816ead440f5a1a7d580bfaccb5c1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105792620"
---
# <a name="line_callinfo-message"></a><span data-ttu-id="5676f-104">Mensagem de CALLINFO de linha \_</span><span class="sxs-lookup"><span data-stu-id="5676f-104">LINE\_CALLINFO message</span></span>

<span data-ttu-id="5676f-105">A mensagem **de \_ CALLINFO de linha** TAPI é enviada quando as informações de chamada sobre a chamada especificada foram alteradas.</span><span class="sxs-lookup"><span data-stu-id="5676f-105">The TAPI **LINE\_CALLINFO** message is sent when the call information about the specified call has changed.</span></span> <span data-ttu-id="5676f-106">O aplicativo pode invocar [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) para determinar as informações de chamada atuais.</span><span class="sxs-lookup"><span data-stu-id="5676f-106">The application can invoke [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) to determine the current call information.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="5676f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5676f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5676f-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="5676f-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="5676f-109">Um identificador para a chamada.</span><span class="sxs-lookup"><span data-stu-id="5676f-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="5676f-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="5676f-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="5676f-111">A instância de retorno de chamada fornecida ao abrir a linha do telefonema.</span><span class="sxs-lookup"><span data-stu-id="5676f-111">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="5676f-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="5676f-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="5676f-113">O item de informações de chamada que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="5676f-113">The call information item that has changed.</span></span> <span data-ttu-id="5676f-114">Pode ser uma ou mais das [**\_ constantes LINECALLINFOSTATE**](linecallinfostate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="5676f-114">Can be one or more of the [**LINECALLINFOSTATE\_ constants**](linecallinfostate--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="5676f-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="5676f-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="5676f-116">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="5676f-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="5676f-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="5676f-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="5676f-118">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="5676f-118">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5676f-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5676f-119">Return value</span></span>

<span data-ttu-id="5676f-120">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="5676f-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5676f-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="5676f-121">Remarks</span></span>

<span data-ttu-id="5676f-122">Uma mensagem de **\_ CALLINFO de linha** com uma indicação *NumOwnersIncr*, *NumOwnersDecr* e/ou *NumMonitorsChanged* é enviada para aplicativos que já têm um identificador para a chamada.</span><span class="sxs-lookup"><span data-stu-id="5676f-122">A **LINE\_CALLINFO** message with a *NumOwnersIncr*, *NumOwnersDecr*, and/or *NumMonitorsChanged* indication is sent to applications that already have a handle for the call.</span></span> <span data-ttu-id="5676f-123">Isso pode ser o resultado de outro aplicativo que altera a propriedade ou monitoração para uma chamada com [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen), [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose), [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown), [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege), [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)e [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls).</span><span class="sxs-lookup"><span data-stu-id="5676f-123">This can be the result of another application changing ownership or monitorship to a call with [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen), [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose), [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown), [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege), [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls), and [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls).</span></span>

<span data-ttu-id="5676f-124">Essas mensagens de **\_ CALLINFO de linha** não são enviadas quando uma notificação de uma nova chamada é fornecida em uma mensagem [**\_ callstate de linha**](line-callstate.md) , porque as informações de chamada já refletem o número correto de proprietários e monitores no momento em que as \_ mensagens callstate de linha são enviadas.</span><span class="sxs-lookup"><span data-stu-id="5676f-124">These **LINE\_CALLINFO** messages are not sent when a notification of a new call is provided in a [**LINE\_CALLSTATE**](line-callstate.md) message, because the call information already reflects the correct number of owners and monitors at the time the LINE\_CALLSTATE messages are sent.</span></span> <span data-ttu-id="5676f-125">**Linha \_** As mensagens CALLINFO também são suprimidas no caso em que uma chamada é oferecida pela TAPI para monitorar por meio do \_ mecanismo desconhecido de LINECALLSTATE.</span><span class="sxs-lookup"><span data-stu-id="5676f-125">**LINE\_CALLINFO** messages are also suppressed in the case where a call is offered by TAPI to monitors through the LINECALLSTATE\_UNKNOWN mechanism.</span></span>

> [!Note]  
> <span data-ttu-id="5676f-126">O aplicativo que faz uma alteração no número de proprietários ou monitores (por exemplo, invocando [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) ou [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)) não recebe uma mensagem indicando que a alteração foi feita.</span><span class="sxs-lookup"><span data-stu-id="5676f-126">The application that causes a change in the number of owners or monitors (for example, by invoking [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) or [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)) does not itself receive a message indicating that the change has been done.</span></span>

 

<span data-ttu-id="5676f-127">Nenhuma mensagem de **\_ CALLINFO de linha** é enviada para uma chamada depois que a chamada entrou no estado *ocioso* .</span><span class="sxs-lookup"><span data-stu-id="5676f-127">No **LINE\_CALLINFO** messages are sent for a call after the call has entered the *idle* state.</span></span> <span data-ttu-id="5676f-128">Especificamente, as alterações no número de proprietários e monitores não são relatadas à medida que os aplicativos desalocam seus identificadores para a chamada ociosa.</span><span class="sxs-lookup"><span data-stu-id="5676f-128">Specifically, changes in the number of owners and monitors are not reported as applications deallocate their handles for the idle call.</span></span>

## <a name="requirements"></a><span data-ttu-id="5676f-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5676f-129">Requirements</span></span>



| <span data-ttu-id="5676f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="5676f-130">Requirement</span></span> | <span data-ttu-id="5676f-131">Valor</span><span class="sxs-lookup"><span data-stu-id="5676f-131">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5676f-132">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="5676f-132">TAPI version</span></span><br/> | <span data-ttu-id="5676f-133">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="5676f-133">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="5676f-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5676f-134">Header</span></span><br/>       | <dl> <span data-ttu-id="5676f-135"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="5676f-135"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5676f-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="5676f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5676f-137">**lineClose**</span><span class="sxs-lookup"><span data-stu-id="5676f-137">**lineClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[<span data-ttu-id="5676f-138">**lineDeallocateCall**</span><span class="sxs-lookup"><span data-stu-id="5676f-138">**lineDeallocateCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall)
</dt> <dt>

[<span data-ttu-id="5676f-139">**lineGetCallInfo**</span><span class="sxs-lookup"><span data-stu-id="5676f-139">**lineGetCallInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)
</dt> <dt>

[<span data-ttu-id="5676f-140">**lineGetConfRelatedCalls**</span><span class="sxs-lookup"><span data-stu-id="5676f-140">**lineGetConfRelatedCalls**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)
</dt> <dt>

[<span data-ttu-id="5676f-141">**lineGetNewCalls**</span><span class="sxs-lookup"><span data-stu-id="5676f-141">**lineGetNewCalls**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)
</dt> <dt>

[<span data-ttu-id="5676f-142">**lineOpen**</span><span class="sxs-lookup"><span data-stu-id="5676f-142">**lineOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[<span data-ttu-id="5676f-143">**lineSetCallPrivilege**</span><span class="sxs-lookup"><span data-stu-id="5676f-143">**lineSetCallPrivilege**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)
</dt> <dt>

[<span data-ttu-id="5676f-144">**lineShutdown**</span><span class="sxs-lookup"><span data-stu-id="5676f-144">**lineShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> </dl>

 

 




