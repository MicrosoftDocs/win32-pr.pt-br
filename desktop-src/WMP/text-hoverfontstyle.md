---
title: TEXT. hoverFontStyle
description: O atributo hoverFontStyle especifica ou recupera o estilo de fonte usado para o controle de texto quando o cursor do mouse passa sobre ele.
ms.assetid: 77ca8512-6150-4a75-8220-19de3fe9e719
keywords:
- TEXT. hoverFontStyle Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.hoverFontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebaeed6d9701b6e81ac91bc5292dc5b431aa70d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747245"
---
# <a name="texthoverfontstyle"></a><span data-ttu-id="16c55-104">TEXT. hoverFontStyle</span><span class="sxs-lookup"><span data-stu-id="16c55-104">TEXT.hoverFontStyle</span></span>

<span data-ttu-id="16c55-105">O atributo **hoverFontStyle** especifica ou recupera o estilo de fonte usado para o controle de texto quando o cursor do mouse passa sobre ele.</span><span class="sxs-lookup"><span data-stu-id="16c55-105">The **hoverFontStyle** attribute specifies or retrieves the font style used for the Text control when the mouse cursor hovers over it.</span></span>

``` syntax
        elementID.hoverFontStyle
```

## <a name="possible-values"></a><span data-ttu-id="16c55-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="16c55-106">Possible Values</span></span>

<span data-ttu-id="16c55-107">Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="16c55-107">This attribute is a read/write **String** containing one or more of the following values.</span></span>



| <span data-ttu-id="16c55-108">Valor</span><span class="sxs-lookup"><span data-stu-id="16c55-108">Value</span></span>     | <span data-ttu-id="16c55-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="16c55-109">Description</span></span>           |
|-----------|-----------------------|
| <span data-ttu-id="16c55-110">Negrito</span><span class="sxs-lookup"><span data-stu-id="16c55-110">Bold</span></span>      | <span data-ttu-id="16c55-111">Estilo de fonte em negrito.</span><span class="sxs-lookup"><span data-stu-id="16c55-111">Bold font style.</span></span>      |
| <span data-ttu-id="16c55-112">Itálico</span><span class="sxs-lookup"><span data-stu-id="16c55-112">Italic</span></span>    | <span data-ttu-id="16c55-113">Estilo de fonte em itálico.</span><span class="sxs-lookup"><span data-stu-id="16c55-113">Italic font style.</span></span>    |
| <span data-ttu-id="16c55-114">Underline</span><span class="sxs-lookup"><span data-stu-id="16c55-114">Underline</span></span> | <span data-ttu-id="16c55-115">Sublinhar estilo da fonte.</span><span class="sxs-lookup"><span data-stu-id="16c55-115">Underline font style.</span></span> |
| <span data-ttu-id="16c55-116">Riscado</span><span class="sxs-lookup"><span data-stu-id="16c55-116">Strikeout</span></span> | <span data-ttu-id="16c55-117">Estilo da fonte de riscado.</span><span class="sxs-lookup"><span data-stu-id="16c55-117">Strikeout font style.</span></span> |
| <span data-ttu-id="16c55-118">Normal</span><span class="sxs-lookup"><span data-stu-id="16c55-118">Normal</span></span>    | <span data-ttu-id="16c55-119">Estilo de fonte normal.</span><span class="sxs-lookup"><span data-stu-id="16c55-119">Normal font style.</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="16c55-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="16c55-120">Remarks</span></span>

<span data-ttu-id="16c55-121">Qualquer combinação dos valores pode ser usada, separada com espaços.</span><span class="sxs-lookup"><span data-stu-id="16c55-121">Any combination of the values can be used, separated with spaces.</span></span> <span data-ttu-id="16c55-122">O estilo normal tem prioridade sobre todos os outros valores, e quaisquer outros especificados juntamente com normal serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="16c55-122">The Normal style has priority over all other values, and any others specified along with Normal will be ignored.</span></span>

<span data-ttu-id="16c55-123">Se **hoverFontStyle** não for especificado, **FontStyle** será usado.</span><span class="sxs-lookup"><span data-stu-id="16c55-123">If **hoverFontStyle** is not specified, **fontStyle** is used.</span></span>

<span data-ttu-id="16c55-124">Consulte o atributo [Value](text-value.md) para ver um exemplo ilustrando como os atributos do elemento **Text** são usados.</span><span class="sxs-lookup"><span data-stu-id="16c55-124">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="16c55-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16c55-125">Requirements</span></span>



| <span data-ttu-id="16c55-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="16c55-126">Requirement</span></span> | <span data-ttu-id="16c55-127">Valor</span><span class="sxs-lookup"><span data-stu-id="16c55-127">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="16c55-128">Versão</span><span class="sxs-lookup"><span data-stu-id="16c55-128">Version</span></span><br/> | <span data-ttu-id="16c55-129">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="16c55-129">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="16c55-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="16c55-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16c55-131">**Elemento de texto**</span><span class="sxs-lookup"><span data-stu-id="16c55-131">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="16c55-132">**TEXT. fontStyle**</span><span class="sxs-lookup"><span data-stu-id="16c55-132">**TEXT.fontStyle**</span></span>](text-fontstyle.md)
</dt> </dl>

 

 





