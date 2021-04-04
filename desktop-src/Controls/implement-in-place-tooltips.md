---
title: Como implementar dicas de ferramentas de In-Place
description: Dicas de ferramenta in-loco são usadas para exibir cadeias de caracteres de texto para objetos que foram recortados. Para obter uma ilustração, consulte sobre os controles de dica de ferramenta.
ms.assetid: 2FE39B99-75F3-4978-B0B3-B769E2961F23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc321ecdd6df151a151e6d21c8419326edb63d38
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104008626"
---
# <a name="how-to-implement-in-place-tooltips"></a><span data-ttu-id="81a31-104">Como implementar dicas de ferramentas de In-Place</span><span class="sxs-lookup"><span data-stu-id="81a31-104">How to Implement In-Place Tooltips</span></span>

<span data-ttu-id="81a31-105">Dicas de ferramenta in-loco são usadas para exibir cadeias de caracteres de texto para objetos que foram recortados.</span><span class="sxs-lookup"><span data-stu-id="81a31-105">In-place tooltips are used to display text strings for objects that have been clipped.</span></span> <span data-ttu-id="81a31-106">Para obter uma ilustração, consulte [sobre os controles de dica de ferramenta](tooltip-controls.md).</span><span class="sxs-lookup"><span data-stu-id="81a31-106">For an illustration, see [About Tooltip Controls](tooltip-controls.md).</span></span>

<span data-ttu-id="81a31-107">A diferença entre as dicas de ferramenta comuns e no local é o posicionamento.</span><span class="sxs-lookup"><span data-stu-id="81a31-107">The difference between ordinary and in-place tooltips is positioning.</span></span> <span data-ttu-id="81a31-108">Por padrão, quando o ponteiro do mouse passa sobre uma região que tem uma dica de ferramenta associada a ela, a dica de ferramenta é exibida adjacente à região.</span><span class="sxs-lookup"><span data-stu-id="81a31-108">By default, when the mouse pointer hovers over a region that has a tooltip associated with it, the tooltip is displayed adjacent to the region.</span></span> <span data-ttu-id="81a31-109">No entanto, as dicas de ferramentas são janelas e podem ser posicionadas em qualquer lugar que você escolher chamando [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span><span class="sxs-lookup"><span data-stu-id="81a31-109">However, tooltips are windows, and they can be positioned anywhere you choose by calling [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span></span> <span data-ttu-id="81a31-110">A criação de uma dica de ferramenta in-loco é uma questão de posicionar a janela de dica de ferramenta para que ela se sobreponha à cadeia de texto.</span><span class="sxs-lookup"><span data-stu-id="81a31-110">Creating an in-place tooltip is a matter of positioning the tooltip window so that it overlays the text string.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="81a31-111">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="81a31-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="81a31-112">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="81a31-112">Technologies</span></span>

-   [<span data-ttu-id="81a31-113">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="81a31-113">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="81a31-114">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="81a31-114">Prerequisites</span></span>

-   <span data-ttu-id="81a31-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="81a31-115">C/C++</span></span>
-   <span data-ttu-id="81a31-116">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="81a31-116">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="81a31-117">Instruções</span><span class="sxs-lookup"><span data-stu-id="81a31-117">Instructions</span></span>

### <a name="positioning-an-in-place-tooltip"></a><span data-ttu-id="81a31-118">Posicionando uma dica de ferramenta In-Place</span><span class="sxs-lookup"><span data-stu-id="81a31-118">Positioning an In-Place Tooltip</span></span>

<span data-ttu-id="81a31-119">Você precisa manter o controle de três retângulos ao posicionar uma dica de ferramenta in-loco:</span><span class="sxs-lookup"><span data-stu-id="81a31-119">You need to keep track of three rectangles when positioning an in-place tooltip:</span></span>

1.  <span data-ttu-id="81a31-120">O retângulo que circunda o texto do rótulo completo.</span><span class="sxs-lookup"><span data-stu-id="81a31-120">The rectangle that surrounds the complete label text.</span></span>
2.  <span data-ttu-id="81a31-121">O retângulo que circunda o texto da dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="81a31-121">The rectangle that surrounds the tooltip text.</span></span> <span data-ttu-id="81a31-122">O texto da dica de ferramenta é idêntico ao texto completo do rótulo e normalmente tem o mesmo tamanho e fonte.</span><span class="sxs-lookup"><span data-stu-id="81a31-122">The tooltip text is identical to the complete label text, and normally is the same size and font.</span></span> <span data-ttu-id="81a31-123">Portanto, os dois retângulos de texto geralmente terão o mesmo tamanho.</span><span class="sxs-lookup"><span data-stu-id="81a31-123">The two text rectangles will thus usually be the same size.</span></span>
3.  <span data-ttu-id="81a31-124">O retângulo da janela de dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="81a31-124">The tooltip window rectangle.</span></span> <span data-ttu-id="81a31-125">Esse retângulo é um pouco maior do que o retângulo de texto de dica de ferramenta que ele fecha.</span><span class="sxs-lookup"><span data-stu-id="81a31-125">This rectangle is somewhat larger than the tooltip text rectangle that it encloses.</span></span>


<span data-ttu-id="81a31-126">Os três retângulos são mostrados esquemáticomente na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="81a31-126">The three rectangles are shown schematically in the following illustration.</span></span> <span data-ttu-id="81a31-127">A parte oculta do texto do rótulo é indicada por um plano de fundo cinza.</span><span class="sxs-lookup"><span data-stu-id="81a31-127">The hidden portion of the label text is indicated by a gray background.</span></span>

![diagrama mostrando uma cadeia de caracteres longa, metade dela tem um plano de fundo cinza e, em seguida, a mesma cadeia de caracteres em um retângulo de janela de dica de ferramenta maior](images/inplace.png)

<span data-ttu-id="81a31-129">Para criar uma dica de ferramenta in-loco, você deve posicionar o retângulo de texto da dica de ferramenta para que ele se sobreponha ao retângulo do texto do rótulo.</span><span class="sxs-lookup"><span data-stu-id="81a31-129">To create an in-place tooltip, you must position the tooltip text rectangle so that it overlays the label text rectangle.</span></span> <span data-ttu-id="81a31-130">O procedimento para alinhar os dois retângulos é relativamente simples:</span><span class="sxs-lookup"><span data-stu-id="81a31-130">The procedure for aligning the two rectangles is relatively straightforward:</span></span>

1.  <span data-ttu-id="81a31-131">Defina o retângulo do texto do rótulo.</span><span class="sxs-lookup"><span data-stu-id="81a31-131">Define the label text rectangle.</span></span>
2.  <span data-ttu-id="81a31-132">Posicione a janela de dica de ferramenta para que o retângulo de texto de dica de ferramenta sobreponha o retângulo de texto do rótulo.</span><span class="sxs-lookup"><span data-stu-id="81a31-132">Position the tooltip window so that the tooltip text rectangle overlays the label text rectangle.</span></span>


<span data-ttu-id="81a31-133">Na prática, geralmente é suficiente alinhar o canto superior esquerdo dos dois retângulos de texto.</span><span class="sxs-lookup"><span data-stu-id="81a31-133">In practice, it is usually sufficient to align the upper-left corner of the two text rectangles.</span></span> <span data-ttu-id="81a31-134">A tentativa de redimensionar o retângulo de texto da dica de ferramenta para corresponder exatamente ao retângulo do texto do rótulo pode causar problemas com a exibição da dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="81a31-134">Attempting to resize the tooltip text rectangle to exactly match the label text rectangle could cause problems with the tooltip display.</span></span>

<span data-ttu-id="81a31-135">O problema com esse esquema simples é que você não pode posicionar o retângulo de texto de dica de ferramenta diretamente.</span><span class="sxs-lookup"><span data-stu-id="81a31-135">The problem with this simple scheme is that you cannot position the tooltip text rectangle directly.</span></span> <span data-ttu-id="81a31-136">Em vez disso, você deve posicionar o retângulo da janela de dica de ferramenta exatamente o suficiente acima e à esquerda do retângulo de texto do rótulo para que os cantos dos dois retângulos de texto coincidam.</span><span class="sxs-lookup"><span data-stu-id="81a31-136">Instead, you must position the tooltip window rectangle just far enough above and to the left of the label text rectangle so that the corners of the two text rectangles coincide.</span></span> <span data-ttu-id="81a31-137">Em outras palavras, você precisa saber o deslocamento entre o retângulo da janela de dica de ferramenta e seu retângulo de texto embutido.</span><span class="sxs-lookup"><span data-stu-id="81a31-137">In other words, you need to know the offset between the tooltip window rectangle and its enclosed text rectangle.</span></span> <span data-ttu-id="81a31-138">Em geral, não há uma maneira simples de determinar esse deslocamento.</span><span class="sxs-lookup"><span data-stu-id="81a31-138">In general, there is no simple way to determine this offset.</span></span>

### <a name="implement-in-place-tooltips"></a><span data-ttu-id="81a31-139">Implementar dicas de ferramentas de In-Place</span><span class="sxs-lookup"><span data-stu-id="81a31-139">Implement In-Place Tooltips</span></span>

<span data-ttu-id="81a31-140">O fragmento de código a seguir ilustra como usar uma mensagem [**TTM \_ ADJUSTRECT**](ttm-adjustrect.md) em um manipulador [TTN \_ show](ttn-show.md) para exibir uma dica de ferramenta in-loco.</span><span class="sxs-lookup"><span data-stu-id="81a31-140">The following code fragment illustrates how to use a [**TTM\_ADJUSTRECT**](ttm-adjustrect.md) message in a [TTN\_SHOW](ttn-show.md) handler to display an in-place tooltip.</span></span> <span data-ttu-id="81a31-141">Seu aplicativo indica que o texto do rótulo está truncado definindo a variável *fMyStringIsTruncated* privada como **true**.</span><span class="sxs-lookup"><span data-stu-id="81a31-141">Your application indicates that the label text is truncated by setting the private *fMyStringIsTruncated* variable to **TRUE**.</span></span> <span data-ttu-id="81a31-142">O manipulador chama uma função definida pelo aplicativo, **GetMyItemRect**, para recuperar o retângulo de texto do rótulo.</span><span class="sxs-lookup"><span data-stu-id="81a31-142">The handler calls an application-defined function, **GetMyItemRect**, to retrieve the label text rectangle.</span></span> <span data-ttu-id="81a31-143">Esse retângulo é passado para o controle ToolTip com **TTM \_ ADJUSTRECT**, que retorna o retângulo de janela correspondente.</span><span class="sxs-lookup"><span data-stu-id="81a31-143">This rectangle is passed to the tooltip control with **TTM\_ADJUSTRECT**, which returns the corresponding window rectangle.</span></span> <span data-ttu-id="81a31-144">Em seguida, [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) é chamado para posicionar a dica de ferramenta sobre o rótulo.</span><span class="sxs-lookup"><span data-stu-id="81a31-144">[**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) is then called to position the tooltip over the label.</span></span>


```C++
case TTN_SHOW:
            
    if (fMyStringIsTruncated) 
    {
        RECT rc;
        
        GetMyItemRect(&rc);
        
        SendMessage(hwndToolTip, TTM_ADJUSTRECT, TRUE, (LPARAM)&rc);
        
        SetWindowPos(hwndToolTip, NULL, rc.left, rc.top, 0, 0, 
                     SWP_NOSIZE | SWP_NOZORDER | SWP_NOACTIVATE);
    }
```



<span data-ttu-id="81a31-145">Este exemplo não altera o tamanho da dica de ferramenta, apenas sua posição.</span><span class="sxs-lookup"><span data-stu-id="81a31-145">This example does not change the size of the tooltip, just its position.</span></span> <span data-ttu-id="81a31-146">Os dois retângulos de texto estão alinhados em seus cantos superior esquerdo, mas não necessariamente com as mesmas dimensões.</span><span class="sxs-lookup"><span data-stu-id="81a31-146">The two text rectangles are aligned at their upper-left corners, but not necessarily with the same dimensions.</span></span> <span data-ttu-id="81a31-147">Na prática, a diferença é geralmente pequena e essa abordagem é recomendada para a maioria das finalidades.</span><span class="sxs-lookup"><span data-stu-id="81a31-147">In practice, the difference is usually small, and this approach is recommended for most purposes.</span></span> <span data-ttu-id="81a31-148">Embora você possa, em princípio, usar [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) para redimensionar e reposicionar a dica de ferramenta, fazer isso pode ter consequências imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="81a31-148">While you can, in principle, use [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) to resize as well as reposition the tooltip, doing so might have unpredictable consequences.</span></span>

## <a name="remarks"></a><span data-ttu-id="81a31-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="81a31-149">Remarks</span></span>

<span data-ttu-id="81a31-150">Os controles comuns [versão 5,80](common-control-versions.md) simplificam o uso de dicas de ferramenta in-loco pela adição de uma nova mensagem, [**TTM \_ ADJUSTRECT**](ttm-adjustrect.md).</span><span class="sxs-lookup"><span data-stu-id="81a31-150">Common controls [version 5.80](common-control-versions.md) simplifies the use of in-place tooltips by the addition of a new message, [**TTM\_ADJUSTRECT**](ttm-adjustrect.md).</span></span> <span data-ttu-id="81a31-151">Envie essa mensagem com as coordenadas do retângulo de texto do rótulo que você deseja que a dica de ferramenta sobreponha e retorne as coordenadas de um retângulo de janela de dica de ferramenta posicionado adequadamente.</span><span class="sxs-lookup"><span data-stu-id="81a31-151">Send this message with the coordinates of the label text rectangle that you want the tooltip to overlay, and it returns the coordinates of an appropriately positioned tooltip window rectangle.</span></span>

## <a name="related-topics"></a><span data-ttu-id="81a31-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="81a31-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81a31-153">Usando controles de dica de ferramenta</span><span class="sxs-lookup"><span data-stu-id="81a31-153">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 