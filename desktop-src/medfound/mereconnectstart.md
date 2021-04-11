---
description: Sinaliza que uma fonte de mídia está tentando se reconectar ao servidor.
ms.assetid: c5975279-c710-4046-9152-d1e1c62eb785
title: Evento MEReconnectStart (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d21944e937f52205416b5e6e2b52d18c3a3c768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091167"
---
# <a name="mereconnectstart-event"></a><span data-ttu-id="f5a8b-103">Evento MEReconnectStart</span><span class="sxs-lookup"><span data-stu-id="f5a8b-103">MEReconnectStart event</span></span>

<span data-ttu-id="f5a8b-104">Sinaliza que uma fonte de mídia está tentando se reconectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="f5a8b-104">Signals that a media source is attempting to reconnect to the server.</span></span>

<span data-ttu-id="f5a8b-105">Gerado por uma fonte de mídia no início de uma tentativa de reconexão.</span><span class="sxs-lookup"><span data-stu-id="f5a8b-105">Raised by a media source at the start of a reconnection attempt.</span></span> <span data-ttu-id="f5a8b-106">A origem da rede gerará esse evento se tentar se reconectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="f5a8b-106">The network source raises this event if it attempts to reconnect to the server.</span></span> <span data-ttu-id="f5a8b-107">A sessão de mídia encaminha esse evento para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f5a8b-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="f5a8b-108">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="f5a8b-108">Event values</span></span>

<span data-ttu-id="f5a8b-109">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="f5a8b-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="f5a8b-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="f5a8b-110">VARTYPE</span></span>              | <span data-ttu-id="f5a8b-111">Description</span><span class="sxs-lookup"><span data-stu-id="f5a8b-111">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="f5a8b-112">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="f5a8b-112">VT\_EMPTY</span></span><br/> | <span data-ttu-id="f5a8b-113">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="f5a8b-113">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="f5a8b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5a8b-114">Requirements</span></span>



| <span data-ttu-id="f5a8b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5a8b-115">Requirement</span></span> | <span data-ttu-id="f5a8b-116">Valor</span><span class="sxs-lookup"><span data-stu-id="f5a8b-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5a8b-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5a8b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f5a8b-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f5a8b-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f5a8b-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5a8b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f5a8b-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f5a8b-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f5a8b-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f5a8b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5a8b-122"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f5a8b-122"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5a8b-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5a8b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5a8b-124">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f5a8b-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




