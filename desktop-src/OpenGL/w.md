---
title: W (OpenGL)
description: Definições de termos OpenGL que começam com a letra W.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 7f8235a3-ea48-40eb-8957-e7a55a5778af
keywords:
- windows
- alinhado à janela
- coordenadas da janela
- wireframe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1f6f1897af46c85ed48171d251ebe1b2de8c5e1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103644093"
---
# <a name="w-opengl"></a><span data-ttu-id="38273-107">W (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="38273-107">W (OpenGL)</span></span>

<span data-ttu-id="38273-108">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [i](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) W [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="38273-108">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) W [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="38273-109"><span id="opengl_window"></span><span id="OPENGL_WINDOW"></span>**Window**</span><span class="sxs-lookup"><span data-stu-id="38273-109"><span id="opengl_window"></span><span id="OPENGL_WINDOW"></span>**window**</span></span>
</dt> <dd>

<span data-ttu-id="38273-110">Uma sub-região do framebuffer, geralmente retangular, cujos pixels têm a mesma configuração de buffer.</span><span class="sxs-lookup"><span data-stu-id="38273-110">A subregion of the framebuffer, usually rectangular, whose pixels all have the same buffer configuration.</span></span> <span data-ttu-id="38273-111">Um contexto OpenGL é renderizado em uma janela por vez.</span><span class="sxs-lookup"><span data-stu-id="38273-111">An OpenGL context renders to one window at a time.</span></span>

</dd> <dt>

<span data-ttu-id="38273-112"><span id="opengl_window_aligned"></span><span id="OPENGL_WINDOW_ALIGNED"></span>**alinhado à janela**</span><span class="sxs-lookup"><span data-stu-id="38273-112"><span id="opengl_window_aligned"></span><span id="OPENGL_WINDOW_ALIGNED"></span>**window-aligned**</span></span>
</dt> <dd>

<span data-ttu-id="38273-113">Ao fazer referência a segmentos de linha ou bordas de polígono, implica que eles são paralelos aos limites da janela.</span><span class="sxs-lookup"><span data-stu-id="38273-113">When referring to line segments or polygon edges, implies that these are parallel to the window boundaries.</span></span> <span data-ttu-id="38273-114">(No OpenGL, a janela é retangular, com bordas horizontais e verticais).</span><span class="sxs-lookup"><span data-stu-id="38273-114">(In OpenGL, the window is rectangular, with horizontal and vertical edges).</span></span> <span data-ttu-id="38273-115">Ao fazer referência a um padrão de polígono, implica que o padrão é fixo em relação à origem da janela.</span><span class="sxs-lookup"><span data-stu-id="38273-115">When referring to a polygon pattern, implies that the pattern is fixed relative to the window origin.</span></span>

</dd> <dt>

<span data-ttu-id="38273-116"><span id="opengl_window_coordinates"></span><span id="OPENGL_WINDOW_COORDINATES"></span>**coordenadas da janela**</span><span class="sxs-lookup"><span data-stu-id="38273-116"><span id="opengl_window_coordinates"></span><span id="OPENGL_WINDOW_COORDINATES"></span>**window coordinates**</span></span>
</dt> <dd>

<span data-ttu-id="38273-117">O sistema de coordenadas de uma janela.</span><span class="sxs-lookup"><span data-stu-id="38273-117">The coordinate system of a window.</span></span> <span data-ttu-id="38273-118">É importante distinguir entre os nomes de pixels, que são discretos e o sistema de coordenadas de janelas, que é contínuo.</span><span class="sxs-lookup"><span data-stu-id="38273-118">It's important to distinguish between the names of pixels, which are discrete, and the window-coordinate system, which is continuous.</span></span> <span data-ttu-id="38273-119">Por exemplo, o pixel no canto inferior esquerdo de uma janela é pixel (0, 0); as coordenadas da janela do centro desse pixel são (0,5, 0,5, z).</span><span class="sxs-lookup"><span data-stu-id="38273-119">For example, the pixel at the lower-left corner of a window is pixel (0, 0); the window coordinates of the center of this pixel are (0.5, 0.5, z).</span></span> <span data-ttu-id="38273-120">Observe que as coordenadas da janela incluem um componente de profundidade ou z, e esse componente também é contínuo.</span><span class="sxs-lookup"><span data-stu-id="38273-120">Note that window coordinates include a depth, or z, component, and that this component is continuous as well.</span></span>

</dd> <dt>

<span data-ttu-id="38273-121"><span id="opengl_wireframe"></span><span id="OPENGL_WIREFRAME"></span>**wireframe**</span><span class="sxs-lookup"><span data-stu-id="38273-121"><span id="opengl_wireframe"></span><span id="OPENGL_WIREFRAME"></span>**wireframe**</span></span>
</dt> <dd>

<span data-ttu-id="38273-122">Uma representação de um objeto que contém somente segmentos de linha.</span><span class="sxs-lookup"><span data-stu-id="38273-122">A representation of an object that contains line segments only.</span></span> <span data-ttu-id="38273-123">Normalmente, os segmentos de linha indicam as bordas do polígono.</span><span class="sxs-lookup"><span data-stu-id="38273-123">Typically, the line segments indicate polygon edges.</span></span>

</dd> </dl>

 

 




