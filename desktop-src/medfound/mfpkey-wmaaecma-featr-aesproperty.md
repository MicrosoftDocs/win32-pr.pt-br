---
description: Especifica quantas vezes o DSP de captura de voz executa a supressão de eco acústico (AES) no sinal restante.
ms.assetid: 409b40f8-38eb-49f7-be30-348ab5cdd33a
title: Propriedade MFPKEY_WMAAECMA_FEATR_AES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5da7505a259a51ca8456f3caffa153790649320
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752173"
---
# <a name="mfpkey_wmaaecma_featr_aes-property"></a><span data-ttu-id="d6052-103">\_ \_ \_ Propriedade AES do MFPKEY WMAAECMA</span><span class="sxs-lookup"><span data-stu-id="d6052-103">MFPKEY\_WMAAECMA\_FEATR\_AES Property</span></span>

<span data-ttu-id="d6052-104">Especifica quantas vezes o DSP de captura de voz executa a supressão de eco acústico (AES) no sinal restante.</span><span class="sxs-lookup"><span data-stu-id="d6052-104">Specifies how many times the Voice Capture DSP performs acoustic echo suppression (AES) on the residual signal.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="d6052-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="d6052-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="d6052-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="d6052-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="d6052-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="d6052-107">Data Type</span></span>

<span data-ttu-id="d6052-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="d6052-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="d6052-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="d6052-109">Default Value</span></span>

<span data-ttu-id="d6052-110">0</span><span class="sxs-lookup"><span data-stu-id="d6052-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="d6052-111">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="d6052-111">Applies To</span></span>

-   [<span data-ttu-id="d6052-112">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="d6052-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="d6052-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6052-113">Remarks</span></span>

<span data-ttu-id="d6052-114">O DSP de captura de voz pode executar o AES no sinal residual após o cancelamento do eco.</span><span class="sxs-lookup"><span data-stu-id="d6052-114">The Voice Capture DSP can perform AES on the residual signal after echo cancellation.</span></span> <span data-ttu-id="d6052-115">Essa propriedade pode ter o valor 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="d6052-115">This property can have the value 0, 1, or 2.</span></span> <span data-ttu-id="d6052-116">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="d6052-116">The default value is 0.</span></span> <span data-ttu-id="d6052-117">Antes de definir essa propriedade, você deve definir a propriedade [ \_ modo de \_ recurso \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) como Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="d6052-117">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="d6052-118">O DSP usa essa propriedade somente quando o processamento de AEC está habilitado.</span><span class="sxs-lookup"><span data-stu-id="d6052-118">The DSP uses this property only when AEC processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6052-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6052-119">Requirements</span></span>



| <span data-ttu-id="d6052-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6052-120">Requirement</span></span> | <span data-ttu-id="d6052-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d6052-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6052-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6052-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d6052-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d6052-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d6052-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6052-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d6052-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d6052-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d6052-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d6052-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6052-127"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6052-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6052-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6052-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6052-129">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d6052-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="d6052-130">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="d6052-130">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
