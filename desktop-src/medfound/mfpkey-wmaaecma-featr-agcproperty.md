---
description: Especifica se o DSP de captura de voz executa o controle de lucro automático.
ms.assetid: 85ac8de0-ac36-4b34-a93d-0ac792a677b2
title: Propriedade MFPKEY_WMAAECMA_FEATR_AGC (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f42c7abd854b8fe18b5cfd4fe23ededb28faa6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813506"
---
# <a name="mfpkey_wmaaecma_featr_agc-property"></a><span data-ttu-id="0fb06-103">\_ \_ \_ Propriedade AGC do MFPKEY WMAAECMA</span><span class="sxs-lookup"><span data-stu-id="0fb06-103">MFPKEY\_WMAAECMA\_FEATR\_AGC Property</span></span>

<span data-ttu-id="0fb06-104">Especifica se o DSP de captura de voz executa o controle de lucro automático.</span><span class="sxs-lookup"><span data-stu-id="0fb06-104">Specifies whether the Voice Capture DSP performs automatic gain control.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="0fb06-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="0fb06-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="0fb06-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="0fb06-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="0fb06-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="0fb06-107">Data Type</span></span>

<span data-ttu-id="0fb06-108">BOOL do VT \_</span><span class="sxs-lookup"><span data-stu-id="0fb06-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="0fb06-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="0fb06-109">Default Value</span></span>

<span data-ttu-id="0fb06-110">VARIANTE \_ falso</span><span class="sxs-lookup"><span data-stu-id="0fb06-110">VARIANT\_FALSE</span></span>

## <a name="applies-to"></a><span data-ttu-id="0fb06-111">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="0fb06-111">Applies To</span></span>

-   [<span data-ttu-id="0fb06-112">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="0fb06-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="0fb06-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="0fb06-113">Remarks</span></span>

<span data-ttu-id="0fb06-114">O controle de lucro automático é um componente do DSP (processamento de sinal digital) que ajusta o lucro para que o nível de saída do sinal permaneça dentro do mesmo intervalo aproximado.</span><span class="sxs-lookup"><span data-stu-id="0fb06-114">Automatic gain control is a digital signal processing (DSP) component that adjusts the gain so that the output level of the signal remains within the same approximate range.</span></span>

<span data-ttu-id="0fb06-115">Essa propriedade pode ter os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="0fb06-115">This property can have the following values.</span></span>



| <span data-ttu-id="0fb06-116">Valor</span><span class="sxs-lookup"><span data-stu-id="0fb06-116">Value</span></span>          | <span data-ttu-id="0fb06-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="0fb06-117">Description</span></span>                     |
|----------------|---------------------------------|
| <span data-ttu-id="0fb06-118">VARIANTE \_ falso</span><span class="sxs-lookup"><span data-stu-id="0fb06-118">VARIANT\_FALSE</span></span> | <span data-ttu-id="0fb06-119">Desabilitar o controle de lucro automático.</span><span class="sxs-lookup"><span data-stu-id="0fb06-119">Disable automatic gain control.</span></span> |
| <span data-ttu-id="0fb06-120">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="0fb06-120">VARIANT\_TRUE</span></span>  | <span data-ttu-id="0fb06-121">Habilitar o controle de lucro automático.</span><span class="sxs-lookup"><span data-stu-id="0fb06-121">Enable automatic gain control.</span></span>  |



 

<span data-ttu-id="0fb06-122">O valor padrão dessa propriedade é VARIANT \_ false (Disabled).</span><span class="sxs-lookup"><span data-stu-id="0fb06-122">The default value of this property is VARIANT\_FALSE (disabled).</span></span> <span data-ttu-id="0fb06-123">Antes de definir essa propriedade, você deve definir a propriedade [ \_ modo de \_ recurso \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) como Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="0fb06-123">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fb06-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fb06-124">Requirements</span></span>



| <span data-ttu-id="0fb06-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fb06-125">Requirement</span></span> | <span data-ttu-id="0fb06-126">Valor</span><span class="sxs-lookup"><span data-stu-id="0fb06-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fb06-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0fb06-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0fb06-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0fb06-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0fb06-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0fb06-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0fb06-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0fb06-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0fb06-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0fb06-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fb06-132"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fb06-132"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fb06-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="0fb06-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fb06-134">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0fb06-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="0fb06-135">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="0fb06-135">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
