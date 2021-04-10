---
title: Portando listas de exibição
description: A implementação do OpenGL de listas de exibição é semelhante à implementação da íris GL, com duas exceções no OpenGL, você não pode editar listas de exibição depois de criá-las e não pode chamar funções de listas de exibição.
ms.assetid: 617e19ff-6a55-4f7c-b229-075cdee8f1cf
keywords:
- Portabilidade do íris GL, listas de exibição
- portando do íris GL, listas de exibição
- portando para OpenGL do íris GL, listas de exibição
- Portabilidade OpenGL do íris GL, listas de exibição
- Exibir listas, portando do íris GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461000e6d785f0d03bbbc8f738eba60768bc5d74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291894"
---
# <a name="porting-display-lists"></a><span data-ttu-id="58288-108">Portando listas de exibição</span><span class="sxs-lookup"><span data-stu-id="58288-108">Porting Display Lists</span></span>

<span data-ttu-id="58288-109">A implementação do OpenGL de listas de exibição é semelhante à implementação da íris GL, com duas exceções: no OpenGL, não é possível editar as listas de exibição depois de criá-las e não é possível chamar funções de dentro de listas de exibição.</span><span class="sxs-lookup"><span data-stu-id="58288-109">The OpenGL implementation of display lists is similar to the IRIS GL implementation, with two exceptions: in OpenGL you can't edit display lists once you've created them and you can't call functions from within display lists.</span></span>

<span data-ttu-id="58288-110">Como não é possível editar ou chamar funções de listas de exibição, essas funções de íris GL não têm nenhum equivalente em OpenGL:</span><span class="sxs-lookup"><span data-stu-id="58288-110">Because you can't edit or call functions from within display lists, these IRIS GL functions have no equivalent in OpenGL:</span></span>

-   <span data-ttu-id="58288-111">**editobj**</span><span class="sxs-lookup"><span data-stu-id="58288-111">**editobj**</span></span>
-   <span data-ttu-id="58288-112">**objdelete**, **objinsert** e **objreplace**</span><span class="sxs-lookup"><span data-stu-id="58288-112">**objdelete**, **objinsert**, and **objreplace**</span></span>
-   <span data-ttu-id="58288-113">**maketag**, **gentag**, **IsTag** e **deltag**</span><span class="sxs-lookup"><span data-stu-id="58288-113">**maketag**, **gentag**, **istag**, and **deltag**</span></span>
-   <span data-ttu-id="58288-114">**callfunc**</span><span class="sxs-lookup"><span data-stu-id="58288-114">**callfunc**</span></span>

<span data-ttu-id="58288-115">No íris GL, você usa as funções **makeobj** e **closeobj** para criar listas de exibição.</span><span class="sxs-lookup"><span data-stu-id="58288-115">In IRIS GL, you use the **makeobj** and **closeobj** functions to create display lists.</span></span> <span data-ttu-id="58288-116">No OpenGL, você usa [**glNewList**](glnewlist.md) e [**glEndList**](glendlist.md).</span><span class="sxs-lookup"><span data-stu-id="58288-116">In OpenGL, you use [**glNewList**](glnewlist.md) and [**glEndList**](glendlist.md).</span></span>

<span data-ttu-id="58288-117">A tabela a seguir lista as funções de lista de exibição do íris GL com suas funções OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="58288-117">The following table lists the IRIS GL display list functions with their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="58288-118">Função GL de íris</span><span class="sxs-lookup"><span data-stu-id="58288-118">IRIS GL function</span></span> | <span data-ttu-id="58288-119">Função OpenGL</span><span class="sxs-lookup"><span data-stu-id="58288-119">OpenGL function</span></span>                                                      | <span data-ttu-id="58288-120">Significado</span><span class="sxs-lookup"><span data-stu-id="58288-120">Meaning</span></span>                                                       |
|------------------|----------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="58288-121">**makeobj**</span><span class="sxs-lookup"><span data-stu-id="58288-121">**makeobj**</span></span>      | <span data-ttu-id="58288-122">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="58288-122">**glNewList**</span></span>                                                        | <span data-ttu-id="58288-123">Cria uma nova lista de exibição.</span><span class="sxs-lookup"><span data-stu-id="58288-123">Creates a new display list.</span></span>                                   |
| <span data-ttu-id="58288-124">**closeobj**</span><span class="sxs-lookup"><span data-stu-id="58288-124">**closeobj**</span></span>     | <span data-ttu-id="58288-125">**glEndList**</span><span class="sxs-lookup"><span data-stu-id="58288-125">**glEndList**</span></span>                                                        | <span data-ttu-id="58288-126">Indica o fim da lista de exibição.</span><span class="sxs-lookup"><span data-stu-id="58288-126">Signals end of display list.</span></span>                                  |
| <span data-ttu-id="58288-127">**callobj**</span><span class="sxs-lookup"><span data-stu-id="58288-127">**callobj**</span></span>      | <span data-ttu-id="58288-128">[**glCallList**](glcalllist.md), [ **glCallLists**](glcalllists.md)</span><span class="sxs-lookup"><span data-stu-id="58288-128">[**glCallList**](glcalllist.md), [**glCallLists**](glcalllists.md)</span></span> | <span data-ttu-id="58288-129">Executa lista ou listas de exibição.</span><span class="sxs-lookup"><span data-stu-id="58288-129">Executes display list or lists.</span></span>                               |
| <span data-ttu-id="58288-130">**isobj**</span><span class="sxs-lookup"><span data-stu-id="58288-130">**isobj**</span></span>        | [<span data-ttu-id="58288-131">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="58288-131">**glIsList**</span></span>](glislist.md)                                         | <span data-ttu-id="58288-132">Testes para a existência da lista de exibição.</span><span class="sxs-lookup"><span data-stu-id="58288-132">Tests for display list existence.</span></span>                             |
| <span data-ttu-id="58288-133">**delobj**</span><span class="sxs-lookup"><span data-stu-id="58288-133">**delobj**</span></span>       | [<span data-ttu-id="58288-134">**glDeleteLists**</span><span class="sxs-lookup"><span data-stu-id="58288-134">**glDeleteLists**</span></span>](gldeletelists.md)                               | <span data-ttu-id="58288-135">Exclui o grupo contíguo de listas de exibição.</span><span class="sxs-lookup"><span data-stu-id="58288-135">Deletes contiguous group of display lists.</span></span>                    |
| <span data-ttu-id="58288-136">**genobj**</span><span class="sxs-lookup"><span data-stu-id="58288-136">**genobj**</span></span>       | [<span data-ttu-id="58288-137">**glGenLists**</span><span class="sxs-lookup"><span data-stu-id="58288-137">**glGenLists**</span></span>](glgenlists.md)                                     | <span data-ttu-id="58288-138">Gera o número determinado de listas de exibição vazias contíguas.</span><span class="sxs-lookup"><span data-stu-id="58288-138">Generates the given number of contiguous empty display lists.</span></span> |



 

<span data-ttu-id="58288-139">Este tópico inclui informações sobre o seguinte.</span><span class="sxs-lookup"><span data-stu-id="58288-139">This topic includes information on the following.</span></span>

-   [<span data-ttu-id="58288-140">Portando a função bbox2</span><span class="sxs-lookup"><span data-stu-id="58288-140">Porting the bbox2 Function</span></span>](porting-the-bbox2-function.md)
-   [<span data-ttu-id="58288-141">Portando listas de exibição editadas</span><span class="sxs-lookup"><span data-stu-id="58288-141">Porting Edited Display Lists</span></span>](porting-edited-display-lists.md)
-   [<span data-ttu-id="58288-142">Uma porta de exemplo de uma lista de exibição</span><span class="sxs-lookup"><span data-stu-id="58288-142">A Sample Port of a Display List</span></span>](a-sample-port-of-a-display-list.md)

 

 




