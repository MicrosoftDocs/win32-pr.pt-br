---
description: Este tópico descreve como trabalhar com perfis ASF no Microsoft Media Foundation.
ms.assetid: 03a0981b-29c3-450d-aa58-bc56a76e6cb6
title: Perfil ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616670e7de68fd73c168c474544fc6236f1586e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501202"
---
# <a name="asf-profile"></a><span data-ttu-id="ecc0d-103">Perfil ASF</span><span class="sxs-lookup"><span data-stu-id="ecc0d-103">ASF Profile</span></span>

<span data-ttu-id="ecc0d-104">Este tópico descreve como trabalhar com perfis ASF no Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="ecc0d-104">This topic describes how to work with ASF profiles in Microsoft Media Foundation.</span></span>

<span data-ttu-id="ecc0d-105">Um arquivo ASF (Advanced Systems Format) contém um ou mais fluxos.</span><span class="sxs-lookup"><span data-stu-id="ecc0d-105">An Advanced Systems Format (ASF) file contains one or more streams.</span></span> <span data-ttu-id="ecc0d-106">Para cada fluxo, o cabeçalho ASF contém um cabeçalho de propriedades de fluxo que descreve o fluxo.</span><span class="sxs-lookup"><span data-stu-id="ecc0d-106">For each stream, the ASF header contains a Stream Properties Header that describes the stream.</span></span> <span data-ttu-id="ecc0d-107">Na camada [WMContainer](wmcontainer-asf-components.md) , os seguintes objetos são usados para definir ou ler as propriedades dos fluxos ASF:</span><span class="sxs-lookup"><span data-stu-id="ecc0d-107">At the [WMContainer](wmcontainer-asf-components.md) layer, the following objects are used to set or read the properties of the ASF streams:</span></span>

-   <span data-ttu-id="ecc0d-108">Objeto de *perfil ASF* : descreve os fluxos e suas relações entre si.</span><span class="sxs-lookup"><span data-stu-id="ecc0d-108">*ASF profile* object: Describes the streams and their relationships with each other.</span></span> <span data-ttu-id="ecc0d-109">O objeto de perfil ASF expõe a interface [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) .</span><span class="sxs-lookup"><span data-stu-id="ecc0d-109">The ASF profile object exposes the [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface.</span></span>
-   <span data-ttu-id="ecc0d-110">Objeto de *configuração de fluxo* : descreve um fluxo.</span><span class="sxs-lookup"><span data-stu-id="ecc0d-110">*Stream configuration* object: Describes one stream.</span></span> <span data-ttu-id="ecc0d-111">O objeto de configuração de fluxo contém um tipo de mídia que descreve o formato do fluxo.</span><span class="sxs-lookup"><span data-stu-id="ecc0d-111">The stream configuration object contains a media type that describes the format of the stream.</span></span> <span data-ttu-id="ecc0d-112">Para fluxos de áudio e vídeo, o tipo de mídia descreve exatamente como o fluxo é configurado e é usado por codecs que codificam ou decodificam o fluxo.</span><span class="sxs-lookup"><span data-stu-id="ecc0d-112">For audio and video streams, the media type describes exactly how the stream is configured, and is used by codecs that encode or decode the stream.</span></span> <span data-ttu-id="ecc0d-113">O objeto de configuração de fluxo expõe a interface [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .</span><span class="sxs-lookup"><span data-stu-id="ecc0d-113">The stream configuration object exposes the [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface.</span></span> <span data-ttu-id="ecc0d-114">Um perfil ASF válido contém pelo menos um objeto de configuração de fluxo.</span><span class="sxs-lookup"><span data-stu-id="ecc0d-114">A valid ASF profile contains at least one stream configuration object.</span></span>
-   <span data-ttu-id="ecc0d-115">Objeto de *exclusão mútua* : descreve vários fluxos que não devem ser lidos simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="ecc0d-115">*Mutual exclusion* object: Describes multiple streams that are not intended be read concurrently.</span></span> <span data-ttu-id="ecc0d-116">Um objeto de exclusão mútua expõe a interface [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion) .</span><span class="sxs-lookup"><span data-stu-id="ecc0d-116">A mutual exclusion object exposes the [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion) interface.</span></span> <span data-ttu-id="ecc0d-117">Um perfil ASF contém zero ou mais objetos de exclusão mútua.</span><span class="sxs-lookup"><span data-stu-id="ecc0d-117">An ASF profile contains zero or more mutual exclusion objects.</span></span>

<span data-ttu-id="ecc0d-118">O diagrama a seguir mostra a relação entre o perfil ASF e os objetos contidos no perfil.</span><span class="sxs-lookup"><span data-stu-id="ecc0d-118">The following diagram shows the relationship between the ASF profile and the objects that are contained in the profile.</span></span>

![diagrama de árvore de um nó de perfil ASF com nós filho de configuração de fluxo; o primeiro aponta para o tipo de mídia, os próximos dois para a exclusão mútua](images/asf-components02.png)

<span data-ttu-id="ecc0d-120">Para reprodução, o perfil ASF é usado para enumerar os fluxos e localizar os formatos de fluxo.</span><span class="sxs-lookup"><span data-stu-id="ecc0d-120">For playback, the ASF profile is used to enumerate the streams and find the stream formats.</span></span> <span data-ttu-id="ecc0d-121">Para codificação, o perfil ASF é usado para configurar os fluxos no arquivo de destino.</span><span class="sxs-lookup"><span data-stu-id="ecc0d-121">For encoding, the ASF profile is used to configure the streams in the destination file.</span></span>

<span data-ttu-id="ecc0d-122">O perfil ASF também é usado para configurar o [coletor de mídia ASF](asf-media-sinks.md).</span><span class="sxs-lookup"><span data-stu-id="ecc0d-122">The ASF profile is also used to configure the [ASF Media Sink](asf-media-sinks.md).</span></span> <span data-ttu-id="ecc0d-123">Para cada fluxo no perfil ASF, o coletor de mídia ASF cria um coletor de fluxo correspondente.</span><span class="sxs-lookup"><span data-stu-id="ecc0d-123">For each stream in the ASF profile, the ASF media sink creates a corresponding stream sink.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ecc0d-124">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="ecc0d-124">In this section</span></span>



| <span data-ttu-id="ecc0d-125">Tópico</span><span class="sxs-lookup"><span data-stu-id="ecc0d-125">Topic</span></span>                                                                                           | <span data-ttu-id="ecc0d-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="ecc0d-126">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="ecc0d-127">Criando um perfil ASF</span><span class="sxs-lookup"><span data-stu-id="ecc0d-127">Creating an ASF Profile</span></span>](creating-an-asf-profile.md)<br/>                               | <span data-ttu-id="ecc0d-128">Descreve como criar um objeto de perfil ASF.</span><span class="sxs-lookup"><span data-stu-id="ecc0d-128">Describes how to create an ASF profile object.</span></span><br/>          |
| [<span data-ttu-id="ecc0d-129">Criando e configurando fluxos ASF</span><span class="sxs-lookup"><span data-stu-id="ecc0d-129">Creating and Configuring ASF Streams</span></span>](creating-and-configuring-asf-streams.md)<br/>     | <span data-ttu-id="ecc0d-130">Descreve como adicionar fluxos a um perfil ASF.</span><span class="sxs-lookup"><span data-stu-id="ecc0d-130">Describes how to add streams to an ASF profile.</span></span><br/>         |
| [<span data-ttu-id="ecc0d-131">Usando a exclusão mútua para fluxos ASF</span><span class="sxs-lookup"><span data-stu-id="ecc0d-131">Using Mutual Exclusion for ASF Streams</span></span>](using-mutual-exclusion-for-asf-streams.md)<br/> | <span data-ttu-id="ecc0d-132">Descreve como adicionar exclusões mútuas a fluxos ASF.</span><span class="sxs-lookup"><span data-stu-id="ecc0d-132">Describes how to add mutual exclusions to ASF streams.</span></span> <br/> |



 

## <a name="related-topics"></a><span data-ttu-id="ecc0d-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ecc0d-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ecc0d-134">Tipos de mídia</span><span class="sxs-lookup"><span data-stu-id="ecc0d-134">Media Types</span></span>](media-types.md)
</dt> <dt>

[<span data-ttu-id="ecc0d-135">Tutorial: 1-transmitir codificação de mídia do Windows</span><span class="sxs-lookup"><span data-stu-id="ecc0d-135">Tutorial: 1-Pass Windows Media Encoding</span></span>](tutorial--1-pass-windows-media-encoding.md)
</dt> <dt>

[<span data-ttu-id="ecc0d-136">Tutorial: gravando um arquivo WMA usando a codificação de CBR</span><span class="sxs-lookup"><span data-stu-id="ecc0d-136">Tutorial: Writing a WMA File by Using CBR Encoding</span></span>](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> <dt>

[<span data-ttu-id="ecc0d-137">Componentes ASF WMContainer</span><span class="sxs-lookup"><span data-stu-id="ecc0d-137">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> </dl>

 

 




