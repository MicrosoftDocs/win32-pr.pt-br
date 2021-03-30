---
title: Obtendo informações de estado
description: Obtendo informações de estado
ms.assetid: 86fc8503-92b9-4b5b-8a28-4c9783983ac6
keywords:
- OpenGL, informações de estado
- OpenGL, variáveis de estado
- informações de estado OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfac92233e971104fd4d343970a9ecc79496ed54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635641"
---
# <a name="obtaining-state-information"></a><span data-ttu-id="8a891-106">Obtendo informações de estado</span><span class="sxs-lookup"><span data-stu-id="8a891-106">Obtaining State Information</span></span>

<span data-ttu-id="8a891-107">O OpenGL mantém muitas variáveis de estado que afetam o comportamento de muitas funções.</span><span class="sxs-lookup"><span data-stu-id="8a891-107">OpenGL maintains many state variables that affect the behavior of many functions.</span></span> <span data-ttu-id="8a891-108">Algumas dessas variáveis têm funções de consulta especializadas.</span><span class="sxs-lookup"><span data-stu-id="8a891-108">Some of these variables have specialized query functions.</span></span>



|                                          |                                                    |                                                          |
|------------------------------------------|----------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="8a891-109">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="8a891-109">**glGetClipPlane**</span></span>](glgetclipplane.md) | [<span data-ttu-id="8a891-110">**glGetPixelMap**</span><span class="sxs-lookup"><span data-stu-id="8a891-110">**glGetPixelMap**</span></span>](glgetpixelmap.md)             | [<span data-ttu-id="8a891-111">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="8a891-111">**glGetTexImage**</span></span>](glgetteximage.md)                   |
| [<span data-ttu-id="8a891-112">**glGetLight**</span><span class="sxs-lookup"><span data-stu-id="8a891-112">**glGetLight**</span></span>](glgetlight.md)         | [<span data-ttu-id="8a891-113">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="8a891-113">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md) | [<span data-ttu-id="8a891-114">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="8a891-114">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |
| [<span data-ttu-id="8a891-115">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="8a891-115">**glGetMap**</span></span>](glgetmap.md)             | [<span data-ttu-id="8a891-116">**glGetTexEnv**</span><span class="sxs-lookup"><span data-stu-id="8a891-116">**glGetTexEnv**</span></span>](glgettexenv.md)                 | [<span data-ttu-id="8a891-117">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="8a891-117">**glGetTexParameter**</span></span>](glgettexparameter.md)           |
| [<span data-ttu-id="8a891-118">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="8a891-118">**glGetMaterial**</span></span>](glgetmaterial.md)   | [<span data-ttu-id="8a891-119">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="8a891-119">**glGetTexGen**</span></span>](glgettexgen.md)                 |                                                          |



 

<span data-ttu-id="8a891-120">Para obter o valor de outras variáveis de estado, use [**glGetBooleanv**](glgetbooleanv.md), [**glGetDoublev**](glgetdoublev.md), [**glGetFloatv**](glgetfloatv.md)ou [**glGetIntegerv**](glgetintegerv.md), conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="8a891-120">To obtain the value of other state variables, use [**glGetBooleanv**](glgetbooleanv.md), [**glGetDoublev**](glgetdoublev.md), [**glGetFloatv**](glgetfloatv.md), or [**glGetIntegerv**](glgetintegerv.md), as appropriate.</span></span> <span data-ttu-id="8a891-121">Consulte [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) para obter informações sobre como usar essas funções.</span><span class="sxs-lookup"><span data-stu-id="8a891-121">See [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) for information about how to use these functions.</span></span> <span data-ttu-id="8a891-122">Outras funções de consulta que você talvez queira usar são [**glGetError**](glgeterror.md), [**glGetString**](glgetstring.md)e [**glIsEnabled**](glisenabled.md).</span><span class="sxs-lookup"><span data-stu-id="8a891-122">Other query functions you might want to use are [**glGetError**](glgeterror.md), [**glGetString**](glgetstring.md), and [**glIsEnabled**](glisenabled.md).</span></span> <span data-ttu-id="8a891-123">(Consulte [tratamento de erros](handling-errors.md) para obter mais informações sobre as funções relacionadas ao tratamento de erros.) Para salvar e restaurar conjuntos de variáveis de estado, use [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="8a891-123">(See [Handling Errors](handling-errors.md) for more information about functions related to error handling.) To save and restore sets of state variables, use [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md).</span></span>

-   [<span data-ttu-id="8a891-124">Usando as funções de consulta</span><span class="sxs-lookup"><span data-stu-id="8a891-124">Using the Query Functions</span></span>](using-the-query-functions.md)
-   [<span data-ttu-id="8a891-125">Tratamento de erro</span><span class="sxs-lookup"><span data-stu-id="8a891-125">Error Handling</span></span>](error-handling.md)
-   [<span data-ttu-id="8a891-126">Códigos de erro OpenGL</span><span class="sxs-lookup"><span data-stu-id="8a891-126">OpenGL Error Codes</span></span>](opengl-error-codes.md)
-   [<span data-ttu-id="8a891-127">Salvando e restaurando conjuntos de variáveis de estado</span><span class="sxs-lookup"><span data-stu-id="8a891-127">Saving and Restoring Sets of State Variables</span></span>](saving-and-restoring-sets-of-state-variables.md)
-   [<span data-ttu-id="8a891-128">Variáveis de estado OpenGL</span><span class="sxs-lookup"><span data-stu-id="8a891-128">OpenGL State Variables</span></span>](opengl-state-variables.md)
-   [<span data-ttu-id="8a891-129">Referência de informações de estado</span><span class="sxs-lookup"><span data-stu-id="8a891-129">State Information Reference</span></span>](state-information-reference.md)

 

 




