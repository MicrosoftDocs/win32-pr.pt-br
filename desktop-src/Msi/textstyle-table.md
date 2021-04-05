---
description: A tabela TextStyle lista diferentes estilos de fonte usados em controles com texto.
ms.assetid: a351e67a-8f51-41bf-9202-56488b870fa7
title: Tabela TextStyle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c9993362228e37f01c0e53683755f7bd1310eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921053"
---
# <a name="textstyle-table"></a><span data-ttu-id="6f703-103">Tabela TextStyle</span><span class="sxs-lookup"><span data-stu-id="6f703-103">TextStyle Table</span></span>

<span data-ttu-id="6f703-104">A tabela TextStyle lista diferentes estilos de fonte usados em controles com texto.</span><span class="sxs-lookup"><span data-stu-id="6f703-104">The TextStyle table lists different font styles used in controls having text.</span></span>

<span data-ttu-id="6f703-105">A tabela TextStyle tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="6f703-105">The TextStyle table has the following columns.</span></span>



| <span data-ttu-id="6f703-106">Coluna</span><span class="sxs-lookup"><span data-stu-id="6f703-106">Column</span></span>    | <span data-ttu-id="6f703-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="6f703-107">Type</span></span>                               | <span data-ttu-id="6f703-108">Chave</span><span class="sxs-lookup"><span data-stu-id="6f703-108">Key</span></span> | <span data-ttu-id="6f703-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="6f703-109">Nullable</span></span> |
|-----------|------------------------------------|-----|----------|
| <span data-ttu-id="6f703-110">Estilo]</span><span class="sxs-lookup"><span data-stu-id="6f703-110">TextStyle</span></span> | [<span data-ttu-id="6f703-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="6f703-111">Identifier</span></span>](identifier.md)       | <span data-ttu-id="6f703-112">S</span><span class="sxs-lookup"><span data-stu-id="6f703-112">Y</span></span>   | <span data-ttu-id="6f703-113">N</span><span class="sxs-lookup"><span data-stu-id="6f703-113">N</span></span>        |
| <span data-ttu-id="6f703-114">FaceName</span><span class="sxs-lookup"><span data-stu-id="6f703-114">FaceName</span></span>  | [<span data-ttu-id="6f703-115">Text</span><span class="sxs-lookup"><span data-stu-id="6f703-115">Text</span></span>](text.md)                   | <span data-ttu-id="6f703-116">N</span><span class="sxs-lookup"><span data-stu-id="6f703-116">N</span></span>   | <span data-ttu-id="6f703-117">N</span><span class="sxs-lookup"><span data-stu-id="6f703-117">N</span></span>        |
| <span data-ttu-id="6f703-118">Tamanho</span><span class="sxs-lookup"><span data-stu-id="6f703-118">Size</span></span>      | [<span data-ttu-id="6f703-119">Inteiro</span><span class="sxs-lookup"><span data-stu-id="6f703-119">Integer</span></span>](integer.md)             | <span data-ttu-id="6f703-120">N</span><span class="sxs-lookup"><span data-stu-id="6f703-120">N</span></span>   | <span data-ttu-id="6f703-121">N</span><span class="sxs-lookup"><span data-stu-id="6f703-121">N</span></span>        |
| <span data-ttu-id="6f703-122">Cor</span><span class="sxs-lookup"><span data-stu-id="6f703-122">Color</span></span>     | [<span data-ttu-id="6f703-123">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="6f703-123">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="6f703-124">N</span><span class="sxs-lookup"><span data-stu-id="6f703-124">N</span></span>   | <span data-ttu-id="6f703-125">S</span><span class="sxs-lookup"><span data-stu-id="6f703-125">Y</span></span>        |
| <span data-ttu-id="6f703-126">StyleBits</span><span class="sxs-lookup"><span data-stu-id="6f703-126">StyleBits</span></span> | [<span data-ttu-id="6f703-127">Inteiro</span><span class="sxs-lookup"><span data-stu-id="6f703-127">Integer</span></span>](integer.md)             | <span data-ttu-id="6f703-128">N</span><span class="sxs-lookup"><span data-stu-id="6f703-128">N</span></span>   | <span data-ttu-id="6f703-129">S</span><span class="sxs-lookup"><span data-stu-id="6f703-129">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="6f703-130">Colunas</span><span class="sxs-lookup"><span data-stu-id="6f703-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="6f703-131"><span id="TextStyle"></span><span id="textstyle"></span><span id="TEXTSTYLE"></span>Estilo]</span><span class="sxs-lookup"><span data-stu-id="6f703-131"><span id="TextStyle"></span><span id="textstyle"></span><span id="TEXTSTYLE"></span>TextStyle</span></span>
</dt> <dd>

<span data-ttu-id="6f703-132">Esta coluna é o nome do estilo da fonte.</span><span class="sxs-lookup"><span data-stu-id="6f703-132">This column is the name of the font style.</span></span> <span data-ttu-id="6f703-133">Esse nome pode ser inserido na cadeia de texto para indicar uma alteração de estilo.</span><span class="sxs-lookup"><span data-stu-id="6f703-133">This name can be embedded in the text string to indicate a style change.</span></span> <span data-ttu-id="6f703-134">Observe que o nome do estilo da fonte usado neste campo não deve terminar com os caracteres: \_ UL.</span><span class="sxs-lookup"><span data-stu-id="6f703-134">Note that the font style name used in this field must not end with the characters: \_UL.</span></span> <span data-ttu-id="6f703-135">Consulte [adicionando controles e texto](adding-controls-and-text.md).</span><span class="sxs-lookup"><span data-stu-id="6f703-135">See [Adding Controls and Text](adding-controls-and-text.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f703-136"><span id="FaceName"></span><span id="facename"></span><span id="FACENAME"></span>FaceName</span><span class="sxs-lookup"><span data-stu-id="6f703-136"><span id="FaceName"></span><span id="facename"></span><span id="FACENAME"></span>FaceName</span></span>
</dt> <dd>

<span data-ttu-id="6f703-137">Uma cadeia de caracteres que indica o nome da fonte.</span><span class="sxs-lookup"><span data-stu-id="6f703-137">A string indicating the name of the font.</span></span> <span data-ttu-id="6f703-138">A cadeia de caracteres não deve ter mais de 31 caracteres.</span><span class="sxs-lookup"><span data-stu-id="6f703-138">The string must be no more than 31 characters long.</span></span>

</dd> <dt>

<span data-ttu-id="6f703-139"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>Tamanho</span><span class="sxs-lookup"><span data-stu-id="6f703-139"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>Size</span></span>
</dt> <dd>

<span data-ttu-id="6f703-140">O tamanho da fonte medido em pontos.</span><span class="sxs-lookup"><span data-stu-id="6f703-140">The font size measured in points.</span></span> <span data-ttu-id="6f703-141">Este deve ser um número não negativo.</span><span class="sxs-lookup"><span data-stu-id="6f703-141">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="6f703-142"><span id="Color"></span><span id="color"></span><span id="COLOR"></span>Cor</span><span class="sxs-lookup"><span data-stu-id="6f703-142"><span id="Color"></span><span id="color"></span><span id="COLOR"></span>Color</span></span>
</dt> <dd>

<span data-ttu-id="6f703-143">Esta coluna especifica a cor do texto exibida por um [controle de texto](text-control.md).</span><span class="sxs-lookup"><span data-stu-id="6f703-143">This column specifies the text color displayed by a [Text Control](text-control.md).</span></span> <span data-ttu-id="6f703-144">Todos os outros tipos de controles sempre usam a cor de texto padrão.</span><span class="sxs-lookup"><span data-stu-id="6f703-144">All other types of controls always use the default text color.</span></span> <span data-ttu-id="6f703-145">O valor colocado nessa coluna deve ser calculado usando a seguinte fórmula: 65536 \* azul + 256 \* verde + vermelho, em que vermelho, verde e azul estão cada um no intervalo de 0-255.</span><span class="sxs-lookup"><span data-stu-id="6f703-145">The value put in this column should be computed using the following formula: 65536 \* blue + 256 \* green + red, where red, green, and blue are each in the range of 0-255.</span></span> <span data-ttu-id="6f703-146">O valor não deve exceder 16777215, que é o valor de branco.</span><span class="sxs-lookup"><span data-stu-id="6f703-146">The value must not exceed 16777215, which is the value for white.</span></span> <span data-ttu-id="6f703-147">O valor é 0 para preto, 255 para vermelho, 65280 para verde, 16711680 para azul e 8421504 para cinza.</span><span class="sxs-lookup"><span data-stu-id="6f703-147">The value is 0 for black, 255 for red, 65280 for green, 16711680 for blue and 8421504 for grey.</span></span> <span data-ttu-id="6f703-148">Deixar o campo vazio especifica a cor padrão.</span><span class="sxs-lookup"><span data-stu-id="6f703-148">Leaving the field empty specifies the default color.</span></span>

<span data-ttu-id="6f703-149">Não coloque controles de [texto](text-control.md) transparentes na parte superior dos bitmaps coloridos.</span><span class="sxs-lookup"><span data-stu-id="6f703-149">Do not place transparent [Text controls](text-control.md) on top of colored bitmaps.</span></span> <span data-ttu-id="6f703-150">O texto pode não estar visível se o usuário alterar o esquema de cores de exibição.</span><span class="sxs-lookup"><span data-stu-id="6f703-150">The text may not be visible if the user changes the display color scheme.</span></span> <span data-ttu-id="6f703-151">Por exemplo, o texto pode se tornar invisível se o usuário definir o parâmetro de alto contraste para acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="6f703-151">For example, text may become invisible if the user sets the high contrast parameter for accessibility.</span></span>

</dd> <dt>

<span data-ttu-id="6f703-152"><span id="StyleBits"></span><span id="stylebits"></span><span id="STYLEBITS"></span>StyleBits</span><span class="sxs-lookup"><span data-stu-id="6f703-152"><span id="StyleBits"></span><span id="stylebits"></span><span id="STYLEBITS"></span>StyleBits</span></span>
</dt> <dd>

<span data-ttu-id="6f703-153">Uma combinação de bits que indica a formatação do texto.</span><span class="sxs-lookup"><span data-stu-id="6f703-153">A combination of bits indicating the formatting for the text.</span></span>

<span data-ttu-id="6f703-154">Os bits de estilo individuais têm os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="6f703-154">The individual style bits have the following values.</span></span>



| <span data-ttu-id="6f703-155">Constante</span><span class="sxs-lookup"><span data-stu-id="6f703-155">Constant</span></span>                             | <span data-ttu-id="6f703-156">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="6f703-156">Hexadecimal</span></span> | <span data-ttu-id="6f703-157">Decimal</span><span class="sxs-lookup"><span data-stu-id="6f703-157">Decimal</span></span> | <span data-ttu-id="6f703-158">Estilo</span><span class="sxs-lookup"><span data-stu-id="6f703-158">Style</span></span>      |
|--------------------------------------|-------------|---------|------------|
| <span data-ttu-id="6f703-159">**msidbTextStyleStyleBitsBold**</span><span class="sxs-lookup"><span data-stu-id="6f703-159">**msidbTextStyleStyleBitsBold**</span></span>      | <span data-ttu-id="6f703-160">0x001</span><span class="sxs-lookup"><span data-stu-id="6f703-160">0x001</span></span>       | <span data-ttu-id="6f703-161">1</span><span class="sxs-lookup"><span data-stu-id="6f703-161">1</span></span>       | <span data-ttu-id="6f703-162">Negrito</span><span class="sxs-lookup"><span data-stu-id="6f703-162">Bold</span></span>       |
| <span data-ttu-id="6f703-163">**msidbTextStyleStyleBitsItalic**</span><span class="sxs-lookup"><span data-stu-id="6f703-163">**msidbTextStyleStyleBitsItalic**</span></span>    | <span data-ttu-id="6f703-164">0x002</span><span class="sxs-lookup"><span data-stu-id="6f703-164">0x002</span></span>       | <span data-ttu-id="6f703-165">2</span><span class="sxs-lookup"><span data-stu-id="6f703-165">2</span></span>       | <span data-ttu-id="6f703-166">Itálico</span><span class="sxs-lookup"><span data-stu-id="6f703-166">Italic</span></span>     |
| <span data-ttu-id="6f703-167">**msidbTextStyleStyleBitsUnderline**</span><span class="sxs-lookup"><span data-stu-id="6f703-167">**msidbTextStyleStyleBitsUnderline**</span></span> | <span data-ttu-id="6f703-168">0x004</span><span class="sxs-lookup"><span data-stu-id="6f703-168">0x004</span></span>       | <span data-ttu-id="6f703-169">4</span><span class="sxs-lookup"><span data-stu-id="6f703-169">4</span></span>       | <span data-ttu-id="6f703-170">Underline</span><span class="sxs-lookup"><span data-stu-id="6f703-170">Underline</span></span>  |
| <span data-ttu-id="6f703-171">**msidbTextStyleStyleBitsStrike**</span><span class="sxs-lookup"><span data-stu-id="6f703-171">**msidbTextStyleStyleBitsStrike**</span></span>    | <span data-ttu-id="6f703-172">0x008</span><span class="sxs-lookup"><span data-stu-id="6f703-172">0x008</span></span>       | <span data-ttu-id="6f703-173">8</span><span class="sxs-lookup"><span data-stu-id="6f703-173">8</span></span>       | <span data-ttu-id="6f703-174">Riscar</span><span class="sxs-lookup"><span data-stu-id="6f703-174">Strike out</span></span> |



 

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="6f703-175">Validação</span><span class="sxs-lookup"><span data-stu-id="6f703-175">Validation</span></span>

<dl>

[<span data-ttu-id="6f703-176">ICE03</span><span class="sxs-lookup"><span data-stu-id="6f703-176">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="6f703-177">ICE06</span><span class="sxs-lookup"><span data-stu-id="6f703-177">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="6f703-178">ICE31</span><span class="sxs-lookup"><span data-stu-id="6f703-178">ICE31</span></span>](ice31.md)  
[<span data-ttu-id="6f703-179">ICE45</span><span class="sxs-lookup"><span data-stu-id="6f703-179">ICE45</span></span>](ice45.md)  
</dl>

 

 



