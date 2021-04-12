---
description: Ocorreu um erro não fatal durante o streaming.
ms.assetid: 04afcca5-34d9-4c99-86bc-b37c19232ec1
title: Evento MENonFatalError (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6af26a87b99e9c2ef649684c4ede53e707e7084
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296573"
---
# <a name="menonfatalerror-event"></a><span data-ttu-id="d5df7-103">Evento MENonFatalError</span><span class="sxs-lookup"><span data-stu-id="d5df7-103">MENonFatalError event</span></span>

<span data-ttu-id="d5df7-104">Ocorreu um erro não fatal durante o streaming.</span><span class="sxs-lookup"><span data-stu-id="d5df7-104">A non-fatal error occurred during streaming.</span></span> <span data-ttu-id="d5df7-105">Qualquer componente Media Foundation pode enviar esse evento a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="d5df7-105">Any Media Foundation component can send this event at any time.</span></span>

## <a name="event-values"></a><span data-ttu-id="d5df7-106">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="d5df7-106">Event values</span></span>

<span data-ttu-id="d5df7-107">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="d5df7-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="d5df7-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="d5df7-108">VARTYPE</span></span>            | <span data-ttu-id="d5df7-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="d5df7-109">Description</span></span>                                                        |
|--------------------|--------------------------------------------------------------------|
| <span data-ttu-id="d5df7-110">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="d5df7-110">VT\_UI4</span></span><br/> | <span data-ttu-id="d5df7-111">Valor **HRESULT** que descreve o erro.</span><span class="sxs-lookup"><span data-stu-id="d5df7-111">**HRESULT** value that describes the error.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="d5df7-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="d5df7-112">Attributes</span></span>

<span data-ttu-id="d5df7-113">Nenhum atributo definido para este evento.</span><span class="sxs-lookup"><span data-stu-id="d5df7-113">No attributes are defined for this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5df7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5df7-114">Remarks</span></span>

<span data-ttu-id="d5df7-115">Esse evento sinaliza um erro inesperado, mas recuperável durante o streaming.</span><span class="sxs-lookup"><span data-stu-id="d5df7-115">This event signals an unexpected but recoverable error during streaming.</span></span> <span data-ttu-id="d5df7-116">Por exemplo, uma fonte de mídia poderá enviar esse evento se ele descartar um pacote.</span><span class="sxs-lookup"><span data-stu-id="d5df7-116">For example, a media source might send this event if it drops a packet.</span></span>

<span data-ttu-id="d5df7-117">Não envie esse evento para sinalizar que um método assíncrono falhou.</span><span class="sxs-lookup"><span data-stu-id="d5df7-117">Do not send this event to signal that an asynchronous method failed.</span></span> <span data-ttu-id="d5df7-118">Se um método assíncrono falhar, o código de erro será retornado no evento normal para esse método.</span><span class="sxs-lookup"><span data-stu-id="d5df7-118">If an asynchronous method fails, the error code is returned in the normal event for that method.</span></span>

<span data-ttu-id="d5df7-119">Se ocorrer um erro de streaming não recuperável, envie o evento [MEError](meerror.md) .</span><span class="sxs-lookup"><span data-stu-id="d5df7-119">If a non-recoverable streaming error occurs, send the [MEError](meerror.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5df7-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5df7-120">Requirements</span></span>



| <span data-ttu-id="d5df7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5df7-121">Requirement</span></span> | <span data-ttu-id="d5df7-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d5df7-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5df7-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5df7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d5df7-124">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d5df7-124">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="d5df7-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5df7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d5df7-126">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="d5df7-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="d5df7-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d5df7-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5df7-128"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5df7-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5df7-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5df7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5df7-130">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d5df7-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




