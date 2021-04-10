---
description: Especifica o intervalo usado em pesquisas de movimento.
ms.assetid: b2026f47-ac39-4276-8359-c939b202f00c
title: Propriedade MFPKEY_MOTIONSEARCHRANGE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c557ea1a462192434222e425dccb8b9a0e291986
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165386"
---
# <a name="mfpkey_motionsearchrange-property"></a><span data-ttu-id="b414d-103">\_Propriedade MFPKEY MOTIONSEARCHRANGE</span><span class="sxs-lookup"><span data-stu-id="b414d-103">MFPKEY\_MOTIONSEARCHRANGE Property</span></span>

<span data-ttu-id="b414d-104">Especifica o intervalo usado em pesquisas de movimento.</span><span class="sxs-lookup"><span data-stu-id="b414d-104">Specifies the range used in motion searches.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="b414d-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="b414d-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="b414d-106">g \_ wszWMVCMotionSearchRange</span><span class="sxs-lookup"><span data-stu-id="b414d-106">g\_wszWMVCMotionSearchRange</span></span>

## <a name="data-type"></a><span data-ttu-id="b414d-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="b414d-107">Data Type</span></span>

<span data-ttu-id="b414d-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="b414d-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="b414d-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="b414d-109">Default Value</span></span>

<span data-ttu-id="b414d-110">0</span><span class="sxs-lookup"><span data-stu-id="b414d-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="b414d-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b414d-111">Remarks</span></span>

<span data-ttu-id="b414d-112">Essa propriedade pode ser definida como um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="b414d-112">This property may be set to one of the following values.</span></span> <span data-ttu-id="b414d-113">H denota intervalo horizontal e V denota intervalo vertical.</span><span class="sxs-lookup"><span data-stu-id="b414d-113">H denotes horizontal range and V denotes vertical range.</span></span> <span data-ttu-id="b414d-114">Todos os intervalos são fornecidos em pixels.</span><span class="sxs-lookup"><span data-stu-id="b414d-114">All ranges are given in pixels.</span></span>



| <span data-ttu-id="b414d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="b414d-115">Value</span></span> | <span data-ttu-id="b414d-116">Intervalo</span><span class="sxs-lookup"><span data-stu-id="b414d-116">Range</span></span>                                |
|-------|--------------------------------------|
| <span data-ttu-id="b414d-117">0</span><span class="sxs-lookup"><span data-stu-id="b414d-117">0</span></span>     | <span data-ttu-id="b414d-118">+ 63.75/-64.0 H, + 31.75/-32.0 V</span><span class="sxs-lookup"><span data-stu-id="b414d-118">+63.75/-64.0 H, +31.75/-32.0 V</span></span>       |
| <span data-ttu-id="b414d-119">1</span><span class="sxs-lookup"><span data-stu-id="b414d-119">1</span></span>     | <span data-ttu-id="b414d-120">+127,75/-128 H, +63,75/-64 V</span><span class="sxs-lookup"><span data-stu-id="b414d-120">+127.75/-128.0 H, +63.75/-64.0 V</span></span>     |
| <span data-ttu-id="b414d-121">2</span><span class="sxs-lookup"><span data-stu-id="b414d-121">2</span></span>     | <span data-ttu-id="b414d-122">+ 511.75/-512.0 H, + 127.75/-128.0 V</span><span class="sxs-lookup"><span data-stu-id="b414d-122">+511.75/-512.0 H, +127.75/-128.0 V</span></span>   |
| <span data-ttu-id="b414d-123">3</span><span class="sxs-lookup"><span data-stu-id="b414d-123">3</span></span>     | <span data-ttu-id="b414d-124">+ 1023.75/-1024.0 H, + 255.75/-256.0 V</span><span class="sxs-lookup"><span data-stu-id="b414d-124">+1023.75/-1024.0 H, +255.75/-256.0 V</span></span> |
| <span data-ttu-id="b414d-125">-1</span><span class="sxs-lookup"><span data-stu-id="b414d-125">-1</span></span>    | <span data-ttu-id="b414d-126">Macrobloco-adaptável (automático)</span><span class="sxs-lookup"><span data-stu-id="b414d-126">Macroblock-adaptive (automatic)</span></span>      |



 

<span data-ttu-id="b414d-127">Essa propriedade controla o tamanho da área do quadro em que o codec pesquisará um elemento que pode ter exibido o movimento entre os quadros.</span><span class="sxs-lookup"><span data-stu-id="b414d-127">This property controls the size of the frame area that the codec will search for an element that may have exhibited motion between frames.</span></span> <span data-ttu-id="b414d-128">Uma janela de pesquisa maior ajudará a encontrar um movimento mais rápido, mas exigirá mais tempo de CPU.</span><span class="sxs-lookup"><span data-stu-id="b414d-128">A larger search window will help find faster motion but will require more CPU time.</span></span> <span data-ttu-id="b414d-129">Os requisitos de CPU são aproximadamente dobrados em cada nível.</span><span class="sxs-lookup"><span data-stu-id="b414d-129">The CPU requirements are approximately doubled at each level.</span></span>

<span data-ttu-id="b414d-130">O modo automático (-1) selecionará dinamicamente o modo mais eficiente.</span><span class="sxs-lookup"><span data-stu-id="b414d-130">The automatic mode (-1) will dynamically select the most efficient mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="b414d-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b414d-131">Requirements</span></span>



| <span data-ttu-id="b414d-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="b414d-132">Requirement</span></span> | <span data-ttu-id="b414d-133">Valor</span><span class="sxs-lookup"><span data-stu-id="b414d-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b414d-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b414d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b414d-135">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b414d-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b414d-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b414d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b414d-137">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b414d-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b414d-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b414d-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="b414d-139"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b414d-139"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b414d-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="b414d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b414d-141">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b414d-141">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




