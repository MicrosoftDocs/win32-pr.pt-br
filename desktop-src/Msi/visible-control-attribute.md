---
description: Se o bit de controle visível estiver definido, o controle ficará visível na caixa de diálogo. Se esse bit não estiver definido, o controle ficará oculto na caixa de diálogo. O estado visível ou oculto do atributo de controle visível pode ser alterado posteriormente por um evento de controle.
ms.assetid: 77d3164c-ea8a-4dcf-afd5-02bb2c2568c6
title: Atributo de controle visível
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550513f6bd0e40e58694c2c15a9986b5b02f289c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790029"
---
# <a name="visible-control-attribute"></a><span data-ttu-id="6f6b6-105">Atributo de controle visível</span><span class="sxs-lookup"><span data-stu-id="6f6b6-105">Visible Control Attribute</span></span>

<span data-ttu-id="6f6b6-106">Se o bit de controle visível estiver definido, o controle ficará visível na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6f6b6-106">If the Visible Control bit is set, the control is visible on the dialog box.</span></span> <span data-ttu-id="6f6b6-107">Se esse bit não estiver definido, o controle ficará oculto na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6f6b6-107">If this bit is not set, the control is hidden on the dialog box.</span></span> <span data-ttu-id="6f6b6-108">O estado visível ou oculto do atributo de controle visível pode ser alterado posteriormente por um [evento de controle](control-events.md).</span><span class="sxs-lookup"><span data-stu-id="6f6b6-108">The visible or hidden state of the Visible control attribute can be later changed by a [Control Event](control-events.md).</span></span>

## <a name="valid-controls"></a><span data-ttu-id="6f6b6-109">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="6f6b6-109">Valid Controls</span></span>

<span data-ttu-id="6f6b6-110">Todos os controles.</span><span class="sxs-lookup"><span data-stu-id="6f6b6-110">All controls.</span></span>

## <a name="value"></a><span data-ttu-id="6f6b6-111">Valor</span><span class="sxs-lookup"><span data-stu-id="6f6b6-111">Value</span></span>



| <span data-ttu-id="6f6b6-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="6f6b6-112">Decimal</span></span> | <span data-ttu-id="6f6b6-113">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="6f6b6-113">Hexadecimal</span></span> | <span data-ttu-id="6f6b6-114">Constante</span><span class="sxs-lookup"><span data-stu-id="6f6b6-114">Constant</span></span>                          |
|---------|-------------|-----------------------------------|
| <span data-ttu-id="6f6b6-115">1</span><span class="sxs-lookup"><span data-stu-id="6f6b6-115">1</span></span>       | <span data-ttu-id="6f6b6-116">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6f6b6-116">0x00000001</span></span>  | <span data-ttu-id="6f6b6-117">**msidbControlAttributesVisible**</span><span class="sxs-lookup"><span data-stu-id="6f6b6-117">**msidbControlAttributesVisible**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6f6b6-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f6b6-118">Remarks</span></span>

<span data-ttu-id="6f6b6-119">Você pode usar a [tabela ControlCondition](controlcondition-table.md) para mostrar ou ocultar um controle de acordo com o valor de uma propriedade ou instrução condicional.</span><span class="sxs-lookup"><span data-stu-id="6f6b6-119">You can use the [ControlCondition table](controlcondition-table.md) to show or hide a control according to the value of a property or conditional statement.</span></span> <span data-ttu-id="6f6b6-120">Você também pode mostrar ou ocultar um controle assinando o controle em um [ControlEvent,](control-events.md).</span><span class="sxs-lookup"><span data-stu-id="6f6b6-120">You can also show or hide a control by subscribing the control to a [ControlEvent](control-events.md).</span></span> <span data-ttu-id="6f6b6-121">Insira o identificador do atributo na coluna atributo e o identificador do evento na coluna evento da [tabela EventMappings](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="6f6b6-121">Enter the attribute's identifier in the Attribute column and the event's identifier in the Event column of the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="6f6b6-122">Consulte [controlar atributos](control-attributes.md) e [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="6f6b6-122">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



