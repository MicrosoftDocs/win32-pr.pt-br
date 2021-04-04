---
title: Barra de rolagem (referência de elemento da interface do usuário do MSAA)
description: As barras de rolagem permitem que um usuário escolha a direção e a distância para rolar as informações em uma janela ou caixa de listagem relacionada. O nome da classe da janela para uma barra de rolagem é \ 0034; SCROLLBAR \ 0034;.
ms.assetid: a4ec1708-d751-4526-bd69-9796c43872a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df381e0d532991f164f2c17d0a261dd3c5006619
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008309"
---
# <a name="scroll-bar-msaa-ui-element-reference"></a><span data-ttu-id="b23da-104">Barra de rolagem (referência de elemento da interface do usuário do MSAA)</span><span class="sxs-lookup"><span data-stu-id="b23da-104">Scroll Bar (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="b23da-105">Este tópico descreve os objetos da **barra de rolagem** para fins de referência de elemento da interface do usuário do MSAA.</span><span class="sxs-lookup"><span data-stu-id="b23da-105">This topic describes **Scroll Bar** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="b23da-106">Como criar objetos de **barra de rolagem** em várias estruturas de interface do usuário não é descrito aqui.</span><span class="sxs-lookup"><span data-stu-id="b23da-106">How to create **Scroll Bar** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="b23da-107">Consulte a documentação de referência da API para a estrutura de interface do usuário que você está usando.</span><span class="sxs-lookup"><span data-stu-id="b23da-107">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="b23da-108">As barras de rolagem permitem que um usuário escolha a direção e a distância para rolar as informações em uma janela ou caixa de listagem relacionada.</span><span class="sxs-lookup"><span data-stu-id="b23da-108">Scroll bars let a user choose the direction and distance to scroll through information in a related window or list box.</span></span> <span data-ttu-id="b23da-109">O nome da classe da janela para uma barra de rolagem é "SCROLLBAR".</span><span class="sxs-lookup"><span data-stu-id="b23da-109">The window class name for a scroll bar is "SCROLLBAR".</span></span>

<span data-ttu-id="b23da-110">O conteúdo das propriedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) depende se a barra de rolagem é vertical ou horizontal e em quais das seguintes partes da barra de rolagem está sendo consultada pelo cliente:</span><span class="sxs-lookup"><span data-stu-id="b23da-110">The contents of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties depends on whether the scroll bar is vertical or horizontal and on which of the following parts of the scroll bar is being queried by the client:</span></span>

-   <span data-ttu-id="b23da-111">A barra de rolagem em si</span><span class="sxs-lookup"><span data-stu-id="b23da-111">The scroll bar itself</span></span>
-   <span data-ttu-id="b23da-112">O botão de seta superior ou direita</span><span class="sxs-lookup"><span data-stu-id="b23da-112">The top or right arrow button</span></span>
-   <span data-ttu-id="b23da-113">O botão de seta para baixo ou para a esquerda</span><span class="sxs-lookup"><span data-stu-id="b23da-113">The bottom or left arrow button</span></span>
-   <span data-ttu-id="b23da-114">A caixa de rolagem (Thumb)</span><span class="sxs-lookup"><span data-stu-id="b23da-114">The scroll box (thumb)</span></span>
-   <span data-ttu-id="b23da-115">A região Page Up ou direita da página</span><span class="sxs-lookup"><span data-stu-id="b23da-115">The page up or page right region</span></span>
-   <span data-ttu-id="b23da-116">A página para baixo ou a região esquerda da página</span><span class="sxs-lookup"><span data-stu-id="b23da-116">The page down or page left region</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="b23da-117">Métodos IAccessible</span><span class="sxs-lookup"><span data-stu-id="b23da-117">IAccessible Methods</span></span>

<span data-ttu-id="b23da-118">Uma barra de rolagem dá suporte aos seguintes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="b23da-118">A scroll bar supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   <span data-ttu-id="b23da-119">[**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)— o próprio objeto de barra de rolagem e o Thumb Scroll não dão suporte ao método **accDoDefaultAction** .</span><span class="sxs-lookup"><span data-stu-id="b23da-119">[**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)—The scroll bar object itself and the scroll thumb do not support the **accDoDefaultAction** method.</span></span>

    <span data-ttu-id="b23da-120">Para as outras partes da barra de rolagem em uma barra de rolagem vertical, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) [**chama a mensagem com**](/windows/desktop/api/winuser/nf-winuser-postmessagea) a mensagem [**\_ VSCROLL do WM**](/windows/desktop/Controls/wm-vscroll) com *wParam* definido com os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="b23da-120">For the other scroll bar parts on a vertical scroll bar, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) calls [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) with the [**WM\_VSCROLL**](/windows/desktop/Controls/wm-vscroll) message with *wParam* set to the following values.</span></span>

    

    | <span data-ttu-id="b23da-121">Botão/região</span><span class="sxs-lookup"><span data-stu-id="b23da-121">Button/Region</span></span>       | <span data-ttu-id="b23da-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b23da-122">Vaule</span></span>        |
    |---------------------|--------------|
    | <span data-ttu-id="b23da-123">Botão de seta superior</span><span class="sxs-lookup"><span data-stu-id="b23da-123">Top arrow button</span></span>    | <span data-ttu-id="b23da-124">linha de SB \_</span><span class="sxs-lookup"><span data-stu-id="b23da-124">SB\_LINEUP</span></span>   |
    | <span data-ttu-id="b23da-125">Botão de seta para baixo</span><span class="sxs-lookup"><span data-stu-id="b23da-125">Bottom arrow button</span></span> | <span data-ttu-id="b23da-126">SB \_ LINEDOWN</span><span class="sxs-lookup"><span data-stu-id="b23da-126">SB\_LINEDOWN</span></span> |
    | <span data-ttu-id="b23da-127">Região de página acima</span><span class="sxs-lookup"><span data-stu-id="b23da-127">Page up region</span></span>      | <span data-ttu-id="b23da-128">SB \_ PageUp</span><span class="sxs-lookup"><span data-stu-id="b23da-128">SB\_PAGEUP</span></span>   |
    | <span data-ttu-id="b23da-129">Região de página abaixo</span><span class="sxs-lookup"><span data-stu-id="b23da-129">Page down region</span></span>    | <span data-ttu-id="b23da-130">SB \_ PageDown</span><span class="sxs-lookup"><span data-stu-id="b23da-130">SB\_PAGEDOWN</span></span> |

    

     

    <span data-ttu-id="b23da-131">Para as outras partes da barra de rolagem em uma barra de rolagem horizontal, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) [**chama a mensagem com**](/windows/desktop/api/winuser/nf-winuser-postmessagea) a mensagem [**\_ HSCROLL do WM**](/windows/desktop/Controls/wm-hscroll) com *wParam* definido com os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="b23da-131">For the other scroll bar parts on a horizontal scroll bar, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) calls [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) with the [**WM\_HSCROLL**](/windows/desktop/Controls/wm-hscroll) message with *wParam* set to the following values.</span></span>

    

    | <span data-ttu-id="b23da-132">Botão/região</span><span class="sxs-lookup"><span data-stu-id="b23da-132">Button/Region</span></span>      | <span data-ttu-id="b23da-133">Valor</span><span class="sxs-lookup"><span data-stu-id="b23da-133">Value</span></span>         |
    |--------------------|---------------|
    | <span data-ttu-id="b23da-134">Botão de seta para a esquerda</span><span class="sxs-lookup"><span data-stu-id="b23da-134">Left arrow button</span></span>  | <span data-ttu-id="b23da-135">SB \_ LINELEFT</span><span class="sxs-lookup"><span data-stu-id="b23da-135">SB\_LINELEFT</span></span>  |
    | <span data-ttu-id="b23da-136">Botão de seta para direita</span><span class="sxs-lookup"><span data-stu-id="b23da-136">Right arrow button</span></span> | <span data-ttu-id="b23da-137">SB \_ LINERIGHT</span><span class="sxs-lookup"><span data-stu-id="b23da-137">SB\_LINERIGHT</span></span> |
    | <span data-ttu-id="b23da-138">Região esquerda da página</span><span class="sxs-lookup"><span data-stu-id="b23da-138">Page left region</span></span>   | <span data-ttu-id="b23da-139">SB \_ PAGELEFT</span><span class="sxs-lookup"><span data-stu-id="b23da-139">SB\_PAGELEFT</span></span>  |
    | <span data-ttu-id="b23da-140">Região direita da página</span><span class="sxs-lookup"><span data-stu-id="b23da-140">Page right region</span></span>  | <span data-ttu-id="b23da-141">SB \_ fixada</span><span class="sxs-lookup"><span data-stu-id="b23da-141">SB\_PAGERIGHT</span></span> |

    

     

-   [<span data-ttu-id="b23da-142">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="b23da-142">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="b23da-143">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="b23da-143">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="b23da-144">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="b23da-144">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a><span data-ttu-id="b23da-145">Propriedades de IAccessible</span><span class="sxs-lookup"><span data-stu-id="b23da-145">IAccessible Properties</span></span>

<span data-ttu-id="b23da-146">Uma barra de rolagem dá suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="b23da-146">A scroll bar supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>

-   <span data-ttu-id="b23da-147">[**Get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)— a propriedade **ChildCount** para o objeto da barra de rolagem é cinco.</span><span class="sxs-lookup"><span data-stu-id="b23da-147">[**get\_accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)—The **ChildCount** property for the scroll bar object is five.</span></span> <span data-ttu-id="b23da-148">Para as outras partes da barra de rolagem, a propriedade **ChildCount** é zero.</span><span class="sxs-lookup"><span data-stu-id="b23da-148">For the other scroll bar parts, the **ChildCount** property is zero.</span></span>
-   <span data-ttu-id="b23da-149">[**obter \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)– o próprio objeto de barra de rolagem e o Thumb Scroll não dão suporte à propriedade **DefaultAction** .</span><span class="sxs-lookup"><span data-stu-id="b23da-149">[**get\_accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)—The scroll bar object itself and the scroll thumb do not support the **DefaultAction** property.</span></span> <span data-ttu-id="b23da-150">A propriedade **DefaultAction** para os botões de seta e as áreas sombreadas em ambos os lados do polegar Thumb é "pressionar".</span><span class="sxs-lookup"><span data-stu-id="b23da-150">The **DefaultAction** property for the arrow buttons and the shaded areas on either side of the scroll thumb is "Press".</span></span>
-   <span data-ttu-id="b23da-151">[**Get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)— a propriedade **Description** depende da parte da barra de rolagem que é consultada.</span><span class="sxs-lookup"><span data-stu-id="b23da-151">[**get\_accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)—The **Description** property depends on the part of the scroll bar that is queried.</span></span>

    <span data-ttu-id="b23da-152">As partes de uma barra de rolagem vertical têm as seguintes descrições.</span><span class="sxs-lookup"><span data-stu-id="b23da-152">The parts of a vertical scroll bar have the following descriptions.</span></span>

    

    | <span data-ttu-id="b23da-153">Parte</span><span class="sxs-lookup"><span data-stu-id="b23da-153">Part</span></span>                | <span data-ttu-id="b23da-154">Descrição</span><span class="sxs-lookup"><span data-stu-id="b23da-154">Description</span></span>                                                                         |
    |---------------------|-------------------------------------------------------------------------------------|
    | <span data-ttu-id="b23da-155">Barra de rolagem em si</span><span class="sxs-lookup"><span data-stu-id="b23da-155">Scroll bar itself</span></span>   | <span data-ttu-id="b23da-156">"Usado para alterar a área de exibição vertical"</span><span class="sxs-lookup"><span data-stu-id="b23da-156">"Used to change the vertical viewing area"</span></span>                                          |
    | <span data-ttu-id="b23da-157">Botão de seta superior</span><span class="sxs-lookup"><span data-stu-id="b23da-157">Top arrow button</span></span>    | <span data-ttu-id="b23da-158">"Move a posição vertical uma linha acima"</span><span class="sxs-lookup"><span data-stu-id="b23da-158">"Moves the vertical position up one line"</span></span>                                           |
    | <span data-ttu-id="b23da-159">Botão de seta para baixo</span><span class="sxs-lookup"><span data-stu-id="b23da-159">Bottom arrow button</span></span> | <span data-ttu-id="b23da-160">"Move a posição vertical uma linha abaixo"</span><span class="sxs-lookup"><span data-stu-id="b23da-160">"Moves the vertical position down one line"</span></span>                                         |
    | <span data-ttu-id="b23da-161">Rolar o polegar</span><span class="sxs-lookup"><span data-stu-id="b23da-161">Scroll thumb</span></span>        | <span data-ttu-id="b23da-162">"Indica a posição vertical atual e pode ser arrastado para alterá-la diretamente"</span><span class="sxs-lookup"><span data-stu-id="b23da-162">"Indicates the current vertical position, and can be dragged to change it directly"</span></span> |
    | <span data-ttu-id="b23da-163">Região de página acima</span><span class="sxs-lookup"><span data-stu-id="b23da-163">Page up region</span></span>      | <span data-ttu-id="b23da-164">"Move a posição vertical para cima em duas linhas"</span><span class="sxs-lookup"><span data-stu-id="b23da-164">"Moves the vertical position up a couple of lines"</span></span>                                  |
    | <span data-ttu-id="b23da-165">Região de página abaixo</span><span class="sxs-lookup"><span data-stu-id="b23da-165">Page down region</span></span>    | <span data-ttu-id="b23da-166">"Indica a posição vertical atual e pode ser arrastado para alterá-la diretamente"</span><span class="sxs-lookup"><span data-stu-id="b23da-166">"Indicates the current vertical position, and can be dragged to change it directly"</span></span> |

    

     

    <span data-ttu-id="b23da-167">As partes de uma barra de rolagem horizontal têm as seguintes descrições.</span><span class="sxs-lookup"><span data-stu-id="b23da-167">The parts of a horizontal scroll bar have the following descriptions.</span></span>

    

    | <span data-ttu-id="b23da-168">Parte</span><span class="sxs-lookup"><span data-stu-id="b23da-168">Part</span></span>               | <span data-ttu-id="b23da-169">Descrição</span><span class="sxs-lookup"><span data-stu-id="b23da-169">Description</span></span>                                                                           |
    |--------------------|---------------------------------------------------------------------------------------|
    | <span data-ttu-id="b23da-170">Barra de rolagem em si</span><span class="sxs-lookup"><span data-stu-id="b23da-170">Scroll bar itself</span></span>  | <span data-ttu-id="b23da-171">"Usado para alterar a área de exibição horizontal"</span><span class="sxs-lookup"><span data-stu-id="b23da-171">"Used to change the horizontal viewing area"</span></span>                                          |
    | <span data-ttu-id="b23da-172">Botão de seta para a esquerda</span><span class="sxs-lookup"><span data-stu-id="b23da-172">Left arrow button</span></span>  | <span data-ttu-id="b23da-173">"Move a posição horizontal uma coluna para a esquerda"</span><span class="sxs-lookup"><span data-stu-id="b23da-173">"Moves the horizontal position left one column"</span></span>                                       |
    | <span data-ttu-id="b23da-174">Botão de seta para direita</span><span class="sxs-lookup"><span data-stu-id="b23da-174">Right arrow button</span></span> | <span data-ttu-id="b23da-175">' Move a posição horizontal uma coluna à direita "</span><span class="sxs-lookup"><span data-stu-id="b23da-175">'Moves the horizontal position right one column"</span></span>                                      |
    | <span data-ttu-id="b23da-176">Rolar o polegar</span><span class="sxs-lookup"><span data-stu-id="b23da-176">Scroll thumb</span></span>       | <span data-ttu-id="b23da-177">"Indica a posição horizontal atual e pode ser arrastada para alterá-la diretamente"</span><span class="sxs-lookup"><span data-stu-id="b23da-177">"Indicates the current horizontal position, and can be dragged to change it directly"</span></span> |
    | <span data-ttu-id="b23da-178">Região esquerda da página</span><span class="sxs-lookup"><span data-stu-id="b23da-178">Page left region</span></span>   | <span data-ttu-id="b23da-179">"Move a posição horizontal para a esquerda de duas colunas"</span><span class="sxs-lookup"><span data-stu-id="b23da-179">"Moves the horizontal position left a couple of columns"</span></span>                              |
    | <span data-ttu-id="b23da-180">Região direita da página</span><span class="sxs-lookup"><span data-stu-id="b23da-180">Page right region</span></span>  | <span data-ttu-id="b23da-181">"Indica a posição vertical atual e pode ser arrastado para alterá-la diretamente"</span><span class="sxs-lookup"><span data-stu-id="b23da-181">"Indicates the current vertical position, and can be dragged to change it directly"</span></span>   |

    

     

-   [<span data-ttu-id="b23da-182">**obter \_ accHelp**</span><span class="sxs-lookup"><span data-stu-id="b23da-182">**get\_accHelp**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [<span data-ttu-id="b23da-183">**obter \_ accHelpTopic**</span><span class="sxs-lookup"><span data-stu-id="b23da-183">**get\_accHelpTopic**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   <span data-ttu-id="b23da-184">[**Get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)— a propriedade **Name** depende da parte da barra de rolagem que é consultada.</span><span class="sxs-lookup"><span data-stu-id="b23da-184">[**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)—The **Name** property depends on the part of the scroll bar that is queried.</span></span>

    <span data-ttu-id="b23da-185">As partes de uma barra de rolagem vertical têm os nomes a seguir.</span><span class="sxs-lookup"><span data-stu-id="b23da-185">The parts of a vertical scroll bar have the following names.</span></span>

    | <span data-ttu-id="b23da-186">Parte</span><span class="sxs-lookup"><span data-stu-id="b23da-186">Part</span></span>                | <span data-ttu-id="b23da-187">Nome</span><span class="sxs-lookup"><span data-stu-id="b23da-187">Name</span></span>        |
    |---------------------|-------------|
    | <span data-ttu-id="b23da-188">Janela de barra de rolagem</span><span class="sxs-lookup"><span data-stu-id="b23da-188">Scroll bar window</span></span>   | <span data-ttu-id="b23da-189">Vertical</span><span class="sxs-lookup"><span data-stu-id="b23da-189">"Vertical"</span></span>  |
    | <span data-ttu-id="b23da-190">Botão de seta superior</span><span class="sxs-lookup"><span data-stu-id="b23da-190">Top arrow button</span></span>    | <span data-ttu-id="b23da-191">"Alinhar"</span><span class="sxs-lookup"><span data-stu-id="b23da-191">"Line up"</span></span>   |
    | <span data-ttu-id="b23da-192">Botão de seta para baixo</span><span class="sxs-lookup"><span data-stu-id="b23da-192">Bottom arrow button</span></span> | <span data-ttu-id="b23da-193">"Linha abaixo"</span><span class="sxs-lookup"><span data-stu-id="b23da-193">"Line down"</span></span> |
    | <span data-ttu-id="b23da-194">Rolar o polegar</span><span class="sxs-lookup"><span data-stu-id="b23da-194">Scroll thumb</span></span>        | <span data-ttu-id="b23da-195">Propostas</span><span class="sxs-lookup"><span data-stu-id="b23da-195">"Position"</span></span>  |
    | <span data-ttu-id="b23da-196">Região de página acima</span><span class="sxs-lookup"><span data-stu-id="b23da-196">Page up region</span></span>      | <span data-ttu-id="b23da-197">"Page Up"</span><span class="sxs-lookup"><span data-stu-id="b23da-197">"Page up"</span></span>   |
    | <span data-ttu-id="b23da-198">Região de página abaixo</span><span class="sxs-lookup"><span data-stu-id="b23da-198">Page down region</span></span>    | <span data-ttu-id="b23da-199">"Page Down"</span><span class="sxs-lookup"><span data-stu-id="b23da-199">"Page down"</span></span> |

    

     

    <span data-ttu-id="b23da-200">As partes de uma barra de rolagem horizontal têm os nomes a seguir.</span><span class="sxs-lookup"><span data-stu-id="b23da-200">The parts of a horizontal scroll bar have the following names.</span></span>

    

    | <span data-ttu-id="b23da-201">Parte</span><span class="sxs-lookup"><span data-stu-id="b23da-201">Part</span></span>               | <span data-ttu-id="b23da-202">Nome</span><span class="sxs-lookup"><span data-stu-id="b23da-202">Name</span></span>           |
    |--------------------|----------------|
    | <span data-ttu-id="b23da-203">Janela de barra de rolagem</span><span class="sxs-lookup"><span data-stu-id="b23da-203">Scroll bar window</span></span>  | <span data-ttu-id="b23da-204">Na</span><span class="sxs-lookup"><span data-stu-id="b23da-204">"Horizontal"</span></span>   |
    | <span data-ttu-id="b23da-205">Botão de seta para a esquerda</span><span class="sxs-lookup"><span data-stu-id="b23da-205">Left arrow button</span></span>  | <span data-ttu-id="b23da-206">"Coluna à esquerda"</span><span class="sxs-lookup"><span data-stu-id="b23da-206">"Column left"</span></span>  |
    | <span data-ttu-id="b23da-207">Botão de seta para direita</span><span class="sxs-lookup"><span data-stu-id="b23da-207">Right arrow button</span></span> | <span data-ttu-id="b23da-208">"Coluna à direita"</span><span class="sxs-lookup"><span data-stu-id="b23da-208">"Column right"</span></span> |
    | <span data-ttu-id="b23da-209">Rolar o polegar</span><span class="sxs-lookup"><span data-stu-id="b23da-209">Scroll thumb</span></span>       | <span data-ttu-id="b23da-210">Propostas</span><span class="sxs-lookup"><span data-stu-id="b23da-210">"Position"</span></span>     |
    | <span data-ttu-id="b23da-211">Região direita da página</span><span class="sxs-lookup"><span data-stu-id="b23da-211">Page right region</span></span>  | <span data-ttu-id="b23da-212">"Direita da página"</span><span class="sxs-lookup"><span data-stu-id="b23da-212">"Page right"</span></span>   |
    | <span data-ttu-id="b23da-213">Região esquerda da página</span><span class="sxs-lookup"><span data-stu-id="b23da-213">Page left region</span></span>   | <span data-ttu-id="b23da-214">"Página à esquerda"</span><span class="sxs-lookup"><span data-stu-id="b23da-214">"Page left"</span></span>    |

    

     

-   <span data-ttu-id="b23da-215">[**Get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)— a propriedade **Parent** dos botões de seta, scroll Thumb e a área sombreada em qualquer lado do Thumb é a janela da barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="b23da-215">[**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)—The **Parent** property of the arrow buttons, scroll thumb, and the shaded area on either side of the thumb is the scroll bar window.</span></span> <span data-ttu-id="b23da-216">A propriedade **Parent** da janela da barra de rolagem é uma janela (janela do sistema de funções \_ \_ ) que envolve o controle e tem a mesma propriedade de **nome** e nome de classe de janela.</span><span class="sxs-lookup"><span data-stu-id="b23da-216">The **Parent** property of the scroll bar window is a window (ROLE\_SYSTEM\_WINDOW) that surrounds the control and has the same **Name** property and window class name.</span></span>
-   <span data-ttu-id="b23da-217">[**obter \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)– a propriedade de **função** depende da parte da barra de rolagem que é consultada.</span><span class="sxs-lookup"><span data-stu-id="b23da-217">[**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)—The **Role** property depends on the part of the scroll bar that is queried.</span></span> <span data-ttu-id="b23da-218">As partes de uma barra de rolagem têm as seguintes funções.</span><span class="sxs-lookup"><span data-stu-id="b23da-218">The parts of a scroll bar have the following roles.</span></span> 

    | <span data-ttu-id="b23da-219">Parte</span><span class="sxs-lookup"><span data-stu-id="b23da-219">Part</span></span>                                                  | <span data-ttu-id="b23da-220">Função</span><span class="sxs-lookup"><span data-stu-id="b23da-220">Role</span></span>                                                                    |
    |-------------------------------------------------------|-------------------------------------------------------------------------|
    | <span data-ttu-id="b23da-221">Barra de rolagem em si</span><span class="sxs-lookup"><span data-stu-id="b23da-221">Scroll bar itself</span></span>                                     | [<span data-ttu-id="b23da-222">**\_barra de rolagem do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="b23da-222">**ROLE\_SYSTEM\_SCROLLBAR**</span></span>](object-roles.md)   |
    | <span data-ttu-id="b23da-223">Botões de seta superior, inferior, esquerdo e direito</span><span class="sxs-lookup"><span data-stu-id="b23da-223">Top, down, left, and right arrow buttons</span></span>              | [<span data-ttu-id="b23da-224">**\_pressão do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="b23da-224">**ROLE\_SYSTEM\_PUSHBUTTON**</span></span>](object-roles.md) |
    | <span data-ttu-id="b23da-225">Rolar o polegar</span><span class="sxs-lookup"><span data-stu-id="b23da-225">Scroll thumb</span></span>                                          | [<span data-ttu-id="b23da-226">**\_indicador do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="b23da-226">**ROLE\_SYSTEM\_INDICATOR**</span></span>](object-roles.md)   |
    | <span data-ttu-id="b23da-227">Páginas acima, Page Down, página à esquerda e à direita da página</span><span class="sxs-lookup"><span data-stu-id="b23da-227">Page up, page down, page left, and page right regions</span></span> | [<span data-ttu-id="b23da-228">**\_pressão do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="b23da-228">**ROLE\_SYSTEM\_PUSHBUTTON**</span></span>](object-roles.md) |

    

     

-   <span data-ttu-id="b23da-229">[**Get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)— a propriedade **State** de cada componente da barra de rolagem inclui uma combinação dos [valores](object-state-constants.md)a seguir.</span><span class="sxs-lookup"><span data-stu-id="b23da-229">[**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)—The **State** property of each scroll bar component includes a combination of the following [values](object-state-constants.md).</span></span>

    | <span data-ttu-id="b23da-230">Estado</span><span class="sxs-lookup"><span data-stu-id="b23da-230">State</span></span>                                                                                 | <span data-ttu-id="b23da-231">Valor</span><span class="sxs-lookup"><span data-stu-id="b23da-231">Value</span></span>                                                                                                                                                                                                                       |
    |---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [<span data-ttu-id="b23da-232">**sistema de estado \_ \_ invisível**</span><span class="sxs-lookup"><span data-stu-id="b23da-232">**STATE\_SYSTEM\_INVISIBLE**</span></span>](object-state-constants.md)     | <span data-ttu-id="b23da-233">Para a barra de rolagem, isso indica que a barra de rolagem vertical ou horizontal especificada não existe.</span><span class="sxs-lookup"><span data-stu-id="b23da-233">For the scroll bar itself, this indicates the specified vertical or horizontal scroll bar does not exist.</span></span> <span data-ttu-id="b23da-234">Para as regiões Page Up ou Page Down, isso indica que o Thumb está posicionado de modo que a região não exista.</span><span class="sxs-lookup"><span data-stu-id="b23da-234">For the page up or page down regions, this indicates the thumb is positioned such that the region does not exist.</span></span> |
    | [<span data-ttu-id="b23da-235">**Estado do \_ sistema \_ fora da tela**</span><span class="sxs-lookup"><span data-stu-id="b23da-235">**STATE\_SYSTEM\_OFFSCREEN**</span></span>](object-state-constants.md)     | <span data-ttu-id="b23da-236">Para a barra de rolagem, isso indica que a janela é dimensionada de modo que a barra de rolagem vertical ou horizontal especificada não seja exibida no momento.</span><span class="sxs-lookup"><span data-stu-id="b23da-236">For the scroll bar itself, this indicates the window is sized such that the specified vertical or horizontal scroll bar is not currently displayed.</span></span>                                                                         |
    | [<span data-ttu-id="b23da-237">**sistema de estado \_ \_ pressionado**</span><span class="sxs-lookup"><span data-stu-id="b23da-237">**STATE\_SYSTEM\_PRESSED**</span></span>](object-state-constants.md)         | <span data-ttu-id="b23da-238">O botão de seta ou a região da página é pressionado.</span><span class="sxs-lookup"><span data-stu-id="b23da-238">The arrow button or page region is pressed.</span></span>                                                                                                                                                                                 |
    | [<span data-ttu-id="b23da-239">**sistema de estado \_ \_ indisponível**</span><span class="sxs-lookup"><span data-stu-id="b23da-239">**STATE\_SYSTEM\_UNAVAILABLE**</span></span>](object-state-constants.md) | <span data-ttu-id="b23da-240">O componente está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="b23da-240">The component is disabled.</span></span>                                                                                                                                                                                                  |

    

     

-   <span data-ttu-id="b23da-241">[**Get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)— a propriedade **Value** da janela da barra de rolagem indica a posição da barra de rolagem e é uma cadeia de caracteres que contém um inteiro de "0" a "100".</span><span class="sxs-lookup"><span data-stu-id="b23da-241">[**get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)—The **Value** property for the scroll bar window indicates the scroll bar position and is a string that contains an integer from "0" through "100".</span></span>

## <a name="related-topics"></a><span data-ttu-id="b23da-242">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b23da-242">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b23da-243">Interface IAccessible</span><span class="sxs-lookup"><span data-stu-id="b23da-243">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 