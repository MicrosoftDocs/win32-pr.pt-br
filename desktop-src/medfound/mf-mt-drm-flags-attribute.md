---
description: Especifica se um tipo de mídia de vídeo requer a imposição da proteção de cópia.
ms.assetid: fb12ba38-a4f4-44fe-bf31-e731c56bb145
title: Atributo MF_MT_DRM_FLAGS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa8ef771cb72050b2273d822ce799092ce51e64c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764161"
---
# <a name="mf_mt_drm_flags-attribute"></a><span data-ttu-id="6254c-103">\_Atributo de \_ \_ sinalizadores DRM do MF MT</span><span class="sxs-lookup"><span data-stu-id="6254c-103">MF\_MT\_DRM\_FLAGS attribute</span></span>

<span data-ttu-id="6254c-104">Especifica se um tipo de mídia de vídeo requer a imposição da proteção de cópia.</span><span class="sxs-lookup"><span data-stu-id="6254c-104">Specifies whether a video media type requires the enforcement of copy protection.</span></span>

## <a name="data-type"></a><span data-ttu-id="6254c-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="6254c-105">Data type</span></span>

<span data-ttu-id="6254c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="6254c-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="6254c-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="6254c-107">Remarks</span></span>

<span data-ttu-id="6254c-108">O valor desse atributo é um membro da enumeração [**MFVideoDRMFlags**](/windows/desktop/api/mfapi/ne-mfapi-mfvideodrmflags) .</span><span class="sxs-lookup"><span data-stu-id="6254c-108">The value of this attribute is a member of the [**MFVideoDRMFlags**](/windows/desktop/api/mfapi/ne-mfapi-mfvideodrmflags) enumeration.</span></span>

<span data-ttu-id="6254c-109">Esse atributo fornece uma dica para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6254c-109">This attribute provides a hint to the application.</span></span> <span data-ttu-id="6254c-110">Ele não é usado para impor a proteção de cópia ou para especificar o mecanismo de proteção de cópia.</span><span class="sxs-lookup"><span data-stu-id="6254c-110">It is not used to enforce copy protection or to specify the copy protection mechanism.</span></span>

<span data-ttu-id="6254c-111">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="6254c-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="6254c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6254c-112">Requirements</span></span>



| <span data-ttu-id="6254c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="6254c-113">Requirement</span></span> | <span data-ttu-id="6254c-114">Valor</span><span class="sxs-lookup"><span data-stu-id="6254c-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6254c-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6254c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6254c-116">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="6254c-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="6254c-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6254c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6254c-118">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="6254c-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="6254c-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6254c-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="6254c-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6254c-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6254c-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="6254c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6254c-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6254c-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6254c-123">MF \_ SD \_ protegido</span><span class="sxs-lookup"><span data-stu-id="6254c-123">MF\_SD\_PROTECTED</span></span>](mf-sd-protected-attribute.md)
</dt> <dt>

[<span data-ttu-id="6254c-124">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="6254c-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="6254c-125">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="6254c-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="6254c-126">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="6254c-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="6254c-127">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="6254c-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




