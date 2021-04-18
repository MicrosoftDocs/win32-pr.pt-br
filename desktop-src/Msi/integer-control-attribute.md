---
description: Se esse bit for definido em um controle, a propriedade associada especificada na coluna propriedade da tabela de controle será um número inteiro. Se esse bit não for definido, a propriedade será um valor de cadeia de caracteres.
ms.assetid: 58db9451-d152-439b-b7cf-39ddea84bcc9
title: Atributo de controle de inteiro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6310f6348a533874ce4dc176043a489b595c28b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812917"
---
# <a name="integer-control-attribute"></a><span data-ttu-id="2e0df-104">Atributo de controle de inteiro</span><span class="sxs-lookup"><span data-stu-id="2e0df-104">Integer Control Attribute</span></span>

<span data-ttu-id="2e0df-105">Se esse bit for definido em um controle, a propriedade associada especificada na coluna propriedade da tabela de [controle](control-table.md) será um número inteiro.</span><span class="sxs-lookup"><span data-stu-id="2e0df-105">If this bit is set on a control, the associated property specified in the Property column of the [Control table](control-table.md) is an integer.</span></span> <span data-ttu-id="2e0df-106">Se esse bit não for definido, a propriedade será um valor de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="2e0df-106">If this bit is not set, the property is a string value.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="2e0df-107">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="2e0df-107">Valid Controls</span></span>

[<span data-ttu-id="2e0df-108">CheckBox</span><span class="sxs-lookup"><span data-stu-id="2e0df-108">CheckBox</span></span>](checkbox-control.md)

[<span data-ttu-id="2e0df-109">ComboBox</span><span class="sxs-lookup"><span data-stu-id="2e0df-109">ComboBox</span></span>](combobox-control.md)

[<span data-ttu-id="2e0df-110">Editar</span><span class="sxs-lookup"><span data-stu-id="2e0df-110">Edit</span></span>](edit-control.md)

[<span data-ttu-id="2e0df-111">ListBox</span><span class="sxs-lookup"><span data-stu-id="2e0df-111">ListBox</span></span>](listbox-control.md)

[<span data-ttu-id="2e0df-112">Botão de opção</span><span class="sxs-lookup"><span data-stu-id="2e0df-112">RadioButtonGroup</span></span>](radiobuttongroup-control.md)

## <a name="value"></a><span data-ttu-id="2e0df-113">Valor</span><span class="sxs-lookup"><span data-stu-id="2e0df-113">Value</span></span>



| <span data-ttu-id="2e0df-114">Decimal</span><span class="sxs-lookup"><span data-stu-id="2e0df-114">Decimal</span></span> | <span data-ttu-id="2e0df-115">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="2e0df-115">Hexadecimal</span></span> | <span data-ttu-id="2e0df-116">Constante</span><span class="sxs-lookup"><span data-stu-id="2e0df-116">Constant</span></span>                          |
|---------|-------------|-----------------------------------|
| <span data-ttu-id="2e0df-117">16</span><span class="sxs-lookup"><span data-stu-id="2e0df-117">16</span></span>      | <span data-ttu-id="2e0df-118">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2e0df-118">0x00000010</span></span>  | <span data-ttu-id="2e0df-119">**msidbControlAttributesInteger**</span><span class="sxs-lookup"><span data-stu-id="2e0df-119">**msidbControlAttributesInteger**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="2e0df-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="2e0df-120">Remarks</span></span>

<span data-ttu-id="2e0df-121">Para definir esse atributo em um controle, inclua o bit inteiro na coluna atributos do registro do controle na [tabela de controle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="2e0df-121">To set this attribute on a control, include the Integer bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="2e0df-122">Consulte [controlar atributos](control-attributes.md) e [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="2e0df-122">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



