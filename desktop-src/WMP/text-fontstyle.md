---
title: TEXT. fontStyle
description: O atributo fontStyle especifica ou recupera o estilo da fonte para o controle de texto.
ms.assetid: 1bb99305-dccc-489d-9a02-7cb306f0d47d
keywords:
- TEXT. fontStyle Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab6ddfb3ff31cba50027c010ed10c2129d45134
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751933"
---
# <a name="textfontstyle"></a><span data-ttu-id="3099b-104">TEXT. fontStyle</span><span class="sxs-lookup"><span data-stu-id="3099b-104">TEXT.fontStyle</span></span>

<span data-ttu-id="3099b-105">O atributo **FontStyle** especifica ou recupera o estilo da fonte para o controle de texto.</span><span class="sxs-lookup"><span data-stu-id="3099b-105">The **fontStyle** attribute specifies or retrieves the font style for the Text control.</span></span>

``` syntax
        elementID.fontStyle
```

## <a name="possible-values"></a><span data-ttu-id="3099b-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="3099b-106">Possible Values</span></span>

<span data-ttu-id="3099b-107">Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="3099b-107">This attribute is a read/write **String** containing one or more of the following values.</span></span>



| <span data-ttu-id="3099b-108">Valor</span><span class="sxs-lookup"><span data-stu-id="3099b-108">Value</span></span>     | <span data-ttu-id="3099b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="3099b-109">Description</span></span>                 |
|-----------|-----------------------------|
| <span data-ttu-id="3099b-110">Negrito</span><span class="sxs-lookup"><span data-stu-id="3099b-110">Bold</span></span>      | <span data-ttu-id="3099b-111">Estilo de fonte em negrito.</span><span class="sxs-lookup"><span data-stu-id="3099b-111">Bold font style.</span></span>            |
| <span data-ttu-id="3099b-112">Itálico</span><span class="sxs-lookup"><span data-stu-id="3099b-112">Italic</span></span>    | <span data-ttu-id="3099b-113">Estilo de fonte em itálico.</span><span class="sxs-lookup"><span data-stu-id="3099b-113">Italic font style.</span></span>          |
| <span data-ttu-id="3099b-114">Underline</span><span class="sxs-lookup"><span data-stu-id="3099b-114">Underline</span></span> | <span data-ttu-id="3099b-115">Sublinhar estilo da fonte.</span><span class="sxs-lookup"><span data-stu-id="3099b-115">Underline font style.</span></span>       |
| <span data-ttu-id="3099b-116">Riscado</span><span class="sxs-lookup"><span data-stu-id="3099b-116">Strikeout</span></span> | <span data-ttu-id="3099b-117">Estilo da fonte de riscado.</span><span class="sxs-lookup"><span data-stu-id="3099b-117">Strikeout font style.</span></span>       |
| <span data-ttu-id="3099b-118">Normal</span><span class="sxs-lookup"><span data-stu-id="3099b-118">Normal</span></span>    | <span data-ttu-id="3099b-119">Padrão.</span><span class="sxs-lookup"><span data-stu-id="3099b-119">Default.</span></span> <span data-ttu-id="3099b-120">Estilo de fonte normal.</span><span class="sxs-lookup"><span data-stu-id="3099b-120">Normal font style.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3099b-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="3099b-121">Remarks</span></span>

<span data-ttu-id="3099b-122">Qualquer combinação dos valores pode ser usada, separada com espaços.</span><span class="sxs-lookup"><span data-stu-id="3099b-122">Any combination of the values can be used, separated with spaces.</span></span> <span data-ttu-id="3099b-123">O estilo normal tem prioridade sobre todos os outros valores, e quaisquer outros especificados juntamente com normal serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="3099b-123">The Normal style has priority over all other values, and any others specified along with Normal will be ignored.</span></span>

<span data-ttu-id="3099b-124">Consulte o atributo [Value](text-value.md) para ver um exemplo ilustrando como os atributos do elemento **Text** são usados.</span><span class="sxs-lookup"><span data-stu-id="3099b-124">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="3099b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3099b-125">Requirements</span></span>



| <span data-ttu-id="3099b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3099b-126">Requirement</span></span> | <span data-ttu-id="3099b-127">Valor</span><span class="sxs-lookup"><span data-stu-id="3099b-127">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="3099b-128">Versão</span><span class="sxs-lookup"><span data-stu-id="3099b-128">Version</span></span><br/> | <span data-ttu-id="3099b-129">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="3099b-129">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3099b-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="3099b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3099b-131">**Elemento de texto**</span><span class="sxs-lookup"><span data-stu-id="3099b-131">**TEXT Element**</span></span>](text-element.md)
</dt> </dl>

 

 





