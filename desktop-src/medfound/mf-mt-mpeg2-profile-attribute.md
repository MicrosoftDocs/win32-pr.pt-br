---
description: Especifica o perfil MPEG-2 ou H. 264 em um tipo de mídia de vídeo.
ms.assetid: 8c6a68cb-d976-4099-8934-064f0e8f6374
title: Atributo MF_MT_MPEG2_PROFILE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee5c64ea9f5bdf73a78d6ae29124c7cd5b37df43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829115"
---
# <a name="mf_mt_mpeg2_profile-attribute"></a><span data-ttu-id="5a06d-103">\_Atributo de perfil MF mt de \_ MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="5a06d-103">MF\_MT\_MPEG2\_PROFILE attribute</span></span>

<span data-ttu-id="5a06d-104">Especifica o perfil MPEG-2 ou H. 264 em um tipo de mídia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5a06d-104">Specifies the MPEG-2 or H.264 profile in a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="5a06d-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="5a06d-105">Data type</span></span>

<span data-ttu-id="5a06d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5a06d-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="5a06d-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a06d-107">Remarks</span></span>

<span data-ttu-id="5a06d-108">Para vídeo MPEG-2, o valor desse atributo é um membro da enumeração [**am \_ MPEG2Profile**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2profile) .</span><span class="sxs-lookup"><span data-stu-id="5a06d-108">For MPEG-2 video, the value of this attribute is a member of the [**AM\_MPEG2Profile**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2profile) enumeration.</span></span>

<span data-ttu-id="5a06d-109">Para o vídeo H. 264, o valor é um membro da enumeração [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) .</span><span class="sxs-lookup"><span data-stu-id="5a06d-109">For H.264 video, the value is a member of the [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) enumeration.</span></span>

<span data-ttu-id="5a06d-110">Esse atributo corresponde ao membro **dwProfile** da estrutura [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="5a06d-110">This attribute corresponds to the **dwProfile** member of the [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure.</span></span>

<span data-ttu-id="5a06d-111">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="5a06d-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a06d-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a06d-112">Requirements</span></span>



| <span data-ttu-id="5a06d-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a06d-113">Requirement</span></span> | <span data-ttu-id="5a06d-114">Valor</span><span class="sxs-lookup"><span data-stu-id="5a06d-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5a06d-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a06d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="5a06d-116">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="5a06d-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="5a06d-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a06d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="5a06d-118">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5a06d-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="5a06d-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5a06d-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a06d-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a06d-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a06d-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a06d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a06d-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5a06d-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5a06d-123">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="5a06d-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="5a06d-124">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="5a06d-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="5a06d-125">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="5a06d-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="5a06d-126">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="5a06d-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
