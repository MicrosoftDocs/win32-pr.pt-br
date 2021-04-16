---
title: Autoseleção de myselecting
description: O método setseleções seleciona o texto no controle caixa de edição do índice inicial especificado para o índice final especificado.
ms.assetid: 97b20a17-4b9c-4144-b448-8d7611c0e994
keywords:
- Admy. setselecting Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.setSelection
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d7077de0ea59940c4afa551d22188d5583d0e4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758217"
---
# <a name="editboxsetselection"></a><span data-ttu-id="606fb-104">Autoseleção de myselecting</span><span class="sxs-lookup"><span data-stu-id="606fb-104">EDITBOX.setSelection</span></span>

<span data-ttu-id="606fb-105">O método **setseleções** seleciona o texto no controle caixa de edição do índice inicial especificado para o índice final especificado.</span><span class="sxs-lookup"><span data-stu-id="606fb-105">The **setSelection** method selects the text in the edit box control from the specified start index to the specified end index.</span></span>

``` syntax
        elementID.setSelection(start, end)
```

## <a name="parameters"></a><span data-ttu-id="606fb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="606fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="606fb-107"><span id="start"></span><span id="START"></span>*Comece*</span><span class="sxs-lookup"><span data-stu-id="606fb-107"><span id="start"></span><span id="START"></span>*start*</span></span>
</dt> <dd>

<span data-ttu-id="606fb-108">**Número** (**longo**) que contém o índice de caracteres da posição inicial do texto selecionado.</span><span class="sxs-lookup"><span data-stu-id="606fb-108">**Number** (**long**) containing the character index of the starting position of the selected text.</span></span>

</dd> <dt>

<span data-ttu-id="606fb-109"><span id="end"></span><span id="END"></span>*completo*</span><span class="sxs-lookup"><span data-stu-id="606fb-109"><span id="end"></span><span id="END"></span>*end*</span></span>
</dt> <dd>

<span data-ttu-id="606fb-110">**Número** (**longo**) que contém o índice de caracteres da posição final do texto selecionado.</span><span class="sxs-lookup"><span data-stu-id="606fb-110">**Number** (**long**) containing the character index of the ending position of the selected text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="606fb-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="606fb-111">Return Value</span></span>

<span data-ttu-id="606fb-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="606fb-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="606fb-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="606fb-113">Remarks</span></span>

<span data-ttu-id="606fb-114">Se o início for 0 e o final for 1, todo o texto no controle caixa de edição será selecionado.</span><span class="sxs-lookup"><span data-stu-id="606fb-114">If the start is 0 and the end is  1, all of the text in the edit box control is selected.</span></span> <span data-ttu-id="606fb-115">Se o início for 1, qualquer seleção atual será desmarcada.</span><span class="sxs-lookup"><span data-stu-id="606fb-115">If the start is  1, any current selection is deselected.</span></span>

<span data-ttu-id="606fb-116">Esse método só pode ser chamado depois que o controle se tornar visível.</span><span class="sxs-lookup"><span data-stu-id="606fb-116">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="606fb-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="606fb-117">Requirements</span></span>



| <span data-ttu-id="606fb-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="606fb-118">Requirement</span></span> | <span data-ttu-id="606fb-119">Valor</span><span class="sxs-lookup"><span data-stu-id="606fb-119">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="606fb-120">Versão</span><span class="sxs-lookup"><span data-stu-id="606fb-120">Version</span></span><br/> | <span data-ttu-id="606fb-121">Windows Media Player para Windows XP ou posterior</span><span class="sxs-lookup"><span data-stu-id="606fb-121">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="606fb-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="606fb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="606fb-123">**Elemento admy**</span><span class="sxs-lookup"><span data-stu-id="606fb-123">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="606fb-124">**GetSelectionEnd de edição**</span><span class="sxs-lookup"><span data-stu-id="606fb-124">**EDITBOX.getSelectionEnd**</span></span>](editbox-getselectionend.md)
</dt> <dt>

[<span data-ttu-id="606fb-125">**GetSelectionStart de edição**</span><span class="sxs-lookup"><span data-stu-id="606fb-125">**EDITBOX.getSelectionStart**</span></span>](editbox-getselectionstart.md)
</dt> <dt>

[<span data-ttu-id="606fb-126">**ReplaceSelection de edição**</span><span class="sxs-lookup"><span data-stu-id="606fb-126">**EDITBOX.replaceSelection**</span></span>](editbox-replaceselection.md)
</dt> </dl>

 

 





