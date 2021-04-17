---
description: A mensagem de GATHERDIGITS de linha TAPI \_ é enviada quando a solicitação de coleta de dígitos em buffer atual termina ou é cancelada. O buffer de dígitos pode ser examinado depois que essa mensagem tiver sido recebida pelo aplicativo.
ms.assetid: 0d27904d-9743-44bf-a7bc-132459351e01
title: Mensagem de LINE_GATHERDIGITS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f0c67c5a9bbd3f798a8f4343b36c311309633ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754736"
---
# <a name="line_gatherdigits-message"></a><span data-ttu-id="94afb-104">Mensagem de GATHERDIGITS de linha \_</span><span class="sxs-lookup"><span data-stu-id="94afb-104">LINE\_GATHERDIGITS message</span></span>

<span data-ttu-id="94afb-105">A mensagem **de \_ GATHERDIGITS de linha** TAPI é enviada quando a solicitação de coleta de dígitos em buffer atual termina ou é cancelada.</span><span class="sxs-lookup"><span data-stu-id="94afb-105">The TAPI **LINE\_GATHERDIGITS** message is sent when the current buffered digit-gathering request has terminated or is canceled.</span></span> <span data-ttu-id="94afb-106">O buffer de dígitos pode ser examinado depois que essa mensagem tiver sido recebida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="94afb-106">The digit buffer can be examined after this message has been received by the application.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="94afb-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="94afb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94afb-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="94afb-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="94afb-109">Um identificador para a chamada.</span><span class="sxs-lookup"><span data-stu-id="94afb-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="94afb-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="94afb-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="94afb-111">A instância de retorno de chamada fornecida ao abrir a linha.</span><span class="sxs-lookup"><span data-stu-id="94afb-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="94afb-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="94afb-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="94afb-113">O motivo pelo qual a coleta de dígitos foi encerrada.</span><span class="sxs-lookup"><span data-stu-id="94afb-113">The reason why digit gathering was terminated.</span></span> <span data-ttu-id="94afb-114">Esse parâmetro deve ser apenas uma das [**\_ constantes LINEGATHERTERM**](linegatherterm--constants.md).</span><span class="sxs-lookup"><span data-stu-id="94afb-114">This parameter must be one and only one of the [**LINEGATHERTERM\_ constants**](linegatherterm--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="94afb-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="94afb-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="94afb-116">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="94afb-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="94afb-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="94afb-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="94afb-118">A "contagem de tiques" (número de milissegundos desde o início do Windows) em que a coleta de dígitos foi concluída.</span><span class="sxs-lookup"><span data-stu-id="94afb-118">The "tick count" (number of milliseconds since Windows started) at which the digit gathering completed.</span></span> <span data-ttu-id="94afb-119">Para versões TAPI anteriores a 2,0, esse parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="94afb-119">For TAPI versions earlier than 2.0, this parameter is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94afb-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="94afb-120">Return value</span></span>

<span data-ttu-id="94afb-121">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="94afb-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="94afb-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="94afb-122">Remarks</span></span>

<span data-ttu-id="94afb-123">A mensagem de **linha \_ GATHERDIGITS** é enviada somente para o aplicativo que iniciou a coleta de dígitos na chamada usando [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits).</span><span class="sxs-lookup"><span data-stu-id="94afb-123">The **LINE\_GATHERDIGITS** message is only sent to the application that initiated the digit gathering on the call using [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits).</span></span>

<span data-ttu-id="94afb-124">Se a função [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits) for usada para cancelar uma solicitação anterior para coletar dígitos, a TAPI enviará uma mensagem **\_ GATHERDIGITS de linha** com *dwParam1* definido como LINEGATHERTERM \_ Cancelar para o aplicativo indicando que o buffer originalmente especificado contém os dígitos coletados até o cancelamento.</span><span class="sxs-lookup"><span data-stu-id="94afb-124">If the [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits) function is used to cancel a previous request to gather digits, TAPI sends a **LINE\_GATHERDIGITS** message with *dwParam1* set to LINEGATHERTERM\_CANCEL to the application indicating that the originally specified buffer contains the digits gathered up to the cancellation.</span></span>

<span data-ttu-id="94afb-125">Como o carimbo de data/hora especificado por *dwParam3* pode ter sido gerado em um computador diferente daquele em que o aplicativo está sendo executado, ele é útil somente para comparação com outras mensagens de carimbo de data/hora semelhantes geradas no mesmo dispositivo de linha ( [**\_ geração de linha**](line-generate.md), [**linha \_ MONITORDIGITS**](line-monitordigits.md), linha [**\_ MONITORMEDIA**](line-monitormedia.md), [**linha \_ MONITORTONE**](line-monitortone.md)), para determinar seu tempo relativo (separação entre eventos).</span><span class="sxs-lookup"><span data-stu-id="94afb-125">Because the timestamp specified by *dwParam3* may have been generated on a computer other than the one on which the application is executing, it is useful only for comparison to other similarly timestamped messages generated on the same line device ( [**LINE\_GENERATE**](line-generate.md), [**LINE\_MONITORDIGITS**](line-monitordigits.md), [**LINE\_MONITORMEDIA**](line-monitormedia.md), [**LINE\_MONITORTONE**](line-monitortone.md)), in order to determine their relative timing (separation between events).</span></span> <span data-ttu-id="94afb-126">A contagem em escala pode "encapsule" depois de aproximadamente 49,7 dias; os aplicativos devem levar isso em conta ao executar cálculos.</span><span class="sxs-lookup"><span data-stu-id="94afb-126">The tick count can "wrap around" after approximately 49.7 days; applications must take this into account when performing calculations.</span></span>

<span data-ttu-id="94afb-127">Se o provedor de serviços não gerar o carimbo de data/hora (por exemplo, se ele foi criado usando uma versão anterior da TAPI), a TAPI fornecerá um carimbo de data/hora no ponto mais próximo do provedor de serviços que gera o evento para que o carimbo de data/hora sintetizado seja o mais preciso possível.</span><span class="sxs-lookup"><span data-stu-id="94afb-127">If the service provider does not generate the timestamp (for example, if it was created using an earlier version of TAPI), then TAPI provides a timestamp at the point closest to the service provider generating the event so that the synthesized timestamp is as accurate as possible.</span></span>

> [!Note]  
> <span data-ttu-id="94afb-128">Quando um aplicativo invoca qualquer operação assíncrona que grava dados de volta na memória do aplicativo, o aplicativo deve manter essa memória disponível para gravação até que uma mensagem de [**\_ resposta**](line-reply.md) ou de **linha \_ GATHERDIGITS** seja recebida.</span><span class="sxs-lookup"><span data-stu-id="94afb-128">When an application invokes any asynchronous operation that writes data back into application memory, the application must keep that memory available for writing until a [**LINE\_REPLY**](line-reply.md) or **LINE\_GATHERDIGITS** message is received.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="94afb-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94afb-129">Requirements</span></span>



| <span data-ttu-id="94afb-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="94afb-130">Requirement</span></span> | <span data-ttu-id="94afb-131">Valor</span><span class="sxs-lookup"><span data-stu-id="94afb-131">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="94afb-132">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="94afb-132">TAPI version</span></span><br/> | <span data-ttu-id="94afb-133">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="94afb-133">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="94afb-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="94afb-134">Header</span></span><br/>       | <dl> <span data-ttu-id="94afb-135"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="94afb-135"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94afb-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="94afb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94afb-137">**geração de linha \_**</span><span class="sxs-lookup"><span data-stu-id="94afb-137">**LINE\_GENERATE**</span></span>](line-generate.md)
</dt> <dt>

[<span data-ttu-id="94afb-138">**MONITORDIGITS de linha \_**</span><span class="sxs-lookup"><span data-stu-id="94afb-138">**LINE\_MONITORDIGITS**</span></span>](line-monitordigits.md)
</dt> <dt>

[<span data-ttu-id="94afb-139">**MONITORMEDIA de linha \_**</span><span class="sxs-lookup"><span data-stu-id="94afb-139">**LINE\_MONITORMEDIA**</span></span>](line-monitormedia.md)
</dt> <dt>

[<span data-ttu-id="94afb-140">**MONITORTONE de linha \_**</span><span class="sxs-lookup"><span data-stu-id="94afb-140">**LINE\_MONITORTONE**</span></span>](line-monitortone.md)
</dt> <dt>

[<span data-ttu-id="94afb-141">**resposta de linha \_**</span><span class="sxs-lookup"><span data-stu-id="94afb-141">**LINE\_REPLY**</span></span>](line-reply.md)
</dt> <dt>

[<span data-ttu-id="94afb-142">**lineGatherDigits**</span><span class="sxs-lookup"><span data-stu-id="94afb-142">**lineGatherDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)
</dt> </dl>

 

 




