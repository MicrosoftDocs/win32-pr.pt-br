---
description: Descreve como o croma foi amostrado para um tipo de mídia de vídeo YCbCr.
ms.assetid: 0c930348-8669-42cc-9d74-df9ef475bdc8
title: Atributo MF_MT_VIDEO_CHROMA_SITING (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa634cf9a9ca7f5c292eb0cf06c6a1a14c788d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105815522"
---
# <a name="mf_mt_video_chroma_siting-attribute"></a><span data-ttu-id="50068-103">\_Atributo MF MT \_ Video \_ croma \_ localizando</span><span class="sxs-lookup"><span data-stu-id="50068-103">MF\_MT\_VIDEO\_CHROMA\_SITING attribute</span></span>

<span data-ttu-id="50068-104">Descreve como o croma foi amostrado para o tipo de mídia de vídeo de um Y'Cb'Cr.</span><span class="sxs-lookup"><span data-stu-id="50068-104">Describes how chroma was sampled for a Y'Cb'Cr' video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="50068-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="50068-105">Data type</span></span>

<span data-ttu-id="50068-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="50068-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="50068-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="50068-107">Remarks</span></span>

<span data-ttu-id="50068-108">O valor desse atributo é um bit a bit **ou** dos sinalizadores da enumeração [**MFVideoChromaSubsampling**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideochromasubsampling) .</span><span class="sxs-lookup"><span data-stu-id="50068-108">The value of this attribute is a bitwise **OR** of flags from the [**MFVideoChromaSubsampling**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideochromasubsampling) enumeration.</span></span>

<span data-ttu-id="50068-109">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="50068-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="50068-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50068-110">Requirements</span></span>



| <span data-ttu-id="50068-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="50068-111">Requirement</span></span> | <span data-ttu-id="50068-112">Valor</span><span class="sxs-lookup"><span data-stu-id="50068-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="50068-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50068-113">Minimum supported client</span></span><br/> | <span data-ttu-id="50068-114">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="50068-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="50068-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50068-115">Minimum supported server</span></span><br/> | <span data-ttu-id="50068-116">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="50068-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="50068-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="50068-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="50068-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="50068-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50068-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="50068-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50068-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="50068-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="50068-121">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="50068-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="50068-122">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="50068-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="50068-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="50068-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="50068-124">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="50068-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="50068-125">Informações de cores estendidas</span><span class="sxs-lookup"><span data-stu-id="50068-125">Extended Color Information</span></span>](extended-color-information.md)
</dt> </dl>

 

 




