---
description: Um comando de parada de controle de fluxo teve efeito.
ms.assetid: a2f7a959-fafd-47ff-9b3d-1a898fdb1f81
title: EC_STREAM_CONTROL_STOPPED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8c5488ba400d90623955c3e9adcba0dde07e04a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760094"
---
# <a name="ec_stream_control_stopped"></a><span data-ttu-id="3bc40-103">controle de fluxo do EC \_ \_ \_ interrompido</span><span class="sxs-lookup"><span data-stu-id="3bc40-103">EC\_STREAM\_CONTROL\_STOPPED</span></span>

<span data-ttu-id="3bc40-104">Um comando de parada de controle de fluxo teve efeito.</span><span class="sxs-lookup"><span data-stu-id="3bc40-104">A stream-control stop command has taken effect.</span></span>

## <a name="parameters"></a><span data-ttu-id="3bc40-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3bc40-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bc40-106"><span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*</span><span class="sxs-lookup"><span data-stu-id="3bc40-106"><span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*</span></span>
</dt> <dd>

<span data-ttu-id="3bc40-107">(**IUnknown** \* ) Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do PIN que interrompeu o fluxo.</span><span class="sxs-lookup"><span data-stu-id="3bc40-107">(**IUnknown**\*) Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the pin that stopped the stream.</span></span>

</dd> <dt>

<span data-ttu-id="3bc40-108"><span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*</span><span class="sxs-lookup"><span data-stu-id="3bc40-108"><span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*</span></span>
</dt> <dd>

<span data-ttu-id="3bc40-109">(**DWORD**) Valor definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="3bc40-109">(**DWORD**) User-defined value.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="3bc40-110">Ação Padrão</span><span class="sxs-lookup"><span data-stu-id="3bc40-110">Default Action</span></span>

<span data-ttu-id="3bc40-111">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="3bc40-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bc40-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="3bc40-112">Remarks</span></span>

<span data-ttu-id="3bc40-113">Os filtros enviam esse evento em resposta ao método [**IAMStreamControl:: StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) .</span><span class="sxs-lookup"><span data-stu-id="3bc40-113">Filters send this event in response to the [**IAMStreamControl::StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) method.</span></span> <span data-ttu-id="3bc40-114">O método **STOPAT** especifica um tempo de referência para um PIN parar de transmitir.</span><span class="sxs-lookup"><span data-stu-id="3bc40-114">The **StopAt** method specifies a reference time for a pin to stop streaming.</span></span> <span data-ttu-id="3bc40-115">Quando o streaming é interrompido, o filtro envia esse evento.</span><span class="sxs-lookup"><span data-stu-id="3bc40-115">When streaming does halt, the filter sends this event.</span></span>

<span data-ttu-id="3bc40-116">O parâmetro *pSender* especifica o PIN que executa o comando Stop.</span><span class="sxs-lookup"><span data-stu-id="3bc40-116">The *pSender* parameter specifies the pin that executes the stop command.</span></span> <span data-ttu-id="3bc40-117">Dependendo da implementação, pode não ser o PIN que recebeu a chamada [**STOPAT**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) .</span><span class="sxs-lookup"><span data-stu-id="3bc40-117">Depending on the implementation, it might not be the pin that received the [**StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) call.</span></span>

<span data-ttu-id="3bc40-118">O parâmetro *dwCookie* é especificado pelo aplicativo no método [**STOPAT**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) .</span><span class="sxs-lookup"><span data-stu-id="3bc40-118">The *dwCookie* parameter is specified by the application in the [**StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) method.</span></span> <span data-ttu-id="3bc40-119">Esse parâmetro permite que o aplicativo rastreie várias chamadas para o método.</span><span class="sxs-lookup"><span data-stu-id="3bc40-119">This parameter enables the application to track multiple calls to the method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bc40-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3bc40-120">Requirements</span></span>



| <span data-ttu-id="3bc40-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bc40-121">Requirement</span></span> | <span data-ttu-id="3bc40-122">Valor</span><span class="sxs-lookup"><span data-stu-id="3bc40-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3bc40-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3bc40-123">Header</span></span><br/> | <dl> <span data-ttu-id="3bc40-124"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bc40-124"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bc40-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="3bc40-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bc40-126">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="3bc40-126">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="3bc40-127">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="3bc40-127">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




