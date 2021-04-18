---
title: Usando as funções de consulta
description: Usando as funções de consulta
ms.assetid: 5f874a0e-77c0-4009-a18f-a852d7ffe891
keywords:
- OpenGL, funções de consulta
- funções de consulta OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14804b260451d4b51b0146b1cb2f796ba6b6778e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105780494"
---
# <a name="using-the-query-functions"></a><span data-ttu-id="62087-105">Usando as funções de consulta</span><span class="sxs-lookup"><span data-stu-id="62087-105">Using the Query Functions</span></span>

<span data-ttu-id="62087-106">Há quatro funções de consulta para obter variáveis de estado simples e uma para determinar se um estado específico está habilitado ou desabilitado:</span><span class="sxs-lookup"><span data-stu-id="62087-106">There are four query functions for obtaining simple state variables and one for determining whether a particular state is enabled or disabled:</span></span>

-   [<span data-ttu-id="62087-107">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="62087-107">**glGetBooleanv**</span></span>](glgetbooleanv.md)
-   [<span data-ttu-id="62087-108">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="62087-108">**glGetIntegerv**</span></span>](glgetintegerv.md)
-   [<span data-ttu-id="62087-109">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="62087-109">**glGetFloatv**</span></span>](glgetfloatv.md)
-   [<span data-ttu-id="62087-110">**glGetDoublev**</span><span class="sxs-lookup"><span data-stu-id="62087-110">**glGetDoublev**</span></span>](glgetdoublev.md)
-   [<span data-ttu-id="62087-111">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="62087-111">**glIsEnabled**</span></span>](glisenabled.md)

<span data-ttu-id="62087-112">Os protótipos para as funções de consulta são:</span><span class="sxs-lookup"><span data-stu-id="62087-112">The prototypes for the query functions are:</span></span>

<span data-ttu-id="62087-113">**void** **glGetBooleanv**(**GLenum** *pname* , **GLboolean \*** *params* );</span><span class="sxs-lookup"><span data-stu-id="62087-113">**void** **glGetBooleanv**(**GLenum** *pname* , **GLboolean \*** *params* );</span></span>

<span data-ttu-id="62087-114">**void** **glGetIntegerv**(**GLenum** *pname* , *parâmetros* de **GLint \*** );</span><span class="sxs-lookup"><span data-stu-id="62087-114">**void** **glGetIntegerv**(**GLenum** *pname* , **GLint \*** *params* );</span></span>

<span data-ttu-id="62087-115">**void** **glGetFloatv**(**GLenum** *pname* , **GLfloat \*** *params* );</span><span class="sxs-lookup"><span data-stu-id="62087-115">**void** **glGetFloatv**(**GLenum** *pname* , **GLfloat \*** *params* );</span></span>

<span data-ttu-id="62087-116">**void** **glGetDoublev**(**GLenum** *pname* , **GLdouble \*** *params* );</span><span class="sxs-lookup"><span data-stu-id="62087-116">**void** **glGetDoublev**(**GLenum** *pname* , **GLdouble \*** *params* );</span></span>

<span data-ttu-id="62087-117">Respectivamente, as funções de consulta obtêm variáveis de estado booliano, inteiro, ponto flutuante ou de precisão dupla.</span><span class="sxs-lookup"><span data-stu-id="62087-117">Respectively, the query functions obtain Boolean, integer, floating-point, or double-precision state variables.</span></span> <span data-ttu-id="62087-118">O parâmetro *pname* é uma constante simbólica que indica a variável de estado a ser retornada, e *params* é um ponteiro para uma matriz do tipo indicado no qual os dados retornados serão colocados.</span><span class="sxs-lookup"><span data-stu-id="62087-118">The *pname* parameter is a symbolic constant indicating the state variable to return, and *params* is a pointer to an array of the indicated type in which to place the returned data.</span></span> <span data-ttu-id="62087-119">Os valores possíveis para *pname* são listados em [variáveis de estado OpenGL](opengl-state-variables.md).</span><span class="sxs-lookup"><span data-stu-id="62087-119">The possible values for *pname* are listed in [OpenGL State Variables](opengl-state-variables.md).</span></span> <span data-ttu-id="62087-120">Uma conversão de tipo é executada, se necessário, para retornar a variável desejada como o tipo de dados solicitado.</span><span class="sxs-lookup"><span data-stu-id="62087-120">A type conversion is performed if necessary to return the desired variable as the requested data type.</span></span>

<span data-ttu-id="62087-121">O protótipo para [**glIsEnabled**](glisenabled.md) é:</span><span class="sxs-lookup"><span data-stu-id="62087-121">The prototype for [**glIsEnabled**](glisenabled.md) is:</span></span>

<span data-ttu-id="62087-122">**GLboolean** **glIsEnabled**(GLenum *Cap* );</span><span class="sxs-lookup"><span data-stu-id="62087-122">**GLboolean** **glIsEnabled**(GLenum *cap* );</span></span>

<span data-ttu-id="62087-123">Se o modo especificado por *Cap* estiver habilitado, **glIsEnabled** retornará GL \_ true.</span><span class="sxs-lookup"><span data-stu-id="62087-123">If the mode specified by *cap* is enabled, **glIsEnabled** returns GL\_TRUE.</span></span> <span data-ttu-id="62087-124">Se o modo especificado por *Cap* estiver desabilitado, **glIsEnabled** retornará GL \_ false.</span><span class="sxs-lookup"><span data-stu-id="62087-124">If the mode specified by *cap* is disabled, **glIsEnabled** returns GL\_FALSE.</span></span> <span data-ttu-id="62087-125">Os valores possíveis para *Cap* são listados em [variáveis de estado OpenGL](opengl-state-variables.md).</span><span class="sxs-lookup"><span data-stu-id="62087-125">The possible values for *cap* are listed in [OpenGL State Variables](opengl-state-variables.md).</span></span>

<span data-ttu-id="62087-126">Outras funções especializadas retornam variáveis de estado específicas.</span><span class="sxs-lookup"><span data-stu-id="62087-126">Other specialized functions return specific state variables.</span></span> <span data-ttu-id="62087-127">Para descobrir quando usar essas funções, consulte variáveis de estado OpenGL e o *manual de referência OpenGL*.</span><span class="sxs-lookup"><span data-stu-id="62087-127">To find out when to use these functions, see OpenGL State Variables and the *OpenGL Reference Manual*.</span></span> <span data-ttu-id="62087-128">Para obter mais informações sobre o recurso de tratamento de erros do OpenGL e a função **glGetError** , consulte [tratamento de erros](error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="62087-128">For more information on OpenGL's error handling facility and the **glGetError** function, see [Error Handling](error-handling.md).</span></span>

<span data-ttu-id="62087-129">As funções que retornam variáveis de estado específicas são:</span><span class="sxs-lookup"><span data-stu-id="62087-129">The functions that return specific state variables are:</span></span>

-   [<span data-ttu-id="62087-130">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="62087-130">**glGetClipPlane**</span></span>](glgetclipplane.md)
-   [<span data-ttu-id="62087-131">**glGetError**</span><span class="sxs-lookup"><span data-stu-id="62087-131">**glGetError**</span></span>](glgeterror.md)
-   [<span data-ttu-id="62087-132">**glGetLight**</span><span class="sxs-lookup"><span data-stu-id="62087-132">**glGetLight**</span></span>](glgetlight.md)
-   [<span data-ttu-id="62087-133">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="62087-133">**glGetMap**</span></span>](glgetmap.md)
-   [<span data-ttu-id="62087-134">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="62087-134">**glGetMaterial**</span></span>](glgetmaterial.md)
-   [<span data-ttu-id="62087-135">**glGetPixelMap**</span><span class="sxs-lookup"><span data-stu-id="62087-135">**glGetPixelMap**</span></span>](glgetpixelmap.md)
-   [<span data-ttu-id="62087-136">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="62087-136">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md)
-   [<span data-ttu-id="62087-137">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="62087-137">**glGetString**</span></span>](glgetstring.md)
-   [<span data-ttu-id="62087-138">**glGetTexEnv**</span><span class="sxs-lookup"><span data-stu-id="62087-138">**glGetTexEnv**</span></span>](glgettexenv.md)
-   [<span data-ttu-id="62087-139">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="62087-139">**glGetTexGen**</span></span>](glgettexgen.md)
-   [<span data-ttu-id="62087-140">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="62087-140">**glGetTexImage**</span></span>](glgetteximage.md)
-   [<span data-ttu-id="62087-141">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="62087-141">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md)
-   [<span data-ttu-id="62087-142">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="62087-142">**glGetTexParameter**</span></span>](glgettexparameter.md)

 

 




