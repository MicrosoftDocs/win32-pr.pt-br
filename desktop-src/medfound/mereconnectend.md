---
description: Sinaliza que uma fonte de mídia concluiu uma tentativa de reconexão com o servidor.
ms.assetid: 228e069a-a26b-472e-915e-ff9aec5ee9c1
title: Evento MEReconnectEnd (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3477abd5d4413faa6b2d965f7ace2d19c48dd786
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502394"
---
# <a name="mereconnectend-event"></a><span data-ttu-id="0c733-103">Evento MEReconnectEnd</span><span class="sxs-lookup"><span data-stu-id="0c733-103">MEReconnectEnd event</span></span>

<span data-ttu-id="0c733-104">Sinaliza que uma fonte de mídia concluiu uma tentativa de reconexão com o servidor.</span><span class="sxs-lookup"><span data-stu-id="0c733-104">Signals that a media source has completed an attempt to reconnect to the server.</span></span>

<span data-ttu-id="0c733-105">Gerado por uma origem de mídia no final de uma tentativa de reconexão.</span><span class="sxs-lookup"><span data-stu-id="0c733-105">Raised by a media source at the end of a reconnection attempt.</span></span> <span data-ttu-id="0c733-106">A origem da rede gerará esse evento se ele se reconectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="0c733-106">The network source raises this event if it reconnects to the server.</span></span> <span data-ttu-id="0c733-107">A sessão de mídia encaminha esse evento para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0c733-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="0c733-108">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="0c733-108">Event values</span></span>

<span data-ttu-id="0c733-109">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="0c733-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="0c733-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0c733-110">VARTYPE</span></span>              | <span data-ttu-id="0c733-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="0c733-111">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="0c733-112">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="0c733-112">VT\_EMPTY</span></span><br/> | <span data-ttu-id="0c733-113">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="0c733-113">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="0c733-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c733-114">Requirements</span></span>



| <span data-ttu-id="0c733-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c733-115">Requirement</span></span> | <span data-ttu-id="0c733-116">Valor</span><span class="sxs-lookup"><span data-stu-id="0c733-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c733-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c733-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0c733-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0c733-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0c733-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c733-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0c733-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0c733-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0c733-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0c733-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c733-122"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0c733-122"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c733-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c733-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c733-124">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0c733-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




