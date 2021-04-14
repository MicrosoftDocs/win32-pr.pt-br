---
description: Introdução aos serviços de edição do DirectShow
ms.assetid: 247c4ba9-53c1-46ed-83ef-a454351920e3
title: Introdução aos serviços de edição do DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c75d9cf22eba81ebb9794310f63983b991bcf22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456598"
---
# <a name="introduction-to-directshow-editing-services"></a><span data-ttu-id="ba241-103">Introdução aos serviços de edição do DirectShow</span><span class="sxs-lookup"><span data-stu-id="ba241-103">Introduction to DirectShow Editing Services</span></span>

<span data-ttu-id="ba241-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="ba241-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="ba241-105">O núcleo do DirectShow é uma arquitetura poderosa para lidar com mídias de streaming.</span><span class="sxs-lookup"><span data-stu-id="ba241-105">The core of DirectShow is a powerful architecture for handling streaming media.</span></span> <span data-ttu-id="ba241-106">Um aplicativo pode usá-lo para reproduzir conteúdo multimídia criado em uma ampla variedade de formatos, sem que o desenvolvedor precise se preocupar com a compactação de arquivos e outros detalhes entediantes.</span><span class="sxs-lookup"><span data-stu-id="ba241-106">An application can use it to play multimedia content authored in a wide variety of formats, without the developer needing to worry about file compression and other tedious details.</span></span> <span data-ttu-id="ba241-107">Antes [dos serviços de edição do DirectShow](directshow-editing-services.md) (des), no entanto, o DirectShow não tinha a flexibilidade necessária para edição não linear.</span><span class="sxs-lookup"><span data-stu-id="ba241-107">Prior to [DirectShow Editing Services](directshow-editing-services.md) (DES), however, DirectShow lacked the flexibility needed for nonlinear editing.</span></span>

<span data-ttu-id="ba241-108">Por exemplo, suponha que você quisesse criar uma sequência de vídeo consistindo de 4 segundos da origem A, seguida de 10 segundos da origem B e terminando com 5 segundos da fonte C. Você poderia fazer isso com muito facilidade usando apenas a API do DirectShow principal.</span><span class="sxs-lookup"><span data-stu-id="ba241-108">For example, suppose you wanted to create a video sequence consisting of 4 seconds from source A, followed by 10 seconds from source B, and ending with 5 seconds from source C. You could accomplish that much fairly easily using only the core DirectShow API.</span></span>

<span data-ttu-id="ba241-109">Mas e se você decidiu que a fonte C deveria vir antes da origem B, não após; que a sequência deve usar 8 segundos da origem A, não 4; e que toda a produção precisava de uma faixa de áudio separada tocando em segundo plano?</span><span class="sxs-lookup"><span data-stu-id="ba241-109">But what if you decided that source C should come before source B, not after; that the sequence should use 8 seconds from source A, not 4; and that the entire production needed a separate audio track playing in the background?</span></span> <span data-ttu-id="ba241-110">Até mesmo alterações secundárias, como essas podem ser difíceis de implementar.</span><span class="sxs-lookup"><span data-stu-id="ba241-110">Even minor changes such as these could be difficult to implement.</span></span> <span data-ttu-id="ba241-111">Mas o cenário que acabei de descrever é um projeto de edição trivial no DES — você pode fazer isso com algumas chamadas de método.</span><span class="sxs-lookup"><span data-stu-id="ba241-111">But the scenario just described is a trivial editing project in DES—you can do it with a handful of method calls.</span></span>

<span data-ttu-id="ba241-112">Aqui estão alguns dos recursos que o DES traz para o DirectShow:</span><span class="sxs-lookup"><span data-stu-id="ba241-112">Here are some of the features that DES brings to DirectShow:</span></span>

-   <span data-ttu-id="ba241-113">Um modelo de linha do tempo que organiza faixas de áudio e vídeo em camadas aninhadas, facilitando a manipulação da produção final</span><span class="sxs-lookup"><span data-stu-id="ba241-113">A timeline model that organizes video and audio tracks into nested layers, making it easy to manipulate the final production</span></span>
-   <span data-ttu-id="ba241-114">A capacidade de Visualizar um projeto de vídeo em tempo real</span><span class="sxs-lookup"><span data-stu-id="ba241-114">The ability to preview a video project on the fly</span></span>
-   <span data-ttu-id="ba241-115">Persistência do projeto por meio de um formato baseado em XML</span><span class="sxs-lookup"><span data-stu-id="ba241-115">Project persistence through an XML-based format</span></span>
-   <span data-ttu-id="ba241-116">Suporte para efeitos de vídeo e áudio, bem como transições entre faixas de vídeo (como fade e borrachas)</span><span class="sxs-lookup"><span data-stu-id="ba241-116">Support for video and audio effects, as well as transitions between video tracks (such as fades and wipes)</span></span>
-   <span data-ttu-id="ba241-117">Mais de 100 de apagamentos padrão, conforme definido pela sociedade de imagem e engenheiros de televisão (SMPTE)</span><span class="sxs-lookup"><span data-stu-id="ba241-117">Over 100 standard wipes, as defined by the Society of Motion Picture and Television Engineers (SMPTE)</span></span>
-   <span data-ttu-id="ba241-118">Inserindo com base em matiz, luminância, valor RGB ou valor alfa</span><span class="sxs-lookup"><span data-stu-id="ba241-118">Keying based on hue, luminance, RGB value, or alpha value</span></span>
-   <span data-ttu-id="ba241-119">Conversão automática de taxas de quadros e taxas de amostragem de áudio, permitindo que uma produção use fontes heterogêneas</span><span class="sxs-lookup"><span data-stu-id="ba241-119">Automatic conversion of frame rates and audio sampling rates, enabling a production to use heterogeneous sources</span></span>
-   <span data-ttu-id="ba241-120">Redimensionamento ou corte de vídeo</span><span class="sxs-lookup"><span data-stu-id="ba241-120">Resizing or cropping of video</span></span>

<span data-ttu-id="ba241-121">Limitações:</span><span class="sxs-lookup"><span data-stu-id="ba241-121">Limitations:</span></span>

-   <span data-ttu-id="ba241-122">O DES não oferece suporte a fontes de vídeo MPEG-2 ou H. 264.</span><span class="sxs-lookup"><span data-stu-id="ba241-122">DES does not support MPEG-2 or H.264 video sources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba241-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ba241-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba241-124">Serviços de edição do DirectShow</span><span class="sxs-lookup"><span data-stu-id="ba241-124">DirectShow Editing Services</span></span>](directshow-editing-services.md)
</dt> </dl>

 

 



