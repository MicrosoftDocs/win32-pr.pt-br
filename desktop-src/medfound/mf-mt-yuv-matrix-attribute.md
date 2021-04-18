---
description: Para tipos de mídia YUV, define a matriz de conversão do espaço de cores YCbCr para o espaço de cores RGB.
ms.assetid: b268d16d-b4cc-4026-9ba7-805cc5409b95
title: Atributo MF_MT_YUV_MATRIX (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0c6976e4652c69b3bddc910dcc536a3d07bf39a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751808"
---
# <a name="mf_mt_yuv_matrix-attribute"></a><span data-ttu-id="c361a-103">\_Atributo de \_ \_ matriz YUV do MF MT</span><span class="sxs-lookup"><span data-stu-id="c361a-103">MF\_MT\_YUV\_MATRIX attribute</span></span>

<span data-ttu-id="c361a-104">Para tipos de mídia YUV, define a matriz de conversão do espaço de cores Y'Cb'Cr para o espaço de cores R'G'B.</span><span class="sxs-lookup"><span data-stu-id="c361a-104">For YUV media types, defines the conversion matrix from the Y'Cb'Cr' color space to the R'G'B' color space.</span></span>

## <a name="data-type"></a><span data-ttu-id="c361a-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c361a-105">Data type</span></span>

<span data-ttu-id="c361a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c361a-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c361a-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="c361a-107">Remarks</span></span>

<span data-ttu-id="c361a-108">O valor desse atributo é um membro da enumeração [**MFVideoTransferMatrix**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideotransfermatrix) .</span><span class="sxs-lookup"><span data-stu-id="c361a-108">The value of this attribute is a member of the [**MFVideoTransferMatrix**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideotransfermatrix) enumeration.</span></span>

<span data-ttu-id="c361a-109">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c361a-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c361a-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c361a-110">Requirements</span></span>



| <span data-ttu-id="c361a-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="c361a-111">Requirement</span></span> | <span data-ttu-id="c361a-112">Valor</span><span class="sxs-lookup"><span data-stu-id="c361a-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c361a-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c361a-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c361a-114">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="c361a-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="c361a-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c361a-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c361a-116">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c361a-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="c361a-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c361a-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="c361a-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c361a-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c361a-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="c361a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c361a-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c361a-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c361a-121">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="c361a-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="c361a-122">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="c361a-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="c361a-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="c361a-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="c361a-124">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="c361a-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="c361a-125">Informações de cores estendidas</span><span class="sxs-lookup"><span data-stu-id="c361a-125">Extended Color Information</span></span>](extended-color-information.md)
</dt> </dl>

 

 




