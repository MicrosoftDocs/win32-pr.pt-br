---
title: Evento KeyDown do objeto AxWindowsMediaPlayer
description: O evento KeyDown ocorre quando uma tecla é pressionada. | Evento KeyDown do objeto AxWindowsMediaPlayer
ms.assetid: e67b9628-6c53-4893-921a-9487ebfc1cd5
keywords:
- Evento KeyDown do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- KeyDown Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc89814063e1a43badd22e658b5f19ece7abb074
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796445"
---
# <a name="keydown-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="149fd-105">Evento KeyDown do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="149fd-105">KeyDown Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="149fd-106">O evento KeyDown ocorre quando uma tecla é pressionada.</span><span class="sxs-lookup"><span data-stu-id="149fd-106">The KeyDown event occurs when a key is pressed.</span></span>

``` syntax
[C#]
private void player_KeyDownEvent(
  object sender,
  _WMPOCXEvents_KeyDownEvent e
)

[Visual Basic]
Private Sub player_KeyDownEvent(  
  sender As Object, 
  e As _WMPOCXEvents_KeyDownEvent
) Handles player.KeyDownEvent
```

## <a name="event-data"></a><span data-ttu-id="149fd-107">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="149fd-107">Event Data</span></span>

<span data-ttu-id="149fd-108">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ KeyDownEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="149fd-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_KeyDownEventHandler**.</span></span> <span data-ttu-id="149fd-109">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ KeyDownEvent**, que contém as propriedades a seguir relacionadas a esse evento.</span><span class="sxs-lookup"><span data-stu-id="149fd-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_KeyDownEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="149fd-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="149fd-110">Property</span></span>    | <span data-ttu-id="149fd-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="149fd-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="149fd-112">nKeyCode</span><span class="sxs-lookup"><span data-stu-id="149fd-112">nKeyCode</span></span>    | <span data-ttu-id="149fd-113">System. Int16Specifies que a chave física é pressionada.</span><span class="sxs-lookup"><span data-stu-id="149fd-113">System.Int16Specifies which physical key is pressed.</span></span> <span data-ttu-id="149fd-114">Para obter os valores possíveis, consulte comentários.</span><span class="sxs-lookup"><span data-stu-id="149fd-114">For possible values, see Remarks.</span></span><br/>                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="149fd-115">nShiftState</span><span class="sxs-lookup"><span data-stu-id="149fd-115">nShiftState</span></span> | <span data-ttu-id="149fd-116">O campo do sistema. Int16a com os bits menos significativos correspondentes à tecla SHIFT (bit 0), a tecla CTRL (bit 1) e a tecla ALT (bit 2).</span><span class="sxs-lookup"><span data-stu-id="149fd-116">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="149fd-117">Esses bits correspondem aos valores 1, 2 e 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="149fd-117">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="149fd-118">O argumento Shift indica o estado dessas chaves.</span><span class="sxs-lookup"><span data-stu-id="149fd-118">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="149fd-119">Alguns, todos ou nenhum dos bits podem ser definidos, indicando que algumas, todas ou nenhuma das chaves são pressionadas.</span><span class="sxs-lookup"><span data-stu-id="149fd-119">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="149fd-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="149fd-120">Remarks</span></span>

<span data-ttu-id="149fd-121">A propriedade **nKeyCode** especifica uma chave física.</span><span class="sxs-lookup"><span data-stu-id="149fd-121">The **nKeyCode** property specifies a physical key.</span></span> <span data-ttu-id="149fd-122">As tabelas a seguir mostram os valores possíveis para as chaves principais em um teclado padrão.</span><span class="sxs-lookup"><span data-stu-id="149fd-122">The following tables show the possible values for the major keys on a standard keyboard.</span></span>

<span data-ttu-id="149fd-123">Valores para as chaves principais.</span><span class="sxs-lookup"><span data-stu-id="149fd-123">Values for the main keys.</span></span>



| <span data-ttu-id="149fd-124">Chave</span><span class="sxs-lookup"><span data-stu-id="149fd-124">Key</span></span>                     | <span data-ttu-id="149fd-125">Valor</span><span class="sxs-lookup"><span data-stu-id="149fd-125">Value</span></span>   |
|-------------------------|---------|
| <span data-ttu-id="149fd-126">A-Z</span><span class="sxs-lookup"><span data-stu-id="149fd-126">A-Z</span></span>                     | <span data-ttu-id="149fd-127">65-90</span><span class="sxs-lookup"><span data-stu-id="149fd-127">65-90</span></span>   |
| <span data-ttu-id="149fd-128">0-9</span><span class="sxs-lookup"><span data-stu-id="149fd-128">0-9</span></span>                     | <span data-ttu-id="149fd-129">48-56</span><span class="sxs-lookup"><span data-stu-id="149fd-129">48-56</span></span>   |
| <span data-ttu-id="149fd-130">F1-F12</span><span class="sxs-lookup"><span data-stu-id="149fd-130">F1-F12</span></span>                  | <span data-ttu-id="149fd-131">112-123</span><span class="sxs-lookup"><span data-stu-id="149fd-131">112-123</span></span> |
| <span data-ttu-id="149fd-132">ESC</span><span class="sxs-lookup"><span data-stu-id="149fd-132">ESC</span></span>                     | <span data-ttu-id="149fd-133">27</span><span class="sxs-lookup"><span data-stu-id="149fd-133">27</span></span>      |
| <span data-ttu-id="149fd-134">TAB</span><span class="sxs-lookup"><span data-stu-id="149fd-134">TAB</span></span>                     | <span data-ttu-id="149fd-135">9</span><span class="sxs-lookup"><span data-stu-id="149fd-135">9</span></span>       |
| <span data-ttu-id="149fd-136">CAPS LOCK</span><span class="sxs-lookup"><span data-stu-id="149fd-136">CAPS LOCK</span></span>               | <span data-ttu-id="149fd-137">20</span><span class="sxs-lookup"><span data-stu-id="149fd-137">20</span></span>      |
| <span data-ttu-id="149fd-138">SHIFT (esquerda ou direita)</span><span class="sxs-lookup"><span data-stu-id="149fd-138">SHIFT (left or right)</span></span>   | <span data-ttu-id="149fd-139">16</span><span class="sxs-lookup"><span data-stu-id="149fd-139">16</span></span>      |
| <span data-ttu-id="149fd-140">CTRL (esquerda ou direita)</span><span class="sxs-lookup"><span data-stu-id="149fd-140">CTRL (left or right)</span></span>    | <span data-ttu-id="149fd-141">17</span><span class="sxs-lookup"><span data-stu-id="149fd-141">17</span></span>      |
| <span data-ttu-id="149fd-142">ALT (esquerda ou direita)</span><span class="sxs-lookup"><span data-stu-id="149fd-142">ALT (left or right)</span></span>     | <span data-ttu-id="149fd-143">18</span><span class="sxs-lookup"><span data-stu-id="149fd-143">18</span></span>      |
| <span data-ttu-id="149fd-144">SPACE</span><span class="sxs-lookup"><span data-stu-id="149fd-144">SPACE</span></span>                   | <span data-ttu-id="149fd-145">32</span><span class="sxs-lookup"><span data-stu-id="149fd-145">32</span></span>      |
| <span data-ttu-id="149fd-146">BACKSPACE</span><span class="sxs-lookup"><span data-stu-id="149fd-146">BACKSPACE</span></span>               | <span data-ttu-id="149fd-147">8</span><span class="sxs-lookup"><span data-stu-id="149fd-147">8</span></span>       |
| <span data-ttu-id="149fd-148">Enter</span><span class="sxs-lookup"><span data-stu-id="149fd-148">ENTER</span></span>                   | <span data-ttu-id="149fd-149">13</span><span class="sxs-lookup"><span data-stu-id="149fd-149">13</span></span>      |
| <span data-ttu-id="149fd-150">Tecla com o logotipo do Windows, esquerda</span><span class="sxs-lookup"><span data-stu-id="149fd-150">Windows logo key, left</span></span>  | <span data-ttu-id="149fd-151">91</span><span class="sxs-lookup"><span data-stu-id="149fd-151">91</span></span>      |
| <span data-ttu-id="149fd-152">Tecla com o logotipo do Windows, direita</span><span class="sxs-lookup"><span data-stu-id="149fd-152">Windows logo key, right</span></span> | <span data-ttu-id="149fd-153">92</span><span class="sxs-lookup"><span data-stu-id="149fd-153">92</span></span>      |
| <span data-ttu-id="149fd-154">Chave do aplicativo</span><span class="sxs-lookup"><span data-stu-id="149fd-154">Application key</span></span>         | <span data-ttu-id="149fd-155">93</span><span class="sxs-lookup"><span data-stu-id="149fd-155">93</span></span>      |



 

<span data-ttu-id="149fd-156">Valores para as chaves do teclado numérico.</span><span class="sxs-lookup"><span data-stu-id="149fd-156">Values for the number pad keys.</span></span>



| <span data-ttu-id="149fd-157">Chave</span><span class="sxs-lookup"><span data-stu-id="149fd-157">Key</span></span>               | <span data-ttu-id="149fd-158">Valor</span><span class="sxs-lookup"><span data-stu-id="149fd-158">Value</span></span>  |
|-------------------|--------|
| <span data-ttu-id="149fd-159">0-9</span><span class="sxs-lookup"><span data-stu-id="149fd-159">0-9</span></span>               | <span data-ttu-id="149fd-160">96-105</span><span class="sxs-lookup"><span data-stu-id="149fd-160">96-105</span></span> |
| <span data-ttu-id="149fd-161">NUM LOCK</span><span class="sxs-lookup"><span data-stu-id="149fd-161">NUM LOCK</span></span>          | <span data-ttu-id="149fd-162">144</span><span class="sxs-lookup"><span data-stu-id="149fd-162">144</span></span>    |
| <span data-ttu-id="149fd-163">DIVIDIR (/)</span><span class="sxs-lookup"><span data-stu-id="149fd-163">DIVIDE (/)</span></span>        | <span data-ttu-id="149fd-164">111</span><span class="sxs-lookup"><span data-stu-id="149fd-164">111</span></span>    |
| <span data-ttu-id="149fd-165">MULTIPLICAr ( \* )</span><span class="sxs-lookup"><span data-stu-id="149fd-165">MULTIPLY (\*)</span></span>     | <span data-ttu-id="149fd-166">106</span><span class="sxs-lookup"><span data-stu-id="149fd-166">106</span></span>    |
| <span data-ttu-id="149fd-167">Subtrair (-)</span><span class="sxs-lookup"><span data-stu-id="149fd-167">SUBTRACT (-)</span></span>      | <span data-ttu-id="149fd-168">109</span><span class="sxs-lookup"><span data-stu-id="149fd-168">109</span></span>    |
| <span data-ttu-id="149fd-169">ADICIONAR (+)</span><span class="sxs-lookup"><span data-stu-id="149fd-169">ADD (+)</span></span>           | <span data-ttu-id="149fd-170">107</span><span class="sxs-lookup"><span data-stu-id="149fd-170">107</span></span>    |
| <span data-ttu-id="149fd-171">Separador (Enter)</span><span class="sxs-lookup"><span data-stu-id="149fd-171">SEPARATOR (Enter)</span></span> | <span data-ttu-id="149fd-172">108</span><span class="sxs-lookup"><span data-stu-id="149fd-172">108</span></span>    |
| <span data-ttu-id="149fd-173">DECIMAL (.)</span><span class="sxs-lookup"><span data-stu-id="149fd-173">DECIMAL (.)</span></span>       | <span data-ttu-id="149fd-174">110</span><span class="sxs-lookup"><span data-stu-id="149fd-174">110</span></span>    |



 

<span data-ttu-id="149fd-175">Valores para as chaves de navegação.</span><span class="sxs-lookup"><span data-stu-id="149fd-175">Values for the navigation keys.</span></span>



| <span data-ttu-id="149fd-176">Chave</span><span class="sxs-lookup"><span data-stu-id="149fd-176">Key</span></span>         | <span data-ttu-id="149fd-177">Valor</span><span class="sxs-lookup"><span data-stu-id="149fd-177">Value</span></span> |
|-------------|-------|
| <span data-ttu-id="149fd-178">INSERT</span><span class="sxs-lookup"><span data-stu-id="149fd-178">INSERT</span></span>      | <span data-ttu-id="149fd-179">45</span><span class="sxs-lookup"><span data-stu-id="149fd-179">45</span></span>    |
| <span data-ttu-id="149fd-180">Delete (excluir)</span><span class="sxs-lookup"><span data-stu-id="149fd-180">DELETE</span></span>      | <span data-ttu-id="149fd-181">46</span><span class="sxs-lookup"><span data-stu-id="149fd-181">46</span></span>    |
| <span data-ttu-id="149fd-182">HOME</span><span class="sxs-lookup"><span data-stu-id="149fd-182">HOME</span></span>        | <span data-ttu-id="149fd-183">36</span><span class="sxs-lookup"><span data-stu-id="149fd-183">36</span></span>    |
| <span data-ttu-id="149fd-184">END</span><span class="sxs-lookup"><span data-stu-id="149fd-184">END</span></span>         | <span data-ttu-id="149fd-185">35</span><span class="sxs-lookup"><span data-stu-id="149fd-185">35</span></span>    |
| <span data-ttu-id="149fd-186">PAGE UP</span><span class="sxs-lookup"><span data-stu-id="149fd-186">PAGE UP</span></span>     | <span data-ttu-id="149fd-187">33</span><span class="sxs-lookup"><span data-stu-id="149fd-187">33</span></span>    |
| <span data-ttu-id="149fd-188">PAGE DOWN</span><span class="sxs-lookup"><span data-stu-id="149fd-188">PAGE DOWN</span></span>   | <span data-ttu-id="149fd-189">34</span><span class="sxs-lookup"><span data-stu-id="149fd-189">34</span></span>    |
| <span data-ttu-id="149fd-190">SETA PARA CIMA</span><span class="sxs-lookup"><span data-stu-id="149fd-190">UP ARROW</span></span>    | <span data-ttu-id="149fd-191">38</span><span class="sxs-lookup"><span data-stu-id="149fd-191">38</span></span>    |
| <span data-ttu-id="149fd-192">SETA PARA BAIXO</span><span class="sxs-lookup"><span data-stu-id="149fd-192">DOWN ARROW</span></span>  | <span data-ttu-id="149fd-193">40</span><span class="sxs-lookup"><span data-stu-id="149fd-193">40</span></span>    |
| <span data-ttu-id="149fd-194">SETA PARA A ESQUERDA</span><span class="sxs-lookup"><span data-stu-id="149fd-194">LEFT ARROW</span></span>  | <span data-ttu-id="149fd-195">37</span><span class="sxs-lookup"><span data-stu-id="149fd-195">37</span></span>    |
| <span data-ttu-id="149fd-196">SETA PARA A DIREITA</span><span class="sxs-lookup"><span data-stu-id="149fd-196">RIGHT ARROW</span></span> | <span data-ttu-id="149fd-197">39</span><span class="sxs-lookup"><span data-stu-id="149fd-197">39</span></span>    |



 

## <a name="requirements"></a><span data-ttu-id="149fd-198">Requisitos</span><span class="sxs-lookup"><span data-stu-id="149fd-198">Requirements</span></span>



| <span data-ttu-id="149fd-199">Requisito</span><span class="sxs-lookup"><span data-stu-id="149fd-199">Requirement</span></span> | <span data-ttu-id="149fd-200">Valor</span><span class="sxs-lookup"><span data-stu-id="149fd-200">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="149fd-201">Versão</span><span class="sxs-lookup"><span data-stu-id="149fd-201">Version</span></span><br/>   | <span data-ttu-id="149fd-202">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="149fd-202">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="149fd-203">Namespace</span><span class="sxs-lookup"><span data-stu-id="149fd-203">Namespace</span></span><br/> | <span data-ttu-id="149fd-204">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="149fd-204">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="149fd-205">Assembly</span><span class="sxs-lookup"><span data-stu-id="149fd-205">Assembly</span></span><br/>  | <dl> <span data-ttu-id="149fd-206"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="149fd-206"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="149fd-207">Confira também</span><span class="sxs-lookup"><span data-stu-id="149fd-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="149fd-208">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="149fd-208">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





