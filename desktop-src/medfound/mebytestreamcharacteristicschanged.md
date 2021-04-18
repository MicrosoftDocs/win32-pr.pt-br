---
description: Enviado por um fluxo de bytes quando as características do fluxo de bytes forem alteradas.
ms.assetid: EC34A7A3-BF01-4F9E-BA79-131B76D4C58F
title: Evento MEByteStreamCharacteristicsChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e626f510927970aad3c51182fca3a6dfddb0009
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762216"
---
# <a name="mebytestreamcharacteristicschanged-event"></a><span data-ttu-id="20e80-103">Evento MEByteStreamCharacteristicsChanged</span><span class="sxs-lookup"><span data-stu-id="20e80-103">MEByteStreamCharacteristicsChanged event</span></span>

<span data-ttu-id="20e80-104">Enviado por um fluxo de bytes quando as características do fluxo de bytes forem alteradas.</span><span class="sxs-lookup"><span data-stu-id="20e80-104">Sent by a byte stream when the characteristics of the byte stream have changed.</span></span>

## <a name="event-values"></a><span data-ttu-id="20e80-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="20e80-105">Event values</span></span>

<span data-ttu-id="20e80-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="20e80-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="20e80-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="20e80-107">VARTYPE</span></span>               | <span data-ttu-id="20e80-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="20e80-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="20e80-109">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="20e80-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="20e80-110">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="20e80-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="20e80-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="20e80-111">Remarks</span></span>

<span data-ttu-id="20e80-112">Esse evento indica que uma ou mais das seguintes características foram alteradas:</span><span class="sxs-lookup"><span data-stu-id="20e80-112">This event indicates that one or more of the following characteristics has changed:</span></span>

-   <span data-ttu-id="20e80-113">Sinalizadores de capacidade ([**IMFByteStream:: GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities))</span><span class="sxs-lookup"><span data-stu-id="20e80-113">Capability flags ([**IMFByteStream::GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities))</span></span>
-   <span data-ttu-id="20e80-114">Sinalizador de fim de fluxo ([**IMFByteStream:: IsEndOfStream**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-isendofstream))</span><span class="sxs-lookup"><span data-stu-id="20e80-114">End-of-stream flag ([**IMFByteStream::IsEndOfStream**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-isendofstream))</span></span>
-   <span data-ttu-id="20e80-115">Comprimento ([**IMFByteStream:: GetLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getlength))</span><span class="sxs-lookup"><span data-stu-id="20e80-115">Length ([**IMFByteStream::GetLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getlength))</span></span>

<span data-ttu-id="20e80-116">Nem todas as implementações de [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) dão suporte a esse evento.</span><span class="sxs-lookup"><span data-stu-id="20e80-116">Not all [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) implementations support this event.</span></span> <span data-ttu-id="20e80-117">Para receber o evento, consulte o objeto byte-Stream para a interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="20e80-117">To receive the event, query the byte-stream object for the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="20e80-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20e80-118">Requirements</span></span>



| <span data-ttu-id="20e80-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="20e80-119">Requirement</span></span> | <span data-ttu-id="20e80-120">Valor</span><span class="sxs-lookup"><span data-stu-id="20e80-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20e80-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20e80-121">Minimum supported client</span></span><br/> | <span data-ttu-id="20e80-122">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="20e80-122">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="20e80-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20e80-123">Minimum supported server</span></span><br/> | <span data-ttu-id="20e80-124">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="20e80-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="20e80-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="20e80-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="20e80-126"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="20e80-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20e80-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="20e80-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20e80-128">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="20e80-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




