---
title: LISTBOX. fontStyle
description: O atributo fontStyle especifica ou recupera o estilo da fonte para o controle da caixa de listagem.
ms.assetid: c42b80b6-0dea-4080-a06e-931fdc02fa55
keywords:
- LISTBOX. fontStyle Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0903ac77f1fa4307dfcabad6311eb556617d8153
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105790550"
---
# <a name="listboxfontstyle"></a><span data-ttu-id="0848a-104">LISTBOX. fontStyle</span><span class="sxs-lookup"><span data-stu-id="0848a-104">LISTBOX.fontStyle</span></span>

<span data-ttu-id="0848a-105">O atributo **FontStyle** especifica ou recupera o estilo da fonte para o controle da caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="0848a-105">The **fontStyle** attribute specifies or retrieves the font style for the list box control.</span></span>

``` syntax
        elementID.fontStyle
```

## <a name="possible-values"></a><span data-ttu-id="0848a-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="0848a-106">Possible Values</span></span>

<span data-ttu-id="0848a-107">Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="0848a-107">This attribute is a read/write **String** containing one or more of the following values.</span></span>



| <span data-ttu-id="0848a-108">Valor</span><span class="sxs-lookup"><span data-stu-id="0848a-108">Value</span></span>     | <span data-ttu-id="0848a-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="0848a-109">Description</span></span>           |
|-----------|-----------------------|
| <span data-ttu-id="0848a-110">Negrito</span><span class="sxs-lookup"><span data-stu-id="0848a-110">Bold</span></span>      | <span data-ttu-id="0848a-111">Estilo de fonte em negrito.</span><span class="sxs-lookup"><span data-stu-id="0848a-111">Bold font style.</span></span>      |
| <span data-ttu-id="0848a-112">Itálico</span><span class="sxs-lookup"><span data-stu-id="0848a-112">Italic</span></span>    | <span data-ttu-id="0848a-113">Estilo de fonte em itálico.</span><span class="sxs-lookup"><span data-stu-id="0848a-113">Italic font style.</span></span>    |
| <span data-ttu-id="0848a-114">Underline</span><span class="sxs-lookup"><span data-stu-id="0848a-114">Underline</span></span> | <span data-ttu-id="0848a-115">Sublinhar estilo da fonte.</span><span class="sxs-lookup"><span data-stu-id="0848a-115">Underline font style.</span></span> |
| <span data-ttu-id="0848a-116">Riscado</span><span class="sxs-lookup"><span data-stu-id="0848a-116">Strikeout</span></span> | <span data-ttu-id="0848a-117">Estilo da fonte de riscado.</span><span class="sxs-lookup"><span data-stu-id="0848a-117">Strikeout font style.</span></span> |
| <span data-ttu-id="0848a-118">Normal</span><span class="sxs-lookup"><span data-stu-id="0848a-118">Normal</span></span>    | <span data-ttu-id="0848a-119">Estilo de fonte normal.</span><span class="sxs-lookup"><span data-stu-id="0848a-119">Normal font style.</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="0848a-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="0848a-120">Remarks</span></span>

<span data-ttu-id="0848a-121">Qualquer combinação dos valores pode ser usada, separada com espaços.</span><span class="sxs-lookup"><span data-stu-id="0848a-121">Any combination of the values can be used, separated with spaces.</span></span> <span data-ttu-id="0848a-122">O estilo normal tem prioridade sobre todos os outros valores, e quaisquer outros especificados juntamente com normal serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="0848a-122">The Normal style has priority over all other values, and any others specified along with Normal will be ignored.</span></span>

<span data-ttu-id="0848a-123">Para fins de renderização, normal é o estilo de fonte padrão.</span><span class="sxs-lookup"><span data-stu-id="0848a-123">For rendering purposes, Normal is the default font style.</span></span> <span data-ttu-id="0848a-124">O valor padrão recuperado desse atributo é "" (cadeia de caracteres vazia).</span><span class="sxs-lookup"><span data-stu-id="0848a-124">The default value retrieved from this attribute is "" (empty string).</span></span>

## <a name="requirements"></a><span data-ttu-id="0848a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0848a-125">Requirements</span></span>



| <span data-ttu-id="0848a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0848a-126">Requirement</span></span> | <span data-ttu-id="0848a-127">Valor</span><span class="sxs-lookup"><span data-stu-id="0848a-127">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="0848a-128">Versão</span><span class="sxs-lookup"><span data-stu-id="0848a-128">Version</span></span><br/> | <span data-ttu-id="0848a-129">Windows Media Player para Windows XP ou posterior</span><span class="sxs-lookup"><span data-stu-id="0848a-129">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0848a-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="0848a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0848a-131">**Elemento LISTBOX**</span><span class="sxs-lookup"><span data-stu-id="0848a-131">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> <dt>

[<span data-ttu-id="0848a-132">**Caixa de listagem. fontSize**</span><span class="sxs-lookup"><span data-stu-id="0848a-132">**LISTBOX.fontSize**</span></span>](listbox-fontsize.md)
</dt> </dl>

 

 





