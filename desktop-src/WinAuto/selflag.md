---
title: Constantes SELFLAG (OleAcc. h)
description: Este tópico descreve os valores constantes usados para especificar como um objeto acessível é selecionado ou leva em foco.
ms.assetid: 52755540-dcf4-4e0b-bb5c-88b05f134d79
topic_type:
- apiref
api_name:
- SELFLAG_NONE
- SELFLAG_TAKEFOCUS
- SELFLAG_TAKESELECTION
- SELFLAG_EXTENDSELECTION
- SELFLAG_ADDSELECTION
- SELFLAG_REMOVESELECTION
api_location:
- oleacc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb49daffd2bb20e705d17aa51c3bff3d9622a6de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105807962"
---
# <a name="selflag-constants"></a><span data-ttu-id="bba50-103">Constantes SELFLAG</span><span class="sxs-lookup"><span data-stu-id="bba50-103">SELFLAG Constants</span></span>

<span data-ttu-id="bba50-104">Este tópico descreve os valores constantes usados para especificar como um objeto acessível é selecionado ou leva em foco.</span><span class="sxs-lookup"><span data-stu-id="bba50-104">This topic describes the constant values used to specify how an accessible object becomes selected or takes the focus.</span></span> <span data-ttu-id="bba50-105">As constantes são definidas em OleAcc. h e são usadas com o método [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) .</span><span class="sxs-lookup"><span data-stu-id="bba50-105">The constants are defined in oleacc.h and are used with the [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) method.</span></span>

<span data-ttu-id="bba50-106">As seguintes combinações não são permitidas:</span><span class="sxs-lookup"><span data-stu-id="bba50-106">The following combinations are not allowed:</span></span>

-   <span data-ttu-id="bba50-107">SELFLAG \_ ADDselecting \| SELFLAG \_ REMOVESELECTION</span><span class="sxs-lookup"><span data-stu-id="bba50-107">SELFLAG\_ADDSELECTION \| SELFLAG\_REMOVESELECTION</span></span>
-   <span data-ttu-id="bba50-108">SELFLAG \_ ADDselecting \| SELFLAG \_ TAKESELECTION</span><span class="sxs-lookup"><span data-stu-id="bba50-108">SELFLAG\_ADDSELECTION \| SELFLAG\_TAKESELECTION</span></span>
-   <span data-ttu-id="bba50-109">SELFLAG \_ REMOVESELECTION \| SELFLAG \_ TAKESELECTION</span><span class="sxs-lookup"><span data-stu-id="bba50-109">SELFLAG\_REMOVESELECTION \| SELFLAG\_TAKESELECTION</span></span>
-   <span data-ttu-id="bba50-110">SELFLAG \_ EXTENDSELECTION \| SELFLAG \_ TAKESELECTION</span><span class="sxs-lookup"><span data-stu-id="bba50-110">SELFLAG\_EXTENDSELECTION \| SELFLAG\_TAKESELECTION</span></span>

<span data-ttu-id="bba50-111">**Observação para clientes:** O Microsoft Acessibilidade Ativa não oferece suporte à seleção do texto contido em controles editar e Rich Edit porque o texto é exposto como uma cadeia de caracteres na [propriedade Value](value-property.md)do objeto.</span><span class="sxs-lookup"><span data-stu-id="bba50-111">**Note to clients :** Microsoft Active Accessibility does not support the selection of the text contained in edit and rich edit controls because the text is exposed as a string in the object's [Value property](value-property.md).</span></span>

<span data-ttu-id="bba50-112">Para obter informações sobre como executar operações de seleção complexas, consulte [selecionando objetos filho](selecting-child-objects.md).</span><span class="sxs-lookup"><span data-stu-id="bba50-112">For information on how to perform complex selection operations, see [Selecting Child Objects](selecting-child-objects.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="bba50-113">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="bba50-113">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="bba50-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="bba50-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_NONE"></span><span id="selflag_none"></span><dl> <span data-ttu-id="bba50-115"><dt><strong>SELFLAG_NONE</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="bba50-115"><dt><strong>SELFLAG_NONE</strong></dt> <dt>0</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bba50-116">Não executa nenhuma ação.</span><span class="sxs-lookup"><span data-stu-id="bba50-116">Performs no action.</span></span> <span data-ttu-id="bba50-117">O Microsoft Acessibilidade Ativa não altera a seleção ou o foco.</span><span class="sxs-lookup"><span data-stu-id="bba50-117">Microsoft Active Accessibility does not change the selection or focus.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_TAKEFOCUS"></span><span id="selflag_takefocus"></span><dl> <span data-ttu-id="bba50-118"><dt><strong>SELFLAG_TAKEFOCUS</strong></dt> <dt>0x1</dt> </span><span class="sxs-lookup"><span data-stu-id="bba50-118"><dt><strong>SELFLAG_TAKEFOCUS</strong></dt> <dt>0x1</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bba50-119">Define o foco para o objeto e o transforma na âncora de seleção.</span><span class="sxs-lookup"><span data-stu-id="bba50-119">Sets the focus to the object and makes it the selection anchor.</span></span> <span data-ttu-id="bba50-120">Usado por si só, esse sinalizador não altera a seleção.</span><span class="sxs-lookup"><span data-stu-id="bba50-120">Used by itself, this flag does not alter the selection.</span></span> <span data-ttu-id="bba50-121">O efeito é semelhante a mover o foco manualmente pressionando uma tecla de seta enquanto mantém pressionada a tecla CTRL no Windows Explorer ou em qualquer caixa de listagem de seleção múltipla.</span><span class="sxs-lookup"><span data-stu-id="bba50-121">The effect is similar to moving the focus manually by pressing an ARROW key while holding down the CTRL key in Windows Explorer or in any multiple-selection list box.</span></span> <br/> <span data-ttu-id="bba50-122">Com objetos que têm o <a href="object-state-constants.md"><strong>STATE_SYSTEM_MULTISELECTABLE</strong></a>, SELFLAG_TAKEFOCUS é combinado com os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="bba50-122">With objects that have the <a href="object-state-constants.md"><strong>STATE_SYSTEM_MULTISELECTABLE</strong></a>, SELFLAG_TAKEFOCUS is combined with the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="bba50-123">SELFLAG_TAKESELECTION</span><span class="sxs-lookup"><span data-stu-id="bba50-123">SELFLAG_TAKESELECTION</span></span></li>
<li><span data-ttu-id="bba50-124">SELFLAG_EXTENDSELECTION</span><span class="sxs-lookup"><span data-stu-id="bba50-124">SELFLAG_EXTENDSELECTION</span></span></li>
<li><span data-ttu-id="bba50-125">SELFLAG_ADDSELECTION</span><span class="sxs-lookup"><span data-stu-id="bba50-125">SELFLAG_ADDSELECTION</span></span></li>
<li><span data-ttu-id="bba50-126">SELFLAG_REMOVESELECTION</span><span class="sxs-lookup"><span data-stu-id="bba50-126">SELFLAG_REMOVESELECTION</span></span></li>
<li><span data-ttu-id="bba50-127">SELFLAG_ADDSELECTION | SELFLAG_EXTENDSELECTION</span><span class="sxs-lookup"><span data-stu-id="bba50-127">SELFLAG_ADDSELECTION | SELFLAG_EXTENDSELECTION</span></span></li>
<li><span data-ttu-id="bba50-128">SELFLAG_REMOVESELECTION | SELFLAG_EXTENDSELECTION</span><span class="sxs-lookup"><span data-stu-id="bba50-128">SELFLAG_REMOVESELECTION | SELFLAG_EXTENDSELECTION</span></span></li>
</ul>
<span data-ttu-id="bba50-129">Se você chamar <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect"><strong>IAccessible:: accSelect</strong></a> com o sinalizador SELFLAG_TAKEFOCUS em um objeto que tem um <strong>HWND</strong>, o sinalizador entrará em vigor somente se o pai do objeto já tiver o foco.</span><span class="sxs-lookup"><span data-stu-id="bba50-129">If you call <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect"><strong>IAccessible::accSelect</strong></a> with the SELFLAG_TAKEFOCUS flag on an object that has an <strong>HWND</strong>, the flag will take effect only if the object's parent already has the focus.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_TAKESELECTION"></span><span id="selflag_takeselection"></span><dl> <span data-ttu-id="bba50-130"><dt><strong>SELFLAG_TAKESELECTION</strong></dt> <dt>0x2</dt> </span><span class="sxs-lookup"><span data-stu-id="bba50-130"><dt><strong>SELFLAG_TAKESELECTION</strong></dt> <dt>0x2</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bba50-131">Seleciona o objeto e remove a seleção de todos os outros objetos no contêiner.</span><span class="sxs-lookup"><span data-stu-id="bba50-131">Selects the object and removes the selection from all other objects in the container.</span></span> <br/> <span data-ttu-id="bba50-132">A menos que seja combinado com SELFLAG_TAKEFOCUS, esse sinalizador não altera o foco ou a âncora de seleção.</span><span class="sxs-lookup"><span data-stu-id="bba50-132">Unless it is combined with SELFLAG_TAKEFOCUS, this flag does not change the focus or the selection anchor.</span></span> <span data-ttu-id="bba50-133">O SELFLAG_TAKESELECTION | SELFLAG_TAKEFOCUS combinação é equivalente a clicar uma vez em um item no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="bba50-133">The SELFLAG_TAKESELECTION | SELFLAG_TAKEFOCUS combination is equivalent to single-clicking an item in Windows Explorer.</span></span><br/> <span data-ttu-id="bba50-134">Esse sinalizador não deve ser combinado com os seguintes sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="bba50-134">This flag must not be combined with the following flags:</span></span><br/>
<ul>
<li><span data-ttu-id="bba50-135">SELFLAG_ADDSELECTION</span><span class="sxs-lookup"><span data-stu-id="bba50-135">SELFLAG_ADDSELECTION</span></span></li>
<li><span data-ttu-id="bba50-136">SELFLAG_REMOVESELECTION</span><span class="sxs-lookup"><span data-stu-id="bba50-136">SELFLAG_REMOVESELECTION</span></span></li>
<li><span data-ttu-id="bba50-137">SELFLAG_EXTENDSELECTION</span><span class="sxs-lookup"><span data-stu-id="bba50-137">SELFLAG_EXTENDSELECTION</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_EXTENDSELECTION"></span><span id="selflag_extendselection"></span><dl> <span data-ttu-id="bba50-138"><dt><strong>SELFLAG_EXTENDSELECTION</strong></dt> <dt>0x4</dt> </span><span class="sxs-lookup"><span data-stu-id="bba50-138"><dt><strong>SELFLAG_EXTENDSELECTION</strong></dt> <dt>0x4</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bba50-139">Altera a seleção de forma que todos os objetos entre a âncora de seleção e esse objeto tenham o estado de seleção do objeto de âncora.</span><span class="sxs-lookup"><span data-stu-id="bba50-139">Alters the selection so that all objects between the selection anchor and this object take on the anchor object's selection state.</span></span> <span data-ttu-id="bba50-140">Se o objeto de âncora não for selecionado, os objetos serão removidos da seleção.</span><span class="sxs-lookup"><span data-stu-id="bba50-140">If the anchor object is not selected, the objects are removed from the selection.</span></span> <span data-ttu-id="bba50-141">Se o objeto Anchor for selecionado, a seleção será estendida para incluir esse objeto e todos os objetos entre eles.</span><span class="sxs-lookup"><span data-stu-id="bba50-141">If the anchor object is selected, the selection is extended to include this object and all the objects in between.</span></span> <span data-ttu-id="bba50-142">Defina o estado de seleção combinando esse sinalizador com SELFLAG_ADDSELECTION ou SELFLAG_REMOVESELECTION.</span><span class="sxs-lookup"><span data-stu-id="bba50-142">Set the selection state by combining this flag with SELFLAG_ADDSELECTION or SELFLAG_REMOVESELECTION.</span></span> <br/> <span data-ttu-id="bba50-143">A menos que seja combinado com SELFLAG_TAKEFOCUS, esse sinalizador não altera o foco ou a âncora de seleção.</span><span class="sxs-lookup"><span data-stu-id="bba50-143">Unless it is combined with SELFLAG_TAKEFOCUS, this flag does not change the focus or the selection anchor.</span></span> <span data-ttu-id="bba50-144">O SELFLAG_EXTENDSELECTION | SELFLAG_TAKEFOCUS combinação é equivalente a adicionar um item a uma seleção manualmente, mantendo a tecla SHIFT pressionada e clicando em um objeto não selecionado no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="bba50-144">The SELFLAG_EXTENDSELECTION | SELFLAG_TAKEFOCUS combination is equivalent to adding an item to a selection manually by holding down the SHIFT key and clicking an unselected object in Windows Explorer.</span></span><br/> <span data-ttu-id="bba50-145">Esse sinalizador não é combinado com SELFLAG_TAKESELECTION.</span><span class="sxs-lookup"><span data-stu-id="bba50-145">This flag is not combined with SELFLAG_TAKESELECTION.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_ADDSELECTION"></span><span id="selflag_addselection"></span><dl> <span data-ttu-id="bba50-146"><dt><strong>SELFLAG_ADDSELECTION</strong></dt> <dt>0x8</dt> </span><span class="sxs-lookup"><span data-stu-id="bba50-146"><dt><strong>SELFLAG_ADDSELECTION</strong></dt> <dt>0x8</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bba50-147">Adiciona o objeto à seleção atual; o resultado possível é uma seleção não contígua.</span><span class="sxs-lookup"><span data-stu-id="bba50-147">Adds the object to the current selection; possible result is a noncontiguous selection.</span></span> <br/> <span data-ttu-id="bba50-148">A menos que seja combinado com SELFLAG_TAKEFOCUS, esse sinalizador não altera o foco ou a âncora de seleção.</span><span class="sxs-lookup"><span data-stu-id="bba50-148">Unless it is combined with SELFLAG_TAKEFOCUS, this flag does not change the focus or the selection anchor.</span></span> <span data-ttu-id="bba50-149">O SELFLAG_ADDSELECTION | SELFLAG_TAKEFOCUS combinação é equivalente a adicionar um item a uma seleção manualmente, mantendo a tecla CTRL pressionada e clicando em um objeto não selecionado no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="bba50-149">The SELFLAG_ADDSELECTION | SELFLAG_TAKEFOCUS combination is equivalent to adding an item to a selection manually by holding down the CTRL key and clicking an unselected object in Windows Explorer.</span></span><br/> <span data-ttu-id="bba50-150">Esse sinalizador não é combinado com SELFLAG_REMOVESELECTION ou SELFLAG_TAKESELECTION.</span><span class="sxs-lookup"><span data-stu-id="bba50-150">This flag is not combined with SELFLAG_REMOVESELECTION or SELFLAG_TAKESELECTION.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_REMOVESELECTION"></span><span id="selflag_removeselection"></span><dl> <span data-ttu-id="bba50-151"><dt><strong>SELFLAG_REMOVESELECTION</strong></dt> <dt>0x10</dt> </span><span class="sxs-lookup"><span data-stu-id="bba50-151"><dt><strong>SELFLAG_REMOVESELECTION</strong></dt> <dt>0x10</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="bba50-152">Remove o objeto da seleção atual; o resultado possível é uma seleção não contígua.</span><span class="sxs-lookup"><span data-stu-id="bba50-152">Removes the object from the current selection; possible result is a noncontiguous selection.</span></span> <br/> <span data-ttu-id="bba50-153">A menos que seja combinado com SELFLAG_TAKEFOCUS, esse sinalizador não altera o foco ou a âncora de seleção.</span><span class="sxs-lookup"><span data-stu-id="bba50-153">Unless it is combined with SELFLAG_TAKEFOCUS, this flag does not change the focus or the selection anchor.</span></span> <span data-ttu-id="bba50-154">O SELFLAG_REMOVESELECTION | SELFLAG_TAKEFOCUS combinação é equivalente a remover um item de uma seleção manualmente, mantendo a tecla CTRL pressionada ao clicar em um objeto selecionado no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="bba50-154">The SELFLAG_REMOVESELECTION | SELFLAG_TAKEFOCUS combination is equivalent to removing an item from a selection manually, by holding down the CTRL key while clicking a selected object in Windows Explorer.</span></span><br/> <span data-ttu-id="bba50-155">Esse sinalizador não é combinado com SELFLAG_ADDSELECTION ou SELFLAG_TAKESELECTION.</span><span class="sxs-lookup"><span data-stu-id="bba50-155">This flag is not combined with SELFLAG_ADDSELECTION or SELFLAG_TAKESELECTION.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="bba50-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bba50-156">Requirements</span></span>



| <span data-ttu-id="bba50-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="bba50-157">Requirement</span></span> | <span data-ttu-id="bba50-158">Valor</span><span class="sxs-lookup"><span data-stu-id="bba50-158">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bba50-159">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bba50-159">Header</span></span><br/> | <dl> <span data-ttu-id="bba50-160"><dt>OleAcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="bba50-160"><dt>Oleacc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bba50-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="bba50-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bba50-162">**IAccessible:: accSelect**</span><span class="sxs-lookup"><span data-stu-id="bba50-162">**IAccessible::accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)
</dt> <dt>

[<span data-ttu-id="bba50-163">Selecionando objetos filho</span><span class="sxs-lookup"><span data-stu-id="bba50-163">Selecting Child Objects</span></span>](selecting-child-objects.md)
</dt> </dl>

 

 





