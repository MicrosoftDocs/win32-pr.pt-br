---
title: Portando chamadas de plano de estêncil
description: No OpenGL, você aloca planos de estêncil solicitando o formato de pixel apropriado com o OpenGL auxInitDisplayMode ou ChoosePixelFormat.
ms.assetid: faea8a10-860a-4495-80fb-e83303e397df
keywords:
- Portabilidade do íris GL, planos de estêncil
- portando do íris GL, planos de estêncil
- portando para OpenGL do íris GL, planos de estêncil
- Portabilidade OpenGL do íris GL, planos de estêncil
- planos de estêncil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 829ea033a75cb1153a475496c3f33398640dbc76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292439"
---
# <a name="porting-stencil-plane-calls"></a><span data-ttu-id="aa2ef-108">Portando chamadas de plano de estêncil</span><span class="sxs-lookup"><span data-stu-id="aa2ef-108">Porting Stencil Plane Calls</span></span>

<span data-ttu-id="aa2ef-109">No OpenGL, você aloca planos de estêncil solicitando o formato de pixel apropriado com o OpenGL **auxInitDisplayMode** ou [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).</span><span class="sxs-lookup"><span data-stu-id="aa2ef-109">In OpenGL, you allocate stencil planes by requesting the appropriate pixel format with the OpenGL **auxInitDisplayMode** or [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).</span></span> <span data-ttu-id="aa2ef-110">funções.</span><span class="sxs-lookup"><span data-stu-id="aa2ef-110">functions.</span></span> <span data-ttu-id="aa2ef-111">A tabela a seguir lista as funções do íris GL que afetam os planos de estêncil e suas funções OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="aa2ef-111">The following table lists IRIS GL functions that affect the stencil planes and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="aa2ef-112">Função GL de íris</span><span class="sxs-lookup"><span data-stu-id="aa2ef-112">IRIS GL function</span></span>             | <span data-ttu-id="aa2ef-113">Função OpenGL</span><span class="sxs-lookup"><span data-stu-id="aa2ef-113">OpenGL function</span></span>                                         | <span data-ttu-id="aa2ef-114">Significado</span><span class="sxs-lookup"><span data-stu-id="aa2ef-114">Meaning</span></span>                                                |
|------------------------------|---------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="aa2ef-115">**stensize**</span><span class="sxs-lookup"><span data-stu-id="aa2ef-115">**stensize**</span></span>                 | <span data-ttu-id="aa2ef-116">**ChoosePixelFormat**</span><span class="sxs-lookup"><span data-stu-id="aa2ef-116">**ChoosePixelFormat**</span></span>                                   |                                                        |
| <span data-ttu-id="aa2ef-117">**estêncil**( **verdadeiro**,...)</span><span class="sxs-lookup"><span data-stu-id="aa2ef-117">**stencil**( **TRUE**, ... )</span></span> | <span data-ttu-id="aa2ef-118">[**glEnable**](glenable.md) ( \_ teste de estêncil GL \_ )</span><span class="sxs-lookup"><span data-stu-id="aa2ef-118">[**glEnable**](glenable.md) ( GL\_STENCIL\_TEST )</span></span>      | <span data-ttu-id="aa2ef-119">Habilita testes de estêncil.</span><span class="sxs-lookup"><span data-stu-id="aa2ef-119">Enables stencil tests.</span></span>                                 |
| <span data-ttu-id="aa2ef-120">**estêncil**</span><span class="sxs-lookup"><span data-stu-id="aa2ef-120">**stencil**</span></span>                  | [<span data-ttu-id="aa2ef-121">**glStencilOp**</span><span class="sxs-lookup"><span data-stu-id="aa2ef-121">**glStencilOp**</span></span>](glstencilop.md)                      | <span data-ttu-id="aa2ef-122">Define ações de teste de estêncil.</span><span class="sxs-lookup"><span data-stu-id="aa2ef-122">Sets stencil test actions.</span></span>                             |
| <span data-ttu-id="aa2ef-123">**estêncil**(... Func,...)</span><span class="sxs-lookup"><span data-stu-id="aa2ef-123">**stencil**(... func, ... )</span></span>  | [<span data-ttu-id="aa2ef-124">**glStencilFunc**</span><span class="sxs-lookup"><span data-stu-id="aa2ef-124">**glStencilFunc**</span></span>](glstencilfunc.md)                  | <span data-ttu-id="aa2ef-125">Define o valor de função e referência para teste de estêncil.</span><span class="sxs-lookup"><span data-stu-id="aa2ef-125">Sets function and reference value for stencil testing.</span></span> |
| <span data-ttu-id="aa2ef-126">**swritemask**</span><span class="sxs-lookup"><span data-stu-id="aa2ef-126">**swritemask**</span></span>               | [<span data-ttu-id="aa2ef-127">**glStencilMask**</span><span class="sxs-lookup"><span data-stu-id="aa2ef-127">**glStencilMask**</span></span>](glstencilmask.md)                  | <span data-ttu-id="aa2ef-128">Especifica quais bits de estêncil podem ser gravados.</span><span class="sxs-lookup"><span data-stu-id="aa2ef-128">Specifies which stencil bits can be written.</span></span>           |
|                              | [<span data-ttu-id="aa2ef-129">**glClearStencil**</span><span class="sxs-lookup"><span data-stu-id="aa2ef-129">**glClearStencil**</span></span>](glclearstencil.md)                | <span data-ttu-id="aa2ef-130">Especifica o valor de limpeza para o buffer de estêncil.</span><span class="sxs-lookup"><span data-stu-id="aa2ef-130">Specifies the clear value for the stencil buffer.</span></span>      |
| <span data-ttu-id="aa2ef-131">**sclear**</span><span class="sxs-lookup"><span data-stu-id="aa2ef-131">**sclear**</span></span>                   | <span data-ttu-id="aa2ef-132">[**glClear**](glclear.md) ( \_ bit de buffer do estêncil GL \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="aa2ef-132">[**glClear**](glclear.md) ( GL\_STENCIL\_BUFFER\_BIT )</span></span> |                                                        |



 

<span data-ttu-id="aa2ef-133">As funções de comparação de estêncil e de passagem/falha de estêncil são quase equivalentes em OpenGL e íris GL.</span><span class="sxs-lookup"><span data-stu-id="aa2ef-133">Stencil-comparison functions and stencil pass/fail operations are nearly equivalent in OpenGL and IRIS GL.</span></span> <span data-ttu-id="aa2ef-134">Os sinalizadores de função de estêncil íris GL são precedidos de it; os sinalizadores OpenGL com GL.</span><span class="sxs-lookup"><span data-stu-id="aa2ef-134">The IRIS GL stencil-function flags are prefaced with SF; the OpenGL flags with GL.</span></span> <span data-ttu-id="aa2ef-135">Os sinalizadores de operação de passagem/reprovação do íris GL são precedidos de ST; os sinalizadores OpenGL com GL.</span><span class="sxs-lookup"><span data-stu-id="aa2ef-135">IRIS GL pass/fail operation flags are prefaced with ST; the OpenGL flags with GL.</span></span>

 

 




