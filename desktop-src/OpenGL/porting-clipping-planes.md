---
title: Portando planos de recorte
description: O OpenGL implementa planos de recorte da mesma forma para o íris GL. Além disso, no OpenGL, você pode consultar os planos de recorte. A tabela a seguir lista as funções de plano de recorte íris GL e suas funções OpenGL equivalentes.
ms.assetid: bfca59c3-b7ef-4545-8b8d-022ea782569b
keywords:
- Portabilidade do íris GL, planos de recorte
- portando do íris GL, planos de recorte
- portando para OpenGL do íris GL, planos de recorte
- Portabilidade do OpenGL do íris GL, planos de recorte
- planos de recorte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b531b39daf6670a3a99d9a4cbcf55158ea2d4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636929"
---
# <a name="porting-clipping-planes"></a><span data-ttu-id="4a41a-110">Portando planos de recorte</span><span class="sxs-lookup"><span data-stu-id="4a41a-110">Porting Clipping Planes</span></span>

<span data-ttu-id="4a41a-111">O OpenGL implementa planos de recorte da mesma forma para o íris GL.</span><span class="sxs-lookup"><span data-stu-id="4a41a-111">OpenGL implements clipping planes similarly to IRIS GL.</span></span> <span data-ttu-id="4a41a-112">Além disso, no OpenGL, você pode consultar os planos de recorte.</span><span class="sxs-lookup"><span data-stu-id="4a41a-112">In addition, in OpenGL you can query clipping planes.</span></span> <span data-ttu-id="4a41a-113">A tabela a seguir lista as funções de plano de recorte íris GL e suas funções OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="4a41a-113">The following table lists IRIS GL clipping plane functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="4a41a-114">Função GL de íris</span><span class="sxs-lookup"><span data-stu-id="4a41a-114">IRIS GL function</span></span>                          | <span data-ttu-id="4a41a-115">Função OpenGL</span><span class="sxs-lookup"><span data-stu-id="4a41a-115">OpenGL function</span></span>                                                                               | <span data-ttu-id="4a41a-116">Significado</span><span class="sxs-lookup"><span data-stu-id="4a41a-116">Meaning</span></span>                                  |
|-------------------------------------------|-----------------------------------------------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="4a41a-117">**clipplane** (i, **CP \_ on**, params)</span><span class="sxs-lookup"><span data-stu-id="4a41a-117">**clipplane** (i, **CP\_ON**, params)</span></span>     | <span data-ttu-id="4a41a-118">[**glEnable**](glenable.md) (GL \_ remediador \_ )</span><span class="sxs-lookup"><span data-stu-id="4a41a-118">[**glEnable**](glenable.md) ( GL\_CLIP\_PLANEi )</span></span>                                             | <span data-ttu-id="4a41a-119">Habilita o recorte no plano i.</span><span class="sxs-lookup"><span data-stu-id="4a41a-119">Enables clipping on plane i.</span></span>             |
| <span data-ttu-id="4a41a-120">**clipplane**(i, **CP \_ definir**, plano)</span><span class="sxs-lookup"><span data-stu-id="4a41a-120">**clipplane**( i, **CP\_DEFINE**, plane )</span></span> | <span data-ttu-id="4a41a-121">[**glClipPlane**](glclipplane.md) (GL do \_ remediador \_ , plano)</span><span class="sxs-lookup"><span data-stu-id="4a41a-121">[**glClipPlane**](glclipplane.md) ( GL\_CLIP\_PLANEi, plane )</span></span>                                | <span data-ttu-id="4a41a-122">Define o plano de recorte.</span><span class="sxs-lookup"><span data-stu-id="4a41a-122">Defines clipping plane.</span></span>                  |
|                                           | [<span data-ttu-id="4a41a-123">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="4a41a-123">**glGetClipPlane**</span></span>](glgetclipplane.md)                                                      | <span data-ttu-id="4a41a-124">Retorna a equação do plano de recorte.</span><span class="sxs-lookup"><span data-stu-id="4a41a-124">Returns clipping plane equation.</span></span>         |
|                                           | <span data-ttu-id="4a41a-125">[**glIsEnabled**](glisenabled.md) (GL \_ remediador \_ )</span><span class="sxs-lookup"><span data-stu-id="4a41a-125">[**glIsEnabled**](glisenabled.md) ( GL\_CLIP\_PLANEi )</span></span>                                       | <span data-ttu-id="4a41a-126">Retornará true se o plano de corte i estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="4a41a-126">Returns true if clip plane i is enabled.</span></span> |
| <span data-ttu-id="4a41a-127">**scrmask**</span><span class="sxs-lookup"><span data-stu-id="4a41a-127">**scrmask**</span></span>                               | [<span data-ttu-id="4a41a-128">**glScissor**</span><span class="sxs-lookup"><span data-stu-id="4a41a-128">**glScissor**</span></span>](glscissor.md)                                                                | <span data-ttu-id="4a41a-129">Define a caixa de tesoura.</span><span class="sxs-lookup"><span data-stu-id="4a41a-129">Defines the scissor box.</span></span>                 |
| <span data-ttu-id="4a41a-130">**getscrmask**</span><span class="sxs-lookup"><span data-stu-id="4a41a-130">**getscrmask**</span></span>                            | <span data-ttu-id="4a41a-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ caixa de tesoura GL \_ )</span><span class="sxs-lookup"><span data-stu-id="4a41a-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_SCISSOR\_BOX )</span></span> | <span data-ttu-id="4a41a-132">Retorna a caixa de tesoura atual.</span><span class="sxs-lookup"><span data-stu-id="4a41a-132">Returns the current scissor box.</span></span>         |



 

<span data-ttu-id="4a41a-133">Para ativar o teste de tesoura, chame **glEnable** usando \_ \_ a caixa de tesoura GL como o parâmetro.</span><span class="sxs-lookup"><span data-stu-id="4a41a-133">To turn on the scissor test, call **glEnable** using GL\_SCISSOR\_BOX as the parameter.</span></span>

<span data-ttu-id="4a41a-134">??</span><span class="sxs-lookup"><span data-stu-id="4a41a-134">??</span></span>

 

 




