---
description: Contém uma lista de idiomas RFC 1766 usados na apresentação atual.
ms.assetid: 8853bd88-d51a-478c-8c78-cf69a260e295
title: Atributo MF_PD_ASF_LANGLIST_LEGACYORDER (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f24abc714a7605800faa8ad66f8c0b888fba6f79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770478"
---
# <a name="mf_pd_asf_langlist_legacyorder-attribute"></a><span data-ttu-id="9e260-103">\_Atributo MF PD \_ ASF \_ langlist \_ LEGACYORDER</span><span class="sxs-lookup"><span data-stu-id="9e260-103">MF\_PD\_ASF\_LANGLIST\_LEGACYORDER attribute</span></span>

<span data-ttu-id="9e260-104">Contém uma lista de idiomas RFC 1766 usados na apresentação atual.</span><span class="sxs-lookup"><span data-stu-id="9e260-104">Contains a list of RFC 1766 languages used in the current presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="9e260-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="9e260-105">Data type</span></span>

<span data-ttu-id="9e260-106">**MINUCIOSA \[\]**</span><span class="sxs-lookup"><span data-stu-id="9e260-106">**BYTE \[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="9e260-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="9e260-107">Get/set</span></span>

<span data-ttu-id="9e260-108">Para obter esse atributo, chame [**IMFAttributes:: getBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="9e260-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="9e260-109">Para definir esse atributo, chame [**IMFAttributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="9e260-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="applies-to"></a><span data-ttu-id="9e260-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="9e260-110">Applies to</span></span>

[<span data-ttu-id="9e260-111">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="9e260-111">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a><span data-ttu-id="9e260-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e260-112">Remarks</span></span>

<span data-ttu-id="9e260-113">Esse atributo se aplica a descritores de apresentação que foram gerados do [objeto ASF ContentInfo](asf-contentinfo-object.md) por uma chamada para [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="9e260-113">This attribute applies to presentation descriptors that were generated from the [ASF ContentInfo Object](asf-contentinfo-object.md) by a call to [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor).</span></span> <span data-ttu-id="9e260-114">O formato da matriz de bytes é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="9e260-114">The format of the byte array is as follows:</span></span>



| <span data-ttu-id="9e260-115">Campo de objeto de lista de idiomas</span><span class="sxs-lookup"><span data-stu-id="9e260-115">Language List Object field</span></span> | <span data-ttu-id="9e260-116">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="9e260-116">Data type</span></span>    | <span data-ttu-id="9e260-117">Tamanho</span><span class="sxs-lookup"><span data-stu-id="9e260-117">Size</span></span>    | <span data-ttu-id="9e260-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="9e260-118">Description</span></span>                            |
|----------------------------|--------------|---------|----------------------------------------|
| <span data-ttu-id="9e260-119">Contagem de registros de ID de idioma</span><span class="sxs-lookup"><span data-stu-id="9e260-119">Language ID Records Count</span></span>  | <span data-ttu-id="9e260-120">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="9e260-120">**DWORD**</span></span>    | <span data-ttu-id="9e260-121">4 bytes</span><span class="sxs-lookup"><span data-stu-id="9e260-121">4 bytes</span></span> | <span data-ttu-id="9e260-122">Número de idiomas</span><span class="sxs-lookup"><span data-stu-id="9e260-122">Number of languages</span></span>                    |
| <span data-ttu-id="9e260-123">Registros de ID de idioma</span><span class="sxs-lookup"><span data-stu-id="9e260-123">Language ID Records</span></span>        | <span data-ttu-id="9e260-124">**MINUCIOSA**\[\]</span><span class="sxs-lookup"><span data-stu-id="9e260-124">**BYTE**\[\]</span></span> | <span data-ttu-id="9e260-125">Varia</span><span class="sxs-lookup"><span data-stu-id="9e260-125">Varies</span></span>  | <span data-ttu-id="9e260-126">Matriz de cadeias de caracteres de linguagem (veja abaixo).</span><span class="sxs-lookup"><span data-stu-id="9e260-126">Array of language strings (see below).</span></span> |



 

<span data-ttu-id="9e260-127">O primeiro **DWORD** é o número de idiomas, seguido por uma matriz de cadeias de caracteres de identificador de linguagem.</span><span class="sxs-lookup"><span data-stu-id="9e260-127">The first **DWORD** is the number of languages, followed by an array of language identifier strings.</span></span> <span data-ttu-id="9e260-128">Cada cadeia de caracteres tem o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="9e260-128">Each string has the following format:</span></span>



| <span data-ttu-id="9e260-129">Campo de objeto de lista de idiomas</span><span class="sxs-lookup"><span data-stu-id="9e260-129">Language List Object field</span></span> | <span data-ttu-id="9e260-130">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="9e260-130">Data type</span></span>     | <span data-ttu-id="9e260-131">Tamanho</span><span class="sxs-lookup"><span data-stu-id="9e260-131">Size</span></span>    | <span data-ttu-id="9e260-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="9e260-132">Description</span></span>                                                                               |
|----------------------------|---------------|---------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e260-133">Comprimento da ID de idioma</span><span class="sxs-lookup"><span data-stu-id="9e260-133">Language ID Length</span></span>         | <span data-ttu-id="9e260-134">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="9e260-134">**DWORD**</span></span>     | <span data-ttu-id="9e260-135">4 bytes</span><span class="sxs-lookup"><span data-stu-id="9e260-135">4 bytes</span></span> | <span data-ttu-id="9e260-136">O comprimento da cadeia de caracteres em bytes, incluindo o tamanho do caractere **nulo** à direita.</span><span class="sxs-lookup"><span data-stu-id="9e260-136">The length of the string in bytes, including the size of the trailing **NULL** character.</span></span> |
| <span data-ttu-id="9e260-137">ID do idioma</span><span class="sxs-lookup"><span data-stu-id="9e260-137">Language ID</span></span>                | <span data-ttu-id="9e260-138">**WCHAR**\[\]</span><span class="sxs-lookup"><span data-stu-id="9e260-138">**WCHAR**\[\]</span></span> | <span data-ttu-id="9e260-139">Varia</span><span class="sxs-lookup"><span data-stu-id="9e260-139">Varies</span></span>  | <span data-ttu-id="9e260-140">Uma cadeia de caracteres terminada em nulo que contém o nome do idioma RFC 1766.</span><span class="sxs-lookup"><span data-stu-id="9e260-140">A null-terminated string containing the RFC 1766 language name.</span></span>                           |



 

<span data-ttu-id="9e260-141">Cada cadeia de caracteres é uma marca de idioma compatível com RFC 1766.</span><span class="sxs-lookup"><span data-stu-id="9e260-141">Each string is a language tag compliant with RFC 1766.</span></span>

<span data-ttu-id="9e260-142">Use esse atributo somente para compatibilidade com versões anteriores com a ordem de enumeração da interface [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) no SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="9e260-142">Use this attribute only for backward compatibility with the enumeration order of the [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) interface in the Windows Media Format SDK.</span></span> <span data-ttu-id="9e260-143">As cadeias de caracteres de idioma são armazenadas em uma ordem diferente no atributo [**MF \_ PD \_ ASF \_ langlist**](mf-pd-asf-langlist-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="9e260-143">The language strings are stored in a different order in the [**MF\_PD\_ASF\_LANGLIST**](mf-pd-asf-langlist-attribute.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e260-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e260-144">Requirements</span></span>



| <span data-ttu-id="9e260-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e260-145">Requirement</span></span> | <span data-ttu-id="9e260-146">Valor</span><span class="sxs-lookup"><span data-stu-id="9e260-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e260-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e260-147">Minimum supported client</span></span><br/> | <span data-ttu-id="9e260-148">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9e260-148">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9e260-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e260-149">Minimum supported server</span></span><br/> | <span data-ttu-id="9e260-150">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="9e260-150">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9e260-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9e260-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e260-152"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e260-152"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e260-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e260-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e260-154">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9e260-154">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9e260-155">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="9e260-155">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 
