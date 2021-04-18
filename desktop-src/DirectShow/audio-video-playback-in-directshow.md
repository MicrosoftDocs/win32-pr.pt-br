---
description: Este tutorial mostra como gravar um aplicativo do DirectShow que reproduz um arquivo de mídia.
ms.assetid: 88f4762a-e6e6-4b1e-9951-a409d9d80da9
title: Reprodução de áudio/vídeo no DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca3d681386d85eafc4f32b4e688b920253a51a7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105755800"
---
# <a name="audiovideo-playback-in-directshow"></a><span data-ttu-id="d5562-103">Reprodução de áudio/vídeo no DirectShow</span><span class="sxs-lookup"><span data-stu-id="d5562-103">Audio/Video Playback in DirectShow</span></span>

<span data-ttu-id="d5562-104">Este tutorial mostra como gravar um aplicativo do DirectShow que reproduz um arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="d5562-104">This tutorial shows how to write a DirectShow application that plays a media file.</span></span>

<span data-ttu-id="d5562-105">Antes de ler este tutorial, talvez você queira ler os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="d5562-105">Before reading this tutorial, you might want to read the following topics:</span></span>

-   [<span data-ttu-id="d5562-106">Introdução à programação de aplicativo do DirectShow</span><span class="sxs-lookup"><span data-stu-id="d5562-106">Introduction to DirectShow Application Programming</span></span>](introduction-to-directshow-application-programming.md)
-   [<span data-ttu-id="d5562-107">Como reproduzir um arquivo</span><span class="sxs-lookup"><span data-stu-id="d5562-107">How To Play a File</span></span>](how-to-play-a-file.md)
-   [<span data-ttu-id="d5562-108">Sobre filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="d5562-108">About DirectShow Filters</span></span>](about-directshow-filters.md)
-   [<span data-ttu-id="d5562-109">Sobre o Gerenciador do grafo de filtro</span><span class="sxs-lookup"><span data-stu-id="d5562-109">About the Filter Graph Manager</span></span>](about-the-filter-graph-manager.md)

## <a name="in-this-section"></a><span data-ttu-id="d5562-110">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="d5562-110">In this section</span></span>

-   [<span data-ttu-id="d5562-111">Etapa 1: declarar a classe DShowPlayer</span><span class="sxs-lookup"><span data-stu-id="d5562-111">Step 1: Declare the DShowPlayer Class</span></span>](step-1--declare-the-dshowplayer-class.md)
-   [<span data-ttu-id="d5562-112">Etapa 2: declarar CVideoRenderer e classes derivadas</span><span class="sxs-lookup"><span data-stu-id="d5562-112">Step 2: Declare CVideoRenderer and Derived Classes</span></span>](step-2--declare-cvideorenderer-and-derived-classes.md)
-   [<span data-ttu-id="d5562-113">Etapa 3: criar o gráfico de filtro</span><span class="sxs-lookup"><span data-stu-id="d5562-113">Step 3: Build the Filter Graph</span></span>](step-3--build-the-filter-graph.md)
-   [<span data-ttu-id="d5562-114">Etapa 4: Adicionar o processador de vídeo</span><span class="sxs-lookup"><span data-stu-id="d5562-114">Step 4: Add the Video Renderer</span></span>](step-4--add-the-video-renderer.md)
-   [<span data-ttu-id="d5562-115">Etapa 5: adicionar a funcionalidade de vídeo</span><span class="sxs-lookup"><span data-stu-id="d5562-115">Step 5: Add Video Functionality</span></span>](step-5--add-video-functionality.md)
-   [<span data-ttu-id="d5562-116">Etapa 6: manipular eventos de grafo</span><span class="sxs-lookup"><span data-stu-id="d5562-116">Step 6: Handle Graph Events</span></span>](step-6--handle-graph-events.md)
-   [<span data-ttu-id="d5562-117">Etapa 7: controles de transporte</span><span class="sxs-lookup"><span data-stu-id="d5562-117">Step 7: Transport Controls</span></span>](step-7--transport-controls.md)
-   [<span data-ttu-id="d5562-118">Exemplo de reprodução do DirectShow</span><span class="sxs-lookup"><span data-stu-id="d5562-118">DirectShow Playback Example</span></span>](directshow-playback-example.md)

## <a name="related-topics"></a><span data-ttu-id="d5562-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d5562-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5562-120">Usando o DirectShow</span><span class="sxs-lookup"><span data-stu-id="d5562-120">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



