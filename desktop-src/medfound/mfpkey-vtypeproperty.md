---
description: Especifica a lógica que o codec usará para detectar o vídeo de origem entrelaçado.
ms.assetid: 29c7fc1c-2047-4562-ba14-48f9cfbfe68c
title: Propriedade MFPKEY_VTYPE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e95bab3120e60a2faa1a3be47c6459205f5f34d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827550"
---
# <a name="mfpkey_vtype-property"></a><span data-ttu-id="90605-103">\_Propriedade MFPKEY VTYPE</span><span class="sxs-lookup"><span data-stu-id="90605-103">MFPKEY\_VTYPE Property</span></span>

<span data-ttu-id="90605-104">Especifica a lógica que o codec usará para detectar o vídeo de origem entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="90605-104">Specifies the logic that the codec will use to detect interlaced source video.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="90605-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="90605-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="90605-106">g \_ wszWMVCVType</span><span class="sxs-lookup"><span data-stu-id="90605-106">g\_wszWMVCVType</span></span>

## <a name="data-type"></a><span data-ttu-id="90605-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="90605-107">Data Type</span></span>

<span data-ttu-id="90605-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="90605-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="90605-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="90605-109">Default Value</span></span>

<span data-ttu-id="90605-110">0</span><span class="sxs-lookup"><span data-stu-id="90605-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="90605-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="90605-111">Remarks</span></span>

<span data-ttu-id="90605-112">Essa propriedade pode ser definida como um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="90605-112">This property may be set to one of the following values.</span></span>



| <span data-ttu-id="90605-113">Valor</span><span class="sxs-lookup"><span data-stu-id="90605-113">Value</span></span> | <span data-ttu-id="90605-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="90605-114">Description</span></span>                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90605-115">0</span><span class="sxs-lookup"><span data-stu-id="90605-115">0</span></span>     | <span data-ttu-id="90605-116">O codec usará a lógica de detecção de tipo de quadro padrão.</span><span class="sxs-lookup"><span data-stu-id="90605-116">The codec will use the standard frame-type detection logic.</span></span>                                                                                 |
| <span data-ttu-id="90605-117">1</span><span class="sxs-lookup"><span data-stu-id="90605-117">1</span></span>     | <span data-ttu-id="90605-118">O codec tratará todos os quadros de vídeo de origem como quadros entrelaçados.</span><span class="sxs-lookup"><span data-stu-id="90605-118">The codec will treat all source video frames as interlaced frames.</span></span>                                                                          |
| <span data-ttu-id="90605-119">2</span><span class="sxs-lookup"><span data-stu-id="90605-119">2</span></span>     | <span data-ttu-id="90605-120">O codec tratará todos os quadros de vídeo de origem como campos de vídeo entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="90605-120">The codec will treat all source video frames as fields of interlaced video.</span></span>                                                                 |
| <span data-ttu-id="90605-121">3</span><span class="sxs-lookup"><span data-stu-id="90605-121">3</span></span>     | <span data-ttu-id="90605-122">O codec determinará automaticamente se os quadros de vídeo de entrada são quadros entrelaçados ou campos de vídeo entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="90605-122">The codec will automatically determine whether input video frames are interlaced frames or fields of interlaced video.</span></span>                      |
| <span data-ttu-id="90605-123">4</span><span class="sxs-lookup"><span data-stu-id="90605-123">4</span></span>     | <span data-ttu-id="90605-124">O codec determinará automaticamente se os quadros de vídeo de entrada são quadros progressivos, quadros entrelaçados ou campos de vídeo entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="90605-124">The codec will automatically determine whether input video frames are progressive frames, interlaced frames, or fields of interlaced video.</span></span> |



 

<span data-ttu-id="90605-125">Essa propriedade determina o método de codificação de imagem usado para codificação de vídeo progressiva ou entrelaçada.</span><span class="sxs-lookup"><span data-stu-id="90605-125">This property determines the picture encoding method used for progressive or interlaced video encoding.</span></span>

<span data-ttu-id="90605-126">Se nenhum tipo de vídeo for especificado, o codec usará a codificação de quadro progressivo para sessões de codificação progressiva e a codificação entrelaçada de campo para sessões de codificação entrelaçadas.</span><span class="sxs-lookup"><span data-stu-id="90605-126">If no video type is specified, the codec will use progressive frame encoding for progressive encoding sessions, and field interlaced encoding for interlaced encoding sessions.</span></span> <span data-ttu-id="90605-127">O tipo de sessão de codificação de vídeo (progressiva ou entrelaçada) é definido usando a propriedade [MFPKEY \_ INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="90605-127">The type of video encoding session (progressive or interlaced) is set by using the [MFPKEY\_INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) property.</span></span>

> [!Note]  
> <span data-ttu-id="90605-128">A propriedade [MFPKEY \_ INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) deve ser definida como Variant \_ true para produzir uma saída entrelaçada; caso contrário, a definição da \_ Propriedade MPFKEY VTYPE não terá efeito.</span><span class="sxs-lookup"><span data-stu-id="90605-128">The [MFPKEY\_INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) property must be set to VARIANT\_TRUE in order to produce interlaced output; otherwise, setting the MPFKEY\_VTYPE property will have no effect.</span></span>

 

<span data-ttu-id="90605-129">Quando o vídeo entrelaçado está sendo codificado, é possível especificar vários métodos de codificação de imagem.</span><span class="sxs-lookup"><span data-stu-id="90605-129">When interlaced video is being encoded, it is possible to specify several picture encoding methods.</span></span> <span data-ttu-id="90605-130">Normalmente, a maneira mais eficiente de codificar vídeo entrelaçado é usar o método entrelaçado de campo (2).</span><span class="sxs-lookup"><span data-stu-id="90605-130">Typically the most efficient way to encode interlaced video is to use the field interlaced method (2).</span></span> <span data-ttu-id="90605-131">Se o vídeo de origem contiver muito pouco movimento, o método entrelaçado do quadro (1) ou o método de quadro/campo automático (2) poderá ser mais adequado.</span><span class="sxs-lookup"><span data-stu-id="90605-131">If the source video contains very little motion, the frame interlaced method (1) or the auto frame/field method (2) might be more suitable.</span></span>

<span data-ttu-id="90605-132">Ao codificar conteúdo misto (contendo quadros progressivos e entrelaçados), é melhor usar o método de valor quadro automático/campo/progressivo (4).</span><span class="sxs-lookup"><span data-stu-id="90605-132">When encoding mixed content (containing both progressive and interlaced frames), it's best to use the value auto frame/field/progressive method (4).</span></span>

## <a name="requirements"></a><span data-ttu-id="90605-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90605-133">Requirements</span></span>



| <span data-ttu-id="90605-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="90605-134">Requirement</span></span> | <span data-ttu-id="90605-135">Valor</span><span class="sxs-lookup"><span data-stu-id="90605-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="90605-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90605-136">Minimum supported client</span></span><br/> | <span data-ttu-id="90605-137">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="90605-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="90605-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90605-138">Minimum supported server</span></span><br/> | <span data-ttu-id="90605-139">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="90605-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="90605-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="90605-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="90605-141"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="90605-141"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90605-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="90605-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90605-143">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="90605-143">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




