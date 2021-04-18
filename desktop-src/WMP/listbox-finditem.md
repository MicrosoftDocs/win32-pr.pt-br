---
title: LISTBOX. findItem
description: O método findItem pesquisa uma determinada cadeia de caracteres começando com o item após o índice de item especificado.
ms.assetid: 8d112d99-1866-45e5-b0ef-5d4a3c8b388d
keywords:
- LISTBOX. findItem Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.findItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 161f4dd8b93fe4fed6a794dffde3e58e840c74e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760511"
---
# <a name="listboxfinditem"></a><span data-ttu-id="2fa88-104">LISTBOX. findItem</span><span class="sxs-lookup"><span data-stu-id="2fa88-104">LISTBOX.findItem</span></span>

<span data-ttu-id="2fa88-105">O método **findItem** pesquisa uma determinada cadeia de caracteres começando com o item após o índice de item especificado.</span><span class="sxs-lookup"><span data-stu-id="2fa88-105">The **findItem** method searches for a given string starting with the item following the specified item index.</span></span>

``` syntax
        elementID.findItem(startIndex, searchString)
```

## <a name="parameters"></a><span data-ttu-id="2fa88-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2fa88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fa88-107"><span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*startIndex*</span><span class="sxs-lookup"><span data-stu-id="2fa88-107"><span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*startIndex*</span></span>
</dt> <dd>

<span data-ttu-id="2fa88-108">**Número** (**longo**) que contém o índice do item no qual iniciar a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="2fa88-108">**Number** (**long**) containing the index of the item at which to start the search.</span></span>

</dd> <dt>

<span data-ttu-id="2fa88-109"><span id="searchString"></span><span id="searchstring"></span><span id="SEARCHSTRING"></span>*searchString*</span><span class="sxs-lookup"><span data-stu-id="2fa88-109"><span id="searchString"></span><span id="searchstring"></span><span id="SEARCHSTRING"></span>*searchString*</span></span>
</dt> <dd>

<span data-ttu-id="2fa88-110">**Cadeia de caracteres** que contém o texto a ser pesquisado.</span><span class="sxs-lookup"><span data-stu-id="2fa88-110">**String** containing the text to search for.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fa88-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="2fa88-111">Return Value</span></span>

<span data-ttu-id="2fa88-112">Esse método retorna um **número** (**Long**) que contém o índice do item que contém a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="2fa88-112">This method returns a **Number** (**long**) containing the index of the item that contains the string.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fa88-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="2fa88-113">Remarks</span></span>

<span data-ttu-id="2fa88-114">Para iniciar a pesquisa na primeira linha do controle caixa de listagem, use 1 como o *startIndex*.</span><span class="sxs-lookup"><span data-stu-id="2fa88-114">To start the search at the first line of the list box control, use  1 as the *startIndex*.</span></span> <span data-ttu-id="2fa88-115">Para continuar pesquisando texto após a primeira linha ser encontrada, use o índice de linha retornado como *startIndex* e a pesquisa será iniciada na próxima linha.</span><span class="sxs-lookup"><span data-stu-id="2fa88-115">To continue to search for text after the first line is found, use the returned line index as the *startIndex*, and the search will start at the next line.</span></span> <span data-ttu-id="2fa88-116">Esse método irá procurar subcadeias de caracteres e não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="2fa88-116">This method will search for substrings and is not case-sensitive.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fa88-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fa88-117">Requirements</span></span>



| <span data-ttu-id="2fa88-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fa88-118">Requirement</span></span> | <span data-ttu-id="2fa88-119">Valor</span><span class="sxs-lookup"><span data-stu-id="2fa88-119">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="2fa88-120">Versão</span><span class="sxs-lookup"><span data-stu-id="2fa88-120">Version</span></span><br/> | <span data-ttu-id="2fa88-121">Windows Media Player para Windows XP ou posterior</span><span class="sxs-lookup"><span data-stu-id="2fa88-121">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2fa88-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="2fa88-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fa88-123">**Elemento LISTBOX**</span><span class="sxs-lookup"><span data-stu-id="2fa88-123">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> </dl>

 

 





