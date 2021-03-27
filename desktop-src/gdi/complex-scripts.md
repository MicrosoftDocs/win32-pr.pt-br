---
description: Embora as funções discutidas anteriormente funcionem bem para muitas linguagens, elas podem não lidar com as necessidades de scripts complexos.
ms.assetid: a60b50c8-13e8-4c61-989f-187bb67cf929
title: Scripts complexos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c149aa1d9a6f5caf78fec5227f25aa30146fc273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827671"
---
# <a name="complex-scripts"></a><span data-ttu-id="d8829-103">Scripts complexos</span><span class="sxs-lookup"><span data-stu-id="d8829-103">Complex Scripts</span></span>

<span data-ttu-id="d8829-104">Embora as funções discutidas anteriormente funcionem bem para muitas linguagens, elas podem não lidar com as necessidades de scripts complexos.</span><span class="sxs-lookup"><span data-stu-id="d8829-104">While the functions discussed in the preceding work well for many languages, they may not deal with the needs of complex scripts.</span></span> <span data-ttu-id="d8829-105">*Scripts complexos* são linguagens cujo formulário impresso não é renderizado de uma maneira simples.</span><span class="sxs-lookup"><span data-stu-id="d8829-105">*Complex scripts* are languages whose printed form is not rendered in a simple way.</span></span> <span data-ttu-id="d8829-106">Por exemplo, um script complexo pode permitir renderização bidirecional, formatação contextual de glifos ou caracteres de combinação.</span><span class="sxs-lookup"><span data-stu-id="d8829-106">For example, a complex script may allow bidirectional rendering, contextual shaping of glyphs, or combining characters.</span></span> <span data-ttu-id="d8829-107">Devido a esses requisitos especiais, o controle da saída de texto deve ser muito flexível.</span><span class="sxs-lookup"><span data-stu-id="d8829-107">Due to these special requirements, the control of text output must be very flexible.</span></span>

<span data-ttu-id="d8829-108">As funções que exibem [**texto TextOut,**](/windows/desktop/api/Wingdi/nf-wingdi-textouta) [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), [**TabbedTextOut**](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta), [**DrawText**](/windows/desktop/api/Winuser/nf-winuser-drawtext)e [**GetTextExtentExPoint**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa) foram estendidas para dar suporte a scripts complexos.</span><span class="sxs-lookup"><span data-stu-id="d8829-108">Functions that display text [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta), [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), [**TabbedTextOut**](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta), [**DrawText**](/windows/desktop/api/Winuser/nf-winuser-drawtext), and [**GetTextExtentExPoint**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa) have been extended to support complex scripts.</span></span> <span data-ttu-id="d8829-109">Em geral, esse suporte é transparente para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d8829-109">In general, this support is transparent to the application.</span></span> <span data-ttu-id="d8829-110">No entanto, os aplicativos devem salvar caracteres em um buffer e exibir uma linha inteira de texto ao mesmo tempo, para que os módulos de modelagem de script complexos possam usar o contexto para reordenar e gerar glifos corretamente.</span><span class="sxs-lookup"><span data-stu-id="d8829-110">However, applications should save characters in a buffer and display a whole line of text at one time, so that the complex script shaping modules can use context to reorder and generate glyphs correctly.</span></span> <span data-ttu-id="d8829-111">Além disso, como a largura de um glifo pode variar por contexto, os aplicativos devem usar [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa) para determinar o comprimento da linha em vez de usar larguras de caracteres em cache.</span><span class="sxs-lookup"><span data-stu-id="d8829-111">In addition, because the width of a glyph can vary by context, applications should use [**GetTextExtentExPoint**](/windows/win32/api/wingdi/nf-wingdi-gettextextentexpointa) to determine line length rather than using cached character widths.</span></span>

<span data-ttu-id="d8829-112">Além disso, aplicativos complexos com reconhecimento de script devem considerar a adição de suporte à ordem de leitura da direita para a esquerda e ao alinhamento à direita para seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="d8829-112">In addition, complex script-aware applications should consider adding support for right-to-left reading order and right alignment to their applications.</span></span> <span data-ttu-id="d8829-113">Você pode alternar a ordem de leitura ou o alinhamento entre a esquerda e a direita com o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="d8829-113">You can toggle the reading order or alignment between left and right with the following code:</span></span>


```C++
// Save lAlign (this example uses static variables) 
static LONG lAlign = TA_LEFT;

// When user toggles alignment (assuming TA_CENTER is not supported). 

lAlign = TA_RIGHT;

// When the user toggles reading order. 

lAlign = TA_RTLREADING;

// Before calling ExtTextOut, for example, when processing WM_PAINT  

SetTextAlign (hDc, lAlign);
```



<span data-ttu-id="d8829-114">Para alternar os dois atributos de uma vez, execute a instrução a seguir e chame [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) e [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), conforme mostrado anteriormente:</span><span class="sxs-lookup"><span data-stu-id="d8829-114">To toggle both attributes at once, execute the following statement and then call [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) and [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta), as shown previously:</span></span>


```C++
lAlign = TA_RIGHT^TA_RTLREADING;  //pre-inline !
```



<span data-ttu-id="d8829-115">Você também pode processar scripts complexos com o Uniscribe.</span><span class="sxs-lookup"><span data-stu-id="d8829-115">You can also process complex scripts with Uniscribe.</span></span> <span data-ttu-id="d8829-116">O Uniscribe é um conjunto de funções que permitem um grau de controle detalhado para scripts complexos.</span><span class="sxs-lookup"><span data-stu-id="d8829-116">Uniscribe is a set of functions that allow a fine degree of control for complex scripts.</span></span> <span data-ttu-id="d8829-117">Para obter mais informações, consulte [Uniscribe](../intl/uniscribe.md) e [processamento de scripts complexos](../intl/processing-complex-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="d8829-117">For more information, see [Uniscribe](../intl/uniscribe.md) and [Processing Complex Scripts](../intl/processing-complex-scripts.md).</span></span>

 

 
