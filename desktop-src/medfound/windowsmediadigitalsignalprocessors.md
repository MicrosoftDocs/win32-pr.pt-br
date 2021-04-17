---
description: Processadores de sinais digitais
ms.assetid: cd3952ca-3958-4944-8fde-f0163a47bff9
title: Processadores de sinais digitais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0961554d9c9902e68f74c6b2b57662b23846614f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105763487"
---
# <a name="digital-signal-processors"></a><span data-ttu-id="b8811-103">Processadores de sinais digitais</span><span class="sxs-lookup"><span data-stu-id="b8811-103">Digital Signal Processors</span></span>

<span data-ttu-id="b8811-104">Esta seção descreve os objetos do processador de sinais digitais (DSP) fornecidos pelo Windows.</span><span class="sxs-lookup"><span data-stu-id="b8811-104">This section describes the digital signal processor (DSP) objects provided by Windows.</span></span>

<span data-ttu-id="b8811-105">A Microsoft usa o termo *processador de sinal digital* para designar um conjunto de objetos com que executam transformações em dados de vídeo e áudio não compactados.</span><span class="sxs-lookup"><span data-stu-id="b8811-105">Microsoft uses the term *digital signal processor* to designate a set of COM objects that perform transformations on uncompressed audio and video data.</span></span> <span data-ttu-id="b8811-106">Os DSPs descritos neste SDK transformam áudio e vídeo em uma variedade de formatos descompactados.</span><span class="sxs-lookup"><span data-stu-id="b8811-106">The DSPs described in this SDK transform audio and video in a variety of uncompressed formats.</span></span>

<span data-ttu-id="b8811-107">Os DSPs podem ser usados por si próprios ou em combinação com codecs de áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="b8811-107">The DSPs can be used by themselves, or in combination with audio and video codecs.</span></span> <span data-ttu-id="b8811-108">Com exceção do DSP de captura de voz, cada DSP listado aqui implementa duas interfaces separadas, mas semelhantes.</span><span class="sxs-lookup"><span data-stu-id="b8811-108">With the exception of the Voice Capture DSP, each DSP listed here implements two separate but similar interfaces.</span></span>



| <span data-ttu-id="b8811-109">Interface</span><span class="sxs-lookup"><span data-stu-id="b8811-109">Interface</span></span>                              | <span data-ttu-id="b8811-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="b8811-110">Description</span></span>                                 |
|----------------------------------------|---------------------------------------------|
| [<span data-ttu-id="b8811-111">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="b8811-111">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)   | <span data-ttu-id="b8811-112">Compatível com Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="b8811-112">Compatible with Microsoft Media Foundation.</span></span> |
| [<span data-ttu-id="b8811-113">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="b8811-113">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) | <span data-ttu-id="b8811-114">Compatível com o DirectShow.</span><span class="sxs-lookup"><span data-stu-id="b8811-114">Compatible with DirectShow.</span></span>                 |



 

<span data-ttu-id="b8811-115">Você pode configurar os DSPs usando a interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para definir propriedades.</span><span class="sxs-lookup"><span data-stu-id="b8811-115">You can configure the DSPs by using the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface to set properties.</span></span> <span data-ttu-id="b8811-116">Alguns dos DSPs têm interfaces adicionais que definem propriedades.</span><span class="sxs-lookup"><span data-stu-id="b8811-116">Some of the DSPs have additional interfaces that set properties.</span></span> <span data-ttu-id="b8811-117">Para usar essas interfaces, chame o método [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) de qualquer outra interface do DSP.</span><span class="sxs-lookup"><span data-stu-id="b8811-117">To use these interfaces, call the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method of any other interface of the DSP.</span></span> <span data-ttu-id="b8811-118">O tópico de referência para cada DSP lista as propriedades, interfaces e outros recursos com suporte.</span><span class="sxs-lookup"><span data-stu-id="b8811-118">The reference topic for each DSP lists the supported properties, interfaces, and other features.</span></span>

<span data-ttu-id="b8811-119">Esta seção contém os seguintes tópicos.</span><span class="sxs-lookup"><span data-stu-id="b8811-119">This section contains the following topics.</span></span>



| <span data-ttu-id="b8811-120">DSP</span><span class="sxs-lookup"><span data-stu-id="b8811-120">DSP</span></span>                                                      | <span data-ttu-id="b8811-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="b8811-121">Description</span></span>                                          |
|----------------------------------------------------------|------------------------------------------------------|
| [<span data-ttu-id="b8811-122">DSP de reamostragem de áudio</span><span class="sxs-lookup"><span data-stu-id="b8811-122">Audio Resampler DSP</span></span>](audioresampler.md)                | <span data-ttu-id="b8811-123">Converte a taxa de amostragem de um fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="b8811-123">Converts the sampling rate of an audio stream.</span></span>       |
| [<span data-ttu-id="b8811-124">DSP de transformação de controle de cores</span><span class="sxs-lookup"><span data-stu-id="b8811-124">Color Control Transform DSP</span></span>](colorcontroltransform.md) | <span data-ttu-id="b8811-125">Ajusta as características de cor de um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b8811-125">Adjusts the color characteristics of a video stream.</span></span> |
| [<span data-ttu-id="b8811-126">DSP de conversor de cores</span><span class="sxs-lookup"><span data-stu-id="b8811-126">Color Converter DSP</span></span>](colorconverter.md)                | <span data-ttu-id="b8811-127">Converte um fluxo de vídeo entre formatos de cor.</span><span class="sxs-lookup"><span data-stu-id="b8811-127">Converts a video stream between color formats.</span></span>       |
| [<span data-ttu-id="b8811-128">Conversor de taxa de quadros DSP</span><span class="sxs-lookup"><span data-stu-id="b8811-128">Frame Rate Converter DSP</span></span>](framerateconverter.md)       | <span data-ttu-id="b8811-129">Altera a taxa de quadros de um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b8811-129">Changes the frame rate of a video stream.</span></span>            |
| [<span data-ttu-id="b8811-130">DSP de redimensionador de vídeo</span><span class="sxs-lookup"><span data-stu-id="b8811-130">Video Resizer DSP</span></span>](videoresizer.md)                    | <span data-ttu-id="b8811-131">Redimensiona um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b8811-131">Resizes a video stream.</span></span>                              |
| [<span data-ttu-id="b8811-132">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="b8811-132">Voice Capture DSP</span></span>](voicecapturedmo.md)                 | <span data-ttu-id="b8811-133">Encapsula vários DSPs relacionados à captura de voz.</span><span class="sxs-lookup"><span data-stu-id="b8811-133">Encapsulates several DSPs related to voice capture.</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="b8811-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b8811-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8811-135">Referência de programação do Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b8811-135">Media Foundation Programming Reference</span></span>](media-foundation-programming-reference.md)
</dt> </dl>

 

 
