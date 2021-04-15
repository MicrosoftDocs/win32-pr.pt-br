---
description: Especifica os marcadores em um arquivo ASF (Advanced Systems Format). Esse atributo corresponde ao objeto de marcador no cabeçalho ASF, definido na especificação ASF.
ms.assetid: 6458eb5f-72a2-4723-b26b-b63516aa2df3
title: Atributo MF_PD_ASF_MARKER (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2ae9c5a6cfd79924b95a3b15a7146539d630aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761429"
---
# <a name="mf_pd_asf_marker-attribute"></a><span data-ttu-id="b02e7-104">\_Atributo de marcador MF PD \_ ASF \_</span><span class="sxs-lookup"><span data-stu-id="b02e7-104">MF\_PD\_ASF\_MARKER attribute</span></span>

<span data-ttu-id="b02e7-105">Especifica os marcadores em um arquivo ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="b02e7-105">Specifies the markers in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="b02e7-106">Esse atributo corresponde ao objeto de marcador no cabeçalho ASF, definido na especificação ASF.</span><span class="sxs-lookup"><span data-stu-id="b02e7-106">This attribute corresponds to the Marker Object in the ASF header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="b02e7-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b02e7-107">Data type</span></span>

<span data-ttu-id="b02e7-108">Matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="b02e7-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="b02e7-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="b02e7-109">Remarks</span></span>

<span data-ttu-id="b02e7-110">Esse atributo se aplica a descritores de apresentação para conteúdo ASF.</span><span class="sxs-lookup"><span data-stu-id="b02e7-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="b02e7-111">O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) cria o descritor de apresentação e gera esse atributo a partir do objeto Marker.</span><span class="sxs-lookup"><span data-stu-id="b02e7-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method creates the presentation descriptor and generates this attribute from the Marker Object.</span></span> <span data-ttu-id="b02e7-112">A tabela a seguir mostra o formato do blob:</span><span class="sxs-lookup"><span data-stu-id="b02e7-112">The following table shows the format of the blob:</span></span>



| <span data-ttu-id="b02e7-113">Campo de objeto de marcador</span><span class="sxs-lookup"><span data-stu-id="b02e7-113">Marker Object field</span></span> | <span data-ttu-id="b02e7-114">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b02e7-114">Data type</span></span>    | <span data-ttu-id="b02e7-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="b02e7-115">Size</span></span>    | <span data-ttu-id="b02e7-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="b02e7-116">Description</span></span>       |
|---------------------|--------------|---------|-------------------|
| <span data-ttu-id="b02e7-117">Contagem de marcadores</span><span class="sxs-lookup"><span data-stu-id="b02e7-117">Markers Count</span></span>       | <span data-ttu-id="b02e7-118">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b02e7-118">**DWORD**</span></span>    | <span data-ttu-id="b02e7-119">4 bytes</span><span class="sxs-lookup"><span data-stu-id="b02e7-119">4 bytes</span></span> | <span data-ttu-id="b02e7-120">Número de marcadores</span><span class="sxs-lookup"><span data-stu-id="b02e7-120">Number of markers</span></span> |
| <span data-ttu-id="b02e7-121">Marcadores</span><span class="sxs-lookup"><span data-stu-id="b02e7-121">Markers</span></span>             | <span data-ttu-id="b02e7-122">**MINUCIOSA**\[\]</span><span class="sxs-lookup"><span data-stu-id="b02e7-122">**BYTE**\[\]</span></span> | <span data-ttu-id="b02e7-123">Varia</span><span class="sxs-lookup"><span data-stu-id="b02e7-123">Varies</span></span>  | <span data-ttu-id="b02e7-124">Matriz de marcadores</span><span class="sxs-lookup"><span data-stu-id="b02e7-124">Array of markers</span></span>  |



 

<span data-ttu-id="b02e7-125">A primeira **DWORD** é o número de marcadores, seguido por uma matriz de marcadores.</span><span class="sxs-lookup"><span data-stu-id="b02e7-125">The first **DWORD** is the number of markers, followed by an array of markers.</span></span> <span data-ttu-id="b02e7-126">Cada marcador tem o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="b02e7-126">Each marker has the following format:</span></span>



| <span data-ttu-id="b02e7-127">Campo de objeto de marcador</span><span class="sxs-lookup"><span data-stu-id="b02e7-127">Marker Object field</span></span>       | <span data-ttu-id="b02e7-128">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b02e7-128">Data type</span></span>     | <span data-ttu-id="b02e7-129">Tamanho</span><span class="sxs-lookup"><span data-stu-id="b02e7-129">Size</span></span>    | <span data-ttu-id="b02e7-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="b02e7-130">Description</span></span>                                                                       |
|---------------------------|---------------|---------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b02e7-131">Comprimento da descrição do marcador</span><span class="sxs-lookup"><span data-stu-id="b02e7-131">Marker Description Length</span></span> | <span data-ttu-id="b02e7-132">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="b02e7-132">**DWORD**</span></span>     | <span data-ttu-id="b02e7-133">4 bytes</span><span class="sxs-lookup"><span data-stu-id="b02e7-133">4 bytes</span></span> | <span data-ttu-id="b02e7-134">Tamanho da cadeia de caracteres de descrição, em bytes, incluindo o caractere nulo.</span><span class="sxs-lookup"><span data-stu-id="b02e7-134">Size of the description string, in bytes, including the NULL character.</span></span>           |
| <span data-ttu-id="b02e7-135">Descrição do marcador</span><span class="sxs-lookup"><span data-stu-id="b02e7-135">Marker Description</span></span>        | <span data-ttu-id="b02e7-136">**WCHAR**\[\]</span><span class="sxs-lookup"><span data-stu-id="b02e7-136">**WCHAR**\[\]</span></span> | <span data-ttu-id="b02e7-137">Varia</span><span class="sxs-lookup"><span data-stu-id="b02e7-137">Varies</span></span>  | <span data-ttu-id="b02e7-138">Cadeia de caracteres terminada em nulo que descreve o marcador.</span><span class="sxs-lookup"><span data-stu-id="b02e7-138">Null-terminated string that describes the marker.</span></span>                                 |
| <span data-ttu-id="b02e7-139">Tempo da apresentação</span><span class="sxs-lookup"><span data-stu-id="b02e7-139">Presentation Time</span></span>         | <span data-ttu-id="b02e7-140">**LONGLONG**</span><span class="sxs-lookup"><span data-stu-id="b02e7-140">**LONGLONG**</span></span>  | <span data-ttu-id="b02e7-141">8 bytes</span><span class="sxs-lookup"><span data-stu-id="b02e7-141">8 bytes</span></span> | <span data-ttu-id="b02e7-142">Hora da apresentação do marcador, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="b02e7-142">Presentation time of the marker, in 100-nanosecond units.</span></span>                         |
| <span data-ttu-id="b02e7-143">Hora de envio</span><span class="sxs-lookup"><span data-stu-id="b02e7-143">Send Time</span></span>                 | <span data-ttu-id="b02e7-144">**LONGLONG**</span><span class="sxs-lookup"><span data-stu-id="b02e7-144">**LONGLONG**</span></span>  | <span data-ttu-id="b02e7-145">8 bytes</span><span class="sxs-lookup"><span data-stu-id="b02e7-145">8 bytes</span></span> | <span data-ttu-id="b02e7-146">Hora de envio da entrada do marcador, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="b02e7-146">Send time of the marker entry, in milliseconds.</span></span>                                   |
| <span data-ttu-id="b02e7-147">Deslocamento</span><span class="sxs-lookup"><span data-stu-id="b02e7-147">Offset</span></span>                    | <span data-ttu-id="b02e7-148">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="b02e7-148">**UINT64**</span></span>    | <span data-ttu-id="b02e7-149">8 bytes</span><span class="sxs-lookup"><span data-stu-id="b02e7-149">8 bytes</span></span> | <span data-ttu-id="b02e7-150">Deslocamento, em bytes, no objeto de dados que especifica a posição do mercado.</span><span class="sxs-lookup"><span data-stu-id="b02e7-150">Offset, in bytes, into the Data Object that specifies the position of the market.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="b02e7-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b02e7-151">Requirements</span></span>



| <span data-ttu-id="b02e7-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="b02e7-152">Requirement</span></span> | <span data-ttu-id="b02e7-153">Valor</span><span class="sxs-lookup"><span data-stu-id="b02e7-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b02e7-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b02e7-154">Minimum supported client</span></span><br/> | <span data-ttu-id="b02e7-155">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b02e7-155">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b02e7-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b02e7-156">Minimum supported server</span></span><br/> | <span data-ttu-id="b02e7-157">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b02e7-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b02e7-158">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b02e7-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="b02e7-159"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="b02e7-159"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b02e7-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="b02e7-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b02e7-161">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b02e7-161">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b02e7-162">**IMFAttributes:: getBlob**</span><span class="sxs-lookup"><span data-stu-id="b02e7-162">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="b02e7-163">**IMFAttributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="b02e7-163">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="b02e7-164">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="b02e7-164">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="b02e7-165">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="b02e7-165">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="b02e7-166">Objeto de cabeçalho ASF</span><span class="sxs-lookup"><span data-stu-id="b02e7-166">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="b02e7-167">Descritores de apresentação</span><span class="sxs-lookup"><span data-stu-id="b02e7-167">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




