---
description: Taxa de dados aproximada do fluxo de vídeo, em bits por segundo, para um tipo de mídia de vídeo.
ms.assetid: cf9374a7-3688-4a6c-8339-d68c267c9bed
title: Atributo MF_MT_AVG_BITRATE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e4497c58abf8587e72dea47d4f8ac222a1b0692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104370765"
---
# <a name="mf_mt_avg_bitrate-attribute"></a><span data-ttu-id="5992b-103">\_Atributo de \_ média de taxa de bits MF MT \_</span><span class="sxs-lookup"><span data-stu-id="5992b-103">MF\_MT\_AVG\_BITRATE attribute</span></span>

<span data-ttu-id="5992b-104">Taxa de dados aproximada do fluxo de vídeo, em bits por segundo, para um tipo de mídia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5992b-104">Approximate data rate of the video stream, in bits per second, for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="5992b-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="5992b-105">Data type</span></span>

<span data-ttu-id="5992b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5992b-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="5992b-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="5992b-107">Remarks</span></span>

<span data-ttu-id="5992b-108">Esse atributo corresponde ao membro **dwBitRate** das estruturas [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) e [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .</span><span class="sxs-lookup"><span data-stu-id="5992b-108">This attribute corresponds to the **dwBitRate** member of the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) and [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structures.</span></span>

<span data-ttu-id="5992b-109">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="5992b-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5992b-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5992b-110">Requirements</span></span>



| <span data-ttu-id="5992b-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="5992b-111">Requirement</span></span> | <span data-ttu-id="5992b-112">Valor</span><span class="sxs-lookup"><span data-stu-id="5992b-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5992b-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5992b-113">Minimum supported client</span></span><br/> | <span data-ttu-id="5992b-114">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="5992b-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="5992b-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5992b-115">Minimum supported server</span></span><br/> | <span data-ttu-id="5992b-116">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5992b-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="5992b-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5992b-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="5992b-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5992b-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5992b-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="5992b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5992b-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5992b-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5992b-121">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="5992b-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="5992b-122">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="5992b-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="5992b-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="5992b-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="5992b-124">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="5992b-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
