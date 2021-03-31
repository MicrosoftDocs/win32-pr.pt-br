---
description: Esta seção descreve como usar a API de transcodificação para codificar novamente os arquivos de mídia. A API de transcodificação foi introduzida no Windows 7.
ms.assetid: 24bf68a8-39bf-4302-b28c-71bb23b63469
title: API de transcodificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9783c6f99a25ba6835171dcc7f7555a1f747c72b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827801"
---
# <a name="transcode-api"></a><span data-ttu-id="5795c-104">API de transcodificação</span><span class="sxs-lookup"><span data-stu-id="5795c-104">Transcode API</span></span>

<span data-ttu-id="5795c-105">Esta seção descreve como usar a API de transcodificação para codificar novamente os arquivos de mídia.</span><span class="sxs-lookup"><span data-stu-id="5795c-105">This section describes how to use the transcode API to re-encode media files.</span></span> <span data-ttu-id="5795c-106">A API de transcodificação foi introduzida no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5795c-106">The transcode API was introduced in Windows 7.</span></span>

<span data-ttu-id="5795c-107">*Transcodificação* é a conversão de um arquivo de mídia digital de um formato para outro.</span><span class="sxs-lookup"><span data-stu-id="5795c-107">*Transcoding* is the conversion of a digital media file from one format to another.</span></span> <span data-ttu-id="5795c-108">A API de transcodificação foi projetada para ser usada com a [sessão de mídia](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="5795c-108">The transcode API is designed to be used with the [Media Session](media-session.md).</span></span> <span data-ttu-id="5795c-109">Ele simplifica o uso da sessão de mídia para determinados tipos de aplicativos de transcodificação:</span><span class="sxs-lookup"><span data-stu-id="5795c-109">It simplifies the use of the Media Session for certain types of transcoding applications:</span></span>

-   <span data-ttu-id="5795c-110">Codificação de taxa de bits constante (CBR), em que a taxa de bits de destino é conhecida com antecedência.</span><span class="sxs-lookup"><span data-stu-id="5795c-110">Constant bit rate (CBR) encoding, where the target bit rate is known in advance.</span></span>
-   <span data-ttu-id="5795c-111">No máximo um fluxo de áudio e um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5795c-111">At most one audio stream and one video stream.</span></span>
-   <span data-ttu-id="5795c-112">Codificação de e para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="5795c-112">Encoding from and to a file.</span></span>

<span data-ttu-id="5795c-113">A API de transcodificação não oferece suporte ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="5795c-113">Transcode API does not support the following:</span></span>

-   <span data-ttu-id="5795c-114">Taxa de bits variável (VBR) ou codificação de passagem múltipla.</span><span class="sxs-lookup"><span data-stu-id="5795c-114">Variable bit rate (VBR) or multi-pass encoding.</span></span>
-   <span data-ttu-id="5795c-115">Vários fluxos de áudio ou vários fluxos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5795c-115">Multiple audio streams or multiple video streams.</span></span>
-   <span data-ttu-id="5795c-116">Conteúdo protegido por DRM diferente dos arquivos ASF protegidos com WMDRM.</span><span class="sxs-lookup"><span data-stu-id="5795c-116">DRM-protected content other than ASF files protected with WMDRM.</span></span>
-   <span data-ttu-id="5795c-117">Transmissão ao vivo, como streaming de Live-to-file ou Live-to-Live streaming.</span><span class="sxs-lookup"><span data-stu-id="5795c-117">Live streaming, such as live-to-file streaming or live-to-live streaming.</span></span>

<span data-ttu-id="5795c-118">Se o aplicativo de codificação se ajustar a essas restrições, a API transcodificará um modelo de programação mais simples do que usar a sessão de mídia sozinha.</span><span class="sxs-lookup"><span data-stu-id="5795c-118">If your encoding application fits within these constraints, the transcode API a simpler programming model than using the Media Session alone.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5795c-119">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="5795c-119">In this section</span></span>



| <span data-ttu-id="5795c-120">Tópico</span><span class="sxs-lookup"><span data-stu-id="5795c-120">Topic</span></span>                                                                                          | <span data-ttu-id="5795c-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="5795c-121">Description</span></span>                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5795c-122">Sobre a API de transcodificação</span><span class="sxs-lookup"><span data-stu-id="5795c-122">About the Transcode API</span></span>](about-the-transcode-api.md)<br/>                              | <span data-ttu-id="5795c-123">Fornece uma visão geral da API de transcodificação.</span><span class="sxs-lookup"><span data-stu-id="5795c-123">Provides a general overview of the transcode API.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="5795c-124">Usando a API de transcodificação</span><span class="sxs-lookup"><span data-stu-id="5795c-124">Using the Transcode API</span></span>](fast-transcode-objects.md)<br/>                               | <span data-ttu-id="5795c-125">Descreve como um aplicativo usa a API de transcodificação.</span><span class="sxs-lookup"><span data-stu-id="5795c-125">Describes how an application uses the transcode API.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="5795c-126">Tutorial: codificando um arquivo MP4</span><span class="sxs-lookup"><span data-stu-id="5795c-126">Tutorial: Encoding an MP4 File</span></span>](tutorial--encoding-an-mp4-file-.md)<br/>               | <span data-ttu-id="5795c-127">Um tutorial passo a passo que mostra como usar a API de transcodificação para codificar um arquivo MP4.</span><span class="sxs-lookup"><span data-stu-id="5795c-127">A step-by-step tutorial that shows how to use the transcode API to encode an MP4 file.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="5795c-128">Tutorial: codificando um arquivo WMA</span><span class="sxs-lookup"><span data-stu-id="5795c-128">Tutorial: Encoding a WMA File</span></span>](tutorial--converting-an-mp3-file-to-a-wma-file.md)<br/> | <span data-ttu-id="5795c-129">Mostra como usar a API de transcodificação para codificar um arquivo WMA.</span><span class="sxs-lookup"><span data-stu-id="5795c-129">Shows how to use the transcode API to encode a WMA file.</span></span> <span data-ttu-id="5795c-130">Este tutorial modifica o código mostrado no [tutorial: codificando um arquivo MP4](tutorial--encoding-an-mp4-file-.md), portanto, você deve ler o tutorial primeiro.</span><span class="sxs-lookup"><span data-stu-id="5795c-130">This tutorial modifies the code shown in [Tutorial: Encoding an MP4 File](tutorial--encoding-an-mp4-file-.md), so you should read that tutorial first.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="5795c-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5795c-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5795c-132">Codificando e criando arquivos</span><span class="sxs-lookup"><span data-stu-id="5795c-132">Encoding and File Authoring</span></span>](encoding-and-file-authoring.md)
</dt> <dt>

[<span data-ttu-id="5795c-133">Media Foundation: conceitos essenciais</span><span class="sxs-lookup"><span data-stu-id="5795c-133">Media Foundation: Essential Concepts</span></span>](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[<span data-ttu-id="5795c-134">Visão geral da codificação no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5795c-134">Overview of Encoding in Media Foundation</span></span>](overview-of-encoding-in-media-foundation.md)
</dt> </dl>

 

 




