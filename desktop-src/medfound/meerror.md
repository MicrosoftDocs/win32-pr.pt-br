---
description: 'Sinaliza um erro sério. Qualquer componente Media Foundation pode enviar esse evento a qualquer momento. Chame IMFMediaEvent:: GetStatus para obter o código de erro da operação que falhou.'
ms.assetid: bff80041-77d8-43b1-a410-9cefaf45eb2c
title: Evento MEError (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0eb557dffb2c73a63031a193c331edabe470db7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763795"
---
# <a name="meerror-event"></a><span data-ttu-id="ffba4-105">Evento MEError</span><span class="sxs-lookup"><span data-stu-id="ffba4-105">MEError event</span></span>

<span data-ttu-id="ffba4-106">Sinaliza um erro sério.</span><span class="sxs-lookup"><span data-stu-id="ffba4-106">Signals a serious error.</span></span> <span data-ttu-id="ffba4-107">Qualquer componente Media Foundation pode enviar esse evento a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="ffba4-107">Any Media Foundation component can send this event at any time.</span></span> <span data-ttu-id="ffba4-108">Chame [**IMFMediaEvent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) para obter o código de erro da operação que falhou.</span><span class="sxs-lookup"><span data-stu-id="ffba4-108">Call [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) to get the error code of the operation that failed.</span></span>

## <a name="event-values"></a><span data-ttu-id="ffba4-109">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="ffba4-109">Event values</span></span>

<span data-ttu-id="ffba4-110">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="ffba4-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="ffba4-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ffba4-111">VARTYPE</span></span>              | <span data-ttu-id="ffba4-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="ffba4-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="ffba4-113">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="ffba4-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="ffba4-114">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="ffba4-114">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="ffba4-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ffba4-115">Remarks</span></span>

<span data-ttu-id="ffba4-116">Esse evento deve ser usado somente para erros inesperados.</span><span class="sxs-lookup"><span data-stu-id="ffba4-116">This event should be used only for unexpected errors.</span></span> <span data-ttu-id="ffba4-117">Não envie esse evento para sinalizar que um método assíncrono falhou.</span><span class="sxs-lookup"><span data-stu-id="ffba4-117">Do not send this event to signal that an asynchronous method failed.</span></span> <span data-ttu-id="ffba4-118">Se um método assíncrono falhar, o código de erro será retornado no evento normal para esse método.</span><span class="sxs-lookup"><span data-stu-id="ffba4-118">If an asynchronous method fails, the error code is returned in the normal event for that method.</span></span>

<span data-ttu-id="ffba4-119">Se ocorrer um erro recuperável durante o streaming, envie o evento [MENonFatalError](menonfatalerror.md) .</span><span class="sxs-lookup"><span data-stu-id="ffba4-119">If a recoverable error occurs during streaming, send the [MENonFatalError](menonfatalerror.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffba4-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ffba4-120">Requirements</span></span>



| <span data-ttu-id="ffba4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffba4-121">Requirement</span></span> | <span data-ttu-id="ffba4-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ffba4-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffba4-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ffba4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ffba4-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ffba4-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ffba4-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ffba4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ffba4-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ffba4-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ffba4-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ffba4-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffba4-128"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ffba4-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffba4-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="ffba4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffba4-130">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ffba4-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




