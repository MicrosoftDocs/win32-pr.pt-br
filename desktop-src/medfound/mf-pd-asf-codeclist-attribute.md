---
description: Contém informações sobre os codecs e formatos que foram usados para codificar o conteúdo em um arquivo ASF (Advanced Systems Format). Esse atributo corresponde ao objeto de lista de codecs no cabeçalho ASF, definido na especificação ASF.
ms.assetid: 6dde30d3-dbdc-469c-ad7e-5e670b7e0a64
title: Atributo MF_PD_ASF_CODECLIST (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 402c53c082ae57fed444168c559f99718322f8a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763915"
---
# <a name="mf_pd_asf_codeclist-attribute"></a><span data-ttu-id="08e17-104">\_Atributo de codec MF PD \_ asflist \_</span><span class="sxs-lookup"><span data-stu-id="08e17-104">MF\_PD\_ASF\_CODECLIST attribute</span></span>

<span data-ttu-id="08e17-105">Contém informações sobre os codecs e formatos que foram usados para codificar o conteúdo em um arquivo ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="08e17-105">Contains information about the codecs and formats that were used to encode the content in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="08e17-106">Esse atributo corresponde ao objeto de lista de codecs no cabeçalho ASF, definido na especificação ASF.</span><span class="sxs-lookup"><span data-stu-id="08e17-106">This attribute corresponds to the Codec List Object in the ASF header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="08e17-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="08e17-107">Data type</span></span>

<span data-ttu-id="08e17-108">Matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="08e17-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="08e17-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="08e17-109">Remarks</span></span>

<span data-ttu-id="08e17-110">Esse atributo se aplica a descritores de apresentação para conteúdo ASF.</span><span class="sxs-lookup"><span data-stu-id="08e17-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="08e17-111">O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) cria o descritor de apresentação e gera esse atributo a partir do objeto de lista de codec no cabeçalho ASF.</span><span class="sxs-lookup"><span data-stu-id="08e17-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method creates the presentation descriptor and generates this attribute from the Codec List Object in the ASF header.</span></span> <span data-ttu-id="08e17-112">Um aplicativo que usa a [fonte de mídia ASF](asf-media-source.md) pode obter esse atributo chamando [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) e obtendo o atributo do descritor de apresentação.</span><span class="sxs-lookup"><span data-stu-id="08e17-112">An application that uses the [ASF Media Source](asf-media-source.md) can get this attribute by calling [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) and then getting the attribute from the presentation descriptor.</span></span>

<span data-ttu-id="08e17-113">A tabela a seguir mostra o layout do blob de atributo.</span><span class="sxs-lookup"><span data-stu-id="08e17-113">The following table shows the layout of the attribute blob.</span></span>



| <span data-ttu-id="08e17-114">Campo de objeto da lista de codecs</span><span class="sxs-lookup"><span data-stu-id="08e17-114">Codec List Object field</span></span> | <span data-ttu-id="08e17-115">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="08e17-115">Data type</span></span>    | <span data-ttu-id="08e17-116">Tamanho</span><span class="sxs-lookup"><span data-stu-id="08e17-116">Size</span></span>    | <span data-ttu-id="08e17-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="08e17-117">Description</span></span>                           |
|-------------------------|--------------|---------|---------------------------------------|
| <span data-ttu-id="08e17-118">Contagem de entradas de codec</span><span class="sxs-lookup"><span data-stu-id="08e17-118">Codec Entries Count</span></span>     | <span data-ttu-id="08e17-119">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="08e17-119">**DWORD**</span></span>    | <span data-ttu-id="08e17-120">4 bytes</span><span class="sxs-lookup"><span data-stu-id="08e17-120">4 bytes</span></span> | <span data-ttu-id="08e17-121">Número de codecs</span><span class="sxs-lookup"><span data-stu-id="08e17-121">Number of codecs</span></span>                      |
| <span data-ttu-id="08e17-122">Entradas de codec</span><span class="sxs-lookup"><span data-stu-id="08e17-122">Codec Entries</span></span>           | <span data-ttu-id="08e17-123">**MINUCIOSA**\[\]</span><span class="sxs-lookup"><span data-stu-id="08e17-123">**BYTE**\[\]</span></span> | <span data-ttu-id="08e17-124">Varia</span><span class="sxs-lookup"><span data-stu-id="08e17-124">Varies</span></span>  | <span data-ttu-id="08e17-125">Matriz de estruturas de informações de codec</span><span class="sxs-lookup"><span data-stu-id="08e17-125">Array of codec information structures</span></span> |



 

<span data-ttu-id="08e17-126">O campo entradas de código é uma matriz de estruturas.</span><span class="sxs-lookup"><span data-stu-id="08e17-126">The Code Entries field is an array of structures.</span></span> <span data-ttu-id="08e17-127">A tabela a seguir mostra o formato de cada entrada:</span><span class="sxs-lookup"><span data-stu-id="08e17-127">The following table shows the format of each entry:</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="08e17-128">Campo de objeto da lista de codecs</span><span class="sxs-lookup"><span data-stu-id="08e17-128">Codec List Object field</span></span></th>
<th><span data-ttu-id="08e17-129">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="08e17-129">Data type</span></span></th>
<th><span data-ttu-id="08e17-130">Tamanho</span><span class="sxs-lookup"><span data-stu-id="08e17-130">Size</span></span></th>
<th><span data-ttu-id="08e17-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="08e17-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="08e17-132">Type</span><span class="sxs-lookup"><span data-stu-id="08e17-132">Type</span></span></td>
<td><span data-ttu-id="08e17-133"><strong>DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="08e17-133"><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="08e17-134">4 bytes</span><span class="sxs-lookup"><span data-stu-id="08e17-134">4 bytes</span></span></td>
<td><span data-ttu-id="08e17-135">Tipo de codec.</span><span class="sxs-lookup"><span data-stu-id="08e17-135">Codec type.</span></span> <span data-ttu-id="08e17-136">Esse valor pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="08e17-136">This can be one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="08e17-137">0x0001: codec de áudio</span><span class="sxs-lookup"><span data-stu-id="08e17-137">0x0001: Audio codec</span></span></li>
<li><span data-ttu-id="08e17-138">0x0002: codec de vídeo</span><span class="sxs-lookup"><span data-stu-id="08e17-138">0x0002: Video codec</span></span></li>
<li><span data-ttu-id="08e17-139">0xFFFF: desconhecido</span><span class="sxs-lookup"><span data-stu-id="08e17-139">0xFFFF: Unknown</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08e17-140">Comprimento do nome do codec</span><span class="sxs-lookup"><span data-stu-id="08e17-140">Codec Name Length</span></span></td>
<td><span data-ttu-id="08e17-141"><strong>DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="08e17-141"><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="08e17-142">4 bytes</span><span class="sxs-lookup"><span data-stu-id="08e17-142">4 bytes</span></span></td>
<td><span data-ttu-id="08e17-143">Tamanho da cadeia de caracteres do nome do codec, em bytes, incluindo o caractere <strong>nulo</strong> .</span><span class="sxs-lookup"><span data-stu-id="08e17-143">Size of the Codec Name string, in bytes, including the <strong>NULL</strong> character.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08e17-144">Nome do codec</span><span class="sxs-lookup"><span data-stu-id="08e17-144">Codec Name</span></span></td>
<td><span data-ttu-id="08e17-145"><strong>WCHAR</strong>[]</span><span class="sxs-lookup"><span data-stu-id="08e17-145"><strong>WCHAR</strong>[]</span></span></td>
<td><span data-ttu-id="08e17-146">Varia</span><span class="sxs-lookup"><span data-stu-id="08e17-146">Varies</span></span></td>
<td><span data-ttu-id="08e17-147">Cadeia de caracteres Unicode terminada em nulo que contém o nome do codec, como o &quot; Windows Media Video 9 &quot; .</span><span class="sxs-lookup"><span data-stu-id="08e17-147">Null-terminated Unicode string that contains the name of the codec, such as &quot;Windows Media Video 9&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08e17-148">Tamanho da descrição do codec</span><span class="sxs-lookup"><span data-stu-id="08e17-148">Codec Description Length</span></span></td>
<td><span data-ttu-id="08e17-149"><strong>DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="08e17-149"><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="08e17-150">4 bytes</span><span class="sxs-lookup"><span data-stu-id="08e17-150">4 bytes</span></span></td>
<td><span data-ttu-id="08e17-151">Tamanho da cadeia de caracteres de descrição do codec, em bytes, incluindo o caractere <strong>nulo</strong> .</span><span class="sxs-lookup"><span data-stu-id="08e17-151">Size of the Codec Description string, in bytes, including the <strong>NULL</strong> character.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08e17-152">Descrição do codec</span><span class="sxs-lookup"><span data-stu-id="08e17-152">Codec Description</span></span></td>
<td><span data-ttu-id="08e17-153"><strong>WCHAR</strong>[]</span><span class="sxs-lookup"><span data-stu-id="08e17-153"><strong>WCHAR</strong>[]</span></span></td>
<td><span data-ttu-id="08e17-154">Varia</span><span class="sxs-lookup"><span data-stu-id="08e17-154">Varies</span></span></td>
<td><span data-ttu-id="08e17-155">Uma cadeia de caracteres Unicode terminada em nulo que contém uma descrição do codec.</span><span class="sxs-lookup"><span data-stu-id="08e17-155">A null-terminated Unicode string that contains a description of the codec.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="08e17-156">Comprimento das informações do codec</span><span class="sxs-lookup"><span data-stu-id="08e17-156">Codec Information Length</span></span></td>
<td><span data-ttu-id="08e17-157"><strong>DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="08e17-157"><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="08e17-158">4 bytes</span><span class="sxs-lookup"><span data-stu-id="08e17-158">4 bytes</span></span></td>
<td><span data-ttu-id="08e17-159">Tamanho do campo de informações do codec, em bytes.</span><span class="sxs-lookup"><span data-stu-id="08e17-159">Size of the Codec Information field, in bytes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="08e17-160">Informações do codec</span><span class="sxs-lookup"><span data-stu-id="08e17-160">Codec Information</span></span></td>
<td><span data-ttu-id="08e17-161"><strong>Byte</strong>[]</span><span class="sxs-lookup"><span data-stu-id="08e17-161"><strong>BYTE</strong>[]</span></span></td>
<td><span data-ttu-id="08e17-162">Varia</span><span class="sxs-lookup"><span data-stu-id="08e17-162">Varies</span></span></td>
<td><span data-ttu-id="08e17-163">Dados de codec.</span><span class="sxs-lookup"><span data-stu-id="08e17-163">Codec data.</span></span> <span data-ttu-id="08e17-164">O significado desses dados depende do codec.</span><span class="sxs-lookup"><span data-stu-id="08e17-164">The meaning of this data depends on the codec.</span></span> <span data-ttu-id="08e17-165">Normalmente, esses dados indicam o formato.</span><span class="sxs-lookup"><span data-stu-id="08e17-165">Typically, this data indicates the format.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="08e17-166">O layout do blob de atributo não corresponde exatamente ao layout do objeto de lista de codec no cabeçalho ASF.</span><span class="sxs-lookup"><span data-stu-id="08e17-166">The layout of the attribute blob does not exactly match the layout of the Codec List Object in the ASF header.</span></span> <span data-ttu-id="08e17-167">Em particular, os comprimentos de cadeia de caracteres são fornecidos em bytes e incluem o tamanho do terminador **nulo** .</span><span class="sxs-lookup"><span data-stu-id="08e17-167">In particular, string lengths are given in bytes and include the size of the **NULL** terminator.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="08e17-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08e17-168">Requirements</span></span>



| <span data-ttu-id="08e17-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="08e17-169">Requirement</span></span> | <span data-ttu-id="08e17-170">Valor</span><span class="sxs-lookup"><span data-stu-id="08e17-170">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="08e17-171">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08e17-171">Minimum supported client</span></span><br/> | <span data-ttu-id="08e17-172">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="08e17-172">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="08e17-173">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08e17-173">Minimum supported server</span></span><br/> | <span data-ttu-id="08e17-174">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="08e17-174">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="08e17-175">parâmetro</span><span class="sxs-lookup"><span data-stu-id="08e17-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="08e17-176"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="08e17-176"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08e17-177">Confira também</span><span class="sxs-lookup"><span data-stu-id="08e17-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08e17-178">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="08e17-178">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="08e17-179">**IMFAttributes:: getBlob**</span><span class="sxs-lookup"><span data-stu-id="08e17-179">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="08e17-180">**IMFAttributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="08e17-180">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="08e17-181">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="08e17-181">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="08e17-182">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="08e17-182">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="08e17-183">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="08e17-183">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="08e17-184">Descritores de apresentação</span><span class="sxs-lookup"><span data-stu-id="08e17-184">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




