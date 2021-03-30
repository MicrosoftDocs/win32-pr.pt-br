---
title: Como implementar dicas de ferramentas de balão
description: As dicas de ferramentas de balão são semelhantes às dicas de ferramenta padrão, mas são exibidas em um balão \ 0034; de estilo animado \ 0034; com uma haste apontando para a ferramenta.
ms.assetid: 59FEA8B6-772D-4BEF-A18C-945EC6A56FA2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe578f69092a35a7f3ccc5eaa6a5987128ebdd66
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635291"
---
# <a name="how-to-implement-balloon-tooltips"></a><span data-ttu-id="299e5-103">Como implementar dicas de ferramentas de balão</span><span class="sxs-lookup"><span data-stu-id="299e5-103">How to Implement Balloon Tooltips</span></span>

<span data-ttu-id="299e5-104">As dicas de ferramentas de balão são semelhantes às dicas de ferramenta padrão, mas são exibidas em um "balão" estilo animado com uma haste apontando para a ferramenta.</span><span class="sxs-lookup"><span data-stu-id="299e5-104">Balloon tooltips are similar to standard tooltips, but are displayed in a cartoon-style "balloon" with a stem pointing to the tool.</span></span> <span data-ttu-id="299e5-105">As dicas de ferramentas de balão podem ser de linha única ou de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="299e5-105">Balloon tooltips can be either single-line or multiline.</span></span> <span data-ttu-id="299e5-106">Eles são criados e manipulados quase da mesma forma que as dicas de ferramentas padrão.</span><span class="sxs-lookup"><span data-stu-id="299e5-106">They are created and handled in much the same way as standard tooltips.</span></span>

<span data-ttu-id="299e5-107">A posição padrão da haste e do retângulo é mostrada na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="299e5-107">The default position of the stem and rectangle is shown in the following illustration.</span></span> <span data-ttu-id="299e5-108">Se a ferramenta estiver muito próxima da parte superior da tela, a dica de ferramenta aparecerá abaixo e à direita do retângulo da ferramentas.</span><span class="sxs-lookup"><span data-stu-id="299e5-108">If the tool is too close to the top of the screen, the tooltip appears below and to the right of the tool's rectangle.</span></span> <span data-ttu-id="299e5-109">Se a ferramenta estiver muito perto do lado direito da tela, os princípios semelhantes se aplicarão, mas a dica de ferramenta aparecerá à esquerda do retângulo de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="299e5-109">If the tool is too close to the right side of the screen, similar principles apply, but the tooltip appears to the left of the tool's rectangle.</span></span>

![captura de tela de uma caixa de diálogo; uma dica de ferramenta de balão com uma linha de texto é exibida acima e à direita do destino](images/tt-balloon.png)

<span data-ttu-id="299e5-111">Você pode alterar o posicionamento padrão definindo o sinalizador **\_ CENTERTIP de TTF** no membro **uFlags** da estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) de dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="299e5-111">You can change the default positioning by setting the **TTF\_CENTERTIP** flag in the **uFlags** member of the tooltip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="299e5-112">Nesse caso, a haste normalmente aponta para o centro da borda inferior do retângulo da ferramenta e o retângulo do texto é exibido diretamente abaixo da ferramenta.</span><span class="sxs-lookup"><span data-stu-id="299e5-112">In that case, the stem normally points to the center of the lower edge of the tool's rectangle, and the text rectangle is displayed directly below the tool.</span></span> <span data-ttu-id="299e5-113">A haste é anexada ao retângulo de texto no centro da borda superior.</span><span class="sxs-lookup"><span data-stu-id="299e5-113">The stem attaches to the text rectangle at the center of the upper edge.</span></span> <span data-ttu-id="299e5-114">Se a ferramenta estiver muito perto da parte inferior da tela, o retângulo de texto será centralizado acima da ferramenta e o tronco se conectará ao centro da borda inferior.</span><span class="sxs-lookup"><span data-stu-id="299e5-114">If the tool is too close to the bottom of the screen, the text rectangle is centered above the tool, and the stem attaches to the center of the lower edge.</span></span>

<span data-ttu-id="299e5-115">A ilustração a seguir mostra uma dica de ferramenta que é centralizada na Tool.</span><span class="sxs-lookup"><span data-stu-id="299e5-115">The following illustration shows a tooltip that is centered on the tool.</span></span>

![captura de tela de uma caixa de diálogo; uma dica de ferramenta de balão com uma linha de texto é exibida centralizada abaixo do destino](images/tt-ballooncenter.png)

<span data-ttu-id="299e5-117">Se você quiser especificar onde os pontos de haste, defina o sinalizador de **\_ faixa de TTF** no membro **uFlags** da estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) da dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="299e5-117">If you want to specify where the stem points, set the **TTF\_TRACK** flag in the **uFlags** member of the tooltip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="299e5-118">Em seguida, você especifica a coordenada enviando uma mensagem [**TTM \_ TRACKPOSITION**](ttm-trackposition.md) , com as coordenadas x e y no valor de *lParam* .</span><span class="sxs-lookup"><span data-stu-id="299e5-118">You then specify the coordinate by sending a [**TTM\_TRACKPOSITION**](ttm-trackposition.md) message, with the x- and y-coordinates in the *lParam* value.</span></span> <span data-ttu-id="299e5-119">Se **ttf \_ CENTERTIP** também for definido, a haste ainda apontará para a posição especificada pela mensagem **TTM \_ TRACKPOSITION** .</span><span class="sxs-lookup"><span data-stu-id="299e5-119">If **TTF\_CENTERTIP** is also set, the stem still points to the position specified by the **TTM\_TRACKPOSITION** message.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="299e5-120">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="299e5-120">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="299e5-121">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="299e5-121">Technologies</span></span>

-   [<span data-ttu-id="299e5-122">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="299e5-122">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="299e5-123">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="299e5-123">Prerequisites</span></span>

-   <span data-ttu-id="299e5-124">C/C++</span><span class="sxs-lookup"><span data-stu-id="299e5-124">C/C++</span></span>
-   <span data-ttu-id="299e5-125">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="299e5-125">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="299e5-126">Instruções</span><span class="sxs-lookup"><span data-stu-id="299e5-126">Instructions</span></span>

### <a name="implement-balloon-tooltips"></a><span data-ttu-id="299e5-127">Implementar dicas de ferramentas de balão</span><span class="sxs-lookup"><span data-stu-id="299e5-127">Implement Balloon Tooltips</span></span>

<span data-ttu-id="299e5-128">O código de exemplo a seguir mostra como implementar uma dica de ferramenta de balão centralizado usando o estilo de controle ToolTip de **\_ balão de TTS** .</span><span class="sxs-lookup"><span data-stu-id="299e5-128">The following example code shows how to implement a centered balloon tooltip by using the **TTS\_BALLOON** tooltip control style.</span></span>


```C++
hwndToolTips = CreateWindow(TOOLTIPS_CLASS, NULL, 
                            WS_POPUP | TTS_NOPREFIX | TTS_BALLOON, 
                            0, 0, 0, 0, NULL, NULL, g_hinst, NULL);

if (hwndTooltip)
{
    TOOLINFO ti;

    ti.cbSize   = sizeof(ti);
    ti.uFlags   = TTF_TRANSPARENT | TTF_CENTERTIP;
    ti.hwnd     = hwnd;
    ti.uId      = 0;
    ti.hinst    = NULL;
    ti.lpszText = LPSTR_TEXTCALLBACK;

    GetClientRect(hwnd, &ti.rect);

    SendMessage(hwndToolTips, TTM_ADDTOOL, 0, (LPARAM) &ti );

}
            
```



## <a name="related-topics"></a><span data-ttu-id="299e5-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="299e5-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="299e5-130">Usando controles de dica de ferramenta</span><span class="sxs-lookup"><span data-stu-id="299e5-130">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> <dt>

[<span data-ttu-id="299e5-131">**Estilos de dica de ferramenta**</span><span class="sxs-lookup"><span data-stu-id="299e5-131">**Tooltip Styles**</span></span>](tooltip-styles.md)
</dt> </dl>

 

 




