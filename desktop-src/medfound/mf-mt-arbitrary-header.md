---
description: Dados específicos de tipo para um fluxo binário em um arquivo ASF (Advanced Systems Format).
ms.assetid: 45608dde-894b-4204-80dc-505f068fb158
title: Atributo MF_MT_ARBITRARY_HEADER (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abd559ede3506335378ae1d56bf5b886e1407946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010715"
---
# <a name="mf_mt_arbitrary_header-attribute"></a><span data-ttu-id="b9517-103">\_Atributo de \_ cabeçalho arbitrário MF MT \_</span><span class="sxs-lookup"><span data-stu-id="b9517-103">MF\_MT\_ARBITRARY\_HEADER attribute</span></span>

<span data-ttu-id="b9517-104">Dados específicos de tipo para um fluxo binário em um arquivo ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="b9517-104">Type-specific data for a binary stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="b9517-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b9517-105">Data type</span></span>

<span data-ttu-id="b9517-106">**[**MT \_ \_Cabeçalho arbitrário**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header)** armazenado como **byte \[ \]**</span><span class="sxs-lookup"><span data-stu-id="b9517-106">**[**MT\_ARBITRARY\_HEADER**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header)** stored as **BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="b9517-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="b9517-107">Get/set</span></span>

<span data-ttu-id="b9517-108">Para obter esse atributo, chame [**IMFAttributes:: getBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="b9517-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="b9517-109">Para definir esse atributo, chame [**IMFAttributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="b9517-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="remarks"></a><span data-ttu-id="b9517-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9517-110">Remarks</span></span>

<span data-ttu-id="b9517-111">Os arquivos ASF podem conter fluxos com dados binários.</span><span class="sxs-lookup"><span data-stu-id="b9517-111">ASF files can contain streams with binary data.</span></span> <span data-ttu-id="b9517-112">O \_ atributo de \_ cabeçalho arbitrário MF MT \_ no tipo de mídia contém uma estrutura de [**\_ \_ cabeçalho arbitrário MT**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) que descreve o fluxo.</span><span class="sxs-lookup"><span data-stu-id="b9517-112">The MF\_MT\_ARBITRARY\_HEADER attribute in the media type contains an [**MT\_ARBITRARY\_HEADER**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) structure that describes the stream.</span></span>

<span data-ttu-id="b9517-113">Além do \_ \_ atributo de cabeçalho arbitrário MF MT \_ , o tipo de mídia para um fluxo binário ASF contém os seguintes atributos:</span><span class="sxs-lookup"><span data-stu-id="b9517-113">In addition to the MF\_MT\_ARBITRARY\_HEADER attribute, the media type for an ASF binary stream contains the following attributes:</span></span>



| <span data-ttu-id="b9517-114">Atributo</span><span class="sxs-lookup"><span data-stu-id="b9517-114">Attribute</span></span>                                                 | <span data-ttu-id="b9517-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="b9517-115">Description</span></span>                                            |
|-----------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="b9517-116">**\_ \_ tipo principal MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="b9517-116">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="b9517-117">O valor do atributo é **\_ binário MFMediaType**.</span><span class="sxs-lookup"><span data-stu-id="b9517-117">The value of the attribute is **MFMediaType\_Binary**.</span></span> |
| [<span data-ttu-id="b9517-118">\_ \_ formato ARBITRÁRIO do MF MT \_</span><span class="sxs-lookup"><span data-stu-id="b9517-118">MF\_MT\_ARBITRARY\_FORMAT</span></span>](mf-mt-arbitrary-format.md)   | <span data-ttu-id="b9517-119">Contém dados de formato adicionais.</span><span class="sxs-lookup"><span data-stu-id="b9517-119">Contains additional format data.</span></span>                       |



 

> [!Note]  
> <span data-ttu-id="b9517-120">No SDK do Windows Media Format, os fluxos binários são chamados de *fluxos arbitrários* ou *fluxos de dados arbitrários*.</span><span class="sxs-lookup"><span data-stu-id="b9517-120">In the Windows Media Format SDK, binary streams are called *arbitrary streams* or *arbitrary data streams*.</span></span>

 

<span data-ttu-id="b9517-121">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b9517-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9517-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9517-122">Requirements</span></span>



| <span data-ttu-id="b9517-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9517-123">Requirement</span></span> | <span data-ttu-id="b9517-124">Valor</span><span class="sxs-lookup"><span data-stu-id="b9517-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b9517-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9517-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b9517-126">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b9517-126">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b9517-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9517-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b9517-128">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="b9517-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b9517-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b9517-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9517-130"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9517-130"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9517-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="b9517-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9517-132">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b9517-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b9517-133">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="b9517-133">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




