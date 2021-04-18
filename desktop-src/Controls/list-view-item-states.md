---
title: Estados do item de List-View (CommCtrl. h)
description: O valor de estado de um item consiste no estado do item, um índice de máscara de sobreposição opcional e um índice de máscara de imagem de estado opcional.
ms.assetid: 21827f4a-f133-489b-bbd2-6979d1928b40
topic_type:
- apiref
api_name:
- LVIS_ACTIVATING
- LVIS_CUT
- LVIS_DROPHILITED
- LVIS_FOCUSED
- LVIS_OVERLAYMASK
- LVIS_SELECTED
- LVIS_STATEIMAGEMASK
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8432760dd4cc7efde30700f837864ddcf04aac31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752798"
---
# <a name="list-view-item-states"></a><span data-ttu-id="61cec-103">List-View Estados do item</span><span class="sxs-lookup"><span data-stu-id="61cec-103">List-View Item States</span></span>

<span data-ttu-id="61cec-104">O valor de estado de um item consiste no estado do item, um índice de máscara de sobreposição opcional e um índice de máscara de imagem de estado opcional.</span><span class="sxs-lookup"><span data-stu-id="61cec-104">An item's state value consists of the item's state, an optional overlay mask index, and an optional state image mask index.</span></span>

<span data-ttu-id="61cec-105">O estado de um item determina sua aparência e funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="61cec-105">An item's state determines its appearance and functionality.</span></span> <span data-ttu-id="61cec-106">O estado pode ser zero ou um ou mais dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="61cec-106">The state can be zero or one or more of the following values:</span></span>



| <span data-ttu-id="61cec-107">Constante</span><span class="sxs-lookup"><span data-stu-id="61cec-107">Constant</span></span>                                                                                                                                                                        | <span data-ttu-id="61cec-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="61cec-108">Description</span></span>                                                                                                                                                          |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVIS_ACTIVATING"></span><span id="lvis_activating"></span><dl> <span data-ttu-id="61cec-109"><dt>**ativação do LVIS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="61cec-109"><dt>**LVIS\_ACTIVATING**</dt></span></span> </dl>             | <span data-ttu-id="61cec-110">Não há suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="61cec-110">Not currently supported.</span></span><br/>                                                                                                                                  |
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <span data-ttu-id="61cec-111"><dt>**LVIS \_ recortar**</dt></span><span class="sxs-lookup"><span data-stu-id="61cec-111"><dt>**LVIS\_CUT**</dt></span></span> </dl>                                  | <span data-ttu-id="61cec-112">O item é marcado para uma operação de recortar e colar.</span><span class="sxs-lookup"><span data-stu-id="61cec-112">The item is marked for a cut-and-paste operation.</span></span><br/>                                                                                                         |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <span data-ttu-id="61cec-113"><dt>**LVIS \_ DROPHILITED**</dt></span><span class="sxs-lookup"><span data-stu-id="61cec-113"><dt>**LVIS\_DROPHILITED**</dt></span></span> </dl>          | <span data-ttu-id="61cec-114">O item é realçado como um destino do tipo "arrastar e soltar".</span><span class="sxs-lookup"><span data-stu-id="61cec-114">The item is highlighted as a drag-and-drop target.</span></span><br/>                                                                                                        |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <span data-ttu-id="61cec-115"><dt>**LVIS com \_ foco**</dt></span><span class="sxs-lookup"><span data-stu-id="61cec-115"><dt>**LVIS\_FOCUSED**</dt></span></span> </dl>                      | <span data-ttu-id="61cec-116">O item tem o foco, portanto, está circundado por um retângulo de foco padrão.</span><span class="sxs-lookup"><span data-stu-id="61cec-116">The item has the focus, so it is surrounded by a standard focus rectangle.</span></span> <span data-ttu-id="61cec-117">Embora mais de um item possa ser selecionado, somente um item pode ter o foco.</span><span class="sxs-lookup"><span data-stu-id="61cec-117">Although more than one item may be selected, only one item can have the focus.</span></span><br/> |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <span data-ttu-id="61cec-118"><dt>**LVIS \_ OVERLAYMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="61cec-118"><dt>**LVIS\_OVERLAYMASK**</dt></span></span> </dl>          | <span data-ttu-id="61cec-119">O índice de imagem de sobreposição do item é recuperado por uma máscara.</span><span class="sxs-lookup"><span data-stu-id="61cec-119">The item's overlay image index is retrieved by a mask.</span></span><br/>                                                                                                    |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <span data-ttu-id="61cec-120"><dt>**LVIS \_ selecionado**</dt></span><span class="sxs-lookup"><span data-stu-id="61cec-120"><dt>**LVIS\_SELECTED**</dt></span></span> </dl>                   | <span data-ttu-id="61cec-121">O item está selecionado.</span><span class="sxs-lookup"><span data-stu-id="61cec-121">The item is selected.</span></span> <span data-ttu-id="61cec-122">A aparência de um item selecionado depende de se ele tem o foco e também das cores do sistema usadas para seleção.</span><span class="sxs-lookup"><span data-stu-id="61cec-122">The appearance of a selected item depends on whether it has the focus and also on the system colors used for selection.</span></span><br/>             |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <span data-ttu-id="61cec-123"><dt>**LVIS \_ STATEIMAGEMASK**</dt></span><span class="sxs-lookup"><span data-stu-id="61cec-123"><dt>**LVIS\_STATEIMAGEMASK**</dt></span></span> </dl> | <span data-ttu-id="61cec-124">O índice de imagem de estado do item é recuperado por uma máscara.</span><span class="sxs-lookup"><span data-stu-id="61cec-124">The item's state image index is retrieved by a mask.</span></span><br/>                                                                                                      |



## <a name="remarks"></a><span data-ttu-id="61cec-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="61cec-125">Remarks</span></span>

<span data-ttu-id="61cec-126">Você pode usar a máscara **LVIS \_ OVERLAYMASK** para isolar o índice baseado em um da imagem de sobreposição.</span><span class="sxs-lookup"><span data-stu-id="61cec-126">You can use the **LVIS\_OVERLAYMASK** mask to isolate the one-based index of the overlay image.</span></span> <span data-ttu-id="61cec-127">Você pode usar a máscara **LVIS \_ STATEIMAGEMASK** para isolar o índice baseado em um da imagem de estado.</span><span class="sxs-lookup"><span data-stu-id="61cec-127">You can use the **LVIS\_STATEIMAGEMASK** mask to isolate the one-based index of the state image.</span></span>

## <a name="requirements"></a><span data-ttu-id="61cec-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61cec-128">Requirements</span></span>



| <span data-ttu-id="61cec-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="61cec-129">Requirement</span></span> | <span data-ttu-id="61cec-130">Valor</span><span class="sxs-lookup"><span data-stu-id="61cec-130">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61cec-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="61cec-131">Header</span></span><br/> | <dl> <span data-ttu-id="61cec-132"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="61cec-132"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





