---
description: Especifica se um quadro de vídeo desentrelaçado foi derivado do campo superior ou do campo inferior.
ms.assetid: 3710ab94-afb3-44d3-a680-b4a716810ec1
title: Atributo MFSampleExtension_DerivedFromTopField (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f90a67edf0b08337748bc118b0aa4ff024ec0ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761058"
---
# <a name="mfsampleextension_derivedfromtopfield-attribute"></a><span data-ttu-id="a32c5-103">\_Atributo MFSampleExtension DerivedFromTopField</span><span class="sxs-lookup"><span data-stu-id="a32c5-103">MFSampleExtension\_DerivedFromTopField attribute</span></span>

<span data-ttu-id="a32c5-104">Especifica se um quadro de vídeo desentrelaçado foi derivado do campo superior ou do campo inferior.</span><span class="sxs-lookup"><span data-stu-id="a32c5-104">Specifies whether a deinterlaced video frame was derived from the upper field or the lower field.</span></span> <span data-ttu-id="a32c5-105">Esse atributo se aplica a exemplos de mídia.</span><span class="sxs-lookup"><span data-stu-id="a32c5-105">This attribute applies to media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="a32c5-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a32c5-106">Data type</span></span>

<span data-ttu-id="a32c5-107">**Bool** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="a32c5-107">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="a32c5-108">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="a32c5-108">Get/set</span></span>

<span data-ttu-id="a32c5-109">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="a32c5-109">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="a32c5-110">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="a32c5-110">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="a32c5-111">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="a32c5-111">Applies to</span></span>

[<span data-ttu-id="a32c5-112">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="a32c5-112">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="a32c5-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a32c5-113">Remarks</span></span>

<span data-ttu-id="a32c5-114">Este atributo é válido somente para amostras desentrelaçadas.</span><span class="sxs-lookup"><span data-stu-id="a32c5-114">This attribute is valid for deinterlaced samples only.</span></span> <span data-ttu-id="a32c5-115">Defina esse atributo se o quadro tiver sido desentrelaçado interpolando um dos campos.</span><span class="sxs-lookup"><span data-stu-id="a32c5-115">Set this attribute if the frame was deinterlaced by interpolating one of the fields.</span></span>

<span data-ttu-id="a32c5-116">Se o valor for **true**, o campo inferior foi interpolado a partir do campo superior.</span><span class="sxs-lookup"><span data-stu-id="a32c5-116">If the value is **TRUE**, the lower field was interpolated from the upper field.</span></span> <span data-ttu-id="a32c5-117">Se o valor for **false**, o campo superior foi interpolado a partir do campo inferior.</span><span class="sxs-lookup"><span data-stu-id="a32c5-117">If the value is **FALSE**, the upper field was interpolated from the lower field.</span></span>

<span data-ttu-id="a32c5-118">Se o atributo não estiver definido, o quadro não foi desentrelaçado.</span><span class="sxs-lookup"><span data-stu-id="a32c5-118">If the attribute is not set, the frame has not been deinterlaced.</span></span> <span data-ttu-id="a32c5-119">O quadro é um quadro progressivo real ou é um quadro entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="a32c5-119">The frame is either a true progressive frame, or it is an interlaced frame.</span></span>

<span data-ttu-id="a32c5-120">Esse atributo é informativo.</span><span class="sxs-lookup"><span data-stu-id="a32c5-120">This attribute is informational.</span></span> <span data-ttu-id="a32c5-121">Um desentrelaçador de software pode definir esse atributo.</span><span class="sxs-lookup"><span data-stu-id="a32c5-121">A software deinterlacer could set this attribute.</span></span> <span data-ttu-id="a32c5-122">Se esse atributo for definido, ele fornecerá uma dica de que você pode recuperar o campo original descartando as linhas de digitalização interpoladas.</span><span class="sxs-lookup"><span data-stu-id="a32c5-122">If this attribute is set, it provides a hint that you can recover the original field by dropping the interpolated scan lines.</span></span> <span data-ttu-id="a32c5-123">Por exemplo, se o atributo for **true**, você poderá recuperar o campo superior original descartando o campo inferior interpolado.</span><span class="sxs-lookup"><span data-stu-id="a32c5-123">For example, if the attribute is **TRUE**, you can recover the original upper field by dropping the interpolated lower field.</span></span>

<span data-ttu-id="a32c5-124">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="a32c5-124">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a32c5-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a32c5-125">Requirements</span></span>



| <span data-ttu-id="a32c5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a32c5-126">Requirement</span></span> | <span data-ttu-id="a32c5-127">Valor</span><span class="sxs-lookup"><span data-stu-id="a32c5-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a32c5-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a32c5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a32c5-129">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="a32c5-129">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="a32c5-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a32c5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a32c5-131">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a32c5-131">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="a32c5-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a32c5-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a32c5-133"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a32c5-133"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a32c5-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="a32c5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a32c5-135">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a32c5-135">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a32c5-136">Atributos de exemplo</span><span class="sxs-lookup"><span data-stu-id="a32c5-136">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="a32c5-137">Amostras de mídia</span><span class="sxs-lookup"><span data-stu-id="a32c5-137">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="a32c5-138">Entrelaçamento de vídeo</span><span class="sxs-lookup"><span data-stu-id="a32c5-138">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




