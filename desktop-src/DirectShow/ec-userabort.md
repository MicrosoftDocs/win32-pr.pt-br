---
description: O usuário terminou a reprodução.
ms.assetid: 974a9c3e-cfc9-4608-9f98-732aeaa0a752
title: EC_USERABORT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bab4f76e90d7e5f51655eda6dc72834053df87b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766993"
---
# <a name="ec_userabort"></a><span data-ttu-id="92597-103">autoanulação do EC \_</span><span class="sxs-lookup"><span data-stu-id="92597-103">EC\_USERABORT</span></span>

<span data-ttu-id="92597-104">O usuário terminou a reprodução.</span><span class="sxs-lookup"><span data-stu-id="92597-104">The user has terminated playback.</span></span>

## <a name="parameters"></a><span data-ttu-id="92597-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92597-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92597-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="92597-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="92597-107">Zero.</span><span class="sxs-lookup"><span data-stu-id="92597-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="92597-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="92597-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="92597-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="92597-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="92597-110">Ação Padrão</span><span class="sxs-lookup"><span data-stu-id="92597-110">Default Action</span></span>

<span data-ttu-id="92597-111">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="92597-111">None.</span></span> <span data-ttu-id="92597-112">O aplicativo deve decidir se deseja parar o grafo.</span><span class="sxs-lookup"><span data-stu-id="92597-112">The application must decide whether to stop the graph.</span></span>

## <a name="remarks"></a><span data-ttu-id="92597-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="92597-113">Remarks</span></span>

<span data-ttu-id="92597-114">Esse código de evento sinaliza que o usuário terminou a reprodução normal do grafo.</span><span class="sxs-lookup"><span data-stu-id="92597-114">This event code signals that the user has terminated normal graph playback.</span></span> <span data-ttu-id="92597-115">Por exemplo, os renderizadores de vídeo enviam esse evento se o usuário fechar a janela de vídeo.</span><span class="sxs-lookup"><span data-stu-id="92597-115">For example, video renderers send this event if the user closes the video window.</span></span>

<span data-ttu-id="92597-116">Depois de enviar esse evento, o filtro deve rejeitar todos os exemplos e não enviar nenhum evento [**\_ redesenhado do EC**](ec-repaint.md) , até que o filtro seja interrompido e redefinido.</span><span class="sxs-lookup"><span data-stu-id="92597-116">After sending this event, the filter should reject all samples and not send any [**EC\_REPAINT**](ec-repaint.md) events, until the filter stops and is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="92597-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92597-117">Requirements</span></span>



| <span data-ttu-id="92597-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="92597-118">Requirement</span></span> | <span data-ttu-id="92597-119">Valor</span><span class="sxs-lookup"><span data-stu-id="92597-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="92597-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="92597-120">Header</span></span><br/> | <dl> <span data-ttu-id="92597-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="92597-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92597-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="92597-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92597-123">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="92597-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="92597-124">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="92597-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




