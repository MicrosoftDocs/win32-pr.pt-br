---
description: Permite que o aplicativo substitua as configurações padrão em várias propriedades do DSP de captura de voz.
ms.assetid: 1c11e817-36bd-4a5d-9c2b-6a91e86f623f
title: Propriedade MFPKEY_WMAAECMA_FEATURE_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9a47ef86a2acf83131800e9cb55b86de2cd3d98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661496"
---
# <a name="mfpkey_wmaaecma_feature_mode-property"></a><span data-ttu-id="d2e9a-103">\_Propriedade do \_ modo de recurso MFPKEY WMAAECMA \_</span><span class="sxs-lookup"><span data-stu-id="d2e9a-103">MFPKEY\_WMAAECMA\_FEATURE\_MODE Property</span></span>

<span data-ttu-id="d2e9a-104">Permite que o aplicativo substitua as configurações padrão em várias propriedades do DSP de captura de voz.</span><span class="sxs-lookup"><span data-stu-id="d2e9a-104">Enables the application to override the default settings on various properties of the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="d2e9a-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="d2e9a-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="d2e9a-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="d2e9a-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="d2e9a-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="d2e9a-107">Data Type</span></span>

<span data-ttu-id="d2e9a-108">BOOL do VT \_</span><span class="sxs-lookup"><span data-stu-id="d2e9a-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="d2e9a-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="d2e9a-109">Default Value</span></span>

<span data-ttu-id="d2e9a-110">VARIANTE \_ falso</span><span class="sxs-lookup"><span data-stu-id="d2e9a-110">VARIANT\_FALSE</span></span>

## <a name="applies-to"></a><span data-ttu-id="d2e9a-111">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="d2e9a-111">Applies To</span></span>

-   [<span data-ttu-id="d2e9a-112">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="d2e9a-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="d2e9a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2e9a-113">Remarks</span></span>

<span data-ttu-id="d2e9a-114">Se essa propriedade for VARIANT \_ true, o aplicativo poderá definir as seguintes propriedades no DSP:</span><span class="sxs-lookup"><span data-stu-id="d2e9a-114">If this property is VARIANT\_TRUE, the application can set the following properties on the DSP:</span></span>

-   [<span data-ttu-id="d2e9a-115">AES do MFPKEY \_ WMAAECMA \_ \_</span><span class="sxs-lookup"><span data-stu-id="d2e9a-115">MFPKEY\_WMAAECMA\_FEATR\_AES</span></span>](mfpkey-wmaaecma-featr-aesproperty.md)
-   [<span data-ttu-id="d2e9a-116">\_AGC MFPKEY WMAAECMA \_ \_</span><span class="sxs-lookup"><span data-stu-id="d2e9a-116">MFPKEY\_WMAAECMA\_FEATR\_AGC</span></span>](mfpkey-wmaaecma-featr-agcproperty.md)
-   [<span data-ttu-id="d2e9a-117">\_clipe do \_ \_ Centro \_ do MFPKEY WMAAECMA</span><span class="sxs-lookup"><span data-stu-id="d2e9a-117">MFPKEY\_WMAAECMA\_FEATR\_CENTER\_CLIP</span></span>](mfpkey-wmaaecma-featr-center-clipproperty.md)
-   [<span data-ttu-id="d2e9a-118">MFPKEY \_ WMAAECMA com \_ comprimento de \_ eco \_</span><span class="sxs-lookup"><span data-stu-id="d2e9a-118">MFPKEY\_WMAAECMA\_FEATR\_ECHO\_LENGTH</span></span>](mfpkey-wmaaecma-featr-echo-lengthproperty.md)
-   [<span data-ttu-id="d2e9a-119">\_tamanho do \_ \_ quadro \_ do MFPKEY WMAAECMA</span><span class="sxs-lookup"><span data-stu-id="d2e9a-119">MFPKEY\_WMAAECMA\_FEATR\_FRAME\_SIZE</span></span>](mfpkey-wmaaecma-featr-frame-sizeproperty.md)
-   [<span data-ttu-id="d2e9a-120">\_ \_ \_ modo MICARR do MFPKEY WMAAECMA \_</span><span class="sxs-lookup"><span data-stu-id="d2e9a-120">MFPKEY\_WMAAECMA\_FEATR\_MICARR\_MODE</span></span>](mfpkey-wmaaecma-featr-micarr-modeproperty.md)
-   [<span data-ttu-id="d2e9a-121">MFPKEY \_ WMAAECMA refeito \_ \_ MICARR \_ preproc</span><span class="sxs-lookup"><span data-stu-id="d2e9a-121">MFPKEY\_WMAAECMA\_FEATR\_MICARR\_PREPROC</span></span>](mfpkey-wmaaecma-featr-micarr-preprocproperty.md)
-   [<span data-ttu-id="d2e9a-122">\_preenchimento de \_ \_ ruído \_ do MFPKEY WMAAECMA</span><span class="sxs-lookup"><span data-stu-id="d2e9a-122">MFPKEY\_WMAAECMA\_FEATR\_NOISE\_FILL</span></span>](mfpkey-wmaaecma-featr-noise-fillproperty.md)
-   [<span data-ttu-id="d2e9a-123">\_ns MFPKEY WMAAECMA \_ \_</span><span class="sxs-lookup"><span data-stu-id="d2e9a-123">MFPKEY\_WMAAECMA\_FEATR\_NS</span></span>](mfpkey-wmaaecma-featr-nsproperty.md)
-   [<span data-ttu-id="d2e9a-124">MFPKEY \_ WMAAECMA para \_ \_ VAD</span><span class="sxs-lookup"><span data-stu-id="d2e9a-124">MFPKEY\_WMAAECMA\_FEATR\_VAD</span></span>](mfpkey-wmaaecma-featr-vadproperty.md)

<span data-ttu-id="d2e9a-125">Se essa propriedade for VARIANT \_ false, o DSP ignorará essas propriedades e usará suas configurações padrão.</span><span class="sxs-lookup"><span data-stu-id="d2e9a-125">If this property is VARIANT\_FALSE, the DSP ignores these properties and uses its default settings.</span></span> <span data-ttu-id="d2e9a-126">O valor padrão dessa propriedade é VARIANT \_ false.</span><span class="sxs-lookup"><span data-stu-id="d2e9a-126">The default value of this property is VARIANT\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2e9a-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2e9a-127">Requirements</span></span>



| <span data-ttu-id="d2e9a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2e9a-128">Requirement</span></span> | <span data-ttu-id="d2e9a-129">Valor</span><span class="sxs-lookup"><span data-stu-id="d2e9a-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2e9a-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2e9a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d2e9a-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d2e9a-131">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d2e9a-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2e9a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d2e9a-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d2e9a-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d2e9a-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d2e9a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2e9a-135"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2e9a-135"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2e9a-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2e9a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2e9a-137">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d2e9a-137">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="d2e9a-138">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="d2e9a-138">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
