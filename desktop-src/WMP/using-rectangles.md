---
title: Usando retângulos (SDK do Windows Media Player)
description: Usando retângulos
ms.assetid: b3fc16b4-dc93-43c0-a97d-5234e36437c8
keywords:
- visualizações, retângulos
- visualizações personalizadas, retângulos
- visualizações, função render
- visualizações personalizadas, função render
- Processar função, retângulos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b48f16888d8e71c052d216a838683f2b7127e75
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105791475"
---
# <a name="using-rectangles-windows-media-player-sdk"></a><span data-ttu-id="cf95e-108">Usando retângulos (SDK do Windows Media Player)</span><span class="sxs-lookup"><span data-stu-id="cf95e-108">Using Rectangles (Windows Media Player SDK)</span></span>

<span data-ttu-id="cf95e-109">Os retângulos são usados para especificar áreas retangulares no Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="cf95e-109">Rectangles are used to specify rectangular areas in Microsoft Windows.</span></span> <span data-ttu-id="cf95e-110">Você pode criar vários retângulos em sua janela, mas o Windows Media Player fornece os valores de um retângulo por meio da função [IWMPEffects:: render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) .</span><span class="sxs-lookup"><span data-stu-id="cf95e-110">You can create many rectangles in your window, but Windows Media Player supplies the values of one rectangle through the [IWMPEffects::Render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) function.</span></span> <span data-ttu-id="cf95e-111">Se o seu plug-in renderizar usando uma janela, o retângulo será a área do cliente da janela.</span><span class="sxs-lookup"><span data-stu-id="cf95e-111">If your plug-in renders using a window, the rectangle is the client area of the window.</span></span> <span data-ttu-id="cf95e-112">Isso é chamado de retângulo PRC e define o retângulo pelo qual o Windows Media Player exibirá sua visualização.</span><span class="sxs-lookup"><span data-stu-id="cf95e-112">This is called the prc rectangle, and it defines the rectangle that Windows Media Player will display your visualization through.</span></span> <span data-ttu-id="cf95e-113">Use isso frequentemente para ter certeza de que você não desenha além das extensões do retângulo fornecido pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="cf95e-113">Use this frequently to be sure you do not draw beyond the extents of the rectangle supplied by Windows Media Player.</span></span>

<span data-ttu-id="cf95e-114">Um retângulo tem quatro valores que o definem.</span><span class="sxs-lookup"><span data-stu-id="cf95e-114">A rectangle has four values that define it.</span></span> <span data-ttu-id="cf95e-115">Elas são esquerda, superior, direita e inferior.</span><span class="sxs-lookup"><span data-stu-id="cf95e-115">They are left, top, right, and bottom.</span></span> <span data-ttu-id="cf95e-116">O canto superior esquerdo do retângulo é definido pela esquerda e na parte superior, e o canto inferior direito do retângulo é definido pela parte inferior e direita.</span><span class="sxs-lookup"><span data-stu-id="cf95e-116">The top, left corner of the rectangle is defined by left and top, and the bottom, right corner of the rectangle is defined by bottom and right.</span></span>

<span data-ttu-id="cf95e-117">Use o código a seguir para obter as extensões do seu retângulo de desenho.</span><span class="sxs-lookup"><span data-stu-id="cf95e-117">Use the following code to get the extents of your drawing rectangle.</span></span> <span data-ttu-id="cf95e-118">Você precisa fazer isso porque o usuário pode redimensionar a janela e você deseja ter certeza de que está sempre desenhando em uma área que o usuário pode ver.</span><span class="sxs-lookup"><span data-stu-id="cf95e-118">You need to do this because the user may resize the window, and you want to be sure that you are always drawing in an area the user can see.</span></span>


```C++
int leftside = prc->left;
int rightside = prc->right;
int topside = prc->top;
int bottomside = prc->bottom;

```



<span data-ttu-id="cf95e-119">Por exemplo, para desenhar da esquerda para a direita, ao longo da parte superior da janela, use um código como este:</span><span class="sxs-lookup"><span data-stu-id="cf95e-119">For example, to draw from left to right, along the top of the window, use code like this:</span></span>


```C++
::MoveToEx( hdc, prc->left, prc->top, NULL );  
::LineTo(hdc, prc->right, prc->top);

```



## <a name="related-topics"></a><span data-ttu-id="cf95e-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cf95e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf95e-121">**Implementando renderização**</span><span class="sxs-lookup"><span data-stu-id="cf95e-121">**Implementing Render**</span></span>](implementing-render.md)
</dt> </dl>

 

 




