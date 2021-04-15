---
title: PLAYLIST. sortColumn
description: O método sortColumn classifica os dados na coluna especificada.
ms.assetid: 1563fee8-044a-4cb4-a9c2-11d4533536da
keywords:
- PLAYLIST. sortColumn Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.sortColumn
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f21f0032ee4db4c7af46b5dda814bb11db551330
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768242"
---
# <a name="playlistsortcolumn"></a><span data-ttu-id="f6a43-104">PLAYLIST. sortColumn</span><span class="sxs-lookup"><span data-stu-id="f6a43-104">PLAYLIST.sortColumn</span></span>

<span data-ttu-id="f6a43-105">O método **SortColumn** classifica os dados na coluna especificada.</span><span class="sxs-lookup"><span data-stu-id="f6a43-105">The **sortColumn** method sorts the data in the specified column.</span></span>

``` syntax
        elementID.sortColumn(column)
```

## <a name="parameters"></a><span data-ttu-id="f6a43-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6a43-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6a43-107"><span id="column"></span><span id="COLUMN"></span>*pilha*</span><span class="sxs-lookup"><span data-stu-id="f6a43-107"><span id="column"></span><span id="COLUMN"></span>*column*</span></span>
</dt> <dd>

<span data-ttu-id="f6a43-108">**Número** (**longo**) indicando o índice da coluna a ser classificada.</span><span class="sxs-lookup"><span data-stu-id="f6a43-108">**Number** (**long**) indicating the index of the column to sort.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6a43-109">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="f6a43-109">Return Value</span></span>

<span data-ttu-id="f6a43-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f6a43-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6a43-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6a43-111">Remarks</span></span>

<span data-ttu-id="f6a43-112">Esse método classifica a coluna especificada da mesma maneira que os botões de cabeçalho de coluna no elemento **playlist** .</span><span class="sxs-lookup"><span data-stu-id="f6a43-112">This method sorts the specified column in the same way as the column header buttons in the **PLAYLIST** element.</span></span> <span data-ttu-id="f6a43-113">Se a coluna ainda não tiver sido classificada, ela será classificada em ordem alfanumérica.</span><span class="sxs-lookup"><span data-stu-id="f6a43-113">If the column has not yet been sorted, it is sorted in alphanumeric order.</span></span> <span data-ttu-id="f6a43-114">Se ele tiver sido classificado, sua ordem será invertida.</span><span class="sxs-lookup"><span data-stu-id="f6a43-114">If it has been sorted, its order is reversed.</span></span>

<span data-ttu-id="f6a43-115">Para que esse método funcione, o atributo **allowColumnSorting** deve ser definido como true.</span><span class="sxs-lookup"><span data-stu-id="f6a43-115">For this method to work, the **allowColumnSorting** attribute must be set to true.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6a43-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6a43-116">Requirements</span></span>



| <span data-ttu-id="f6a43-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6a43-117">Requirement</span></span> | <span data-ttu-id="f6a43-118">Valor</span><span class="sxs-lookup"><span data-stu-id="f6a43-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="f6a43-119">Versão</span><span class="sxs-lookup"><span data-stu-id="f6a43-119">Version</span></span><br/> | <span data-ttu-id="f6a43-120">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="f6a43-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f6a43-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6a43-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6a43-122">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="f6a43-122">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="f6a43-123">**PLAYLIST. allowColumnSorting**</span><span class="sxs-lookup"><span data-stu-id="f6a43-123">**PLAYLIST.allowColumnSorting**</span></span>](playlist-allowcolumnsorting.md)
</dt> </dl>

 

 





