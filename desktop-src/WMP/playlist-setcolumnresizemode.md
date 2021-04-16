---
title: PLAYLIST. setColumnResizeMode
description: O método setColumnResizeMode especifica como os tamanhos de coluna indexados em si.
ms.assetid: 84ca0e60-ca24-4058-ae08-5b9cf3d7c38f
keywords:
- PLAYLIST. setColumnResizeMode Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setColumnResizeMode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a1b83020f4400f4f1095c84e281fe498f2b67da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105773046"
---
# <a name="playlistsetcolumnresizemode"></a><span data-ttu-id="6ba5c-104">PLAYLIST. setColumnResizeMode</span><span class="sxs-lookup"><span data-stu-id="6ba5c-104">PLAYLIST.setColumnResizeMode</span></span>

<span data-ttu-id="6ba5c-105">O método **setColumnResizeMode** especifica como os tamanhos de coluna indexados em si.</span><span class="sxs-lookup"><span data-stu-id="6ba5c-105">The **setColumnResizeMode** method specifies how the indexed column sizes itself.</span></span>

``` syntax
        elementID.setColumnResizeMode(column, mode)
```

## <a name="parameters"></a><span data-ttu-id="6ba5c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ba5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ba5c-107"><span id="column"></span><span id="COLUMN"></span>*pilha*</span><span class="sxs-lookup"><span data-stu-id="6ba5c-107"><span id="column"></span><span id="COLUMN"></span>*column*</span></span>
</dt> <dd>

<span data-ttu-id="6ba5c-108">**Número** (**longo**) indicando o índice da coluna a ser alterada.</span><span class="sxs-lookup"><span data-stu-id="6ba5c-108">**Number** (**long**) indicating the index of the column to be changed.</span></span>

</dd> <dt>

<span data-ttu-id="6ba5c-109"><span id="mode"></span><span id="MODE"></span>*moda*</span><span class="sxs-lookup"><span data-stu-id="6ba5c-109"><span id="mode"></span><span id="MODE"></span>*mode*</span></span>
</dt> <dd>

<span data-ttu-id="6ba5c-110">**Cadeia de caracteres** que indica o modo de dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="6ba5c-110">**String** indicating the sizing mode.</span></span> <span data-ttu-id="6ba5c-111">Contém um dos seguintes valores.</span><span class="sxs-lookup"><span data-stu-id="6ba5c-111">Contains one of the following values.</span></span>



| <span data-ttu-id="6ba5c-112">Valor</span><span class="sxs-lookup"><span data-stu-id="6ba5c-112">Value</span></span>          | <span data-ttu-id="6ba5c-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="6ba5c-113">Description</span></span>                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ba5c-114">AutosizeHeader</span><span class="sxs-lookup"><span data-stu-id="6ba5c-114">AutosizeHeader</span></span> | <span data-ttu-id="6ba5c-115">A coluna é redimensionada para acomodar todos os dados na coluna e no cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="6ba5c-115">The column resizes to accommodate all data in both the column and the header.</span></span>                                  |
| <span data-ttu-id="6ba5c-116">AutosizeData</span><span class="sxs-lookup"><span data-stu-id="6ba5c-116">AutosizeData</span></span>   | <span data-ttu-id="6ba5c-117">A coluna é redimensionada para acomodar todos os dados somente na coluna.</span><span class="sxs-lookup"><span data-stu-id="6ba5c-117">The column resizes to accommodate all data in the column only.</span></span>                                                 |
| <span data-ttu-id="6ba5c-118">Fixo</span><span class="sxs-lookup"><span data-stu-id="6ba5c-118">Fixed</span></span>          | <span data-ttu-id="6ba5c-119">A coluna é um tamanho fixo.</span><span class="sxs-lookup"><span data-stu-id="6ba5c-119">The column is a fixed size.</span></span>                                                                                    |
| <span data-ttu-id="6ba5c-120">Se estende</span><span class="sxs-lookup"><span data-stu-id="6ba5c-120">Stretches</span></span>      | <span data-ttu-id="6ba5c-121">A coluna é redimensionada para usar o espaço restante no elemento **playlist** depois que todas as outras colunas são redimensionadas.</span><span class="sxs-lookup"><span data-stu-id="6ba5c-121">The column resizes to use the remaining space in the **PLAYLIST** element after all other columns are resized.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ba5c-122">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="6ba5c-122">Return Value</span></span>

<span data-ttu-id="6ba5c-123">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6ba5c-123">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ba5c-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ba5c-124">Requirements</span></span>



| <span data-ttu-id="6ba5c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ba5c-125">Requirement</span></span> | <span data-ttu-id="6ba5c-126">Valor</span><span class="sxs-lookup"><span data-stu-id="6ba5c-126">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="6ba5c-127">Versão</span><span class="sxs-lookup"><span data-stu-id="6ba5c-127">Version</span></span><br/> | <span data-ttu-id="6ba5c-128">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="6ba5c-128">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6ba5c-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ba5c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ba5c-130">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="6ba5c-130">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





