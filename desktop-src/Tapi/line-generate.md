---
description: A mensagem de geração de linha TAPI \_ é enviada para notificar o aplicativo que o dígito atual ou a geração de Tom foi encerrada.
ms.assetid: 375823c5-22c2-4010-bfb4-5b8b46141c72
title: Mensagem de LINE_GENERATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b916dc95d1a6343b0f8ebc0eef9e589b04aa2112
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757963"
---
# <a name="line_generate-message"></a><span data-ttu-id="b29e9-103">Mensagem de geração de linha \_</span><span class="sxs-lookup"><span data-stu-id="b29e9-103">LINE\_GENERATE message</span></span>

<span data-ttu-id="b29e9-104">A mensagem **de \_ geração de linha** TAPI é enviada para notificar o aplicativo que o dígito atual ou a geração de Tom foi encerrada.</span><span class="sxs-lookup"><span data-stu-id="b29e9-104">The TAPI **LINE\_GENERATE** message is sent to notify the application that the current digit or tone generation has terminated.</span></span> <span data-ttu-id="b29e9-105">Somente uma solicitação de geração desse tipo pode estar em andamento em uma chamada específica a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="b29e9-105">Only one such generation request can be in progress an a given call at any time.</span></span> <span data-ttu-id="b29e9-106">Essa mensagem também é enviada quando a geração de dígitos ou tons é cancelada.</span><span class="sxs-lookup"><span data-stu-id="b29e9-106">This message is also sent when digit or tone generation is canceled.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="b29e9-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b29e9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b29e9-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="b29e9-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="b29e9-109">Um identificador para a chamada.</span><span class="sxs-lookup"><span data-stu-id="b29e9-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="b29e9-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="b29e9-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="b29e9-111">A instância de retorno de chamada fornecida ao abrir a linha.</span><span class="sxs-lookup"><span data-stu-id="b29e9-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="b29e9-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="b29e9-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="b29e9-113">O motivo pelo qual a geração de dígitos ou tons foi encerrada.</span><span class="sxs-lookup"><span data-stu-id="b29e9-113">The reason why digit or tone generation was terminated.</span></span> <span data-ttu-id="b29e9-114">Esse parâmetro deve ser apenas uma das [**\_ constantes LINEGENERATETERM**](linegenerateterm--constants.md).</span><span class="sxs-lookup"><span data-stu-id="b29e9-114">This parameter must be one and only one of the [**LINEGENERATETERM\_ constants**](linegenerateterm--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="b29e9-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="b29e9-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="b29e9-116">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="b29e9-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="b29e9-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="b29e9-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="b29e9-118">A "contagem de tiques" (número de milissegundos desde o início do Windows) em que a geração de dígitos ou tons foi concluída.</span><span class="sxs-lookup"><span data-stu-id="b29e9-118">The "tick count" (number of milliseconds since Windows started) at which the digit or tone generation completed.</span></span> <span data-ttu-id="b29e9-119">Para versões de API anteriores a 2,0, esse parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="b29e9-119">For API versions earlier than 2.0, this parameter is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b29e9-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b29e9-120">Return value</span></span>

<span data-ttu-id="b29e9-121">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="b29e9-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b29e9-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="b29e9-122">Remarks</span></span>

<span data-ttu-id="b29e9-123">A mensagem de **\_ geração de linha** é enviada somente para o aplicativo que solicitou a geração de dígito ou de Tom.</span><span class="sxs-lookup"><span data-stu-id="b29e9-123">The **LINE\_GENERATE** message is only sent to the application that requested the digit or tone generation.</span></span>

<span data-ttu-id="b29e9-124">Como o carimbo de data/hora especificado por *dwParam3* pode ter sido gerado em um computador diferente daquele em que o aplicativo está sendo executado, ele é útil somente para comparação com outras mensagens de carimbo de data/hora semelhantes geradas no mesmo dispositivo de linha ( [**line \_ GATHERDIGITS**](line-gatherdigits.md), [**line \_ MONITORDIGITS**](line-monitordigits.md), line [**\_ MONITORMEDIA**](line-monitormedia.md), [**line \_ MONITORTONE**](line-monitortone.md)), a fim de determinar seu tempo relativo (separação entre eventos).</span><span class="sxs-lookup"><span data-stu-id="b29e9-124">Because the timestamp specified by *dwParam3* may have been generated on a computer other than the one on which the application is executing, it is useful only for comparison to other similarly timestamped messages generated on the same line device ( [**LINE\_GATHERDIGITS**](line-gatherdigits.md), [**LINE\_MONITORDIGITS**](line-monitordigits.md), [**LINE\_MONITORMEDIA**](line-monitormedia.md), [**LINE\_MONITORTONE**](line-monitortone.md)), in order to determine their relative timing (separation between events).</span></span> <span data-ttu-id="b29e9-125">A contagem em escala pode "encapsule" depois de aproximadamente 49,7 dias; os aplicativos devem levar isso em conta ao executar cálculos.</span><span class="sxs-lookup"><span data-stu-id="b29e9-125">The tick count can "wrap around" after approximately 49.7 days; applications must take this into account when performing calculations.</span></span>

<span data-ttu-id="b29e9-126">Se o provedor de serviços não gerar o carimbo de data/hora (por exemplo, se ele foi criado usando uma versão anterior da TAPI), a TAPI fornecerá um carimbo de data/hora no ponto mais próximo do provedor de serviços que gera o evento para que o carimbo de data/hora sintetizado seja o mais preciso possível.</span><span class="sxs-lookup"><span data-stu-id="b29e9-126">If the service provider does not generate the timestamp (for example, if it was created using an earlier version of TAPI), then TAPI provides a timestamp at the point closest to the service provider generating the event so that the synthesized timestamp is as accurate as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="b29e9-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b29e9-127">Requirements</span></span>



| <span data-ttu-id="b29e9-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b29e9-128">Requirement</span></span> | <span data-ttu-id="b29e9-129">Valor</span><span class="sxs-lookup"><span data-stu-id="b29e9-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b29e9-130">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="b29e9-130">TAPI version</span></span><br/> | <span data-ttu-id="b29e9-131">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="b29e9-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="b29e9-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b29e9-132">Header</span></span><br/>       | <dl> <span data-ttu-id="b29e9-133"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="b29e9-133"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b29e9-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="b29e9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b29e9-135">**GATHERDIGITS de linha \_**</span><span class="sxs-lookup"><span data-stu-id="b29e9-135">**LINE\_GATHERDIGITS**</span></span>](line-gatherdigits.md)
</dt> <dt>

[<span data-ttu-id="b29e9-136">**MONITORDIGITS de linha \_**</span><span class="sxs-lookup"><span data-stu-id="b29e9-136">**LINE\_MONITORDIGITS**</span></span>](line-monitordigits.md)
</dt> <dt>

[<span data-ttu-id="b29e9-137">**MONITORMEDIA de linha \_**</span><span class="sxs-lookup"><span data-stu-id="b29e9-137">**LINE\_MONITORMEDIA**</span></span>](line-monitormedia.md)
</dt> <dt>

[<span data-ttu-id="b29e9-138">**MONITORTONE de linha \_**</span><span class="sxs-lookup"><span data-stu-id="b29e9-138">**LINE\_MONITORTONE**</span></span>](line-monitortone.md)
</dt> </dl>

 

 




