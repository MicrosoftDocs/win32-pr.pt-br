---
description: A \_ mensagem de LINEDEVSTATE de linha TAPI é enviada quando o estado de um dispositivo de linha é alterado. O aplicativo pode invocar lineGetLineDevStatus para determinar o novo status da linha.
ms.assetid: 15f616de-db47-4577-9a47-94f9292253dd
title: Mensagem de LINE_LINEDEVSTATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 079e4494b7eb2e1bfe46b5470138e4e9f44fbb0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779304"
---
# <a name="line_linedevstate-message"></a><span data-ttu-id="614c0-104">Mensagem de LINEDEVSTATE de linha \_</span><span class="sxs-lookup"><span data-stu-id="614c0-104">LINE\_LINEDEVSTATE message</span></span>

<span data-ttu-id="614c0-105">A mensagem **de \_ LINEDEVSTATE de linha** TAPI é enviada quando o estado de um dispositivo de linha é alterado.</span><span class="sxs-lookup"><span data-stu-id="614c0-105">The TAPI **LINE\_LINEDEVSTATE** message is sent when the state of a line device has changed.</span></span> <span data-ttu-id="614c0-106">O aplicativo pode invocar [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) para determinar o novo status da linha.</span><span class="sxs-lookup"><span data-stu-id="614c0-106">The application can invoke [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) to determine the new status of the line.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="614c0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="614c0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="614c0-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="614c0-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="614c0-109">Um identificador para o dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="614c0-109">A handle to the line device.</span></span> <span data-ttu-id="614c0-110">Esse parâmetro é **nulo** quando *dwParam1* é LINEDEVSTATE \_ reinit.</span><span class="sxs-lookup"><span data-stu-id="614c0-110">This parameter is **NULL** when *dwParam1* is LINEDEVSTATE\_REINIT.</span></span>

</dd> <dt>

<span data-ttu-id="614c0-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="614c0-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="614c0-112">A instância de retorno de chamada fornecida ao abrir a linha.</span><span class="sxs-lookup"><span data-stu-id="614c0-112">The callback instance supplied when opening the line.</span></span> <span data-ttu-id="614c0-113">Se o parâmetro *dwParam1* for LINEDEVSTATE \_ REINIT, o parâmetro *dwCallBackInstance* não será válido e será definido como zero.</span><span class="sxs-lookup"><span data-stu-id="614c0-113">If the *dwParam1* parameter is LINEDEVSTATE\_REINIT, the *dwCallbackInstance* parameter is not valid and is set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="614c0-114">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="614c0-114">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="614c0-115">O item de status do dispositivo de linha que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="614c0-115">The line device status item that has changed.</span></span> <span data-ttu-id="614c0-116">O parâmetro pode ser uma ou mais das [**\_ constantes LINEDEVSTATE**](linedevstate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="614c0-116">The parameter can be one or more of the [**LINEDEVSTATE\_ constants**](linedevstate--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="614c0-117">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="614c0-117">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="614c0-118">A interpretação desse parâmetro depende do valor de *dwParam1*.</span><span class="sxs-lookup"><span data-stu-id="614c0-118">The interpretation of this parameter depends on the value of *dwParam1*.</span></span> <span data-ttu-id="614c0-119">Se *dwParam1* for LINEDEVSTATE \_ tocando, *dwParam2* conterá o modo de anel com o qual a opção instrui a linha a tocar.</span><span class="sxs-lookup"><span data-stu-id="614c0-119">If *dwParam1* is LINEDEVSTATE\_RINGING, *dwParam2* contains the ring mode with which the switch instructs the line to ring.</span></span> <span data-ttu-id="614c0-120">Os modos de toque válidos são números no intervalo um para **dwNumRingModes**, em que **dwNumRingModes** é uma funcionalidade de dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="614c0-120">Valid ring modes are numbers in the range one to **dwNumRingModes**, where **dwNumRingModes** is a line device capability.</span></span>

<span data-ttu-id="614c0-121">Se *dwParam1* for LINEDEVSTATE \_ reinit e a mensagem tiver sido emitida pela TAPI como resultado da conversão de uma nova mensagem de API em uma mensagem de reinicialização, *dwParam2* conterá o parâmetro *dwMsg* da mensagem original (por exemplo, [**linha \_ Create**](line-create.md) ou line \_ LINEDEVSTATE).</span><span class="sxs-lookup"><span data-stu-id="614c0-121">If *dwParam1* is LINEDEVSTATE\_REINIT, and the message was issued by TAPI as a result of translation of a new API message into a REINIT message, then *dwParam2* contains the *dwMsg* parameter of the original message (for example, [**LINE\_CREATE**](line-create.md) or LINE\_LINEDEVSTATE).</span></span> <span data-ttu-id="614c0-122">Se *dwParam2* for zero, isso indica que a mensagem de reinicialização é uma mensagem de reinicialização "real" que exige que o aplicativo chame [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown) de sua primeira conveniência.</span><span class="sxs-lookup"><span data-stu-id="614c0-122">If *dwParam2* is zero, this indicates that the REINIT message is a "real" REINIT message that requires the application to call [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown) at its earliest convenience.</span></span>

</dd> <dt>

<span data-ttu-id="614c0-123">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="614c0-123">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="614c0-124">A interpretação desse parâmetro depende do valor de *dwParam1*.</span><span class="sxs-lookup"><span data-stu-id="614c0-124">The interpretation of this parameter depends on the value of *dwParam1*.</span></span> <span data-ttu-id="614c0-125">Se *dwParam1* for LINEDEVSTATE \_ tocando, *dwParam3* conterá a contagem de anéis para este evento de toque.</span><span class="sxs-lookup"><span data-stu-id="614c0-125">If *dwParam1* is LINEDEVSTATE\_RINGING, *dwParam3* contains the ring count for this ring event.</span></span> <span data-ttu-id="614c0-126">A contagem de anéis começa em zero.</span><span class="sxs-lookup"><span data-stu-id="614c0-126">The ring count starts at zero.</span></span>

<span data-ttu-id="614c0-127">Se *dwParam1* for LINEDEVSTATE \_ reinit e a mensagem tiver sido emitida pela TAPI como resultado da conversão de uma nova mensagem de API em uma mensagem de reinicialização, *dwParam3* conterá o parâmetro *dwParam1* da mensagem original (por exemplo, LINEDEVSTATE \_ TRANSLATECHANGE ou algum outro \_ valor LINEDEVSTATE, se *dwParam2* for line \_ LINEDEVSTATE ou o novo identificador de dispositivo, se *dwParam2* for [**line \_ Create**](line-create.md)).</span><span class="sxs-lookup"><span data-stu-id="614c0-127">If *dwParam1* is LINEDEVSTATE\_REINIT, and the message was issued by TAPI as a result of translation of a new API message into a REINIT message, then *dwParam3* contains the *dwParam1* parameter of the original message (for example, LINEDEVSTATE\_TRANSLATECHANGE or some other LINEDEVSTATE\_ value, if *dwParam2* is LINE\_LINEDEVSTATE, or the new device identifier, if *dwParam2* is [**LINE\_CREATE**](line-create.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="614c0-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="614c0-128">Return value</span></span>

<span data-ttu-id="614c0-129">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="614c0-129">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="614c0-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="614c0-130">Remarks</span></span>

<span data-ttu-id="614c0-131">O envio da mensagem **\_ LINEDEVSTATE de linha** pode ser controlado com [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span><span class="sxs-lookup"><span data-stu-id="614c0-131">The sending of the **LINE\_LINEDEVSTATE** message can be controlled with [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span></span> <span data-ttu-id="614c0-132">Um aplicativo pode indicar alterações de item de status sobre as quais deseja ser notificado.</span><span class="sxs-lookup"><span data-stu-id="614c0-132">An application can indicate status item changes about which it wants to be notified.</span></span> <span data-ttu-id="614c0-133">Por padrão, todos os relatórios de status são desabilitados, exceto para \_ REinicialização de LINEDEVSTATE, que não pode ser desabilitado.</span><span class="sxs-lookup"><span data-stu-id="614c0-133">By default, all status reporting is disabled except for LINEDEVSTATE\_REINIT, which cannot be disabled.</span></span> <span data-ttu-id="614c0-134">Essa mensagem é enviada para todos os aplicativos que têm um identificador para a linha, incluindo aqueles que chamaram [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) com o parâmetro *DWPRIVILEGES* definido como LINECALLPRIVILEGE \_ None, LINECALLPRIVILEGE \_ Owner, LINECALLPRIVILEGE \_ Monitor ou as combinações permitidas desses.</span><span class="sxs-lookup"><span data-stu-id="614c0-134">This message is sent to all applications that have a handle to the line, including those that called [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) with the *dwPrivileges* parameter set to LINECALLPRIVILEGE\_NONE, LINECALLPRIVILEGE\_OWNER, LINECALLPRIVILEGE\_MONITOR, or permitted combinations of these.</span></span>

## <a name="requirements"></a><span data-ttu-id="614c0-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="614c0-135">Requirements</span></span>



| <span data-ttu-id="614c0-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="614c0-136">Requirement</span></span> | <span data-ttu-id="614c0-137">Valor</span><span class="sxs-lookup"><span data-stu-id="614c0-137">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="614c0-138">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="614c0-138">TAPI version</span></span><br/> | <span data-ttu-id="614c0-139">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="614c0-139">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="614c0-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="614c0-140">Header</span></span><br/>       | <dl> <span data-ttu-id="614c0-141"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="614c0-141"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="614c0-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="614c0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="614c0-143">**fechamento de linha \_**</span><span class="sxs-lookup"><span data-stu-id="614c0-143">**LINE\_CLOSE**</span></span>](line-close.md)
</dt> <dt>

[<span data-ttu-id="614c0-144">**criação de linha \_**</span><span class="sxs-lookup"><span data-stu-id="614c0-144">**LINE\_CREATE**</span></span>](line-create.md)
</dt> <dt>

[<span data-ttu-id="614c0-145">**LINEDEVCAPS**</span><span class="sxs-lookup"><span data-stu-id="614c0-145">**LINEDEVCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[<span data-ttu-id="614c0-146">**lineGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="614c0-146">**lineGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)
</dt> <dt>

[<span data-ttu-id="614c0-147">**lineGetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="614c0-147">**lineGetDevConfig**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)
</dt> <dt>

[<span data-ttu-id="614c0-148">**lineGetTranslateCaps**</span><span class="sxs-lookup"><span data-stu-id="614c0-148">**lineGetTranslateCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)
</dt> <dt>

[<span data-ttu-id="614c0-149">**lineInitialize**</span><span class="sxs-lookup"><span data-stu-id="614c0-149">**lineInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[<span data-ttu-id="614c0-150">**lineOpen**</span><span class="sxs-lookup"><span data-stu-id="614c0-150">**lineOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[<span data-ttu-id="614c0-151">**lineSetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="614c0-151">**lineSetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)
</dt> <dt>

[<span data-ttu-id="614c0-152">**lineShutdown**</span><span class="sxs-lookup"><span data-stu-id="614c0-152">**lineShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> <dt>

[<span data-ttu-id="614c0-153">**LINETRANSLATECAPS**</span><span class="sxs-lookup"><span data-stu-id="614c0-153">**LINETRANSLATECAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps)
</dt> <dt>

[<span data-ttu-id="614c0-154">**lineUncompleteCall**</span><span class="sxs-lookup"><span data-stu-id="614c0-154">**lineUncompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall)
</dt> </dl>

 

 




