---
description: Especifica se o DSP de captura de voz usa modo de origem ou modo de filtro.
ms.assetid: d1d3beba-678c-48fd-ad12-45e0418e1236
title: Propriedade MFPKEY_WMAAECMA_DMO_SOURCE_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5749ff1f142603cc45df475caae7bc71182bde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164927"
---
# <a name="mfpkey_wmaaecma_dmo_source_mode-property"></a><span data-ttu-id="05f97-103">\_Propriedade do \_ \_ modo de origem MFPKEY WMAAECMA DMO \_</span><span class="sxs-lookup"><span data-stu-id="05f97-103">MFPKEY\_WMAAECMA\_DMO\_SOURCE\_MODE Property</span></span>

<span data-ttu-id="05f97-104">Especifica se o DSP de captura de voz usa modo de origem ou modo de filtro.</span><span class="sxs-lookup"><span data-stu-id="05f97-104">Specifies whether the Voice Capture DSP uses source mode or filter mode.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="05f97-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="05f97-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="05f97-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="05f97-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="05f97-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="05f97-107">Data Type</span></span>

<span data-ttu-id="05f97-108">BOOL do VT \_</span><span class="sxs-lookup"><span data-stu-id="05f97-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="05f97-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="05f97-109">Default Value</span></span>

<span data-ttu-id="05f97-110">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="05f97-110">VARIANT\_TRUE</span></span>

## <a name="applies-to"></a><span data-ttu-id="05f97-111">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="05f97-111">Applies To</span></span>

-   [<span data-ttu-id="05f97-112">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="05f97-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="05f97-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="05f97-113">Remarks</span></span>

<span data-ttu-id="05f97-114">No modo de origem, o aplicativo não precisa enviar dados de entrada para o DSP, pois o DSP recebe automaticamente os dados dos dispositivos de áudio.</span><span class="sxs-lookup"><span data-stu-id="05f97-114">In source mode, the application does not need to send input data to the DSP, because the DSP automatically pulls data from the audio devices.</span></span> <span data-ttu-id="05f97-115">No modo de filtro, o aplicativo deve enviar os dados de entrada para o DSP.</span><span class="sxs-lookup"><span data-stu-id="05f97-115">In filter mode, the application must send the input data to the DSP.</span></span>

<span data-ttu-id="05f97-116">Essa propriedade pode ter os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="05f97-116">This property can have the following values.</span></span>



| <span data-ttu-id="05f97-117">Valor</span><span class="sxs-lookup"><span data-stu-id="05f97-117">Value</span></span>          | <span data-ttu-id="05f97-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="05f97-118">Description</span></span>  |
|----------------|--------------|
| <span data-ttu-id="05f97-119">VARIANTE \_ falso</span><span class="sxs-lookup"><span data-stu-id="05f97-119">VARIANT\_FALSE</span></span> | <span data-ttu-id="05f97-120">Modo de filtro.</span><span class="sxs-lookup"><span data-stu-id="05f97-120">Filter mode.</span></span> |
| <span data-ttu-id="05f97-121">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="05f97-121">VARIANT\_TRUE</span></span>  | <span data-ttu-id="05f97-122">Modo de origem.</span><span class="sxs-lookup"><span data-stu-id="05f97-122">Source mode.</span></span> |



 

> [!Note]  
> <span data-ttu-id="05f97-123">Quando o DMO está no modo de origem, você só deve chamar [**IMediaObject:: SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) para definir o formato de fluxo de saída e não chamar [**IMediaObject:: SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) para definir formatos de fluxo de entrada.</span><span class="sxs-lookup"><span data-stu-id="05f97-123">When the DMO is in source mode, you should only call [**IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) to set output stream format, and do not call [**IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) to set input stream formats.</span></span> <span data-ttu-id="05f97-124">Caso contrário, a inicialização do DMO falhará.</span><span class="sxs-lookup"><span data-stu-id="05f97-124">Otherwise DMO initialization will fail.</span></span>

 

<span data-ttu-id="05f97-125">Se o valor dessa propriedade for VARIANT \_ true, o DSP terá zero entradas.</span><span class="sxs-lookup"><span data-stu-id="05f97-125">If the value of this property is VARIANT\_TRUE, the DSP has zero inputs.</span></span> <span data-ttu-id="05f97-126">Se o valor for VARIANT \_ false, o DSP terá uma ou duas entradas, dependendo do valor da Propriedade do [modo do \_ \_ sistema MFPKEY \_ WMAAECMA](mfpkey-wmaaecma-system-modeproperty.md) , conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="05f97-126">If the value is VARIANT\_FALSE, the DSP has one or two inputs, depending on the value of the [MFPKEY\_WMAAECMA\_SYSTEM\_MODE](mfpkey-wmaaecma-system-modeproperty.md) property, as shown in the following table.</span></span>



| <span data-ttu-id="05f97-127">Valor</span><span class="sxs-lookup"><span data-stu-id="05f97-127">Value</span></span>                     | <span data-ttu-id="05f97-128">Número de entradas</span><span class="sxs-lookup"><span data-stu-id="05f97-128">Number of inputs</span></span> |
|---------------------------|------------------|
| <span data-ttu-id="05f97-129">OPTIBEAM \_ \_ de matriz e \_ AEC</span><span class="sxs-lookup"><span data-stu-id="05f97-129">OPTIBEAM\_ARRAY\_AND\_AEC</span></span> | <span data-ttu-id="05f97-130">2</span><span class="sxs-lookup"><span data-stu-id="05f97-130">2</span></span>                |
| <span data-ttu-id="05f97-131">\_somente matriz \_ OPTIBEAM</span><span class="sxs-lookup"><span data-stu-id="05f97-131">OPTIBEAM\_ARRAY\_ONLY</span></span>     | <span data-ttu-id="05f97-132">1</span><span class="sxs-lookup"><span data-stu-id="05f97-132">1</span></span>                |
| <span data-ttu-id="05f97-133">\_AEC de canal único \_</span><span class="sxs-lookup"><span data-stu-id="05f97-133">SINGLE\_CHANNEL\_AEC</span></span>      | <span data-ttu-id="05f97-134">2</span><span class="sxs-lookup"><span data-stu-id="05f97-134">2</span></span>                |
| <span data-ttu-id="05f97-135">\_NSAGC de canal único \_</span><span class="sxs-lookup"><span data-stu-id="05f97-135">SINGLE\_CHANNEL\_NSAGC</span></span>    | <span data-ttu-id="05f97-136">1</span><span class="sxs-lookup"><span data-stu-id="05f97-136">1</span></span>                |



 

> [!Note]  
> <span data-ttu-id="05f97-137">Somente os modos com uma única entrada funcionarão com o filtro de wrapper DMO da API do DirectShow 9,0.</span><span class="sxs-lookup"><span data-stu-id="05f97-137">Only modes with a single input will work with the wrapper filter DMO from the DirectShow 9.0 API.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="05f97-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05f97-138">Requirements</span></span>



| <span data-ttu-id="05f97-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="05f97-139">Requirement</span></span> | <span data-ttu-id="05f97-140">Valor</span><span class="sxs-lookup"><span data-stu-id="05f97-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05f97-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05f97-141">Minimum supported client</span></span><br/> | <span data-ttu-id="05f97-142">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="05f97-142">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="05f97-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05f97-143">Minimum supported server</span></span><br/> | <span data-ttu-id="05f97-144">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="05f97-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="05f97-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="05f97-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="05f97-146"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="05f97-146"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05f97-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="05f97-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05f97-148">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="05f97-148">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="05f97-149">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="05f97-149">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
