---
description: Especifica se o DSP de captura de voz executa a supressão de ruído.
ms.assetid: d63e9ac1-9584-4f74-8404-c95d17eb8c2d
title: Propriedade MFPKEY_WMAAECMA_FEATR_NS (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02218ce621123066e5e61435d93f8539de95e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105786165"
---
# <a name="mfpkey_wmaaecma_featr_ns-property"></a><span data-ttu-id="03767-103">\_ \_ \_ Propriedade ns do MFPKEY WMAAECMA</span><span class="sxs-lookup"><span data-stu-id="03767-103">MFPKEY\_WMAAECMA\_FEATR\_NS Property</span></span>

<span data-ttu-id="03767-104">Especifica se o DSP de captura de voz executa a supressão de ruído.</span><span class="sxs-lookup"><span data-stu-id="03767-104">Specifies whether the Voice Capture DSP performs noise suppression.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="03767-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="03767-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="03767-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="03767-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="03767-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="03767-107">Data Type</span></span>

<span data-ttu-id="03767-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="03767-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="03767-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="03767-109">Default Value</span></span>

<span data-ttu-id="03767-110">1</span><span class="sxs-lookup"><span data-stu-id="03767-110">1</span></span>

## <a name="applies-to"></a><span data-ttu-id="03767-111">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="03767-111">Applies To</span></span>

-   [<span data-ttu-id="03767-112">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="03767-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="03767-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="03767-113">Remarks</span></span>

<span data-ttu-id="03767-114">A supressão de ruído é um componente de DSP (processamento de sinal digital) que suprime ou reduz o ruído de fundo estacionário no sinal de áudio.</span><span class="sxs-lookup"><span data-stu-id="03767-114">Noise suppression is a digital signal processing (DSP) component that suppresses or reduces stationary background noise in the audio signal.</span></span> <span data-ttu-id="03767-115">A supressão de ruído é aplicada após o processamento do AEC (cancelamento de eco acústico) e da matriz de microfone.</span><span class="sxs-lookup"><span data-stu-id="03767-115">Noise suppression is applied after the acoustic echo cancellation (AEC) and microphone array processing.</span></span>

<span data-ttu-id="03767-116">Essa propriedade pode ter os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="03767-116">This property can have the following values.</span></span>



| <span data-ttu-id="03767-117">Valor</span><span class="sxs-lookup"><span data-stu-id="03767-117">Value</span></span> | <span data-ttu-id="03767-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="03767-118">Description</span></span>                |
|-------|----------------------------|
| <span data-ttu-id="03767-119">0</span><span class="sxs-lookup"><span data-stu-id="03767-119">0</span></span>     | <span data-ttu-id="03767-120">Desabilitar supressão de ruído.</span><span class="sxs-lookup"><span data-stu-id="03767-120">Disable noise suppression.</span></span> |
| <span data-ttu-id="03767-121">1</span><span class="sxs-lookup"><span data-stu-id="03767-121">1</span></span>     | <span data-ttu-id="03767-122">Habilitar supressão de ruído.</span><span class="sxs-lookup"><span data-stu-id="03767-122">Enable noise suppression.</span></span>  |



 

<span data-ttu-id="03767-123">O valor padrão dessa propriedade é 1 (habilitado).</span><span class="sxs-lookup"><span data-stu-id="03767-123">The default value of this property is 1 (enabled).</span></span> <span data-ttu-id="03767-124">Antes de definir essa propriedade, você deve definir a propriedade [ \_ modo de \_ recurso \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) como Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="03767-124">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="03767-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03767-125">Requirements</span></span>



| <span data-ttu-id="03767-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="03767-126">Requirement</span></span> | <span data-ttu-id="03767-127">Valor</span><span class="sxs-lookup"><span data-stu-id="03767-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03767-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03767-128">Minimum supported client</span></span><br/> | <span data-ttu-id="03767-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="03767-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="03767-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03767-130">Minimum supported server</span></span><br/> | <span data-ttu-id="03767-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="03767-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="03767-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="03767-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="03767-133"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="03767-133"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03767-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="03767-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03767-135">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="03767-135">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="03767-136">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="03767-136">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
