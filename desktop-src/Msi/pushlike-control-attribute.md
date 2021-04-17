---
description: Se esse bit for definido em uma caixa de seleção ou em um grupo de botões de opção, o botão será desenhado com a aparência de um botão de ação, mas sua lógica permanecerá a mesma. Se o bit não estiver definido, os controles serão desenhados em seu estilo normal.
ms.assetid: c30b383a-7fae-413a-a6e6-8e958009f10c
title: Atributo de controle PushLike
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 839adfceb0484bc908b8c8c6d14616cfd03acdb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760834"
---
# <a name="pushlike-control-attribute"></a><span data-ttu-id="a3c3f-104">Atributo de controle PushLike</span><span class="sxs-lookup"><span data-stu-id="a3c3f-104">PushLike Control Attribute</span></span>

<span data-ttu-id="a3c3f-105">Se esse bit for definido em uma caixa de seleção ou em um grupo de botões de opção, o botão será desenhado com a aparência de um botão de ação, mas sua lógica permanecerá a mesma.</span><span class="sxs-lookup"><span data-stu-id="a3c3f-105">If this bit is set on a check box or a radio button group, the button is drawn with the appearance of a push button, but its logic stays the same.</span></span> <span data-ttu-id="a3c3f-106">Se o bit não estiver definido, os controles serão desenhados em seu estilo normal.</span><span class="sxs-lookup"><span data-stu-id="a3c3f-106">If the bit is not set, the controls are drawn in their usual style.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="a3c3f-107">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="a3c3f-107">Valid Controls</span></span>

<span data-ttu-id="a3c3f-108">[](checkbox-control.md)[Botão de opção](radiobuttongroup-control.md) de caixa de seleção</span><span class="sxs-lookup"><span data-stu-id="a3c3f-108">[CheckBox](checkbox-control.md)[RadioButtonGroup](radiobuttongroup-control.md)</span></span>

## <a name="value"></a><span data-ttu-id="a3c3f-109">Valor</span><span class="sxs-lookup"><span data-stu-id="a3c3f-109">Value</span></span>



| <span data-ttu-id="a3c3f-110">Decimal</span><span class="sxs-lookup"><span data-stu-id="a3c3f-110">Decimal</span></span> | <span data-ttu-id="a3c3f-111">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="a3c3f-111">Hexadecimal</span></span> | <span data-ttu-id="a3c3f-112">Constante</span><span class="sxs-lookup"><span data-stu-id="a3c3f-112">Constant</span></span>                           |
|---------|-------------|------------------------------------|
| <span data-ttu-id="a3c3f-113">131072</span><span class="sxs-lookup"><span data-stu-id="a3c3f-113">131072</span></span>  | <span data-ttu-id="a3c3f-114">0x00020000</span><span class="sxs-lookup"><span data-stu-id="a3c3f-114">0x00020000</span></span>  | <span data-ttu-id="a3c3f-115">**msidbControlAttributesPushLike**</span><span class="sxs-lookup"><span data-stu-id="a3c3f-115">**msidbControlAttributesPushLike**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a3c3f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="a3c3f-116">Remarks</span></span>

<span data-ttu-id="a3c3f-117">Para definir esse atributo em um controle, inclua o bit PushLike na coluna atributos do registro do controle na [tabela de controle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="a3c3f-117">To set this attribute on a control, include the PushLike bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="a3c3f-118">Consulte [controlar atributos](control-attributes.md) e [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="a3c3f-118">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



