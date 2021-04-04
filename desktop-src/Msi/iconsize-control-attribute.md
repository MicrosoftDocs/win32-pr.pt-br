---
description: Um arquivo de ícone pode conter vários tamanhos diferentes da mesma imagem de ícone.
ms.assetid: 2d4d3689-a45a-4088-b466-e2b3bf4c8fb5
title: Atributo de controle de ícones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cb615a53c589ebc2ad2cafb8a2ff7dec902865e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010905"
---
# <a name="iconsize-control-attribute"></a><span data-ttu-id="8c7ea-103">Atributo de controle de ícones</span><span class="sxs-lookup"><span data-stu-id="8c7ea-103">IconSize Control Attribute</span></span>

<span data-ttu-id="8c7ea-104">Um arquivo de ícone pode conter vários tamanhos diferentes da mesma imagem de ícone.</span><span class="sxs-lookup"><span data-stu-id="8c7ea-104">An icon file can hold several different sizes of the same icon image.</span></span> <span data-ttu-id="8c7ea-105">Esses bits especificam o tamanho da imagem de ícone a ser carregada.</span><span class="sxs-lookup"><span data-stu-id="8c7ea-105">These bits specify which size of the icon image to load.</span></span> <span data-ttu-id="8c7ea-106">Se nenhum dos bits estiver definido, a primeira imagem será carregada.</span><span class="sxs-lookup"><span data-stu-id="8c7ea-106">If none of the bits are set, the first image is loaded.</span></span> <span data-ttu-id="8c7ea-107">Se apenas **msidbControlAttributesIconSize16** for definido, a primeira imagem de 16x16 será carregada.</span><span class="sxs-lookup"><span data-stu-id="8c7ea-107">If only **msidbControlAttributesIconSize16** is set, the first 16x16 image is loaded.</span></span> <span data-ttu-id="8c7ea-108">Se apenas o **msidbControlAttributesIconSize32** for definido, a primeira imagem 32x32 será carregada.</span><span class="sxs-lookup"><span data-stu-id="8c7ea-108">If only the **msidbControlAttributesIconSize32** is set, the first 32x32 image is loaded.</span></span> <span data-ttu-id="8c7ea-109">Se **msidbControlAttributesIconSize48** for definido, a primeira imagem 48x48 será carregada.</span><span class="sxs-lookup"><span data-stu-id="8c7ea-109">If **msidbControlAttributesIconSize48** is set, the first 48x48 image is loaded.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="8c7ea-110">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="8c7ea-110">Valid Controls</span></span>

[<span data-ttu-id="8c7ea-111">CheckBox</span><span class="sxs-lookup"><span data-stu-id="8c7ea-111">CheckBox</span></span>](checkbox-control.md)

[<span data-ttu-id="8c7ea-112">Ícone</span><span class="sxs-lookup"><span data-stu-id="8c7ea-112">Icon</span></span>](icon-control.md)

[<span data-ttu-id="8c7ea-113">Botão</span><span class="sxs-lookup"><span data-stu-id="8c7ea-113">PushButton</span></span>](pushbutton-control.md)

[<span data-ttu-id="8c7ea-114">Botão de opção</span><span class="sxs-lookup"><span data-stu-id="8c7ea-114">RadioButtonGroup</span></span>](radiobuttongroup-control.md)

## <a name="value"></a><span data-ttu-id="8c7ea-115">Valor</span><span class="sxs-lookup"><span data-stu-id="8c7ea-115">Value</span></span>



| <span data-ttu-id="8c7ea-116">Decimal</span><span class="sxs-lookup"><span data-stu-id="8c7ea-116">Decimal</span></span> | <span data-ttu-id="8c7ea-117">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="8c7ea-117">Hexadecimal</span></span> | <span data-ttu-id="8c7ea-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="8c7ea-118">Description</span></span>                          |
|---------|-------------|--------------------------------------|
| <span data-ttu-id="8c7ea-119">2097152</span><span class="sxs-lookup"><span data-stu-id="8c7ea-119">2097152</span></span> | <span data-ttu-id="8c7ea-120">0x00200000</span><span class="sxs-lookup"><span data-stu-id="8c7ea-120">0x00200000</span></span>  | <span data-ttu-id="8c7ea-121">**msidbControlAttributesIconSize16**</span><span class="sxs-lookup"><span data-stu-id="8c7ea-121">**msidbControlAttributesIconSize16**</span></span> |
| <span data-ttu-id="8c7ea-122">4194304</span><span class="sxs-lookup"><span data-stu-id="8c7ea-122">4194304</span></span> | <span data-ttu-id="8c7ea-123">0x00400000</span><span class="sxs-lookup"><span data-stu-id="8c7ea-123">0x00400000</span></span>  | <span data-ttu-id="8c7ea-124">**msidbControlAttributesIconSize32**</span><span class="sxs-lookup"><span data-stu-id="8c7ea-124">**msidbControlAttributesIconSize32**</span></span> |
| <span data-ttu-id="8c7ea-125">6291456</span><span class="sxs-lookup"><span data-stu-id="8c7ea-125">6291456</span></span> | <span data-ttu-id="8c7ea-126">0x00600000</span><span class="sxs-lookup"><span data-stu-id="8c7ea-126">0x00600000</span></span>  | <span data-ttu-id="8c7ea-127">**msidbControlAttributesIconSize48**</span><span class="sxs-lookup"><span data-stu-id="8c7ea-127">**msidbControlAttributesIconSize48**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8c7ea-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c7ea-128">Remarks</span></span>

<span data-ttu-id="8c7ea-129">Para definir esse atributo em um controle, inclua os bits de ícones na coluna atributos do registro do controle na [tabela de controle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="8c7ea-129">To set this attribute on a control, include the IconSize bits in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="8c7ea-130">Se o bit [FixedSize](fixedsize-control-attribute.md) não for definido, a imagem carregada será reduzida ou ampliada para se ajustar ao controle de ícone.</span><span class="sxs-lookup"><span data-stu-id="8c7ea-130">If the [FixedSize](fixedsize-control-attribute.md) bit is not set, the loaded image is shrunk or stretched to fit the icon control.</span></span> <span data-ttu-id="8c7ea-131">Se o bit [FixedSize](fixedsize-control-attribute.md) for definido e a imagem carregada for menor do que o controle de ícone, a imagem será exibida centralizada dentro do controle.</span><span class="sxs-lookup"><span data-stu-id="8c7ea-131">If the [FixedSize](fixedsize-control-attribute.md) bit is set, and the loaded image is smaller than the icon control, the picture is displayed centered inside the control.</span></span> <span data-ttu-id="8c7ea-132">Se o bit [FixedSize](fixedsize-control-attribute.md) for definido e a imagem carregada for maior que o controle de ícone, a imagem será reduzida para se ajustar ao controle.</span><span class="sxs-lookup"><span data-stu-id="8c7ea-132">If the [FixedSize](fixedsize-control-attribute.md) bit is set, and the loaded image is larger than the icon control, the picture is reduced to fit the control.</span></span>

<span data-ttu-id="8c7ea-133">Consulte [atributos de controle](control-attributes.md) e o controle que você precisa criar sob [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="8c7ea-133">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



