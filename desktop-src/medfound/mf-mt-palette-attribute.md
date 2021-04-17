---
description: Contém as entradas da paleta para um tipo de mídia de vídeo. Use esse atributo para formatos de vídeo palettized, como RGB 8.
ms.assetid: 3efc124b-073e-4c48-9550-c100e29f2d6f
title: Atributo MF_MT_PALETTE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45dcfc596ae463cf642cc462da1c73dc641356d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748914"
---
# <a name="mf_mt_palette-attribute"></a><span data-ttu-id="c9733-104">\_Atributo de \_ paleta MF MT</span><span class="sxs-lookup"><span data-stu-id="c9733-104">MF\_MT\_PALETTE attribute</span></span>

<span data-ttu-id="c9733-105">Contém as entradas da paleta para um tipo de mídia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c9733-105">Contains the palette entries for a video media type.</span></span> <span data-ttu-id="c9733-106">Use esse atributo para formatos de vídeo palettized, como RGB 8.</span><span class="sxs-lookup"><span data-stu-id="c9733-106">Use this attribute for palettized video formats, such as RGB 8.</span></span>

## <a name="data-type"></a><span data-ttu-id="c9733-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c9733-107">Data type</span></span>

<span data-ttu-id="c9733-108">Matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="c9733-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="c9733-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9733-109">Remarks</span></span>

<span data-ttu-id="c9733-110">Os dados de atributo são uma matriz de uniões [**MFPaletteEntry**](/windows/win32/api/mfobjects/ns-mfobjects-mfpaletteentry) .</span><span class="sxs-lookup"><span data-stu-id="c9733-110">The attribute data is an array of [**MFPaletteEntry**](/windows/win32/api/mfobjects/ns-mfobjects-mfpaletteentry) unions.</span></span>

<span data-ttu-id="c9733-111">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c9733-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9733-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9733-112">Requirements</span></span>



| <span data-ttu-id="c9733-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9733-113">Requirement</span></span> | <span data-ttu-id="c9733-114">Valor</span><span class="sxs-lookup"><span data-stu-id="c9733-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c9733-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9733-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c9733-116">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="c9733-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="c9733-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9733-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c9733-118">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c9733-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="c9733-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c9733-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9733-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9733-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9733-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9733-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9733-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c9733-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c9733-123">**IMFAttributes:: getBlob**</span><span class="sxs-lookup"><span data-stu-id="c9733-123">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="c9733-124">**IMFAttributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="c9733-124">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="c9733-125">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="c9733-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="c9733-126">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="c9733-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




