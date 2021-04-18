---
description: A mensagem de LINE_MONITORMEDIA TAPI é enviada quando uma alteração no tipo de mídia de chamadas é detectada. O envio dessa mensagem é controlado com a função lineMonitorMedia
ms.assetid: 1cfba455-9a15-45f3-8d56-74b8348e080e
title: Mensagem de LINE_MONITORMEDIA (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7b6e3d0d2928ab3256b844a27727657978dbe0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789453"
---
# <a name="line_monitormedia-message"></a><span data-ttu-id="e892c-104">Mensagem de MONITORMEDIA de linha \_</span><span class="sxs-lookup"><span data-stu-id="e892c-104">LINE\_MONITORMEDIA message</span></span>

<span data-ttu-id="e892c-105">A mensagem **de \_ MONITORMEDIA de linha** TAPI é enviada quando uma alteração no tipo de mídia da chamada é detectada.</span><span class="sxs-lookup"><span data-stu-id="e892c-105">The TAPI **LINE\_MONITORMEDIA** message is sent when a change in the call's media type is detected.</span></span> <span data-ttu-id="e892c-106">O envio dessa mensagem é controlado com a função [**lineMonitorMedia**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia) .</span><span class="sxs-lookup"><span data-stu-id="e892c-106">The sending of this message is controlled with the [**lineMonitorMedia**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia) function.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="e892c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e892c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e892c-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="e892c-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="e892c-109">Um identificador para a chamada.</span><span class="sxs-lookup"><span data-stu-id="e892c-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="e892c-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="e892c-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="e892c-111">A instância de retorno de chamada fornecida ao abrir a linha.</span><span class="sxs-lookup"><span data-stu-id="e892c-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="e892c-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="e892c-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="e892c-113">O novo tipo de mídia (ou modo).</span><span class="sxs-lookup"><span data-stu-id="e892c-113">The new media type (or mode).</span></span> <span data-ttu-id="e892c-114">Esse parâmetro deve ser apenas uma das [**\_ constantes LINEMEDIAMODE**](linemediamode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="e892c-114">This parameter must be one and only one of the [**LINEMEDIAMODE\_ constants**](linemediamode--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="e892c-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="e892c-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="e892c-116">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="e892c-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="e892c-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="e892c-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="e892c-118">A "contagem de tiques" (número de milissegundos desde o início do Windows) em que a mídia especificada foi detectada.</span><span class="sxs-lookup"><span data-stu-id="e892c-118">The "tick count" (number of milliseconds since Windows started) at which the specified media was detected.</span></span> <span data-ttu-id="e892c-119">Para versões TAPI anteriores a 2,0, esse parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="e892c-119">For TAPI versions earlier than 2.0, this parameter is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e892c-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e892c-120">Return value</span></span>

<span data-ttu-id="e892c-121">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="e892c-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e892c-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="e892c-122">Remarks</span></span>

<span data-ttu-id="e892c-123">A mensagem de **linha \_ MONITORMEDIA** é enviada para o aplicativo que habilitou o monitoramento de mídia para o tipo de mídia detectado.</span><span class="sxs-lookup"><span data-stu-id="e892c-123">The **LINE\_MONITORMEDIA** message is sent to the application that has enabled media monitoring for the media type detected.</span></span>

<span data-ttu-id="e892c-124">Como esse carimbo de data/hora pode ter sido gerado em um computador diferente daquele em que o aplicativo está sendo executado, ele é útil somente para comparação com outras mensagens com carimbo de data/hora semelhantes geradas no mesmo dispositivo de linha ( [**linha \_ GATHERDIGITS**](line-gatherdigits.md), [**\_ GENERATE line**](line-generate.md), [**line \_ MONITORDIGITS**](line-monitordigits.md), [**line \_ MONITORTONE**](line-monitortone.md)), para determinar seu tempo relativo (separação entre os eventos).</span><span class="sxs-lookup"><span data-stu-id="e892c-124">Because this timestamp may have been generated on a computer other than the one on which the application is executing, it is useful only for comparison to other similarly timestamped messages generated on the same line device ( [**LINE\_GATHERDIGITS**](line-gatherdigits.md), [**LINE\_GENERATE**](line-generate.md), [**LINE\_MONITORDIGITS**](line-monitordigits.md), [**LINE\_MONITORTONE**](line-monitortone.md)), in order to determine their relative timing (separation between events).</span></span> <span data-ttu-id="e892c-125">A contagem em escala pode "encapsule" depois de aproximadamente 49,7 dias; os aplicativos devem levar isso em conta ao executar cálculos.</span><span class="sxs-lookup"><span data-stu-id="e892c-125">The tick count can "wrap around" after approximately 49.7 days; applications must take this into account when performing calculations.</span></span>

<span data-ttu-id="e892c-126">Se o provedor de serviços não gerar o carimbo de data/hora (por exemplo, se ele foi criado usando uma versão anterior da TAPI), a TAPI fornecerá um carimbo de data/hora no ponto mais próximo do provedor de serviços que gera o evento para que o carimbo de data/hora sintetizado seja o mais preciso possível.</span><span class="sxs-lookup"><span data-stu-id="e892c-126">If the service provider does not generate the timestamp (for example, if it was created using an earlier version of TAPI), then TAPI provides a timestamp at the point closest to the service provider generating the event so that the synthesized timestamp is as accurate as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="e892c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e892c-127">Requirements</span></span>



| <span data-ttu-id="e892c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e892c-128">Requirement</span></span> | <span data-ttu-id="e892c-129">Valor</span><span class="sxs-lookup"><span data-stu-id="e892c-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e892c-130">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="e892c-130">TAPI version</span></span><br/> | <span data-ttu-id="e892c-131">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="e892c-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="e892c-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e892c-132">Header</span></span><br/>       | <dl> <span data-ttu-id="e892c-133"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="e892c-133"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e892c-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="e892c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e892c-135">**GATHERDIGITS de linha \_**</span><span class="sxs-lookup"><span data-stu-id="e892c-135">**LINE\_GATHERDIGITS**</span></span>](line-gatherdigits.md)
</dt> <dt>

[<span data-ttu-id="e892c-136">**geração de linha \_**</span><span class="sxs-lookup"><span data-stu-id="e892c-136">**LINE\_GENERATE**</span></span>](line-generate.md)
</dt> <dt>

[<span data-ttu-id="e892c-137">**MONITORDIGITS de linha \_**</span><span class="sxs-lookup"><span data-stu-id="e892c-137">**LINE\_MONITORDIGITS**</span></span>](line-monitordigits.md)
</dt> <dt>

[<span data-ttu-id="e892c-138">**MONITORTONE de linha \_**</span><span class="sxs-lookup"><span data-stu-id="e892c-138">**LINE\_MONITORTONE**</span></span>](line-monitortone.md)
</dt> </dl>

 

 




