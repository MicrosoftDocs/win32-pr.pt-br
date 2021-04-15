---
description: Especifica para um tipo de mídia se os dados de mídia estão compactados.
ms.assetid: b44fb757-4390-4392-b1cb-37772b4ae3fb
title: Atributo MF_MT_COMPRESSED (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d049795f09845b5d32daf29ef033ab2e4b23007f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502384"
---
# <a name="mf_mt_compressed-attribute"></a><span data-ttu-id="ac3f3-103">\_ \_ Atributo compactado do MF MT</span><span class="sxs-lookup"><span data-stu-id="ac3f3-103">MF\_MT\_COMPRESSED attribute</span></span>

<span data-ttu-id="ac3f3-104">Especifica para um tipo de mídia se os dados de mídia estão compactados.</span><span class="sxs-lookup"><span data-stu-id="ac3f3-104">Specifies for a media type whether the media data is compressed.</span></span>

## <a name="data-type"></a><span data-ttu-id="ac3f3-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ac3f3-105">Data type</span></span>

<span data-ttu-id="ac3f3-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ac3f3-106">**UINT32**</span></span>

<span data-ttu-id="ac3f3-107">Tratar como um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="ac3f3-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac3f3-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac3f3-108">Remarks</span></span>

<span data-ttu-id="ac3f3-109">Se esse atributo for **true**, o tipo de mídia será um formato compactado.</span><span class="sxs-lookup"><span data-stu-id="ac3f3-109">If this attribute is **TRUE**, the media type is a compressed format.</span></span> <span data-ttu-id="ac3f3-110">Caso contrário, o tipo de mídia é descompactado ou o tipo de compactação não é conhecido.</span><span class="sxs-lookup"><span data-stu-id="ac3f3-110">Otherwise, either the media type is uncompressed or the compression type is not known.</span></span>

<span data-ttu-id="ac3f3-111">Não há garantia de que esse atributo seja definido como **true** para todos os formatos compactados; portanto, os aplicativos geralmente não devem confiar nesse atributo.</span><span class="sxs-lookup"><span data-stu-id="ac3f3-111">This attribute is not guaranteed to be set to **TRUE** for all compressed formats, so applications should generally not rely this attribute.</span></span> <span data-ttu-id="ac3f3-112">A maneira mais confiável de determinar se um formato é compactado é manter uma lista de formatos conhecidos.</span><span class="sxs-lookup"><span data-stu-id="ac3f3-112">The most reliable way to determine whether a format is compressed is to maintain a list of known formats.</span></span> <span data-ttu-id="ac3f3-113">Se um aplicativo não reconhecer um formato, conforme especificado no atributo de [**\_ \_ subtipo MF MT**](mf-mt-subtype-attribute.md) , ele não deverá assumir nada sobre a compactação do formato.</span><span class="sxs-lookup"><span data-stu-id="ac3f3-113">If an application does not recognize a format, as specified in the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute, it should not assume anything about the compression of the format.</span></span>

<span data-ttu-id="ac3f3-114">Para determinar se um formato usa a compactação temporal (o que significa que alguns exemplos são calculados como deltas de amostras anteriores), verifique o atributo [**\_ \_ independente de todos os \_ exemplos \_ do MF MT**](mf-mt-all-samples-independent-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="ac3f3-114">To determine whether a format uses temporal compression (meaning that some samples are computed as deltas from earlier samples), check the [**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**](mf-mt-all-samples-independent-attribute.md) attribute.</span></span>

<span data-ttu-id="ac3f3-115">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ac3f3-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac3f3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac3f3-116">Requirements</span></span>



| <span data-ttu-id="ac3f3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac3f3-117">Requirement</span></span> | <span data-ttu-id="ac3f3-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ac3f3-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ac3f3-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac3f3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ac3f3-120">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="ac3f3-120">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="ac3f3-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac3f3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ac3f3-122">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ac3f3-122">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="ac3f3-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ac3f3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac3f3-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac3f3-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac3f3-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac3f3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac3f3-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ac3f3-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ac3f3-127">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ac3f3-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="ac3f3-128">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="ac3f3-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="ac3f3-129">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="ac3f3-129">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="ac3f3-130">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="ac3f3-130">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




