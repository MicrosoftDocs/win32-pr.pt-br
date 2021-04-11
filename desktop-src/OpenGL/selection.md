---
title: Seleção
description: A seleção retorna o conteúdo atual da pilha de nomes, que é uma matriz de nomes com valores inteiros.
ms.assetid: 66902d2c-0cd7-49b3-a685-5c0bdba0df1c
keywords:
- modo de seleção OpenGL
- acertos de seleção OpenGL
- registros de clique OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 851fac28cda979a383d183a12c79656bfebcbb0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292357"
---
# <a name="selection"></a><span data-ttu-id="72869-106">Seleção</span><span class="sxs-lookup"><span data-stu-id="72869-106">Selection</span></span>

<span data-ttu-id="72869-107">A seleção retorna o conteúdo atual da pilha de nomes, que é uma matriz de nomes com valores inteiros.</span><span class="sxs-lookup"><span data-stu-id="72869-107">Selection returns the current contents of the name stack, which is an array of names with integer values.</span></span> <span data-ttu-id="72869-108">Você atribui os nomes e cria a pilha de nomes dentro do código de modelagem que especifica a geometria de objetos que você deseja desenhar.</span><span class="sxs-lookup"><span data-stu-id="72869-108">You assign the names and build the name stack within the modeling code that specifies the geometry of objects you want to draw.</span></span> <span data-ttu-id="72869-109">Em seguida, no modo de seleção, sempre que um primitivo intercepta o volume do clipe, ocorre uma ocorrência de seleção.</span><span class="sxs-lookup"><span data-stu-id="72869-109">Then, in selection mode, whenever a primitive intersects the clip volume, a selection hit occurs.</span></span> <span data-ttu-id="72869-110">O registro de acesso, que é gravado na matriz de seleção que você forneceu com [**glSelectBuffer**](glselectbuffer.md), contém informações sobre o conteúdo da pilha de nomes no momento da visita.</span><span class="sxs-lookup"><span data-stu-id="72869-110">The hit record, which is written into the selection array you've supplied with [**glSelectBuffer**](glselectbuffer.md), contains information about the contents of the name stack at the time of the hit.</span></span>

> [!Note]  
> <span data-ttu-id="72869-111">Chame [**glSelectBuffer**](glselectbuffer.md) antes de colocar o OpenGL no modo de seleção com [**glRenderMode**](glrendermode.md).</span><span class="sxs-lookup"><span data-stu-id="72869-111">Call [**glSelectBuffer**](glselectbuffer.md) before you put OpenGL into selection mode with [**glRenderMode**](glrendermode.md).</span></span> <span data-ttu-id="72869-112">Não há garantia de que todo o conteúdo da pilha de nomes seja retornado até que você chame **glRenderMode** para retirar o OpenGL do modo de seleção.</span><span class="sxs-lookup"><span data-stu-id="72869-112">The entire contents of the name stack aren't guaranteed to be returned until you call **glRenderMode** to take OpenGL out of selection mode.</span></span>

 

<span data-ttu-id="72869-113">Manipule a pilha de nomes com [**glInitNames**](glinitnames.md), [**glLoadName**](glloadname.md), [**glPushName**](glpushname.md)e [**glPopName**](glpopname.md).</span><span class="sxs-lookup"><span data-stu-id="72869-113">Manipulate the name stack with [**glInitNames**](glinitnames.md), [**glLoadName**](glloadname.md), [**glPushName**](glpushname.md), and [**glPopName**](glpopname.md).</span></span> <span data-ttu-id="72869-114">Você também pode usar [**gluPickMatrix**](glupickmatrix.md) para seleção.</span><span class="sxs-lookup"><span data-stu-id="72869-114">You can also use [**gluPickMatrix**](glupickmatrix.md) for selection.</span></span>

 

 




