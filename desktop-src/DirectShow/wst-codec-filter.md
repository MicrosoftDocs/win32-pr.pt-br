---
description: Filtro de codec de WST
ms.assetid: 0a06acbf-b842-4ab6-bcf9-d2d006301d83
title: Filtro de codec de WST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338db987986a5f4706c144907d122eec3a0615a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297608"
---
# <a name="wst-codec-filter"></a><span data-ttu-id="f380d-103">Filtro de codec de WST</span><span class="sxs-lookup"><span data-stu-id="f380d-103">WST Codec Filter</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f380d-104">Este componente foi removido do Windows Vista e de sistemas operacionais posteriores.</span><span class="sxs-lookup"><span data-stu-id="f380d-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="f380d-105">Ele está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f380d-105">It is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

 

<span data-ttu-id="f380d-106">A partir do Windows Vista, esse filtro é substituído pelo filtro VBICodec, que está documentado na documentação das tecnologias de TV da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f380d-106">Starting in Windows Vista, this filter is replaced by the VBICodec filter, which is documented in the Microsoft TV Technologies documentation.</span></span>

<span data-ttu-id="f380d-107">O teletexto padrão mundial (WST) é o padrão europeu para transmissão de dados usando VBI em sinais de televisão analógicas da PAL.</span><span class="sxs-lookup"><span data-stu-id="f380d-107">World Standard Teletext (WST) is the European standard for data transmission using VBI on PAL analog television signals.</span></span> <span data-ttu-id="f380d-108">Tanto a legenda quanto os serviços de dados são fornecidos usando esse padrão.</span><span class="sxs-lookup"><span data-stu-id="f380d-108">Both captioning and data services are provided using this standard.</span></span> <span data-ttu-id="f380d-109">O codec de WST é um filtro de modo kernel que recebe exemplos VBI brutos e, opcionalmente, exemplos de telecódigo de telecodificação do filtro de captura por meio do filtro de [conversor de alto e Sink para coletor](tee-sink-to-sink-converter.md) .</span><span class="sxs-lookup"><span data-stu-id="f380d-109">The WST Codec is a kernel-mode filter that receives raw VBI samples and, optionally, decoded Teletext samples from the Capture Filter via the [Tee/Sink-to-Sink Converter](tee-sink-to-sink-converter.md) filter.</span></span> <span data-ttu-id="f380d-110">Esse codec decodifica e/ou duplica os dados de telecodificação e de encaminhamento de erros corrigidos para o filtro de [decodificador de WST](wst-decoder-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="f380d-110">This codec decodes and/or duplicates the decoded and forward-error-corrected Teletext data for the [WST Decoder](wst-decoder-filter.md) filter.</span></span> <span data-ttu-id="f380d-111">O codec de WST corresponde ao filtro de decodificador de CC para transmissões NTSC.</span><span class="sxs-lookup"><span data-stu-id="f380d-111">The WST Codec corresponds to the CC Decoder filter for NTSC transmissions.</span></span> <span data-ttu-id="f380d-112">O decodificador de WST corresponde ao [decodificador de linha 21](line-21-decoder-filter.md) para NTSC; esses filtros criam os bitmaps que são enviados para o mixer de sobreposição ou o processador de mixagem de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f380d-112">The WST Decoder corresponds to the [Line 21 Decoder](line-21-decoder-filter.md) for NTSC; these filters create the bitmaps that are sent to the Overlay Mixer or the Video Mixing Renderer.</span></span>

<span data-ttu-id="f380d-113">Esse filtro tem dois pinos de entrada, VBI e HWCC.</span><span class="sxs-lookup"><span data-stu-id="f380d-113">This filter has two input pins, VBI and HWCC.</span></span> <span data-ttu-id="f380d-114">O PIN do VBI é usado para dados brutos do VBI e o PIN do HWCC é usado quando a decodificação de VBI é executada no hardware pelo filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="f380d-114">The VBI pin is used for raw VBI data, and the HWCC pin is used when the VBI decoding is performed in hardware by the capture filter.</span></span> <span data-ttu-id="f380d-115">Quando os dados são recebidos no PIN do HWCC, o codec de WST opera no modo de "passagem" e envia os dados diretamente para o decodificador de WST sem processá-los de forma alguma.</span><span class="sxs-lookup"><span data-stu-id="f380d-115">When the data is received on the HWCC pin, the WST Codec operates in "pass-through" mode, and sends the data directly to the WST Decoder without processing it in any way.</span></span> <span data-ttu-id="f380d-116">Se o filtro de captura expõe um PIN HWCC, ele deve ser conectado diretamente ao PIN correspondente no codec de WST.</span><span class="sxs-lookup"><span data-stu-id="f380d-116">If the capture filter exposes an HWCC pin, it must be connected directly to the corresponding pin on the WST Codec.</span></span>

<span data-ttu-id="f380d-117">O filtro de codec de WST aparece na categoria de filtro "codecs VBI de streaming WDM" (**am \_ KSCATEGORY \_ VBICODEC**).</span><span class="sxs-lookup"><span data-stu-id="f380d-117">The WST Codec filter appears in the "WDM Streaming VBI Codecs" filter category (**AM\_KSCATEGORY\_VBICODEC**).</span></span>

<span data-ttu-id="f380d-118">Como esse é um filtro de modo kernel, os aplicativos não podem criá-lo diretamente usando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="f380d-118">Because this is a kernel-mode filter, applications cannot create it directly using **CoCreateInstance**.</span></span> <span data-ttu-id="f380d-119">Em vez disso, use o [enumerador de dispositivo do sistema](system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="f380d-119">Instead, use the [System Device Enumerator](system-device-enumerator.md).</span></span> <span data-ttu-id="f380d-120">Para obter mais informações, consulte [Criando filtros de Kernel-Mode](creating-kernel-mode-filters.md).</span><span class="sxs-lookup"><span data-stu-id="f380d-120">For more information, see [Creating Kernel-Mode Filters](creating-kernel-mode-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f380d-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f380d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f380d-122">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="f380d-122">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="f380d-123">Exibindo teletexto do mundo Standard</span><span class="sxs-lookup"><span data-stu-id="f380d-123">Viewing World Standard Teletext</span></span>](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



