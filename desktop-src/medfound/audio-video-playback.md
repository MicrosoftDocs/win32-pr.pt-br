---
description: Esta seção descreve como implementar a reprodução de áudio/vídeo em seu aplicativo, usando Microsoft Media Foundation.
ms.assetid: 6efadfe6-013a-4942-9df5-bed557d9af8b
title: Reprodução de áudio/vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6781c531bc7e5c595125d5353a381cc44c08fd5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105797494"
---
# <a name="audiovideo-playback"></a><span data-ttu-id="29de2-103">Reprodução de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="29de2-103">Audio/Video Playback</span></span>

<span data-ttu-id="29de2-104">Esta seção descreve como implementar a reprodução de áudio/vídeo em seu aplicativo, usando Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="29de2-104">This section describes how to implement audio/video playback in your application, using Microsoft Media Foundation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="29de2-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="29de2-105">In this section</span></span>



| <span data-ttu-id="29de2-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="29de2-106">Topic</span></span>                                                                                               | <span data-ttu-id="29de2-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="29de2-107">Description</span></span>                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="29de2-108">Como reproduzir arquivos de mídia com Media Foundation</span><span class="sxs-lookup"><span data-stu-id="29de2-108">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)<br/> | <span data-ttu-id="29de2-109">Este tutorial mostra como reproduzir arquivos de mídia usando o objeto de [sessão de mídia](media-session.md) .</span><span class="sxs-lookup"><span data-stu-id="29de2-109">This tutorial shows how to play media files using the [Media Session](media-session.md) object.</span></span> <br/>                                 |
| [<span data-ttu-id="29de2-110">Como reproduzir arquivos de mídia protegidos</span><span class="sxs-lookup"><span data-stu-id="29de2-110">How to Play Protected Media Files</span></span>](how-to-play-protected-media-files.md)<br/>               | <span data-ttu-id="29de2-111">Como reproduzir arquivos que contêm mídia protegida por DRM.</span><span class="sxs-lookup"><span data-stu-id="29de2-111">How to play files that contain DRM-protected media.</span></span><br/>                                                                               |
| [<span data-ttu-id="29de2-112">Como localizar a duração de um arquivo de mídia</span><span class="sxs-lookup"><span data-stu-id="29de2-112">How to Find the Duration of a Media File</span></span>](how-to-find-the-duration-of-a-media-file.md)<br/> | <span data-ttu-id="29de2-113">Como localizar a duração de um arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="29de2-113">How to find the duration of a media file.</span></span><br/>                                                                                         |
| [<span data-ttu-id="29de2-114">Busca, avanço rápido e reprodução reversa</span><span class="sxs-lookup"><span data-stu-id="29de2-114">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)<br/>   | <span data-ttu-id="29de2-115">Este tópico mostra o código de exemplo para gerenciar alterações de busca e taxa, ao usar a [sessão de mídia](media-session.md) para reprodução.</span><span class="sxs-lookup"><span data-stu-id="29de2-115">This topic shows example code to manage seeking and rate changes, when using the [Media Session](media-session.md) for playback.</span></span><br/> |
| [<span data-ttu-id="29de2-116">Como definir a hora de parada da reprodução</span><span class="sxs-lookup"><span data-stu-id="29de2-116">How to Set the Playback Stop Time</span></span>](how-to-set-the-playback-stop-time-.md)<br/>              | <span data-ttu-id="29de2-117">Este tópico descreve como definir uma hora de parada para reprodução ao usar a [sessão de mídia](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="29de2-117">This topic describes how to set a stop time for playback when using the [Media Session](media-session.md).</span></span><br/>                       |
| [<span data-ttu-id="29de2-118">Processador de vídeo aprimorado</span><span class="sxs-lookup"><span data-stu-id="29de2-118">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)<br/>                                   | <span data-ttu-id="29de2-119">O processador de vídeo avançado (EVR) é um componente que exibe o vídeo no monitor do usuário.</span><span class="sxs-lookup"><span data-stu-id="29de2-119">The enhanced video renderer (EVR) is a component that displays video on the user's monitor.</span></span><br/>                                       |
| [<span data-ttu-id="29de2-120">Processador de streaming de áudio</span><span class="sxs-lookup"><span data-stu-id="29de2-120">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)<br/>                                 | <span data-ttu-id="29de2-121">O SAR (processamento de áudio de streaming) é um coletor de mídia que renderiza áudio.</span><span class="sxs-lookup"><span data-stu-id="29de2-121">The streaming audio renderer (SAR) is a media sink that renders audio.</span></span><br/>                                                            |
| [<span data-ttu-id="29de2-122">MFPlay</span><span class="sxs-lookup"><span data-stu-id="29de2-122">MFPlay</span></span>](using-mfplay-for-audio-video-playback.md)<br/>                                      | <span data-ttu-id="29de2-123">A API MFPlay foi preterida.</span><span class="sxs-lookup"><span data-stu-id="29de2-123">The MFPlay API is deprecated.</span></span><br/>                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="29de2-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="29de2-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29de2-125">Arquitetura Media Foundation</span><span class="sxs-lookup"><span data-stu-id="29de2-125">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="29de2-126">Guia de programação Media Foundation</span><span class="sxs-lookup"><span data-stu-id="29de2-126">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="29de2-127">Suporte a MPEG-4 no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="29de2-127">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> </dl>

 

 




