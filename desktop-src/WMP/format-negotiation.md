---
title: Negociação de formato
description: Negociação de formato
ms.assetid: 7847d4e3-1250-4c35-88e1-52d61bf1553f
keywords:
- Plug-ins do Windows Media Player, negociação de formato
- plug-ins, negociação de formato
- plug-ins de processamento de sinal digital, negociação de formato
- Plug-ins do DSP, negociação de formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc805b18d3e2be081e4f85bcc5ed42aded06853
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105794470"
---
# <a name="format-negotiation"></a><span data-ttu-id="12b05-107">Negociação de formato</span><span class="sxs-lookup"><span data-stu-id="12b05-107">Format Negotiation</span></span>

<span data-ttu-id="12b05-108">Para o Windows Media Player e um plug-in do DSP para compartilhar dados, ambos os programas devem concordar com o formato dos dados que estão processando.</span><span class="sxs-lookup"><span data-stu-id="12b05-108">For Windows Media Player and a DSP plug-in to share data, both programs must agree on the format of the data they are processing.</span></span> <span data-ttu-id="12b05-109">O plug-in do DSP implementa métodos que o Player chama para determinar os formatos aos quais o plug-in dá suporte.</span><span class="sxs-lookup"><span data-stu-id="12b05-109">The DSP plug-in implements methods that the Player calls to determine which formats the plug-in supports.</span></span> <span data-ttu-id="12b05-110">O plug-in também implementa métodos que o Player chama para definir o formato atual.</span><span class="sxs-lookup"><span data-stu-id="12b05-110">The plug-in also implements methods that the Player calls to set the current format.</span></span>

<span data-ttu-id="12b05-111">Se o plug-in estiver agindo como um DMO (DirextX Media Object), o Windows Media Player descobre e define os formatos de mídia chamando métodos da interface **IMediaObject** .</span><span class="sxs-lookup"><span data-stu-id="12b05-111">If the plug-in is acting as a DirextX Media Object (DMO), Windows Media Player discovers and sets media formats by calling methods of the **IMediaObject** interface.</span></span> <span data-ttu-id="12b05-112">Por exemplo, o Player chama repetidamente o plug-in **IMediaObject:: GetInputType** para obter uma lista de todos os formatos de entrada com suporte pelo plug-in.</span><span class="sxs-lookup"><span data-stu-id="12b05-112">For example, the Player calls the plug-in's **IMediaObject::GetInputType** repeatedly to get a list of all input formats supported by the plug-in.</span></span> <span data-ttu-id="12b05-113">Plug-ins do DMO usam a estrutura do **\_ \_ tipo de mídia DMO** para organizar as informações que especificam um formato de mídia.</span><span class="sxs-lookup"><span data-stu-id="12b05-113">DMO plug-ins use the **DMO\_MEDIA\_TYPE** structure to organize the information that specifies a media format.</span></span> <span data-ttu-id="12b05-114">Para obter mais informações sobre como plug-ins de DMO e o formato de negociação do Player, consulte [about IMediaObject](about-imediaobject.md).</span><span class="sxs-lookup"><span data-stu-id="12b05-114">For more information about how DMO plug-ins and the Player negotiate format, see [About IMediaObject](about-imediaobject.md).</span></span>

<span data-ttu-id="12b05-115">Se o plug-in estiver agindo como uma Media Foundation transformação (MFT), o Windows Media Player descobre e define os formatos de mídia chamando métodos da interface **IMFTransform** .</span><span class="sxs-lookup"><span data-stu-id="12b05-115">If the plug-in is acting as a Media Foundation Transform (MFT), Windows Media Player discovers and sets media formats by calling methods of the **IMFTransform** interface.</span></span> <span data-ttu-id="12b05-116">Por exemplo, o Player chama a **IMFTransform:: GetInputAvailableType** repetidamente do plug-in para obter uma lista de todos os formatos de entrada com suporte no plug-in.</span><span class="sxs-lookup"><span data-stu-id="12b05-116">For example, the Player calls the plug-in's **IMFTransform::GetInputAvailableType** repeatedly to get a list of all input formats supported by the plug-in.</span></span> <span data-ttu-id="12b05-117">Plug-ins de MFT e o Player usam a interface **IMFMediaType** para organizar e trocar informações de formato.</span><span class="sxs-lookup"><span data-stu-id="12b05-117">MFT plug-ins and the Player use the **IMFMediaType** interface to organize and exchange format information.</span></span>

<span data-ttu-id="12b05-118">O Windows Media Player usará um plug-in de DSP de áudio somente se o plug-in der suporte à mesma profundidade do áudio digital que está sendo reproduzido.</span><span class="sxs-lookup"><span data-stu-id="12b05-118">Windows Media Player will use an audio DSP plug-in only if the plug-in supports the same bit depth as the digital audio being played.</span></span> <span data-ttu-id="12b05-119">Por exemplo, se o áudio digital for de 20 bits, o plug-in deverá ser escrito para processar áudio de 20 bits.</span><span class="sxs-lookup"><span data-stu-id="12b05-119">For instance, if the digital audio is 20-bit, the plug-in must be written to process 20-bit audio.</span></span> <span data-ttu-id="12b05-120">Para áudio de CD, plug-ins DSP devem dar suporte ao processamento de 20 bits.</span><span class="sxs-lookup"><span data-stu-id="12b05-120">For CD audio, DSP plug-ins must support 20-bit processing.</span></span>

<span data-ttu-id="12b05-121">Durante a negociação de formato de conteúdo de vários canais em um computador configurado para uso com alto-falantes estéreo, o Windows Media Player primeiro tenta se conectar a um plug-in de DSP de áudio usando o formato de entrada e saída existente chamando **IMediaObject:: SetInputType** e **IMediaObject:: SetOutputType**.</span><span class="sxs-lookup"><span data-stu-id="12b05-121">During format negotiation of multi-channel content on a computer configured for use with stereo speakers, Windows Media Player first attempts to connect to an audio DSP plug-in using the existing input and output format by calling **IMediaObject::SetInputType** and **IMediaObject::SetOutputType**.</span></span> <span data-ttu-id="12b05-122">Depois que essa negociação inicial ocorre, o Player enumera os formatos aos quais o plug-in dá suporte e tenta negociar a melhor combinação de formato para o Player e o plug-in.</span><span class="sxs-lookup"><span data-stu-id="12b05-122">Once this initial negotiation occurs, the Player then enumerates the formats the plug-in supports and attempts to negotiate the best format combination for the Player and the plug-in.</span></span> <span data-ttu-id="12b05-123">Se o plug-in aceitar áudio estéreo (definido por uma estrutura **WAVEFORMATEX** ) como o formato de entrada durante a negociação inicial e depois aceitar somente o áudio de vários canais (definido por uma estrutura **WAVEFORMATEXTENSIBLE** ), o Player fornecerá áudio multicanal como o formato de entrada para o plug-in.</span><span class="sxs-lookup"><span data-stu-id="12b05-123">If the plug-in accepts stereo audio (defined by a **WAVEFORMATEX** structure) as the input format during the initial negotiation, and then subsequently accepts only multi-channel audio (defined by a **WAVEFORMATEXTENSIBLE** structure), the Player will provide multi-channel audio as the input format to the plug-in.</span></span> <span data-ttu-id="12b05-124">Esse comportamento durante a negociação de formato está disponível para uso no sistema operacional Microsoft Windows XP.</span><span class="sxs-lookup"><span data-stu-id="12b05-124">This behavior during format negotiation is available for use in the Microsoft Windows XP operating system.</span></span> <span data-ttu-id="12b05-125">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="12b05-125">It may be altered or unavailable in subsequent versions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="12b05-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="12b05-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12b05-127">**Visão geral do desenvolvedor de plug-in do DSP**</span><span class="sxs-lookup"><span data-stu-id="12b05-127">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




