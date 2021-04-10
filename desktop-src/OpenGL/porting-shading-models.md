---
title: Modelos de sombreamento de portador
description: Como o íris GL, o OpenGL permite alternar entre sombreamento suave (Gouraud) e sombreamento simples. A tabela a seguir lista as funções de pontilhamento e sombreamento da íris GL e suas funções OpenGL equivalentes.
ms.assetid: 93e8f437-381f-4620-ad6f-52ce830d99b6
keywords:
- Portabilidade do íris GL, sombreamento
- portando do íris GL, sombreamento
- portando para OpenGL do íris GL, sombreamento
- Portabilidade do OpenGL do íris GL, sombreamento
- sombreamento suave
- Sombreamento Gouraud
- sombreamento simples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 124bb002f6f133b4d47dd40e1a0e8738c512ce99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292440"
---
# <a name="porting-shading-models"></a><span data-ttu-id="faa51-111">Modelos de sombreamento de portador</span><span class="sxs-lookup"><span data-stu-id="faa51-111">Porting Shading Models</span></span>

<span data-ttu-id="faa51-112">Como o íris GL, o OpenGL permite alternar entre sombreamento suave (Gouraud) e sombreamento simples.</span><span class="sxs-lookup"><span data-stu-id="faa51-112">Like IRIS GL, OpenGL lets you switch between smooth (Gouraud) shading and flat shading.</span></span> <span data-ttu-id="faa51-113">A tabela a seguir lista as funções de pontilhamento e sombreamento da íris GL e suas funções OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="faa51-113">The following table lists the IRIS GL shading and dithering functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="faa51-114">Função GL de íris</span><span class="sxs-lookup"><span data-stu-id="faa51-114">IRIS GL function</span></span>                                   | <span data-ttu-id="faa51-115">Função OpenGL</span><span class="sxs-lookup"><span data-stu-id="faa51-115">OpenGL function</span></span>                                                                                    | <span data-ttu-id="faa51-116">Significado</span><span class="sxs-lookup"><span data-stu-id="faa51-116">Meaning</span></span>                      |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="faa51-117">**shademodel**(simples)</span><span class="sxs-lookup"><span data-stu-id="faa51-117">**shademodel**(FLAT)</span></span>                               | <span data-ttu-id="faa51-118">[**glShadeModel**](glshademodel.md) (GL \_ simples)</span><span class="sxs-lookup"><span data-stu-id="faa51-118">[**glShadeModel**](glshademodel.md) ( GL\_FLAT )</span></span>                                                  | <span data-ttu-id="faa51-119">O sombreamento simples.</span><span class="sxs-lookup"><span data-stu-id="faa51-119">Does flat shading.</span></span>           |
| <span data-ttu-id="faa51-120">**shademodel**(GOURAUD)</span><span class="sxs-lookup"><span data-stu-id="faa51-120">**shademodel**(GOURAUD)</span></span>                            | <span data-ttu-id="faa51-121">**glShadeModel**(GL \_ suave)</span><span class="sxs-lookup"><span data-stu-id="faa51-121">**glShadeModel**( GL\_SMOOTH )</span></span>                                                                     | <span data-ttu-id="faa51-122">O sombreamento suave.</span><span class="sxs-lookup"><span data-stu-id="faa51-122">Does smooth shading.</span></span>         |
| <span data-ttu-id="faa51-123">**obter**</span><span class="sxs-lookup"><span data-stu-id="faa51-123">**getsm**</span></span>                                          | <span data-ttu-id="faa51-124">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ modelo de sombreamento GL \_ )</span><span class="sxs-lookup"><span data-stu-id="faa51-124">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_SHADE\_MODEL )</span></span>      | <span data-ttu-id="faa51-125">Retorna o modelo de sombra atual.</span><span class="sxs-lookup"><span data-stu-id="faa51-125">Returns current shade model.</span></span> |
| <span data-ttu-id="faa51-126">**pontilhamento (DT**) de pontilhamento \_ (DT  \_ desativado)</span><span class="sxs-lookup"><span data-stu-id="faa51-126">**dither**(DT\_ON) **dither**(DT\_OFF)</span></span> <br/> | <span data-ttu-id="faa51-127">[**glEnable**](glenable.md) ( \_ pontilhamento GL [**) glDisable**](gldisable.md)( \_ pontilhamento GL)</span><span class="sxs-lookup"><span data-stu-id="faa51-127">[**glEnable**](glenable.md) ( GL\_DITHER )[**glDisable**](gldisable.md)( GL\_DITHER )</span></span><br/> | <span data-ttu-id="faa51-128">Ativa/desativa o pontilhamento.</span><span class="sxs-lookup"><span data-stu-id="faa51-128">Turns dithering on/off.</span></span>      |



 

<span data-ttu-id="faa51-129">??</span><span class="sxs-lookup"><span data-stu-id="faa51-129">??</span></span>

 

 





