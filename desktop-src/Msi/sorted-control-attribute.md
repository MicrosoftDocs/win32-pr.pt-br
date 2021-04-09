---
description: Se esse bit for definido, os itens listados no controle serão exibidos em uma ordem especificada. Se o bit não estiver definido, os itens serão exibidos em ordem alfabética.
ms.assetid: c55bf6bf-6625-47cb-867a-14b3ef8aea0a
title: Atributo de controle classificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84af4b0683e35c66e159602b9ed2fe1b3005d8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010372"
---
# <a name="sorted-control-attribute"></a><span data-ttu-id="8abd0-104">Atributo de controle classificado</span><span class="sxs-lookup"><span data-stu-id="8abd0-104">Sorted Control Attribute</span></span>

<span data-ttu-id="8abd0-105">Se esse bit for definido, os itens listados no controle serão exibidos em uma ordem especificada.</span><span class="sxs-lookup"><span data-stu-id="8abd0-105">If this bit is set, the items listed in the control are displayed in a specified order.</span></span> <span data-ttu-id="8abd0-106">Se o bit não estiver definido, os itens serão exibidos em ordem alfabética.</span><span class="sxs-lookup"><span data-stu-id="8abd0-106">If the bit is not set, items are displayed in alphabetical order.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="8abd0-107">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="8abd0-107">Valid Controls</span></span>

[<span data-ttu-id="8abd0-108">ComboBox</span><span class="sxs-lookup"><span data-stu-id="8abd0-108">ComboBox</span></span>](combobox-control.md)

 

[<span data-ttu-id="8abd0-109">ListBox</span><span class="sxs-lookup"><span data-stu-id="8abd0-109">ListBox</span></span>](listbox-control.md)

 

[<span data-ttu-id="8abd0-110">Controle ListView</span><span class="sxs-lookup"><span data-stu-id="8abd0-110">ListView Control</span></span>](listview-control.md)

## <a name="value"></a><span data-ttu-id="8abd0-111">Valor</span><span class="sxs-lookup"><span data-stu-id="8abd0-111">Value</span></span>



| <span data-ttu-id="8abd0-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="8abd0-112">Decimal</span></span> | <span data-ttu-id="8abd0-113">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="8abd0-113">Hexadecimal</span></span> | <span data-ttu-id="8abd0-114">Constante</span><span class="sxs-lookup"><span data-stu-id="8abd0-114">Constant</span></span>                         |
|---------|-------------|----------------------------------|
| <span data-ttu-id="8abd0-115">65536</span><span class="sxs-lookup"><span data-stu-id="8abd0-115">65536</span></span>   | <span data-ttu-id="8abd0-116">0x00010000</span><span class="sxs-lookup"><span data-stu-id="8abd0-116">0x00010000</span></span>  | <span data-ttu-id="8abd0-117">**msidbControlAttributesSorted**</span><span class="sxs-lookup"><span data-stu-id="8abd0-117">**msidbControlAttributesSorted**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8abd0-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="8abd0-118">Remarks</span></span>

<span data-ttu-id="8abd0-119">Para classificar os itens em uma [ComboBox](combobox-control.md), inclua o bit classificado na coluna atributos da tabela de [controle](control-table.md) e especifique a ordem do item na coluna ordem da [tabela ComboBox](combobox-table.md).</span><span class="sxs-lookup"><span data-stu-id="8abd0-119">To sort the items in a [ComboBox](combobox-control.md), include the Sorted bit in the Attributes column of the [Control table](control-table.md) and specify the item order in the Order column of the [ComboBox table](combobox-table.md).</span></span>

<span data-ttu-id="8abd0-120">Para classificar os itens em uma caixa de [listagem](listbox-control.md), inclua o bit classificado na coluna atributos da [tabela de controle](control-table.md) e especifique a ordem do item na coluna ordem da [tabela ComboBox](combobox-table.md).</span><span class="sxs-lookup"><span data-stu-id="8abd0-120">To sort the items in a [ListBox](listbox-control.md), include the Sorted bit in the Attributes column of the [Control table](control-table.md) and specify the item order in the Order column of the [ComboBox table](combobox-table.md).</span></span>

<span data-ttu-id="8abd0-121">Para classificar os itens em um [ListView](listview-control.md), inclua o bit classificado na coluna atributos da tabela de [controle](control-table.md) e especifique a ordem dos itens na [tabela ComboBox](combobox-table.md).</span><span class="sxs-lookup"><span data-stu-id="8abd0-121">To sort the items in a [ListView](listview-control.md), include the Sorted bit in the Attributes column of the [Control table](control-table.md) and specify the order of items in the [ComboBox table](combobox-table.md).</span></span>

<span data-ttu-id="8abd0-122">Consulte [controlar atributos](control-attributes.md) e [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="8abd0-122">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



