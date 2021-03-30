---
title: Mensagem de EM_SETFONTSIZE (RichEdit. h)
description: Define o tamanho da fonte para o texto selecionado em um controle rich edit.
ms.assetid: 18d91370-12c0-4e5f-a0e9-ffde02abc966
keywords:
- Controles de EM_SETFONTSIZE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETFONTSIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eb75276acbb86cbd452a8ad97698f1cd7382bd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455184"
---
# <a name="em_setfontsize-message"></a><span data-ttu-id="635e1-104">\_Mensagem em SETfontize</span><span class="sxs-lookup"><span data-stu-id="635e1-104">EM\_SETFONTSIZE message</span></span>

<span data-ttu-id="635e1-105">Define o tamanho da fonte para o texto selecionado em um controle rich edit.</span><span class="sxs-lookup"><span data-stu-id="635e1-105">Sets the font size for the selected text in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="635e1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="635e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="635e1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="635e1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="635e1-108">Alteração no tamanho do ponto do texto selecionado.</span><span class="sxs-lookup"><span data-stu-id="635e1-108">Change in point size of the selected text.</span></span> <span data-ttu-id="635e1-109">O resultado será arredondado de acordo com os valores mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="635e1-109">The result will be rounded according to values shown in the following table.</span></span> <span data-ttu-id="635e1-110">Esse parâmetro deve estar no intervalo de-1637 a 1638.</span><span class="sxs-lookup"><span data-stu-id="635e1-110">This parameter should be in the range of -1637 to 1638.</span></span> <span data-ttu-id="635e1-111">O tamanho da fonte resultante estará dentro do intervalo de 1 a 1638.</span><span class="sxs-lookup"><span data-stu-id="635e1-111">The resulting font size will be within the range of 1 to 1638.</span></span>

</dd> <dt>

<span data-ttu-id="635e1-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="635e1-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="635e1-113">Esse parâmetro não é usado; Ele deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="635e1-113">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="635e1-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="635e1-114">Return value</span></span>

<span data-ttu-id="635e1-115">Se nenhum erro tiver ocorrido, o valor de retorno será **true**.</span><span class="sxs-lookup"><span data-stu-id="635e1-115">If no error occurred, the return value is **TRUE**.</span></span>

<span data-ttu-id="635e1-116">Se ocorrer um erro, o valor de retorno será **false**.</span><span class="sxs-lookup"><span data-stu-id="635e1-116">If an error occurred, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="635e1-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="635e1-117">Remarks</span></span>

<span data-ttu-id="635e1-118">Você pode obter facilmente o tamanho da fonte enviando a mensagem em [**\_ GETCHARFORMAT**](em-getcharformat.md) .</span><span class="sxs-lookup"><span data-stu-id="635e1-118">You can easily get the font size by sending the [**EM\_GETCHARFORMAT**](em-getcharformat.md) message.</span></span>

<span data-ttu-id="635e1-119">A edição avançada primeiro adiciona *wParam* ao tamanho da fonte atual e, em seguida, usa o tamanho resultante e a tabela a seguir para determinar o valor de arredondamento.</span><span class="sxs-lookup"><span data-stu-id="635e1-119">Rich Edit first adds *wParam* to the current font size and then uses the resulting size and the following table to determine the rounding value.</span></span>



| <span data-ttu-id="635e1-120">Banda</span><span class="sxs-lookup"><span data-stu-id="635e1-120">Band</span></span>    | <span data-ttu-id="635e1-121">Valor de arredondamento</span><span class="sxs-lookup"><span data-stu-id="635e1-121">Rounding value</span></span> |
|---------|----------------|
| <span data-ttu-id="635e1-122"><= 12</span><span class="sxs-lookup"><span data-stu-id="635e1-122"><=12</span></span> | <span data-ttu-id="635e1-123">1</span><span class="sxs-lookup"><span data-stu-id="635e1-123">1</span></span>              |
| <span data-ttu-id="635e1-124">28</span><span class="sxs-lookup"><span data-stu-id="635e1-124">28</span></span>      | <span data-ttu-id="635e1-125">2</span><span class="sxs-lookup"><span data-stu-id="635e1-125">2</span></span>              |
| <span data-ttu-id="635e1-126">36</span><span class="sxs-lookup"><span data-stu-id="635e1-126">36</span></span>      | <span data-ttu-id="635e1-127">0</span><span class="sxs-lookup"><span data-stu-id="635e1-127">0</span></span>              |
| <span data-ttu-id="635e1-128">48</span><span class="sxs-lookup"><span data-stu-id="635e1-128">48</span></span>      | <span data-ttu-id="635e1-129">0</span><span class="sxs-lookup"><span data-stu-id="635e1-129">0</span></span>              |
| <span data-ttu-id="635e1-130">72</span><span class="sxs-lookup"><span data-stu-id="635e1-130">72</span></span>      | <span data-ttu-id="635e1-131">0</span><span class="sxs-lookup"><span data-stu-id="635e1-131">0</span></span>              |
| <span data-ttu-id="635e1-132">80</span><span class="sxs-lookup"><span data-stu-id="635e1-132">80</span></span>      | <span data-ttu-id="635e1-133">0</span><span class="sxs-lookup"><span data-stu-id="635e1-133">0</span></span>              |
| <span data-ttu-id="635e1-134">> 80</span><span class="sxs-lookup"><span data-stu-id="635e1-134">> 80</span></span> | <span data-ttu-id="635e1-135">10</span><span class="sxs-lookup"><span data-stu-id="635e1-135">10</span></span>             |



 

<span data-ttu-id="635e1-136">Se o tamanho da fonte resultante não for divisível igualmente pelo valor de arredondamento, o tamanho da fonte será arredondado para um número igualmente divisível pelo valor de arredondamento.</span><span class="sxs-lookup"><span data-stu-id="635e1-136">If the resulting font size is not evenly divisible by the rounding value, the font size is then rounded to a number evenly divisible by the rounding value.</span></span> <span data-ttu-id="635e1-137">Portanto, se o tamanho da fonte for menor ou igual a 12, o valor de arredondamento será 1.</span><span class="sxs-lookup"><span data-stu-id="635e1-137">So if the font size is less than or equal to 12, the rounding value will be 1.</span></span> <span data-ttu-id="635e1-138">Da mesma forma, se o tamanho da fonte for menor ou igual a 28, o valor de arredondamento será 2.</span><span class="sxs-lookup"><span data-stu-id="635e1-138">Similarly, if the font size is less than or equal to 28, the rounding value is 2.</span></span> <span data-ttu-id="635e1-139">Para valores maiores que 28, os tamanhos de fonte são arredondados para a próxima faixa.</span><span class="sxs-lookup"><span data-stu-id="635e1-139">For values greater than 28, font sizes are rounded to the next band.</span></span> <span data-ttu-id="635e1-140">Portanto, o tamanho da fonte vai para 36, 48, 72, 80.</span><span class="sxs-lookup"><span data-stu-id="635e1-140">So, the font size jumps to 36, 48, 72, 80.</span></span> <span data-ttu-id="635e1-141">Após 80, todo o arredondamento é feito em incrementos de dez pontos.</span><span class="sxs-lookup"><span data-stu-id="635e1-141">After 80, all rounding is done in increments of ten points.</span></span>

<span data-ttu-id="635e1-142">O tamanho da fonte é arredondado para cima ou para baixo, dependendo do sinal de *wParam*.</span><span class="sxs-lookup"><span data-stu-id="635e1-142">The font size is rounded up or down depending on the sign of *wParam*.</span></span> <span data-ttu-id="635e1-143">Se *wParam* for positivo, o arredondamento estará sempre ativo.</span><span class="sxs-lookup"><span data-stu-id="635e1-143">If *wParam* is positive, the rounding is always up.</span></span> <span data-ttu-id="635e1-144">Caso contrário, o arredondamento estará sempre inoperante.</span><span class="sxs-lookup"><span data-stu-id="635e1-144">Otherwise, rounding is always down.</span></span> <span data-ttu-id="635e1-145">Portanto, se o tamanho da fonte atual for 10 e *wParam* for 3, o tamanho da fonte resultante será 14 (10 + 3 = 13, que não é divisível por 2, portanto, o tamanho será arredondado para até 14).</span><span class="sxs-lookup"><span data-stu-id="635e1-145">So, if the current font size is 10 and *wParam* is 3, the resulting font size would be 14 (10 + 3 = 13, which is not divisible by 2, so the size rounds up to 14).</span></span> <span data-ttu-id="635e1-146">Por outro lado, se o tamanho da fonte atual for 14 e *wParam* for-3, o tamanho da fonte resultante será 10 (14-3 = 11, que não é divisível por 2, portanto, o tamanho será arredondado para 10).</span><span class="sxs-lookup"><span data-stu-id="635e1-146">Conversely, if the current font size is 14 and *wParam* is -3, the resulting font size would be 10 (14 - 3 = 11, which is not divisible by 2, so the size rounds down to 10).</span></span>

<span data-ttu-id="635e1-147">A alteração é aplicada a cada parte da seleção.</span><span class="sxs-lookup"><span data-stu-id="635e1-147">The change is applied to each part of the selection.</span></span> <span data-ttu-id="635e1-148">Portanto, se algum texto for 10pt e algum 20pt, após uma chamada com *wParam* definido como 1, os tamanhos de fonte se tornarão 11pt e 22PT, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="635e1-148">So, if some of the text is 10pt and some 20pt, after a call with *wParam* set to 1, the font sizes become 11pt and 22pt, respectively.</span></span>

<span data-ttu-id="635e1-149">Exemplos adicionais são mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="635e1-149">Additional examples are shown in the following table.</span></span>



| <span data-ttu-id="635e1-150">Tamanho da fonte original</span><span class="sxs-lookup"><span data-stu-id="635e1-150">Original font size</span></span> | <span data-ttu-id="635e1-151">*wParam*</span><span class="sxs-lookup"><span data-stu-id="635e1-151">*wParam*</span></span> | <span data-ttu-id="635e1-152">Tamanho de fonte resultante</span><span class="sxs-lookup"><span data-stu-id="635e1-152">Resulting font size</span></span> |
|--------------------|----------|---------------------|
| <span data-ttu-id="635e1-153">7</span><span class="sxs-lookup"><span data-stu-id="635e1-153">7</span></span>                  | <span data-ttu-id="635e1-154">1</span><span class="sxs-lookup"><span data-stu-id="635e1-154">1</span></span>        | <span data-ttu-id="635e1-155">8</span><span class="sxs-lookup"><span data-stu-id="635e1-155">8</span></span>                   |
| <span data-ttu-id="635e1-156">7</span><span class="sxs-lookup"><span data-stu-id="635e1-156">7</span></span>                  | <span data-ttu-id="635e1-157">3</span><span class="sxs-lookup"><span data-stu-id="635e1-157">3</span></span>        | <span data-ttu-id="635e1-158">10</span><span class="sxs-lookup"><span data-stu-id="635e1-158">10</span></span>                  |
| <span data-ttu-id="635e1-159">10</span><span class="sxs-lookup"><span data-stu-id="635e1-159">10</span></span>                 | <span data-ttu-id="635e1-160">3</span><span class="sxs-lookup"><span data-stu-id="635e1-160">3</span></span>        | <span data-ttu-id="635e1-161">14</span><span class="sxs-lookup"><span data-stu-id="635e1-161">14</span></span>                  |
| <span data-ttu-id="635e1-162">14</span><span class="sxs-lookup"><span data-stu-id="635e1-162">14</span></span>                 | <span data-ttu-id="635e1-163">-3</span><span class="sxs-lookup"><span data-stu-id="635e1-163">-3</span></span>       | <span data-ttu-id="635e1-164">10</span><span class="sxs-lookup"><span data-stu-id="635e1-164">10</span></span>                  |
| <span data-ttu-id="635e1-165">28</span><span class="sxs-lookup"><span data-stu-id="635e1-165">28</span></span>                 | <span data-ttu-id="635e1-166">1</span><span class="sxs-lookup"><span data-stu-id="635e1-166">1</span></span>        | <span data-ttu-id="635e1-167">36</span><span class="sxs-lookup"><span data-stu-id="635e1-167">36</span></span>                  |
| <span data-ttu-id="635e1-168">28</span><span class="sxs-lookup"><span data-stu-id="635e1-168">28</span></span>                 | <span data-ttu-id="635e1-169">3</span><span class="sxs-lookup"><span data-stu-id="635e1-169">3</span></span>        | <span data-ttu-id="635e1-170">36</span><span class="sxs-lookup"><span data-stu-id="635e1-170">36</span></span>                  |
| <span data-ttu-id="635e1-171">80</span><span class="sxs-lookup"><span data-stu-id="635e1-171">80</span></span>                 | <span data-ttu-id="635e1-172">1</span><span class="sxs-lookup"><span data-stu-id="635e1-172">1</span></span>        | <span data-ttu-id="635e1-173">90</span><span class="sxs-lookup"><span data-stu-id="635e1-173">90</span></span>                  |
| <span data-ttu-id="635e1-174">80</span><span class="sxs-lookup"><span data-stu-id="635e1-174">80</span></span>                 | <span data-ttu-id="635e1-175">-1</span><span class="sxs-lookup"><span data-stu-id="635e1-175">-1</span></span>       | <span data-ttu-id="635e1-176">72</span><span class="sxs-lookup"><span data-stu-id="635e1-176">72</span></span>                  |



 

## <a name="requirements"></a><span data-ttu-id="635e1-177">Requisitos</span><span class="sxs-lookup"><span data-stu-id="635e1-177">Requirements</span></span>



| <span data-ttu-id="635e1-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="635e1-178">Requirement</span></span> | <span data-ttu-id="635e1-179">Valor</span><span class="sxs-lookup"><span data-stu-id="635e1-179">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="635e1-180">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="635e1-180">Minimum supported client</span></span><br/> | <span data-ttu-id="635e1-181">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="635e1-181">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="635e1-182">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="635e1-182">Minimum supported server</span></span><br/> | <span data-ttu-id="635e1-183">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="635e1-183">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="635e1-184">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="635e1-184">Redistributable</span></span><br/>          | <span data-ttu-id="635e1-185">Edição avançada 3,0</span><span class="sxs-lookup"><span data-stu-id="635e1-185">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="635e1-186">parâmetro</span><span class="sxs-lookup"><span data-stu-id="635e1-186">Header</span></span><br/>                   | <dl> <span data-ttu-id="635e1-187"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="635e1-187"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="635e1-188">Consulte também</span><span class="sxs-lookup"><span data-stu-id="635e1-188">See also</span></span>

<dl> <dt>

<span data-ttu-id="635e1-189">**Referência**</span><span class="sxs-lookup"><span data-stu-id="635e1-189">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="635e1-190">**em \_ GETCHARFORMAT**</span><span class="sxs-lookup"><span data-stu-id="635e1-190">**EM\_GETCHARFORMAT**</span></span>](em-getcharformat.md)
</dt> <dt>

[<span data-ttu-id="635e1-191">**CHARFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="635e1-191">**CHARFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> <dt>

<span data-ttu-id="635e1-192">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="635e1-192">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="635e1-193">Sobre os controles de edição avançados</span><span class="sxs-lookup"><span data-stu-id="635e1-193">About Rich Edit Controls</span></span>](about-rich-edit-controls.md)
</dt> </dl>

 

 





