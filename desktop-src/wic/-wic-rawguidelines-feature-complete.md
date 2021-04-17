---
description: 'Integridade do recurso: interfaces recomendadas'
ms.assetid: 759bf253-7450-4895-a550-9f81f3498f79
title: 'Integridade do recurso: interfaces recomendadas'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1dba4bcc029b2205985afb443526376c0eecb16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813311"
---
# <a name="feature-completeness-recommended-interfaces"></a><span data-ttu-id="b3eb8-103">Integridade do recurso: interfaces recomendadas</span><span class="sxs-lookup"><span data-stu-id="b3eb8-103">Feature Completeness: Recommended Interfaces</span></span>

<span data-ttu-id="b3eb8-104">A tabela a seguir lista os codecs BRUTOs de interfaces do Windows Imaging Component (WIC) que devem ser implementados.</span><span class="sxs-lookup"><span data-stu-id="b3eb8-104">The following table lists the Windows Imaging Component (WIC) interfaces RAW codecs should implement.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b3eb8-105">Interface</span><span class="sxs-lookup"><span data-stu-id="b3eb8-105">Interface</span></span></th>
<th><span data-ttu-id="b3eb8-106">Obrigatório para</span><span class="sxs-lookup"><span data-stu-id="b3eb8-106">Required for</span></span></th>
<th><span data-ttu-id="b3eb8-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="b3eb8-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b3eb8-108"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3eb8-108"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a></span></span></td>
<td><span data-ttu-id="b3eb8-109">Decodificadores</span><span class="sxs-lookup"><span data-stu-id="b3eb8-109">Decoders</span></span></td>
<td><span data-ttu-id="b3eb8-110">Representa o ponto de partida para a decodificação de um arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="b3eb8-110">Represents the starting point for decoding an image file.</span></span> <span data-ttu-id="b3eb8-111">Fornece acesso a propriedades de nível de contêiner como miniaturas, quadros e paleta.</span><span class="sxs-lookup"><span data-stu-id="b3eb8-111">Provides access to container-level properties like thumbnails, frames, and palette.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3eb8-112"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3eb8-112"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a></span></span></td>
<td><span data-ttu-id="b3eb8-113">Decodificadores</span><span class="sxs-lookup"><span data-stu-id="b3eb8-113">Decoders</span></span></td>
<td><span data-ttu-id="b3eb8-114">Representa um quadro de imagem específico dentro do contêiner que fornece acesso a propriedades em nível de quadro.</span><span class="sxs-lookup"><span data-stu-id="b3eb8-114">Represents a specific image frame within the container that provides access to frame-level properties.</span></span> <span data-ttu-id="b3eb8-115">Essa é a interface que decodifica os bits de imagem reais.</span><span class="sxs-lookup"><span data-stu-id="b3eb8-115">This is the interface that decodes the actual image bits.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3eb8-116"><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3eb8-116"><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a></span></span></td>
<td><span data-ttu-id="b3eb8-117">Decodificadores</span><span class="sxs-lookup"><span data-stu-id="b3eb8-117">Decoders</span></span></td>
<td><span data-ttu-id="b3eb8-118">Necessário para enumerar e iterar por meio de blocos de metadados e invocar os leitores de metadados apropriados ao ler de um arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="b3eb8-118">Required for enumerating and iterating through metadata blocks and invoking the appropriate metadata readers when reading from an image file.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b3eb8-119">Se o formato de contêiner bruto for compatível com TIFF ou usar IFDs ou IRBs padrão para armazenar metadados EXIF ou XMP, os autores de codec poderão optar por invocar os leitores de metadados internos em vez de escrever seus próprios.</span><span class="sxs-lookup"><span data-stu-id="b3eb8-119">If the RAW container format is TIFF compatible or uses standard IFDs or IRBs to store EXIF or XMP metadata, codec authors can choose to invoke the built-in metadata readers rather than writing their own.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3eb8-120"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform"><strong>IWICBitmapSourceTransform</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3eb8-120"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform"><strong>IWICBitmapSourceTransform</strong></a></span></span></td>
<td><span data-ttu-id="b3eb8-121">Decodificadores</span><span class="sxs-lookup"><span data-stu-id="b3eb8-121">Decoders</span></span></td>
<td><span data-ttu-id="b3eb8-122">Permite que o chamador especifique o formato de escala, corte, rotação ou pixel desejado para a imagem decodificada, o que pode melhorar significativamente o desempenho do decodificador.</span><span class="sxs-lookup"><span data-stu-id="b3eb8-122">Allows the caller to specify desired scaling, cropping, rotation, or pixel format for the decoded image, which can significantly improve decoder performance.</span></span> <span data-ttu-id="b3eb8-123">Por exemplo, os decodificadores de JPEG e WDP (protocolo de datagrama sem fio) da Microsoft usam um esquema de otimização de pirâmide para obter uma decodificação mais rápida quando o bitmap de destino é menor do que o bitmap de origem.</span><span class="sxs-lookup"><span data-stu-id="b3eb8-123">For example, Microsoft's JPEG and Wireless Datagram Protocol (WDP) decoders use a pyramid optimization scheme to achieve faster decoding when the target bitmap is smaller than the source bitmap.</span></span> <span data-ttu-id="b3eb8-124">O Windows Vista (e posterior) tentará usar essa interface para extrair uma &quot; &quot; visualização rápida de uma imagem bruta sempre que a visualização inserida estiver faltando ou tiver menos de 1.024 pixels em sua dimensão maior.</span><span class="sxs-lookup"><span data-stu-id="b3eb8-124">Windows Vista (and later) will attempt to use this interface to extract a &quot;fast&quot; preview from a RAW image whenever the embedded preview is missing or less than 1,024 pixels in its largest dimension.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3eb8-125"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw"><strong>IWICDevelopRaw</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3eb8-125"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw"><strong>IWICDevelopRaw</strong></a></span></span></td>
<td><span data-ttu-id="b3eb8-126">Decodificadores</span><span class="sxs-lookup"><span data-stu-id="b3eb8-126">Decoders</span></span></td>
<td><span data-ttu-id="b3eb8-127">Necessário para formatos BRUTOs.</span><span class="sxs-lookup"><span data-stu-id="b3eb8-127">Required for RAW formats.</span></span> <span data-ttu-id="b3eb8-128">Expõe parâmetros que são específicos do processamento de imagem bruto.</span><span class="sxs-lookup"><span data-stu-id="b3eb8-128">Exposes parameters that are specific to RAW image processing.</span></span> <span data-ttu-id="b3eb8-129">Os codecs BRUTOs devem dar suporte a quantos desses parâmetros forem aplicados ao codec.</span><span class="sxs-lookup"><span data-stu-id="b3eb8-129">RAW codecs should support as many of these parameters as apply to the codec.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3eb8-130"><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3eb8-130"><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a></span></span></td>
<td><span data-ttu-id="b3eb8-131">Codificadores</span><span class="sxs-lookup"><span data-stu-id="b3eb8-131">Encoders</span></span></td>
<td><span data-ttu-id="b3eb8-132">Representa o ponto de partida para codificar um arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="b3eb8-132">Represents the starting point for encoding an image file.</span></span> <span data-ttu-id="b3eb8-133">Essa interface é usada para definir propriedades em nível de contêiner, como miniaturas, quadros e paleta.</span><span class="sxs-lookup"><span data-stu-id="b3eb8-133">This interface is used for setting container-level properties, such as thumbnails, frames, and palette.</span></span> <span data-ttu-id="b3eb8-134">Também é necessário invocar um gravador de metadados para habilitar a persistência de metadados para o arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="b3eb8-134">It is also required to invoke a metadata writer to enable metadata persistence to the image file.</span></span> <span data-ttu-id="b3eb8-135">Por esses motivos, essa interface é necessária mesmo que a codificação do bitmap primário para o formato bruto não seja suportada.</span><span class="sxs-lookup"><span data-stu-id="b3eb8-135">For these reasons, this interface is necessary even if encoding the primary bitmap to the RAW format is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3eb8-136"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3eb8-136"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a></span></span></td>
<td><span data-ttu-id="b3eb8-137">Codificadores</span><span class="sxs-lookup"><span data-stu-id="b3eb8-137">Encoders</span></span></td>
<td><span data-ttu-id="b3eb8-138">Representa um quadro de imagem específico dentro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="b3eb8-138">Represents a specific image frame within the container.</span></span> <span data-ttu-id="b3eb8-139">Essa interface é usada para codificar os bits de imagem reais e para definir as propriedades e os metadados por quadro.</span><span class="sxs-lookup"><span data-stu-id="b3eb8-139">This interface is used to encode the actual image bits and to set per-frame metadata and properties.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3eb8-140"><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3eb8-140"><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a></span></span></td>
<td><span data-ttu-id="b3eb8-141">Codificadores</span><span class="sxs-lookup"><span data-stu-id="b3eb8-141">Encoders</span></span></td>
<td><span data-ttu-id="b3eb8-142">Necessário para iterar por meio de blocos de metadados e invocar os gravadores de metadados apropriados ao serializar um arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="b3eb8-142">Required for iterating through metadata blocks and invoking the appropriate metadata writers when serializing an image file.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b3eb8-143">Se o formato de contêiner bruto for compatível com TIFF, os autores de codec poderão optar por invocar os gravadores de metadados internos em vez de escrever seus próprios.</span><span class="sxs-lookup"><span data-stu-id="b3eb8-143">If the RAW container format is TIFF-compatible, codec authors can choose to invoke the built-in metadata writers rather than writing their own.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="b3eb8-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b3eb8-144">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b3eb8-145">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="b3eb8-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b3eb8-146">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="b3eb8-146">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="b3eb8-147">Diretrizes do WIC para formatos de imagem bruta de câmera</span><span class="sxs-lookup"><span data-stu-id="b3eb8-147">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="b3eb8-148">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="b3eb8-148">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 




