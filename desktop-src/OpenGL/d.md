---
title: D (OpenGL)
description: Definições de termos OpenGL que começam com a letra D.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: f97470e7-a500-47d7-84f0-b3045d04b8fc
keywords:
- depth
- advertência de profundidade
- Exibir listas
- pontilhado
- buffer duplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97cb068f06135c6ba29e8a61f472d98907090a78
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103644149"
---
# <a name="d-opengl"></a><span data-ttu-id="bea37-108">D (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="bea37-108">D (OpenGL)</span></span>

<span data-ttu-id="bea37-109">[A](a.md) [B](b.md) [C](c.md) D [E](e.md) [F](f.md) [G](g.md) [H](h.md) [i](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="bea37-109">[A](a.md) [B](b.md) [C](c.md) D [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="bea37-110"><span id="opengl_depth"></span><span id="OPENGL_DEPTH"></span>**Detalhado**</span><span class="sxs-lookup"><span data-stu-id="bea37-110"><span id="opengl_depth"></span><span id="OPENGL_DEPTH"></span>**depth**</span></span>
</dt> <dd>

<span data-ttu-id="bea37-111">Geralmente refere-se à coordenada de janela z.</span><span class="sxs-lookup"><span data-stu-id="bea37-111">Generally refers to the z window coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="bea37-112"><span id="opengl_depth_cueing"></span><span id="OPENGL_DEPTH_CUEING"></span>**advertência de profundidade**</span><span class="sxs-lookup"><span data-stu-id="bea37-112"><span id="opengl_depth_cueing"></span><span id="OPENGL_DEPTH_CUEING"></span>**depth cueing**</span></span>
</dt> <dd>

<span data-ttu-id="bea37-113">Uma técnica de renderização que atribui cor com base na distância do ponto de vista.</span><span class="sxs-lookup"><span data-stu-id="bea37-113">A rendering technique that assigns color based on distance from the viewpoint.</span></span>

</dd> <dt>

<span data-ttu-id="bea37-114"><span id="opengl_display_list"></span><span id="OPENGL_DISPLAY_LIST"></span>**lista de exibição**</span><span class="sxs-lookup"><span data-stu-id="bea37-114"><span id="opengl_display_list"></span><span id="OPENGL_DISPLAY_LIST"></span>**display list**</span></span>
</dt> <dd>

<span data-ttu-id="bea37-115">Uma lista nomeada de comandos OpenGL.</span><span class="sxs-lookup"><span data-stu-id="bea37-115">A named list of OpenGL commands.</span></span> <span data-ttu-id="bea37-116">As listas de exibição são sempre armazenadas no servidor, portanto, as listas de exibição podem ser usadas para reduzir o tráfego de rede em ambientes de cliente/servidor.</span><span class="sxs-lookup"><span data-stu-id="bea37-116">Display lists are always stored on the server, so display lists can be used to reduce the network traffic in client/server environments.</span></span> <span data-ttu-id="bea37-117">O conteúdo de uma lista de exibição pode ser pré-processado e, portanto, pode ser executado com mais eficiência do que o mesmo conjunto de comandos OpenGL executados no modo imediato.</span><span class="sxs-lookup"><span data-stu-id="bea37-117">The contents of a display list may be preprocessed, and might therefore execute more efficiently than the same set of OpenGL commands executed in immediate mode.</span></span> <span data-ttu-id="bea37-118">Esse pré-processamento é especialmente importante para a computação de comandos intensivos, como [**glTexImage**](glteximage1d.md).</span><span class="sxs-lookup"><span data-stu-id="bea37-118">Such preprocessing is especially important for computing intensive commands such as [**glTexImage**](glteximage1d.md).</span></span>

</dd> <dt>

<span data-ttu-id="bea37-119"><span id="opengl_dithering"></span><span id="OPENGL_DITHERING"></span>**pontilhado**</span><span class="sxs-lookup"><span data-stu-id="bea37-119"><span id="opengl_dithering"></span><span id="OPENGL_DITHERING"></span>**dithering**</span></span>
</dt> <dd>

<span data-ttu-id="bea37-120">Uma técnica para aumentar o intervalo percebido de cores em uma imagem no custo da resolução espacial.</span><span class="sxs-lookup"><span data-stu-id="bea37-120">A technique for increasing the perceived range of colors in an image at the cost of spatial resolution.</span></span> <span data-ttu-id="bea37-121">Os pixels adjacentes são atribuídos a valores de cor diferentes.</span><span class="sxs-lookup"><span data-stu-id="bea37-121">Adjacent pixels are assigned differing color values.</span></span> <span data-ttu-id="bea37-122">Quando visualizados de uma distância, essas cores parecem misturar em uma única cor intermediária.</span><span class="sxs-lookup"><span data-stu-id="bea37-122">When viewed from a distance, these colors seem to blend into a single intermediate color.</span></span> <span data-ttu-id="bea37-123">A técnica é semelhante ao meio-Toning usado em publicações em preto e branco para obter sombras de cinza.</span><span class="sxs-lookup"><span data-stu-id="bea37-123">The technique is similar to the half-toning used in black-and-white publications to achieve shades of gray.</span></span>

</dd> <dt>

<span data-ttu-id="bea37-124"><span id="opengl_double_buffering"></span><span id="OPENGL_DOUBLE_BUFFERING"></span>**buffer duplo**</span><span class="sxs-lookup"><span data-stu-id="bea37-124"><span id="opengl_double_buffering"></span><span id="OPENGL_DOUBLE_BUFFERING"></span>**double buffering**</span></span>
</dt> <dd>

<span data-ttu-id="bea37-125">Usando contextos OpenGL no qual os buffers de cor frontal e traseira são armazenados em buffer duplo.</span><span class="sxs-lookup"><span data-stu-id="bea37-125">Using OpenGL contexts in which both front and back color buffers are double-buffered.</span></span> <span data-ttu-id="bea37-126">A animação suave é realizada pela renderização somente no buffer de fundo (que não é exibido), fazendo com que os buffers de frente e de trás sejam trocados.</span><span class="sxs-lookup"><span data-stu-id="bea37-126">Smooth animation is accomplished by rendering into only the back buffer (which isn't displayed), then causing the front and back buffers to be swapped.</span></span>

</dd> </dl>

 

 




