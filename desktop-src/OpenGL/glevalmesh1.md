---
title: função glEvalMesh1 (GL. h)
description: Computa uma grade unidimensional de pontos ou linhas.
ms.assetid: 176a4b81-f1a7-42fc-8ecd-bba77a0ec5b3
keywords:
- função glEvalMesh1 OpenGL
topic_type:
- apiref
api_name:
- glEvalMesh1
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8950dcf397816fca8eb5a6add45c45512c48866
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499480"
---
# <a name="glevalmesh1-function"></a><span data-ttu-id="87191-104">função glEvalMesh1</span><span class="sxs-lookup"><span data-stu-id="87191-104">glEvalMesh1 function</span></span>

<span data-ttu-id="87191-105">Computa uma grade unidimensional de pontos ou linhas.</span><span class="sxs-lookup"><span data-stu-id="87191-105">Computes a one-dimensional grid of points or lines.</span></span>

## <a name="syntax"></a><span data-ttu-id="87191-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87191-106">Syntax</span></span>


```C++
void WINAPI glEvalMesh1(
   GLenum mode,
   GLint  i1,
   GLint  i2
);
```



## <a name="parameters"></a><span data-ttu-id="87191-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87191-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87191-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="87191-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="87191-109">Um valor que especifica se uma malha unidimensional de pontos ou linhas deve ser computada.</span><span class="sxs-lookup"><span data-stu-id="87191-109">A value that specifies whether to compute a one-dimensional mesh of points or lines.</span></span> <span data-ttu-id="87191-110">As seguintes constantes simbólicas são aceitas: ingl \_ Point e GL \_ line.</span><span class="sxs-lookup"><span data-stu-id="87191-110">The following symbolic constants are accepted: GL\_POINT and GL\_LINE.</span></span>

</dd> <dt>

<span data-ttu-id="87191-111">*I1*</span><span class="sxs-lookup"><span data-stu-id="87191-111">*i1*</span></span> 
</dt> <dd>

<span data-ttu-id="87191-112">O primeiro valor inteiro para a variável de domínio de grade i.</span><span class="sxs-lookup"><span data-stu-id="87191-112">The first integer value for grid domain variable i.</span></span>

</dd> <dt>

<span data-ttu-id="87191-113">*i2*</span><span class="sxs-lookup"><span data-stu-id="87191-113">*i2*</span></span> 
</dt> <dd>

<span data-ttu-id="87191-114">O último valor inteiro para a variável de domínio de grade i.</span><span class="sxs-lookup"><span data-stu-id="87191-114">The last integer value for grid domain variable i.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87191-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="87191-115">Return value</span></span>

<span data-ttu-id="87191-116">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="87191-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="87191-117">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="87191-117">Error codes</span></span>

<span data-ttu-id="87191-118">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="87191-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="87191-119">Nome</span><span class="sxs-lookup"><span data-stu-id="87191-119">Name</span></span>                                                                                                  | <span data-ttu-id="87191-120">Significado</span><span class="sxs-lookup"><span data-stu-id="87191-120">Meaning</span></span>                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="87191-121"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="87191-121"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="87191-122">Indica que o *modo* não é um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="87191-122">Indicates that *mode* is not an accepted value.</span></span> <br/>                                                                            |
| <dl> <span data-ttu-id="87191-123"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="87191-123"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="87191-124">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="87191-124">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="87191-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="87191-125">Remarks</span></span>

<span data-ttu-id="87191-126">Use [**glMapGrid**](glmapgrid-functions.md) e [**glEvalMesh**](glevalmesh-functions.md) juntos para gerar e avaliar com eficiência uma série de valores de domínio de mapa com espaçamento uniforme.</span><span class="sxs-lookup"><span data-stu-id="87191-126">Use [**glMapGrid**](glmapgrid-functions.md) and [**glEvalMesh**](glevalmesh-functions.md) together to efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="87191-127">A função **glEvalMesh** percorre o domínio inteiro de uma grade de uma ou duas dimensões, cujo intervalo é o domínio dos mapas de avaliação especificados por [**glMap1**](glmap1.md) e [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="87191-127">The **glEvalMesh** function steps through the integer domain of a one- or two-dimensional grid, whose range is the domain of the evaluation maps specified by [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span> <span data-ttu-id="87191-128">O parâmetro mode determina se os vértices resultantes são conectados como pontos, linhas ou polígonos preenchidos.</span><span class="sxs-lookup"><span data-stu-id="87191-128">The mode parameter determines whether the resulting vertices are connected as points, lines, or filled polygons.</span></span>

<span data-ttu-id="87191-129">No caso unidimensional, **glEvalMesh1**, a malha é gerada como se o fragmento de código a seguir fosse executado:</span><span class="sxs-lookup"><span data-stu-id="87191-129">In the one-dimensional case, **glEvalMesh1**, the mesh is generated as if the following code fragment were executed:</span></span>

<span data-ttu-id="87191-130">[**glBegin**](glbegin.md)(*tipo*);</span><span class="sxs-lookup"><span data-stu-id="87191-130">[**glBegin**](glbegin.md)(*type*);</span></span>

<span data-ttu-id="87191-131">for (i = i1; i <= i2; i + = 1)</span><span class="sxs-lookup"><span data-stu-id="87191-131">for (i = i1; i <= i2; i += 1)</span></span>

<span data-ttu-id="87191-132">{</span><span class="sxs-lookup"><span data-stu-id="87191-132">{</span></span>

<span data-ttu-id="87191-133">[**glEvalCoord1**](glevalcoord1d.md)(i? u + U1)</span><span class="sxs-lookup"><span data-stu-id="87191-133">[**glEvalCoord1**](glevalcoord1d.md)(i?u + u1)</span></span>

<span data-ttu-id="87191-134">}</span><span class="sxs-lookup"><span data-stu-id="87191-134">}</span></span>

<span data-ttu-id="87191-135">[**glEnd**](glend.md)();</span><span class="sxs-lookup"><span data-stu-id="87191-135">[**glEnd**](glend.md)( );</span></span>

<span data-ttu-id="87191-136">onde</span><span class="sxs-lookup"><span data-stu-id="87191-136">where</span></span>

<span data-ttu-id="87191-137">? u = (U2 U1)/n</span><span class="sxs-lookup"><span data-stu-id="87191-137">?u = (u2 u1) / n</span></span>

<span data-ttu-id="87191-138">e n, U1 e U2 são os argumentos para a função [**glMapGrid1**](glmapgrid1d.md) mais recente.</span><span class="sxs-lookup"><span data-stu-id="87191-138">and n, u1, and u2 are the arguments to the most recent [**glMapGrid1**](glmapgrid1d.md) function.</span></span> <span data-ttu-id="87191-139">O parâmetro de *tipo* será o GL \_ Points se Mode for GL \_ Point ou GL \_ linhas se Mode for GL \_ line.</span><span class="sxs-lookup"><span data-stu-id="87191-139">The *type* parameter is GL\_POINTS if mode is GL\_POINT, or GL\_LINES if mode is GL\_LINE.</span></span> <span data-ttu-id="87191-140">O requisito numérico absoluto é que, se eu = n, o valor calculado de i? u + U1 é exatamente U2.</span><span class="sxs-lookup"><span data-stu-id="87191-140">The one absolute numeric requirement is that if i = n, then the value computed from i?u + u1 is exactly u2.</span></span>

## <a name="requirements"></a><span data-ttu-id="87191-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87191-141">Requirements</span></span>



| <span data-ttu-id="87191-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="87191-142">Requirement</span></span> | <span data-ttu-id="87191-143">Valor</span><span class="sxs-lookup"><span data-stu-id="87191-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87191-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87191-144">Minimum supported client</span></span><br/> | <span data-ttu-id="87191-145">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="87191-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="87191-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87191-146">Minimum supported server</span></span><br/> | <span data-ttu-id="87191-147">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="87191-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="87191-148">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="87191-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="87191-149"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="87191-149"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="87191-150">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="87191-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="87191-151"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="87191-151"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="87191-152">DLL</span><span class="sxs-lookup"><span data-stu-id="87191-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87191-153"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87191-153"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87191-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="87191-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87191-155">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="87191-155">**glBegin**</span></span>](glbegin.md)
</dt> </dl>

 

 





