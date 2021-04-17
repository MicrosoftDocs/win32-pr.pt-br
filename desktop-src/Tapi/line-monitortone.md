---
description: A mensagem de MONITORTONE de linha TAPI \_ é enviada quando um tom é detectado. O envio dessa mensagem é controlado com a função lineMonitorTones.
ms.assetid: ffdca615-5341-4f02-bb38-b8133cd9477d
title: Mensagem de LINE_MONITORTONE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de88863111dc0d00ea32953eeac76d4b570b5848
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769409"
---
# <a name="line_monitortone-message"></a><span data-ttu-id="3882e-104">Mensagem de MONITORTONE de linha \_</span><span class="sxs-lookup"><span data-stu-id="3882e-104">LINE\_MONITORTONE message</span></span>

<span data-ttu-id="3882e-105">A mensagem **de \_ MONITORTONE de linha** TAPI é enviada quando um tom é detectado.</span><span class="sxs-lookup"><span data-stu-id="3882e-105">The TAPI **LINE\_MONITORTONE** message is sent when a tone is detected.</span></span> <span data-ttu-id="3882e-106">O envio dessa mensagem é controlado com a função [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) .</span><span class="sxs-lookup"><span data-stu-id="3882e-106">The sending of this message is controlled with the [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) function.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="3882e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3882e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3882e-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="3882e-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="3882e-109">Um identificador para a chamada.</span><span class="sxs-lookup"><span data-stu-id="3882e-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="3882e-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="3882e-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="3882e-111">A instância de retorno de chamada fornecida ao abrir a linha do telefonema.</span><span class="sxs-lookup"><span data-stu-id="3882e-111">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="3882e-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="3882e-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="3882e-113">O membro **dwAppSpecific** específico do aplicativo da estrutura [**LINEMONITORTONE**](/windows/desktop/api/Tapi/ns-tapi-linemonitortone) para o Tom que foi detectado.</span><span class="sxs-lookup"><span data-stu-id="3882e-113">The application-specific **dwAppSpecific** member of the [**LINEMONITORTONE**](/windows/desktop/api/Tapi/ns-tapi-linemonitortone) structure for the tone that was detected.</span></span>

</dd> <dt>

<span data-ttu-id="3882e-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="3882e-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="3882e-115">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="3882e-115">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="3882e-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="3882e-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="3882e-117">A "contagem de tiques" (número de milissegundos desde o início do Windows) em que o Tom foi detectado.</span><span class="sxs-lookup"><span data-stu-id="3882e-117">The "tick count" (number of milliseconds since Windows started) at which the tone was detected.</span></span> <span data-ttu-id="3882e-118">Para versões de API anteriores a 2,0, esse parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="3882e-118">For API versions earlier than 2.0, this parameter is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3882e-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3882e-119">Return value</span></span>

<span data-ttu-id="3882e-120">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="3882e-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3882e-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="3882e-121">Remarks</span></span>

<span data-ttu-id="3882e-122">A mensagem de **linha \_ MONITORTONE** é enviada somente para o aplicativo que solicitou o monitoramento do Tom.</span><span class="sxs-lookup"><span data-stu-id="3882e-122">The **LINE\_MONITORTONE** message is only sent to the application that has requested the tone be monitored.</span></span>

<span data-ttu-id="3882e-123">Como esse carimbo de data/hora pode ter sido gerado em um computador diferente daquele em que o aplicativo está sendo executado, ele é útil somente para comparação com outras mensagens com carimbo de data/hora semelhantes geradas no mesmo dispositivo de linha ( [**linha \_ GATHERDIGITS**](line-gatherdigits.md), [**\_ GENERATE line**](line-generate.md), [**line \_ MONITORDIGITS**](line-monitordigits.md), **line \_ MONITORTONE**), para determinar seu tempo relativo (separação entre os eventos).</span><span class="sxs-lookup"><span data-stu-id="3882e-123">Because this timestamp may have been generated on a computer other than the one on which the application is executing, it is useful only for comparison to other similarly timestamped messages generated on the same line device ( [**LINE\_GATHERDIGITS**](line-gatherdigits.md), [**LINE\_GENERATE**](line-generate.md), [**LINE\_MONITORDIGITS**](line-monitordigits.md), **LINE\_MONITORTONE**), in order to determine their relative timing (separation between events).</span></span> <span data-ttu-id="3882e-124">A contagem em escala pode "encapsule" depois de aproximadamente 49,7 dias; os aplicativos devem levar isso em conta ao executar cálculos.</span><span class="sxs-lookup"><span data-stu-id="3882e-124">The tick count can "wrap around" after approximately 49.7 days; applications must take this into account when performing calculations.</span></span>

<span data-ttu-id="3882e-125">Se o provedor de serviços não gerar o carimbo de data/hora (por exemplo, se ele foi criado usando uma versão anterior da TAPI), a TAPI fornecerá um carimbo de data/hora no ponto mais próximo do provedor de serviços que gera o evento para que o carimbo de data/hora sintetizado seja o mais preciso possível.</span><span class="sxs-lookup"><span data-stu-id="3882e-125">If the service provider does not generate the timestamp (for example, if it was created using an earlier version of TAPI), then TAPI provides a timestamp at the point closest to the service provider generating the event so that the synthesized timestamp is as accurate as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="3882e-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3882e-126">Requirements</span></span>



| <span data-ttu-id="3882e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3882e-127">Requirement</span></span> | <span data-ttu-id="3882e-128">Valor</span><span class="sxs-lookup"><span data-stu-id="3882e-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="3882e-129">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="3882e-129">TAPI version</span></span><br/> | <span data-ttu-id="3882e-130">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="3882e-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="3882e-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3882e-131">Header</span></span><br/>       | <dl> <span data-ttu-id="3882e-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="3882e-132"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3882e-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="3882e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3882e-134">**GATHERDIGITS de linha \_**</span><span class="sxs-lookup"><span data-stu-id="3882e-134">**LINE\_GATHERDIGITS**</span></span>](line-gatherdigits.md)
</dt> <dt>

[<span data-ttu-id="3882e-135">**geração de linha \_**</span><span class="sxs-lookup"><span data-stu-id="3882e-135">**LINE\_GENERATE**</span></span>](line-generate.md)
</dt> <dt>

[<span data-ttu-id="3882e-136">**MONITORDIGITS de linha \_**</span><span class="sxs-lookup"><span data-stu-id="3882e-136">**LINE\_MONITORDIGITS**</span></span>](line-monitordigits.md)
</dt> <dt>

[<span data-ttu-id="3882e-137">**LINEMONITORTONE**</span><span class="sxs-lookup"><span data-stu-id="3882e-137">**LINEMONITORTONE**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linemonitortone)
</dt> <dt>

[<span data-ttu-id="3882e-138">**lineMonitorTones**</span><span class="sxs-lookup"><span data-stu-id="3882e-138">**lineMonitorTones**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemonitortones)
</dt> </dl>

 

 




