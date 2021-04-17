---
description: Especifica a duração do eco que o algoritmo de cancelamento de eco acústico (AEC) pode manipular, em milissegundos.
ms.assetid: d451b90f-7ef7-4f66-be83-aca93e3ad894
title: Propriedade MFPKEY_WMAAECMA_FEATR_ECHO_LENGTH (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d66f7dcc4764447495e0f3ae55d2d038c2a8d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783774"
---
# <a name="mfpkey_wmaaecma_featr_echo_length-property"></a><span data-ttu-id="222a5-103">\_Propriedade de \_ comprimento de \_ eco \_ do MFPKEY WMAAECMA</span><span class="sxs-lookup"><span data-stu-id="222a5-103">MFPKEY\_WMAAECMA\_FEATR\_ECHO\_LENGTH Property</span></span>

<span data-ttu-id="222a5-104">Especifica a duração do eco que o algoritmo de cancelamento de eco acústico (AEC) pode manipular, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="222a5-104">Specifies the duration of echo that the acoustic echo cancellation (AEC) algorithm can handle, in milliseconds.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="222a5-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="222a5-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="222a5-106">Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="222a5-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="222a5-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="222a5-107">Data Type</span></span>

<span data-ttu-id="222a5-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="222a5-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="222a5-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="222a5-109">Default Value</span></span>

<span data-ttu-id="222a5-110">256</span><span class="sxs-lookup"><span data-stu-id="222a5-110">256</span></span>

## <a name="applies-to"></a><span data-ttu-id="222a5-111">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="222a5-111">Applies To</span></span>

-   [<span data-ttu-id="222a5-112">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="222a5-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="222a5-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="222a5-113">Remarks</span></span>

<span data-ttu-id="222a5-114">O algoritmo AEC usa um filtro adaptável cujo comprimento é determinado pela duração do eco.</span><span class="sxs-lookup"><span data-stu-id="222a5-114">The AEC algorithm uses an adaptive filter whose length is determined by the duration of the echo.</span></span> <span data-ttu-id="222a5-115">É recomendável que os aplicativos usem um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="222a5-115">It is recommended that applications use one of the following values:</span></span>

-   <span data-ttu-id="222a5-116">128</span><span class="sxs-lookup"><span data-stu-id="222a5-116">128</span></span>
-   <span data-ttu-id="222a5-117">256</span><span class="sxs-lookup"><span data-stu-id="222a5-117">256</span></span>
-   <span data-ttu-id="222a5-118">512</span><span class="sxs-lookup"><span data-stu-id="222a5-118">512</span></span>
-   <span data-ttu-id="222a5-119">1024</span><span class="sxs-lookup"><span data-stu-id="222a5-119">1024</span></span>

<span data-ttu-id="222a5-120">O valor padrão é 256 milissegundos, o que é suficiente para a maioria dos ambientes domésticos e do Office.</span><span class="sxs-lookup"><span data-stu-id="222a5-120">The default value is 256 milliseconds, which is sufficient for most office and home environments.</span></span> <span data-ttu-id="222a5-121">Antes de definir essa propriedade, você deve definir a propriedade [ \_ modo de \_ recurso \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) como Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="222a5-121">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="222a5-122">O DSP usa essa propriedade somente quando o processamento de AEC está habilitado.</span><span class="sxs-lookup"><span data-stu-id="222a5-122">The DSP uses this property only when AEC processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="222a5-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="222a5-123">Requirements</span></span>



| <span data-ttu-id="222a5-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="222a5-124">Requirement</span></span> | <span data-ttu-id="222a5-125">Valor</span><span class="sxs-lookup"><span data-stu-id="222a5-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="222a5-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="222a5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="222a5-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="222a5-127">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="222a5-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="222a5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="222a5-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="222a5-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="222a5-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="222a5-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="222a5-131"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="222a5-131"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="222a5-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="222a5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="222a5-133">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="222a5-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="222a5-134">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="222a5-134">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
