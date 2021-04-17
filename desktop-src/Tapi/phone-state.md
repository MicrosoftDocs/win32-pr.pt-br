---
description: A TAPI envia a \_ mensagem de estado do telefone para um aplicativo sempre que o status de um dispositivo de telefone é alterado.
ms.assetid: 74e74b62-8387-4056-83e6-2350b3da4077
title: Mensagem de PHONE_STATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db52f16d6c377087fd6ccadc5e70b5bb2865da2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755176"
---
# <a name="phone_state-message"></a><span data-ttu-id="7c517-103">Mensagem de estado do telefone \_</span><span class="sxs-lookup"><span data-stu-id="7c517-103">PHONE\_STATE message</span></span>

<span data-ttu-id="7c517-104">A TAPI envia a mensagem de **\_ estado do telefone** para um aplicativo sempre que o status de um dispositivo de telefone é alterado.</span><span class="sxs-lookup"><span data-stu-id="7c517-104">TAPI sends the **PHONE\_STATE** message to an application whenever the status of a phone device changes.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="7c517-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c517-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c517-106">*hPhone*</span><span class="sxs-lookup"><span data-stu-id="7c517-106">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="7c517-107">Um identificador para o dispositivo de telefone.</span><span class="sxs-lookup"><span data-stu-id="7c517-107">A handle to the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="7c517-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="7c517-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="7c517-109">A instância de retorno de chamada do aplicativo fornecida ao abrir o dispositivo de telefone.</span><span class="sxs-lookup"><span data-stu-id="7c517-109">The application's callback instance provided when opening the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="7c517-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="7c517-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="7c517-111">O estado do telefone que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="7c517-111">The phone state that has changed.</span></span> <span data-ttu-id="7c517-112">Esse parâmetro usa uma das [**\_ constantes PHONESTATE**](phonestate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="7c517-112">This parameter uses one of the [**PHONESTATE\_ constants**](phonestate--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c517-113">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="7c517-113">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="7c517-114">Informações dependentes do estado do telefone detalhando a alteração do status.</span><span class="sxs-lookup"><span data-stu-id="7c517-114">Phone state-dependent information detailing the status change.</span></span> <span data-ttu-id="7c517-115">Esse parâmetro não será usado se vários sinalizadores forem definidos em *dwParam1*, pois vários itens de status foram alterados.</span><span class="sxs-lookup"><span data-stu-id="7c517-115">This parameter is not used if multiple flags are set in *dwParam1*, because multiple status items have changed.</span></span> <span data-ttu-id="7c517-116">O aplicativo deve invocar [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) para obter um conjunto completo de informações.</span><span class="sxs-lookup"><span data-stu-id="7c517-116">The application should invoke [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) to obtain a complete set of information.</span></span>

<span data-ttu-id="7c517-117">Se *dwParam1* for \_ proprietário de PHONESTATE, *dwParam2* conterá o novo número de proprietários.</span><span class="sxs-lookup"><span data-stu-id="7c517-117">If *dwParam1* is PHONESTATE\_OWNER, *dwParam2* contains the new number of owners.</span></span>

<span data-ttu-id="7c517-118">Se *dwParam1* for um PHONESTATE \_ monitores, *dwParam2* conterá o novo número de monitores.</span><span class="sxs-lookup"><span data-stu-id="7c517-118">If *dwParam1* is PHONESTATE\_MONITORS, *dwParam2* contains the new number of monitors.</span></span>

<span data-ttu-id="7c517-119">Se *dwParam1* for a lâmpada PHONESTATE \_ , *dwParam2* conterá o identificador de botão/lâmpada da lâmpada que foi alterada.</span><span class="sxs-lookup"><span data-stu-id="7c517-119">If *dwParam1* is PHONESTATE\_LAMP, *dwParam2* contains the button/lamp identifier of the lamp that has changed.</span></span>

<span data-ttu-id="7c517-120">Se *dwParam1* for PHONESTATE \_ Anéismode, *dwParam2* conterá o novo modo de anel.</span><span class="sxs-lookup"><span data-stu-id="7c517-120">If *dwParam1* is PHONESTATE\_RINGMODE, *dwParam2* contains the new ring mode.</span></span>

<span data-ttu-id="7c517-121">Se *dwParam1* for fone de telefone \_ , palestrante ou headset, *dwParam2* conterá o novo modo Hookswitch do Dispositivo Hookswitch.</span><span class="sxs-lookup"><span data-stu-id="7c517-121">If *dwParam1* is PHONESTATE\_HANDSET, SPEAKER or HEADSET, *dwParam2* contains the new hookswitch mode of that hookswitch device.</span></span> <span data-ttu-id="7c517-122">Esse parâmetro usa uma das [**\_ constantes PHONEHOOKSWITCHMODE**](phonehookswitchmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="7c517-122">This parameter uses one of the [**PHONEHOOKSWITCHMODE\_ constants**](phonehookswitchmode--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c517-123">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="7c517-123">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="7c517-124">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="7c517-124">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c517-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7c517-125">Return value</span></span>

<span data-ttu-id="7c517-126">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="7c517-126">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c517-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c517-127">Remarks</span></span>

<span data-ttu-id="7c517-128">O envio da mensagem de **\_ estado do telefone** para o aplicativo pode ser controlado e consultado usando [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) e [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages).</span><span class="sxs-lookup"><span data-stu-id="7c517-128">Sending the **PHONE\_STATE** message to the application can be controlled and queried using [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) and [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages).</span></span> <span data-ttu-id="7c517-129">Por padrão, essa mensagem é desabilitada para todas as alterações de estado, exceto para \_ REinicialização de PHONESTATE, que não pode ser desabilitada.</span><span class="sxs-lookup"><span data-stu-id="7c517-129">By default, this message is disabled for all state changes except for PHONESTATE\_REINIT, which cannot be disabled.</span></span> <span data-ttu-id="7c517-130">Essa mensagem é enviada para todos os aplicativos que têm um identificador para o telefone, incluindo aqueles que chamaram [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) com o parâmetro *DWPRIVILEGES* definido como PHONEPRIVILEGE \_ Owner ou PHONEPRIVILEGE \_ Monitor.</span><span class="sxs-lookup"><span data-stu-id="7c517-130">This message is sent to all applications that have a handle to the phone, including those that called [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) with the *dwPrivileges* parameter set to PHONEPRIVILEGE\_OWNER or PHONEPRIVILEGE\_MONITOR.</span></span>

<span data-ttu-id="7c517-131">Uma mensagem de **\_ estado do telefone** com uma indicação de proprietários e/ou monitores é enviada para aplicativos que já têm um identificador para o telefone.</span><span class="sxs-lookup"><span data-stu-id="7c517-131">A **PHONE\_STATE** message with an Owners and/or Monitors indication is sent to applications that already have a handle for the phone.</span></span> <span data-ttu-id="7c517-132">Isso pode ser o resultado de outro aplicativo alterar a propriedade ou a monitoração do dispositivo de telefone com [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen), [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) ou [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown).</span><span class="sxs-lookup"><span data-stu-id="7c517-132">This can be the result of another application changing ownership or monitorship of the phone device with [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen), [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) or [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown).</span></span>

## <a name="requirements"></a><span data-ttu-id="7c517-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c517-133">Requirements</span></span>



| <span data-ttu-id="7c517-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c517-134">Requirement</span></span> | <span data-ttu-id="7c517-135">Valor</span><span class="sxs-lookup"><span data-stu-id="7c517-135">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7c517-136">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="7c517-136">TAPI version</span></span><br/> | <span data-ttu-id="7c517-137">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="7c517-137">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="7c517-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7c517-138">Header</span></span><br/>       | <dl> <span data-ttu-id="7c517-139"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c517-139"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c517-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c517-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c517-141">**\_fechar telefone**</span><span class="sxs-lookup"><span data-stu-id="7c517-141">**PHONE\_CLOSE**</span></span>](phone-close.md)
</dt> <dt>

[<span data-ttu-id="7c517-142">**PHONECAPS**</span><span class="sxs-lookup"><span data-stu-id="7c517-142">**PHONECAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-phonecaps)
</dt> <dt>

[<span data-ttu-id="7c517-143">**phoneClose**</span><span class="sxs-lookup"><span data-stu-id="7c517-143">**phoneClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneclose)
</dt> <dt>

[<span data-ttu-id="7c517-144">**phoneGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="7c517-144">**phoneGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> <dt>

[<span data-ttu-id="7c517-145">**phoneGetStatus**</span><span class="sxs-lookup"><span data-stu-id="7c517-145">**phoneGetStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus)
</dt> <dt>

[<span data-ttu-id="7c517-146">**phoneGetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="7c517-146">**phoneGetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages)
</dt> <dt>

[<span data-ttu-id="7c517-147">**phoneInitialize**</span><span class="sxs-lookup"><span data-stu-id="7c517-147">**phoneInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[<span data-ttu-id="7c517-148">**phoneInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="7c517-148">**phoneInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> <dt>

[<span data-ttu-id="7c517-149">**phoneOpen**</span><span class="sxs-lookup"><span data-stu-id="7c517-149">**phoneOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneopen)
</dt> <dt>

[<span data-ttu-id="7c517-150">**phoneSetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="7c517-150">**phoneSetStatusMessages**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages)
</dt> <dt>

[<span data-ttu-id="7c517-151">**phoneShutdown**</span><span class="sxs-lookup"><span data-stu-id="7c517-151">**phoneShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)
</dt> </dl>

 

 




