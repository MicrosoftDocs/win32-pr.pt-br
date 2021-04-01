---
description: Especifica a taxa de quadros no fluxo de saída do codificador, em quadros por segundo.
ms.assetid: 72e16c7d-977e-4269-9576-afc789e31826
title: Propriedade AVEncVideoOutputFrameRate (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad4cb675c266d146936a3402934e51486ded5b02
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645832"
---
# <a name="avencvideooutputframerate-property"></a><span data-ttu-id="7fc12-103">Propriedade AVEncVideoOutputFrameRate</span><span class="sxs-lookup"><span data-stu-id="7fc12-103">AVEncVideoOutputFrameRate property</span></span>

<span data-ttu-id="7fc12-104">Especifica a taxa de quadros no fluxo de saída do codificador, em quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="7fc12-104">Specifies the frame rate on the encoder's output stream, in frames per second.</span></span>

<span data-ttu-id="7fc12-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="7fc12-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="7fc12-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="7fc12-106">Data type</span></span>

<span data-ttu-id="7fc12-107">**UINT64** (**VT \_ UI8**)</span><span class="sxs-lookup"><span data-stu-id="7fc12-107">**UINT64** (**VT\_UI8**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="7fc12-108">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="7fc12-108">Property GUID</span></span>

<span data-ttu-id="7fc12-109">**CODECAPI \_ AVEncVideoOutputFrameRate**</span><span class="sxs-lookup"><span data-stu-id="7fc12-109">**CODECAPI\_AVEncVideoOutputFrameRate**</span></span>

## <a name="property-value"></a><span data-ttu-id="7fc12-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7fc12-110">Property value</span></span>

<span data-ttu-id="7fc12-111">O valor dessa propriedade é uma razão que define a taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="7fc12-111">The value of this property is a ratio that defines the frame rate.</span></span> <span data-ttu-id="7fc12-112">Os bits superiores de 32 contêm o numerador e os bits inferiores de 32 contêm o denominador.</span><span class="sxs-lookup"><span data-stu-id="7fc12-112">The upper 32 bits contain the numerator, and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="7fc12-113">A tabela a seguir mostra as taxas de quadros comuns, em quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="7fc12-113">The following table shows common frame rates, in frames per second.</span></span>



| <span data-ttu-id="7fc12-114">Taxa de quadros</span><span class="sxs-lookup"><span data-stu-id="7fc12-114">Frame rate</span></span> | <span data-ttu-id="7fc12-115">Proporção</span><span class="sxs-lookup"><span data-stu-id="7fc12-115">Ratio</span></span>      |
|------------|------------|
| <span data-ttu-id="7fc12-116">23,97</span><span class="sxs-lookup"><span data-stu-id="7fc12-116">23.97</span></span>      | <span data-ttu-id="7fc12-117">24000/1001</span><span class="sxs-lookup"><span data-stu-id="7fc12-117">24000/1001</span></span> |
| <span data-ttu-id="7fc12-118">24</span><span class="sxs-lookup"><span data-stu-id="7fc12-118">24</span></span>         | <span data-ttu-id="7fc12-119">24/1</span><span class="sxs-lookup"><span data-stu-id="7fc12-119">24/1</span></span>       |
| <span data-ttu-id="7fc12-120">25</span><span class="sxs-lookup"><span data-stu-id="7fc12-120">25</span></span>         | <span data-ttu-id="7fc12-121">25/1</span><span class="sxs-lookup"><span data-stu-id="7fc12-121">25/1</span></span>       |
| <span data-ttu-id="7fc12-122">29,97</span><span class="sxs-lookup"><span data-stu-id="7fc12-122">29.97</span></span>      | <span data-ttu-id="7fc12-123">30000/1001</span><span class="sxs-lookup"><span data-stu-id="7fc12-123">30000/1001</span></span> |
| <span data-ttu-id="7fc12-124">30</span><span class="sxs-lookup"><span data-stu-id="7fc12-124">30</span></span>         | <span data-ttu-id="7fc12-125">30/1</span><span class="sxs-lookup"><span data-stu-id="7fc12-125">30/1</span></span>       |
| <span data-ttu-id="7fc12-126">50</span><span class="sxs-lookup"><span data-stu-id="7fc12-126">50</span></span>         | <span data-ttu-id="7fc12-127">50/1</span><span class="sxs-lookup"><span data-stu-id="7fc12-127">50/1</span></span>       |
| <span data-ttu-id="7fc12-128">59,94</span><span class="sxs-lookup"><span data-stu-id="7fc12-128">59.94</span></span>      | <span data-ttu-id="7fc12-129">60000/1001</span><span class="sxs-lookup"><span data-stu-id="7fc12-129">60000/1001</span></span> |
| <span data-ttu-id="7fc12-130">60</span><span class="sxs-lookup"><span data-stu-id="7fc12-130">60</span></span>         | <span data-ttu-id="7fc12-131">60/1</span><span class="sxs-lookup"><span data-stu-id="7fc12-131">60/1</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="7fc12-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="7fc12-132">Remarks</span></span>

<span data-ttu-id="7fc12-133">Os aplicativos podem definir essa propriedade para especificar a taxa de quadros de saída.</span><span class="sxs-lookup"><span data-stu-id="7fc12-133">Applications can set this property to specify the output frame rate.</span></span> <span data-ttu-id="7fc12-134">Os codificadores também podem retornar essa propriedade como um recurso.</span><span class="sxs-lookup"><span data-stu-id="7fc12-134">Encoders can also return this property as a capability.</span></span> <span data-ttu-id="7fc12-135">Dependendo do codificador, o valor pode ser restrito à taxa de quadros de entrada.</span><span class="sxs-lookup"><span data-stu-id="7fc12-135">Depending on the encoder, the value might be restricted to the input frame rate.</span></span> <span data-ttu-id="7fc12-136">Caso contrário, o codificador será capaz de converter a taxa de quadros internamente.</span><span class="sxs-lookup"><span data-stu-id="7fc12-136">If not, the encoder is able to convert the frame rate internally.</span></span> <span data-ttu-id="7fc12-137">Consulte a [**Propriedade AVEncVideoOutputFrameRateConversion**](avencvideooutputframerateconversion-property.md).</span><span class="sxs-lookup"><span data-stu-id="7fc12-137">See [**AVEncVideoOutputFrameRateConversion Property**](avencvideooutputframerateconversion-property.md).</span></span>

<span data-ttu-id="7fc12-138">Essa propriedade também é usada com [codificadores de câmera H. 264 UVC 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span><span class="sxs-lookup"><span data-stu-id="7fc12-138">This property is also used with [H.264 UVC 1.5 camera encoders](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span></span>

## <a name="requirements"></a><span data-ttu-id="7fc12-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fc12-139">Requirements</span></span>



| <span data-ttu-id="7fc12-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fc12-140">Requirement</span></span> | <span data-ttu-id="7fc12-141">Valor</span><span class="sxs-lookup"><span data-stu-id="7fc12-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7fc12-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7fc12-142">Minimum supported client</span></span><br/> | <span data-ttu-id="7fc12-143">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="7fc12-143">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="7fc12-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7fc12-144">Minimum supported server</span></span><br/> | <span data-ttu-id="7fc12-145">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="7fc12-145">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="7fc12-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7fc12-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fc12-147"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fc12-147"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fc12-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="7fc12-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fc12-149">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="7fc12-149">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="7fc12-150">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="7fc12-150">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

