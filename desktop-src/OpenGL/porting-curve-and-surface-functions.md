---
title: Funções de curva e superfície de portabilidade
description: Funções de curva e superfície de portabilidade
ms.assetid: 2e80f742-6665-4e7c-a8a1-c43c4764ccc8
keywords:
- Portabilidade do íris GL, curvas
- portando do íris GL, curvas
- portando para OpenGL do íris GL, curvas
- Portabilidade OpenGL do íris GL, curvas
- Portabilidade do íris GL, patches da superfície
- portando do íris GL, patches de superfície
- portando para OpenGL do íris GL, patches de superfície
- Portabilidade OpenGL do íris GL, patches de superfície
- curvas
- patches da superfície
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3caedc89697d1c83325a00b3dc1cb55c34612e64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291896"
---
# <a name="porting-curve-and-surface-functions"></a><span data-ttu-id="1f572-113">Funções de curva e superfície de portabilidade</span><span class="sxs-lookup"><span data-stu-id="1f572-113">Porting Curve and Surface Functions</span></span>

<span data-ttu-id="1f572-114">O OpenGL não dá suporte a equivalentes às funções da íris GL para as curvas e os patches de superfície.</span><span class="sxs-lookup"><span data-stu-id="1f572-114">OpenGL doesn't support equivalents to the IRIS GL functions for curves and surface patches.</span></span> <span data-ttu-id="1f572-115">Você precisará reescrever seu código se ele incluir qualquer uma das seguintes chamadas:</span><span class="sxs-lookup"><span data-stu-id="1f572-115">You'll need to rewrite your code if it includes any of the following calls:</span></span>

-   <span data-ttu-id="1f572-116">**defbasis**</span><span class="sxs-lookup"><span data-stu-id="1f572-116">**defbasis**</span></span>
-   <span data-ttu-id="1f572-117">**curvebasis**, **curveprecision**, **CRV**, **crvn**, **rcrv**, **rcrvn** e **curveit**</span><span class="sxs-lookup"><span data-stu-id="1f572-117">**curvebasis**, **curveprecision**, **crv**, **crvn**, **rcrv**, **rcrvn**, and **curveit**</span></span>
-   <span data-ttu-id="1f572-118">**patchbasis**, **patchcurves**, **patchprecision**, **patch** e **rpatch**</span><span class="sxs-lookup"><span data-stu-id="1f572-118">**patchbasis**, **patchcurves**, **patchprecision**, **patch**, and **rpatch**</span></span>

<span data-ttu-id="1f572-119">Este tópico inclui informações sobre o seguinte.</span><span class="sxs-lookup"><span data-stu-id="1f572-119">This topic includes information on the following.</span></span>

-   [<span data-ttu-id="1f572-120">Portando objetos NURBS</span><span class="sxs-lookup"><span data-stu-id="1f572-120">Porting NURBS Objects</span></span>](porting-nurbs-objects.md)
-   [<span data-ttu-id="1f572-121">Portando curvas NURBS</span><span class="sxs-lookup"><span data-stu-id="1f572-121">Porting NURBS Curves</span></span>](porting-nurbs-curves.md)
-   [<span data-ttu-id="1f572-122">Transportando curvas de corte</span><span class="sxs-lookup"><span data-stu-id="1f572-122">Porting Trimming Curves</span></span>](porting-trimming-curves.md)
-   [<span data-ttu-id="1f572-123">Portando superfícies NURBS</span><span class="sxs-lookup"><span data-stu-id="1f572-123">Porting NURBS Surfaces</span></span>](porting-nurbs-surfaces.md)

 

 




