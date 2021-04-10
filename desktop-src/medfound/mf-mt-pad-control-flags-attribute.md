---
description: Especifica a taxa de proporção do retângulo de saída para um tipo de mídia de vídeo.
ms.assetid: d7fec5fb-a1fe-4cc9-aa27-a3af0456ea8d
title: Atributo MF_MT_PAD_CONTROL_FLAGS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02610b54b84c2470eba19eaa696f633243df347f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169762"
---
# <a name="mf_mt_pad_control_flags-attribute"></a><span data-ttu-id="0b9d4-103">\_Atributo de \_ sinalizador de controle de painel \_ \_ do MF MT</span><span class="sxs-lookup"><span data-stu-id="0b9d4-103">MF\_MT\_PAD\_CONTROL\_FLAGS attribute</span></span>

<span data-ttu-id="0b9d4-104">Especifica a taxa de proporção do retângulo de saída para um tipo de mídia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0b9d4-104">Specifies the aspect ratio of the output rectangle for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="0b9d4-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="0b9d4-105">Data type</span></span>

<span data-ttu-id="0b9d4-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0b9d4-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="0b9d4-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b9d4-107">Remarks</span></span>

<span data-ttu-id="0b9d4-108">O valor desse atributo é um membro da enumeração [**MFVideoPadFlags**](/windows/desktop/api/mfapi/ne-mfapi-mfvideopadflags) .</span><span class="sxs-lookup"><span data-stu-id="0b9d4-108">The value of this attribute is a member of the [**MFVideoPadFlags**](/windows/desktop/api/mfapi/ne-mfapi-mfvideopadflags) enumeration.</span></span>

<span data-ttu-id="0b9d4-109">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="0b9d4-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b9d4-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b9d4-110">Requirements</span></span>



| <span data-ttu-id="0b9d4-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b9d4-111">Requirement</span></span> | <span data-ttu-id="0b9d4-112">Valor</span><span class="sxs-lookup"><span data-stu-id="0b9d4-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0b9d4-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b9d4-113">Minimum supported client</span></span><br/> | <span data-ttu-id="0b9d4-114">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="0b9d4-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="0b9d4-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b9d4-115">Minimum supported server</span></span><br/> | <span data-ttu-id="0b9d4-116">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0b9d4-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="0b9d4-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0b9d4-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b9d4-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b9d4-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b9d4-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b9d4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b9d4-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0b9d4-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0b9d4-121">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="0b9d4-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="0b9d4-122">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="0b9d4-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="0b9d4-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="0b9d4-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="0b9d4-124">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="0b9d4-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




