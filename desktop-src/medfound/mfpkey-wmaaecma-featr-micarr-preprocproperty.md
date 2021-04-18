---
description: Especifica se o DSP de captura de voz executa o pré-processamento da matriz do microfone.
ms.assetid: 0f197165-e6e5-456b-9615-1edc8ada7bb5
title: Propriedade MFPKEY_WMAAECMA_FEATR_MICARR_PREPROC (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f992d8d26ba547eb1b5d1eac470536a963209f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105786166"
---
# <a name="mfpkey_wmaaecma_featr_micarr_preproc-property"></a><span data-ttu-id="1a77f-103">\_ \_ \_ \_ Propriedade preproc MICARR do MFPKEY WMAAECMA</span><span class="sxs-lookup"><span data-stu-id="1a77f-103">MFPKEY\_WMAAECMA\_FEATR\_MICARR\_PREPROC Property</span></span>

<span data-ttu-id="1a77f-104">Especifica se o DSP de captura de voz executa o pré-processamento da matriz do microfone.</span><span class="sxs-lookup"><span data-stu-id="1a77f-104">Specifies whether the Voice Capture DSP performs microphone array preprocessing.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="1a77f-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="1a77f-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="1a77f-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="1a77f-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="1a77f-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="1a77f-107">Data Type</span></span>

<span data-ttu-id="1a77f-108">BOOL do VT \_</span><span class="sxs-lookup"><span data-stu-id="1a77f-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="1a77f-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="1a77f-109">Default Value</span></span>

<span data-ttu-id="1a77f-110">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="1a77f-110">VARIANT\_TRUE</span></span>

## <a name="applies-to"></a><span data-ttu-id="1a77f-111">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="1a77f-111">Applies To</span></span>

-   [<span data-ttu-id="1a77f-112">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="1a77f-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="1a77f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a77f-113">Remarks</span></span>

<span data-ttu-id="1a77f-114">O pré-processamento pode remover tons estacionários que interferem no processamento, como um tom com uma densidade fixa.</span><span class="sxs-lookup"><span data-stu-id="1a77f-114">Preprocessing can remove stationary tones that interfere with processing, such as a tone with a fixed pitch.</span></span>

<span data-ttu-id="1a77f-115">Essa propriedade pode ter os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="1a77f-115">This property can have the following values.</span></span>



| <span data-ttu-id="1a77f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="1a77f-116">Value</span></span>          | <span data-ttu-id="1a77f-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="1a77f-117">Description</span></span>            |
|----------------|------------------------|
| <span data-ttu-id="1a77f-118">VARIANTE \_ falso</span><span class="sxs-lookup"><span data-stu-id="1a77f-118">VARIANT\_FALSE</span></span> | <span data-ttu-id="1a77f-119">Desabilitar o pré-processamento.</span><span class="sxs-lookup"><span data-stu-id="1a77f-119">Disable preprocessing.</span></span> |
| <span data-ttu-id="1a77f-120">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="1a77f-120">VARIANT\_TRUE</span></span>  | <span data-ttu-id="1a77f-121">Habilite o pré-processamento.</span><span class="sxs-lookup"><span data-stu-id="1a77f-121">Enable preprocessing.</span></span>  |



 

<span data-ttu-id="1a77f-122">O valor padrão dessa propriedade é VARIANT \_ true (Enabled).</span><span class="sxs-lookup"><span data-stu-id="1a77f-122">The default value of this property is VARIANT\_TRUE (enabled).</span></span> <span data-ttu-id="1a77f-123">Antes de definir essa propriedade, você deve definir a propriedade [ \_ modo de \_ recurso \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) como Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="1a77f-123">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="1a77f-124">O DSP usa essa propriedade somente quando o processamento da matriz de microfone está habilitado.</span><span class="sxs-lookup"><span data-stu-id="1a77f-124">The DSP uses this property only when microphone array processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a77f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a77f-125">Requirements</span></span>



| <span data-ttu-id="1a77f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a77f-126">Requirement</span></span> | <span data-ttu-id="1a77f-127">Valor</span><span class="sxs-lookup"><span data-stu-id="1a77f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a77f-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a77f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1a77f-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1a77f-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="1a77f-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a77f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1a77f-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1a77f-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1a77f-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1a77f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a77f-133"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a77f-133"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a77f-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a77f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a77f-135">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1a77f-135">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="1a77f-136">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="1a77f-136">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
