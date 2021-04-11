---
title: Coângulos de portabilidade
description: Você pode desenhar três tipos de triângulos nos triângulos separados do OpenGL, nas faixas de triângulo e nos ventiladores de triângulo.
ms.assetid: 48617892-c9a0-4c67-b42e-afa4243023e7
keywords:
- Portabilidade do íris GL, triângulos
- portando do íris GL, triângulos
- portando para OpenGL do íris GL, triângulos
- Portabilidade do OpenGL do íris GL, triângulos
- funções de desenho, triângulos
- triângulos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad0c7a0af4b538bb951cf0d1c5f2e12b2e1badda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292436"
---
# <a name="porting-triangles"></a><span data-ttu-id="0fb02-109">Coângulos de portabilidade</span><span class="sxs-lookup"><span data-stu-id="0fb02-109">Porting Triangles</span></span>

<span data-ttu-id="0fb02-110">Você pode desenhar três tipos de triângulos em OpenGL: triângulos separados, faixas de triângulo e ventiladores de triângulo.</span><span class="sxs-lookup"><span data-stu-id="0fb02-110">You can draw three types of triangles in OpenGL: separate triangles, triangle strips, and triangle fans.</span></span>

<span data-ttu-id="0fb02-111">O OpenGL não tem nenhum equivalente para a função **swaptmesh** do íris GL.</span><span class="sxs-lookup"><span data-stu-id="0fb02-111">OpenGL has no equivalent for the IRIS GL **swaptmesh** function.</span></span> <span data-ttu-id="0fb02-112">Você pode obter o mesmo efeito usando uma combinação de triângulos, faixas de triângulo e ventiladores de triângulo.</span><span class="sxs-lookup"><span data-stu-id="0fb02-112">You can achieve the same effect using a combination of triangles, triangle strips, and triangle fans.</span></span>

<span data-ttu-id="0fb02-113">A tabela a seguir lista as funções do íris GL para desenhar triângulos e suas funções OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="0fb02-113">The following table lists the IRIS GL functions for drawing triangles and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="0fb02-114">Função GL de íris</span><span class="sxs-lookup"><span data-stu-id="0fb02-114">IRIS GL function</span></span>           | <span data-ttu-id="0fb02-115">Parâmetro glBegin equivalente</span><span class="sxs-lookup"><span data-stu-id="0fb02-115">Equivalent glBegin parameter</span></span> | <span data-ttu-id="0fb02-116">Significado</span><span class="sxs-lookup"><span data-stu-id="0fb02-116">Meaning</span></span>                                       |
|----------------------------|------------------------------|-----------------------------------------------|
|                            | <span data-ttu-id="0fb02-117">\_TRIângulos GL</span><span class="sxs-lookup"><span data-stu-id="0fb02-117">GL\_TRIANGLES</span></span>                | <span data-ttu-id="0fb02-118">As corridas de vértices interpretadas como triângulos.</span><span class="sxs-lookup"><span data-stu-id="0fb02-118">Triples of vertices interpreted as triangles.</span></span> |
| <span data-ttu-id="0fb02-119">**bgntmesh**, **endtmesh**</span><span class="sxs-lookup"><span data-stu-id="0fb02-119">**bgntmesh**, **endtmesh**</span></span> | <span data-ttu-id="0fb02-120">\_faixa de triângulo GL \_</span><span class="sxs-lookup"><span data-stu-id="0fb02-120">GL\_TRIANGLE\_STRIP</span></span>          | <span data-ttu-id="0fb02-121">Faixas vinculadas de triângulos.</span><span class="sxs-lookup"><span data-stu-id="0fb02-121">Linked strips of triangles.</span></span>                   |
|                            | <span data-ttu-id="0fb02-122">\_ \_ ventilador do triângulo GL</span><span class="sxs-lookup"><span data-stu-id="0fb02-122">GL\_TRIANGLE\_FAN</span></span>            | <span data-ttu-id="0fb02-123">Ventiladores vinculados de triângulos.</span><span class="sxs-lookup"><span data-stu-id="0fb02-123">Linked fans of triangles.</span></span>                     |



 

<span data-ttu-id="0fb02-124">??</span><span class="sxs-lookup"><span data-stu-id="0fb02-124">??</span></span>

 

 




