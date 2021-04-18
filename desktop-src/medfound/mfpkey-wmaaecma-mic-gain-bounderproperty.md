---
description: Especifica se o DSP de captura de voz aplica o limite de lucro do microfone.
ms.assetid: b9f0bcc7-57ab-4339-bf1d-2b12c8744f01
title: Propriedade MFPKEY_WMAAECMA_MIC_GAIN_BOUNDER (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c1b09f2095f5accb44e4e0edaff2b8c94941d3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760600"
---
# <a name="mfpkey_wmaaecma_mic_gain_bounder-property"></a><span data-ttu-id="b48c3-103">\_Propriedade do \_ \_ \_ limitador de MFPKEY WMAAECMA MIC</span><span class="sxs-lookup"><span data-stu-id="b48c3-103">MFPKEY\_WMAAECMA\_MIC\_GAIN\_BOUNDER Property</span></span>

<span data-ttu-id="b48c3-104">Especifica se o DSP de captura de voz aplica o limite de lucro do microfone.</span><span class="sxs-lookup"><span data-stu-id="b48c3-104">Specifies whether the Voice Capture DSP applies microphone gain bounding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="b48c3-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="b48c3-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="b48c3-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="b48c3-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="b48c3-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="b48c3-107">Data Type</span></span>

<span data-ttu-id="b48c3-108">BOOL do VT \_</span><span class="sxs-lookup"><span data-stu-id="b48c3-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="b48c3-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="b48c3-109">Default Value</span></span>

<span data-ttu-id="b48c3-110">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="b48c3-110">VARIANT\_TRUE</span></span>

## <a name="applies-to"></a><span data-ttu-id="b48c3-111">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="b48c3-111">Applies To</span></span>

-   [<span data-ttu-id="b48c3-112">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="b48c3-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="b48c3-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b48c3-113">Remarks</span></span>

<span data-ttu-id="b48c3-114">O limite de lucro do microfone garante que o microfone tenha o nível correto de lucro.</span><span class="sxs-lookup"><span data-stu-id="b48c3-114">Microphone gain bounding ensures that the microphone has the correct level of gain.</span></span> <span data-ttu-id="b48c3-115">Se o lucro for muito alto, o sinal capturado poderá ser saturado e será recortado.</span><span class="sxs-lookup"><span data-stu-id="b48c3-115">If gain is too high, the captured signal might be saturated and will be clipped.</span></span> <span data-ttu-id="b48c3-116">O recorte é um efeito não linear, o que fará com que o algoritmo de cancelamento de eco acústico (AEC) falhe.</span><span class="sxs-lookup"><span data-stu-id="b48c3-116">Clipping is a non-linear effect, which will cause the acoustic echo cancellation (AEC) algorithm to fail.</span></span> <span data-ttu-id="b48c3-117">Se o lucro for muito baixo, a taxa de sinal para ruído é baixa, o que também pode fazer com que o algoritmo AEC falhe ou não funcione bem.</span><span class="sxs-lookup"><span data-stu-id="b48c3-117">If the gain is too low, the signal-to-noise ratio is low, which can also cause the AEC algorithm to fail or not perform well.</span></span>

<span data-ttu-id="b48c3-118">Essa propriedade pode ter os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="b48c3-118">This property can have the following values.</span></span>



| <span data-ttu-id="b48c3-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b48c3-119">Value</span></span>          | <span data-ttu-id="b48c3-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="b48c3-120">Description</span></span>                       |
|----------------|-----------------------------------|
| <span data-ttu-id="b48c3-121">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="b48c3-121">VARIANT\_TRUE</span></span>  | <span data-ttu-id="b48c3-122">Habilitar limite de lucro de microfone.</span><span class="sxs-lookup"><span data-stu-id="b48c3-122">Enable microphone gain bounding.</span></span>  |
| <span data-ttu-id="b48c3-123">VARIANTE \_ falso</span><span class="sxs-lookup"><span data-stu-id="b48c3-123">VARIANT\_FALSE</span></span> | <span data-ttu-id="b48c3-124">Desabilitar limite de lucro de microfone.</span><span class="sxs-lookup"><span data-stu-id="b48c3-124">Disable microphone gain bounding.</span></span> |



 

<span data-ttu-id="b48c3-125">O valor padrão dessa propriedade é VARIANT \_ true (Enabled).</span><span class="sxs-lookup"><span data-stu-id="b48c3-125">The default value of this property is VARIANT\_TRUE (enabled).</span></span>

<span data-ttu-id="b48c3-126">O limite de lucro do microfone é aplicado somente quando o DSP opera no modo de origem.</span><span class="sxs-lookup"><span data-stu-id="b48c3-126">Microphone gain bounding is applies only when the DSP operates in source mode.</span></span> <span data-ttu-id="b48c3-127">No modo de filtro, o aplicativo deve garantir que o microfone tenha o nível de lucro correto.</span><span class="sxs-lookup"><span data-stu-id="b48c3-127">In filter mode, the application must ensure that the microphone has the correct gain level.</span></span>

## <a name="requirements"></a><span data-ttu-id="b48c3-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b48c3-128">Requirements</span></span>



| <span data-ttu-id="b48c3-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="b48c3-129">Requirement</span></span> | <span data-ttu-id="b48c3-130">Valor</span><span class="sxs-lookup"><span data-stu-id="b48c3-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b48c3-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b48c3-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b48c3-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b48c3-132">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b48c3-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b48c3-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b48c3-134">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b48c3-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b48c3-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b48c3-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="b48c3-136"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b48c3-136"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b48c3-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="b48c3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b48c3-138">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b48c3-138">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="b48c3-139">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="b48c3-139">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
