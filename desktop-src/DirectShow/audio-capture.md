---
description: Captura de áudio
ms.assetid: 2b7fbdcb-7b59-407e-8e82-e66bd5606507
title: Captura de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e91c9063d96a5e56d078651c338b0ffd80f5aa79
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104296052"
---
# <a name="audio-capture"></a><span data-ttu-id="62447-103">Captura de áudio</span><span class="sxs-lookup"><span data-stu-id="62447-103">Audio Capture</span></span>

<span data-ttu-id="62447-104">Um aplicativo pode usar o DirectShow para capturar dados de áudio de microfones, players de fita e outros dispositivos, por meio das entradas na placa de som.</span><span class="sxs-lookup"><span data-stu-id="62447-104">An application can use DirectShow to capture audio data from microphones, tape players, and other devices, through the inputs on the sound card.</span></span> <span data-ttu-id="62447-105">Os cenários típicos incluem:</span><span class="sxs-lookup"><span data-stu-id="62447-105">Typical scenarios include:</span></span>

-   <span data-ttu-id="62447-106">Gravando uma narração de VoiceOver para Dubbing posteriores em um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="62447-106">Recording a voiceover narration for later dubbing over a video stream.</span></span>
-   <span data-ttu-id="62447-107">Convertendo conteúdo de áudio analógico herdado em formato digital.</span><span class="sxs-lookup"><span data-stu-id="62447-107">Converting legacy analog audio content to digital format.</span></span>
-   <span data-ttu-id="62447-108">Capturando voz ou música para transmissão em uma rede.</span><span class="sxs-lookup"><span data-stu-id="62447-108">Capturing voice or music for transmission over a network.</span></span>

<span data-ttu-id="62447-109">Os usuários finais têm várias opções para capturar áudio da placa de som para o disco rígido.</span><span class="sxs-lookup"><span data-stu-id="62447-109">End users have several options for capturing audio from the sound card to the hard disk.</span></span> <span data-ttu-id="62447-110">A maioria dos cartões fornece aplicativos para misturar e gravar de suas entradas de áudio.</span><span class="sxs-lookup"><span data-stu-id="62447-110">Most cards provide applications for mixing and recording from their audio inputs.</span></span> <span data-ttu-id="62447-111">O Windows fornece o gravador de som, um aplicativo utilitário simples para gravação de um microfone.</span><span class="sxs-lookup"><span data-stu-id="62447-111">Windows provides Sound Recorder, a simple utility application for recording from a microphone.</span></span> <span data-ttu-id="62447-112">O codificador do Windows Media pode ser incorporado em um aplicativo do DirectShow como um DMO ( [objeto de mídia do DirectX](directx-media-objects.md) ).</span><span class="sxs-lookup"><span data-stu-id="62447-112">The Windows Media Encoder can be incorporated into a DirectShow application as a [DirectX Media Object](directx-media-objects.md) (DMO).</span></span> <span data-ttu-id="62447-113">Esta seção descreve como integrar a funcionalidade de captura de áudio em seu próprio aplicativo usando o DirectShow.</span><span class="sxs-lookup"><span data-stu-id="62447-113">This section describes how to integrate audio capture functionality within your own application using DirectShow.</span></span>

<span data-ttu-id="62447-114">Esta seção contém os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="62447-114">This section contains the following topics:</span></span>

-   [<span data-ttu-id="62447-115">Sobre o filtro de captura de áudio</span><span class="sxs-lookup"><span data-stu-id="62447-115">About the Audio Capture Filter</span></span>](about-the-audio-capture-filter.md)
-   [<span data-ttu-id="62447-116">Selecionando um dispositivo de captura</span><span class="sxs-lookup"><span data-stu-id="62447-116">Selecting a Capture Device</span></span>](selecting-a-capture-device.md)
-   [<span data-ttu-id="62447-117">Criando um grafo de captura de áudio</span><span class="sxs-lookup"><span data-stu-id="62447-117">Creating an Audio Capture Graph</span></span>](creating-an-audio-capture-graph.md)
-   [<span data-ttu-id="62447-118">Criando um grafo de captura de áudio com visualização</span><span class="sxs-lookup"><span data-stu-id="62447-118">Creating an Audio Capture Graph with Preview</span></span>](creating-an-audio-capture-graph-with-preview.md)
-   [<span data-ttu-id="62447-119">Definindo propriedades de captura de áudio</span><span class="sxs-lookup"><span data-stu-id="62447-119">Setting Audio Capture Properties</span></span>](setting-audio-capture-properties.md)

## <a name="related-topics"></a><span data-ttu-id="62447-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="62447-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62447-121">Usando o DirectShow</span><span class="sxs-lookup"><span data-stu-id="62447-121">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



