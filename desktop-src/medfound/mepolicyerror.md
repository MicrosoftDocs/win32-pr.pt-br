---
description: Gerado por uma saída confiável se ocorrer um erro ao impor a política de saída.
ms.assetid: 0cc62915-1ed6-4d1d-9600-0dac0b9034e3
title: Evento MEPolicyError (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b75083974ee0e76d7d8e21f0a2c83c2feee8d59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768252"
---
# <a name="mepolicyerror-event"></a><span data-ttu-id="20eb4-103">Evento MEPolicyError</span><span class="sxs-lookup"><span data-stu-id="20eb4-103">MEPolicyError event</span></span>

<span data-ttu-id="20eb4-104">Gerado por uma saída confiável se ocorrer um erro ao impor a política de saída.</span><span class="sxs-lookup"><span data-stu-id="20eb4-104">Raised by a trusted output if an error occurs while enforcing the output policy.</span></span>

<span data-ttu-id="20eb4-105">Se a sessão de mídia receber esse evento, ele interromperá a reprodução e encaminhará o evento para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="20eb4-105">If the Media Session receives this event, it stops playback and forwards the event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="20eb4-106">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="20eb4-106">Event values</span></span>

<span data-ttu-id="20eb4-107">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="20eb4-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="20eb4-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="20eb4-108">VARTYPE</span></span>              | <span data-ttu-id="20eb4-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="20eb4-109">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="20eb4-110">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="20eb4-110">VT\_EMPTY</span></span><br/> | <span data-ttu-id="20eb4-111">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="20eb4-111">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="20eb4-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="20eb4-112">Remarks</span></span>

<span data-ttu-id="20eb4-113">Os valores possíveis recuperados de [**IMFMediaEvent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="20eb4-113">Possible values retrieved from [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) include the following.</span></span>



| <span data-ttu-id="20eb4-114">Valor</span><span class="sxs-lookup"><span data-stu-id="20eb4-114">Value</span></span>                      | <span data-ttu-id="20eb4-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="20eb4-115">Description</span></span>                                                    |
|----------------------------|----------------------------------------------------------------|
| <span data-ttu-id="20eb4-116">\_política MF \_ E \_ sem suporte</span><span class="sxs-lookup"><span data-stu-id="20eb4-116">MF\_E\_POLICY\_UNSUPPORTED</span></span> | <span data-ttu-id="20eb4-117">A saída confiável não oferece suporte à política de saída atual.</span><span class="sxs-lookup"><span data-stu-id="20eb4-117">The trusted output does not support the current output policy.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="20eb4-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20eb4-118">Requirements</span></span>



| <span data-ttu-id="20eb4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="20eb4-119">Requirement</span></span> | <span data-ttu-id="20eb4-120">Valor</span><span class="sxs-lookup"><span data-stu-id="20eb4-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20eb4-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20eb4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="20eb4-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="20eb4-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="20eb4-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20eb4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="20eb4-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="20eb4-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="20eb4-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="20eb4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="20eb4-126"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="20eb4-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20eb4-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="20eb4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20eb4-128">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="20eb4-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




