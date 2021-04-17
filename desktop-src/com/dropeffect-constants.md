---
title: Constantes DROPEFFECT (OleIdl. h)
description: Representa informações sobre os efeitos de uma operação de arrastar e soltar.
ms.assetid: d8e46899-3fbf-4012-8dd3-67fa627526d5
topic_type:
- apiref
api_name:
- DROPEFFECT_NONE
- DROPEFFECT_COPY
- DROPEFFECT_MOVE
- DROPEFFECT_LINK
- DROPEFFECT_SCROLL
api_location:
- OleIdl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2b1888aa028d4e047a9a8ec1f54e2497fa28ce4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105784955"
---
# <a name="dropeffect-constants"></a><span data-ttu-id="20ee7-103">Constantes DROPEFFECT</span><span class="sxs-lookup"><span data-stu-id="20ee7-103">DROPEFFECT Constants</span></span>

<span data-ttu-id="20ee7-104">Representa informações sobre os efeitos de uma operação de arrastar e soltar.</span><span class="sxs-lookup"><span data-stu-id="20ee7-104">Represents information about the effects of a drag-and-drop operation.</span></span> <span data-ttu-id="20ee7-105">A função [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) e muitos dos métodos em [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) e [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) usam os valores dessa enumeração.</span><span class="sxs-lookup"><span data-stu-id="20ee7-105">The [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) function and many of the methods in the [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) and [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) use the values of this enumeration.</span></span>



| <span data-ttu-id="20ee7-106">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="20ee7-106">Constant/value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="20ee7-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="20ee7-107">Description</span></span>                                                                                                                         |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DROPEFFECT_NONE"></span><span id="dropeffect_none"></span><dl> <span data-ttu-id="20ee7-108"><dt>**DROPEFFECT \_ NENHUM**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="20ee7-108"><dt>**DROPEFFECT\_NONE**</dt> <dt>0</dt></span></span> </dl>                | <span data-ttu-id="20ee7-109">O destino de soltura não pode aceitar os dados.</span><span class="sxs-lookup"><span data-stu-id="20ee7-109">Drop target cannot accept the data.</span></span><br/>                                                                                      |
| <span id="DROPEFFECT_COPY"></span><span id="dropeffect_copy"></span><dl> <span data-ttu-id="20ee7-110"><dt>**DROPEFFECT \_ CÓPIA**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="20ee7-110"><dt>**DROPEFFECT\_COPY**</dt> <dt>1</dt></span></span> </dl>                | <span data-ttu-id="20ee7-111">Descartar resultados em uma cópia.</span><span class="sxs-lookup"><span data-stu-id="20ee7-111">Drop results in a copy.</span></span> <span data-ttu-id="20ee7-112">Os dados originais são inalterados pela fonte de arrastar.</span><span class="sxs-lookup"><span data-stu-id="20ee7-112">The original data is untouched by the drag source.</span></span><br/>                                               |
| <span id="DROPEFFECT_MOVE"></span><span id="dropeffect_move"></span><dl> <span data-ttu-id="20ee7-113"><dt>**DROPEFFECT \_ MOVER**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="20ee7-113"><dt>**DROPEFFECT\_MOVE**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="20ee7-114">A origem de arrastar deve remover os dados.</span><span class="sxs-lookup"><span data-stu-id="20ee7-114">Drag source should remove the data.</span></span> <br/>                                                                                     |
| <span id="DROPEFFECT_LINK"></span><span id="dropeffect_link"></span><dl> <span data-ttu-id="20ee7-115"><dt>**DROPEFFECT \_ LINK**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="20ee7-115"><dt>**DROPEFFECT\_LINK**</dt> <dt>4</dt></span></span> </dl>                | <span data-ttu-id="20ee7-116">A origem de arrastar deve criar um link para os dados originais.</span><span class="sxs-lookup"><span data-stu-id="20ee7-116">Drag source should create a link to the original data.</span></span><br/>                                                                   |
| <span id="DROPEFFECT_SCROLL"></span><span id="dropeffect_scroll"></span><dl> <span data-ttu-id="20ee7-117"><dt>**DROPEFFECT \_ ROLAR**</dt> <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="20ee7-117"><dt>**DROPEFFECT\_SCROLL**</dt> <dt>0x80000000</dt></span></span> </dl> | <span data-ttu-id="20ee7-118">A rolagem está prestes a iniciar ou está ocorrendo no momento no destino.</span><span class="sxs-lookup"><span data-stu-id="20ee7-118">Scrolling is about to start or is currently occurring in the target.</span></span> <span data-ttu-id="20ee7-119">Esse valor é usado além dos outros valores.</span><span class="sxs-lookup"><span data-stu-id="20ee7-119">This value is used in addition to the other values.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="20ee7-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="20ee7-120">Remarks</span></span>

<span data-ttu-id="20ee7-121">Seu aplicativo sempre deve mascarar valores da enumeração **DROPEFFECT** para garantir a compatibilidade com futuras implementações.</span><span class="sxs-lookup"><span data-stu-id="20ee7-121">Your application should always mask values from the **DROPEFFECT** enumeration to ensure compatibility with future implementations.</span></span> <span data-ttu-id="20ee7-122">Atualmente, apenas algumas das posições em um valor **DROPEFFECT** têm significado.</span><span class="sxs-lookup"><span data-stu-id="20ee7-122">Presently, only some of the positions in a **DROPEFFECT** value have meaning.</span></span> <span data-ttu-id="20ee7-123">No futuro, mais interpretações para os bits serão adicionadas.</span><span class="sxs-lookup"><span data-stu-id="20ee7-123">In the future, more interpretations for the bits will be added.</span></span> <span data-ttu-id="20ee7-124">Arrastar fontes e soltar destinos deve mascarar cuidadosamente esses valores adequadamente antes de comparar.</span><span class="sxs-lookup"><span data-stu-id="20ee7-124">Drag sources and drop targets should carefully mask these values appropriately before comparing.</span></span> <span data-ttu-id="20ee7-125">Eles nunca devem comparar um **DROPEFFECT** com relação à cópia, por exemplo, de DROPEFFECT, \_ fazendo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="20ee7-125">They should never compare a **DROPEFFECT** against, say, DROPEFFECT\_COPY by doing the following:</span></span>

``` syntax
if (dwDropEffect == DROPEFFECT_COPY)... 
```

<span data-ttu-id="20ee7-126">Em vez disso, o aplicativo sempre deve mascarar o valor ou os valores que estão sendo buscados como usando uma das seguintes técnicas:</span><span class="sxs-lookup"><span data-stu-id="20ee7-126">Instead, the application should always mask for the value or values being sought as using one of the following techniques:</span></span>

``` syntax
if (dwDropEffect & DROPEFFECT_COPY) == DROPEFFECT_COPY)...

if (dwDropEffect & DROPEFFECT_COPY)... 
```

<span data-ttu-id="20ee7-127">Isso permite a definição de novos efeitos de soltar, enquanto preserva a compatibilidade com versões anteriores com o código existente.</span><span class="sxs-lookup"><span data-stu-id="20ee7-127">This allows for the definition of new drop effects, while preserving backward compatibility with existing code.</span></span>

## <a name="requirements"></a><span data-ttu-id="20ee7-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20ee7-128">Requirements</span></span>



| <span data-ttu-id="20ee7-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="20ee7-129">Requirement</span></span> | <span data-ttu-id="20ee7-130">Valor</span><span class="sxs-lookup"><span data-stu-id="20ee7-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="20ee7-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20ee7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="20ee7-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="20ee7-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="20ee7-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20ee7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="20ee7-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="20ee7-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="20ee7-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="20ee7-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="20ee7-136"><dt>OleIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="20ee7-136"><dt>OleIdl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20ee7-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="20ee7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20ee7-138">**DoDragDrop**</span><span class="sxs-lookup"><span data-stu-id="20ee7-138">**DoDragDrop**</span></span>](/windows/desktop/api/Ole2/nf-ole2-dodragdrop)
</dt> <dt>

[<span data-ttu-id="20ee7-139">**IDropSource**</span><span class="sxs-lookup"><span data-stu-id="20ee7-139">**IDropSource**</span></span>](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)
</dt> <dt>

[<span data-ttu-id="20ee7-140">**IDropTarget**</span><span class="sxs-lookup"><span data-stu-id="20ee7-140">**IDropTarget**</span></span>](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)
</dt> </dl>

 

 





