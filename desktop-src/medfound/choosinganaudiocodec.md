---
description: Escolhendo um codec de áudio
ms.assetid: 37f3582c-c718-42ae-b887-d7d31ee853e9
title: Escolhendo um codec de áudio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a04b16dc0c6e65356f7d7e74b85b0671c2b41369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164217"
---
# <a name="choosing-an-audio-codec-microsoft-media-foundation"></a><span data-ttu-id="29f10-103">Escolhendo um codec de áudio (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="29f10-103">Choosing an Audio Codec (Microsoft Media Foundation)</span></span>

<span data-ttu-id="29f10-104">O [**codificador de áudio do Windows Media**](windowsmediaaudioencoder.md) fornece três categorias de codificação de áudio, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="29f10-104">The [**Windows Media Audio Encoder**](windowsmediaaudioencoder.md) provides three categories of audio encoding as shown in the following table.</span></span>



| <span data-ttu-id="29f10-105">Categoria</span><span class="sxs-lookup"><span data-stu-id="29f10-105">Category</span></span>                         | <span data-ttu-id="29f10-106">Finalidade</span><span class="sxs-lookup"><span data-stu-id="29f10-106">Purpose</span></span>                                                    |
|----------------------------------|------------------------------------------------------------|
| <span data-ttu-id="29f10-107">Padrão de áudio do Windows Media</span><span class="sxs-lookup"><span data-stu-id="29f10-107">Windows Media Audio Standard</span></span>     | <span data-ttu-id="29f10-108">Compactação de uso geral de áudio.</span><span class="sxs-lookup"><span data-stu-id="29f10-108">General-purpose compression of audio.</span></span>                      |
| <span data-ttu-id="29f10-109">Windows Media Audio Professional</span><span class="sxs-lookup"><span data-stu-id="29f10-109">Windows Media Audio Professional</span></span> | <span data-ttu-id="29f10-110">Compactação de áudio de alta definição e de vários canais.</span><span class="sxs-lookup"><span data-stu-id="29f10-110">Compressing multi-channel and high-definition audio.</span></span>       |
| <span data-ttu-id="29f10-111">Windows Media Audio sem perdas</span><span class="sxs-lookup"><span data-stu-id="29f10-111">Windows Media Audio Lossless</span></span>     | <span data-ttu-id="29f10-112">Compactação de áudio sem perder nenhum dos dados originais.</span><span class="sxs-lookup"><span data-stu-id="29f10-112">Compressing audio without losing any of the original data.</span></span> |



 

<span data-ttu-id="29f10-113">A categoria padrão fornece codificação de áudio de uso geral adequada para uma variedade de cenários de reprodução.</span><span class="sxs-lookup"><span data-stu-id="29f10-113">The Standard category provides general-purpose audio encoding suitable for a variety of playback scenarios.</span></span> <span data-ttu-id="29f10-114">Por exemplo, ele pode compactar áudio para uma taxa de bits baixa para streaming em uma rede com largura de banda limitada ou para renderização em dispositivos portáteis.</span><span class="sxs-lookup"><span data-stu-id="29f10-114">For example, it can compress audio to a low bit rate for streaming over a network with limited bandwidth, or for rendering on portable devices.</span></span> <span data-ttu-id="29f10-115">Na outra extremidade da escala, ele pode produzir conteúdo de áudio compactado para reprodução de alta qualidade.</span><span class="sxs-lookup"><span data-stu-id="29f10-115">On the other end of the scale, it can produce compressed audio content for high-quality playback.</span></span> <span data-ttu-id="29f10-116">A ênfase dos algoritmos de codificação padrão está em música, mas eles são adequados para outros conteúdos de áudio complexos também.</span><span class="sxs-lookup"><span data-stu-id="29f10-116">The emphasis of the Standard encoding algorithms is on music, but they are suitable for other complex audio content as well.</span></span> <span data-ttu-id="29f10-117">A categoria padrão deve ser seu padrão de conteúdo de áudio.</span><span class="sxs-lookup"><span data-stu-id="29f10-117">The Standard category should be your default for audio content.</span></span> <span data-ttu-id="29f10-118">As categorias Professional e Lossless devem ser usadas para atender a necessidades específicas.</span><span class="sxs-lookup"><span data-stu-id="29f10-118">The Professional and Lossless categories should be used to meet specific needs.</span></span>

<span data-ttu-id="29f10-119">Um codificador separado, o [**codificador do Windows Media Voice**](windowsmediaaudiovoiceencoder.md), fornece a compactação de fala.</span><span class="sxs-lookup"><span data-stu-id="29f10-119">A separate encoder, the [**Windows Media Voice Encoder**](windowsmediaaudiovoiceencoder.md), provides compression of speech.</span></span>

## <a name="related-topics"></a><span data-ttu-id="29f10-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="29f10-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29f10-121">Trabalhando com áudio</span><span class="sxs-lookup"><span data-stu-id="29f10-121">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 



