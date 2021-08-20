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
ms.openlocfilehash: bb69307f869031bb9fd176ec85dd20eac5d543ef3e7f63086c6ea0801d1b8b8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128366"
---
# <a name="a-opengl"></a>A (OpenGL)

A [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [i](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)

<dl> <dt>

<span id="opengl_aliasing"></span><span id="OPENGL_ALIASING"></span>**alias**
</dt> <dd>

Uma técnica de renderização que atribui a pixels a cor do primitivo que está sendo renderizado, se esse primitivo abrange toda ou parte da área do pixel. O alias resulta em bordas irregulares ou jaggies. Consulte também [jaggies](jk.md).

</dd> <dt>

<span id="opengl_alpha"></span><span id="OPENGL_ALPHA"></span>**Alfa**
</dt> <dd>

Um componente da quarta cor normalmente usado para controlar a mesclagem de cores. O componente alfa nunca é exibido diretamente. Por convenção, OpenGL Alpha indica opacidade e transparência em uma escala de 0,0 a 1,0. Um valor alfa de 1,0 implica opacidade completa, um valor alfa de 0,0 implica transparência completa.

</dd> <dt>

<span id="opengl_animation"></span><span id="OPENGL_ANIMATION"></span>**animada**
</dt> <dd>

A geração de renderizações repetidas de uma cena com rapidez suficiente, com o ponto de vista ou posições de objeto com alteração suave, que a ilusão de movimento é alcançada. A animação OpenGL quase sempre usa o buffer duplo.

</dd> <dt>

<span id="opengl_antialiasing"></span><span id="OPENGL_ANTIALIASING"></span>**suavização**
</dt> <dd>

Uma técnica de renderização que atribui cores a pixels com base na fração da área de pixel coberta pelo primitivo que está sendo renderizado. A renderização AntiAlias reduz ou elimina o jaggies que resulta da renderização com alias. Confira também [jaggies](jk.md), [renderização](r.md).

</dd> <dt>

<span id="opengl_application_specific_clipping"></span><span id="OPENGL_APPLICATION_SPECIFIC_CLIPPING"></span>**recorte específico do aplicativo** 
</dt> <dd>

Recorte de primitivas em planos em coordenadas de olho. Os planos são especificados pelo aplicativo usando [**glClipPlane**](glclipplane.md). Consulte também as [coordenadas de olho](e.md).

</dd> </dl>

 

 




