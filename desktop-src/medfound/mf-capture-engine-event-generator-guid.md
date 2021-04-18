---
description: Identifica o componente que gerou um evento de captura.
ms.assetid: DCCF3054-AF14-44C7-84C0-B03E35B5D90A
title: Atributo MF_CAPTURE_ENGINE_EVENT_GENERATOR_GUID (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb9a5068db357523a626404910fb7d752ea0b621
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760602"
---
# <a name="mf_capture_engine_event_generator_guid-attribute"></a><span data-ttu-id="d35e1-103">\_Atributo de \_ \_ GUID do gerador de eventos do mecanismo de \_ captura MF \_</span><span class="sxs-lookup"><span data-stu-id="d35e1-103">MF\_CAPTURE\_ENGINE\_EVENT\_GENERATOR\_GUID attribute</span></span>

<span data-ttu-id="d35e1-104">Identifica o componente que gerou um evento de captura.</span><span class="sxs-lookup"><span data-stu-id="d35e1-104">Identifies the component that generated a capture event.</span></span>

## <a name="data-type"></a><span data-ttu-id="d35e1-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d35e1-105">Data type</span></span>

<span data-ttu-id="d35e1-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="d35e1-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="d35e1-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="d35e1-107">Remarks</span></span>

<span data-ttu-id="d35e1-108">Esse atributo aparece em alguns eventos do mecanismo de captura.</span><span class="sxs-lookup"><span data-stu-id="d35e1-108">This attribute appears on some events from the capture engine.</span></span> <span data-ttu-id="d35e1-109">Para obter esse atributo, chame [**IMFAttributes:: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) no objeto de evento.</span><span class="sxs-lookup"><span data-stu-id="d35e1-109">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) on the event object.</span></span> <span data-ttu-id="d35e1-110">O objeto de evento é passado para o aplicativo por meio do método [**IMFCaptureEngineOnEventCallback:: OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) .</span><span class="sxs-lookup"><span data-stu-id="d35e1-110">The event object is passed to the application through the [**IMFCaptureEngineOnEventCallback::OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) method.</span></span>

<span data-ttu-id="d35e1-111">O valor é um identificador de interface para o componente que gerou o evento.</span><span class="sxs-lookup"><span data-stu-id="d35e1-111">The value is an interface identifier for the component that generated the event.</span></span> <span data-ttu-id="d35e1-112">Por exemplo, o valor **IID \_ IMFCapturePreviewSink** indica o coletor de visualização ([**IMFCapturePreviewSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink)).</span><span class="sxs-lookup"><span data-stu-id="d35e1-112">For example, the value **IID\_IMFCapturePreviewSink** indicates the preview sink ([**IMFCapturePreviewSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink)).</span></span> <span data-ttu-id="d35e1-113">Nem todo evento de captura contém esse atributo.</span><span class="sxs-lookup"><span data-stu-id="d35e1-113">Not every capture event contains this attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="d35e1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d35e1-114">Requirements</span></span>



| <span data-ttu-id="d35e1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d35e1-115">Requirement</span></span> | <span data-ttu-id="d35e1-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d35e1-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d35e1-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d35e1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d35e1-118">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d35e1-118">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="d35e1-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d35e1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d35e1-120">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d35e1-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d35e1-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d35e1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d35e1-122"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="d35e1-122"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d35e1-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="d35e1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d35e1-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d35e1-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d35e1-125">Atributos do mecanismo de captura</span><span class="sxs-lookup"><span data-stu-id="d35e1-125">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="d35e1-126">**IMFCaptureEngine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="d35e1-126">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




