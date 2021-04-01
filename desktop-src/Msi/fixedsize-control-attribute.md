---
description: Se o bit de controle FixedSize for definido, a imagem será cortada ou centralizada no controle sem alterar sua forma ou tamanho.
ms.assetid: fb1ef0ba-5183-4708-a47d-26c83584df6c
title: Atributo de controle FixedSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4ee044860b79e56998da68dc6ddf4926e9115ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647060"
---
# <a name="fixedsize-control-attribute"></a><span data-ttu-id="fe22c-103">Atributo de controle FixedSize</span><span class="sxs-lookup"><span data-stu-id="fe22c-103">FixedSize Control Attribute</span></span>

<span data-ttu-id="fe22c-104">Se o bit de controle FixedSize for definido, a imagem será cortada ou centralizada no controle sem alterar sua forma ou tamanho.</span><span class="sxs-lookup"><span data-stu-id="fe22c-104">If the FixedSize Control bit is set, the picture is cropped or centered in the control without changing its shape or size.</span></span>

<span data-ttu-id="fe22c-105">Se esse bit não estiver definido, a imagem será ampliada para se ajustar ao controle.</span><span class="sxs-lookup"><span data-stu-id="fe22c-105">If this bit is not set the picture is stretched to fit the control.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="fe22c-106">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="fe22c-106">Valid Controls</span></span>

[<span data-ttu-id="fe22c-107">Bitmap</span><span class="sxs-lookup"><span data-stu-id="fe22c-107">Bitmap</span></span>](bitmap-control.md)

[<span data-ttu-id="fe22c-108">CheckBox</span><span class="sxs-lookup"><span data-stu-id="fe22c-108">CheckBox</span></span>](checkbox-control.md)

[<span data-ttu-id="fe22c-109">Ícone</span><span class="sxs-lookup"><span data-stu-id="fe22c-109">Icon</span></span>](icon-control.md)

[<span data-ttu-id="fe22c-110">Botão</span><span class="sxs-lookup"><span data-stu-id="fe22c-110">PushButton</span></span>](pushbutton-control.md)

[<span data-ttu-id="fe22c-111">Botão de opção</span><span class="sxs-lookup"><span data-stu-id="fe22c-111">RadioButtonGroup</span></span>](radiobuttongroup-control.md)

## <a name="value"></a><span data-ttu-id="fe22c-112">Valor</span><span class="sxs-lookup"><span data-stu-id="fe22c-112">Value</span></span>



| <span data-ttu-id="fe22c-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="fe22c-113">Decimal</span></span> | <span data-ttu-id="fe22c-114">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="fe22c-114">Hexadecimal</span></span> | <span data-ttu-id="fe22c-115">Constante</span><span class="sxs-lookup"><span data-stu-id="fe22c-115">Constant</span></span>                            |
|---------|-------------|-------------------------------------|
| <span data-ttu-id="fe22c-116">1048576</span><span class="sxs-lookup"><span data-stu-id="fe22c-116">1048576</span></span> | <span data-ttu-id="fe22c-117">0x00100000</span><span class="sxs-lookup"><span data-stu-id="fe22c-117">0x00100000</span></span>  | <span data-ttu-id="fe22c-118">**msidbControlAttributesFixedSize**</span><span class="sxs-lookup"><span data-stu-id="fe22c-118">**msidbControlAttributesFixedSize**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fe22c-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe22c-119">Remarks</span></span>

<span data-ttu-id="fe22c-120">Para definir esse atributo em um controle, inclua o bit FixedSize na coluna atributos do registro do controle na [tabela de controle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="fe22c-120">To set this attribute on a control, include the FixedSize bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="fe22c-121">Definir o bit FixedSize não terá nenhum efeito em [uma caixa de seleção](checkbox-control.md), um botão de [pressão](pushbutton-control.md)ou um grupo de [botões](radiobuttongroup-control.md) , se nem o [bitmap](bitmap-control-attribute.md) ou o [ícone](icon-control-attribute.md) tiverem sido definidos.</span><span class="sxs-lookup"><span data-stu-id="fe22c-121">Setting the FixedSize bit has no effect on a [CheckBox](checkbox-control.md), [PushButton](pushbutton-control.md), or [RadioButtonGroup](radiobuttongroup-control.md) if neither the [Bitmap](bitmap-control-attribute.md) or the [Icon](icon-control-attribute.md) have been set.</span></span>

<span data-ttu-id="fe22c-122">Definir o bit FixedSize não terá nenhum efeito sobre um controle de ícone ou uma pressão associada a um ícone se os bits de [ícones](iconsize-control-attribute.md) não estiverem definidos.</span><span class="sxs-lookup"><span data-stu-id="fe22c-122">Setting the FixedSize bit has no effect on an Icon control, or a PushButton associated with an icon, if the [IconSize](iconsize-control-attribute.md) bits is not set.</span></span>

<span data-ttu-id="fe22c-123">Consulte [atributos de controle](control-attributes.md) e o controle que você precisa criar sob [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="fe22c-123">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



