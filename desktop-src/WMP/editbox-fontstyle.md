---
title: FontStyle de edição
description: O atributo fontStyle especifica ou recupera o estilo da fonte para o controle caixa de edição.
ms.assetid: bc71359d-2b75-4134-99e8-52b2ca48dcde
keywords:
- Admy. fontStyle Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4249f6224099c3d2a36a3b26244c9b804be519c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794484"
---
# <a name="editboxfontstyle"></a><span data-ttu-id="4d314-104">FontStyle de edição</span><span class="sxs-lookup"><span data-stu-id="4d314-104">EDITBOX.fontStyle</span></span>

<span data-ttu-id="4d314-105">O atributo **FontStyle** especifica ou recupera o estilo da fonte para o controle caixa de edição.</span><span class="sxs-lookup"><span data-stu-id="4d314-105">The **fontStyle** attribute specifies or retrieves the font style for the edit box control.</span></span>

``` syntax
        elementID.fontStyle
```

## <a name="possible-values"></a><span data-ttu-id="4d314-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="4d314-106">Possible Values</span></span>

<span data-ttu-id="4d314-107">Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="4d314-107">This attribute is a read/write **String** containing one or more of the following values.</span></span>



| <span data-ttu-id="4d314-108">Valor</span><span class="sxs-lookup"><span data-stu-id="4d314-108">Value</span></span>     | <span data-ttu-id="4d314-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4d314-109">Description</span></span>           |
|-----------|-----------------------|
| <span data-ttu-id="4d314-110">Negrito</span><span class="sxs-lookup"><span data-stu-id="4d314-110">Bold</span></span>      | <span data-ttu-id="4d314-111">Estilo de fonte em negrito.</span><span class="sxs-lookup"><span data-stu-id="4d314-111">Bold font style.</span></span>      |
| <span data-ttu-id="4d314-112">Itálico</span><span class="sxs-lookup"><span data-stu-id="4d314-112">Italic</span></span>    | <span data-ttu-id="4d314-113">Estilo de fonte em itálico.</span><span class="sxs-lookup"><span data-stu-id="4d314-113">Italic font style.</span></span>    |
| <span data-ttu-id="4d314-114">Underline</span><span class="sxs-lookup"><span data-stu-id="4d314-114">Underline</span></span> | <span data-ttu-id="4d314-115">Sublinhar estilo da fonte.</span><span class="sxs-lookup"><span data-stu-id="4d314-115">Underline font style.</span></span> |
| <span data-ttu-id="4d314-116">Riscado</span><span class="sxs-lookup"><span data-stu-id="4d314-116">Strikeout</span></span> | <span data-ttu-id="4d314-117">Estilo da fonte de riscado.</span><span class="sxs-lookup"><span data-stu-id="4d314-117">Strikeout font style.</span></span> |
| <span data-ttu-id="4d314-118">Normal</span><span class="sxs-lookup"><span data-stu-id="4d314-118">Normal</span></span>    | <span data-ttu-id="4d314-119">Estilo de fonte normal.</span><span class="sxs-lookup"><span data-stu-id="4d314-119">Normal font style.</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="4d314-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="4d314-120">Remarks</span></span>

<span data-ttu-id="4d314-121">Qualquer combinação dos valores pode ser usada, separada com espaços.</span><span class="sxs-lookup"><span data-stu-id="4d314-121">Any combination of the values can be used, separated with spaces.</span></span> <span data-ttu-id="4d314-122">O estilo normal tem prioridade sobre todos os outros valores, e quaisquer outros especificados juntamente com normal serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="4d314-122">The Normal style has priority over all other values, and any others specified along with Normal will be ignored.</span></span>

<span data-ttu-id="4d314-123">Para fins de renderização, normal é o estilo de fonte padrão.</span><span class="sxs-lookup"><span data-stu-id="4d314-123">For rendering purposes, Normal is the default font style.</span></span> <span data-ttu-id="4d314-124">O valor padrão recuperado desse atributo é "" (cadeia de caracteres vazia).</span><span class="sxs-lookup"><span data-stu-id="4d314-124">The default value retrieved from this attribute is "" (empty string).</span></span>

## <a name="requirements"></a><span data-ttu-id="4d314-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d314-125">Requirements</span></span>



| <span data-ttu-id="4d314-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d314-126">Requirement</span></span> | <span data-ttu-id="4d314-127">Valor</span><span class="sxs-lookup"><span data-stu-id="4d314-127">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="4d314-128">Versão</span><span class="sxs-lookup"><span data-stu-id="4d314-128">Version</span></span><br/> | <span data-ttu-id="4d314-129">Windows Media Player para Windows XP ou posterior</span><span class="sxs-lookup"><span data-stu-id="4d314-129">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4d314-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="4d314-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d314-131">**Elemento admy**</span><span class="sxs-lookup"><span data-stu-id="4d314-131">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="4d314-132">**FontFace de edição**</span><span class="sxs-lookup"><span data-stu-id="4d314-132">**EDITBOX.fontFace**</span></span>](editbox-fontface.md)
</dt> <dt>

[<span data-ttu-id="4d314-133">**Mythe. fontSize**</span><span class="sxs-lookup"><span data-stu-id="4d314-133">**EDITBOX.fontSize**</span></span>](editbox-fontsize.md)
</dt> </dl>

 

 





