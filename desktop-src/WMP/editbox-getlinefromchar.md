---
title: GetLineFromChar de edição
description: O método getLineFromChar recupera o índice de linha para o índice de caracteres especificado.
ms.assetid: c3a29bdf-ff63-4b6d-90e8-d414dde87f85
keywords:
- Admy. getLineFromChar Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getLineFromChar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3462ce628da72ca1e55df79e408fc79e0ec8b63a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780010"
---
# <a name="editboxgetlinefromchar"></a><span data-ttu-id="ec8f0-104">GetLineFromChar de edição</span><span class="sxs-lookup"><span data-stu-id="ec8f0-104">EDITBOX.getLineFromChar</span></span>

<span data-ttu-id="ec8f0-105">O método **getLineFromChar** recupera o índice de linha para o índice de caracteres especificado.</span><span class="sxs-lookup"><span data-stu-id="ec8f0-105">The **getLineFromChar** method retrieves the line index for the specified character index.</span></span>

``` syntax
        elementID.getLineFromChar(index)
```

## <a name="parameters"></a><span data-ttu-id="ec8f0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ec8f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec8f0-107"><span id="index"></span><span id="INDEX"></span>*index*</span><span class="sxs-lookup"><span data-stu-id="ec8f0-107"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="ec8f0-108">**Número** (**longo**) que contém o índice do caractere cujo índice de linha deve ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="ec8f0-108">**Number** (**long**) containing the index of the character whose line index is to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec8f0-109">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="ec8f0-109">Return Value</span></span>

<span data-ttu-id="ec8f0-110">Esse método retorna um **número** (**longo**).</span><span class="sxs-lookup"><span data-stu-id="ec8f0-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="ec8f0-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec8f0-111">Remarks</span></span>

<span data-ttu-id="ec8f0-112">Se a posição do caractere especificado for 1, esse método recuperará o índice de linha da linha atual.</span><span class="sxs-lookup"><span data-stu-id="ec8f0-112">If the specified character position is  1, this method retrieves the line index of the current line.</span></span>

<span data-ttu-id="ec8f0-113">Esse método só pode ser chamado depois que o controle se tornar visível.</span><span class="sxs-lookup"><span data-stu-id="ec8f0-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec8f0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec8f0-114">Requirements</span></span>



| <span data-ttu-id="ec8f0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec8f0-115">Requirement</span></span> | <span data-ttu-id="ec8f0-116">Valor</span><span class="sxs-lookup"><span data-stu-id="ec8f0-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="ec8f0-117">Versão</span><span class="sxs-lookup"><span data-stu-id="ec8f0-117">Version</span></span><br/> | <span data-ttu-id="ec8f0-118">Windows Media Player para Windows XP ou posterior</span><span class="sxs-lookup"><span data-stu-id="ec8f0-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ec8f0-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec8f0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec8f0-120">**Elemento admy**</span><span class="sxs-lookup"><span data-stu-id="ec8f0-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="ec8f0-121">**Paminhar. getline**</span><span class="sxs-lookup"><span data-stu-id="ec8f0-121">**EDITBOX.getLine**</span></span>](editbox-getline.md)
</dt> <dt>

[<span data-ttu-id="ec8f0-122">**GetLineIndex de edição**</span><span class="sxs-lookup"><span data-stu-id="ec8f0-122">**EDITBOX.getLineIndex**</span></span>](editbox-getlineindex.md)
</dt> </dl>

 

 





