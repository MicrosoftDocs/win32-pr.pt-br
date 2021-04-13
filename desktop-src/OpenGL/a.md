---
title: A (OpenGL)
description: Definições de termos OpenGL que começam com a letra A.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: e583610f-37da-47bb-bbd6-41d353b88244
keywords:
- alias
- alpha
- animação
- suavização
- recorte específico do aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d161832eb6d81738038e10564233f26920f0d60
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369138"
---
# <a name="a-opengl"></a><span data-ttu-id="47de2-108">A (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="47de2-108">A (OpenGL)</span></span>

<span data-ttu-id="47de2-109">A [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [i](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="47de2-109">A [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="47de2-110"><span id="opengl_aliasing"></span><span id="OPENGL_ALIASING"></span>**alias**</span><span class="sxs-lookup"><span data-stu-id="47de2-110"><span id="opengl_aliasing"></span><span id="OPENGL_ALIASING"></span>**aliasing**</span></span>
</dt> <dd>

<span data-ttu-id="47de2-111">Uma técnica de renderização que atribui a pixels a cor do primitivo que está sendo renderizado, se esse primitivo abrange toda ou parte da área do pixel.</span><span class="sxs-lookup"><span data-stu-id="47de2-111">A rendering technique that assigns to pixels the color of the primitive being rendered, whether that primitive covers all or part of the pixel's area.</span></span> <span data-ttu-id="47de2-112">O alias resulta em bordas irregulares ou jaggies.</span><span class="sxs-lookup"><span data-stu-id="47de2-112">Aliasing results in jagged edges, or jaggies.</span></span> <span data-ttu-id="47de2-113">Consulte também [jaggies](jk.md).</span><span class="sxs-lookup"><span data-stu-id="47de2-113">See also [jaggies](jk.md).</span></span>

</dd> <dt>

<span data-ttu-id="47de2-114"><span id="opengl_alpha"></span><span id="OPENGL_ALPHA"></span>**Alfa**</span><span class="sxs-lookup"><span data-stu-id="47de2-114"><span id="opengl_alpha"></span><span id="OPENGL_ALPHA"></span>**alpha**</span></span>
</dt> <dd>

<span data-ttu-id="47de2-115">Um componente da quarta cor normalmente usado para controlar a mesclagem de cores.</span><span class="sxs-lookup"><span data-stu-id="47de2-115">A fourth color component typically used to control color blending.</span></span> <span data-ttu-id="47de2-116">O componente alfa nunca é exibido diretamente.</span><span class="sxs-lookup"><span data-stu-id="47de2-116">The alpha component is never displayed directly.</span></span> <span data-ttu-id="47de2-117">Por convenção, OpenGL Alpha indica opacidade e transparência em uma escala de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="47de2-117">By convention, OpenGL alpha indicates opacity and transparency on a scale of 0.0 to 1.0.</span></span> <span data-ttu-id="47de2-118">Um valor alfa de 1,0 implica opacidade completa, um valor alfa de 0,0 implica transparência completa.</span><span class="sxs-lookup"><span data-stu-id="47de2-118">An alpha value of 1.0 implies complete opacity, an alpha value of 0.0 implies complete transparency.</span></span>

</dd> <dt>

<span data-ttu-id="47de2-119"><span id="opengl_animation"></span><span id="OPENGL_ANIMATION"></span>**animada**</span><span class="sxs-lookup"><span data-stu-id="47de2-119"><span id="opengl_animation"></span><span id="OPENGL_ANIMATION"></span>**animation**</span></span>
</dt> <dd>

<span data-ttu-id="47de2-120">A geração de renderizações repetidas de uma cena com rapidez suficiente, com o ponto de vista ou posições de objeto com alteração suave, que a ilusão de movimento é alcançada.</span><span class="sxs-lookup"><span data-stu-id="47de2-120">The generation of repeated renderings of a scene quickly enough, with smoothly changing viewpoint or object positions, that the illusion of motion is achieved.</span></span> <span data-ttu-id="47de2-121">A animação OpenGL quase sempre usa o buffer duplo.</span><span class="sxs-lookup"><span data-stu-id="47de2-121">OpenGL animation almost always uses double-buffering.</span></span>

</dd> <dt>

<span data-ttu-id="47de2-122"><span id="opengl_antialiasing"></span><span id="OPENGL_ANTIALIASING"></span>**suavização**</span><span class="sxs-lookup"><span data-stu-id="47de2-122"><span id="opengl_antialiasing"></span><span id="OPENGL_ANTIALIASING"></span>**antialiasing**</span></span>
</dt> <dd>

<span data-ttu-id="47de2-123">Uma técnica de renderização que atribui cores a pixels com base na fração da área de pixel coberta pelo primitivo que está sendo renderizado.</span><span class="sxs-lookup"><span data-stu-id="47de2-123">A rendering technique that assigns colors to pixels based on the fraction of the pixel area that is covered by the primitive being rendered.</span></span> <span data-ttu-id="47de2-124">A renderização AntiAlias reduz ou elimina o jaggies que resulta da renderização com alias.</span><span class="sxs-lookup"><span data-stu-id="47de2-124">Antialiased rendering reduces or eliminates the jaggies that result from aliased rendering.</span></span> <span data-ttu-id="47de2-125">Confira também [jaggies](jk.md), [renderização](r.md).</span><span class="sxs-lookup"><span data-stu-id="47de2-125">See also [jaggies](jk.md), [rendering](r.md).</span></span>

</dd> <dt>

<span data-ttu-id="47de2-126"><span id="opengl_application_specific_clipping"></span><span id="OPENGL_APPLICATION_SPECIFIC_CLIPPING"></span>**recorte específico do aplicativo**</span><span class="sxs-lookup"><span data-stu-id="47de2-126"><span id="opengl_application_specific_clipping"></span><span id="OPENGL_APPLICATION_SPECIFIC_CLIPPING"></span>**application-specific clipping**</span></span> 
</dt> <dd>

<span data-ttu-id="47de2-127">Recorte de primitivas em planos em coordenadas de olho.</span><span class="sxs-lookup"><span data-stu-id="47de2-127">Clipping of primitives against planes in eye coordinates.</span></span> <span data-ttu-id="47de2-128">Os planos são especificados pelo aplicativo usando [**glClipPlane**](glclipplane.md).</span><span class="sxs-lookup"><span data-stu-id="47de2-128">The planes are specified by the application using [**glClipPlane**](glclipplane.md).</span></span> <span data-ttu-id="47de2-129">Consulte também as [coordenadas de olho](e.md).</span><span class="sxs-lookup"><span data-stu-id="47de2-129">See also [eye coordinates](e.md).</span></span>

</dd> </dl>

 

 




