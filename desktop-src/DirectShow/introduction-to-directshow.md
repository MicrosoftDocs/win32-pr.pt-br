---
description: Introdução ao DirectShow
ms.assetid: 39a701b3-2633-426f-9733-2172ad3ea372
title: Introdução ao DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01733db5f8168a67871ec1797f79cd10a90c6c22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087550"
---
# <a name="introduction-to-directshow"></a><span data-ttu-id="7eae0-103">Introdução ao DirectShow</span><span class="sxs-lookup"><span data-stu-id="7eae0-103">Introduction to DirectShow</span></span>

<span data-ttu-id="7eae0-104">O Microsoft® DirectShow® é uma arquitetura para streaming de mídia na plataforma Microsoft Windows®.</span><span class="sxs-lookup"><span data-stu-id="7eae0-104">Microsoft® DirectShow® is an architecture for streaming media on the Microsoft Windows® platform.</span></span> <span data-ttu-id="7eae0-105">O DirectShow fornece captura de alta qualidade e reprodução de fluxos de multimídia.</span><span class="sxs-lookup"><span data-stu-id="7eae0-105">DirectShow provides for high-quality capture and playback of multimedia streams.</span></span> <span data-ttu-id="7eae0-106">Ele dá suporte a uma ampla variedade de formatos, incluindo ASF (Advanced System Format), MPEG (Motion Picture Experts Group), Audio-Video intercalado (AVI), MPEG Audio Layer-3 (MP3) e arquivos de som WAV.</span><span class="sxs-lookup"><span data-stu-id="7eae0-106">It supports a wide variety of formats, including Advanced Systems Format (ASF), Motion Picture Experts Group (MPEG), Audio-Video Interleaved (AVI), MPEG Audio Layer-3 (MP3), and WAV sound files.</span></span> <span data-ttu-id="7eae0-107">Ele dá suporte à captura de dispositivos digitais e analógicos com base no Windows Driver Model (WDM) ou vídeo para Windows.</span><span class="sxs-lookup"><span data-stu-id="7eae0-107">It supports capture from digital and analog devices based on the Windows Driver Model (WDM) or Video for Windows.</span></span> <span data-ttu-id="7eae0-108">Ele detecta e usa automaticamente o hardware de aceleração de vídeo e áudio quando disponível, mas também oferece suporte a sistemas sem aceleração de hardware.</span><span class="sxs-lookup"><span data-stu-id="7eae0-108">It automatically detects and uses video and audio acceleration hardware when available, but also supports systems without acceleration hardware.</span></span>

<span data-ttu-id="7eae0-109">O DirectShow é baseado na Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="7eae0-109">DirectShow is based on the Component Object Model (COM).</span></span> <span data-ttu-id="7eae0-110">Para escrever um aplicativo ou componente do DirectShow, você deve entender a programação de cliente COM.</span><span class="sxs-lookup"><span data-stu-id="7eae0-110">To write a DirectShow application or component, you must understand COM client programming.</span></span> <span data-ttu-id="7eae0-111">Para a maioria dos aplicativos, você não precisa implementar seus próprios objetos COM.</span><span class="sxs-lookup"><span data-stu-id="7eae0-111">For most applications, you do not need to implement your own COM objects.</span></span> <span data-ttu-id="7eae0-112">O DirectShow fornece os componentes de que você precisa.</span><span class="sxs-lookup"><span data-stu-id="7eae0-112">DirectShow provides the components you need.</span></span> <span data-ttu-id="7eae0-113">No entanto, se você quiser estender o DirectShow escrevendo seus próprios componentes, você deve implementá-los como objetos COM.</span><span class="sxs-lookup"><span data-stu-id="7eae0-113">If you want to extend DirectShow by writing your own components, however, you must implement them as COM objects.</span></span>

<span data-ttu-id="7eae0-114">O DirectShow foi projetado para C++.</span><span class="sxs-lookup"><span data-stu-id="7eae0-114">DirectShow is designed for C++.</span></span> <span data-ttu-id="7eae0-115">A Microsoft não fornece uma API gerenciada para o DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7eae0-115">Microsoft does not provide a managed API for DirectShow.</span></span>

<span data-ttu-id="7eae0-116">O DirectShow simplifica a reprodução de mídia, a conversão de formato e as tarefas de captura.</span><span class="sxs-lookup"><span data-stu-id="7eae0-116">DirectShow simplifies media playback, format conversion, and capture tasks.</span></span> <span data-ttu-id="7eae0-117">Ao mesmo tempo, ele fornece acesso à arquitetura de controle de fluxo subjacente para aplicativos que exigem soluções personalizadas.</span><span class="sxs-lookup"><span data-stu-id="7eae0-117">At the same time, it provides access to the underlying stream control architecture for applications that require custom solutions.</span></span> <span data-ttu-id="7eae0-118">Você também pode criar seus próprios componentes do DirectShow para dar suporte a novos formatos ou efeitos personalizados.</span><span class="sxs-lookup"><span data-stu-id="7eae0-118">You can also create your own DirectShow components to support new formats or custom effects.</span></span>

<span data-ttu-id="7eae0-119">Exemplos dos tipos de aplicativo que você pode escrever com o DirectShow incluem players de arquivos, TV e DVD players, aplicativos de edição de vídeo, conversores de formato de arquivo, aplicativos de captura de vídeo de áudio, codificadores e decodificadores, processadores de sinais digitais e muito mais.</span><span class="sxs-lookup"><span data-stu-id="7eae0-119">Examples of the types of application you can write with DirectShow include file players, TV and DVD players, video editing applications, file format converters, audio-video capture applications, encoders and decoders, digital signal processors, and more.</span></span>

<span data-ttu-id="7eae0-120">Esta seção contém os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="7eae0-120">This section contains the following topics:</span></span>

-   [<span data-ttu-id="7eae0-121">O que há de novo no DirectShow</span><span class="sxs-lookup"><span data-stu-id="7eae0-121">What's New in DirectShow</span></span>](whats-new-in-directshow.md)
-   [<span data-ttu-id="7eae0-122">Formatos com suporte no DirectShow</span><span class="sxs-lookup"><span data-stu-id="7eae0-122">Supported Formats in DirectShow</span></span>](supported-formats-in-directshow.md)
-   [<span data-ttu-id="7eae0-123">Perguntas frequentes do DirectShow</span><span class="sxs-lookup"><span data-stu-id="7eae0-123">DirectShow FAQ</span></span>](directshow-faq.md)

## <a name="related-topics"></a><span data-ttu-id="7eae0-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7eae0-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7eae0-125">Introdução</span><span class="sxs-lookup"><span data-stu-id="7eae0-125">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="7eae0-126">Usando o DirectShow</span><span class="sxs-lookup"><span data-stu-id="7eae0-126">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



