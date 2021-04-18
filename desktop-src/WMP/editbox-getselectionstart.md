---
title: GetSelectionStart de edição
description: O método getSelectionStart recupera a posição inicial do texto selecionado no controle admy.
ms.assetid: 2d7efe14-549c-4f73-96a7-b8ce88b881ad
keywords:
- Admy. getSelectionStart Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getSelectionStart
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2508119e5b1d46d09b3531582e86caad7e7facbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760266"
---
# <a name="editboxgetselectionstart"></a><span data-ttu-id="5a28e-104">GetSelectionStart de edição</span><span class="sxs-lookup"><span data-stu-id="5a28e-104">EDITBOX.getSelectionStart</span></span>

<span data-ttu-id="5a28e-105">O método **getSelectionStart** recupera a posição inicial do texto selecionado no controle admy.</span><span class="sxs-lookup"><span data-stu-id="5a28e-105">The **getSelectionStart** method retrieves the starting position of the selected text in the editbox control.</span></span>

``` syntax
        elementID.getSelectionStart()
```

## <a name="parameters"></a><span data-ttu-id="5a28e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5a28e-106">Parameters</span></span>

<span data-ttu-id="5a28e-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5a28e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5a28e-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="5a28e-108">Return Value</span></span>

<span data-ttu-id="5a28e-109">Esse método retorna um **número** (**longo**).</span><span class="sxs-lookup"><span data-stu-id="5a28e-109">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="5a28e-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a28e-110">Remarks</span></span>

<span data-ttu-id="5a28e-111">Se nenhum texto for selecionado, esse método retornará a posição do ponto de inserção.</span><span class="sxs-lookup"><span data-stu-id="5a28e-111">If no text is selected, this method returns the position of the insertion point.</span></span>

<span data-ttu-id="5a28e-112">Se o controle for Multiline, esse método retornará o índice de caracteres no controle, não o índice de linha.</span><span class="sxs-lookup"><span data-stu-id="5a28e-112">If the control is multiline, this method returns the character index in the control, not the line index.</span></span>

<span data-ttu-id="5a28e-113">Esse método só pode ser chamado depois que o controle se tornar visível.</span><span class="sxs-lookup"><span data-stu-id="5a28e-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a28e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a28e-114">Requirements</span></span>



| <span data-ttu-id="5a28e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a28e-115">Requirement</span></span> | <span data-ttu-id="5a28e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="5a28e-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="5a28e-117">Versão</span><span class="sxs-lookup"><span data-stu-id="5a28e-117">Version</span></span><br/> | <span data-ttu-id="5a28e-118">Windows Media Player para Windows XP ou posterior</span><span class="sxs-lookup"><span data-stu-id="5a28e-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5a28e-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a28e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a28e-120">**Elemento admy**</span><span class="sxs-lookup"><span data-stu-id="5a28e-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="5a28e-121">**GetSelectionEnd de edição**</span><span class="sxs-lookup"><span data-stu-id="5a28e-121">**EDITBOX.getSelectionEnd**</span></span>](editbox-getselectionend.md)
</dt> <dt>

[<span data-ttu-id="5a28e-122">**ReplaceSelection de edição**</span><span class="sxs-lookup"><span data-stu-id="5a28e-122">**EDITBOX.replaceSelection**</span></span>](editbox-replaceselection.md)
</dt> <dt>

[<span data-ttu-id="5a28e-123">**Autoseleção de myselecting**</span><span class="sxs-lookup"><span data-stu-id="5a28e-123">**EDITBOX.setSelection**</span></span>](editbox-setselection.md)
</dt> </dl>

 

 





