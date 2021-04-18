---
title: TEXT. disabledFontStyle
description: O atributo disabledFontStyle especifica ou recupera o estilo de fonte usado para o controle de texto quando ele está desabilitado.
ms.assetid: d0593fe0-f80d-44a3-b989-e85887465d8a
keywords:
- TEXT. disabledFontStyle Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.disabledFontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 563ab039a5eae00324f3a810c7d32f08729629b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105791285"
---
# <a name="textdisabledfontstyle"></a><span data-ttu-id="10ce3-104">TEXT. disabledFontStyle</span><span class="sxs-lookup"><span data-stu-id="10ce3-104">TEXT.disabledFontStyle</span></span>

<span data-ttu-id="10ce3-105">O atributo **disabledFontStyle** especifica ou recupera o estilo de fonte usado para o controle de texto quando ele está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="10ce3-105">The **disabledFontStyle** attribute specifies or retrieves the font style used for the Text control when it is disabled.</span></span>

``` syntax
        elementID.disabledFontStyle
```

## <a name="possible-values"></a><span data-ttu-id="10ce3-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="10ce3-106">Possible Values</span></span>

<span data-ttu-id="10ce3-107">Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="10ce3-107">This attribute is a read/write **String** containing one or more of the following values.</span></span>



| <span data-ttu-id="10ce3-108">Valor</span><span class="sxs-lookup"><span data-stu-id="10ce3-108">Value</span></span>     | <span data-ttu-id="10ce3-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="10ce3-109">Description</span></span>           |
|-----------|-----------------------|
| <span data-ttu-id="10ce3-110">Negrito</span><span class="sxs-lookup"><span data-stu-id="10ce3-110">Bold</span></span>      | <span data-ttu-id="10ce3-111">Estilo de fonte em negrito.</span><span class="sxs-lookup"><span data-stu-id="10ce3-111">Bold font style.</span></span>      |
| <span data-ttu-id="10ce3-112">Itálico</span><span class="sxs-lookup"><span data-stu-id="10ce3-112">Italic</span></span>    | <span data-ttu-id="10ce3-113">Estilo de fonte em itálico.</span><span class="sxs-lookup"><span data-stu-id="10ce3-113">Italic font style.</span></span>    |
| <span data-ttu-id="10ce3-114">Underline</span><span class="sxs-lookup"><span data-stu-id="10ce3-114">Underline</span></span> | <span data-ttu-id="10ce3-115">Sublinhar estilo da fonte.</span><span class="sxs-lookup"><span data-stu-id="10ce3-115">Underline font style.</span></span> |
| <span data-ttu-id="10ce3-116">Riscado</span><span class="sxs-lookup"><span data-stu-id="10ce3-116">Strikeout</span></span> | <span data-ttu-id="10ce3-117">Estilo da fonte de riscado.</span><span class="sxs-lookup"><span data-stu-id="10ce3-117">Strikeout font style.</span></span> |
| <span data-ttu-id="10ce3-118">Normal</span><span class="sxs-lookup"><span data-stu-id="10ce3-118">Normal</span></span>    | <span data-ttu-id="10ce3-119">Estilo de fonte normal.</span><span class="sxs-lookup"><span data-stu-id="10ce3-119">Normal font style.</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="10ce3-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="10ce3-120">Remarks</span></span>

<span data-ttu-id="10ce3-121">Qualquer combinação dos valores pode ser usada, separada com espaços.</span><span class="sxs-lookup"><span data-stu-id="10ce3-121">Any combination of the values can be used, separated with spaces.</span></span> <span data-ttu-id="10ce3-122">O estilo normal tem prioridade sobre todos os outros valores, e quaisquer outros especificados juntamente com normal serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="10ce3-122">The Normal style has priority over all other values, and any others specified along with Normal will be ignored.</span></span>

<span data-ttu-id="10ce3-123">Se **disabledFontStyle** não for especificado, **FontStyle** será usado.</span><span class="sxs-lookup"><span data-stu-id="10ce3-123">If **disabledFontStyle** is not specified, **fontStyle** is used.</span></span>

<span data-ttu-id="10ce3-124">Consulte o atributo [Value](text-value.md) para ver um exemplo ilustrando como os atributos do elemento **Text** são usados.</span><span class="sxs-lookup"><span data-stu-id="10ce3-124">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="10ce3-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10ce3-125">Requirements</span></span>



| <span data-ttu-id="10ce3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="10ce3-126">Requirement</span></span> | <span data-ttu-id="10ce3-127">Valor</span><span class="sxs-lookup"><span data-stu-id="10ce3-127">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="10ce3-128">Versão</span><span class="sxs-lookup"><span data-stu-id="10ce3-128">Version</span></span><br/> | <span data-ttu-id="10ce3-129">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="10ce3-129">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="10ce3-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="10ce3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10ce3-131">**Elemento de texto**</span><span class="sxs-lookup"><span data-stu-id="10ce3-131">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="10ce3-132">**TEXT. fontStyle**</span><span class="sxs-lookup"><span data-stu-id="10ce3-132">**TEXT.fontStyle**</span></span>](text-fontstyle.md)
</dt> </dl>

 

 





