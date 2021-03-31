---
description: Se o bit de controle de bitmap for definido, o texto no controle será substituído por uma imagem de bitmap. A coluna de texto na tabela de controle é uma chave estrangeira na tabela binária.
ms.assetid: ec774f31-7712-4a70-8c69-1cc731009049
title: Atributo de controle de bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bda78231c1689c4c5faebeab98fbf6566c7e667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828048"
---
# <a name="bitmap-control-attribute"></a><span data-ttu-id="8fd17-104">Atributo de controle de bitmap</span><span class="sxs-lookup"><span data-stu-id="8fd17-104">Bitmap Control Attribute</span></span>

<span data-ttu-id="8fd17-105">Se o bit de controle de bitmap for definido, o texto no controle será substituído por uma imagem de bitmap.</span><span class="sxs-lookup"><span data-stu-id="8fd17-105">If the Bitmap Control bit is set, the text in the control is replaced by a bitmap image.</span></span> <span data-ttu-id="8fd17-106">A coluna de texto na [tabela de controle](control-table.md) é uma chave estrangeira na [tabela binária](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="8fd17-106">The Text column in the [Control table](control-table.md) is a foreign key into the [Binary table](binary-table.md).</span></span>

<span data-ttu-id="8fd17-107">Se esse bit não for definido, o texto no controle será especificado na coluna de texto da tabela de [controle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="8fd17-107">If this bit is not set, the text in the control is specified in the Text column of the [Control table](control-table.md).</span></span>

## <a name="valid-controls"></a><span data-ttu-id="8fd17-108">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="8fd17-108">Valid Controls</span></span>

[<span data-ttu-id="8fd17-109">CheckBox</span><span class="sxs-lookup"><span data-stu-id="8fd17-109">CheckBox</span></span>](checkbox-control.md)

 

[<span data-ttu-id="8fd17-110">Botão</span><span class="sxs-lookup"><span data-stu-id="8fd17-110">PushButton</span></span>](pushbutton-control.md)

 

[<span data-ttu-id="8fd17-111">Botão de opção</span><span class="sxs-lookup"><span data-stu-id="8fd17-111">RadioButtonGroup</span></span>](radiobuttongroup-control.md)

## <a name="value"></a><span data-ttu-id="8fd17-112">Valor</span><span class="sxs-lookup"><span data-stu-id="8fd17-112">Value</span></span>



| <span data-ttu-id="8fd17-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="8fd17-113">Decimal</span></span> | <span data-ttu-id="8fd17-114">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="8fd17-114">Hexadecimal</span></span> | <span data-ttu-id="8fd17-115">Constante</span><span class="sxs-lookup"><span data-stu-id="8fd17-115">Constant</span></span>                         |
|---------|-------------|----------------------------------|
| <span data-ttu-id="8fd17-116">262144</span><span class="sxs-lookup"><span data-stu-id="8fd17-116">262144</span></span>  | <span data-ttu-id="8fd17-117">0x00040000</span><span class="sxs-lookup"><span data-stu-id="8fd17-117">0x00040000</span></span>  | <span data-ttu-id="8fd17-118">**msidbControlAttributesBitmap**</span><span class="sxs-lookup"><span data-stu-id="8fd17-118">**msidbControlAttributesBitmap**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8fd17-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="8fd17-119">Remarks</span></span>

<span data-ttu-id="8fd17-120">Para definir esse atributo em um controle, inclua o bit bitmap na coluna atributos do registro do controle na [tabela de controle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="8fd17-120">To set this attribute on a control, include the Bitmap bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="8fd17-121">A coluna de texto na tabela de controle é usada como uma chave estrangeira para a [tabela binária](binary-table.md), portanto, o controle não pode conter uma imagem de ícone e um texto.</span><span class="sxs-lookup"><span data-stu-id="8fd17-121">The Text column in the Control table is used as a foreign key to the [Binary table](binary-table.md), therefore the control cannot contain both an icon image and text.</span></span>

<span data-ttu-id="8fd17-122">Não defina os bits de [ícone](icon-control-attribute.md) e bitmap.</span><span class="sxs-lookup"><span data-stu-id="8fd17-122">Do not set both the [Icon](icon-control-attribute.md) and Bitmap bits.</span></span>

<span data-ttu-id="8fd17-123">Consulte [atributos de controle](control-attributes.md) e o controle que você precisa criar sob [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="8fd17-123">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



