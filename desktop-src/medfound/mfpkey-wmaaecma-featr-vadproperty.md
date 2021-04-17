---
description: Especifica o tipo de detecção de atividade de voz que o DSP de captura de voz executa.
ms.assetid: 59c8e348-8c08-4cf8-9c72-8d0f4fabc473
title: Propriedade MFPKEY_WMAAECMA_FEATR_VAD (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e41b8ad80d909a0285b266587d02c09c08d794
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782441"
---
# <a name="mfpkey_wmaaecma_featr_vad-property"></a><span data-ttu-id="7d16d-103">\_ \_ \_ Propriedade VAD do MFPKEY WMAAECMA</span><span class="sxs-lookup"><span data-stu-id="7d16d-103">MFPKEY\_WMAAECMA\_FEATR\_VAD Property</span></span>

<span data-ttu-id="7d16d-104">Especifica o tipo de detecção de atividade de voz que o DSP de captura de voz executa.</span><span class="sxs-lookup"><span data-stu-id="7d16d-104">Specifies the type of voice activity detection that the Voice Capture DSP performs.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="7d16d-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="7d16d-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="7d16d-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="7d16d-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="7d16d-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="7d16d-107">Data Type</span></span>

<span data-ttu-id="7d16d-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="7d16d-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="7d16d-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="7d16d-109">Default Value</span></span>

<span data-ttu-id="7d16d-110">0</span><span class="sxs-lookup"><span data-stu-id="7d16d-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="7d16d-111">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="7d16d-111">Applies To</span></span>

-   [<span data-ttu-id="7d16d-112">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="7d16d-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="7d16d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d16d-113">Remarks</span></span>

<span data-ttu-id="7d16d-114">O valor dessa propriedade é um membro da enumeração do [ \_ \_ modo de VAD do AEC](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_vad_mode) .</span><span class="sxs-lookup"><span data-stu-id="7d16d-114">The value of this property is a member of the [AEC\_VAD\_MODE](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_vad_mode) enumeration.</span></span> <span data-ttu-id="7d16d-115">A saída da detecção de atividade de voz é um número de 0 a 3, calculada para cada quadro de áudio.</span><span class="sxs-lookup"><span data-stu-id="7d16d-115">The output from voice activity detection is a number from 0 to 3, calculated for each audio frame.</span></span> <span data-ttu-id="7d16d-116">O DSP codifica o resultado no menor bit dos primeiros dois exemplos de áudio em cada quadro de áudio.</span><span class="sxs-lookup"><span data-stu-id="7d16d-116">The DSP encodes the result in the lowest bit of the first two audio samples in each audio frame.</span></span> <span data-ttu-id="7d16d-117">O significado do valor depende do modo especificado.</span><span class="sxs-lookup"><span data-stu-id="7d16d-117">The meaning of the value depends on the specified mode.</span></span>

<span data-ttu-id="7d16d-118">O código a seguir mostra como extrair os resultados dos dados de áudio.</span><span class="sxs-lookup"><span data-stu-id="7d16d-118">The following code shows how to extract the results from the audio data.</span></span> <span data-ttu-id="7d16d-119">Neste exemplo, *pOutput* é um ponteiro para o início de um quadro de áudio nos dados de saída.</span><span class="sxs-lookup"><span data-stu-id="7d16d-119">In this example, *pOutput* is a pointer to the start of an audio frame in the output data.</span></span>


```
int AecDecodeVAD(short *pOutput)
{
    int iVAD = (*pOutput) & 0x01;
    pOutput++;
    iVAD |= (*pOutput << 1) & 0x02;
    return iVAD;
}
```



<span data-ttu-id="7d16d-120">O valor padrão dessa propriedade é 0 (desabilitado).</span><span class="sxs-lookup"><span data-stu-id="7d16d-120">The default value of this property is 0 (disabled).</span></span> <span data-ttu-id="7d16d-121">Antes de definir essa propriedade, você deve definir a propriedade [ \_ modo de \_ recurso \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) como Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="7d16d-121">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d16d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d16d-122">Requirements</span></span>



| <span data-ttu-id="7d16d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d16d-123">Requirement</span></span> | <span data-ttu-id="7d16d-124">Valor</span><span class="sxs-lookup"><span data-stu-id="7d16d-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d16d-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d16d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7d16d-126">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7d16d-126">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7d16d-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d16d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7d16d-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7d16d-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7d16d-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7d16d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d16d-130"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d16d-130"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d16d-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d16d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d16d-132">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7d16d-132">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
