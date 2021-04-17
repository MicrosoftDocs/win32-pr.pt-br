---
title: ReplaceSelection de edição
description: O método replaceSelection substitui a seleção atual pelo texto especificado.
ms.assetid: 600650fb-f0c8-489a-9bf2-04f31705c6b0
keywords:
- Admy. replaceSelection Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.replaceSelection
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6546f24c864d0b466acd17d9a42616c3f8ab01b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811334"
---
# <a name="editboxreplaceselection"></a><span data-ttu-id="0f09f-104">ReplaceSelection de edição</span><span class="sxs-lookup"><span data-stu-id="0f09f-104">EDITBOX.replaceSelection</span></span>

<span data-ttu-id="0f09f-105">O método **replaceSelection** substitui a seleção atual pelo texto especificado.</span><span class="sxs-lookup"><span data-stu-id="0f09f-105">The **replaceSelection** method replaces the current selection with the specified text.</span></span>

``` syntax
        elementID.replaceSelection(newValue)
```

## <a name="parameters"></a><span data-ttu-id="0f09f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0f09f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f09f-107"><span id="newValue"></span><span id="newvalue"></span><span id="NEWVALUE"></span>*newValue*</span><span class="sxs-lookup"><span data-stu-id="0f09f-107"><span id="newValue"></span><span id="newvalue"></span><span id="NEWVALUE"></span>*newValue*</span></span>
</dt> <dd>

<span data-ttu-id="0f09f-108">**Cadeia de caracteres** que contém o texto para substituir o texto selecionado.</span><span class="sxs-lookup"><span data-stu-id="0f09f-108">**String** containing the text to replace the selected text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f09f-109">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="0f09f-109">Return Value</span></span>

<span data-ttu-id="0f09f-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="0f09f-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f09f-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f09f-111">Remarks</span></span>

<span data-ttu-id="0f09f-112">Se não houver nenhum texto selecionado, o texto de substituição será inserido no local atual do ponto de inserção.</span><span class="sxs-lookup"><span data-stu-id="0f09f-112">If there is no text selected, the replacement text is inserted at the current location of the insertion point.</span></span>

<span data-ttu-id="0f09f-113">Esse método só pode ser chamado depois que o controle se tornar visível.</span><span class="sxs-lookup"><span data-stu-id="0f09f-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f09f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f09f-114">Requirements</span></span>



| <span data-ttu-id="0f09f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f09f-115">Requirement</span></span> | <span data-ttu-id="0f09f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="0f09f-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="0f09f-117">Versão</span><span class="sxs-lookup"><span data-stu-id="0f09f-117">Version</span></span><br/> | <span data-ttu-id="0f09f-118">Windows Media Player para Windows XP ou posterior</span><span class="sxs-lookup"><span data-stu-id="0f09f-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0f09f-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="0f09f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f09f-120">**Elemento admy**</span><span class="sxs-lookup"><span data-stu-id="0f09f-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="0f09f-121">**GetSelectionEnd de edição**</span><span class="sxs-lookup"><span data-stu-id="0f09f-121">**EDITBOX.getSelectionEnd**</span></span>](editbox-getselectionend.md)
</dt> <dt>

[<span data-ttu-id="0f09f-122">**GetSelectionStart de edição**</span><span class="sxs-lookup"><span data-stu-id="0f09f-122">**EDITBOX.getSelectionStart**</span></span>](editbox-getselectionstart.md)
</dt> <dt>

[<span data-ttu-id="0f09f-123">**Autoseleção de myselecting**</span><span class="sxs-lookup"><span data-stu-id="0f09f-123">**EDITBOX.setSelection**</span></span>](editbox-setselection.md)
</dt> </dl>

 

 





