---
description: Usando o coletor de mídia do EVR
ms.assetid: cd98266a-bc62-43da-b4d7-3561447d634f
title: Usando o coletor de mídia do EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84f8c666e88b495ad2d2e53fb1de10364f91636f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105785265"
---
# <a name="using-the-evr-media-sink"></a><span data-ttu-id="83094-103">Usando o coletor de mídia do EVR</span><span class="sxs-lookup"><span data-stu-id="83094-103">Using the EVR Media Sink</span></span>

<span data-ttu-id="83094-104">O coletor de mídia EVR (processador de vídeo avançado) pode ser usado como um componente autônomo.</span><span class="sxs-lookup"><span data-stu-id="83094-104">The enhanced video renderer (EVR) media sink can be used as a stand-alone component.</span></span> <span data-ttu-id="83094-105">No entanto, com mais frequência, um aplicativo criará o coletor de mídia do EVR dentro de uma topologia e, em seguida, usará a sessão de mídia para controlar a reprodução.</span><span class="sxs-lookup"><span data-stu-id="83094-105">More often, however, an application will create the EVR media sink inside a topology, and then use the Media Session to control playback.</span></span>

<span data-ttu-id="83094-106">Há duas maneiras de criar o coletor de mídia do EVR:</span><span class="sxs-lookup"><span data-stu-id="83094-106">There are two ways to create the EVR media sink:</span></span>

-   <span data-ttu-id="83094-107">A função [**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) cria o coletor de mídia.</span><span class="sxs-lookup"><span data-stu-id="83094-107">The [**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) function creates the media sink.</span></span>

-   <span data-ttu-id="83094-108">A função [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) cria um objeto de ativação para o coletor de mídia.</span><span class="sxs-lookup"><span data-stu-id="83094-108">The [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function creates an activation object for the media sink.</span></span>

<span data-ttu-id="83094-109">Inicialmente, o coletor de mídia EVR tem um coletor de fluxo, que corresponde ao fluxo de referência.</span><span class="sxs-lookup"><span data-stu-id="83094-109">The EVR media sink initially has one stream sink, which corresponds to the reference stream.</span></span> <span data-ttu-id="83094-110">Para adicionar novos coletores de fluxo, chame [**IMFMediaSink:: AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink).</span><span class="sxs-lookup"><span data-stu-id="83094-110">To add new stream sinks, call [**IMFMediaSink::AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink).</span></span>

## <a name="related-topics"></a><span data-ttu-id="83094-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="83094-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83094-112">Processador de vídeo aprimorado</span><span class="sxs-lookup"><span data-stu-id="83094-112">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> <dt>

[<span data-ttu-id="83094-113">Coletores de mídia</span><span class="sxs-lookup"><span data-stu-id="83094-113">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 



