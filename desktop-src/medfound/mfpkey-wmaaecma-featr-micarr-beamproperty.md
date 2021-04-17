---
description: Especifica qual transmissão o DSP de captura de voz usa para processamento de matriz de microfone.
ms.assetid: 9ed761da-3f1b-47e8-b71f-becc56fe8801
title: Propriedade MFPKEY_WMAAECMA_FEATR_MICARR_BEAM (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9165eec0dee87fa5d9f6a751f41e81d0de2d9958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759871"
---
# <a name="mfpkey_wmaaecma_featr_micarr_beam-property"></a><span data-ttu-id="f5932-103">\_Propriedade de \_ \_ \_ transmissão MICARR do MFPKEY WMAAECMA</span><span class="sxs-lookup"><span data-stu-id="f5932-103">MFPKEY\_WMAAECMA\_FEATR\_MICARR\_BEAM Property</span></span>

<span data-ttu-id="f5932-104">Especifica qual transmissão o DSP de captura de voz usa para processamento de matriz de microfone.</span><span class="sxs-lookup"><span data-stu-id="f5932-104">Specifies which beam the Voice Capture DSP uses for microphone array processing.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="f5932-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="f5932-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="f5932-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="f5932-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="f5932-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="f5932-107">Data Type</span></span>

<span data-ttu-id="f5932-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="f5932-108">VT\_I4</span></span>

## <a name="applies-to"></a><span data-ttu-id="f5932-109">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="f5932-109">Applies To</span></span>

-   [<span data-ttu-id="f5932-110">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="f5932-110">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="f5932-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5932-111">Remarks</span></span>

<span data-ttu-id="f5932-112">Defina essa propriedade se o valor da propriedade [do \_ \_ \_ \_ modo MICARR do MFPKEY WMAAECMA](mfpkey-wmaaecma-featr-micarr-modeproperty.md) for MICARRAY de \_ \_ transmissão externa.</span><span class="sxs-lookup"><span data-stu-id="f5932-112">Set this property if the value of the [MFPKEY\_WMAAECMA\_FEATR\_MICARR\_MODE](mfpkey-wmaaecma-featr-micarr-modeproperty.md) property is MICARRAY\_EXTERN\_BEAM.</span></span>

<span data-ttu-id="f5932-113">Se o valor de [**MFPKEY \_ WMAAECMA do \_ \_ \_ modo MICARR**](mfpkey-wmaaecma-featr-micarr-modeproperty.md) for MICARRAY \_ Single \_ feixe, você poderá ler essa propriedade para consultar qual feixe foi selecionado pelo DSP.</span><span class="sxs-lookup"><span data-stu-id="f5932-113">If the value of [**MFPKEY\_WMAAECMA\_FEATR\_MICARR\_MODE**](mfpkey-wmaaecma-featr-micarr-modeproperty.md) is MICARRAY\_SINGLE\_BEAM, you can read this property to query which beam was selected by the DSP.</span></span>

<span data-ttu-id="f5932-114">Essa propriedade pode ter os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f5932-114">This property can have the following values.</span></span> <span data-ttu-id="f5932-115">Os valores estão em graus horizontal.</span><span class="sxs-lookup"><span data-stu-id="f5932-115">Values are in degrees horizontal.</span></span>



| <span data-ttu-id="f5932-116">Valor</span><span class="sxs-lookup"><span data-stu-id="f5932-116">Value</span></span> | <span data-ttu-id="f5932-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="f5932-117">Description</span></span>              |
|-------|--------------------------|
| <span data-ttu-id="f5932-118">0</span><span class="sxs-lookup"><span data-stu-id="f5932-118">0</span></span>     | <span data-ttu-id="f5932-119">-50 graus.</span><span class="sxs-lookup"><span data-stu-id="f5932-119">-50 degrees.</span></span>             |
| <span data-ttu-id="f5932-120">1</span><span class="sxs-lookup"><span data-stu-id="f5932-120">1</span></span>     | <span data-ttu-id="f5932-121">-40 graus.</span><span class="sxs-lookup"><span data-stu-id="f5932-121">-40 degrees.</span></span>             |
| <span data-ttu-id="f5932-122">2</span><span class="sxs-lookup"><span data-stu-id="f5932-122">2</span></span>     | <span data-ttu-id="f5932-123">-30 graus.</span><span class="sxs-lookup"><span data-stu-id="f5932-123">-30 degrees.</span></span>             |
| <span data-ttu-id="f5932-124">3</span><span class="sxs-lookup"><span data-stu-id="f5932-124">3</span></span>     | <span data-ttu-id="f5932-125">-20 graus.</span><span class="sxs-lookup"><span data-stu-id="f5932-125">-20 degrees.</span></span>             |
| <span data-ttu-id="f5932-126">4</span><span class="sxs-lookup"><span data-stu-id="f5932-126">4</span></span>     | <span data-ttu-id="f5932-127">-10 graus.</span><span class="sxs-lookup"><span data-stu-id="f5932-127">-10 degrees.</span></span>             |
| <span data-ttu-id="f5932-128">5</span><span class="sxs-lookup"><span data-stu-id="f5932-128">5</span></span>     | <span data-ttu-id="f5932-129">0 graus (feixe central).</span><span class="sxs-lookup"><span data-stu-id="f5932-129">0 degrees (center beam).</span></span> |
| <span data-ttu-id="f5932-130">6</span><span class="sxs-lookup"><span data-stu-id="f5932-130">6</span></span>     | <span data-ttu-id="f5932-131">10 graus.</span><span class="sxs-lookup"><span data-stu-id="f5932-131">10 degrees.</span></span>              |
| <span data-ttu-id="f5932-132">7</span><span class="sxs-lookup"><span data-stu-id="f5932-132">7</span></span>     | <span data-ttu-id="f5932-133">20 graus.</span><span class="sxs-lookup"><span data-stu-id="f5932-133">20 degrees.</span></span>              |
| <span data-ttu-id="f5932-134">8</span><span class="sxs-lookup"><span data-stu-id="f5932-134">8</span></span>     | <span data-ttu-id="f5932-135">30 graus.</span><span class="sxs-lookup"><span data-stu-id="f5932-135">30 degrees.</span></span>              |
| <span data-ttu-id="f5932-136">9</span><span class="sxs-lookup"><span data-stu-id="f5932-136">9</span></span>     | <span data-ttu-id="f5932-137">40 graus.</span><span class="sxs-lookup"><span data-stu-id="f5932-137">40 degrees.</span></span>              |
| <span data-ttu-id="f5932-138">10</span><span class="sxs-lookup"><span data-stu-id="f5932-138">10</span></span>    | <span data-ttu-id="f5932-139">50 graus.</span><span class="sxs-lookup"><span data-stu-id="f5932-139">50 degrees.</span></span>              |



 

## <a name="requirements"></a><span data-ttu-id="f5932-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5932-140">Requirements</span></span>



| <span data-ttu-id="f5932-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5932-141">Requirement</span></span> | <span data-ttu-id="f5932-142">Valor</span><span class="sxs-lookup"><span data-stu-id="f5932-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5932-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5932-143">Minimum supported client</span></span><br/> | <span data-ttu-id="f5932-144">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f5932-144">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f5932-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5932-145">Minimum supported server</span></span><br/> | <span data-ttu-id="f5932-146">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f5932-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f5932-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f5932-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5932-148"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5932-148"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5932-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5932-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5932-150">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f5932-150">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="f5932-151">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="f5932-151">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
