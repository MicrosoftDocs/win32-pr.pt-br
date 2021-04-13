---
title: Funções de fonte e texto (OpenGL)
description: As funções a seguir podem ser usadas para gerenciar fontes e texto.
ms.assetid: 42e16967-1eeb-4d37-bbd6-33c473eb2757
keywords:
- Funções WGL, texto
- Funções do WGL, fonte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e205549346cccc2c44b7670db91530cfbc24017d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369120"
---
# <a name="font-and-text-functions-opengl"></a><span data-ttu-id="5eb46-105">Funções de fonte e texto (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="5eb46-105">Font and Text Functions (OpenGL)</span></span>

<span data-ttu-id="5eb46-106">As funções a seguir podem ser usadas para gerenciar fontes e texto.</span><span class="sxs-lookup"><span data-stu-id="5eb46-106">The following functions can be used to manage fonts and text.</span></span>



| <span data-ttu-id="5eb46-107">Função do Windows</span><span class="sxs-lookup"><span data-stu-id="5eb46-107">Windows Function</span></span>                                 | <span data-ttu-id="5eb46-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="5eb46-108">Description</span></span>                                                                                                                                                                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5eb46-109">**wglUseFontBitmaps**</span><span class="sxs-lookup"><span data-stu-id="5eb46-109">**wglUseFontBitmaps**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa)   | <span data-ttu-id="5eb46-110">Cria um conjunto de listas de exibição de bitmaps de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5eb46-110">Creates a set of character bitmap display lists.</span></span> <span data-ttu-id="5eb46-111">Os caracteres são provenientes de uma fonte atual do contexto de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="5eb46-111">Characters come from a specified device context's current font.</span></span> <span data-ttu-id="5eb46-112">Os caracteres são especificados como uma execução consecutiva dentro do conjunto de glifos da fonte.</span><span class="sxs-lookup"><span data-stu-id="5eb46-112">Characters are specified as a consecutive run within the font's glyph set.</span></span>                                      |
| [<span data-ttu-id="5eb46-113">**wglUseFontOutlines**</span><span class="sxs-lookup"><span data-stu-id="5eb46-113">**wglUseFontOutlines**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) | <span data-ttu-id="5eb46-114">Cria um conjunto de listas de exibição, com base nos glifos da fonte da estrutura de tópicos selecionada no momento de um contexto de dispositivo, para uso com o contexto de renderização atual.</span><span class="sxs-lookup"><span data-stu-id="5eb46-114">Creates a set of display lists, based on the glyphs of the currently selected outline font of a device context, for use with the current rendering context.</span></span> <span data-ttu-id="5eb46-115">As listas de exibição são usadas para desenhar caracteres de 3-D de fontes TrueType.</span><span class="sxs-lookup"><span data-stu-id="5eb46-115">The display lists are used to draw 3-D characters of TrueType fonts.</span></span> |



 

<span data-ttu-id="5eb46-116">As funções **wglUseFontBitmaps** e **wglUseFontOutlines** usam um identificador para um contexto de dispositivo e usam a fonte atual desse contexto de dispositivo como uma fonte para os bitmaps.</span><span class="sxs-lookup"><span data-stu-id="5eb46-116">The **wglUseFontBitmaps** and **wglUseFontOutlines** functions take a handle to a device context, and use that device context's current font as a source for the bitmaps.</span></span> <span data-ttu-id="5eb46-117">Portanto, é necessário definir a fonte do contexto do dispositivo e as propriedades da fonte antes de chamar **wglUseFontBitmaps** ou **wglUseFontOutlines**.</span><span class="sxs-lookup"><span data-stu-id="5eb46-117">It is therefore necessary to set the device context's font and the font's properties before calling **wglUseFontBitmaps** or **wglUseFontOutlines**.</span></span>

<span data-ttu-id="5eb46-118">As funções [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) e [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) também usam um parâmetro que transforma o primeiro glifo na fonte em uma lista de exibição de bitmap e um parâmetro que especifica quantos glifos se transforma em listas de exibição.</span><span class="sxs-lookup"><span data-stu-id="5eb46-118">The [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) and [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) functions also take a parameter that turns the first glyph in the font into a bitmap display list, and a parameter that specifies how many glyphs to turn into display lists.</span></span> <span data-ttu-id="5eb46-119">Em seguida, a função cria listas de exibição para a execução consecutiva especificada de glifos.</span><span class="sxs-lookup"><span data-stu-id="5eb46-119">The function then creates display lists for the specified consecutive run of glyphs.</span></span> <span data-ttu-id="5eb46-120">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="5eb46-120">For example:</span></span>

-   <span data-ttu-id="5eb46-121">Para criar um conjunto de listas de exibição de bitmap 224 para todos os glifos do conjunto de caracteres do Windows, defina esses dois parâmetros como 32 e 224, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="5eb46-121">To create a set of 224 bitmap display lists for all of the Windows character set glyphs, set these two parameters to 32 and 224, respectively.</span></span>
-   <span data-ttu-id="5eb46-122">Para criar um conjunto de listas de exibição de bitmap 256 para todos os glifos de conjunto de caracteres OEM, defina esses dois parâmetros como 0 e 256, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="5eb46-122">To create a set of 256 bitmap display lists for all of the OEM character set glyphs, set these two parameters to 0 and 256, respectively.</span></span>
-   <span data-ttu-id="5eb46-123">Para criar uma única lista de exibição de bitmap para qualquer glifo de conjunto de caracteres único, defina o segundo desses parâmetros como 1.</span><span class="sxs-lookup"><span data-stu-id="5eb46-123">To create a single bitmap display list for any single character set glyph, set the second of these parameters to 1.</span></span>

<span data-ttu-id="5eb46-124">As funções **wglUseFontBitmaps** e **wglUseFontOutlines** representam um glifo nulo em uma fonte com uma lista de exibição vazia.</span><span class="sxs-lookup"><span data-stu-id="5eb46-124">The **wglUseFontBitmaps** and **wglUseFontOutlines** functions represent a null glyph in a font with an empty display list.</span></span>

<span data-ttu-id="5eb46-125">As listas de exibição criadas por uma chamada para **wglUseFontBitmaps** ou **wglUseFontOutlines** são automaticamente numeradas consecutivamente.</span><span class="sxs-lookup"><span data-stu-id="5eb46-125">The display lists created by a call to **wglUseFontBitmaps** or **wglUseFontOutlines** are automatically numbered consecutively.</span></span>

<span data-ttu-id="5eb46-126">Depois de chamar a função [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) ou [**WglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) , chame [**glCallLists**](glcalllists.md) para desenhar uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5eb46-126">After calling the [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) or [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) function, call [**glCallLists**](glcalllists.md) to draw a string of characters.</span></span> <span data-ttu-id="5eb46-127">Consulte [desenho de texto em uma janela Double-Buffered OpenGL](drawing-text-in-a-double-buffered-opengl-window.md) para obter o código de exemplo.</span><span class="sxs-lookup"><span data-stu-id="5eb46-127">See [Drawing Text in a Double-Buffered OpenGL Window](drawing-text-in-a-double-buffered-opengl-window.md) for sample code.</span></span> <span data-ttu-id="5eb46-128">Nesse contexto, **glCallLists** usa cada caractere em uma cadeia de caracteres como um índice na matriz de listas de exibição numeradas consecutivamente criadas por **wglUseFontBitmaps** ou **wglUseFontOutlines**.</span><span class="sxs-lookup"><span data-stu-id="5eb46-128">In this context, **glCallLists** uses each character in a string as an index into the array of consecutively numbered display lists created by **wglUseFontBitmaps** or **wglUseFontOutlines**.</span></span>

<span data-ttu-id="5eb46-129">Quando você terminar de desenhar o texto, chame a função [**glDeleteLists**](gldeletelists.md) para liberar o conjunto contíguo de listas de exibição criadas por **wglUseFontBitmaps** e **wglUseFontOutlines**.</span><span class="sxs-lookup"><span data-stu-id="5eb46-129">When you finish drawing text, call the [**glDeleteLists**](gldeletelists.md) function to release the contiguous set of display lists created by **wglUseFontBitmaps** and **wglUseFontOutlines**.</span></span>

 

 




