---
description: Especifica para um tipo de mídia se os exemplos têm um tamanho fixo.
ms.assetid: 2d67864a-fd2f-400d-8a1e-e71dc1920593
title: Atributo MF_MT_FIXED_SIZE_SAMPLES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d1bb5bdd4e1330e4744902ed1b37cc55b7a67a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756072"
---
# <a name="mf_mt_fixed_size_samples-attribute"></a><span data-ttu-id="050dc-103">\_Atributo de \_ \_ exemplos de tamanho fixo MF MT \_</span><span class="sxs-lookup"><span data-stu-id="050dc-103">MF\_MT\_FIXED\_SIZE\_SAMPLES attribute</span></span>

<span data-ttu-id="050dc-104">Especifica para um tipo de mídia se os exemplos têm um tamanho fixo.</span><span class="sxs-lookup"><span data-stu-id="050dc-104">Specifies for a media type whether the samples have a fixed size.</span></span>

## <a name="data-type"></a><span data-ttu-id="050dc-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="050dc-105">Data type</span></span>

<span data-ttu-id="050dc-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="050dc-106">**UINT32**</span></span>

<span data-ttu-id="050dc-107">Tratar como um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="050dc-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="050dc-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="050dc-108">Remarks</span></span>

<span data-ttu-id="050dc-109">Se esse atributo for **true**, todas as amostras no fluxo serão do mesmo tamanho (em bytes).</span><span class="sxs-lookup"><span data-stu-id="050dc-109">If this attribute is **TRUE**, every sample in the stream is the same size (in bytes).</span></span> <span data-ttu-id="050dc-110">Caso contrário, os exemplos podem variar em tamanho.</span><span class="sxs-lookup"><span data-stu-id="050dc-110">Otherwise, samples might vary in size.</span></span>

<span data-ttu-id="050dc-111">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="050dc-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="050dc-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="050dc-112">Requirements</span></span>



| <span data-ttu-id="050dc-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="050dc-113">Requirement</span></span> | <span data-ttu-id="050dc-114">Valor</span><span class="sxs-lookup"><span data-stu-id="050dc-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="050dc-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="050dc-115">Minimum supported client</span></span><br/> | <span data-ttu-id="050dc-116">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="050dc-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="050dc-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="050dc-117">Minimum supported server</span></span><br/> | <span data-ttu-id="050dc-118">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="050dc-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="050dc-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="050dc-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="050dc-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="050dc-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="050dc-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="050dc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="050dc-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="050dc-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="050dc-123">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="050dc-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="050dc-124">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="050dc-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="050dc-125">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="050dc-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="050dc-126">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="050dc-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




