---
description: Contém sinalizadores diversos para um tipo de mídia de vídeo MPEG-2.
ms.assetid: 2e1bf3e3-c005-418b-b9fd-1d43c42dad6f
title: Atributo MF_MT_MPEG2_FLAGS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2ef0a0def9c3e5413ec9b9bf7568fcbe9add851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793620"
---
# <a name="mf_mt_mpeg2_flags-attribute"></a><span data-ttu-id="e058e-103">\_Atributo de \_ sinalizadores de MPEG2 do MF MT \_</span><span class="sxs-lookup"><span data-stu-id="e058e-103">MF\_MT\_MPEG2\_FLAGS attribute</span></span>

<span data-ttu-id="e058e-104">Contém sinalizadores diversos para um tipo de mídia de vídeo MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="e058e-104">Contains miscellaneous flags for an MPEG-2 video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="e058e-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e058e-105">Data type</span></span>

<span data-ttu-id="e058e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e058e-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="e058e-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="e058e-107">Remarks</span></span>

<span data-ttu-id="e058e-108">Esse atributo corresponde ao membro **dwFlags** da estrutura [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="e058e-108">This attribute corresponds to the **dwFlags** member of the [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure.</span></span> <span data-ttu-id="e058e-109">Para obter uma lista de sinalizadores válidos, consulte a documentação de **MPEG2VIDEOINFO**.</span><span class="sxs-lookup"><span data-stu-id="e058e-109">For a list of valid flags, see the documentation for **MPEG2VIDEOINFO**.</span></span>

<span data-ttu-id="e058e-110">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="e058e-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e058e-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e058e-111">Requirements</span></span>



| <span data-ttu-id="e058e-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="e058e-112">Requirement</span></span> | <span data-ttu-id="e058e-113">Valor</span><span class="sxs-lookup"><span data-stu-id="e058e-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e058e-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e058e-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e058e-115">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="e058e-115">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="e058e-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e058e-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e058e-117">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e058e-117">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="e058e-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e058e-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="e058e-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e058e-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e058e-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="e058e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e058e-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e058e-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e058e-122">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="e058e-122">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="e058e-123">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="e058e-123">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="e058e-124">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="e058e-124">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="e058e-125">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="e058e-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
