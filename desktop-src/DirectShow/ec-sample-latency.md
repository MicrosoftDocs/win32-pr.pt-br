---
description: Especifica o quanto o agendamento de um componente é muito atrasado para o processamento de exemplos.
ms.assetid: 8bd202fb-3015-41a2-ad14-862f64cb252f
title: EC_SAMPLE_LATENCY (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee90d42e6464eccc4bc93b1052e29392b74bb2d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779854"
---
# <a name="ec_sample_latency"></a><span data-ttu-id="7d070-103">\_latência de exemplo de EC \_</span><span class="sxs-lookup"><span data-stu-id="7d070-103">EC\_SAMPLE\_LATENCY</span></span>

<span data-ttu-id="7d070-104">Especifica o quanto o agendamento de um componente é muito atrasado para o processamento de exemplos.</span><span class="sxs-lookup"><span data-stu-id="7d070-104">Specifies how far behind schedule a component is for processing samples.</span></span>

## <a name="parameters"></a><span data-ttu-id="7d070-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7d070-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d070-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="7d070-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="7d070-107">(o **\_ tempo de referência const** \* ) o quanto o componente está muito atrás, em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="7d070-107">(**const REFERENCE\_TIME**\*) How far behind the component is, in 100-nanosecond units.</span></span> <span data-ttu-id="7d070-108">Se esse valor for positivo, o componente estará atrás do agendamento.</span><span class="sxs-lookup"><span data-stu-id="7d070-108">If this value is positive, the component is behind schedule.</span></span> <span data-ttu-id="7d070-109">Se esse valor for negativo, o componente está à frente da agenda.</span><span class="sxs-lookup"><span data-stu-id="7d070-109">If this value is negative, the component is ahead of schedule.</span></span>

</dd> <dt>

<span data-ttu-id="7d070-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="7d070-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="7d070-111">Zero.</span><span class="sxs-lookup"><span data-stu-id="7d070-111">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="7d070-112">Ação Padrão</span><span class="sxs-lookup"><span data-stu-id="7d070-112">Default Action</span></span>

<span data-ttu-id="7d070-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="7d070-113">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d070-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d070-114">Remarks</span></span>

<span data-ttu-id="7d070-115">Um apresentador personalizado para o filtro EVR ( [**processador de vídeo avançado**](enhanced-video-renderer-filter.md) ) pode enviar essa mensagem para o EVR para notificar o EVR se o apresentador está atrasado ou adiantado.</span><span class="sxs-lookup"><span data-stu-id="7d070-115">A custom presenter for the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) filter can send this message to the EVR, to notify the EVR whether the presenter is behind schedule or ahead of schedule.</span></span>

<span data-ttu-id="7d070-116">A maneira mais simples de calcular *lParam1* é: *QPC agora*   *QPC Target*, em que *QPC agora* é o tempo de relógio agora, e *QPC Target* é o tempo de apresentação.</span><span class="sxs-lookup"><span data-stu-id="7d070-116">The simplest way to calculate *lParam1* is: *QPC now*   *QPC target*, where *QPC now* is the clock time now, and *QPC target* is the presentation time.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d070-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d070-117">Requirements</span></span>



| <span data-ttu-id="7d070-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d070-118">Requirement</span></span> | <span data-ttu-id="7d070-119">Valor</span><span class="sxs-lookup"><span data-stu-id="7d070-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7d070-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7d070-120">Header</span></span><br/> | <dl> <span data-ttu-id="7d070-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d070-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d070-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d070-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d070-123">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="7d070-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="7d070-124">Como escrever um apresentador EVR</span><span class="sxs-lookup"><span data-stu-id="7d070-124">How to Write an EVR Presenter</span></span>](/windows/desktop/medfound/how-to-write-an-evr-presenter)
</dt> </dl>

 

