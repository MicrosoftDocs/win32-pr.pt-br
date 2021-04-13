---
title: I (OpenGL)
description: Definições de termos OpenGL que começam com a letra I.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2c78efce-9aed-4bcd-a254-7bff053b0acd
keywords:
- images
- primitivos de imagem
- modo imediato
- índice
- ÍRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fe340cfbd7dbef3d93cc68ba310d863717225c0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104499203"
---
# <a name="i-opengl"></a><span data-ttu-id="1e56c-108">I (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="1e56c-108">I (OpenGL)</span></span>

<span data-ttu-id="1e56c-109">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) i [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="1e56c-109">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) I [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="1e56c-110"><span id="opengl_image"></span><span id="OPENGL_IMAGE"></span>**imagem**</span><span class="sxs-lookup"><span data-stu-id="1e56c-110"><span id="opengl_image"></span><span id="OPENGL_IMAGE"></span>**image**</span></span>
</dt> <dd>

<span data-ttu-id="1e56c-111">Uma matriz retangular de pixels, seja na memória do cliente ou no framebuffer.</span><span class="sxs-lookup"><span data-stu-id="1e56c-111">A rectangular array of pixels, either in client memory or in the framebuffer.</span></span>

</dd> <dt>

<span data-ttu-id="1e56c-112"><span id="opengl_image_primitive"></span><span id="OPENGL_IMAGE_PRIMITIVE"></span>**primitiva de imagem**</span><span class="sxs-lookup"><span data-stu-id="1e56c-112"><span id="opengl_image_primitive"></span><span id="OPENGL_IMAGE_PRIMITIVE"></span>**image primitive**</span></span> 
</dt> <dd>

<span data-ttu-id="1e56c-113">Um bitmap ou uma imagem.</span><span class="sxs-lookup"><span data-stu-id="1e56c-113">A bitmap or an image.</span></span>

</dd> <dt>

<span data-ttu-id="1e56c-114"><span id="opengl_immediate_mode"></span><span id="OPENGL_IMMEDIATE_MODE"></span>**modo imediato**</span><span class="sxs-lookup"><span data-stu-id="1e56c-114"><span id="opengl_immediate_mode"></span><span id="OPENGL_IMMEDIATE_MODE"></span>**immediate mode**</span></span>
</dt> <dd>

<span data-ttu-id="1e56c-115">Modo no qual um comando OpenGL é chamado diretamente, em vez de uma lista de exibição.</span><span class="sxs-lookup"><span data-stu-id="1e56c-115">Mode in which an OpenGL command is called directly, rather than from a display list.</span></span> <span data-ttu-id="1e56c-116">Não existe nenhum bit de modo imediato; o modo no modo imediato refere-se ao uso do OpenGL, em vez de um bit específico de estado OpenGL.</span><span class="sxs-lookup"><span data-stu-id="1e56c-116">No immediate-mode bit exists; the mode in immediate mode refers to usage of OpenGL, rather than to a specific bit of OpenGL state.</span></span>

</dd> <dt>

<span data-ttu-id="1e56c-117"><span id="opengl_index"></span><span id="OPENGL_INDEX"></span>**index**</span><span class="sxs-lookup"><span data-stu-id="1e56c-117"><span id="opengl_index"></span><span id="OPENGL_INDEX"></span>**index**</span></span>
</dt> <dd>

<span data-ttu-id="1e56c-118">Um único valor que é interpretado como um valor absoluto, em vez de um valor normalizado em um intervalo especificado (como é um componente).</span><span class="sxs-lookup"><span data-stu-id="1e56c-118">A single value that is interpreted as an absolute value, rather than as a normalized value in a specified range (as is a component).</span></span> <span data-ttu-id="1e56c-119">Os índices de cores são os nomes das cores, que são desreferenciadas pelo hardware de vídeo usando o mapa de cores.</span><span class="sxs-lookup"><span data-stu-id="1e56c-119">Color indexes are the names of colors, which are dereferenced by the display hardware using the color map.</span></span> <span data-ttu-id="1e56c-120">Normalmente, os índices são mascarados, em vez de clamped, quando estão fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="1e56c-120">Indexes are typically masked, rather than clamped, when out of range.</span></span> <span data-ttu-id="1e56c-121">Por exemplo, o índice 0xf7 é mascarado para 0x7 quando gravado em um buffer de 4 bits (cor ou estêncil).</span><span class="sxs-lookup"><span data-stu-id="1e56c-121">For example, the index 0xf7 is masked to 0x7 when written to a 4-bit buffer (color or stencil).</span></span> <span data-ttu-id="1e56c-122">Os índices de cor e os índices de estêncil são sempre tratados como índices, nunca como componentes.</span><span class="sxs-lookup"><span data-stu-id="1e56c-122">Color indexes and stencil indexes are always treated as indexes, never as components.</span></span>

</dd> <dt>

<span data-ttu-id="1e56c-123"><span id="opengl_iris_gl"></span><span id="OPENGL_IRIS_GL"></span>**ÍRIS GL**</span><span class="sxs-lookup"><span data-stu-id="1e56c-123"><span id="opengl_iris_gl"></span><span id="OPENGL_IRIS_GL"></span>**IRIS GL**</span></span>
</dt> <dd>

<span data-ttu-id="1e56c-124">Biblioteca gráfica proprietária do Silicon Graphics, desenvolvida de 1982 até 1992.</span><span class="sxs-lookup"><span data-stu-id="1e56c-124">Silicon Graphics' proprietary graphics library, developed from 1982 through 1992.</span></span> <span data-ttu-id="1e56c-125">O OpenGL foi projetado com o íris GL como um ponto de partida.</span><span class="sxs-lookup"><span data-stu-id="1e56c-125">OpenGL was designed with IRIS GL as a starting point.</span></span>

</dd> </dl>

 

 




