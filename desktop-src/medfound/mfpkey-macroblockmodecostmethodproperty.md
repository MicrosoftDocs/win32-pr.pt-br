---
description: Especifica o método de custo usado pelo codec para determinar qual modo de macrobloco usar.
ms.assetid: 2ba9b943-0daa-40c1-87ea-2fa647fb7095
title: Propriedade MFPKEY_MACROBLOCKMODECOSTMETHOD (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 289219300a79c67565891c48cec848851c17bd7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761015"
---
# <a name="mfpkey_macroblockmodecostmethod-property"></a><span data-ttu-id="e0db5-103">\_Propriedade MFPKEY MACROBLOCKMODECOSTMETHOD</span><span class="sxs-lookup"><span data-stu-id="e0db5-103">MFPKEY\_MACROBLOCKMODECOSTMETHOD Property</span></span>

<span data-ttu-id="e0db5-104">Especifica o método de custo usado pelo codec para determinar qual modo de macrobloco usar.</span><span class="sxs-lookup"><span data-stu-id="e0db5-104">Specifies the cost method used by the codec to determine which macroblock mode to use.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="e0db5-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="e0db5-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="e0db5-106">g \_ wszWMVCMacroblockModeCostMethod</span><span class="sxs-lookup"><span data-stu-id="e0db5-106">g\_wszWMVCMacroblockModeCostMethod</span></span>

## <a name="data-type"></a><span data-ttu-id="e0db5-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="e0db5-107">Data Type</span></span>

<span data-ttu-id="e0db5-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="e0db5-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="e0db5-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="e0db5-109">Default Value</span></span>

<span data-ttu-id="e0db5-110">0</span><span class="sxs-lookup"><span data-stu-id="e0db5-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="e0db5-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0db5-111">Remarks</span></span>

<span data-ttu-id="e0db5-112">Essa propriedade pode ser definida como um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e0db5-112">This property may be set to one of the following values.</span></span>



| <span data-ttu-id="e0db5-113">Valor</span><span class="sxs-lookup"><span data-stu-id="e0db5-113">Value</span></span> | <span data-ttu-id="e0db5-114">Método usado</span><span class="sxs-lookup"><span data-stu-id="e0db5-114">Method used</span></span>                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0db5-115">0</span><span class="sxs-lookup"><span data-stu-id="e0db5-115">0</span></span>     | <span data-ttu-id="e0db5-116">TRISTE/Hadamard.</span><span class="sxs-lookup"><span data-stu-id="e0db5-116">SAD/Hadamard.</span></span> <span data-ttu-id="e0db5-117">Esta opção configura o codec para usar apenas distorção ao calcular o custo.</span><span class="sxs-lookup"><span data-stu-id="e0db5-117">This option configures the codec to use only distortion when computing cost.</span></span>             |
| <span data-ttu-id="e0db5-118">1</span><span class="sxs-lookup"><span data-stu-id="e0db5-118">1</span></span>     | <span data-ttu-id="e0db5-119">Custo da área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="e0db5-119">RD cost.</span></span> <span data-ttu-id="e0db5-120">Esta opção configura o codec para considerar a taxa e a distorção ao calcular o custo.</span><span class="sxs-lookup"><span data-stu-id="e0db5-120">This option configures the codec to account for both rate and distortion when computing cost.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="e0db5-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0db5-121">Requirements</span></span>



| <span data-ttu-id="e0db5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0db5-122">Requirement</span></span> | <span data-ttu-id="e0db5-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e0db5-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0db5-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0db5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e0db5-125">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e0db5-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e0db5-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0db5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e0db5-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e0db5-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e0db5-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e0db5-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0db5-129"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0db5-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0db5-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0db5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0db5-131">MFPKEY \_ MOTIONMATCHMETHOD</span><span class="sxs-lookup"><span data-stu-id="e0db5-131">MFPKEY\_MOTIONMATCHMETHOD</span></span>](mfpkey-motionmatchmethodproperty.md)
</dt> <dt>

[<span data-ttu-id="e0db5-132">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e0db5-132">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




