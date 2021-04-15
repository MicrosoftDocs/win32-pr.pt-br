---
title: Especificando retornos de chamada
description: Você pode especificar até cinco funções de retorno de chamada para um mosaico.
ms.assetid: b49a8400-8111-450d-a2d7-c313a898a213
keywords:
- Utilitário OpenGL (GLU), especificando funções de retorno de chamada
- GLU (utilitário OpenGL), especificando funções de retorno de chamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6086448cf6f4a71ea6a49359d5656f12f613d760
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498791"
---
# <a name="specifying-callbacks"></a><span data-ttu-id="04d27-105">Especificando retornos de chamada</span><span class="sxs-lookup"><span data-stu-id="04d27-105">Specifying Callbacks</span></span>

<span data-ttu-id="04d27-106">Você pode especificar até cinco funções de retorno de chamada para um mosaico.</span><span class="sxs-lookup"><span data-stu-id="04d27-106">You can specify up to five callback functions for a tessellation.</span></span> <span data-ttu-id="04d27-107">Qualquer função que você não especificar não será chamada durante o mosaico e você não obterá nenhuma informação que possa ter retornado.</span><span class="sxs-lookup"><span data-stu-id="04d27-107">Any functions that you do not specify are not called during the tessellation, and you do not get any information they might have returned.</span></span> <span data-ttu-id="04d27-108">Você especifica as funções de retorno de chamada com [*gluTessCallback*](glutess.md).</span><span class="sxs-lookup"><span data-stu-id="04d27-108">You specify the callback functions with [*gluTessCallback*](glutess.md).</span></span>

<span data-ttu-id="04d27-109">A função **gluTessCallback** associa a função de retorno de chamada *FN* com o objeto de mosaico *tessobj*.</span><span class="sxs-lookup"><span data-stu-id="04d27-109">The **gluTessCallback** function associates the callback function *fn* with the tessellation object *tessobj*.</span></span> <span data-ttu-id="04d27-110">O tipo de retorno de chamada é determinado pelo *tipo* de parâmetro, que pode **ser \_ Glu Begin**, **Glu \_ \_ flag de borda**, **Glu \_ Vertex**, **Glu \_ end** ou **Glu \_ Error**.</span><span class="sxs-lookup"><span data-stu-id="04d27-110">The type of the callback is determined by the parameter *type*, which can be **GLU\_BEGIN**, **GLU\_EDGE\_FLAG**, **GLU\_VERTEX**, **GLU\_END**, or **GLU\_ERROR**.</span></span> <span data-ttu-id="04d27-111">As cinco funções de retorno de chamada possíveis têm os seguintes protótipos.</span><span class="sxs-lookup"><span data-stu-id="04d27-111">The five possible callback functions have the following prototypes.</span></span>



| <span data-ttu-id="04d27-112">Função de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="04d27-112">Callback function</span></span>   | <span data-ttu-id="04d27-113">Protótipo</span><span class="sxs-lookup"><span data-stu-id="04d27-113">Prototype</span></span>                                    |
|---------------------|----------------------------------------------|
| <span data-ttu-id="04d27-114">**início do GLU \_**</span><span class="sxs-lookup"><span data-stu-id="04d27-114">**GLU\_BEGIN**</span></span>      | <span data-ttu-id="04d27-115">**void** **begin**(\**GLenum \* \* \* Type* );</span><span class="sxs-lookup"><span data-stu-id="04d27-115">**void** **begin**(\**GLenum\*\*\*type* );</span></span>       |
| <span data-ttu-id="04d27-116">**\_sinalizador de borda Glu \_**</span><span class="sxs-lookup"><span data-stu-id="04d27-116">**GLU\_EDGE\_FLAG**</span></span> | <span data-ttu-id="04d27-117">**void** **EdgeFlag**(\**GLboolean \* \* \* sinalizador* );</span><span class="sxs-lookup"><span data-stu-id="04d27-117">**void** **edgeFlag**(\**GLboolean\*\*\*flag* );</span></span> |
| <span data-ttu-id="04d27-118">**\_vértice Glu**</span><span class="sxs-lookup"><span data-stu-id="04d27-118">**GLU\_VERTEX**</span></span>     | <span data-ttu-id="04d27-119"> **vértice** nulo \(**void \*\ *\ *\ * dados* );</span><span class="sxs-lookup"><span data-stu-id="04d27-119">**void** **vertex**(\**void \*\*\*\*data* );</span></span>     |
| <span data-ttu-id="04d27-120">**GLU \_ fim**</span><span class="sxs-lookup"><span data-stu-id="04d27-120">**GLU\_END**</span></span>        | <span data-ttu-id="04d27-121">**anular** **término**( *void* );</span><span class="sxs-lookup"><span data-stu-id="04d27-121">**void** **end**( *void* );</span></span>                  |
| <span data-ttu-id="04d27-122">**erro de GLU \_**</span><span class="sxs-lookup"><span data-stu-id="04d27-122">**GLU\_ERROR**</span></span>      | <span data-ttu-id="04d27-123"> **erro** de void \(**GLenum\ *\ *\ * errno* );</span><span class="sxs-lookup"><span data-stu-id="04d27-123">**void** **error**(\**GLenum\*\*\*errno* );</span></span>      |



 

<span data-ttu-id="04d27-124">Para alterar uma função de retorno de chamada, chame [*gluTessCallback*](glutess.md) com a nova função.</span><span class="sxs-lookup"><span data-stu-id="04d27-124">To change a callback function, call [*gluTessCallback*](glutess.md) with the new function.</span></span> <span data-ttu-id="04d27-125">Para eliminar uma função de retorno de chamada sem substituí-la por uma nova, passe **gluTessCallback** um ponteiro nulo para a função apropriada.</span><span class="sxs-lookup"><span data-stu-id="04d27-125">To eliminate a callback function without replacing it with a new one, pass **gluTessCallback** a null pointer for the appropriate function.</span></span>

<span data-ttu-id="04d27-126">Como o mosaico prossegue, as funções de retorno de chamada são chamadas de forma semelhante à forma como você usaria as funções OpenGL [**glBegin**](glbegin.md), [glEdgeFlag](gledgeflag-functions.md), [glVertex](glvertex-functions.md)e [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="04d27-126">As tessellation proceeds, the callback functions are called in a manner similar to the way you would use the OpenGL functions [**glBegin**](glbegin.md), [glEdgeFlag](gledgeflag-functions.md), [glVertex](glvertex-functions.md), and [**glEnd**](glend.md).</span></span>

<span data-ttu-id="04d27-127">A função de retorno de chamada **Glu \_ begin** é invocada com um dos três parâmetros possíveis:</span><span class="sxs-lookup"><span data-stu-id="04d27-127">The **GLU\_BEGIN** callback function is invoked with one of three possible parameters:</span></span>

-   <span data-ttu-id="04d27-128">\_ \_ ventilador do triângulo GL</span><span class="sxs-lookup"><span data-stu-id="04d27-128">GL\_TRIANGLE\_FAN</span></span>
-   <span data-ttu-id="04d27-129">\_faixa de triângulo GL \_</span><span class="sxs-lookup"><span data-stu-id="04d27-129">GL\_TRIANGLE\_STRIP</span></span>
-   <span data-ttu-id="04d27-130">\_TRIângulos GL</span><span class="sxs-lookup"><span data-stu-id="04d27-130">GL\_TRIANGLES</span></span>

<span data-ttu-id="04d27-131">Depois de chamar a função de retorno de chamada **Glu \_ begin** e antes de chamar a função de retorno de chamada associada ao **\_ término de Glu**, uma combinação do **\_ \_ sinalizador de borda Glu** e retornos de chamada de **\_ vértice Glu** é invocada.</span><span class="sxs-lookup"><span data-stu-id="04d27-131">After calling the **GLU\_BEGIN** callback function, and before calling the callback function associated with **GLU\_END**, some combination of the **GLU\_EDGE\_FLAG** and **GLU\_VERTEX** callbacks is invoked.</span></span> <span data-ttu-id="04d27-132">Os vértices associados e os sinalizadores de borda são interpretados exatamente como estão no OpenGL entre **glBegin**( \_ \_ ventilador do triângulo GL), **glBegin**(faixa de \_ triângulo GL \_ ) ou **glBegin**( \_ triângulos GL **)** e **glEnd** correspondentes.</span><span class="sxs-lookup"><span data-stu-id="04d27-132">The associated vertices and edge flags are interpreted exactly as they are in OpenGL between **glBegin**(GL\_TRIANGLE\_FAN), **glBegin**(GL\_TRIANGLE\_STRIP), or **glBegin**(GL\_TRIANGLES **)** and the matching **glEnd**.</span></span>

<span data-ttu-id="04d27-133">Como os sinalizadores de borda não fazem sentido em um ventilador de triângulo ou em uma faixa de triângulo, se houver uma função de retorno de chamada associada ao **\_ \_ sinalizador de borda Glu**, o retorno de chamada de **Glu \_ começar** será chamado apenas com **\_ triângulos GL**.</span><span class="sxs-lookup"><span data-stu-id="04d27-133">Because edge flags make no sense in a triangle fan or triangle strip, if there is a callback function associated with **GLU\_EDGE\_FLAG**, the **GLU\_BEGIN** callback is called only with **GL\_TRIANGLES**.</span></span> <span data-ttu-id="04d27-134">A função de retorno de chamada do **\_ \_ sinalizador de borda Glu** funciona de forma análoga com a função [glEdgeFlag](gledgeflag-functions.md) do OpenGL.</span><span class="sxs-lookup"><span data-stu-id="04d27-134">The **GLU\_EDGE\_FLAG** callback function works analogously to the OpenGL [glEdgeFlag](gledgeflag-functions.md) function.</span></span>

<span data-ttu-id="04d27-135">Se houver um erro durante o mosaico, a função de retorno de chamada de erro será invocada.</span><span class="sxs-lookup"><span data-stu-id="04d27-135">If there is an error during the tessellation, the error callback function is invoked.</span></span> <span data-ttu-id="04d27-136">A função de retorno de chamada de erro recebe um número de erro GLU.</span><span class="sxs-lookup"><span data-stu-id="04d27-136">The error callback function is passed a GLU error number.</span></span> <span data-ttu-id="04d27-137">Você pode obter uma cadeia de caracteres que descreve o erro com a função [**gluErrorString**](gluerrorstring.md) .</span><span class="sxs-lookup"><span data-stu-id="04d27-137">You can obtain a character string describing the error with the [**gluErrorString**](gluerrorstring.md) function.</span></span>

 

 




