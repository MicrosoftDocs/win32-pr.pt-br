---
description: O código de hora de início do grupo de imagens (GOP), para um tipo de mídia de vídeo MPEG-1 ou MPEG-2.
ms.assetid: 8313b83c-5a0a-4aaa-bdc8-58a987c329c7
title: Atributo MF_MT_MPEG_START_TIME_CODE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73b19a041dbcd791359d704b407445779927d0fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764205"
---
# <a name="mf_mt_mpeg_start_time_code-attribute"></a><span data-ttu-id="c7379-103">Atributo de código de hora de início do MF \_ MT \_ MPEG \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="c7379-103">MF\_MT\_MPEG\_START\_TIME\_CODE attribute</span></span>

<span data-ttu-id="c7379-104">O código de hora de início do grupo de imagens (GOP), para um tipo de mídia de vídeo MPEG-1 ou MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="c7379-104">Group-of-pictures (GOP) start time code, for an MPEG-1 or MPEG-2 video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="c7379-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c7379-105">Data type</span></span>

<span data-ttu-id="c7379-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c7379-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c7379-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7379-107">Remarks</span></span>

<span data-ttu-id="c7379-108">Esse atributo corresponde ao membro **dwStartTimeCode** das estruturas [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) e [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="c7379-108">This attribute corresponds to the **dwStartTimeCode** member of the [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) and [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structures.</span></span>

<span data-ttu-id="c7379-109">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c7379-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7379-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7379-110">Requirements</span></span>



| <span data-ttu-id="c7379-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7379-111">Requirement</span></span> | <span data-ttu-id="c7379-112">Valor</span><span class="sxs-lookup"><span data-stu-id="c7379-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c7379-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7379-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c7379-114">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="c7379-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="c7379-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7379-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c7379-116">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c7379-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="c7379-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c7379-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7379-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7379-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7379-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7379-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7379-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c7379-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c7379-121">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="c7379-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="c7379-122">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="c7379-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="c7379-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="c7379-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="c7379-124">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="c7379-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="c7379-125">Atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c7379-125">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 
