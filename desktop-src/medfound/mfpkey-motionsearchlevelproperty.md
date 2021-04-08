---
description: Especifica como as informações de cores são usadas em operações de pesquisa de movimento.
ms.assetid: a625b103-0a55-4268-a01a-6a464a56fec2
title: Propriedade MFPKEY_MOTIONSEARCHLEVEL (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 231c2c0ae70466d41f4bf348ec47ee0a74cb135b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010842"
---
# <a name="mfpkey_motionsearchlevel-property"></a><span data-ttu-id="70cb9-103">\_Propriedade MFPKEY MOTIONSEARCHLEVEL</span><span class="sxs-lookup"><span data-stu-id="70cb9-103">MFPKEY\_MOTIONSEARCHLEVEL Property</span></span>

<span data-ttu-id="70cb9-104">Especifica como as informações de cores são usadas em operações de pesquisa de movimento.</span><span class="sxs-lookup"><span data-stu-id="70cb9-104">Specifies how color information is used in motion search operations.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="70cb9-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="70cb9-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="70cb9-106">g \_ wszWMVCMotionSearchLevel</span><span class="sxs-lookup"><span data-stu-id="70cb9-106">g\_wszWMVCMotionSearchLevel</span></span>

## <a name="data-type"></a><span data-ttu-id="70cb9-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="70cb9-107">Data Type</span></span>

<span data-ttu-id="70cb9-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="70cb9-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="70cb9-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="70cb9-109">Default Value</span></span>

<span data-ttu-id="70cb9-110">0</span><span class="sxs-lookup"><span data-stu-id="70cb9-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="70cb9-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="70cb9-111">Remarks</span></span>

<span data-ttu-id="70cb9-112">Essa propriedade pode ser definida como um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="70cb9-112">This property may be set to one of the following values.</span></span>



| <span data-ttu-id="70cb9-113">Valor</span><span class="sxs-lookup"><span data-stu-id="70cb9-113">Value</span></span> | <span data-ttu-id="70cb9-114">Informações de vídeo usadas</span><span class="sxs-lookup"><span data-stu-id="70cb9-114">Video information used</span></span>                           |
|-------|--------------------------------------------------|
| <span data-ttu-id="70cb9-115">0</span><span class="sxs-lookup"><span data-stu-id="70cb9-115">0</span></span>     | <span data-ttu-id="70cb9-116">Somente Luma.</span><span class="sxs-lookup"><span data-stu-id="70cb9-116">Luma only.</span></span>                                       |
| <span data-ttu-id="70cb9-117">1</span><span class="sxs-lookup"><span data-stu-id="70cb9-117">1</span></span>     | <span data-ttu-id="70cb9-118">Luma com croma de inteiro mais próximo.</span><span class="sxs-lookup"><span data-stu-id="70cb9-118">Luma with nearest-integer chroma.</span></span>                |
| <span data-ttu-id="70cb9-119">2</span><span class="sxs-lookup"><span data-stu-id="70cb9-119">2</span></span>     | <span data-ttu-id="70cb9-120">Luma com a croma verdadeira.</span><span class="sxs-lookup"><span data-stu-id="70cb9-120">Luma with true chroma.</span></span>                           |
| <span data-ttu-id="70cb9-121">-1</span><span class="sxs-lookup"><span data-stu-id="70cb9-121">-1</span></span>    | <span data-ttu-id="70cb9-122">Macrobloco-adaptativo com verdadeiro croma.</span><span class="sxs-lookup"><span data-stu-id="70cb9-122">Macroblock-adaptive with true chroma.</span></span>            |
| <span data-ttu-id="70cb9-123">-2</span><span class="sxs-lookup"><span data-stu-id="70cb9-123">-2</span></span>    | <span data-ttu-id="70cb9-124">Macrobloco-Adaptive com croma de inteiros mais próximo.</span><span class="sxs-lookup"><span data-stu-id="70cb9-124">Macroblock-adaptive with nearest-integer chroma.</span></span> |



 

<span data-ttu-id="70cb9-125">Por padrão, o codec executa a pesquisa de movimento somente no canal Luma.</span><span class="sxs-lookup"><span data-stu-id="70cb9-125">By default, the codec performs motion search only in the luma channel.</span></span> <span data-ttu-id="70cb9-126">Incluir informações de croma em estimativa de movimento pode melhorar significativamente a qualidade do vídeo codificado.</span><span class="sxs-lookup"><span data-stu-id="70cb9-126">Including chroma information in motion estimation can significantly improve the quality of encoded video.</span></span> <span data-ttu-id="70cb9-127">A pesquisa de movimento com Luma e true croma resultará na melhor qualidade de vídeo, mas com o custo de desempenho mais alto.</span><span class="sxs-lookup"><span data-stu-id="70cb9-127">Motion search with luma and true chroma will yield the best video quality, but at the highest performance cost.</span></span> <span data-ttu-id="70cb9-128">Os dois modos dinâmicos (-1 e-2) e o Luma com o modo de croma de inteiro mais próximo fornecerão comprometimentos razoáveis entre qualidade e desempenho.</span><span class="sxs-lookup"><span data-stu-id="70cb9-128">The two dynamic modes (-1 and -2) and the luma with nearest-integer chroma mode will provide reasonable compromises between quality and performance.</span></span>

## <a name="requirements"></a><span data-ttu-id="70cb9-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70cb9-129">Requirements</span></span>



| <span data-ttu-id="70cb9-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="70cb9-130">Requirement</span></span> | <span data-ttu-id="70cb9-131">Valor</span><span class="sxs-lookup"><span data-stu-id="70cb9-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70cb9-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70cb9-132">Minimum supported client</span></span><br/> | <span data-ttu-id="70cb9-133">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="70cb9-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="70cb9-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70cb9-134">Minimum supported server</span></span><br/> | <span data-ttu-id="70cb9-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="70cb9-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="70cb9-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="70cb9-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="70cb9-137"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="70cb9-137"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70cb9-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="70cb9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70cb9-139">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="70cb9-139">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




