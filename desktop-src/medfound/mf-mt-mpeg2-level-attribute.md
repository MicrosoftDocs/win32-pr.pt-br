---
description: Especifica o nível MPEG-2 ou H. 264 em um tipo de mídia de vídeo.
ms.assetid: 8dd8e8c4-5a6f-4a87-a643-73af35c362a9
title: Atributo MF_MT_MPEG2_LEVEL (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 111c4b30befb1d4b25a688d25f46f02bcef21541
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170372"
---
# <a name="mf_mt_mpeg2_level-attribute"></a><span data-ttu-id="54abf-103">\_Atributo de \_ nível de MPEG2 do MF MT \_</span><span class="sxs-lookup"><span data-stu-id="54abf-103">MF\_MT\_MPEG2\_LEVEL attribute</span></span>

<span data-ttu-id="54abf-104">Especifica o nível MPEG-2 ou H. 264 em um tipo de mídia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="54abf-104">Specifies the MPEG-2 or H.264 level in a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="54abf-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="54abf-105">Data type</span></span>

<span data-ttu-id="54abf-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="54abf-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="54abf-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="54abf-107">Remarks</span></span>

<span data-ttu-id="54abf-108">Para vídeo MPEG-2, o valor desse atributo é um membro da enumeração [**am \_ MPEG2Level**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2level) .</span><span class="sxs-lookup"><span data-stu-id="54abf-108">For MPEG-2 video, the value of this attribute is a member of the [**AM\_MPEG2Level**](/previous-versions/windows/desktop/api/dvdmedia/ne-dvdmedia-am_mpeg2level) enumeration.</span></span>

<span data-ttu-id="54abf-109">Para o vídeo H. 264, o valor é um membro da enumeração [**eAVEncH264VLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel) .</span><span class="sxs-lookup"><span data-stu-id="54abf-109">For H.264 video, the value is a member of the [**eAVEncH264VLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel) enumeration.</span></span>

<span data-ttu-id="54abf-110">Esse atributo corresponde ao membro **dwLevel** da estrutura [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="54abf-110">This attribute corresponds to the **dwLevel** member of the [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure.</span></span>

<span data-ttu-id="54abf-111">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="54abf-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="54abf-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54abf-112">Requirements</span></span>



| <span data-ttu-id="54abf-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="54abf-113">Requirement</span></span> | <span data-ttu-id="54abf-114">Valor</span><span class="sxs-lookup"><span data-stu-id="54abf-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="54abf-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54abf-115">Minimum supported client</span></span><br/> | <span data-ttu-id="54abf-116">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="54abf-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="54abf-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54abf-117">Minimum supported server</span></span><br/> | <span data-ttu-id="54abf-118">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="54abf-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="54abf-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="54abf-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="54abf-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="54abf-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54abf-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="54abf-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54abf-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="54abf-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="54abf-123">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="54abf-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="54abf-124">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="54abf-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="54abf-125">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="54abf-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="54abf-126">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="54abf-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
