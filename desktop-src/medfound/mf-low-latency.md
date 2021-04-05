---
description: Habilita o processamento de baixa latência no pipeline de Microsoft Media Foundation.
ms.assetid: 4D11B4D6-8CFF-4850-BF8F-9019A1F79153
title: Atributo MF_LOW_LATENCY (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02d1b0a89452256f01fc893ced7dc191fd064bbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662610"
---
# <a name="mf_low_latency-attribute"></a><span data-ttu-id="94827-103">\_Atributo de baixa \_ latência MF</span><span class="sxs-lookup"><span data-stu-id="94827-103">MF\_LOW\_LATENCY attribute</span></span>

<span data-ttu-id="94827-104">Habilita o processamento de baixa latência no pipeline de Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="94827-104">Enables low-latency processing in the Microsoft Media Foundation pipeline.</span></span>

## <a name="data-type"></a><span data-ttu-id="94827-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="94827-105">Data type</span></span>

<span data-ttu-id="94827-106">**Bool** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="94827-106">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="94827-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="94827-107">Get/set</span></span>

<span data-ttu-id="94827-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="94827-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="94827-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="94827-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="94827-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="94827-110">Remarks</span></span>

<span data-ttu-id="94827-111">A baixa latência é definida como o menor atraso possível de quando os dados de mídia são gerados (ou recebidos) quando são renderizados.</span><span class="sxs-lookup"><span data-stu-id="94827-111">Low latency is defined as the smallest possible delay from when the media data is generated (or received) to when it is rendered.</span></span> <span data-ttu-id="94827-112">Baixa latência é desejável para cenários de comunicação em tempo real.</span><span class="sxs-lookup"><span data-stu-id="94827-112">Low latency is desirable for real-time communication scenarios.</span></span> <span data-ttu-id="94827-113">Para outros cenários, como reprodução ou transcodificação local, você normalmente não deve habilitar o modo de baixa latência, pois ele pode afetar a qualidade.</span><span class="sxs-lookup"><span data-stu-id="94827-113">For other scenarios, such as local playback or transcoding, you typically should not enable low-latency mode, because it can affect quality.</span></span>

> [!Note]  
> <span data-ttu-id="94827-114">O valor de GUID desse atributo é idêntico à propriedade [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md) definida para a interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="94827-114">The GUID value of this attribute is identical to the [CODECAPI\_AVLowLatencyMode](codecapi-avlowlatencymode.md) property defined for the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span>

 

<span data-ttu-id="94827-115">Defina esse atributo em componentes de pipeline da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="94827-115">Set this attribute on pipeline components as follows:</span></span>

-   <span data-ttu-id="94827-116">Origem da mídia: Use o método [**IMFMediaSourceEx:: Getsourceattributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getsourceattributes) .</span><span class="sxs-lookup"><span data-stu-id="94827-116">Media source: Use the [**IMFMediaSourceEx::GetSourceAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getsourceattributes) method.</span></span>
-   <span data-ttu-id="94827-117">Media Foundation transformar (MFT): Use o método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .</span><span class="sxs-lookup"><span data-stu-id="94827-117">Media Foundation transform (MFT): Use the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="94827-118">Para os codificadores, o codificador pode dar suporte à baixa latência por meio da interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="94827-118">For encoders, the encoder might support low latency through the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span>
-   <span data-ttu-id="94827-119">Coletor de mídia: consulte o coletor de mídia para a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="94827-119">Media sink: Query the media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="94827-120">Normalmente, os aplicativos não definem esse atributo diretamente nos componentes do pipeline, mas, em vez disso, definem o atributo em um dos seguintes objetos:</span><span class="sxs-lookup"><span data-stu-id="94827-120">Applications typically do not set this attribute directly on the pipeline components, but instead set the attribute on one of the following objects:</span></span>

-   <span data-ttu-id="94827-121">[Sessão de mídia](media-session.md): Use o parâmetro *PConfiguation* da função [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) ou [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) , ou então defina o atributo na topologia.</span><span class="sxs-lookup"><span data-stu-id="94827-121">[Media Session](media-session.md): Use the *pConfiguation* parameter of the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) or [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function, or else set the attribute on the topology.</span></span>
-   <span data-ttu-id="94827-122">[Leitor de origem](source-reader.md): defina o atributo com as propriedades de configuração ao criar o leitor de origem.</span><span class="sxs-lookup"><span data-stu-id="94827-122">[Source Reader](source-reader.md): Set the attribute with the configuration properties when you create the Source Reader.</span></span> <span data-ttu-id="94827-123">Para obter mais informações, consulte [atributos do leitor de origem](source-reader-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="94827-123">For more information, see [Source Reader Attributes](source-reader-attributes.md).</span></span>
-   <span data-ttu-id="94827-124">[Gravador de coletor](sink-writer.md): defina o atributo com as propriedades de configuração ao criar o gravador de coletor.</span><span class="sxs-lookup"><span data-stu-id="94827-124">[Sink Writer](sink-writer.md): Set the attribute with the configuration properties when you create the Sink Writer.</span></span> <span data-ttu-id="94827-125">Para obter mais informações, consulte [atributos do gravador do coletor](sink-writer-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="94827-125">For more information, see [Sink Writer Attributes](sink-writer-attributes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="94827-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94827-126">Requirements</span></span>



| <span data-ttu-id="94827-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="94827-127">Requirement</span></span> | <span data-ttu-id="94827-128">Valor</span><span class="sxs-lookup"><span data-stu-id="94827-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="94827-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94827-129">Minimum supported client</span></span><br/> | <span data-ttu-id="94827-130">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="94827-130">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="94827-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94827-131">Minimum supported server</span></span><br/> | <span data-ttu-id="94827-132">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="94827-132">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="94827-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="94827-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="94827-134"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="94827-134"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94827-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="94827-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94827-136">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="94827-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="94827-137">Atributos do gravador de coletor</span><span class="sxs-lookup"><span data-stu-id="94827-137">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> <dt>

[<span data-ttu-id="94827-138">Atributos do leitor de origem</span><span class="sxs-lookup"><span data-stu-id="94827-138">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> <dt>

[<span data-ttu-id="94827-139">Atributos de transformação</span><span class="sxs-lookup"><span data-stu-id="94827-139">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 
