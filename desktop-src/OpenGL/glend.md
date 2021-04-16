---
title: função glEnd (GL. h)
description: As funções glBegin e glend delimitam os vértices de um primitivo ou de um grupo de primitivas como primitivos. | função glEnd (GL. h)
ms.assetid: 040f8573-683c-4a8a-ae51-66abb0541ac4
keywords:
- função glEnd OpenGL
topic_type:
- apiref
api_name:
- glEnd
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9bb41395b3ed2e38a64094506e07e2a69ad1d52
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105750460"
---
# <a name="glend-function"></a><span data-ttu-id="2add9-105">função glEnd</span><span class="sxs-lookup"><span data-stu-id="2add9-105">glEnd function</span></span>

<span data-ttu-id="2add9-106">As funções [**glBegin**](glbegin.md) e **glend** delimitam os vértices de um primitivo ou de um grupo de primitivas como primitivos.</span><span class="sxs-lookup"><span data-stu-id="2add9-106">The [**glBegin**](glbegin.md) and **glend** functions delimit the vertices of a primitive or a group of like primitives.</span></span>

## <a name="syntax"></a><span data-ttu-id="2add9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2add9-107">Syntax</span></span>


```C++
void WINAPI glEnd(void);
```



## <a name="parameters"></a><span data-ttu-id="2add9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2add9-108">Parameters</span></span>

<span data-ttu-id="2add9-109">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="2add9-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2add9-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2add9-110">Return value</span></span>

<span data-ttu-id="2add9-111">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="2add9-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2add9-112">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="2add9-112">Error codes</span></span>

<span data-ttu-id="2add9-113">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="2add9-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="2add9-114">Nome</span><span class="sxs-lookup"><span data-stu-id="2add9-114">Name</span></span>                                                                                                  | <span data-ttu-id="2add9-115">Significado</span><span class="sxs-lookup"><span data-stu-id="2add9-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2add9-116"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2add9-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="2add9-117">Uma função diferente de **glVertex**, **glColor**, **glIndex**, **glNormal**, **glTexCoord**, **glEvalCoord**, **glEvalPoint**, **glMaterial**, **glEdgeFlag**, **glCallList** ou **glCallLists** foi chamada entre **glBegin** e o **glEnd** correspondente.</span><span class="sxs-lookup"><span data-stu-id="2add9-117">A function other than **glVertex**, **glColor**, **glIndex**, **glNormal**, **glTexCoord**, **glEvalCoord**, **glEvalPoint**, **glMaterial**, **glEdgeFlag**, **glCallList**, or **glCallLists** was called between **glBegin** and the corresponding **glEnd**.</span></span> <span data-ttu-id="2add9-118">A função **glEnd** foi chamada antes que o **glBegin** correspondente fosse chamado ou **glBegin** foi chamado dentro de uma / sequência **glEnd** glBegin.</span><span class="sxs-lookup"><span data-stu-id="2add9-118">The function **glEnd** was called before the corresponding **glBegin** was called, or **glBegin** was called within a **glBegin**/**glEnd** sequence.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="2add9-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="2add9-119">Remarks</span></span>

<span data-ttu-id="2add9-120">As funções [**glBegin**](glbegin.md) e **glend** delimitam os vértices que definem um primitivo ou um grupo de primitivas como primitivos.</span><span class="sxs-lookup"><span data-stu-id="2add9-120">The [**glBegin**](glbegin.md) and **glend** functions delimit the vertices that define a primitive or a group of like primitives.</span></span> <span data-ttu-id="2add9-121">A função **glBegin** aceita um único argumento que especifica qual dos dez primitivos os vértices compõem.</span><span class="sxs-lookup"><span data-stu-id="2add9-121">The **glBegin** function accepts a single argument that specifies which of ten primitives the vertices compose.</span></span> <span data-ttu-id="2add9-122">Colocando *n* como uma contagem de inteiros começando em um, e *n* como o número total de vértices especificado, as interpretações são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="2add9-122">Taking *n* as an integer count starting at one, and *N* as the total number of vertices specified, the interpretations are as follows:</span></span>

-   <span data-ttu-id="2add9-123">Você pode usar apenas um subconjunto de funções OpenGL entre **glBegin** e **glEnd**.</span><span class="sxs-lookup"><span data-stu-id="2add9-123">You can use only a subset of OpenGL functions between **glBegin** and **glEnd**.</span></span> <span data-ttu-id="2add9-124">As funções que você pode usar são:</span><span class="sxs-lookup"><span data-stu-id="2add9-124">The functions you can use are:</span></span>

    -   [<span data-ttu-id="2add9-125">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="2add9-125">**glVertex**</span></span>](glvertex-functions.md)
    -   [<span data-ttu-id="2add9-126">**glColor**</span><span class="sxs-lookup"><span data-stu-id="2add9-126">**glColor**</span></span>](glcolor-functions.md)
    -   [<span data-ttu-id="2add9-127">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="2add9-127">**glIndex**</span></span>](glindex-functions.md)
    -   [<span data-ttu-id="2add9-128">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="2add9-128">**glNormal**</span></span>](glnormal-functions.md)
    -   [<span data-ttu-id="2add9-129">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="2add9-129">**glTexCoord**</span></span>](gltexcoord-functions.md)
    -   [<span data-ttu-id="2add9-130">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="2add9-130">**glEvalCoord**</span></span>](glevalcoord-functions.md)
    -   [<span data-ttu-id="2add9-131">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="2add9-131">**glEvalPoint**</span></span>](glevalpoint.md)
    -   [<span data-ttu-id="2add9-132">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="2add9-132">**glMaterial**</span></span>](glmaterial-functions.md)
    -   [<span data-ttu-id="2add9-133">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="2add9-133">**glEdgeFlag**</span></span>](gledgeflag-functions.md)

    <span data-ttu-id="2add9-134">Você também pode usar [**glCallList**](glcalllist.md) ou [**glCallLists**](glcalllists.md) para executar listas de exibição que incluem apenas as funções anteriores.</span><span class="sxs-lookup"><span data-stu-id="2add9-134">You can also use [**glCallList**](glcalllist.md) or [**glCallLists**](glcalllists.md) to execute display lists that include only the preceding functions.</span></span> <span data-ttu-id="2add9-135">Se qualquer outra função OpenGL for chamada entre **glBegin** e **glEnd**, o sinalizador de erro será definido e a função será ignorada.</span><span class="sxs-lookup"><span data-stu-id="2add9-135">If any other OpenGL function is called between **glBegin** and **glEnd**, the error flag is set and the function is ignored.</span></span>

-   <span data-ttu-id="2add9-136">Independentemente do valor escolhido para o *modo* em **glBegin**, não há nenhum limite para o número de vértices que você pode definir entre **glBegin** e **glEnd**.</span><span class="sxs-lookup"><span data-stu-id="2add9-136">Regardless of the value chosen for *mode* in **glBegin**, there is no limit to the number of vertices you can define between **glBegin** and **glEnd**.</span></span> <span data-ttu-id="2add9-137">Linhas, triângulos, quadrilaterals e polígonos especificados incompletamente não são desenhadas.</span><span class="sxs-lookup"><span data-stu-id="2add9-137">Lines, triangles, quadrilaterals, and polygons that are incompletely specified are not drawn.</span></span> <span data-ttu-id="2add9-138">Resultados incompletos de especificação quando um número muito pequeno de vértices são fornecidos para especificar até mesmo um único primitivo ou quando um múltiplo incorreto de vértices é especificado.</span><span class="sxs-lookup"><span data-stu-id="2add9-138">Incomplete specification results when either too few vertices are provided to specify even a single primitive or when an incorrect multiple of vertices is specified.</span></span> <span data-ttu-id="2add9-139">O primitivo incompleto é ignorado; os primitivos completos são desenhados.</span><span class="sxs-lookup"><span data-stu-id="2add9-139">The incomplete primitive is ignored; the complete primitives are drawn.</span></span>
-   <span data-ttu-id="2add9-140">A especificação mínima de vértices para cada primitivo é:</span><span class="sxs-lookup"><span data-stu-id="2add9-140">The minimum specification of vertices for each primitive is:</span></span> 

    | <span data-ttu-id="2add9-141">Número mínimo de vértices</span><span class="sxs-lookup"><span data-stu-id="2add9-141">Minimum number of vertices</span></span> | <span data-ttu-id="2add9-142">Tipo de primitiva</span><span class="sxs-lookup"><span data-stu-id="2add9-142">Type of primitive</span></span> |
    |----------------------------|-------------------|
    | <span data-ttu-id="2add9-143">1</span><span class="sxs-lookup"><span data-stu-id="2add9-143">1</span></span>                          | <span data-ttu-id="2add9-144">point</span><span class="sxs-lookup"><span data-stu-id="2add9-144">point</span></span>             |
    | <span data-ttu-id="2add9-145">2</span><span class="sxs-lookup"><span data-stu-id="2add9-145">2</span></span>                          | <span data-ttu-id="2add9-146">line</span><span class="sxs-lookup"><span data-stu-id="2add9-146">line</span></span>              |
    | <span data-ttu-id="2add9-147">3</span><span class="sxs-lookup"><span data-stu-id="2add9-147">3</span></span>                          | <span data-ttu-id="2add9-148">triangle</span><span class="sxs-lookup"><span data-stu-id="2add9-148">triangle</span></span>          |
    | <span data-ttu-id="2add9-149">4</span><span class="sxs-lookup"><span data-stu-id="2add9-149">4</span></span>                          | <span data-ttu-id="2add9-150">diamante</span><span class="sxs-lookup"><span data-stu-id="2add9-150">quadrilateral</span></span>     |
    | <span data-ttu-id="2add9-151">3</span><span class="sxs-lookup"><span data-stu-id="2add9-151">3</span></span>                          | <span data-ttu-id="2add9-152">polygon</span><span class="sxs-lookup"><span data-stu-id="2add9-152">polygon</span></span>           |

    

     

-   <span data-ttu-id="2add9-153">Os modos que exigem um determinado múltiplo de vértices são \_ linhas GL (2), \_ triângulos GL (3), GL \_ quádruplos (4) e GL \_ Quad \_ strip (2).</span><span class="sxs-lookup"><span data-stu-id="2add9-153">Modes that require a certain multiple of vertices are GL\_LINES (2), GL\_TRIANGLES (3), GL\_QUADS (4), and GL\_QUAD\_STRIP (2).</span></span>

## <a name="requirements"></a><span data-ttu-id="2add9-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2add9-154">Requirements</span></span>



| <span data-ttu-id="2add9-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="2add9-155">Requirement</span></span> | <span data-ttu-id="2add9-156">Valor</span><span class="sxs-lookup"><span data-stu-id="2add9-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2add9-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2add9-157">Minimum supported client</span></span><br/> | <span data-ttu-id="2add9-158">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2add9-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2add9-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2add9-159">Minimum supported server</span></span><br/> | <span data-ttu-id="2add9-160">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2add9-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2add9-161">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2add9-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="2add9-162"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="2add9-162"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="2add9-163">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2add9-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="2add9-164"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2add9-164"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2add9-165">DLL</span><span class="sxs-lookup"><span data-stu-id="2add9-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2add9-166"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2add9-166"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2add9-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="2add9-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2add9-168">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="2add9-168">**glBegin**</span></span>](/windows/desktop/OpenGL/glbegin)
</dt> <dt>

[<span data-ttu-id="2add9-169">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="2add9-169">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="2add9-170">**glColor**</span><span class="sxs-lookup"><span data-stu-id="2add9-170">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="2add9-171">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="2add9-171">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="2add9-172">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="2add9-172">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="2add9-173">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="2add9-173">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="2add9-174">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="2add9-174">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="2add9-175">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="2add9-175">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="2add9-176">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="2add9-176">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="2add9-177">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="2add9-177">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="2add9-178">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="2add9-178">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

