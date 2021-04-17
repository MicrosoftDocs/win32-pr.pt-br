---
title: Portando funções de separação
description: Todas as funções de separação do íris GL têm equivalentes a OpenGL, com exceção de clearhitcode. A tabela a seguir lista as funções de separação do íris GL e suas funções OpenGL equivalentes.
ms.assetid: f8fbd0c2-14bf-47bc-be7f-eeef346dbac1
keywords:
- Portabilidade do íris GL, separação
- portando do íris GL, escolhendo
- portando para OpenGL do íris GL, escolhendo
- Portabilidade OpenGL do íris GL, separação
- seleção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db4c0ea6011860f7d5010dd0bb7d5d23b671d99a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105748420"
---
# <a name="porting-picking-functions"></a><span data-ttu-id="c7aad-109">Portando funções de separação</span><span class="sxs-lookup"><span data-stu-id="c7aad-109">Porting Picking Functions</span></span>

<span data-ttu-id="c7aad-110">Todas as funções de separação do íris GL têm equivalentes a OpenGL, com exceção de **clearhitcode**.</span><span class="sxs-lookup"><span data-stu-id="c7aad-110">All IRIS GL picking functions have OpenGL equivalents, with the exception of **clearhitcode**.</span></span> <span data-ttu-id="c7aad-111">A tabela a seguir lista as funções de separação do íris GL e suas funções OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="c7aad-111">The following table lists the IRIS GL picking functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="c7aad-112">Função GL de íris</span><span class="sxs-lookup"><span data-stu-id="c7aad-112">IRIS GL function</span></span>                | <span data-ttu-id="c7aad-113">Função OpenGL</span><span class="sxs-lookup"><span data-stu-id="c7aad-113">OpenGL function</span></span>                                                                           | <span data-ttu-id="c7aad-114">Significado</span><span class="sxs-lookup"><span data-stu-id="c7aad-114">Meaning</span></span>                                |
|---------------------------------|-------------------------------------------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="c7aad-115">**clearhitcode**</span><span class="sxs-lookup"><span data-stu-id="c7aad-115">**clearhitcode**</span></span>                | <span data-ttu-id="c7aad-116">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="c7aad-116">Not supported.</span></span>                                                                            | <span data-ttu-id="c7aad-117">Limpa a variável global e hitcode.</span><span class="sxs-lookup"><span data-stu-id="c7aad-117">Clears global variable and hitcode.</span></span>    |
| <span data-ttu-id="c7aad-118">**pickselect**</span><span class="sxs-lookup"><span data-stu-id="c7aad-118">**pickselect**</span></span><br/>       | <span data-ttu-id="c7aad-119">[**glRenderMode**](glrendermode.md) (GL \_ Select)</span><span class="sxs-lookup"><span data-stu-id="c7aad-119">[**glRenderMode**](glrendermode.md) ( GL\_SELECT )</span></span>                                       | <span data-ttu-id="c7aad-120">Alterna para o modo de seleção ou de separação.</span><span class="sxs-lookup"><span data-stu-id="c7aad-120">Switches to selection or picking mode.</span></span> |
| <span data-ttu-id="c7aad-121">**endpickendselect**</span><span class="sxs-lookup"><span data-stu-id="c7aad-121">**endpickendselect**</span></span><br/> | <span data-ttu-id="c7aad-122">[**glRenderMode**](glrendermode.md) ( \_ renderização GL)</span><span class="sxs-lookup"><span data-stu-id="c7aad-122">[**glRenderMode**](glrendermode.md) ( GL\_RENDER )</span></span>                                       | <span data-ttu-id="c7aad-123">Alterna para o modo de renderização.</span><span class="sxs-lookup"><span data-stu-id="c7aad-123">Switches to rendering mode.</span></span>            |
| <span data-ttu-id="c7aad-124">**picksize**</span><span class="sxs-lookup"><span data-stu-id="c7aad-124">**picksize**</span></span>                    | <span data-ttu-id="c7aad-125">[**gluPickMatrix**](glupickmatrix.md)[**glSelectBuffer**](glselectbuffer.md)</span><span class="sxs-lookup"><span data-stu-id="c7aad-125">[**gluPickMatrix**](glupickmatrix.md)[**glSelectBuffer**](glselectbuffer.md)</span></span><br/> | <span data-ttu-id="c7aad-126">Define a matriz de retorno.</span><span class="sxs-lookup"><span data-stu-id="c7aad-126">Sets the return array.</span></span>                 |
| <span data-ttu-id="c7aad-127">**initnames**</span><span class="sxs-lookup"><span data-stu-id="c7aad-127">**initnames**</span></span>                   | [<span data-ttu-id="c7aad-128">**glInitNames**</span><span class="sxs-lookup"><span data-stu-id="c7aad-128">**glInitNames**</span></span>](glinitnames.md)                                                        |                                        |
| <span data-ttu-id="c7aad-129">**pushnamepopname**</span><span class="sxs-lookup"><span data-stu-id="c7aad-129">**pushnamepopname**</span></span><br/>  | <span data-ttu-id="c7aad-130">[**glPushName**](glpushname.md)[**glPopName**](glpopname.md)</span><span class="sxs-lookup"><span data-stu-id="c7aad-130">[**glPushName**](glpushname.md)[**glPopName**](glpopname.md)</span></span><br/>                 |                                        |
| <span data-ttu-id="c7aad-131">**loadname**</span><span class="sxs-lookup"><span data-stu-id="c7aad-131">**loadname**</span></span>                    | [<span data-ttu-id="c7aad-132">**glLoadName**</span><span class="sxs-lookup"><span data-stu-id="c7aad-132">**glLoadName**</span></span>](glloadname.md)                                                          |                                        |



 

<span data-ttu-id="c7aad-133">Para obter mais informações sobre a escolha, consulte [**gluPickMatrix**](glupickmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="c7aad-133">For more information on picking, see [**gluPickMatrix**](glupickmatrix.md).</span></span>

 

 





