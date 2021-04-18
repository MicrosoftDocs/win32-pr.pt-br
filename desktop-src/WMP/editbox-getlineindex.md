---
title: GetLineIndex de edição
description: O método getLineIndex recupera o índice de caracteres do primeiro caractere na linha com o índice de linha especificado.
ms.assetid: 1298227a-d839-44fc-bacb-44c3c968bd94
keywords:
- Admy. getLineIndex Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getLineIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5f55027bb7d577b7080ad2f006a5a006e718c2d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770502"
---
# <a name="editboxgetlineindex"></a><span data-ttu-id="f944e-104">GetLineIndex de edição</span><span class="sxs-lookup"><span data-stu-id="f944e-104">EDITBOX.getLineIndex</span></span>

<span data-ttu-id="f944e-105">O método **getLineIndex** recupera o índice de caracteres do primeiro caractere na linha com o índice de linha especificado.</span><span class="sxs-lookup"><span data-stu-id="f944e-105">The **getLineIndex** method retrieves the character index of the first character on the line with the specified line index.</span></span>

``` syntax
        elementID.getLineIndex(index)
```

## <a name="parameters"></a><span data-ttu-id="f944e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f944e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f944e-107"><span id="index"></span><span id="INDEX"></span>*index*</span><span class="sxs-lookup"><span data-stu-id="f944e-107"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="f944e-108">**Número** (**longo**) que contém o índice da linha cujo índice de caracteres deve ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="f944e-108">**Number** (**long**) containing the index of the line whose character index is to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f944e-109">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="f944e-109">Return Value</span></span>

<span data-ttu-id="f944e-110">Esse método retorna um **número** (**longo**).</span><span class="sxs-lookup"><span data-stu-id="f944e-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="f944e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f944e-111">Remarks</span></span>

<span data-ttu-id="f944e-112">Se o índice de linha especificado for 1, a linha que contém o ponto de inserção será usada.</span><span class="sxs-lookup"><span data-stu-id="f944e-112">If the specified line index is  1, the line containing the insertion point is used.</span></span>

<span data-ttu-id="f944e-113">Esse método só pode ser chamado depois que o controle se tornar visível.</span><span class="sxs-lookup"><span data-stu-id="f944e-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="f944e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f944e-114">Requirements</span></span>



| <span data-ttu-id="f944e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f944e-115">Requirement</span></span> | <span data-ttu-id="f944e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="f944e-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="f944e-117">Versão</span><span class="sxs-lookup"><span data-stu-id="f944e-117">Version</span></span><br/> | <span data-ttu-id="f944e-118">Windows Media Player para Windows XP ou posterior</span><span class="sxs-lookup"><span data-stu-id="f944e-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f944e-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="f944e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f944e-120">**Elemento admy**</span><span class="sxs-lookup"><span data-stu-id="f944e-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="f944e-121">**Paminhar. getline**</span><span class="sxs-lookup"><span data-stu-id="f944e-121">**EDITBOX.getLine**</span></span>](editbox-getline.md)
</dt> <dt>

[<span data-ttu-id="f944e-122">**GetLineFromChar de edição**</span><span class="sxs-lookup"><span data-stu-id="f944e-122">**EDITBOX.getLineFromChar**</span></span>](editbox-getlinefromchar.md)
</dt> </dl>

 

 





