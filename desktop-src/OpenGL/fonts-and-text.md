---
title: Fontes e texto (OpenGL)
description: A implementação da Microsoft do OpenGL no Windows dá suporte a gráficos GDI em uma janela OpenGL de buffer único.
ms.assetid: 25a45e1a-6c1e-416b-8993-daeefc1100f3
keywords:
- OpenGL no Windows, fontes
- OpenGL no Windows, texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fba4ffe996bd88a6285f615ddacb31e57fc311
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369119"
---
# <a name="fonts-and-text-opengl"></a><span data-ttu-id="59a6c-105">Fontes e texto (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="59a6c-105">Fonts and Text (OpenGL)</span></span>

<span data-ttu-id="59a6c-106">A implementação da Microsoft do OpenGL no Windows dá suporte a gráficos GDI em uma janela OpenGL de buffer único.</span><span class="sxs-lookup"><span data-stu-id="59a6c-106">Microsoft's implementation of OpenGL in Windows supports GDI graphics in a single-buffered OpenGL window.</span></span> <span data-ttu-id="59a6c-107">Ele não dá suporte a elementos gráficos GDI em uma janela OpenGL com buffer duplo.</span><span class="sxs-lookup"><span data-stu-id="59a6c-107">It does not support GDI graphics in a double-buffered OpenGL window.</span></span> <span data-ttu-id="59a6c-108">Portanto, você pode chamar apenas as funções de fonte e texto do GDI padrão para desenhar texto em uma janela OpenGL com buffer único; Você não pode chamar essas funções para desenhar texto em uma janela OpenGL com buffer duplo.</span><span class="sxs-lookup"><span data-stu-id="59a6c-108">Thus, you can call only the standard GDI font and text functions to draw text in a single-buffered OpenGL window; you cannot call those functions to draw text in a double-buffered OpenGL window.</span></span>

<span data-ttu-id="59a6c-109">Há uma solução alternativa para essa restrição no texto em janelas com buffer duplo: criar listas de exibição OpenGL para imagens de bitmap de caracteres e, em seguida, executar essas listas de exibição para desenhar caracteres.</span><span class="sxs-lookup"><span data-stu-id="59a6c-109">There is a workaround for this restriction on text in double-buffered windows: build OpenGL display lists for bitmap images of characters, and then execute those display lists to draw characters.</span></span> <span data-ttu-id="59a6c-110">Há três etapas principais neste processo:</span><span class="sxs-lookup"><span data-stu-id="59a6c-110">There are three main steps in this process:</span></span>

1.  <span data-ttu-id="59a6c-111">Selecione uma fonte para um contexto de dispositivo, definindo as propriedades da fonte conforme desejado.</span><span class="sxs-lookup"><span data-stu-id="59a6c-111">Select a font for a device context, setting the font's properties as desired.</span></span>
2.  <span data-ttu-id="59a6c-112">Crie um conjunto de listas de exibição de bitmap com base nos glifos na fonte do contexto do dispositivo, uma lista de exibição para cada glifo que o aplicativo irá desenhar.</span><span class="sxs-lookup"><span data-stu-id="59a6c-112">Create a set of bitmap display lists based on the glyphs in the device context's font, one display list for each glyph that the application will draw.</span></span>
3.  <span data-ttu-id="59a6c-113">Desenhe cada glifo em uma cadeia de caracteres, usando essas listas de exibição de bitmap.</span><span class="sxs-lookup"><span data-stu-id="59a6c-113">Draw each glyph in a string, using those bitmap display lists.</span></span>

<span data-ttu-id="59a6c-114">Para criar as listas de exibição, chame as funções [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) e [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) .</span><span class="sxs-lookup"><span data-stu-id="59a6c-114">To create the display lists, call the [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) and [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) functions.</span></span> <span data-ttu-id="59a6c-115">Para desenhar caracteres em uma seqüência de caracteres usando as listas de exibição, chame [**glCallLists**](glcalllists.md).</span><span class="sxs-lookup"><span data-stu-id="59a6c-115">To draw characters in a string using those display lists, call [**glCallLists**](glcalllists.md).</span></span>

<span data-ttu-id="59a6c-116">Para criar aplicativos que são fáceis de localizar e que usam recursos com moderação, a criação e o armazenamento dessas listas de exibição de imagem de glifo devem ser gerenciados com cuidado.</span><span class="sxs-lookup"><span data-stu-id="59a6c-116">To create applications that are easy to localize and that use resources sparingly, the creation and storage of these glyph image display lists must be managed carefully.</span></span> <span data-ttu-id="59a6c-117">Muitas linguagens, ao contrário do inglês, têm alfabetos cujos códigos de caractere variam em um conjunto de valores relativamente grande.</span><span class="sxs-lookup"><span data-stu-id="59a6c-117">Many languages, unlike English, have alphabets whose character codes range over a relatively large set of values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="59a6c-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="59a6c-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59a6c-119">Funções de fonte e texto</span><span class="sxs-lookup"><span data-stu-id="59a6c-119">Font and Text Functions</span></span>](font-and-text-functions.md)
</dt> </dl>

 

 




