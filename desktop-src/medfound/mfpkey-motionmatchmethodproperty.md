---
description: Especifica o método a ser usado para a correspondência de movimento.
ms.assetid: 75bbc189-3092-4813-9f45-54e8e48b05cd
title: Propriedade MFPKEY_MOTIONMATCHMETHOD (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09496e714633dd394f55122b7461f29a2daa3656
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921397"
---
# <a name="mfpkey_motionmatchmethod-property"></a><span data-ttu-id="8314d-103">\_Propriedade MFPKEY MOTIONMATCHMETHOD</span><span class="sxs-lookup"><span data-stu-id="8314d-103">MFPKEY\_MOTIONMATCHMETHOD Property</span></span>

<span data-ttu-id="8314d-104">Especifica o método a ser usado para a correspondência de movimento.</span><span class="sxs-lookup"><span data-stu-id="8314d-104">Specifies the method to use for motion matching.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="8314d-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="8314d-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="8314d-106">g \_ wszWMVCMotionMatchMethod</span><span class="sxs-lookup"><span data-stu-id="8314d-106">g\_wszWMVCMotionMatchMethod</span></span>

## <a name="data-type"></a><span data-ttu-id="8314d-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="8314d-107">Data Type</span></span>

<span data-ttu-id="8314d-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="8314d-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="8314d-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="8314d-109">Default Value</span></span>

<span data-ttu-id="8314d-110">0</span><span class="sxs-lookup"><span data-stu-id="8314d-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="8314d-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="8314d-111">Remarks</span></span>

<span data-ttu-id="8314d-112">Essa propriedade pode ser definida como um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8314d-112">This property may be set to one of the following values.</span></span>



| <span data-ttu-id="8314d-113">Valor</span><span class="sxs-lookup"><span data-stu-id="8314d-113">Value</span></span> | <span data-ttu-id="8314d-114">Método usado</span><span class="sxs-lookup"><span data-stu-id="8314d-114">Method used</span></span>                       |
|-------|-----------------------------------|
| <span data-ttu-id="8314d-115">0</span><span class="sxs-lookup"><span data-stu-id="8314d-115">0</span></span>     | <span data-ttu-id="8314d-116">soma de diferenças absolutas (SAD)</span><span class="sxs-lookup"><span data-stu-id="8314d-116">sum of absolute differences (SAD)</span></span> |
| <span data-ttu-id="8314d-117">1</span><span class="sxs-lookup"><span data-stu-id="8314d-117">1</span></span>     | <span data-ttu-id="8314d-118">Hadamard</span><span class="sxs-lookup"><span data-stu-id="8314d-118">Hadamard</span></span>                          |
| <span data-ttu-id="8314d-119">-1</span><span class="sxs-lookup"><span data-stu-id="8314d-119">-1</span></span>    | <span data-ttu-id="8314d-120">Macrobloco.</span><span class="sxs-lookup"><span data-stu-id="8314d-120">Macroblock-adaptive.</span></span>              |



 

<span data-ttu-id="8314d-121">A soma das diferenças absolutas (triste) é um método mais rápido, mas menos preciso do que a transformação Hadamard.</span><span class="sxs-lookup"><span data-stu-id="8314d-121">The sum of absolute differences (SAD) is a faster but less accurate method than the Hadamard transform.</span></span> <span data-ttu-id="8314d-122">A transformação Hadamard é mais precisa, mas computacionalmente intensiva.</span><span class="sxs-lookup"><span data-stu-id="8314d-122">The Hadamard transform is more accurate but computationally intensive.</span></span> <span data-ttu-id="8314d-123">O modo adaptável macrobloco fornece um comprometimento razoável entre os dois métodos, escolhendo dinamicamente entre as duas transformações, selecionando a transformação Hadamard somente quando apropriado.</span><span class="sxs-lookup"><span data-stu-id="8314d-123">The macroblock-adaptive mode provides a reasonable compromise between the two methods by dynamically choosing between the two transforms, selecting the Hadamard transform only when appropriate.</span></span>

## <a name="requirements"></a><span data-ttu-id="8314d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8314d-124">Requirements</span></span>



| <span data-ttu-id="8314d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8314d-125">Requirement</span></span> | <span data-ttu-id="8314d-126">Valor</span><span class="sxs-lookup"><span data-stu-id="8314d-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8314d-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8314d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8314d-128">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8314d-128">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8314d-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8314d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8314d-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8314d-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8314d-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8314d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="8314d-132"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8314d-132"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8314d-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="8314d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8314d-134">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8314d-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




