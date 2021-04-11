---
description: Descreve como os quadros em um tipo de mídia de vídeo são entrelaçados.
ms.assetid: 19aa0147-ac49-4a2e-ac75-e967fec9ca68
title: Atributo MF_MT_INTERLACE_MODE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1826978c39ff8cd80b2aa66b91161ee8b476944f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090568"
---
# <a name="mf_mt_interlace_mode-attribute"></a><span data-ttu-id="dae9e-103">\_Atributo do \_ modo de entrelaçamento MF MT \_</span><span class="sxs-lookup"><span data-stu-id="dae9e-103">MF\_MT\_INTERLACE\_MODE attribute</span></span>

<span data-ttu-id="dae9e-104">Descreve como os quadros em um tipo de mídia de vídeo são entrelaçados.</span><span class="sxs-lookup"><span data-stu-id="dae9e-104">Describes how the frames in a video media type are interlaced.</span></span>

## <a name="data-type"></a><span data-ttu-id="dae9e-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="dae9e-105">Data type</span></span>

<span data-ttu-id="dae9e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="dae9e-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="dae9e-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="dae9e-107">Remarks</span></span>

<span data-ttu-id="dae9e-108">O valor desse atributo é um membro da enumeração [**MFVideoInterlaceMode**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideointerlacemode) .</span><span class="sxs-lookup"><span data-stu-id="dae9e-108">The value of this attribute is a member of the [**MFVideoInterlaceMode**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideointerlacemode) enumeration.</span></span>

<span data-ttu-id="dae9e-109">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="dae9e-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="dae9e-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dae9e-110">Requirements</span></span>



| <span data-ttu-id="dae9e-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="dae9e-111">Requirement</span></span> | <span data-ttu-id="dae9e-112">Valor</span><span class="sxs-lookup"><span data-stu-id="dae9e-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dae9e-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dae9e-113">Minimum supported client</span></span><br/> | <span data-ttu-id="dae9e-114">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="dae9e-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="dae9e-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dae9e-115">Minimum supported server</span></span><br/> | <span data-ttu-id="dae9e-116">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="dae9e-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="dae9e-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dae9e-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="dae9e-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="dae9e-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dae9e-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="dae9e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dae9e-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dae9e-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="dae9e-121">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="dae9e-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="dae9e-122">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="dae9e-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="dae9e-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="dae9e-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="dae9e-124">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="dae9e-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="dae9e-125">Entrelaçamento de vídeo</span><span class="sxs-lookup"><span data-stu-id="dae9e-125">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




