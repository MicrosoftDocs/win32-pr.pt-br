---
title: função glMapGrid1d (GL. h)
description: Define uma malha unidimensional. | função glMapGrid1d (GL. h)
ms.assetid: a0bc822e-dd98-4586-a322-2779e11f38ca
keywords:
- função glMapGrid1d OpenGL
topic_type:
- apiref
api_name:
- glMapGrid1d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30b1900f5597e8c516100504ca7288137ed99ded
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103837736"
---
# <a name="glmapgrid1d-function"></a><span data-ttu-id="b3a1f-105">função glMapGrid1d</span><span class="sxs-lookup"><span data-stu-id="b3a1f-105">glMapGrid1d function</span></span>

<span data-ttu-id="b3a1f-106">Define uma malha unidimensional.</span><span class="sxs-lookup"><span data-stu-id="b3a1f-106">Defines a one-dimensional mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3a1f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b3a1f-107">Syntax</span></span>


```C++
void WINAPI glMapGrid1d(
   GLint    un,
   GLdouble u1,
   GLdouble u2
);
```



## <a name="parameters"></a><span data-ttu-id="b3a1f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3a1f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3a1f-109">*anula*</span><span class="sxs-lookup"><span data-stu-id="b3a1f-109">*un*</span></span> 
</dt> <dd>

<span data-ttu-id="b3a1f-110">O número de partições no intervalo de intervalo de grade \[ U1, U2 \] .</span><span class="sxs-lookup"><span data-stu-id="b3a1f-110">The number of partitions in the grid range interval \[u1, u2\].</span></span> <span data-ttu-id="b3a1f-111">Esse valor deve ser positivo.</span><span class="sxs-lookup"><span data-stu-id="b3a1f-111">This value must be positive.</span></span>

</dd> <dt>

<span data-ttu-id="b3a1f-112">*U1*</span><span class="sxs-lookup"><span data-stu-id="b3a1f-112">*u1*</span></span> 
</dt> <dd>

<span data-ttu-id="b3a1f-113">Um valor usado como o mapeamento para o valor de domínio da grade de inteiros i = 0.</span><span class="sxs-lookup"><span data-stu-id="b3a1f-113">A value used as the mapping for integer grid domain value i = 0.</span></span>

</dd> <dt>

<span data-ttu-id="b3a1f-114">*U2*</span><span class="sxs-lookup"><span data-stu-id="b3a1f-114">*u2*</span></span> 
</dt> <dd>

<span data-ttu-id="b3a1f-115">Um valor usado como o mapeamento para o valor de domínio da grade de inteiros i = un.</span><span class="sxs-lookup"><span data-stu-id="b3a1f-115">A value used as the mapping for integer grid domain value i = un.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3a1f-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b3a1f-116">Return value</span></span>

<span data-ttu-id="b3a1f-117">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b3a1f-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b3a1f-118">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="b3a1f-118">Error codes</span></span>

<span data-ttu-id="b3a1f-119">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="b3a1f-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b3a1f-120">Nome</span><span class="sxs-lookup"><span data-stu-id="b3a1f-120">Name</span></span>                                                                                                  | <span data-ttu-id="b3a1f-121">Significado</span><span class="sxs-lookup"><span data-stu-id="b3a1f-121">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b3a1f-122"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b3a1f-122"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="b3a1f-123">O  *vn* não era positivo.</span><span class="sxs-lookup"><span data-stu-id="b3a1f-123">Either *un* or *vn* was not positive.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="b3a1f-124"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b3a1f-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b3a1f-125">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="b3a1f-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b3a1f-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3a1f-126">Remarks</span></span>

<span data-ttu-id="b3a1f-127">Use as funções **glMapGrid** e [glEvalMesh](glevalmesh-functions.md) juntas para gerar e avaliar com eficiência uma série de valores de domínio de mapa com espaçamento uniforme.</span><span class="sxs-lookup"><span data-stu-id="b3a1f-127">Use the **glMapGrid** and [glEvalMesh](glevalmesh-functions.md) functions togetherto efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="b3a1f-128">A função glEvalMesh percorre o domínio inteiro de uma grade de uma ou duas dimensões, cujo intervalo é o domínio dos mapas de avaliação especificados por [**glMap1**](glmap1.md) e [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="b3a1f-128">The glEvalMesh function steps through the integer domain of a one- or two-dimensional grid, whose range is the domain of the evaluation maps specified by [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span>

<span data-ttu-id="b3a1f-129">As funções **glMapGrid1** e [**glMapGrid2**](glmapgrid2d.md) especificam os mapeamentos de grade linear entre as coordenadas de grade de inteiros i (ou i e j) para as coordenadas de mapa de avaliação de ponto flutuante u (ou você e v).</span><span class="sxs-lookup"><span data-stu-id="b3a1f-129">The **glMapGrid1** and [**glMapGrid2**](glmapgrid2d.md) functions specify the linear grid mappings between the i (or i and j) integer grid coordinates, to the u (or u and v) floating-point evaluation map coordinates.</span></span> <span data-ttu-id="b3a1f-130">Consulte [**glMap1**](glmap1.md) e [**glMap2**](glmap2.md) para obter detalhes de como você e as coordenadas v são avaliados.</span><span class="sxs-lookup"><span data-stu-id="b3a1f-130">See [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md) for details of how u and v coordinates are evaluated.</span></span>

<span data-ttu-id="b3a1f-131">A função **glMapGrid1** especifica um mapeamento linear único, de modo que *a coordenada* de grade de inteiros 0 é mapeada exatamente para U1, e a coordenada de grade de inteiros remapeia exatamente para *U2*.</span><span class="sxs-lookup"><span data-stu-id="b3a1f-131">The **glMapGrid1** function specifies a single linear mapping such that integer grid coordinate 0 maps exactly to u1, and integer grid coordinate *un* maps exactly to *u2*.</span></span> <span data-ttu-id="b3a1f-132">Todas as outras coordenadas de grade de *inteiros que são* mapeadas de modo que:</span><span class="sxs-lookup"><span data-stu-id="b3a1f-132">All other integer grid coordinates *i* are mapped such that:</span></span>

<span data-ttu-id="b3a1f-133">*u = i (U2 U1)/un + U1*</span><span class="sxs-lookup"><span data-stu-id="b3a1f-133">*u = i(u2 u1)/un + u1*</span></span>

<span data-ttu-id="b3a1f-134">A função [**glMapGrid2**](glmapgrid2d.md) especifica dois mapeamentos lineares.</span><span class="sxs-lookup"><span data-stu-id="b3a1f-134">The [**glMapGrid2**](glmapgrid2d.md) function specifies two such linear mappings.</span></span> <span data-ttu-id="b3a1f-135">Um mapeia a coordenada de grade de inteiros *i = 0* exatamente para *U1* e a coordenada de grade de inteiros *i =* não exatamente como *U2*.</span><span class="sxs-lookup"><span data-stu-id="b3a1f-135">One maps integer grid coordinate *i = 0* exactly to *u1*, and integer grid coordinate *i = un* exactly to *u2*.</span></span> <span data-ttu-id="b3a1f-136">A outra coordenada de grade de inteiros de mapas *j = 0* exatamente para *v1* e a coordenada de grade de inteiros *j = vn* exatamente para *v2*.</span><span class="sxs-lookup"><span data-stu-id="b3a1f-136">The other maps integer grid coordinate *j = 0* exactly to *v1*, and integer grid coordinate *j = vn* exactly to *v2*.</span></span> <span data-ttu-id="b3a1f-137">Outras coordenadas de grade de inteiros i e j são mapeadas de modo que</span><span class="sxs-lookup"><span data-stu-id="b3a1f-137">Other integer grid coordinates i and j are mapped such that</span></span>

<span data-ttu-id="b3a1f-138">*u = i (U2 U1)/un + U1*</span><span class="sxs-lookup"><span data-stu-id="b3a1f-138">*u = i(u2 u1)/un + u1*</span></span>

<span data-ttu-id="b3a1f-139">*v = j (v2 v1)/VN + v1*</span><span class="sxs-lookup"><span data-stu-id="b3a1f-139">*v = j (v2 v1)/vn + v1*</span></span>

<span data-ttu-id="b3a1f-140">Os mapeamentos especificados por **glMapGrid** são usados de forma idêntica por [glEvalMesh](glevalmesh-functions.md) e [**glEvalPoint**](glevalpoint.md).</span><span class="sxs-lookup"><span data-stu-id="b3a1f-140">The mappings specified by **glMapGrid** are used identically by [glEvalMesh](glevalmesh-functions.md) and [**glEvalPoint**](glevalpoint.md).</span></span>

<span data-ttu-id="b3a1f-141">As funções a seguir recuperam informações relacionadas ao **glMapGrid**:</span><span class="sxs-lookup"><span data-stu-id="b3a1f-141">The following functions retrieve information related to **glMapGrid**:</span></span>

<dl>

<span data-ttu-id="b3a1f-142">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ MAP1 \_ grade \_ Domain</span><span class="sxs-lookup"><span data-stu-id="b3a1f-142">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_DOMAIN</span></span>  
<span data-ttu-id="b3a1f-143">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ map2 \_ grade \_ Domain</span><span class="sxs-lookup"><span data-stu-id="b3a1f-143">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_DOMAIN</span></span>  
<span data-ttu-id="b3a1f-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com os segmentos de grade Argument GL \_ MAP1 \_ \_</span><span class="sxs-lookup"><span data-stu-id="b3a1f-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_SEGMENTS</span></span>  
<span data-ttu-id="b3a1f-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com os segmentos de grade Argument GL \_ map2 \_ \_</span><span class="sxs-lookup"><span data-stu-id="b3a1f-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_SEGMENTS</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="b3a1f-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3a1f-146">Requirements</span></span>



| <span data-ttu-id="b3a1f-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3a1f-147">Requirement</span></span> | <span data-ttu-id="b3a1f-148">Valor</span><span class="sxs-lookup"><span data-stu-id="b3a1f-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3a1f-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3a1f-149">Minimum supported client</span></span><br/> | <span data-ttu-id="b3a1f-150">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b3a1f-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b3a1f-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3a1f-151">Minimum supported server</span></span><br/> | <span data-ttu-id="b3a1f-152">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b3a1f-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b3a1f-153">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b3a1f-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3a1f-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3a1f-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b3a1f-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b3a1f-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="b3a1f-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3a1f-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b3a1f-157">DLL</span><span class="sxs-lookup"><span data-stu-id="b3a1f-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3a1f-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3a1f-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3a1f-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3a1f-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3a1f-160">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b3a1f-160">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b3a1f-161">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b3a1f-161">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b3a1f-162">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="b3a1f-162">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="b3a1f-163">glEvalMesh</span><span class="sxs-lookup"><span data-stu-id="b3a1f-163">glEvalMesh</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="b3a1f-164">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="b3a1f-164">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="b3a1f-165">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="b3a1f-165">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="b3a1f-166">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="b3a1f-166">**glMap2**</span></span>](glmap2.md)
</dt> </dl>

 

 





