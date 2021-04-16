---
description: A mensagem de MONITORDIGITS de linha TAPI \_ é enviada quando um dígito é detectado. O envio dessa mensagem é controlado com a função lineMonitorDigits.
ms.assetid: 1c1a729c-a6bb-4432-9617-4a892c76cb8d
title: Mensagem de LINE_MONITORDIGITS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c6e85ed515d20c18c6e41cdb185b036312c54ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758405"
---
# <a name="line_monitordigits-message"></a><span data-ttu-id="692cf-104">Mensagem de MONITORDIGITS de linha \_</span><span class="sxs-lookup"><span data-stu-id="692cf-104">LINE\_MONITORDIGITS message</span></span>

<span data-ttu-id="692cf-105">A mensagem **de \_ MONITORDIGITS de linha** TAPI é enviada quando um dígito é detectado.</span><span class="sxs-lookup"><span data-stu-id="692cf-105">The TAPI **LINE\_MONITORDIGITS** message is sent when a digit is detected.</span></span> <span data-ttu-id="692cf-106">O envio dessa mensagem é controlado com a função [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) .</span><span class="sxs-lookup"><span data-stu-id="692cf-106">The sending of this message is controlled with the [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) function.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="692cf-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="692cf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="692cf-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="692cf-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="692cf-109">Um identificador para a chamada.</span><span class="sxs-lookup"><span data-stu-id="692cf-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="692cf-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="692cf-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="692cf-111">A instância de retorno de chamada fornecida ao abrir a linha do telefonema.</span><span class="sxs-lookup"><span data-stu-id="692cf-111">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="692cf-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="692cf-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="692cf-113">O byte de ordem inferior contém o último dígito recebido em uma representação de texto.</span><span class="sxs-lookup"><span data-stu-id="692cf-113">The low-order byte contains the last digit received in a text representation.</span></span>

</dd> <dt>

<span data-ttu-id="692cf-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="692cf-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="692cf-115">O modo de dígito que foi detectado.</span><span class="sxs-lookup"><span data-stu-id="692cf-115">The digit mode that was detected.</span></span> <span data-ttu-id="692cf-116">Esse parâmetro deve ser apenas uma das [**\_ constantes LINEDIGITMODE**](linedigitmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="692cf-116">This parameter must be one and only one of the [**LINEDIGITMODE\_ constants**](linedigitmode--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="692cf-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="692cf-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="692cf-118">A "contagem de tiques" (número de milissegundos desde o início do Windows) em que o dígito especificado foi detectado.</span><span class="sxs-lookup"><span data-stu-id="692cf-118">The "tick count" (number of milliseconds since Windows started) at which the specified digit was detected.</span></span> <span data-ttu-id="692cf-119">Para versões TAPI anteriores a 2,0, esse parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="692cf-119">For TAPI versions earlier than 2.0, this parameter is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="692cf-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="692cf-120">Return value</span></span>

<span data-ttu-id="692cf-121">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="692cf-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="692cf-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="692cf-122">Remarks</span></span>

<span data-ttu-id="692cf-123">A mensagem de **linha \_ MONITORDIGITS** é enviada para o aplicativo que tem o monitoramento de dígito habilitado.</span><span class="sxs-lookup"><span data-stu-id="692cf-123">The **LINE\_MONITORDIGITS** message is sent to the application that has enabled digit monitoring.</span></span>

<span data-ttu-id="692cf-124">Como esse carimbo de data/hora pode ter sido gerado em um computador diferente daquele em que o aplicativo está sendo executado, ele é útil somente para comparação com outras mensagens com carimbo de data/hora semelhantes geradas no mesmo dispositivo de linha ( [**linha \_ GATHERDIGITS**](line-gatherdigits.md), [**\_ GENERATE line**](line-generate.md), [**line \_ MONITORMEDIA**](line-monitormedia.md), [**line \_ MONITORTONE**](line-monitortone.md)), para determinar seu tempo relativo (separação entre os eventos).</span><span class="sxs-lookup"><span data-stu-id="692cf-124">Because this timestamp may have been generated on a computer other than the one on which the application is executing, it is useful only for comparison to other similarly timestamped messages generated on the same line device ( [**LINE\_GATHERDIGITS**](line-gatherdigits.md), [**LINE\_GENERATE**](line-generate.md), [**LINE\_MONITORMEDIA**](line-monitormedia.md), [**LINE\_MONITORTONE**](line-monitortone.md)), in order to determine their relative timing (separation between events).</span></span> <span data-ttu-id="692cf-125">A contagem em escala pode "encapsule" depois de aproximadamente 49,7 dias; os aplicativos devem levar isso em conta ao executar cálculos.</span><span class="sxs-lookup"><span data-stu-id="692cf-125">The tick count can "wrap around" after approximately 49.7 days; applications must take this into account when performing calculations.</span></span>

<span data-ttu-id="692cf-126">Se o provedor de serviços não gerar o carimbo de data/hora (por exemplo, se ele foi criado usando uma versão anterior da TAPI), a TAPI fornecerá um carimbo de data/hora no ponto mais próximo do provedor de serviços que gera o evento para que o carimbo de data/hora sintetizado seja o mais preciso possível.</span><span class="sxs-lookup"><span data-stu-id="692cf-126">If the service provider does not generate the timestamp (for example, if it was created using an earlier version of TAPI), then TAPI provides a timestamp at the point closest to the service provider generating the event so that the synthesized timestamp is as accurate as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="692cf-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="692cf-127">Requirements</span></span>



| <span data-ttu-id="692cf-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="692cf-128">Requirement</span></span> | <span data-ttu-id="692cf-129">Valor</span><span class="sxs-lookup"><span data-stu-id="692cf-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="692cf-130">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="692cf-130">TAPI version</span></span><br/> | <span data-ttu-id="692cf-131">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="692cf-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="692cf-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="692cf-132">Header</span></span><br/>       | <dl> <span data-ttu-id="692cf-133"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="692cf-133"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="692cf-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="692cf-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="692cf-135">**GATHERDIGITS de linha \_**</span><span class="sxs-lookup"><span data-stu-id="692cf-135">**LINE\_GATHERDIGITS**</span></span>](line-gatherdigits.md)
</dt> <dt>

[<span data-ttu-id="692cf-136">**geração de linha \_**</span><span class="sxs-lookup"><span data-stu-id="692cf-136">**LINE\_GENERATE**</span></span>](line-generate.md)
</dt> <dt>

[<span data-ttu-id="692cf-137">**MONITORMEDIA de linha \_**</span><span class="sxs-lookup"><span data-stu-id="692cf-137">**LINE\_MONITORMEDIA**</span></span>](line-monitormedia.md)
</dt> <dt>

[<span data-ttu-id="692cf-138">**MONITORTONE de linha \_**</span><span class="sxs-lookup"><span data-stu-id="692cf-138">**LINE\_MONITORTONE**</span></span>](line-monitortone.md)
</dt> <dt>

[<span data-ttu-id="692cf-139">**lineMonitorDigits**</span><span class="sxs-lookup"><span data-stu-id="692cf-139">**lineMonitorDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits)
</dt> </dl>

 

 




