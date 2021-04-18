---
description: Contém o cabeçalho de sequência MPEG-1 ou MPEG-2 para um tipo de mídia de vídeo.
ms.assetid: 17b7f76c-404c-4aa9-9746-1488fee027f2
title: Atributo MF_MT_MPEG_SEQUENCE_HEADER (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4003137ec4d2942bc95f56b2ce54644eb7b678d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783744"
---
# <a name="mf_mt_mpeg_sequence_header-attribute"></a><span data-ttu-id="733ae-103">\_Atributo de \_ \_ cabeçalho de sequência MF MT MPEG \_</span><span class="sxs-lookup"><span data-stu-id="733ae-103">MF\_MT\_MPEG\_SEQUENCE\_HEADER attribute</span></span>

<span data-ttu-id="733ae-104">Contém o cabeçalho de sequência MPEG-1 ou MPEG-2 para um tipo de mídia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="733ae-104">Contains the MPEG-1 or MPEG-2 sequence header for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="733ae-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="733ae-105">Data type</span></span>

<span data-ttu-id="733ae-106">Matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="733ae-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="733ae-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="733ae-107">Remarks</span></span>

<span data-ttu-id="733ae-108">Esse atributo corresponde ao membro **dwSequenceHeader** da estrutura [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) ou ao membro **bSequenceHeader** da estrutura [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="733ae-108">This attribute corresponds to the **dwSequenceHeader** member of the [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure, or the **bSequenceHeader** member of the [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) structure.</span></span>

<span data-ttu-id="733ae-109">Para o vídeo H264 e h265, o BLOB contém [unidades de nal](https://en.wikipedia.org/wiki/Network_Abstraction_Layer) concatenadas no formato anexo B, juntamente com seus códigos de início.</span><span class="sxs-lookup"><span data-stu-id="733ae-109">For h264 and h265 video, the blob contains concatenated [NAL units](https://en.wikipedia.org/wiki/Network_Abstraction_Layer) in Annex B format, along with their start codes.</span></span> <span data-ttu-id="733ae-110">Especificamente, para o vídeo H264, eles são SPS & unidades de NAL PPS.</span><span class="sxs-lookup"><span data-stu-id="733ae-110">Specifically, for h264 video they are SPS & PPS NAL units.</span></span> <span data-ttu-id="733ae-111">Para h265, eles são VPSs, SPS & PPS.</span><span class="sxs-lookup"><span data-stu-id="733ae-111">For h265 they are VPS, SPS & PPS.</span></span>

<span data-ttu-id="733ae-112">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="733ae-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="733ae-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="733ae-113">Requirements</span></span>



| <span data-ttu-id="733ae-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="733ae-114">Requirement</span></span> | <span data-ttu-id="733ae-115">Valor</span><span class="sxs-lookup"><span data-stu-id="733ae-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="733ae-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="733ae-116">Minimum supported client</span></span><br/> | <span data-ttu-id="733ae-117">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="733ae-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="733ae-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="733ae-118">Minimum supported server</span></span><br/> | <span data-ttu-id="733ae-119">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="733ae-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="733ae-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="733ae-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="733ae-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="733ae-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="733ae-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="733ae-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="733ae-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="733ae-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="733ae-124">**IMFAttributes:: getBlob**</span><span class="sxs-lookup"><span data-stu-id="733ae-124">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="733ae-125">**IMFAttributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="733ae-125">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="733ae-126">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="733ae-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="733ae-127">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="733ae-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
