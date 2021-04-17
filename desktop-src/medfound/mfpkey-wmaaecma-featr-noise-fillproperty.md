---
description: Especifica se o DSP de captura de voz executa o preenchimento de ruído.
ms.assetid: 8bb64686-8f02-4e0d-a664-aeee1744fc8e
title: Propriedade MFPKEY_WMAAECMA_FEATR_NOISE_FILL (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea0c0af2b47767a7798d9b583ac55ad5112ddf1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790616"
---
# <a name="mfpkey_wmaaecma_featr_noise_fill-property"></a><span data-ttu-id="be149-103">\_Propriedade de \_ preenchimento de \_ ruído MFPKEY WMAAECMA \_</span><span class="sxs-lookup"><span data-stu-id="be149-103">MFPKEY\_WMAAECMA\_FEATR\_NOISE\_FILL Property</span></span>

<span data-ttu-id="be149-104">Especifica se o DSP de captura de voz executa o preenchimento de ruído.</span><span class="sxs-lookup"><span data-stu-id="be149-104">Specifies whether the Voice Capture DSP performs noise filling.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="be149-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="be149-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="be149-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="be149-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="be149-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="be149-107">Data Type</span></span>

<span data-ttu-id="be149-108">BOOL do VT \_</span><span class="sxs-lookup"><span data-stu-id="be149-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="be149-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="be149-109">Default Value</span></span>

<span data-ttu-id="be149-110">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="be149-110">VARIANT\_TRUE</span></span>

## <a name="applies-to"></a><span data-ttu-id="be149-111">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="be149-111">Applies To</span></span>

-   [<span data-ttu-id="be149-112">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="be149-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="be149-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="be149-113">Remarks</span></span>

<span data-ttu-id="be149-114">O preenchimento de ruído adiciona uma pequena quantidade de ruído a partes do sinal em que o recorte de centro removeu os ecos residuais.</span><span class="sxs-lookup"><span data-stu-id="be149-114">Noise filling adds a small amount of noise to portions of the signal where center clipping has removed the residual echoes.</span></span> <span data-ttu-id="be149-115">Isso resulta em uma melhor experiência para o usuário do que deixar lacunas silenciosas no sinal.</span><span class="sxs-lookup"><span data-stu-id="be149-115">This results in a better experience for the user than leaving silent gaps in the signal.</span></span>

<span data-ttu-id="be149-116">Essa propriedade pode ter os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="be149-116">This property can have the following values.</span></span>



| <span data-ttu-id="be149-117">Valor</span><span class="sxs-lookup"><span data-stu-id="be149-117">Value</span></span>          | <span data-ttu-id="be149-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="be149-118">Description</span></span>            |
|----------------|------------------------|
| <span data-ttu-id="be149-119">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="be149-119">VARIANT\_TRUE</span></span>  | <span data-ttu-id="be149-120">Habilite o preenchimento de ruído.</span><span class="sxs-lookup"><span data-stu-id="be149-120">Enable noise filling.</span></span>  |
| <span data-ttu-id="be149-121">VARIANTE \_ falso</span><span class="sxs-lookup"><span data-stu-id="be149-121">VARIANT\_FALSE</span></span> | <span data-ttu-id="be149-122">Desabilite o preenchimento de ruído.</span><span class="sxs-lookup"><span data-stu-id="be149-122">Disable noise filling.</span></span> |



 

<span data-ttu-id="be149-123">O valor padrão dessa propriedade é VARIANT \_ true (Enabled).</span><span class="sxs-lookup"><span data-stu-id="be149-123">The default value of this property is VARIANT\_TRUE (enabled).</span></span> <span data-ttu-id="be149-124">Antes de definir essa propriedade, você deve definir a propriedade [ \_ modo de \_ recurso \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) como Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="be149-124">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="be149-125">O DSP usa essa propriedade somente quando o processamento de AEC está habilitado.</span><span class="sxs-lookup"><span data-stu-id="be149-125">The DSP uses this property only when AEC processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="be149-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be149-126">Requirements</span></span>



| <span data-ttu-id="be149-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="be149-127">Requirement</span></span> | <span data-ttu-id="be149-128">Valor</span><span class="sxs-lookup"><span data-stu-id="be149-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be149-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be149-129">Minimum supported client</span></span><br/> | <span data-ttu-id="be149-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="be149-130">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="be149-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be149-131">Minimum supported server</span></span><br/> | <span data-ttu-id="be149-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="be149-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="be149-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="be149-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="be149-134"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="be149-134"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be149-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="be149-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be149-136">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="be149-136">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="be149-137">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="be149-137">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
