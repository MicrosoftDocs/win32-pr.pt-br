---
description: Especifica o tamanho de cada amostra, em bytes, em um tipo de mídia.
ms.assetid: 4c28f73d-ff40-4eb9-a45f-57a60df719c6
title: Atributo MF_MT_SAMPLE_SIZE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bb897524dac5f73f4d4553f8e77e02ef473f611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784045"
---
# <a name="mf_mt_sample_size-attribute"></a><span data-ttu-id="482f4-103">\_Atributo de \_ tamanho de amostra MF MT \_</span><span class="sxs-lookup"><span data-stu-id="482f4-103">MF\_MT\_SAMPLE\_SIZE attribute</span></span>

<span data-ttu-id="482f4-104">Especifica o tamanho de cada amostra, em bytes, em um tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="482f4-104">Specifies the size of each sample, in bytes, in a media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="482f4-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="482f4-105">Data type</span></span>

<span data-ttu-id="482f4-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="482f4-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="482f4-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="482f4-107">Remarks</span></span>

<span data-ttu-id="482f4-108">Esse atributo será válido somente se o atributo de [**\_ \_ \_ \_ exemplos de tamanho fixo MF MT**](mf-mt-fixed-size-samples-attribute.md) for **true**.</span><span class="sxs-lookup"><span data-stu-id="482f4-108">This attribute is valid only if the [**MF\_MT\_FIXED\_SIZE\_SAMPLES**](mf-mt-fixed-size-samples-attribute.md) attribute is **TRUE**.</span></span>

<span data-ttu-id="482f4-109">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="482f4-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="482f4-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="482f4-110">Requirements</span></span>



| <span data-ttu-id="482f4-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="482f4-111">Requirement</span></span> | <span data-ttu-id="482f4-112">Valor</span><span class="sxs-lookup"><span data-stu-id="482f4-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="482f4-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="482f4-113">Minimum supported client</span></span><br/> | <span data-ttu-id="482f4-114">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="482f4-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="482f4-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="482f4-115">Minimum supported server</span></span><br/> | <span data-ttu-id="482f4-116">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="482f4-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="482f4-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="482f4-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="482f4-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="482f4-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="482f4-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="482f4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="482f4-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="482f4-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="482f4-121">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="482f4-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="482f4-122">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="482f4-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="482f4-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="482f4-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="482f4-124">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="482f4-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




