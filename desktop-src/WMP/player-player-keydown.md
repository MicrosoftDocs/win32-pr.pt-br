---
title: Evento Player. KeyDown
description: O evento KeyDown ocorre quando uma tecla é pressionada. | Evento Player. KeyDown
ms.assetid: a34dafca-5db2-4065-bcfe-d66e633b26fb
keywords:
- Evento KeyDown Windows Media Player
- Evento KeyDown Windows Media Player, classe Player
- Classe Player Windows Media Player, evento KeyDown
topic_type:
- apiref
api_name:
- Player.KeyDown
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 226430421977a58eca02b7a42cf0349f2a5ff520
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811093"
---
# <a name="playerkeydown-event"></a><span data-ttu-id="d1633-107">Evento Player. KeyDown</span><span class="sxs-lookup"><span data-stu-id="d1633-107">Player.KeyDown event</span></span>

<span data-ttu-id="d1633-108">O evento **KeyDown** ocorre quando uma tecla é pressionada.</span><span class="sxs-lookup"><span data-stu-id="d1633-108">The **KeyDown** event occurs when a key is pressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1633-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1633-109">Syntax</span></span>


```JScript
Player.KeyDown(
  nKeyCode,
  nShiftState
)
```



## <a name="parameters"></a><span data-ttu-id="d1633-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1633-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1633-111">*nKeyCode*</span><span class="sxs-lookup"><span data-stu-id="d1633-111">*nKeyCode*</span></span> 
</dt> <dd>

<span data-ttu-id="d1633-112">**Número** (**int**) que especifica qual chave física é pressionada.</span><span class="sxs-lookup"><span data-stu-id="d1633-112">**Number** (**int**) specifying which physical key is pressed.</span></span> <span data-ttu-id="d1633-113">Para obter os valores possíveis, consulte a seção comentários.</span><span class="sxs-lookup"><span data-stu-id="d1633-113">For possible values, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="d1633-114">*nShiftState*</span><span class="sxs-lookup"><span data-stu-id="d1633-114">*nShiftState*</span></span> 
</dt> <dd>

<span data-ttu-id="d1633-115">**Número** (**int**) especificando um campo de bits com os menos significativos que correspondem à tecla Shift (bit 0), a tecla Ctrl (bit 1) e a tecla Alt (bit 2).</span><span class="sxs-lookup"><span data-stu-id="d1633-115">**Number** (**int**) specifying a bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="d1633-116">Esses bits correspondem aos valores 1, 2 e 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d1633-116">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="d1633-117">O argumento Shift indica o estado dessas chaves.</span><span class="sxs-lookup"><span data-stu-id="d1633-117">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="d1633-118">Alguns, todos ou nenhum dos bits podem ser definidos, indicando que algumas, todas ou nenhuma das chaves são pressionadas.</span><span class="sxs-lookup"><span data-stu-id="d1633-118">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1633-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d1633-119">Return value</span></span>

<span data-ttu-id="d1633-120">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d1633-120">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1633-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1633-121">Remarks</span></span>

<span data-ttu-id="d1633-122">O argumento *nKeyCode* especifica uma chave física.</span><span class="sxs-lookup"><span data-stu-id="d1633-122">The *nKeyCode* argument specifies a physical key.</span></span> <span data-ttu-id="d1633-123">As tabelas a seguir mostram os valores possíveis para as chaves principais em um teclado padrão.</span><span class="sxs-lookup"><span data-stu-id="d1633-123">The following tables show the possible values for the major keys on a standard keyboard.</span></span>

<span data-ttu-id="d1633-124">Valores para as chaves principais.</span><span class="sxs-lookup"><span data-stu-id="d1633-124">Values for the main keys.</span></span>



| <span data-ttu-id="d1633-125">Chave</span><span class="sxs-lookup"><span data-stu-id="d1633-125">Key</span></span>                     | <span data-ttu-id="d1633-126">Valor</span><span class="sxs-lookup"><span data-stu-id="d1633-126">Value</span></span>   |
|-------------------------|---------|
| <span data-ttu-id="d1633-127">A-Z</span><span class="sxs-lookup"><span data-stu-id="d1633-127">A-Z</span></span>                     | <span data-ttu-id="d1633-128">65-90</span><span class="sxs-lookup"><span data-stu-id="d1633-128">65-90</span></span>   |
| <span data-ttu-id="d1633-129">0-9</span><span class="sxs-lookup"><span data-stu-id="d1633-129">0-9</span></span>                     | <span data-ttu-id="d1633-130">48-56</span><span class="sxs-lookup"><span data-stu-id="d1633-130">48-56</span></span>   |
| <span data-ttu-id="d1633-131">F1-F12</span><span class="sxs-lookup"><span data-stu-id="d1633-131">F1-F12</span></span>                  | <span data-ttu-id="d1633-132">112-123</span><span class="sxs-lookup"><span data-stu-id="d1633-132">112-123</span></span> |
| <span data-ttu-id="d1633-133">ESC</span><span class="sxs-lookup"><span data-stu-id="d1633-133">ESC</span></span>                     | <span data-ttu-id="d1633-134">27</span><span class="sxs-lookup"><span data-stu-id="d1633-134">27</span></span>      |
| <span data-ttu-id="d1633-135">TAB</span><span class="sxs-lookup"><span data-stu-id="d1633-135">TAB</span></span>                     | <span data-ttu-id="d1633-136">9</span><span class="sxs-lookup"><span data-stu-id="d1633-136">9</span></span>       |
| <span data-ttu-id="d1633-137">CAPS LOCK</span><span class="sxs-lookup"><span data-stu-id="d1633-137">CAPS LOCK</span></span>               | <span data-ttu-id="d1633-138">20</span><span class="sxs-lookup"><span data-stu-id="d1633-138">20</span></span>      |
| <span data-ttu-id="d1633-139">SHIFT (esquerda ou direita)</span><span class="sxs-lookup"><span data-stu-id="d1633-139">SHIFT (left or right)</span></span>   | <span data-ttu-id="d1633-140">16</span><span class="sxs-lookup"><span data-stu-id="d1633-140">16</span></span>      |
| <span data-ttu-id="d1633-141">CTRL (esquerda ou direita)</span><span class="sxs-lookup"><span data-stu-id="d1633-141">CTRL (left or right)</span></span>    | <span data-ttu-id="d1633-142">17</span><span class="sxs-lookup"><span data-stu-id="d1633-142">17</span></span>      |
| <span data-ttu-id="d1633-143">ALT (esquerda ou direita)</span><span class="sxs-lookup"><span data-stu-id="d1633-143">ALT (left or right)</span></span>     | <span data-ttu-id="d1633-144">18</span><span class="sxs-lookup"><span data-stu-id="d1633-144">18</span></span>      |
| <span data-ttu-id="d1633-145">SPACE</span><span class="sxs-lookup"><span data-stu-id="d1633-145">SPACE</span></span>                   | <span data-ttu-id="d1633-146">32</span><span class="sxs-lookup"><span data-stu-id="d1633-146">32</span></span>      |
| <span data-ttu-id="d1633-147">BACKSPACE</span><span class="sxs-lookup"><span data-stu-id="d1633-147">BACKSPACE</span></span>               | <span data-ttu-id="d1633-148">8</span><span class="sxs-lookup"><span data-stu-id="d1633-148">8</span></span>       |
| <span data-ttu-id="d1633-149">Enter</span><span class="sxs-lookup"><span data-stu-id="d1633-149">ENTER</span></span>                   | <span data-ttu-id="d1633-150">13</span><span class="sxs-lookup"><span data-stu-id="d1633-150">13</span></span>      |
| <span data-ttu-id="d1633-151">Tecla com o logotipo do Windows, esquerda</span><span class="sxs-lookup"><span data-stu-id="d1633-151">Windows logo key, left</span></span>  | <span data-ttu-id="d1633-152">91</span><span class="sxs-lookup"><span data-stu-id="d1633-152">91</span></span>      |
| <span data-ttu-id="d1633-153">Tecla com o logotipo do Windows, direita</span><span class="sxs-lookup"><span data-stu-id="d1633-153">Windows logo key, right</span></span> | <span data-ttu-id="d1633-154">92</span><span class="sxs-lookup"><span data-stu-id="d1633-154">92</span></span>      |
| <span data-ttu-id="d1633-155">Chave do aplicativo</span><span class="sxs-lookup"><span data-stu-id="d1633-155">Application key</span></span>         | <span data-ttu-id="d1633-156">93</span><span class="sxs-lookup"><span data-stu-id="d1633-156">93</span></span>      |



 

<span data-ttu-id="d1633-157">Valores para as chaves do teclado numérico.</span><span class="sxs-lookup"><span data-stu-id="d1633-157">Values for the number pad keys.</span></span>



| <span data-ttu-id="d1633-158">Chave</span><span class="sxs-lookup"><span data-stu-id="d1633-158">Key</span></span>               | <span data-ttu-id="d1633-159">Valor</span><span class="sxs-lookup"><span data-stu-id="d1633-159">Value</span></span>  |
|-------------------|--------|
| <span data-ttu-id="d1633-160">0-9</span><span class="sxs-lookup"><span data-stu-id="d1633-160">0-9</span></span>               | <span data-ttu-id="d1633-161">96-105</span><span class="sxs-lookup"><span data-stu-id="d1633-161">96-105</span></span> |
| <span data-ttu-id="d1633-162">NUM LOCK</span><span class="sxs-lookup"><span data-stu-id="d1633-162">NUM LOCK</span></span>          | <span data-ttu-id="d1633-163">144</span><span class="sxs-lookup"><span data-stu-id="d1633-163">144</span></span>    |
| <span data-ttu-id="d1633-164">DIVIDIR (/)</span><span class="sxs-lookup"><span data-stu-id="d1633-164">DIVIDE (/)</span></span>        | <span data-ttu-id="d1633-165">111</span><span class="sxs-lookup"><span data-stu-id="d1633-165">111</span></span>    |
| <span data-ttu-id="d1633-166">MULTIPLICAr ( \* )</span><span class="sxs-lookup"><span data-stu-id="d1633-166">MULTIPLY (\*)</span></span>     | <span data-ttu-id="d1633-167">106</span><span class="sxs-lookup"><span data-stu-id="d1633-167">106</span></span>    |
| <span data-ttu-id="d1633-168">Subtrair (-)</span><span class="sxs-lookup"><span data-stu-id="d1633-168">SUBTRACT (-)</span></span>      | <span data-ttu-id="d1633-169">109</span><span class="sxs-lookup"><span data-stu-id="d1633-169">109</span></span>    |
| <span data-ttu-id="d1633-170">ADICIONAR (+)</span><span class="sxs-lookup"><span data-stu-id="d1633-170">ADD (+)</span></span>           | <span data-ttu-id="d1633-171">107</span><span class="sxs-lookup"><span data-stu-id="d1633-171">107</span></span>    |
| <span data-ttu-id="d1633-172">Separador (Enter)</span><span class="sxs-lookup"><span data-stu-id="d1633-172">SEPARATOR (Enter)</span></span> | <span data-ttu-id="d1633-173">108</span><span class="sxs-lookup"><span data-stu-id="d1633-173">108</span></span>    |
| <span data-ttu-id="d1633-174">DECIMAL (.)</span><span class="sxs-lookup"><span data-stu-id="d1633-174">DECIMAL (.)</span></span>       | <span data-ttu-id="d1633-175">110</span><span class="sxs-lookup"><span data-stu-id="d1633-175">110</span></span>    |



 

<span data-ttu-id="d1633-176">Valores para as chaves de navegação.</span><span class="sxs-lookup"><span data-stu-id="d1633-176">Values for the navigation keys.</span></span>



| <span data-ttu-id="d1633-177">Chave</span><span class="sxs-lookup"><span data-stu-id="d1633-177">Key</span></span>         | <span data-ttu-id="d1633-178">Valor</span><span class="sxs-lookup"><span data-stu-id="d1633-178">Value</span></span> |
|-------------|-------|
| <span data-ttu-id="d1633-179">INSERT</span><span class="sxs-lookup"><span data-stu-id="d1633-179">INSERT</span></span>      | <span data-ttu-id="d1633-180">45</span><span class="sxs-lookup"><span data-stu-id="d1633-180">45</span></span>    |
| <span data-ttu-id="d1633-181">Delete (excluir)</span><span class="sxs-lookup"><span data-stu-id="d1633-181">DELETE</span></span>      | <span data-ttu-id="d1633-182">46</span><span class="sxs-lookup"><span data-stu-id="d1633-182">46</span></span>    |
| <span data-ttu-id="d1633-183">HOME</span><span class="sxs-lookup"><span data-stu-id="d1633-183">HOME</span></span>        | <span data-ttu-id="d1633-184">36</span><span class="sxs-lookup"><span data-stu-id="d1633-184">36</span></span>    |
| <span data-ttu-id="d1633-185">END</span><span class="sxs-lookup"><span data-stu-id="d1633-185">END</span></span>         | <span data-ttu-id="d1633-186">35</span><span class="sxs-lookup"><span data-stu-id="d1633-186">35</span></span>    |
| <span data-ttu-id="d1633-187">PAGE UP</span><span class="sxs-lookup"><span data-stu-id="d1633-187">PAGE UP</span></span>     | <span data-ttu-id="d1633-188">33</span><span class="sxs-lookup"><span data-stu-id="d1633-188">33</span></span>    |
| <span data-ttu-id="d1633-189">PAGE DOWN</span><span class="sxs-lookup"><span data-stu-id="d1633-189">PAGE DOWN</span></span>   | <span data-ttu-id="d1633-190">34</span><span class="sxs-lookup"><span data-stu-id="d1633-190">34</span></span>    |
| <span data-ttu-id="d1633-191">SETA PARA CIMA</span><span class="sxs-lookup"><span data-stu-id="d1633-191">UP ARROW</span></span>    | <span data-ttu-id="d1633-192">38</span><span class="sxs-lookup"><span data-stu-id="d1633-192">38</span></span>    |
| <span data-ttu-id="d1633-193">SETA PARA BAIXO</span><span class="sxs-lookup"><span data-stu-id="d1633-193">DOWN ARROW</span></span>  | <span data-ttu-id="d1633-194">40</span><span class="sxs-lookup"><span data-stu-id="d1633-194">40</span></span>    |
| <span data-ttu-id="d1633-195">SETA PARA A ESQUERDA</span><span class="sxs-lookup"><span data-stu-id="d1633-195">LEFT ARROW</span></span>  | <span data-ttu-id="d1633-196">37</span><span class="sxs-lookup"><span data-stu-id="d1633-196">37</span></span>    |
| <span data-ttu-id="d1633-197">SETA PARA A DIREITA</span><span class="sxs-lookup"><span data-stu-id="d1633-197">RIGHT ARROW</span></span> | <span data-ttu-id="d1633-198">39</span><span class="sxs-lookup"><span data-stu-id="d1633-198">39</span></span>    |



 

<span data-ttu-id="d1633-199">O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido.</span><span class="sxs-lookup"><span data-stu-id="d1633-199">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="d1633-200">Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.</span><span class="sxs-lookup"><span data-stu-id="d1633-200">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="d1633-201">**Windows Media Player 10 Mobile:** Não há suporte para esse evento.</span><span class="sxs-lookup"><span data-stu-id="d1633-201">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1633-202">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1633-202">Requirements</span></span>



| <span data-ttu-id="d1633-203">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1633-203">Requirement</span></span> | <span data-ttu-id="d1633-204">Valor</span><span class="sxs-lookup"><span data-stu-id="d1633-204">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d1633-205">Versão</span><span class="sxs-lookup"><span data-stu-id="d1633-205">Version</span></span><br/> | <span data-ttu-id="d1633-206">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="d1633-206">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="d1633-207">DLL</span><span class="sxs-lookup"><span data-stu-id="d1633-207">DLL</span></span><br/>     | <dl> <span data-ttu-id="d1633-208"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1633-208"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1633-209">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1633-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1633-210">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="d1633-210">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





