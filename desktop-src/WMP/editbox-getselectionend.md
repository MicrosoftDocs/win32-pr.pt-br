---
title: GetSelectionEnd de edição
description: O método getSelectionEnd recupera a posição final do texto selecionado no controle admy.
ms.assetid: 82a445da-3c50-41b7-8ac8-da6c860056ba
keywords:
- Admy. getSelectionEnd Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getSelectionEnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f27c2974360e7e77becfa67a27b4e96b529ad1e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811113"
---
# <a name="editboxgetselectionend"></a><span data-ttu-id="c679c-104">GetSelectionEnd de edição</span><span class="sxs-lookup"><span data-stu-id="c679c-104">EDITBOX.getSelectionEnd</span></span>

<span data-ttu-id="c679c-105">O método **getSelectionEnd** recupera a posição final do texto selecionado no controle admy.</span><span class="sxs-lookup"><span data-stu-id="c679c-105">The **getSelectionEnd** method retrieves the ending position of the selected text in the editbox control.</span></span>

``` syntax
        elementID.getSelectionEnd()
```

## <a name="parameters"></a><span data-ttu-id="c679c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c679c-106">Parameters</span></span>

<span data-ttu-id="c679c-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c679c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c679c-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c679c-108">Return Value</span></span>

<span data-ttu-id="c679c-109">Esse método retorna um **número** (**longo**).</span><span class="sxs-lookup"><span data-stu-id="c679c-109">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="c679c-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="c679c-110">Remarks</span></span>

<span data-ttu-id="c679c-111">Se nenhum texto for selecionado, esse método retornará a posição do ponto de inserção.</span><span class="sxs-lookup"><span data-stu-id="c679c-111">If no text is selected, this method returns the position of the insertion point.</span></span>

<span data-ttu-id="c679c-112">Se o controle for Multiline, esse método retornará o índice de caracteres no controle, não o índice de linha.</span><span class="sxs-lookup"><span data-stu-id="c679c-112">If the control is multiline, this method returns the character index in the control, not the line index.</span></span>

<span data-ttu-id="c679c-113">Esse método só pode ser chamado depois que o controle se tornar visível.</span><span class="sxs-lookup"><span data-stu-id="c679c-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="c679c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c679c-114">Requirements</span></span>



| <span data-ttu-id="c679c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c679c-115">Requirement</span></span> | <span data-ttu-id="c679c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c679c-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="c679c-117">Versão</span><span class="sxs-lookup"><span data-stu-id="c679c-117">Version</span></span><br/> | <span data-ttu-id="c679c-118">Windows Media Player para Windows XP ou posterior</span><span class="sxs-lookup"><span data-stu-id="c679c-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c679c-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="c679c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c679c-120">**Elemento admy**</span><span class="sxs-lookup"><span data-stu-id="c679c-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="c679c-121">**GetSelectionStart de edição**</span><span class="sxs-lookup"><span data-stu-id="c679c-121">**EDITBOX.getSelectionStart**</span></span>](editbox-getselectionstart.md)
</dt> <dt>

[<span data-ttu-id="c679c-122">**ReplaceSelection de edição**</span><span class="sxs-lookup"><span data-stu-id="c679c-122">**EDITBOX.replaceSelection**</span></span>](editbox-replaceselection.md)
</dt> <dt>

[<span data-ttu-id="c679c-123">**Autoseleção de myselecting**</span><span class="sxs-lookup"><span data-stu-id="c679c-123">**EDITBOX.setSelection**</span></span>](editbox-setselection.md)
</dt> </dl>

 

 





