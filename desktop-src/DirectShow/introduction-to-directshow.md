---
description: Introdução ao DirectShow
ms.assetid: 39a701b3-2633-426f-9733-2172ad3ea372
title: Introdução ao DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5706ff0dec34c5db3762f5782f96804e5c85e889
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827220"
---
# <a name="introduction-to-directshow"></a><span data-ttu-id="7bddc-103">Introdução ao DirectShow</span><span class="sxs-lookup"><span data-stu-id="7bddc-103">Introduction to DirectShow</span></span>

<span data-ttu-id="7bddc-104">Microsoft® DirectShow® é uma arquitetura para mídia de streaming na plataforma microsoft Windows®.</span><span class="sxs-lookup"><span data-stu-id="7bddc-104">Microsoft® DirectShow® is an architecture for streaming media on the Microsoft Windows® platform.</span></span> <span data-ttu-id="7bddc-105">O DirectShow fornece captura de alta qualidade e reprodução de fluxos multimídia.</span><span class="sxs-lookup"><span data-stu-id="7bddc-105">DirectShow provides for high-quality capture and playback of multimedia streams.</span></span> <span data-ttu-id="7bddc-106">Ele dá suporte a uma ampla variedade de formatos, incluindo ASF (Advanced Systems Format), MPEG (Motion Picture Experts Group), Audio-Video INTERleaved (AVI), MPEG Audio Layer-3 (MP3) e arquivos de som WAV.</span><span class="sxs-lookup"><span data-stu-id="7bddc-106">It supports a wide variety of formats, including Advanced Systems Format (ASF), Motion Picture Experts Group (MPEG), Audio-Video Interleaved (AVI), MPEG Audio Layer-3 (MP3), and WAV sound files.</span></span> <span data-ttu-id="7bddc-107">Ele dá suporte à captura de dispositivos digitais e análogos com base Windows Driver Model (WDM) ou Vídeo para Windows.</span><span class="sxs-lookup"><span data-stu-id="7bddc-107">It supports capture from digital and analog devices based on the Windows Driver Model (WDM) or Video for Windows.</span></span> <span data-ttu-id="7bddc-108">Ele detecta e usa automaticamente o hardware de aceleração de áudio e vídeo quando disponível, mas também dá suporte a sistemas sem hardware de aceleração.</span><span class="sxs-lookup"><span data-stu-id="7bddc-108">It automatically detects and uses video and audio acceleration hardware when available, but also supports systems without acceleration hardware.</span></span>

<span data-ttu-id="7bddc-109">O DirectShow é baseado no COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="7bddc-109">DirectShow is based on the Component Object Model (COM).</span></span> <span data-ttu-id="7bddc-110">Para escrever um aplicativo ou componente do DirectShow, você deve entender a programação do cliente COM.</span><span class="sxs-lookup"><span data-stu-id="7bddc-110">To write a DirectShow application or component, you must understand COM client programming.</span></span> <span data-ttu-id="7bddc-111">Para a maioria dos aplicativos, você não precisa implementar seus próprios objetos COM.</span><span class="sxs-lookup"><span data-stu-id="7bddc-111">For most applications, you do not need to implement your own COM objects.</span></span> <span data-ttu-id="7bddc-112">O DirectShow fornece os componentes necessários.</span><span class="sxs-lookup"><span data-stu-id="7bddc-112">DirectShow provides the components you need.</span></span> <span data-ttu-id="7bddc-113">No entanto, se você quiser estender o DirectShow escrevendo seus próprios componentes, deverá implementá-los como objetos COM.</span><span class="sxs-lookup"><span data-stu-id="7bddc-113">If you want to extend DirectShow by writing your own components, however, you must implement them as COM objects.</span></span>

<span data-ttu-id="7bddc-114">O DirectShow foi projetado para C++.</span><span class="sxs-lookup"><span data-stu-id="7bddc-114">DirectShow is designed for C++.</span></span> <span data-ttu-id="7bddc-115">A Microsoft não fornece uma API gerenciada para o DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7bddc-115">Microsoft does not provide a managed API for DirectShow.</span></span>

<span data-ttu-id="7bddc-116">O DirectShow simplifica as tarefas de reprodução de mídia, conversão de formato e captura.</span><span class="sxs-lookup"><span data-stu-id="7bddc-116">DirectShow simplifies media playback, format conversion, and capture tasks.</span></span> <span data-ttu-id="7bddc-117">Ao mesmo tempo, ele fornece acesso à arquitetura de controle de fluxo subjacente para aplicativos que exigem soluções personalizadas.</span><span class="sxs-lookup"><span data-stu-id="7bddc-117">At the same time, it provides access to the underlying stream control architecture for applications that require custom solutions.</span></span> <span data-ttu-id="7bddc-118">Você também pode criar seus próprios componentes do DirectShow para dar suporte a novos formatos ou efeitos personalizados.</span><span class="sxs-lookup"><span data-stu-id="7bddc-118">You can also create your own DirectShow components to support new formats or custom effects.</span></span>

<span data-ttu-id="7bddc-119">Exemplos dos tipos de aplicativo que você pode escrever com o DirectShow incluem players de arquivos, players de TV e DVD, aplicativos de edição de vídeo, conversores de formato de arquivo, aplicativos de captura de áudio e vídeo, codificadores e decodificadores, processadores de sinal digital e muito mais.</span><span class="sxs-lookup"><span data-stu-id="7bddc-119">Examples of the types of application you can write with DirectShow include file players, TV and DVD players, video editing applications, file format converters, audio-video capture applications, encoders and decoders, digital signal processors, and more.</span></span>

<span data-ttu-id="7bddc-120">Esta seção contém os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="7bddc-120">This section contains the following topics:</span></span>

-   [<span data-ttu-id="7bddc-121">Novidades no DirectShow</span><span class="sxs-lookup"><span data-stu-id="7bddc-121">What's New in DirectShow</span></span>](whats-new-in-directshow.md)
-   [<span data-ttu-id="7bddc-122">Formatos com suporte no DirectShow</span><span class="sxs-lookup"><span data-stu-id="7bddc-122">Supported Formats in DirectShow</span></span>](supported-formats-in-directshow.md)
-   [<span data-ttu-id="7bddc-123">Perguntas frequentes sobre o DirectShow</span><span class="sxs-lookup"><span data-stu-id="7bddc-123">DirectShow FAQ</span></span>](directshow-faq.yml)

## <a name="related-topics"></a><span data-ttu-id="7bddc-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7bddc-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bddc-125">Introdução</span><span class="sxs-lookup"><span data-stu-id="7bddc-125">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="7bddc-126">Usando o DirectShow</span><span class="sxs-lookup"><span data-stu-id="7bddc-126">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



