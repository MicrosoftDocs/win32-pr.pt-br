---
description: Especifica como o DSP de captura de voz executa o processamento de matriz de microfone.
ms.assetid: 5e04fe50-d764-4497-9999-37279e156204
title: Propriedade MFPKEY_WMAAECMA_FEATR_MICARR_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25bf8ffcae465e8abfddedb3e6d6dded683bb2bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164924"
---
# <a name="mfpkey_wmaaecma_featr_micarr_mode-property"></a><span data-ttu-id="9efa1-103">\_Propriedade do \_ \_ \_ modo MICARR do MFPKEY WMAAECMA</span><span class="sxs-lookup"><span data-stu-id="9efa1-103">MFPKEY\_WMAAECMA\_FEATR\_MICARR\_MODE Property</span></span>

<span data-ttu-id="9efa1-104">Especifica como o DSP de captura de voz executa o processamento de matriz de microfone.</span><span class="sxs-lookup"><span data-stu-id="9efa1-104">Specifies how the Voice Capture DSP performs microphone array processing.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="9efa1-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="9efa1-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="9efa1-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="9efa1-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="9efa1-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="9efa1-107">Data Type</span></span>

<span data-ttu-id="9efa1-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="9efa1-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="9efa1-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="9efa1-109">Default Value</span></span>

<span data-ttu-id="9efa1-110">MICARRAY \_ \_ feixe único</span><span class="sxs-lookup"><span data-stu-id="9efa1-110">MICARRAY\_SINGLE\_BEAM</span></span>

## <a name="applies-to"></a><span data-ttu-id="9efa1-111">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="9efa1-111">Applies To</span></span>

-   [<span data-ttu-id="9efa1-112">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="9efa1-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="9efa1-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="9efa1-113">Remarks</span></span>

<span data-ttu-id="9efa1-114">O valor dessa propriedade é um membro da enumeração do [ \_ \_ modo de matriz MIC](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mic_array_mode) .</span><span class="sxs-lookup"><span data-stu-id="9efa1-114">The value of this property is a member of the [MIC\_ARRAY\_MODE](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mic_array_mode) enumeration.</span></span> <span data-ttu-id="9efa1-115">O valor padrão é MICARRAY \_ Single \_ feixe.</span><span class="sxs-lookup"><span data-stu-id="9efa1-115">The default value is MICARRAY\_SINGLE\_BEAM.</span></span> <span data-ttu-id="9efa1-116">Antes de definir essa propriedade, você deve definir a propriedade [ \_ modo de \_ recurso \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) como Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="9efa1-116">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="9efa1-117">O DSP usa essa propriedade somente quando o processamento da matriz de microfone está habilitado.</span><span class="sxs-lookup"><span data-stu-id="9efa1-117">The DSP uses this property only when microphone array processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="9efa1-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9efa1-118">Requirements</span></span>



| <span data-ttu-id="9efa1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9efa1-119">Requirement</span></span> | <span data-ttu-id="9efa1-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9efa1-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9efa1-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9efa1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9efa1-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9efa1-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9efa1-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9efa1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9efa1-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9efa1-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9efa1-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9efa1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9efa1-126"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9efa1-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9efa1-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="9efa1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9efa1-128">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9efa1-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="9efa1-129">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="9efa1-129">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
