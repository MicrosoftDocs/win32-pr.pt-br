---
description: Identifica qual fluxo gerou um evento de captura.
ms.assetid: A15B334A-716A-467E-AEA5-C13710FFE109
title: Atributo MF_CAPTURE_ENGINE_EVENT_STREAM_INDEX (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8172a79bae2a2eeb529beb0c0ce57273830c1787
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827628"
---
# <a name="mf_capture_engine_event_stream_index-attribute"></a><span data-ttu-id="5c5fa-103">\_Atributo de \_ \_ índice de fluxo de eventos do mecanismo de \_ captura MF \_</span><span class="sxs-lookup"><span data-stu-id="5c5fa-103">MF\_CAPTURE\_ENGINE\_EVENT\_STREAM\_INDEX attribute</span></span>

<span data-ttu-id="5c5fa-104">Identifica qual fluxo gerou um evento de captura.</span><span class="sxs-lookup"><span data-stu-id="5c5fa-104">Identifies which stream generated a capture event.</span></span>

## <a name="data-type"></a><span data-ttu-id="5c5fa-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="5c5fa-105">Data type</span></span>

<span data-ttu-id="5c5fa-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5c5fa-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="5c5fa-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="5c5fa-107">Get/set</span></span>

<span data-ttu-id="5c5fa-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="5c5fa-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="5c5fa-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="5c5fa-109">Remarks</span></span>

<span data-ttu-id="5c5fa-110">Esse atributo aparece em alguns eventos do mecanismo de captura.</span><span class="sxs-lookup"><span data-stu-id="5c5fa-110">This attribute appears on some events from the capture engine.</span></span> <span data-ttu-id="5c5fa-111">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) no objeto de evento.</span><span class="sxs-lookup"><span data-stu-id="5c5fa-111">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) on the event object.</span></span> <span data-ttu-id="5c5fa-112">O objeto de evento é passado para o aplicativo por meio do método [**IMFCaptureEngineOnEventCallback:: OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) .</span><span class="sxs-lookup"><span data-stu-id="5c5fa-112">The event object is passed to the application through the [**IMFCaptureEngineOnEventCallback::OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c5fa-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c5fa-113">Requirements</span></span>



| <span data-ttu-id="5c5fa-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c5fa-114">Requirement</span></span> | <span data-ttu-id="5c5fa-115">Valor</span><span class="sxs-lookup"><span data-stu-id="5c5fa-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c5fa-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c5fa-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5c5fa-117">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5c5fa-117">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="5c5fa-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c5fa-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5c5fa-119">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5c5fa-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5c5fa-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5c5fa-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c5fa-121"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c5fa-121"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c5fa-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c5fa-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c5fa-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5c5fa-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5c5fa-124">**IMFCaptureEngineOnEventCallback:: OnEvent**</span><span class="sxs-lookup"><span data-stu-id="5c5fa-124">**IMFCaptureEngineOnEventCallback::OnEvent**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent)
</dt> </dl>

 

 




