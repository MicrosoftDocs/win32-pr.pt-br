---
description: Um comando de início de controle de fluxo entrou em vigor.
ms.assetid: e2f8d9a2-c96c-457c-8a88-7c86d4405928
title: EC_STREAM_CONTROL_STARTED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 984562fde9001de14067e5865d5583636b264852
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751466"
---
# <a name="ec_stream_control_started"></a><span data-ttu-id="47a96-103">controle de fluxo de EC \_ \_ \_ iniciado</span><span class="sxs-lookup"><span data-stu-id="47a96-103">EC\_STREAM\_CONTROL\_STARTED</span></span>

<span data-ttu-id="47a96-104">Um comando de início de controle de fluxo entrou em vigor.</span><span class="sxs-lookup"><span data-stu-id="47a96-104">A stream-control start command has taken effect.</span></span>

## <a name="parameters"></a><span data-ttu-id="47a96-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47a96-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47a96-106"><span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*</span><span class="sxs-lookup"><span data-stu-id="47a96-106"><span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*</span></span>
</dt> <dd>

<span data-ttu-id="47a96-107">(**IUnknown** \* ) Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do PIN que iniciou o fluxo.</span><span class="sxs-lookup"><span data-stu-id="47a96-107">(**IUnknown**\*) Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the pin that started the stream.</span></span>

</dd> <dt>

<span data-ttu-id="47a96-108"><span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*</span><span class="sxs-lookup"><span data-stu-id="47a96-108"><span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*</span></span>
</dt> <dd>

<span data-ttu-id="47a96-109">(**DWORD**) Valor definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="47a96-109">(**DWORD**) User-defined value.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="47a96-110">Ação Padrão</span><span class="sxs-lookup"><span data-stu-id="47a96-110">Default Action</span></span>

<span data-ttu-id="47a96-111">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="47a96-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="47a96-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="47a96-112">Remarks</span></span>

<span data-ttu-id="47a96-113">Os filtros enviam esse evento em resposta ao método [**IAMStreamControl:: StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) .</span><span class="sxs-lookup"><span data-stu-id="47a96-113">Filters send this event in response to the [**IAMStreamControl::StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) method.</span></span> <span data-ttu-id="47a96-114">Esse método especifica um tempo de referência para um PIN iniciar streaming.</span><span class="sxs-lookup"><span data-stu-id="47a96-114">This method specifies a reference time for a pin to begin streaming.</span></span> <span data-ttu-id="47a96-115">Quando o streaming começa, o filtro envia esse evento.</span><span class="sxs-lookup"><span data-stu-id="47a96-115">When streaming does begin, the filter sends this event.</span></span>

<span data-ttu-id="47a96-116">O parâmetro *pSender* especifica o PIN que executa o comando Start.</span><span class="sxs-lookup"><span data-stu-id="47a96-116">The *pSender* parameter specifies the pin that executes the start command.</span></span> <span data-ttu-id="47a96-117">Dependendo da implementação, pode não ser o PIN que recebeu a chamada [**StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) .</span><span class="sxs-lookup"><span data-stu-id="47a96-117">Depending on the implementation, it might not be the pin that received the [**StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) call.</span></span>

<span data-ttu-id="47a96-118">O parâmetro *dwCookie* é especificado pelo aplicativo no método [**StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) .</span><span class="sxs-lookup"><span data-stu-id="47a96-118">The *dwCookie* parameter is specified by the application in the [**StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) method.</span></span> <span data-ttu-id="47a96-119">Esse parâmetro permite que o aplicativo rastreie várias chamadas para o método.</span><span class="sxs-lookup"><span data-stu-id="47a96-119">This parameter enables the application to track multiple calls to the method.</span></span>

## <a name="requirements"></a><span data-ttu-id="47a96-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47a96-120">Requirements</span></span>



| <span data-ttu-id="47a96-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="47a96-121">Requirement</span></span> | <span data-ttu-id="47a96-122">Valor</span><span class="sxs-lookup"><span data-stu-id="47a96-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="47a96-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="47a96-123">Header</span></span><br/> | <dl> <span data-ttu-id="47a96-124"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="47a96-124"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47a96-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="47a96-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47a96-126">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="47a96-126">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="47a96-127">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="47a96-127">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




