---
description: Codificação de arquivos e interfaces de decodificação
ms.assetid: 5456392d-2557-43b6-93b7-b2ebde218d12
title: Codificação de arquivos e interfaces de decodificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f73de2304f2b473a634127755ca900b99592ed63
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104088803"
---
# <a name="file-encoding-and-decoding-interfaces"></a><span data-ttu-id="05294-103">Codificação de arquivos e interfaces de decodificação</span><span class="sxs-lookup"><span data-stu-id="05294-103">File Encoding and Decoding Interfaces</span></span>

<span data-ttu-id="05294-104">Essas interfaces dão suporte à codificação e decodificação de arquivos.</span><span class="sxs-lookup"><span data-stu-id="05294-104">These interfaces support file encoding and decoding.</span></span>



| <span data-ttu-id="05294-105">Interface</span><span class="sxs-lookup"><span data-stu-id="05294-105">Interface</span></span>                                                    | <span data-ttu-id="05294-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="05294-106">Description</span></span>                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="05294-107">**IAMMediaContent**</span><span class="sxs-lookup"><span data-stu-id="05294-107">**IAMMediaContent**</span></span>](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent)                   | <span data-ttu-id="05294-108">Recupere metadados de um fluxo, como o autor e o título.</span><span class="sxs-lookup"><span data-stu-id="05294-108">Retrieve meta-data from a stream, such as the author and title.</span></span>                                              |
| [<span data-ttu-id="05294-109">**IAMOpenProgress**</span><span class="sxs-lookup"><span data-stu-id="05294-109">**IAMOpenProgress**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress)                   | <span data-ttu-id="05294-110">Determine o progresso de uma operação de abertura de arquivo.</span><span class="sxs-lookup"><span data-stu-id="05294-110">Determine the progress of a file-open operation.</span></span>                                                             |
| [<span data-ttu-id="05294-111">**IAMParse**</span><span class="sxs-lookup"><span data-stu-id="05294-111">**IAMParse**</span></span>](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse)                                 | <span data-ttu-id="05294-112">Consulte e defina o tempo de análise para a posição atual em um fluxo MPEG.</span><span class="sxs-lookup"><span data-stu-id="05294-112">Query and set the parse time for the current position in an MPEG stream.</span></span>                                     |
| [<span data-ttu-id="05294-113">**IAMStreamSelect**</span><span class="sxs-lookup"><span data-stu-id="05294-113">**IAMStreamSelect**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect)                   | <span data-ttu-id="05294-114">Controlar quais fluxos lógicos são reproduzidos e recuperar informações sobre eles.</span><span class="sxs-lookup"><span data-stu-id="05294-114">Control which logical streams are played, and retrieve information about them.</span></span>                               |
| [<span data-ttu-id="05294-115">**IAMVfwCompressDialogs**</span><span class="sxs-lookup"><span data-stu-id="05294-115">**IAMVfwCompressDialogs**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs)       | <span data-ttu-id="05294-116">Exibir caixas de diálogo fornecidas por codecs VFW.</span><span class="sxs-lookup"><span data-stu-id="05294-116">Display dialog boxes provided by VFW codecs.</span></span>                                                                 |
| [<span data-ttu-id="05294-117">**IAMVideoCompression**</span><span class="sxs-lookup"><span data-stu-id="05294-117">**IAMVideoCompression**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression)           | <span data-ttu-id="05294-118">Defina os parâmetros de compactação de vídeo.</span><span class="sxs-lookup"><span data-stu-id="05294-118">Set video compression parameters.</span></span>                                                                            |
| [<span data-ttu-id="05294-119">**IConfigAsfWriter**</span><span class="sxs-lookup"><span data-stu-id="05294-119">**IConfigAsfWriter**</span></span>](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter)                 | <span data-ttu-id="05294-120">Controle como o filtro do [gravador ASF do WM](wm-asf-writer-filter.md) grava arquivos ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="05294-120">Control how the [WM ASF Writer](wm-asf-writer-filter.md) filter writes Advanced Systems Format (ASF) files.</span></span> |
| [<span data-ttu-id="05294-121">**IConfigAviMux**</span><span class="sxs-lookup"><span data-stu-id="05294-121">**IConfigAviMux**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux)                       | <span data-ttu-id="05294-122">Controle como o filtro [AVI Mux](avi-mux-filter.md) grava arquivos AVI.</span><span class="sxs-lookup"><span data-stu-id="05294-122">Control how the [AVI Mux](avi-mux-filter.md) filter writes AVI files.</span></span>                                       |
| [<span data-ttu-id="05294-123">**IConfigInterleaving**</span><span class="sxs-lookup"><span data-stu-id="05294-123">**IConfigInterleaving**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving)           | <span data-ttu-id="05294-124">Configure a intercalação quando o filtro AVI Mux gravar arquivos AVI.</span><span class="sxs-lookup"><span data-stu-id="05294-124">Configure interleaving when the AVI Mux filter writes AVI files.</span></span>                                             |
| [<span data-ttu-id="05294-125">**IDVEnc**</span><span class="sxs-lookup"><span data-stu-id="05294-125">**IDVEnc**</span></span>](/windows/desktop/api/Strmif/nn-strmif-idvenc)                                     | <span data-ttu-id="05294-126">Defina a resolução de codificação no filtro do [codificador de vídeo DV](dv-video-encoder-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="05294-126">Set the encoding resolution on the [DV Video Encoder](dv-video-encoder-filter.md) filter.</span></span>                   |
| [<span data-ttu-id="05294-127">**IDVSplitter**</span><span class="sxs-lookup"><span data-stu-id="05294-127">**IDVSplitter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-idvsplitter)                           | <span data-ttu-id="05294-128">Fazer downgrade da taxa de quadros em um fluxo de vídeo digital (DV)</span><span class="sxs-lookup"><span data-stu-id="05294-128">Downgrade the frame rate on a digital video (DV) stream</span></span>                                                      |
| [<span data-ttu-id="05294-129">**IIPDVDec**</span><span class="sxs-lookup"><span data-stu-id="05294-129">**IIPDVDec**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iipdvdec)                                 | <span data-ttu-id="05294-130">Defina a resolução de decodificação no filtro do [decodificador de vídeo DV](dv-video-decoder-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="05294-130">Set the decoding resolution on the [DV Video Decoder](dv-video-decoder-filter.md) filter.</span></span>                   |
| [<span data-ttu-id="05294-131">**IPersistMediaPropertyBag**</span><span class="sxs-lookup"><span data-stu-id="05294-131">**IPersistMediaPropertyBag**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag) | <span data-ttu-id="05294-132">Definir e recuperar informações e partes de DISP em fluxos AVI.</span><span class="sxs-lookup"><span data-stu-id="05294-132">Set and retrieve INFO and DISP chunks in AVI streams.</span></span>                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="05294-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="05294-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05294-134">Interfaces</span><span class="sxs-lookup"><span data-stu-id="05294-134">Interfaces</span></span>](interfaces.md)
</dt> </dl>

 

 



