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
ms.openlocfilehash: 8329fd34fc68122be8d63e4dc28756f88faf7797
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120681"
---
# <a name="obtaining-state-information"></a><span data-ttu-id="6f07e-106">Obtendo informações de estado</span><span class="sxs-lookup"><span data-stu-id="6f07e-106">Obtaining State Information</span></span>

<span data-ttu-id="6f07e-107">O OpenGL mantém muitas variáveis de estado que afetam o comportamento de muitas funções.</span><span class="sxs-lookup"><span data-stu-id="6f07e-107">OpenGL maintains many state variables that affect the behavior of many functions.</span></span> <span data-ttu-id="6f07e-108">Algumas dessas variáveis têm funções de consulta especializadas.</span><span class="sxs-lookup"><span data-stu-id="6f07e-108">Some of these variables have specialized query functions.</span></span>

:::row:::
    :::column:::
        [<span data-ttu-id="6f07e-109">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="6f07e-109">**glGetClipPlane**</span></span>](glgetclipplane.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="6f07e-110">**glGetPixelMap**</span><span class="sxs-lookup"><span data-stu-id="6f07e-110">**glGetPixelMap**</span></span>](glgetpixelmap.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="6f07e-111">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="6f07e-111">**glGetTexImage**</span></span>](glgetteximage.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [<span data-ttu-id="6f07e-112">**glGetLight**</span><span class="sxs-lookup"><span data-stu-id="6f07e-112">**glGetLight**</span></span>](glgetlight.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="6f07e-113">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="6f07e-113">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="6f07e-114">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="6f07e-114">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [<span data-ttu-id="6f07e-115">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="6f07e-115">**glGetMap**</span></span>](glgetmap.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="6f07e-116">**glGetTexEnv**</span><span class="sxs-lookup"><span data-stu-id="6f07e-116">**glGetTexEnv**</span></span>](glgettexenv.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="6f07e-117">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="6f07e-117">**glGetTexParameter**</span></span>](glgettexparameter.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [<span data-ttu-id="6f07e-118">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="6f07e-118">**glGetMaterial**</span></span>](glgetmaterial.md)
    :::column-end:::
    :::column:::
        [<span data-ttu-id="6f07e-119">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="6f07e-119">**glGetTexGen**</span></span>](glgettexgen.md)
    :::column-end:::
    :::column:::

    :::column-end:::
:::row-end:::

<span data-ttu-id="6f07e-120">Para obter o valor de outras variáveis de estado, use [**glGetBooleanv**](glgetbooleanv.md), [**glGetDoublev**](glgetdoublev.md), [**glGetFloatv**](glgetfloatv.md)ou [**glGetIntegerv**](glgetintegerv.md), conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="6f07e-120">To obtain the value of other state variables, use [**glGetBooleanv**](glgetbooleanv.md), [**glGetDoublev**](glgetdoublev.md), [**glGetFloatv**](glgetfloatv.md), or [**glGetIntegerv**](glgetintegerv.md), as appropriate.</span></span> <span data-ttu-id="6f07e-121">Consulte [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) para obter informações sobre como usar essas funções.</span><span class="sxs-lookup"><span data-stu-id="6f07e-121">See [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) for information about how to use these functions.</span></span> <span data-ttu-id="6f07e-122">Outras funções de consulta que você talvez queira usar são [**glGetError**](glgeterror.md), [**glGetString**](glgetstring.md)e [**glIsEnabled**](glisenabled.md).</span><span class="sxs-lookup"><span data-stu-id="6f07e-122">Other query functions you might want to use are [**glGetError**](glgeterror.md), [**glGetString**](glgetstring.md), and [**glIsEnabled**](glisenabled.md).</span></span> <span data-ttu-id="6f07e-123">(Consulte [tratamento de erros](handling-errors.md) para obter mais informações sobre as funções relacionadas ao tratamento de erros.) Para salvar e restaurar conjuntos de variáveis de estado, use [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="6f07e-123">(See [Handling Errors](handling-errors.md) for more information about functions related to error handling.) To save and restore sets of state variables, use [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md).</span></span>

-   [<span data-ttu-id="6f07e-124">Usando as funções de consulta</span><span class="sxs-lookup"><span data-stu-id="6f07e-124">Using the Query Functions</span></span>](using-the-query-functions.md)
-   [<span data-ttu-id="6f07e-125">Tratamento de erro</span><span class="sxs-lookup"><span data-stu-id="6f07e-125">Error Handling</span></span>](error-handling.md)
-   [<span data-ttu-id="6f07e-126">Códigos de erro OpenGL</span><span class="sxs-lookup"><span data-stu-id="6f07e-126">OpenGL Error Codes</span></span>](opengl-error-codes.md)
-   [<span data-ttu-id="6f07e-127">Salvando e restaurando conjuntos de variáveis de estado</span><span class="sxs-lookup"><span data-stu-id="6f07e-127">Saving and Restoring Sets of State Variables</span></span>](saving-and-restoring-sets-of-state-variables.md)
-   [<span data-ttu-id="6f07e-128">Variáveis de estado OpenGL</span><span class="sxs-lookup"><span data-stu-id="6f07e-128">OpenGL State Variables</span></span>](opengl-state-variables.md)
-   [<span data-ttu-id="6f07e-129">Referência de informações de estado</span><span class="sxs-lookup"><span data-stu-id="6f07e-129">State Information Reference</span></span>](state-information-reference.md)

 

 




