---
title: Fluxos de áudio
description: Fluxos de áudio
ms.assetid: 7bb39c48-5d0b-483d-83ee-946adfc9724f
keywords:
- Lojas online do Windows Media Player, fluxos de áudio
- lojas online, fluxos de áudio
- Digite 1 lojas online, fluxos de áudio
- Armazenamentos online do Windows Media Player, fluxos de servidores de música
- lojas online, fluxos de servidores de música
- Digite 1 lojas online, fluxos de servidores de música
- Lojas online do Windows Media Player, fluxos do servidor de música
- lojas online, fluxos de servidor de música
- tipos 1 lojas online, fluxos de servidor de música
- fluxos de áudio
- fluxos do servidor de música
- fluxos de servidores de música
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7164a703417e2efb8e32b2632890972957f7adf7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007137"
---
# <a name="audio-streams"></a><span data-ttu-id="e646f-115">Fluxos de áudio</span><span class="sxs-lookup"><span data-stu-id="e646f-115">Audio Streams</span></span>

<span data-ttu-id="e646f-116">As lojas online podem fornecer música como um fluxo de um servidor de música.</span><span class="sxs-lookup"><span data-stu-id="e646f-116">Online stores can provide music as a stream from a music server.</span></span> <span data-ttu-id="e646f-117">Isso é útil para fornecer exemplos, itens promocionais especiais ou para permitir que os usuários de assinatura desfrutem de música sem precisar baixar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="e646f-117">This is useful for providing samples, special promotional items, or to enable subscription users to enjoy music without having to download the content.</span></span> <span data-ttu-id="e646f-118">É comum não armazenar a URL do fluxo como parte do catálogo de música, mas sim para resolver a URL logo antes da reprodução com base na ID da faixa.</span><span class="sxs-lookup"><span data-stu-id="e646f-118">It is common not to store the URL of the stream as part of the music catalog, but instead to resolve the URL just before playback based upon the track ID.</span></span> <span data-ttu-id="e646f-119">Para habilitar isso, o Windows Media Player chama [IWMPContentPartner:: GetStreamingURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getstreamingurl) e fornece o tipo de streaming (como um valor de enumeração [WMPStreamingType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmpstreamingtype) ) e a ID do fluxo.</span><span class="sxs-lookup"><span data-stu-id="e646f-119">To enable this, Windows Media Player calls [IWMPContentPartner::GetStreamingURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getstreamingurl) and provides the streaming type (as a [WMPStreamingType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmpstreamingtype) enumeration value) and the ID for the stream.</span></span> <span data-ttu-id="e646f-120">O plug-in retorna a URL para o fluxo por meio do parâmetro *pbstrURL* .</span><span class="sxs-lookup"><span data-stu-id="e646f-120">The plug-in returns the URL for the stream through the *pbstrURL* parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e646f-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e646f-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e646f-122">**Sobre o tipo 1 lojas online**</span><span class="sxs-lookup"><span data-stu-id="e646f-122">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> </dl>

 

 




