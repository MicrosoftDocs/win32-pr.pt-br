---
title: LISTBOX. getNextSelectedItem
description: O método getNextSelectedItem recupera o próximo item selecionado no controle caixa de listagem, começando no item após aquele com o índice especificado.
ms.assetid: 060d196d-2b14-4386-ba01-34256c137db5
keywords:
- LISTBOX. getNextSelectedItem Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8afb3df1f1b6a6adc528e02dd6531ac4fc1a9a3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784494"
---
# <a name="listboxgetnextselecteditem"></a><span data-ttu-id="bf892-104">LISTBOX. getNextSelectedItem</span><span class="sxs-lookup"><span data-stu-id="bf892-104">LISTBOX.getNextSelectedItem</span></span>

<span data-ttu-id="bf892-105">O método **getNextSelectedItem** recupera o próximo item selecionado no controle caixa de listagem, começando no item após aquele com o índice especificado.</span><span class="sxs-lookup"><span data-stu-id="bf892-105">The **getNextSelectedItem** method retrieves the next selected item in the list box control starting at the item after the one with the specified index.</span></span>

``` syntax
        elementID.getNextSelectedItem(startIndex)
```

## <a name="parameters"></a><span data-ttu-id="bf892-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bf892-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf892-107"><span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*startIndex*</span><span class="sxs-lookup"><span data-stu-id="bf892-107"><span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*startIndex*</span></span>
</dt> <dd>

<span data-ttu-id="bf892-108">**Número** (**longo**) que contém o índice do item que precede o item que está sendo recuperado.</span><span class="sxs-lookup"><span data-stu-id="bf892-108">**Number** (**long**) containing the index of the item that precedes the item being retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf892-109">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="bf892-109">Return Value</span></span>

<span data-ttu-id="bf892-110">Esse método retorna um **número** (**Long**) que contém o índice do próximo item selecionado.</span><span class="sxs-lookup"><span data-stu-id="bf892-110">This method returns a **Number** (**long**) containing the index of the next selected item.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf892-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf892-111">Remarks</span></span>

<span data-ttu-id="bf892-112">Para iniciar a pesquisa desde o início, use 1 para o índice inicial.</span><span class="sxs-lookup"><span data-stu-id="bf892-112">To start search from the beginning, use  1 for the start index.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf892-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf892-113">Requirements</span></span>



| <span data-ttu-id="bf892-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf892-114">Requirement</span></span> | <span data-ttu-id="bf892-115">Valor</span><span class="sxs-lookup"><span data-stu-id="bf892-115">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="bf892-116">Versão</span><span class="sxs-lookup"><span data-stu-id="bf892-116">Version</span></span><br/> | <span data-ttu-id="bf892-117">Windows Media Player para Windows XP ou posterior</span><span class="sxs-lookup"><span data-stu-id="bf892-117">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bf892-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf892-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf892-119">**Elemento LISTBOX**</span><span class="sxs-lookup"><span data-stu-id="bf892-119">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> </dl>

 

 





