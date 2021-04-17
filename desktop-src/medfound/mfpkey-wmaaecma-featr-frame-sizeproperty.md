---
description: Especifica o tamanho do quadro de áudio usado pelo DSP de captura de voz.
ms.assetid: b414ac34-c60a-4f43-924f-43431d6ba25f
title: Propriedade MFPKEY_WMAAECMA_FEATR_FRAME_SIZE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5623cf3d26b968c7e7745fa0c01c69c034505cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761211"
---
# <a name="mfpkey_wmaaecma_featr_frame_size-property"></a><span data-ttu-id="f4836-103">\_ \_ \_ Propriedade tamanho do quadro do MFPKEY WMAAECMA \_</span><span class="sxs-lookup"><span data-stu-id="f4836-103">MFPKEY\_WMAAECMA\_FEATR\_FRAME\_SIZE Property</span></span>

<span data-ttu-id="f4836-104">Especifica o tamanho do quadro de áudio usado pelo DSP de captura de voz.</span><span class="sxs-lookup"><span data-stu-id="f4836-104">Specifies the audio frame size used by the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="f4836-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="f4836-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="f4836-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="f4836-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="f4836-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="f4836-107">Data Type</span></span>

<span data-ttu-id="f4836-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="f4836-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="f4836-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="f4836-109">Default Value</span></span>

<span data-ttu-id="f4836-110">0</span><span class="sxs-lookup"><span data-stu-id="f4836-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="f4836-111">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="f4836-111">Applies To</span></span>

-   [<span data-ttu-id="f4836-112">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="f4836-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="f4836-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4836-113">Remarks</span></span>

<span data-ttu-id="f4836-114">O algoritmo AEC (cancelamento de eco acústico) processa amostras de áudio PCM um quadro por vez.</span><span class="sxs-lookup"><span data-stu-id="f4836-114">The acoustic echo cancellation (AEC) algorithm processes PCM audio samples one frame at a time.</span></span> <span data-ttu-id="f4836-115">O valor dessa propriedade é o tamanho do quadro de áudio, em exemplos.</span><span class="sxs-lookup"><span data-stu-id="f4836-115">The value of this property is the size of the audio frame, in samples.</span></span> <span data-ttu-id="f4836-116">Antes de definir essa propriedade, você deve definir a propriedade [ \_ modo de \_ recurso \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) como Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="f4836-116">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="f4836-117">O DSP de captura de voz dá suporte aos seguintes tamanhos de quadro:</span><span class="sxs-lookup"><span data-stu-id="f4836-117">The Voice Capture DSP supports the following frame sizes:</span></span>

-   <span data-ttu-id="f4836-118">80</span><span class="sxs-lookup"><span data-stu-id="f4836-118">80</span></span>
-   <span data-ttu-id="f4836-119">128</span><span class="sxs-lookup"><span data-stu-id="f4836-119">128</span></span>
-   <span data-ttu-id="f4836-120">160</span><span class="sxs-lookup"><span data-stu-id="f4836-120">160</span></span>
-   <span data-ttu-id="f4836-121">240</span><span class="sxs-lookup"><span data-stu-id="f4836-121">240</span></span>
-   <span data-ttu-id="f4836-122">256</span><span class="sxs-lookup"><span data-stu-id="f4836-122">256</span></span>
-   <span data-ttu-id="f4836-123">320</span><span class="sxs-lookup"><span data-stu-id="f4836-123">320</span></span>

<span data-ttu-id="f4836-124">Se o valor dessa propriedade for zero, o DSP selecionará o tamanho do quadro com base no modo do sistema e no formato de saída.</span><span class="sxs-lookup"><span data-stu-id="f4836-124">If the value of this property is zero, the DSP selects the frame size based on the system mode and the output format.</span></span>

<span data-ttu-id="f4836-125">No entanto, para obter o melhor desempenho, é recomendável que os aplicativos usem o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="f4836-125">For the best performance, however, it is recommended that applications use the default value.</span></span> <span data-ttu-id="f4836-126">Se o modo de processamento for somente matriz de microfone, o valor padrão será 320 exemplos.</span><span class="sxs-lookup"><span data-stu-id="f4836-126">If the processing mode is microphone array only, the default value is 320 samples.</span></span> <span data-ttu-id="f4836-127">Para todos os outros modos de processamento, o valor padrão é 160 exemplos.</span><span class="sxs-lookup"><span data-stu-id="f4836-127">For all other processing modes, the default value is 160 samples.</span></span> <span data-ttu-id="f4836-128">Para obter mais informações sobre os modos de processamento do DSP de captura de voz, consulte [MFPKEY \_ WMAAECMA \_ System \_ Mode](mfpkey-wmaaecma-system-modeproperty.md).</span><span class="sxs-lookup"><span data-stu-id="f4836-128">For more information about the processing modes of the Voice Capture DSP, see [MFPKEY\_WMAAECMA\_SYSTEM\_MODE](mfpkey-wmaaecma-system-modeproperty.md).</span></span>

<span data-ttu-id="f4836-129">Após a primeira chamada para [**IMediaObject:: AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) ou [**IMediaObject::P rocessoutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput), você pode ler essa propriedade para obter o tamanho real do quadro em uso, mesmo quando o [**\_ modo de \_ recurso \_ MFPKEY WMAAECMA**](mfpkey-wmaaecma-feature-modeproperty.md) for false.</span><span class="sxs-lookup"><span data-stu-id="f4836-129">After the first call to [**IMediaObject::AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) or [**IMediaObject::ProcessOutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput), you can read this property to get the actual frame size in use, even when [**MFPKEY\_WMAAECMA\_FEATURE\_MODE**](mfpkey-wmaaecma-feature-modeproperty.md) is false.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4836-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4836-130">Requirements</span></span>



| <span data-ttu-id="f4836-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4836-131">Requirement</span></span> | <span data-ttu-id="f4836-132">Valor</span><span class="sxs-lookup"><span data-stu-id="f4836-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4836-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4836-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f4836-134">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f4836-134">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f4836-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4836-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f4836-136">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f4836-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f4836-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f4836-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4836-138"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4836-138"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4836-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4836-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4836-140">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f4836-140">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="f4836-141">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="f4836-141">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
