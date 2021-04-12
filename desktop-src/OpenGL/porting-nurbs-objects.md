---
title: Portando objetos NURBS
description: O OpenGL trata a NURBS como objetos, semelhante ao modo como ele trata quadrics você cria um objeto NURBS e, em seguida, especifica como ele deve ser renderizado. A tabela a seguir lista as funções OpenGL GLU para gerenciar objetos NURBS.
ms.assetid: baddf81b-219f-44bb-aa17-37404028b258
keywords:
- Portabilidade do íris GL, objetos NURBS
- portando de objetos íris GL, NURBS
- portando para OpenGL do íris GL, objetos NURBS
- Portabilidade OpenGL do íris GL, objetos NURBS
- Objetos NURBS
- NURBS (B racional não uniforme-spline)
- B-spline racional não uniforme (NURBS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0e56c06eea4e4a9a48f9062205277f8b999499
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364175"
---
# <a name="porting-nurbs-objects"></a><span data-ttu-id="8a987-111">Portando objetos NURBS</span><span class="sxs-lookup"><span data-stu-id="8a987-111">Porting NURBS Objects</span></span>

<span data-ttu-id="8a987-112">O OpenGL trata a NURBS como objetos, semelhante ao modo como ele trata quadrics: você cria um objeto NURBS e, em seguida, especifica como ele deve ser renderizado.</span><span class="sxs-lookup"><span data-stu-id="8a987-112">OpenGL treats NURBS as objects, similar to the way it treats quadrics: you create a NURBS object and then specify how it should be rendered.</span></span> <span data-ttu-id="8a987-113">A tabela a seguir lista as funções OpenGL GLU para gerenciar objetos NURBS.</span><span class="sxs-lookup"><span data-stu-id="8a987-113">The following table lists the OpenGL GLU functions for managing NURBS objects.</span></span>



| <span data-ttu-id="8a987-114">Função OpenGL GLU</span><span class="sxs-lookup"><span data-stu-id="8a987-114">OpenGL GLU function</span></span>                                      | <span data-ttu-id="8a987-115">Significado</span><span class="sxs-lookup"><span data-stu-id="8a987-115">Meaning</span></span>                                                        |
|----------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="8a987-116">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="8a987-116">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)       | <span data-ttu-id="8a987-117">Cria um novo objeto NURBS.</span><span class="sxs-lookup"><span data-stu-id="8a987-117">Creates a new NURBS object.</span></span>                                    |
| [<span data-ttu-id="8a987-118">**gluDeleteNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="8a987-118">**gluDeleteNurbsRenderer**</span></span>](gludeletenurbsrenderer.md) | <span data-ttu-id="8a987-119">Exclui um objeto NURBS.</span><span class="sxs-lookup"><span data-stu-id="8a987-119">Deletes a NURBS object.</span></span>                                        |
| [<span data-ttu-id="8a987-120">*gluNurbsCallback*</span><span class="sxs-lookup"><span data-stu-id="8a987-120">*gluNurbsCallback*</span></span>](glunurbs.md)                       | <span data-ttu-id="8a987-121">Associa um retorno de chamada com um objeto NURBS, para tratamento de erros.</span><span class="sxs-lookup"><span data-stu-id="8a987-121">Associates a callback with a NURBS object, for error handling.</span></span> |



 

<span data-ttu-id="8a987-122">Ao portar o código NURBS do íris GL para OpenGL, tenha em mente os seguintes pontos:</span><span class="sxs-lookup"><span data-stu-id="8a987-122">When porting IRIS GL NURBS code to OpenGL, keep the following points in mind:</span></span>

-   <span data-ttu-id="8a987-123">Pontos de controle NURBS são floats, não duplos.</span><span class="sxs-lookup"><span data-stu-id="8a987-123">NURBS control points are floats, not doubles.</span></span>
-   <span data-ttu-id="8a987-124">O parâmetro Stride é contado em floats, não em bytes.</span><span class="sxs-lookup"><span data-stu-id="8a987-124">The stride parameter is counted in floats, not bytes.</span></span>
-   <span data-ttu-id="8a987-125">Se você estiver usando a iluminação e não estiver especificando normais, chame [**glEnable**](glenable.md) com o GL \_ auto \_ normal como o parâmetro para gerar normais automaticamente.</span><span class="sxs-lookup"><span data-stu-id="8a987-125">If you're using lighting and you're not specifying normals, call [**glEnable**](glenable.md) with GL\_AUTO\_NORMAL as the parameter to generate normals automatically.</span></span>

<span data-ttu-id="8a987-126">??</span><span class="sxs-lookup"><span data-stu-id="8a987-126">??</span></span>

 

 




