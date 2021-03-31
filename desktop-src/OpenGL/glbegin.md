---
title: função glBegin (GL. h)
description: As funções glBegin e glend delimitam os vértices de um primitivo ou de um grupo de primitivas como primitivos. | função glBegin (GL. h)
ms.assetid: 8e8e98f8-89e8-40f5-89c1-492c9e3bbd74
keywords:
- função glBegin OpenGL
topic_type:
- apiref
api_name:
- glBegin
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8227d30adf97bf27fecc19603a5e5e32e4f44822
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930416"
---
# <a name="glbegin-function"></a><span data-ttu-id="7c65f-105">função glBegin</span><span class="sxs-lookup"><span data-stu-id="7c65f-105">glBegin function</span></span>

<span data-ttu-id="7c65f-106">As funções **glBegin** e [**glend**](glend.md) delimitam os vértices de um primitivo ou de um grupo de primitivas como primitivos.</span><span class="sxs-lookup"><span data-stu-id="7c65f-106">The **glBegin** and [**glend**](glend.md) functions delimit the vertices of a primitive or a group of like primitives.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c65f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7c65f-107">Syntax</span></span>


```C++
void WINAPI glBegin(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="7c65f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c65f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c65f-109">*mode*</span><span class="sxs-lookup"><span data-stu-id="7c65f-109">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="7c65f-110">Os primitivos ou primitivos que serão criados a partir de vértices apresentados entre **glBegin** e o [**glend**](glend.md)subsequente.</span><span class="sxs-lookup"><span data-stu-id="7c65f-110">The primitive or primitives that will be created from vertices presented between **glBegin** and the subsequent [**glend**](glend.md).</span></span> <span data-ttu-id="7c65f-111">As seguintes constantes simbólicas aceitas e seus significados:</span><span class="sxs-lookup"><span data-stu-id="7c65f-111">The following are accepted symbolic constants and their meanings:</span></span>



| <span data-ttu-id="7c65f-112">Valor</span><span class="sxs-lookup"><span data-stu-id="7c65f-112">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="7c65f-113">Significado</span><span class="sxs-lookup"><span data-stu-id="7c65f-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_POINTS"></span><span id="gl_points"></span><dl> <span data-ttu-id="7c65f-114"><dt>**\_pontos GL**</dt></span><span class="sxs-lookup"><span data-stu-id="7c65f-114"><dt>**GL\_POINTS**</dt></span></span> </dl>                          | <span data-ttu-id="7c65f-115">Trata cada vértice como um único ponto.</span><span class="sxs-lookup"><span data-stu-id="7c65f-115">Treats each vertex as a single point.</span></span> <span data-ttu-id="7c65f-116">O vértice *n* define o ponto *n*.</span><span class="sxs-lookup"><span data-stu-id="7c65f-116">Vertex *n* defines point *n*.</span></span> <span data-ttu-id="7c65f-117">*N* pontos são desenhados.</span><span class="sxs-lookup"><span data-stu-id="7c65f-117">*N* points are drawn.</span></span><br/>                                                                                                                                                                                                                                                                                                      |
| <span id="GL_LINES"></span><span id="gl_lines"></span><dl> <span data-ttu-id="7c65f-118"><dt>**\_linhas GL**</dt></span><span class="sxs-lookup"><span data-stu-id="7c65f-118"><dt>**GL\_LINES**</dt></span></span> </dl>                             | <span data-ttu-id="7c65f-119">Trata cada par de vértices como um segmento de linha independente.</span><span class="sxs-lookup"><span data-stu-id="7c65f-119">Treats each pair of vertices as an independent line segment.</span></span> <span data-ttu-id="7c65f-120">Os vértices *2n-1* e *2n* definem a linha *n*.</span><span class="sxs-lookup"><span data-stu-id="7c65f-120">Vertices *2n - 1* and *2n* define line *n*.</span></span> <span data-ttu-id="7c65f-121">As linhas *N/2* são desenhadas.</span><span class="sxs-lookup"><span data-stu-id="7c65f-121">*N/2* lines are drawn.</span></span><br/>                                                                                                                                                                                                                                                                |
| <span id="GL_LINE_STRIP"></span><span id="gl_line_strip"></span><dl> <span data-ttu-id="7c65f-122"><dt>**\_faixa de linha gl \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7c65f-122"><dt>**GL\_LINE\_STRIP**</dt></span></span> </dl>             | <span data-ttu-id="7c65f-123">Desenha um grupo conectado de segmentos de linha do primeiro vértice até o último.</span><span class="sxs-lookup"><span data-stu-id="7c65f-123">Draws a connected group of line segments from the first vertex to the last.</span></span> <span data-ttu-id="7c65f-124">Os vértices *n* e *n + 1* definem a linha *n*.</span><span class="sxs-lookup"><span data-stu-id="7c65f-124">Vertices *n* and *n+1* define line *n*.</span></span> <span data-ttu-id="7c65f-125">As linhas *N-1* são desenhadas.</span><span class="sxs-lookup"><span data-stu-id="7c65f-125">*N - 1* lines are drawn.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span id="GL_LINE_LOOP"></span><span id="gl_line_loop"></span><dl> <span data-ttu-id="7c65f-126"><dt>**\_loop de linha gl \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7c65f-126"><dt>**GL\_LINE\_LOOP**</dt></span></span> </dl>                | <span data-ttu-id="7c65f-127">Desenha um grupo conectado de segmentos de linha do primeiro vértice até o último e, em seguida, de volta para o primeiro.</span><span class="sxs-lookup"><span data-stu-id="7c65f-127">Draws a connected group of line segments from the first vertex to the last, then back to the first.</span></span> <span data-ttu-id="7c65f-128">Os vértices *n* e *n + 1* definem a linha *n*.</span><span class="sxs-lookup"><span data-stu-id="7c65f-128">Vertices *n* and *n + 1* define line *n*.</span></span> <span data-ttu-id="7c65f-129">A última linha, no entanto, é definida pelos vértices *N* e *1*.</span><span class="sxs-lookup"><span data-stu-id="7c65f-129">The last line, however, is defined by vertices *N* and *1*.</span></span> <span data-ttu-id="7c65f-130">*N* linhas são desenhadas.</span><span class="sxs-lookup"><span data-stu-id="7c65f-130">*N* lines are drawn.</span></span><br/>                                                                                                                                                                 |
| <span id="GL_TRIANGLES"></span><span id="gl_triangles"></span><dl> <span data-ttu-id="7c65f-131"><dt>**\_TRIângulos GL**</dt></span><span class="sxs-lookup"><span data-stu-id="7c65f-131"><dt>**GL\_TRIANGLES**</dt></span></span> </dl>                 | <span data-ttu-id="7c65f-132">Trata cada terceto de vértices como um triângulo independente.</span><span class="sxs-lookup"><span data-stu-id="7c65f-132">Treats each triplet of vertices as an independent triangle.</span></span> <span data-ttu-id="7c65f-133">Os vértices *3N-2*, *3n-1* e *3N* definem o triângulo *n*.</span><span class="sxs-lookup"><span data-stu-id="7c65f-133">Vertices *3n - 2*, *3n - 1*, and *3n* define triangle *n*.</span></span> <span data-ttu-id="7c65f-134">Os triângulos *N/3* são desenhados.</span><span class="sxs-lookup"><span data-stu-id="7c65f-134">*N/3* triangles are drawn.</span></span><br/>                                                                                                                                                                                                                                              |
| <span id="GL_TRIANGLE_STRIP"></span><span id="gl_triangle_strip"></span><dl> <span data-ttu-id="7c65f-135"><dt>**\_faixa de triângulo GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7c65f-135"><dt>**GL\_TRIANGLE\_STRIP**</dt></span></span> </dl> | <span data-ttu-id="7c65f-136">Desenha um grupo conectado de triângulos.</span><span class="sxs-lookup"><span data-stu-id="7c65f-136">Draws a connected group of triangles.</span></span> <span data-ttu-id="7c65f-137">Um triângulo é definido para cada vértice apresentado após os dois primeiros vértices.</span><span class="sxs-lookup"><span data-stu-id="7c65f-137">One triangle is defined for each vertex presented after the first two vertices.</span></span> <span data-ttu-id="7c65f-138">Para os *n* ímpares, os vértices *n*, *n + 1* e *n + 2* definem o triângulo *n*.</span><span class="sxs-lookup"><span data-stu-id="7c65f-138">For odd *n*, vertices *n*, *n + 1*, and *n + 2* define triangle *n*.</span></span> <span data-ttu-id="7c65f-139">Para até *n*, os vértices *n + 1*, *n* e *n + 2* definem o triângulo *n*.</span><span class="sxs-lookup"><span data-stu-id="7c65f-139">For even *n*, vertices *n + 1*, *n*, and *n + 2* define triangle *n*.</span></span> <span data-ttu-id="7c65f-140">Os triângulos *N-2* são desenhados.</span><span class="sxs-lookup"><span data-stu-id="7c65f-140">*N - 2* triangles are drawn.</span></span><br/>                                                                                                  |
| <span id="GL_TRIANGLE_FAN"></span><span id="gl_triangle_fan"></span><dl> <span data-ttu-id="7c65f-141"><dt>**\_ \_ ventilador do triângulo GL**</dt></span><span class="sxs-lookup"><span data-stu-id="7c65f-141"><dt>**GL\_TRIANGLE\_FAN**</dt></span></span> </dl>       | <span data-ttu-id="7c65f-142">Desenha um grupo conectado de triângulos.</span><span class="sxs-lookup"><span data-stu-id="7c65f-142">Draws a connected group of triangles.</span></span> <span data-ttu-id="7c65f-143">um triângulo é definido para cada vértice apresentado após os dois primeiros vértices.</span><span class="sxs-lookup"><span data-stu-id="7c65f-143">one triangle is defined for each vertex presented after the first two vertices.</span></span> <span data-ttu-id="7c65f-144">Os vértices *1*, *n + 1*, *n + 2* definem o triângulo *n*.</span><span class="sxs-lookup"><span data-stu-id="7c65f-144">Vertices *1*, *n + 1*, *n + 2* define triangle *n*.</span></span> <span data-ttu-id="7c65f-145">Os triângulos *N-2* são desenhados.</span><span class="sxs-lookup"><span data-stu-id="7c65f-145">*N - 2* triangles are drawn.</span></span><br/>                                                                                                                                                                                         |
| <span id="GL_QUADS"></span><span id="gl_quads"></span><dl> <span data-ttu-id="7c65f-146"><dt>**GL \_ quádruplos**</dt></span><span class="sxs-lookup"><span data-stu-id="7c65f-146"><dt>**GL\_QUADS**</dt></span></span> </dl>                             | <span data-ttu-id="7c65f-147">Trata cada grupo de quatro vértices como um diamante independente.</span><span class="sxs-lookup"><span data-stu-id="7c65f-147">Treats each group of four vertices as an independent quadrilateral.</span></span> <span data-ttu-id="7c65f-148">Vértices *4n-3*, *4n-2*, *4n-1* e *4n* definem diamante *n*.</span><span class="sxs-lookup"><span data-stu-id="7c65f-148">Vertices *4n - 3*, *4n - 2*, *4n - 1*, and *4n* define quadrilateral *n*.</span></span> <span data-ttu-id="7c65f-149">*N/4* quadrilaterals são desenhados.</span><span class="sxs-lookup"><span data-stu-id="7c65f-149">*N/4* quadrilaterals are drawn.</span></span><br/>                                                                                                                                                                                                                  |
| <span id="GL_QUAD_STRIP"></span><span id="gl_quad_strip"></span><dl> <span data-ttu-id="7c65f-150"><dt>**extensão do GL \_ Quad \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7c65f-150"><dt>**GL\_QUAD\_STRIP**</dt></span></span> </dl>             | <span data-ttu-id="7c65f-151">Desenha um grupo conectado de quadrilaterals.</span><span class="sxs-lookup"><span data-stu-id="7c65f-151">Draws a connected group of quadrilaterals.</span></span> <span data-ttu-id="7c65f-152">Um diamante é definido para cada par de vértices apresentados após o primeiro par.</span><span class="sxs-lookup"><span data-stu-id="7c65f-152">One quadrilateral is defined for each pair of vertices presented after the first pair.</span></span> <span data-ttu-id="7c65f-153">Os vértices *2n-1*, *2n*, *2n + 2* e *2n + 1* definem diamante *n*.</span><span class="sxs-lookup"><span data-stu-id="7c65f-153">Vertices *2n - 1*, *2n*, *2n + 2*, and *2n + 1* define quadrilateral *n*.</span></span> <span data-ttu-id="7c65f-154">*N/2-1* quadrilaterals são desenhados.</span><span class="sxs-lookup"><span data-stu-id="7c65f-154">*N/2 - 1* quadrilaterals are drawn.</span></span> <span data-ttu-id="7c65f-155">Observe que a ordem na qual os vértices são usados para construir um diamante de dados de strip é diferente da usada com dados independentes.</span><span class="sxs-lookup"><span data-stu-id="7c65f-155">Note that the order in which vertices are used to construct a quadrilateral from strip data is different from that used with independent data.</span></span><br/> |
| <span id="GL_POLYGON"></span><span id="gl_polygon"></span><dl> <span data-ttu-id="7c65f-156"><dt>**polígono do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7c65f-156"><dt>**GL\_POLYGON**</dt></span></span> </dl>                       | <span data-ttu-id="7c65f-157">Desenha um polígono único e convexa.</span><span class="sxs-lookup"><span data-stu-id="7c65f-157">Draws a single, convex polygon.</span></span> <span data-ttu-id="7c65f-158">Os vértices de *1* a *N* definem este polígono.</span><span class="sxs-lookup"><span data-stu-id="7c65f-158">Vertices *1* through *N* define this polygon.</span></span><br/>                                                                                                                                                                                                                                                                                                                  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c65f-159">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7c65f-159">Return value</span></span>

<span data-ttu-id="7c65f-160">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7c65f-160">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7c65f-161">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="7c65f-161">Error codes</span></span>

<span data-ttu-id="7c65f-162">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="7c65f-162">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="7c65f-163">Name</span><span class="sxs-lookup"><span data-stu-id="7c65f-163">Name</span></span>                                                                                                  | <span data-ttu-id="7c65f-164">Significado</span><span class="sxs-lookup"><span data-stu-id="7c65f-164">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7c65f-165"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="7c65f-165"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="7c65f-166">o *modo* foi definido como um valor não aceito.</span><span class="sxs-lookup"><span data-stu-id="7c65f-166">*mode* was set to an unaccepted value.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="7c65f-167"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7c65f-167"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="7c65f-168">Uma função diferente de [glVertex](glvertex-functions.md), [glColor](glcolor-functions.md), [glIndex](glindex-functions.md), [glNormal](glnormal-functions.md), [glTexCoord](gltexcoord-functions.md), [glEvalCoord](glevalcoord-functions.md), [glEvalPoint](glevalpoint.md), [glMaterial](glmaterial-functions.md), [glEdgeFlag](gledgeflag-functions.md), [**glCallList**](glcalllist.md)ou [**glCallLists**](glcalllists.md) foi chamada entre **glBegin** e o [**glend**](glend.md)correspondente.</span><span class="sxs-lookup"><span data-stu-id="7c65f-168">A function other than [glVertex](glvertex-functions.md), [glColor](glcolor-functions.md), [glIndex](glindex-functions.md), [glNormal](glnormal-functions.md), [glTexCoord](gltexcoord-functions.md), [glEvalCoord](glevalcoord-functions.md), [glEvalPoint](glevalpoint.md), [glMaterial](glmaterial-functions.md), [glEdgeFlag](gledgeflag-functions.md), [**glCallList**](glcalllist.md), or [**glCallLists**](glcalllists.md) was called between **glBegin** and the corresponding [**glend**](glend.md).</span></span> <span data-ttu-id="7c65f-169">A função **glend** foi chamada antes que o **glBegin** correspondente fosse chamado ou **glBegin** foi chamado dentro de uma / sequência **glend** glBegin.</span><span class="sxs-lookup"><span data-stu-id="7c65f-169">The function **glend** was called before the corresponding **glBegin** was called, or **glBegin** was called within a **glBegin**/**glend** sequence.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="7c65f-170">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c65f-170">Remarks</span></span>

<span data-ttu-id="7c65f-171">As funções **glBegin** e [**glend**](glend.md) delimitam os vértices que definem um primitivo ou um grupo de primitivas como primitivos.</span><span class="sxs-lookup"><span data-stu-id="7c65f-171">The **glBegin** and [**glend**](glend.md) functions delimit the vertices that define a primitive or a group of like primitives.</span></span> <span data-ttu-id="7c65f-172">A função **glBegin** aceita um único argumento que especifica qual dos dez primitivos os vértices compõem.</span><span class="sxs-lookup"><span data-stu-id="7c65f-172">The **glBegin** function accepts a single argument that specifies which of ten primitives the vertices compose.</span></span> <span data-ttu-id="7c65f-173">Colocando *n* como uma contagem de inteiros começando em um, e *n* como o número total de vértices especificado, as interpretações são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="7c65f-173">Taking *n* as an integer count starting at one, and *N* as the total number of vertices specified, the interpretations are as follows:</span></span>

-   <span data-ttu-id="7c65f-174">Você pode usar apenas um subconjunto de funções OpenGL entre **glBegin** e [**glend**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="7c65f-174">You can use only a subset of OpenGL functions between **glBegin** and [**glend**](glend.md).</span></span> <span data-ttu-id="7c65f-175">As funções que você pode usar são:</span><span class="sxs-lookup"><span data-stu-id="7c65f-175">The functions you can use are:</span></span>

    [<span data-ttu-id="7c65f-176">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="7c65f-176">**glVertex**</span></span>](glvertex-functions.md)

     

    [<span data-ttu-id="7c65f-177">**glColor**</span><span class="sxs-lookup"><span data-stu-id="7c65f-177">**glColor**</span></span>](glcolor-functions.md)

     

    [<span data-ttu-id="7c65f-178">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="7c65f-178">**glIndex**</span></span>](glindex-functions.md)

     

    [<span data-ttu-id="7c65f-179">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="7c65f-179">**glNormal**</span></span>](glnormal-functions.md)

     

    [<span data-ttu-id="7c65f-180">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="7c65f-180">**glTexCoord**</span></span>](gltexcoord-functions.md)

     

    [<span data-ttu-id="7c65f-181">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="7c65f-181">**glEvalCoord**</span></span>](glevalcoord-functions.md)

     

    [<span data-ttu-id="7c65f-182">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="7c65f-182">**glEvalPoint**</span></span>](glevalpoint.md)

     

    [<span data-ttu-id="7c65f-183">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="7c65f-183">**glMaterial**</span></span>](glmaterial-functions.md)

     

    [<span data-ttu-id="7c65f-184">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="7c65f-184">**glEdgeFlag**</span></span>](gledgeflag-functions.md)

    <span data-ttu-id="7c65f-185">Você também pode usar [**glCallList**](glcalllist.md) ou [**glCallLists**](glcalllists.md) para executar listas de exibição que incluem apenas as funções anteriores.</span><span class="sxs-lookup"><span data-stu-id="7c65f-185">You can also use [**glCallList**](glcalllist.md) or [**glCallLists**](glcalllists.md) to execute display lists that include only the preceding functions.</span></span> <span data-ttu-id="7c65f-186">Se qualquer outra função OpenGL for chamada entre **glBegin** e [**glend**](glend.md), o sinalizador de erro será definido e a função será ignorada.</span><span class="sxs-lookup"><span data-stu-id="7c65f-186">If any other OpenGL function is called between **glBegin** and [**glend**](glend.md), the error flag is set and the function is ignored.</span></span>

-   <span data-ttu-id="7c65f-187">Independentemente do valor escolhido para o *modo* em **glBegin**, não há nenhum limite para o número de vértices que você pode definir entre **glBegin** e [**glend**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="7c65f-187">Regardless of the value chosen for *mode* in **glBegin**, there is no limit to the number of vertices you can define between **glBegin** and [**glend**](glend.md).</span></span> <span data-ttu-id="7c65f-188">Linhas, triângulos, quadrilaterals e polígonos especificados incompletamente não são desenhadas.</span><span class="sxs-lookup"><span data-stu-id="7c65f-188">Lines, triangles, quadrilaterals, and polygons that are incompletely specified are not drawn.</span></span> <span data-ttu-id="7c65f-189">Resultados incompletos de especificação quando um número muito pequeno de vértices são fornecidos para especificar até mesmo um único primitivo ou quando um múltiplo incorreto de vértices é especificado.</span><span class="sxs-lookup"><span data-stu-id="7c65f-189">Incomplete specification results when either too few vertices are provided to specify even a single primitive or when an incorrect multiple of vertices is specified.</span></span> <span data-ttu-id="7c65f-190">O primitivo incompleto é ignorado; os primitivos completos são desenhados.</span><span class="sxs-lookup"><span data-stu-id="7c65f-190">The incomplete primitive is ignored; the complete primitives are drawn.</span></span>
-   <span data-ttu-id="7c65f-191">A especificação mínima de vértices para cada primitivo é:</span><span class="sxs-lookup"><span data-stu-id="7c65f-191">The minimum specification of vertices for each primitive is:</span></span> 

    | <span data-ttu-id="7c65f-192">Número mínimo de vértices</span><span class="sxs-lookup"><span data-stu-id="7c65f-192">Minimum number of vertices</span></span> | <span data-ttu-id="7c65f-193">Tipo de primitiva</span><span class="sxs-lookup"><span data-stu-id="7c65f-193">Type of primitive</span></span> |
    |----------------------------|-------------------|
    | <span data-ttu-id="7c65f-194">1</span><span class="sxs-lookup"><span data-stu-id="7c65f-194">1</span></span>                          | <span data-ttu-id="7c65f-195">point</span><span class="sxs-lookup"><span data-stu-id="7c65f-195">point</span></span>             |
    | <span data-ttu-id="7c65f-196">2</span><span class="sxs-lookup"><span data-stu-id="7c65f-196">2</span></span>                          | <span data-ttu-id="7c65f-197">line</span><span class="sxs-lookup"><span data-stu-id="7c65f-197">line</span></span>              |
    | <span data-ttu-id="7c65f-198">3</span><span class="sxs-lookup"><span data-stu-id="7c65f-198">3</span></span>                          | <span data-ttu-id="7c65f-199">triangle</span><span class="sxs-lookup"><span data-stu-id="7c65f-199">triangle</span></span>          |
    | <span data-ttu-id="7c65f-200">4</span><span class="sxs-lookup"><span data-stu-id="7c65f-200">4</span></span>                          | <span data-ttu-id="7c65f-201">diamante</span><span class="sxs-lookup"><span data-stu-id="7c65f-201">quadrilateral</span></span>     |
    | <span data-ttu-id="7c65f-202">3</span><span class="sxs-lookup"><span data-stu-id="7c65f-202">3</span></span>                          | <span data-ttu-id="7c65f-203">polygon</span><span class="sxs-lookup"><span data-stu-id="7c65f-203">polygon</span></span>           |

    

     

-   <span data-ttu-id="7c65f-204">Os modos que exigem um determinado múltiplo de vértices são \_ linhas GL (2), \_ triângulos GL (3), GL \_ quádruplos (4) e GL \_ Quad \_ strip (2).</span><span class="sxs-lookup"><span data-stu-id="7c65f-204">Modes that require a certain multiple of vertices are GL\_LINES (2), GL\_TRIANGLES (3), GL\_QUADS (4), and GL\_QUAD\_STRIP (2).</span></span>

## <a name="requirements"></a><span data-ttu-id="7c65f-205">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c65f-205">Requirements</span></span>



| <span data-ttu-id="7c65f-206">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c65f-206">Requirement</span></span> | <span data-ttu-id="7c65f-207">Valor</span><span class="sxs-lookup"><span data-stu-id="7c65f-207">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c65f-208">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c65f-208">Minimum supported client</span></span><br/> | <span data-ttu-id="7c65f-209">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7c65f-209">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7c65f-210">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c65f-210">Minimum supported server</span></span><br/> | <span data-ttu-id="7c65f-211">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7c65f-211">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7c65f-212">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7c65f-212">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c65f-213"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c65f-213"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="7c65f-214">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7c65f-214">Library</span></span><br/>                  | <dl> <span data-ttu-id="7c65f-215"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c65f-215"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7c65f-216">DLL</span><span class="sxs-lookup"><span data-stu-id="7c65f-216">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c65f-217"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c65f-217"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c65f-218">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c65f-218">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c65f-219">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="7c65f-219">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="7c65f-220">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="7c65f-220">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="7c65f-221">**glColor**</span><span class="sxs-lookup"><span data-stu-id="7c65f-221">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="7c65f-222">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="7c65f-222">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="7c65f-223">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="7c65f-223">**glEnd**</span></span>](/windows/desktop/OpenGL/glend)
</dt> <dt>

[<span data-ttu-id="7c65f-224">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="7c65f-224">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="7c65f-225">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="7c65f-225">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="7c65f-226">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="7c65f-226">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="7c65f-227">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="7c65f-227">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="7c65f-228">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="7c65f-228">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="7c65f-229">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="7c65f-229">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="7c65f-230">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="7c65f-230">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

