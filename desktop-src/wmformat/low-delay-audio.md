---
title: Low-Delay áudio
description: Low-Delay áudio
ms.assetid: f93819eb-f38a-45a0-aa1b-4e677e33daf8
keywords:
- SDK do Windows Media Format, áudio de baixo atraso
- SDK do Windows Media Format, suporte a áudio
- codecs, áudio de baixo atraso
- codecs, suporte a áudio
- áudio de atraso baixo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be8cedd3a6bb54942f5a517c7133e993cf5b11cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105761141"
---
# <a name="low-delay-audio"></a><span data-ttu-id="a3b50-108">Low-Delay áudio</span><span class="sxs-lookup"><span data-stu-id="a3b50-108">Low-Delay Audio</span></span>

<span data-ttu-id="a3b50-109">O áudio de baixo atraso é um modo de codificação que produz áudio compactado com uma configuração de janela de buffer menor que outros modos.</span><span class="sxs-lookup"><span data-stu-id="a3b50-109">Low-delay audio is an encoding mode that produces compressed audio with a smaller buffer-window setting than other modes.</span></span> <span data-ttu-id="a3b50-110">Isso é útil para fluxos que precisam ser alternados rapidamente durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="a3b50-110">This is useful for streams that need to be switched quickly during playback.</span></span> <span data-ttu-id="a3b50-111">O cenário típico para esse recurso é uma apresentação transmitida que inclui a capacidade de alternar arbitrariamente o conteúdo, como alterar o canal de uma televisão.</span><span class="sxs-lookup"><span data-stu-id="a3b50-111">The typical scenario for this feature is a streamed presentation that includes the ability to arbitrarily switch content, like changing the channel of a television.</span></span>

<span data-ttu-id="a3b50-112">Quando você usa um formato de áudio de baixo atraso, a latência para alternar conteúdo é drasticamente reduzida em comparação com outros formatos de áudio.</span><span class="sxs-lookup"><span data-stu-id="a3b50-112">When you use a low-delay audio format, the latency for switching content is drastically reduced compared to other audio formats.</span></span> <span data-ttu-id="a3b50-113">A latência também é reduzida para transmissões ao vivo quando você usa formatos de atraso baixo.</span><span class="sxs-lookup"><span data-stu-id="a3b50-113">Latency is also reduced for live broadcasts when you use low-delay formats.</span></span>

<span data-ttu-id="a3b50-114">Esse recurso tem suporte dos codecs Windows Media áudio 9,1 e Windows Media Audio 9,1 Professional.</span><span class="sxs-lookup"><span data-stu-id="a3b50-114">This feature is supported by the Windows Media Audio 9.1 and Windows Media Audio 9.1 Professional codecs.</span></span> <span data-ttu-id="a3b50-115">Os formatos de atraso baixo estão disponíveis apenas para codificação de taxa de bits constante (uma e duas passagens).</span><span class="sxs-lookup"><span data-stu-id="a3b50-115">Low-delay formats are available only for constant bit rate encoding (both one-pass and two-pass).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3b50-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a3b50-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3b50-117">**Recursos do codec**</span><span class="sxs-lookup"><span data-stu-id="a3b50-117">**Codec Features**</span></span>](codec-features.md)
</dt> </dl>

 

 




