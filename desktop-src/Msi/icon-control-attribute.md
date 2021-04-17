---
description: Se esse bit for definido, o texto será substituído por uma imagem de ícone e a coluna de texto na tabela de controle será uma chave estrangeira na tabela binária.
ms.assetid: 5eefdfcb-89a5-4885-bab0-6409ef3ce349
title: Atributo de controle de ícone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60c19674ac26f108109fad04e0836ed8dfeba6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751198"
---
# <a name="icon-control-attribute"></a><span data-ttu-id="f6d13-103">Atributo de controle de ícone</span><span class="sxs-lookup"><span data-stu-id="f6d13-103">Icon Control Attribute</span></span>

<span data-ttu-id="f6d13-104">Se esse bit for definido, o texto será substituído por uma imagem de ícone e a coluna de texto na [tabela de controle](control-table.md) será uma chave estrangeira na [tabela binária](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="f6d13-104">If this bit is set, text is replaced by an icon image and the Text column in the [Control table](control-table.md) is a foreign key into the [Binary table](binary-table.md).</span></span>

<span data-ttu-id="f6d13-105">Se esse bit não estiver definido, o texto no controle será especificado na coluna de texto da [tabela de controle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="f6d13-105">If this bit is not set, text in the control is specified in the Text column of the [Control table](control-table.md).</span></span>

## <a name="valid-controls"></a><span data-ttu-id="f6d13-106">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="f6d13-106">Valid Controls</span></span>

[<span data-ttu-id="f6d13-107">CheckBox</span><span class="sxs-lookup"><span data-stu-id="f6d13-107">CheckBox</span></span>](checkbox-control.md)

[<span data-ttu-id="f6d13-108">Botão</span><span class="sxs-lookup"><span data-stu-id="f6d13-108">PushButton</span></span>](pushbutton-control.md)

[<span data-ttu-id="f6d13-109">Botão de opção</span><span class="sxs-lookup"><span data-stu-id="f6d13-109">RadioButtonGroup</span></span>](radiobuttongroup-control.md)

## <a name="value"></a><span data-ttu-id="f6d13-110">Valor</span><span class="sxs-lookup"><span data-stu-id="f6d13-110">Value</span></span>



| <span data-ttu-id="f6d13-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="f6d13-111">Decimal</span></span> | <span data-ttu-id="f6d13-112">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="f6d13-112">Hexadecimal</span></span> | <span data-ttu-id="f6d13-113">Constante</span><span class="sxs-lookup"><span data-stu-id="f6d13-113">Constant</span></span>                       |
|---------|-------------|--------------------------------|
| <span data-ttu-id="f6d13-114">5242288</span><span class="sxs-lookup"><span data-stu-id="f6d13-114">5242288</span></span> | <span data-ttu-id="f6d13-115">0x00080000</span><span class="sxs-lookup"><span data-stu-id="f6d13-115">0x00080000</span></span>  | <span data-ttu-id="f6d13-116">**msidbControlAttributesIcon**</span><span class="sxs-lookup"><span data-stu-id="f6d13-116">**msidbControlAttributesIcon**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f6d13-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6d13-117">Remarks</span></span>

<span data-ttu-id="f6d13-118">Para definir esse atributo em um controle, inclua os bits do ícone na coluna atributos do registro do controle na tabela de [controle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="f6d13-118">To set this attribute on a control, include the Icon bits in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="f6d13-119">A coluna de texto na tabela de controle é usada como uma chave estrangeira para a [tabela binária](binary-table.md), portanto, o controle não pode conter uma imagem de ícone e um texto.</span><span class="sxs-lookup"><span data-stu-id="f6d13-119">The Text column in the Control table is used as a foreign key to the [Binary table](binary-table.md), therefore the control cannot contain both an icon image and text.</span></span>

<span data-ttu-id="f6d13-120">Não defina os bits de ícone e [bitmap](bitmap-control-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="f6d13-120">Do not set both the Icon and [Bitmap](bitmap-control-attribute.md) bits.</span></span>

<span data-ttu-id="f6d13-121">Consulte [atributos de controle](control-attributes.md) e o controle que você precisa criar sob [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="f6d13-121">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



