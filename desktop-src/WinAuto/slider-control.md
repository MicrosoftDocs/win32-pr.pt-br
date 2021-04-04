---
title: Controle Slider (referência de elemento de interface do usuário do MSAA)
description: Um controle deslizante, também chamado de controle TrackBar, permite que um usuário selecione um intervalo de valores movendo um controle deslizante. Os controles de volume no sistema operacional Windows são controles deslizantes.
ms.assetid: 8df4ed1d-d63c-49d7-94f1-df2113643484
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03c39d6638557b9dfff90740132d3e22a7e2511
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006090"
---
# <a name="slider-control-msaa-ui-element-reference"></a><span data-ttu-id="1d643-104">Controle Slider (referência de elemento de interface do usuário do MSAA)</span><span class="sxs-lookup"><span data-stu-id="1d643-104">Slider Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="1d643-105">Este tópico descreve os objetos de **controle Slider** para fins de referência de elemento da interface do usuário do MSAA.</span><span class="sxs-lookup"><span data-stu-id="1d643-105">This topic describes **Slider Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="1d643-106">Como criar objetos de **controle Slider** em várias estruturas de interface do usuário não é descrito aqui.</span><span class="sxs-lookup"><span data-stu-id="1d643-106">How to create **Slider Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="1d643-107">Consulte a documentação de referência da API para a estrutura de interface do usuário que você está usando.</span><span class="sxs-lookup"><span data-stu-id="1d643-107">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="1d643-108">Um controle deslizante, também chamado de controle TrackBar, permite que um usuário selecione um intervalo de valores movendo um controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="1d643-108">A slider control, also called a trackbar control, lets a user select from a range of values by moving a slider.</span></span> <span data-ttu-id="1d643-109">Os controles de volume no sistema operacional Windows são controles deslizantes.</span><span class="sxs-lookup"><span data-stu-id="1d643-109">The volume controls in the Windows operating system are slider controls.</span></span>

<span data-ttu-id="1d643-110">O nome da classe Window para um controle Slider é TRACKBAR \_ Class, que é definido como "msctls \_ TrackBar" em commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="1d643-110">The window class name for a slider control is TRACKBAR\_CLASS, which is defined as "msctls\_trackbar" in Commctrl.h.</span></span>

<span data-ttu-id="1d643-111">O conteúdo das propriedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) depende de o controle deslizante ser vertical ou horizontal e em quais das seguintes partes do controle deslizante é consultado pelo cliente:</span><span class="sxs-lookup"><span data-stu-id="1d643-111">The contents of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties depend on whether the slider is vertical or horizontal and on which of the following parts of the slider control is queried by the client:</span></span>

-   <span data-ttu-id="1d643-112">Janela de controle deslizante</span><span class="sxs-lookup"><span data-stu-id="1d643-112">Slider window</span></span>
-   <span data-ttu-id="1d643-113">Thumb Slider</span><span class="sxs-lookup"><span data-stu-id="1d643-113">Slider thumb</span></span>
-   <span data-ttu-id="1d643-114">Área sombreada acima (ou para</span><span class="sxs-lookup"><span data-stu-id="1d643-114">Shaded area above (or to</span></span>
-   <span data-ttu-id="1d643-115">Área sombreada abaixo (ou à direita) do controle deslizante</span><span class="sxs-lookup"><span data-stu-id="1d643-115">Shaded area below (or to the right of) the slider thumb</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="1d643-116">Métodos IAccessible</span><span class="sxs-lookup"><span data-stu-id="1d643-116">IAccessible Methods</span></span>

<span data-ttu-id="1d643-117">Um controle deslizante dá suporte aos seguintes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="1d643-117">A slider control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="1d643-118">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="1d643-118">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="1d643-119">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="1d643-119">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="1d643-120">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="1d643-120">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="1d643-121">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="1d643-121">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="1d643-122">Propriedades de IAccessible</span><span class="sxs-lookup"><span data-stu-id="1d643-122">IAccessible Properties</span></span>

<span data-ttu-id="1d643-123">Um controle deslizante dá suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="1d643-123">A slider control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>

-   [<span data-ttu-id="1d643-124">**obter \_ accChild**</span><span class="sxs-lookup"><span data-stu-id="1d643-124">**get\_accChild**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)
-   [<span data-ttu-id="1d643-125">**obter \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="1d643-125">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)
-   [<span data-ttu-id="1d643-126">**obter \_ accDescription**</span><span class="sxs-lookup"><span data-stu-id="1d643-126">**get\_accDescription**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)
-   [<span data-ttu-id="1d643-127">**obter \_ accHelp**</span><span class="sxs-lookup"><span data-stu-id="1d643-127">**get\_accHelp**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [<span data-ttu-id="1d643-128">**obter \_ accHelpTopic**</span><span class="sxs-lookup"><span data-stu-id="1d643-128">**get\_accHelpTopic**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   <span data-ttu-id="1d643-129">[**Get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut)— a propriedade **KeyboardShortcut** é a chave de acesso da janela de controle deslizante, que é um caractere sublinhado no texto do rótulo do controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="1d643-129">[**get\_accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut)—The **KeyboardShortcut** property is the slider window's access key, which is an underlined character in the text of the label for the slider.</span></span> <span data-ttu-id="1d643-130">A cadeia de caracteres retornada contém o caractere de chave de acesso anexado à cadeia de caracteres "Alt +".</span><span class="sxs-lookup"><span data-stu-id="1d643-130">The returned string contains the access key character appended to the string "Alt+".</span></span>
-   <span data-ttu-id="1d643-131">[**Get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)— a propriedade **Name** depende da parte do controle deslizante que é consultado.</span><span class="sxs-lookup"><span data-stu-id="1d643-131">[**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)—The **Name** property depends on the part of the slider that is queried.</span></span>

    <span data-ttu-id="1d643-132">As partes de um controle deslizante vertical têm os seguintes nomes:</span><span class="sxs-lookup"><span data-stu-id="1d643-132">The parts of a vertical slider have the following names:</span></span>

    

    | <span data-ttu-id="1d643-133">Parte do controle deslizante</span><span class="sxs-lookup"><span data-stu-id="1d643-133">Slider part</span></span>                    | <span data-ttu-id="1d643-134">Nome</span><span class="sxs-lookup"><span data-stu-id="1d643-134">Name</span></span>                                |
    |--------------------------------|-------------------------------------|
    | <span data-ttu-id="1d643-135">Janela de controle deslizante</span><span class="sxs-lookup"><span data-stu-id="1d643-135">Slider window</span></span>                  | <span data-ttu-id="1d643-136">Controle de texto estático usado como um rótulo</span><span class="sxs-lookup"><span data-stu-id="1d643-136">Static text control used as a label</span></span> |
    | <span data-ttu-id="1d643-137">Thumb Slider</span><span class="sxs-lookup"><span data-stu-id="1d643-137">Slider thumb</span></span>                   | <span data-ttu-id="1d643-138">Propostas</span><span class="sxs-lookup"><span data-stu-id="1d643-138">"Position"</span></span>                          |
    | <span data-ttu-id="1d643-139">Área sombreada acima do controle deslizante</span><span class="sxs-lookup"><span data-stu-id="1d643-139">Shaded area above slider thumb</span></span> | <span data-ttu-id="1d643-140">"Page Up"</span><span class="sxs-lookup"><span data-stu-id="1d643-140">"Page up"</span></span>                           |
    | <span data-ttu-id="1d643-141">Área sombreada abaixo do controle deslizante</span><span class="sxs-lookup"><span data-stu-id="1d643-141">Shaded area below slider thumb</span></span> | <span data-ttu-id="1d643-142">"Page Down"</span><span class="sxs-lookup"><span data-stu-id="1d643-142">"Page down"</span></span>                         |

    

     

    <span data-ttu-id="1d643-143">As partes de um controle deslizante horizontal têm os seguintes nomes:</span><span class="sxs-lookup"><span data-stu-id="1d643-143">The parts of a horizontal slider have the following names:</span></span>

    

    | <span data-ttu-id="1d643-144">Parte do controle deslizante</span><span class="sxs-lookup"><span data-stu-id="1d643-144">Slider part</span></span>                              | <span data-ttu-id="1d643-145">Nome</span><span class="sxs-lookup"><span data-stu-id="1d643-145">Name</span></span>                                |
    |------------------------------------------|-------------------------------------|
    | <span data-ttu-id="1d643-146">Janela de controle deslizante</span><span class="sxs-lookup"><span data-stu-id="1d643-146">Slider window</span></span>                            | <span data-ttu-id="1d643-147">Controle de texto estático usado como um rótulo</span><span class="sxs-lookup"><span data-stu-id="1d643-147">Static text control used as a label</span></span> |
    | <span data-ttu-id="1d643-148">Thumb Slider</span><span class="sxs-lookup"><span data-stu-id="1d643-148">Slider thumb</span></span>                             | <span data-ttu-id="1d643-149">Propostas</span><span class="sxs-lookup"><span data-stu-id="1d643-149">"Position"</span></span>                          |
    | <span data-ttu-id="1d643-150">Área sombreada à esquerda do controle deslizante Thumb</span><span class="sxs-lookup"><span data-stu-id="1d643-150">Shaded area to the left of slider thumb</span></span>  | <span data-ttu-id="1d643-151">"Página à esquerda"</span><span class="sxs-lookup"><span data-stu-id="1d643-151">"Page left"</span></span>                         |
    | <span data-ttu-id="1d643-152">Área sombreada à direita do controle deslizante</span><span class="sxs-lookup"><span data-stu-id="1d643-152">Shaded area to the right of slider thumb</span></span> | <span data-ttu-id="1d643-153">"Direita da página"</span><span class="sxs-lookup"><span data-stu-id="1d643-153">"Page right"</span></span>                        |

    

     

-   <span data-ttu-id="1d643-154">[**Get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)— a propriedade **Parent** dos botões de seta, scroll Thumb e a área sombreada em ambos os lados do Thumb é a janela Slider.</span><span class="sxs-lookup"><span data-stu-id="1d643-154">[**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)—The **Parent** property of the arrow buttons, scroll thumb, and the shaded area on either side of the thumb is the slider window.</span></span> <span data-ttu-id="1d643-155">A propriedade **Parent** da janela Slider é uma janela ( [**\_ \_ janela do sistema de funções**](object-roles.md) ) que envolve o controle e tem a mesma propriedade de **nome** e nome de classe de janela.</span><span class="sxs-lookup"><span data-stu-id="1d643-155">The **Parent** property of the slider window is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name.</span></span>
-   <span data-ttu-id="1d643-156">[**Get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)— a propriedade **role** depende da parte do controle deslizante que é consultado.</span><span class="sxs-lookup"><span data-stu-id="1d643-156">[**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)—The **Role** property depends on the part of the slider that is queried.</span></span> 

    | <span data-ttu-id="1d643-157">Parte do controle deslizante</span><span class="sxs-lookup"><span data-stu-id="1d643-157">Slider part</span></span>                                     | [<span data-ttu-id="1d643-158">Função</span><span class="sxs-lookup"><span data-stu-id="1d643-158">Role</span></span>](object-roles.md)                                                |
    |-------------------------------------------------|-------------------------------------------------------------------------|
    | <span data-ttu-id="1d643-159">Janela de controle deslizante</span><span class="sxs-lookup"><span data-stu-id="1d643-159">Slider window</span></span>                                   | [<span data-ttu-id="1d643-160">**\_controle deslizante do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="1d643-160">**ROLE\_SYSTEM\_SLIDER**</span></span>](object-roles.md)         |
    | <span data-ttu-id="1d643-161">Thumb Slider</span><span class="sxs-lookup"><span data-stu-id="1d643-161">Slider thumb</span></span>                                    | [<span data-ttu-id="1d643-162">**\_indicador do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="1d643-162">**ROLE\_SYSTEM\_INDICATOR**</span></span>](object-roles.md)   |
    | <span data-ttu-id="1d643-163">Áreas sombreadas em qualquer lado do controle deslizante</span><span class="sxs-lookup"><span data-stu-id="1d643-163">Shaded areas on either side of the slider thumb</span></span> | [<span data-ttu-id="1d643-164">**\_pressão do sistema de funções \_**</span><span class="sxs-lookup"><span data-stu-id="1d643-164">**ROLE\_SYSTEM\_PUSHBUTTON**</span></span>](object-roles.md) |

    

     

-   <span data-ttu-id="1d643-165">[**Get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)— os [valores](object-state-constants.md) para a propriedade **State** dependem da parte do controle deslizante que é consultado.</span><span class="sxs-lookup"><span data-stu-id="1d643-165">[**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)—[Values](object-state-constants.md) for the **State** property depend on the part of the slider that is queried.</span></span> 

    | <span data-ttu-id="1d643-166">Parte do controle deslizante</span><span class="sxs-lookup"><span data-stu-id="1d643-166">Slider Part</span></span>                                     | <span data-ttu-id="1d643-167">Valores de estado possíveis</span><span class="sxs-lookup"><span data-stu-id="1d643-167">Possible state values</span></span>                                                                                                                                                                                                                                                                                                                                                                                                           |
    |-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="1d643-168">Janela de controle deslizante</span><span class="sxs-lookup"><span data-stu-id="1d643-168">Slider window</span></span>                                   | <span data-ttu-id="1d643-169">[**Estado \_ sistema \_ invisível**](object-state-constants.md) sistema de estado \| [**\_ \_ indisponível**](object-state-constants.md) sistema de estado \| [**\_ \_ focalizado**](object-state-constants.md) sistema de \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) estado focado System normal</span><span class="sxs-lookup"><span data-stu-id="1d643-169">[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_NORMAL**](object-state-constants.md)</span></span> |
    | <span data-ttu-id="1d643-170">Thumb Slider</span><span class="sxs-lookup"><span data-stu-id="1d643-170">Slider thumb</span></span>                                    | <span data-ttu-id="1d643-171">Zero (0), o que significa que o objeto está visível ou estado sistema de estado [**\_ \_ invisível**](object-state-constants.md) sistema \| [**\_ \_ indisponível**](object-state-constants.md) sistema de estado \| [**\_ \_ normal**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="1d643-171">Zero (0), which means the object is visible, or [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_NORMAL**](object-state-constants.md)</span></span>                                                                                                                       |
    | <span data-ttu-id="1d643-172">Áreas sombreadas em qualquer lado do controle deslizante</span><span class="sxs-lookup"><span data-stu-id="1d643-172">Shaded areas on either side of the slider thumb</span></span> | <span data-ttu-id="1d643-173">Zero (0), o que significa que o objeto está visível ou estado sistema de estado [**\_ \_ invisível**](object-state-constants.md) sistema \| [**\_ \_ indisponível**](object-state-constants.md) sistema de estado \| [**\_ \_ normal**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="1d643-173">Zero (0), which means the object is visible, or [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_NORMAL**](object-state-constants.md)</span></span>                                                                                                                       |

    

     

-   <span data-ttu-id="1d643-174">[**Get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)— a propriedade **Value** da janela Slider indica a posição do Thumb e é uma cadeia de caracteres que contém um inteiro de "0" por meio de "100".</span><span class="sxs-lookup"><span data-stu-id="1d643-174">[**get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)—The **Value** property for the slider window indicates the position of the thumb and is a string that contains an integer from "0" through "100".</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d643-175">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1d643-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d643-176">Interface IAccessible</span><span class="sxs-lookup"><span data-stu-id="1d643-176">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[<span data-ttu-id="1d643-177">**Barra de rolagem**</span><span class="sxs-lookup"><span data-stu-id="1d643-177">**Scroll Bar**</span></span>](scroll-bar.md)
</dt> </dl>

 

 




