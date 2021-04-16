---
description: Esse atributo especifica se o controle fornecido está habilitado ou desabilitado. A maioria dos controles aparece cinza quando desabilitada.
ms.assetid: d84b1b55-34e1-4173-b945-39a809014d55
title: Atributo de controle habilitado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb7c5cbbbc12353fc07cf50404a1feae1d98f1b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751204"
---
# <a name="enabled-control-attribute"></a><span data-ttu-id="48534-104">Atributo de controle habilitado</span><span class="sxs-lookup"><span data-stu-id="48534-104">Enabled Control Attribute</span></span>

<span data-ttu-id="48534-105">Esse atributo especifica se o controle fornecido está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="48534-105">This attribute specifies if the given control is enabled or disabled.</span></span> <span data-ttu-id="48534-106">A maioria dos controles aparece cinza quando desabilitada.</span><span class="sxs-lookup"><span data-stu-id="48534-106">Most controls appear gray when disabled.</span></span>

<span data-ttu-id="48534-107">Se esse bit for definido, o controle será criado como habilitado.</span><span class="sxs-lookup"><span data-stu-id="48534-107">If this bit is set, the control is created as enabled.</span></span>

<span data-ttu-id="48534-108">Se esse bit não estiver definido, o controle será criado como desabilitado.</span><span class="sxs-lookup"><span data-stu-id="48534-108">If this bit is not set, the control is created as disabled.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="48534-109">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="48534-109">Valid Controls</span></span>

<span data-ttu-id="48534-110">Todos os controles.</span><span class="sxs-lookup"><span data-stu-id="48534-110">All controls.</span></span> <span data-ttu-id="48534-111">A aparência de alguns controles que não estão associados a uma propriedade, como bitmaps e ícones, não é afetada pela definição deste atributo.</span><span class="sxs-lookup"><span data-stu-id="48534-111">The appearance of some controls that are not associated with a property, such as Bitmaps and Icons, are unaffected by setting this attribute.</span></span>

## <a name="value"></a><span data-ttu-id="48534-112">Valor</span><span class="sxs-lookup"><span data-stu-id="48534-112">Value</span></span>



| <span data-ttu-id="48534-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="48534-113">Decimal</span></span> | <span data-ttu-id="48534-114">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="48534-114">Hexadecimal</span></span> | <span data-ttu-id="48534-115">Constante</span><span class="sxs-lookup"><span data-stu-id="48534-115">Constant</span></span>                          |
|---------|-------------|-----------------------------------|
| <span data-ttu-id="48534-116">2</span><span class="sxs-lookup"><span data-stu-id="48534-116">2</span></span>       | <span data-ttu-id="48534-117">0x00000002</span><span class="sxs-lookup"><span data-stu-id="48534-117">0x00000002</span></span>  | <span data-ttu-id="48534-118">**msidbControlAttributesEnabled**</span><span class="sxs-lookup"><span data-stu-id="48534-118">**msidbControlAttributesEnabled**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="48534-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="48534-119">Remarks</span></span>

<span data-ttu-id="48534-120">Você também pode usar a [tabela ControlCondition](controlcondition-table.md) para desabilitar ou habilitar um controle de acordo com o valor de uma propriedade ou instrução condicional.</span><span class="sxs-lookup"><span data-stu-id="48534-120">You can also use the [ControlCondition table](controlcondition-table.md) to disable or enable a control according to the value of a property or conditional statement.</span></span>

<span data-ttu-id="48534-121">Você também pode habilitar ou desabilitar um controle inscrevendo o controle em um [ControlEvent,](control-events.md).</span><span class="sxs-lookup"><span data-stu-id="48534-121">You can also enable or disable a control by subscribing the control to a [ControlEvent](control-events.md).</span></span> <span data-ttu-id="48534-122">Insira o identificador do atributo na coluna atributo e o identificador do evento na coluna evento da [tabela EventMappings](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="48534-122">Enter the attribute's identifier in the Attribute column and the event's identifier in the Event column of the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="48534-123">Consulte [atributos de controle](control-attributes.md) e o controle que você precisa criar sob [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="48534-123">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



