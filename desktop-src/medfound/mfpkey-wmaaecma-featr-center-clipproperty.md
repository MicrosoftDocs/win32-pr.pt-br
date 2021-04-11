---
description: Especifica se o DSP de captura de voz executa recorte de centro.
ms.assetid: 6830cadd-fa8d-41e1-ac11-a6c8f2795941
title: Propriedade MFPKEY_WMAAECMA_FEATR_CENTER_CLIP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0936ddfe9e34664e55a20efea35a3c06dd6990e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164926"
---
# <a name="mfpkey_wmaaecma_featr_center_clip-property"></a><span data-ttu-id="024f9-103">\_Propriedade de \_ clipe do \_ Centro \_ do MFPKEY WMAAECMA</span><span class="sxs-lookup"><span data-stu-id="024f9-103">MFPKEY\_WMAAECMA\_FEATR\_CENTER\_CLIP Property</span></span>

<span data-ttu-id="024f9-104">Especifica se o DSP de captura de voz executa recorte de centro.</span><span class="sxs-lookup"><span data-stu-id="024f9-104">Specifies whether the Voice Capture DSP performs center clipping.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="024f9-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="024f9-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="024f9-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="024f9-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="024f9-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="024f9-107">Data Type</span></span>

<span data-ttu-id="024f9-108">BOOL do VT \_</span><span class="sxs-lookup"><span data-stu-id="024f9-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="024f9-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="024f9-109">Default Value</span></span>

<span data-ttu-id="024f9-110">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="024f9-110">VARIANT\_TRUE</span></span>

## <a name="applies-to"></a><span data-ttu-id="024f9-111">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="024f9-111">Applies To</span></span>

-   [<span data-ttu-id="024f9-112">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="024f9-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="024f9-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="024f9-113">Remarks</span></span>

<span data-ttu-id="024f9-114">O recorte centralizado é um processo que remove resíduos de eco pequeno que permanecem após o processamento de AEC, em situações de uma só conversa (quando a fala ocorre apenas em uma extremidade da linha).</span><span class="sxs-lookup"><span data-stu-id="024f9-114">Center clipping is a process that removes small echo residuals that remain after AEC processing, in single-talk situations (when speech occurs only on one end of the line).</span></span>

<span data-ttu-id="024f9-115">Essa propriedade pode ter os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="024f9-115">This property can have the following values.</span></span>



| <span data-ttu-id="024f9-116">Valor</span><span class="sxs-lookup"><span data-stu-id="024f9-116">Value</span></span>          | <span data-ttu-id="024f9-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="024f9-117">Description</span></span>              |
|----------------|--------------------------|
| <span data-ttu-id="024f9-118">VARIANTE \_ falso</span><span class="sxs-lookup"><span data-stu-id="024f9-118">VARIANT\_FALSE</span></span> | <span data-ttu-id="024f9-119">Desabilitar recorte de centro.</span><span class="sxs-lookup"><span data-stu-id="024f9-119">Disable center clipping.</span></span> |
| <span data-ttu-id="024f9-120">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="024f9-120">VARIANT\_TRUE</span></span>  | <span data-ttu-id="024f9-121">Habilitar recorte de centro.</span><span class="sxs-lookup"><span data-stu-id="024f9-121">Enable center clipping.</span></span>  |



 

<span data-ttu-id="024f9-122">O valor padrão dessa propriedade é VARIANT \_ true (Enabled).</span><span class="sxs-lookup"><span data-stu-id="024f9-122">The default value of this property is VARIANT\_TRUE (enabled).</span></span> <span data-ttu-id="024f9-123">Antes de definir essa propriedade, você deve definir a propriedade [ \_ modo de \_ recurso \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) como Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="024f9-123">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="024f9-124">O DSP usa essa propriedade somente quando o processamento de AEC está habilitado.</span><span class="sxs-lookup"><span data-stu-id="024f9-124">The DSP uses this property only when AEC processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="024f9-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="024f9-125">Requirements</span></span>



| <span data-ttu-id="024f9-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="024f9-126">Requirement</span></span> | <span data-ttu-id="024f9-127">Valor</span><span class="sxs-lookup"><span data-stu-id="024f9-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="024f9-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="024f9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="024f9-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="024f9-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="024f9-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="024f9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="024f9-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="024f9-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="024f9-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="024f9-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="024f9-133"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="024f9-133"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="024f9-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="024f9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="024f9-135">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="024f9-135">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="024f9-136">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="024f9-136">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
