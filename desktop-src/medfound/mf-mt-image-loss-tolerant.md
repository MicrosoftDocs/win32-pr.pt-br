---
description: Especifica se um fluxo de imagem ASF é um tipo de JPEG degradado.
ms.assetid: e29d0893-8561-4a8c-99e2-168186becd82
title: Atributo MF_MT_IMAGE_LOSS_TOLERANT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eea33f9f5f49725d164bd26ba21b9602bffef2b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827203"
---
# <a name="mf_mt_image_loss_tolerant-attribute"></a><span data-ttu-id="e9888-103">\_ \_ \_ Atributo tolerante a perda de imagem MF MT \_</span><span class="sxs-lookup"><span data-stu-id="e9888-103">MF\_MT\_IMAGE\_LOSS\_TOLERANT attribute</span></span>

<span data-ttu-id="e9888-104">Especifica se um fluxo de imagem ASF é um tipo de JPEG degradado.</span><span class="sxs-lookup"><span data-stu-id="e9888-104">Specifies whether an ASF image stream is a degradable JPEG type.</span></span>

## <a name="data-type"></a><span data-ttu-id="e9888-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e9888-105">Data type</span></span>

<span data-ttu-id="e9888-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e9888-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="e9888-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="e9888-107">Get/set</span></span>

<span data-ttu-id="e9888-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="e9888-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="e9888-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="e9888-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="e9888-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="e9888-110">Applies to</span></span>

[<span data-ttu-id="e9888-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="e9888-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="e9888-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="e9888-112">Remarks</span></span>

<span data-ttu-id="e9888-113">Esse atributo se aplica ao tipo de mídia para fluxos de imagem no ASF.</span><span class="sxs-lookup"><span data-stu-id="e9888-113">This attribute applies to the media type for image streams in ASF.</span></span> <span data-ttu-id="e9888-114">Se o valor for **true**, o fluxo será um tipo de imagem JPEG degradado.</span><span class="sxs-lookup"><span data-stu-id="e9888-114">If the value is **TRUE**, the stream is a degradable JPEG image type.</span></span> <span data-ttu-id="e9888-115">Caso contrário, o fluxo é um tipo de imagem JFIF.</span><span class="sxs-lookup"><span data-stu-id="e9888-115">Otherwise, the stream is a JFIF image type.</span></span> <span data-ttu-id="e9888-116">Para obter mais informações sobre esses tipos de fluxo, consulte a especificação do ASF.</span><span class="sxs-lookup"><span data-stu-id="e9888-116">For more information about these stream types, see the ASF specification.</span></span>

<span data-ttu-id="e9888-117">Além do \_ atributo de tolerância a perda de imagem MF MT \_ \_ \_ , o tipo de mídia para um fluxo de imagem ASF contém os seguintes atributos:</span><span class="sxs-lookup"><span data-stu-id="e9888-117">In addition to the MF\_MT\_IMAGE\_LOSS\_TOLERANT attribute, the media type for an ASF image stream contains the following attributes:</span></span>



| <span data-ttu-id="e9888-118">Atributo</span><span class="sxs-lookup"><span data-stu-id="e9888-118">Attribute</span></span>                                                 | <span data-ttu-id="e9888-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="e9888-119">Description</span></span>                                |
|-----------------------------------------------------------|--------------------------------------------|
| [<span data-ttu-id="e9888-120">**\_ \_ tipo principal MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="e9888-120">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="e9888-121">Contém a **\_ imagem** do valor MFMediaType.</span><span class="sxs-lookup"><span data-stu-id="e9888-121">Contains the value **MFMediaType\_Image**.</span></span> |
| [<span data-ttu-id="e9888-122">**\_tamanho do \_ quadro MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="e9888-122">**MF\_MT\_FRAME\_SIZE**</span></span>](mf-mt-frame-size-attribute.md) | <span data-ttu-id="e9888-123">Retorna o tamanho da imagem em pixels.</span><span class="sxs-lookup"><span data-stu-id="e9888-123">Gives the image size in pixels.</span></span>            |



 

<span data-ttu-id="e9888-124">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="e9888-124">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9888-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9888-125">Requirements</span></span>



| <span data-ttu-id="e9888-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9888-126">Requirement</span></span> | <span data-ttu-id="e9888-127">Valor</span><span class="sxs-lookup"><span data-stu-id="e9888-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e9888-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9888-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e9888-129">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e9888-129">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="e9888-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9888-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e9888-131">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="e9888-131">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="e9888-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e9888-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9888-133"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9888-133"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9888-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9888-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9888-135">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e9888-135">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e9888-136">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="e9888-136">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




