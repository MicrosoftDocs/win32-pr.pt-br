---
description: Especifica o intervalo nominal das informações de cor em um tipo de mídia de vídeo.
ms.assetid: 7b2b809e-aae4-401c-816a-626fb88f5f87
title: Atributo MF_MT_VIDEO_NOMINAL_RANGE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4539b06281655e079d9ff6ca4000e0ed75462b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754233"
---
# <a name="mf_mt_video_nominal_range-attribute"></a><span data-ttu-id="b74c9-103">\_Atributo de \_ \_ intervalo nominal de vídeo MF MT \_</span><span class="sxs-lookup"><span data-stu-id="b74c9-103">MF\_MT\_VIDEO\_NOMINAL\_RANGE attribute</span></span>

<span data-ttu-id="b74c9-104">Especifica o intervalo nominal das informações de cor em um tipo de mídia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b74c9-104">Specifies the nominal range of the color information in a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="b74c9-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b74c9-105">Data type</span></span>

<span data-ttu-id="b74c9-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b74c9-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="b74c9-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="b74c9-107">Remarks</span></span>

<span data-ttu-id="b74c9-108">O valor desse atributo é um membro da enumeração [**MFNominalRange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange) .</span><span class="sxs-lookup"><span data-stu-id="b74c9-108">The value of this attribute is a member of the [**MFNominalRange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange) enumeration.</span></span>

<span data-ttu-id="b74c9-109">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b74c9-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

<span data-ttu-id="b74c9-110">**Codificadores H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="b74c9-110">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="b74c9-111">No tipo de mídia de saída, \_ o \_ intervalo nominal de vídeo MF MT \_ \_ pode ser definido com **MFNominalRange \_ 0 \_ 255** e **MFNominalRange \_ 16 \_ 235**.</span><span class="sxs-lookup"><span data-stu-id="b74c9-111">On the output media type, MF\_MT\_VIDEO\_NOMINAL\_RANGE can be set with **MFNominalRange\_0\_255** and **MFNominalRange\_16\_235**.</span></span>

<span data-ttu-id="b74c9-112">O codificador H. 264/AVC deve tratar **MFNominalRange \_ desconhecido** como **MFNominalRange \_ 16 \_ 235**.</span><span class="sxs-lookup"><span data-stu-id="b74c9-112">H.264/AVC encoder shall treat **MFNominalRange\_Unknown** as **MFNominalRange\_16\_235**.</span></span>

<span data-ttu-id="b74c9-113">O codificador H. 264/AVC deve rejeitar um tipo de mídia de saída quando o \_ \_ intervalo nominal de vídeo MF MT \_ \_ é definido como **MFNominalRange \_ 48 \_ 208**, **MFNominalRange \_ 64 \_ 127** ou quaisquer outros valores não definidos em [**MFNominalRange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange).</span><span class="sxs-lookup"><span data-stu-id="b74c9-113">H.264/AVC encoder shall reject a output media type when MF\_MT\_VIDEO\_NOMINAL\_RANGE is set to **MFNominalRange\_48\_208**, **MFNominalRange\_64\_127**, or any other values not defined on [**MFNominalRange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange).</span></span>

## <a name="requirements"></a><span data-ttu-id="b74c9-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b74c9-114">Requirements</span></span>



| <span data-ttu-id="b74c9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b74c9-115">Requirement</span></span> | <span data-ttu-id="b74c9-116">Valor</span><span class="sxs-lookup"><span data-stu-id="b74c9-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b74c9-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b74c9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b74c9-118">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="b74c9-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="b74c9-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b74c9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b74c9-120">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b74c9-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="b74c9-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b74c9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b74c9-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b74c9-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b74c9-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="b74c9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b74c9-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b74c9-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b74c9-125">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="b74c9-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="b74c9-126">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="b74c9-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="b74c9-127">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="b74c9-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="b74c9-128">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="b74c9-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="b74c9-129">Informações de cores estendidas</span><span class="sxs-lookup"><span data-stu-id="b74c9-129">Extended Color Information</span></span>](extended-color-information.md)
</dt> </dl>

 

 




