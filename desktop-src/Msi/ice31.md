---
description: ICE31 valida todos os estilos de fonte predefinidos usados em controles que exibem texto. Ele também valida que a propriedade DefaultUIFont se refere a um estilo de fonte válido.
ms.assetid: 07e60774-0e26-4a50-b818-a8f074512e3e
title: ICE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4797d577ceaa2a2b7838f1f03a8577d9a633fb65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170230"
---
# <a name="ice31"></a><span data-ttu-id="b5418-104">ICE31</span><span class="sxs-lookup"><span data-stu-id="b5418-104">ICE31</span></span>

<span data-ttu-id="b5418-105">ICE31 valida todos os estilos de fonte predefinidos usados em [controles](controls.md) que exibem texto.</span><span class="sxs-lookup"><span data-stu-id="b5418-105">ICE31 validates any predefined font styles used in [controls](controls.md) that display text.</span></span> <span data-ttu-id="b5418-106">Ele também valida que a propriedade [**DefaultUIFont**](defaultuifont.md) se refere a um estilo de fonte válido.</span><span class="sxs-lookup"><span data-stu-id="b5418-106">It also validates that the [**DefaultUIFont**](defaultuifont.md) property refers to a valid font style.</span></span>

<span data-ttu-id="b5418-107">Os controles podem ter um estilo de fonte predefinido, conforme descrito em [adicionando controles e texto](adding-controls-and-text.md).</span><span class="sxs-lookup"><span data-stu-id="b5418-107">Controls can have a predefined font style as described in [Adding Controls and Text](adding-controls-and-text.md).</span></span> <span data-ttu-id="b5418-108">Para definir a fonte e o estilo da fonte de uma cadeia de texto, Prefixe a cadeia de caracteres exibidos com { \\ Style} ou {&*Style*}.</span><span class="sxs-lookup"><span data-stu-id="b5418-108">To set the font and font style of a text string, prefix the string of displayed characters with {\\style} or {&*style*}.</span></span> <span data-ttu-id="b5418-109">Em que Style é um identificador listado na coluna TextStyle da [tabela TextStyle](textstyle-table.md).</span><span class="sxs-lookup"><span data-stu-id="b5418-109">Where style is an identifier listed in the TextStyle column of the [TextStyle table](textstyle-table.md).</span></span> <span data-ttu-id="b5418-110">Se nenhuma dessas opções estiver presente, mas a propriedade [**DefaultUIFont**](defaultuifont.md) for definida como um estilo de texto válido, essa fonte será usada.</span><span class="sxs-lookup"><span data-stu-id="b5418-110">If neither of these are present, but the [**DefaultUIFont**](defaultuifont.md) property is defined as a valid text style, that font will be used.</span></span>

<span data-ttu-id="b5418-111">ICE31 verifica a coluna de texto de cada controle na [tabela de controle](control-table.md) para verificar se existe uma entrada válida na [tabela TextStyle](textstyle-table.md).</span><span class="sxs-lookup"><span data-stu-id="b5418-111">ICE31 checks the Text column for each control in the [Control Table](control-table.md) to verifies that a valid entry exist in the [TextStyle table](textstyle-table.md).</span></span>

<span data-ttu-id="b5418-112">ICE31 ignora o [controle ScrollableText](scrollabletext-control.md).</span><span class="sxs-lookup"><span data-stu-id="b5418-112">ICE31 ignores the [ScrollableText Control](scrollabletext-control.md).</span></span>

## <a name="results"></a><span data-ttu-id="b5418-113">Resultados</span><span class="sxs-lookup"><span data-stu-id="b5418-113">Results</span></span>

<span data-ttu-id="b5418-114">ICE31 posta uma mensagem de erro para estilos indefinidos, nomes de estilo que são muito longos, uma tabela de TextStyle ausente e marcas de estilo sem chave de fechamento.</span><span class="sxs-lookup"><span data-stu-id="b5418-114">ICE31 posts an error message for undefined styles, style names that are too long, a missing TextStyle table, and style tags with no closing brace.</span></span>

<span data-ttu-id="b5418-115">ICE31 lançará um aviso se a marca de estilo não estiver no início da linha ou se um controle tiver várias marcas de estilo.</span><span class="sxs-lookup"><span data-stu-id="b5418-115">ICE31 posts a warning if the style tag is not at the beginning of the line, or if a control has multiple style tags.</span></span>

## <a name="example"></a><span data-ttu-id="b5418-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b5418-116">Example</span></span>

<span data-ttu-id="b5418-117">ICE31 posta os seguintes erros para o exemplo mostrado:</span><span class="sxs-lookup"><span data-stu-id="b5418-117">ICE31 posts the following errors for the example shown:</span></span>

-   <span data-ttu-id="b5418-118">O controle DialogB. Control1 usa o BadStyle TextStyle indefinido.</span><span class="sxs-lookup"><span data-stu-id="b5418-118">Control DialogB.Control1 uses undefined TextStyle BadStyle.</span></span>
-   <span data-ttu-id="b5418-119">O controle DialogB. Control2 usa BadStyle TextStyle indefinido.</span><span class="sxs-lookup"><span data-stu-id="b5418-119">Control DialogB.Control2 uses undefined TextStyle BadStyle.</span></span>
-   <span data-ttu-id="b5418-120">O controle DialogB. Control6 não tem chaves de fechamento no estilo de texto.</span><span class="sxs-lookup"><span data-stu-id="b5418-120">Control DialogB.Control6 is missing closing brace in text style.</span></span>
-   <span data-ttu-id="b5418-121">O controle DialogB. Control3 especifica um estilo de texto muito longo para ser válido.</span><span class="sxs-lookup"><span data-stu-id="b5418-121">Control DialogB.Control3 specifies a text style that is too long to be valid.</span></span>

<span data-ttu-id="b5418-122">ICE31 posta o seguinte aviso para o exemplo mostrado:</span><span class="sxs-lookup"><span data-stu-id="b5418-122">ICE31 posts the following warning for the example shown:</span></span>

-   <span data-ttu-id="b5418-123">A marca de estilo de texto em DialogB. Control4 não tem efeito.</span><span class="sxs-lookup"><span data-stu-id="b5418-123">Text Style tag in DialogB.Control4 has no effect.</span></span> <span data-ttu-id="b5418-124">Você realmente deseja que ele apareça como texto?</span><span class="sxs-lookup"><span data-stu-id="b5418-124">Do you really want it to appear as text?</span></span>

<span data-ttu-id="b5418-125">[Tabela de controle](control-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="b5418-125">[Control Table](control-table.md) (partial)</span></span>



| <span data-ttu-id="b5418-126">caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="b5418-126">Dialog</span></span>  | <span data-ttu-id="b5418-127">Control</span><span class="sxs-lookup"><span data-stu-id="b5418-127">Control</span></span>  | <span data-ttu-id="b5418-128">Texto</span><span class="sxs-lookup"><span data-stu-id="b5418-128">Text</span></span>                                                                                                                                                                |
|---------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5418-129">Caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="b5418-129">DialogA</span></span> | <span data-ttu-id="b5418-130">Control0</span><span class="sxs-lookup"><span data-stu-id="b5418-130">Control0</span></span> | <span data-ttu-id="b5418-131">{ \\ OKStyle} este é o texto a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="b5418-131">{\\OKStyle}This is the text to display.</span></span>                                                                                                                             |
| <span data-ttu-id="b5418-132">Caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="b5418-132">DialogA</span></span> | <span data-ttu-id="b5418-133">Control1</span><span class="sxs-lookup"><span data-stu-id="b5418-133">Control1</span></span> | <span data-ttu-id="b5418-134">{&OKStyle} Este é o texto a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="b5418-134">{&OKStyle}This is the text to display.</span></span>                                                                                                                              |
| <span data-ttu-id="b5418-135">DialogB</span><span class="sxs-lookup"><span data-stu-id="b5418-135">DialogB</span></span> | <span data-ttu-id="b5418-136">Control1</span><span class="sxs-lookup"><span data-stu-id="b5418-136">Control1</span></span> | <span data-ttu-id="b5418-137">{&BadStyle} Este é o texto a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="b5418-137">{&BadStyle}This is the text to display.</span></span>                                                                                                                             |
| <span data-ttu-id="b5418-138">DialogB</span><span class="sxs-lookup"><span data-stu-id="b5418-138">DialogB</span></span> | <span data-ttu-id="b5418-139">Control2</span><span class="sxs-lookup"><span data-stu-id="b5418-139">Control2</span></span> | <span data-ttu-id="b5418-140">{ \\ BadStyle} este é o texto a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="b5418-140">{\\BadStyle}This is the text to display.</span></span>                                                                                                                            |
| <span data-ttu-id="b5418-141">DialogB</span><span class="sxs-lookup"><span data-stu-id="b5418-141">DialogB</span></span> | <span data-ttu-id="b5418-142">Control3</span><span class="sxs-lookup"><span data-stu-id="b5418-142">Control3</span></span> | <span data-ttu-id="b5418-143">{&estilo que está acima de 72 caracteres e, portanto, não pode ser um estilo mesmo que, de alguma forma, você tenha gerenciado para obtê-lo na tabela TextStyle} Este é o texto a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="b5418-143">{&Style that is over 72 chars and therefore cannot possibly be a style even if somehow you did manage to get it in the TextStyle table}This is the text to display.</span></span> |
| <span data-ttu-id="b5418-144">DialogB</span><span class="sxs-lookup"><span data-stu-id="b5418-144">DialogB</span></span> | <span data-ttu-id="b5418-145">Control4</span><span class="sxs-lookup"><span data-stu-id="b5418-145">Control4</span></span> | <span data-ttu-id="b5418-146">Aviso { \\ OKStyle} este é o texto a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="b5418-146">Warning {\\OKStyle}This is the text to display.</span></span>                                                                                                                     |
| <span data-ttu-id="b5418-147">DialogB</span><span class="sxs-lookup"><span data-stu-id="b5418-147">DialogB</span></span> | <span data-ttu-id="b5418-148">Control5</span><span class="sxs-lookup"><span data-stu-id="b5418-148">Control5</span></span> | <span data-ttu-id="b5418-149">{ \\ OKStyle} {&OKStyle} este é o texto a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="b5418-149">{\\OKStyle}{&OKStyle}This is the text to display.</span></span>                                                                                                                   |
| <span data-ttu-id="b5418-150">DialogB</span><span class="sxs-lookup"><span data-stu-id="b5418-150">DialogB</span></span> | <span data-ttu-id="b5418-151">Control6</span><span class="sxs-lookup"><span data-stu-id="b5418-151">Control6</span></span> | <span data-ttu-id="b5418-152">{ \\ OKStyle este é o texto a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="b5418-152">{\\OKStyle This is the text to display.</span></span>                                                                                                                             |



 

<span data-ttu-id="b5418-153">[Tabela TextStyle](textstyle-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="b5418-153">[TextStyle table](textstyle-table.md) (partial)</span></span>



| <span data-ttu-id="b5418-154">Estilo]</span><span class="sxs-lookup"><span data-stu-id="b5418-154">TextStyle</span></span> |
|-----------|
| <span data-ttu-id="b5418-155">OkStyle</span><span class="sxs-lookup"><span data-stu-id="b5418-155">OkStyle</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="b5418-156">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b5418-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5418-157">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="b5418-157">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



