---
description: Atributos do descritor de fluxo
ms.assetid: 1364d7c5-67e8-49b6-8038-d6d4ea03fb7d
title: Atributos do descritor de fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc7b49b8da74bacc84151148047ccdeaffc364a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647735"
---
# <a name="stream-descriptor-attributes"></a><span data-ttu-id="0b0f9-103">Atributos do descritor de fluxo</span><span class="sxs-lookup"><span data-stu-id="0b0f9-103">Stream Descriptor Attributes</span></span>

## <a name="common-stream-descriptor-attributes"></a><span data-ttu-id="0b0f9-104">Atributos comuns de descritor de fluxo</span><span class="sxs-lookup"><span data-stu-id="0b0f9-104">Common Stream Descriptor Attributes</span></span>

<span data-ttu-id="0b0f9-105">Os atributos a seguir se aplicam aos descritores de fluxo.</span><span class="sxs-lookup"><span data-stu-id="0b0f9-105">The following attributes apply to stream descriptors.</span></span>



| <span data-ttu-id="0b0f9-106">Atributo</span><span class="sxs-lookup"><span data-stu-id="0b0f9-106">Attribute</span></span>                                                   | <span data-ttu-id="0b0f9-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0b0f9-107">Description</span></span>                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b0f9-108">**\_linguagem SD \_ MF**</span><span class="sxs-lookup"><span data-stu-id="0b0f9-108">**MF\_SD\_LANGUAGE**</span></span>](mf-sd-language-attribute.md)        | <span data-ttu-id="0b0f9-109">Especifica o idioma de um fluxo.</span><span class="sxs-lookup"><span data-stu-id="0b0f9-109">Specifies the language for a stream.</span></span>                                                  |
| [<span data-ttu-id="0b0f9-110">MF \_ SD \_ mutuamente \_ exclusivo</span><span class="sxs-lookup"><span data-stu-id="0b0f9-110">MF\_SD\_MUTUALLY\_EXCLUSIVE</span></span>](mf-sd-mutually-exclusive.md) | <span data-ttu-id="0b0f9-111">Especifica se um fluxo é mutuamente exclusivo com outros fluxos do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="0b0f9-111">Specifies whether a stream is mutually exclusive with other streams of the same type.</span></span> |
| [<span data-ttu-id="0b0f9-112">**MF \_ SD \_ protegido**</span><span class="sxs-lookup"><span data-stu-id="0b0f9-112">**MF\_SD\_PROTECTED**</span></span>](mf-sd-protected-attribute.md)      | <span data-ttu-id="0b0f9-113">Especifica se um fluxo contém conteúdo protegido.</span><span class="sxs-lookup"><span data-stu-id="0b0f9-113">Specifies whether a stream contains protected content.</span></span>                                |
| [<span data-ttu-id="0b0f9-114">\_nome do \_ fluxo \_ SD MF</span><span class="sxs-lookup"><span data-stu-id="0b0f9-114">MF\_SD\_STREAM\_NAME</span></span>](mf-sd-stream-name.md)               | <span data-ttu-id="0b0f9-115">Contém o nome de um fluxo.</span><span class="sxs-lookup"><span data-stu-id="0b0f9-115">Contains the name of a stream.</span></span>                                                        |



 

## <a name="asf-specific-stream-descriptor-attributes"></a><span data-ttu-id="0b0f9-116">ASF-Specific atributos de descritor de fluxo</span><span class="sxs-lookup"><span data-stu-id="0b0f9-116">ASF-Specific Stream Descriptor Attributes</span></span>

<span data-ttu-id="0b0f9-117">Os atributos a seguir se aplicam a descritores de fluxo para arquivos ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="0b0f9-117">The following attributes apply to stream descriptors for Advanced Systems Format (ASF) files.</span></span>



| <span data-ttu-id="0b0f9-118">Atributo</span><span class="sxs-lookup"><span data-stu-id="0b0f9-118">Attribute</span></span>                                                                                                                | <span data-ttu-id="0b0f9-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="0b0f9-119">Description</span></span>                                                                                |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b0f9-120">**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ média \_ BUFFERSIZE**</span><span class="sxs-lookup"><span data-stu-id="0b0f9-120">**MF\_SD\_ASF\_EXTSTRMPROP\_AVG\_BUFFERSIZE**</span></span>](mf-sd-asf-extstrmprop-avg-buffersize-attribute.md)                      | <span data-ttu-id="0b0f9-121">Especifica o tamanho médio do buffer necessário para um fluxo em um arquivo ASF, em bytes.</span><span class="sxs-lookup"><span data-stu-id="0b0f9-121">Specifies the average buffer size needed for a stream in an ASF file, in bytes.</span></span>            |
| [<span data-ttu-id="0b0f9-122">**\_taxa de \_ \_ \_ bits média de \_ dados \_ do MF SD EXTSTRMPROP**</span><span class="sxs-lookup"><span data-stu-id="0b0f9-122">**MF\_SD\_ASF\_EXTSTRMPROP\_AVG\_DATA\_BITRATE**</span></span>](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)                 | <span data-ttu-id="0b0f9-123">Especifica a taxa média de bits de dados de um fluxo em um arquivo ASF, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="0b0f9-123">Specifies the average data bit rate of a stream in an ASF file, in bits per second.</span></span>        |
| [<span data-ttu-id="0b0f9-124">**índice de ID de idioma do MF \_ SD \_ ASF \_ EXTSTRMPROP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0b0f9-124">**MF\_SD\_ASF\_EXTSTRMPROP\_LANGUAGE\_ID\_INDEX**</span></span>](mf-sd-asf-extstrmprop-language-id-index-attribute.md)               | <span data-ttu-id="0b0f9-125">Especifica o idioma usado por um fluxo em um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="0b0f9-125">Specifies the language used by a stream in an ASF file.</span></span>                                    |
| [<span data-ttu-id="0b0f9-126">**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ Max \_ BUFFERSIZE**</span><span class="sxs-lookup"><span data-stu-id="0b0f9-126">**MF\_SD\_ASF\_EXTSTRMPROP\_MAX\_BUFFERSIZE**</span></span>](mf-sd-asf-extstrmprop-max-buffersize-attribute.md)                      | <span data-ttu-id="0b0f9-127">Especifica o tamanho máximo de buffer necessário para um fluxo em um arquivo ASF, em bytes.</span><span class="sxs-lookup"><span data-stu-id="0b0f9-127">Specifies the maximum buffer size needed for a stream in an ASF file, in bytes.</span></span>            |
| [<span data-ttu-id="0b0f9-128">**\_taxa de \_ \_ \_ bits máxima de \_ dados EXTSTRMPROP \_ MF SD**</span><span class="sxs-lookup"><span data-stu-id="0b0f9-128">**MF\_SD\_ASF\_EXTSTRMPROP\_MAX\_DATA\_BITRATE**</span></span>](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)                 | <span data-ttu-id="0b0f9-129">Especifica a taxa máxima de bits de dados de um fluxo em um arquivo ASF, em bits por segundo</span><span class="sxs-lookup"><span data-stu-id="0b0f9-129">Specifies the maximum data bit rate of a stream in an ASF file, in bits per second</span></span>         |
| [<span data-ttu-id="0b0f9-130">**\_modelo de \_ \_ conformidade do dispositivo de metadados do ASF \_ SD \_ MF \_**</span><span class="sxs-lookup"><span data-stu-id="0b0f9-130">**MF\_SD\_ASF\_METADATA\_DEVICE\_CONFORMANCE\_TEMPLATE**</span></span>](mf-sd-asf-metadata-device-conformance-template-attribute.md) | <span data-ttu-id="0b0f9-131">Especifica o modelo de conformidade do dispositivo para um fluxo em um arquivo ASF, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="0b0f9-131">Specifies the device conformance template for a stream in an ASF file, in bits per second.</span></span> |
| [<span data-ttu-id="0b0f9-132">**\_taxa de \_ \_ bits STREAMBITRATES do ASF SD \_**</span><span class="sxs-lookup"><span data-stu-id="0b0f9-132">**MF\_SD\_ASF\_STREAMBITRATES\_BITRATE**</span></span>](mf-sd-asf-streambitrates-bitrate-attribute.md)                               | <span data-ttu-id="0b0f9-133">Especifica a taxa média de bits de um fluxo em um arquivo ASF, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="0b0f9-133">Specifies the average bit rate of a stream in an ASF file, in bits per second.</span></span>             |



 

## <a name="sami-media-source-stream-descriptor-attributes"></a><span data-ttu-id="0b0f9-134">Atributos do descritor de fluxo de origem de mídia SAMI</span><span class="sxs-lookup"><span data-stu-id="0b0f9-134">SAMI Media Source Stream Descriptor Attributes</span></span>

<span data-ttu-id="0b0f9-135">O atributo a seguir aplica-se ao descritor de fluxo para a origem de mídia SAMI.</span><span class="sxs-lookup"><span data-stu-id="0b0f9-135">The following attribute applies to the stream descriptor for the SAMI media source.</span></span>



| <span data-ttu-id="0b0f9-136">Atributo</span><span class="sxs-lookup"><span data-stu-id="0b0f9-136">Attribute</span></span>                                                       | <span data-ttu-id="0b0f9-137">Descrição</span><span class="sxs-lookup"><span data-stu-id="0b0f9-137">Description</span></span>                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b0f9-138">**\_linguagem de \_ Sami \_ SD MF**</span><span class="sxs-lookup"><span data-stu-id="0b0f9-138">**MF\_SD\_SAMI\_LANGUAGE**</span></span>](mf-sd-sami-language-attribute.md) | <span data-ttu-id="0b0f9-139">Contém o nome do idioma de intercâmbio de mídia acessível (SAMI) que é definido para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="0b0f9-139">Contains the Synchronized Accessible Media Interchange (SAMI) language name that is defined for the stream.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0b0f9-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0b0f9-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b0f9-141">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="0b0f9-141">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="0b0f9-142">Atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0b0f9-142">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 



