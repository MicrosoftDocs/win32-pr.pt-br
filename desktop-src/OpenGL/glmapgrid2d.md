---
title: função glMapGrid2d (GL. h)
description: Define uma malha unidimensional. | função glMapGrid2d (GL. h)
ms.assetid: 5e5887d1-e137-434b-a1f3-b3f10d462823
keywords:
- função glMapGrid2d OpenGL
topic_type:
- apiref
api_name:
- glMapGrid2d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6992a904528cf961f27335e7241c50fbd14f058b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105753126"
---
# <a name="glmapgrid2d-function"></a><span data-ttu-id="6f735-105">função glMapGrid2d</span><span class="sxs-lookup"><span data-stu-id="6f735-105">glMapGrid2d function</span></span>

<span data-ttu-id="6f735-106">Define uma malha unidimensional.</span><span class="sxs-lookup"><span data-stu-id="6f735-106">Defines a one-dimensional mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f735-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6f735-107">Syntax</span></span>


```C++
void WINAPI glMapGrid2d(
   GLint    un,
   GLdouble u1,
   GLdouble u2,
   GLint    vn,
   GLdouble v1,
   GLdouble v2
);
```



## <a name="parameters"></a><span data-ttu-id="6f735-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6f735-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f735-109">*anula*</span><span class="sxs-lookup"><span data-stu-id="6f735-109">*un*</span></span> 
</dt> <dd>

<span data-ttu-id="6f735-110">O número de partições no intervalo de intervalo de grade \[ U1, U2 \] .</span><span class="sxs-lookup"><span data-stu-id="6f735-110">The number of partitions in the grid range interval \[u1, u2\].</span></span> <span data-ttu-id="6f735-111">Esse valor deve ser positivo.</span><span class="sxs-lookup"><span data-stu-id="6f735-111">This value must be positive.</span></span>

</dd> <dt>

<span data-ttu-id="6f735-112">*U1*</span><span class="sxs-lookup"><span data-stu-id="6f735-112">*u1*</span></span> 
</dt> <dd>

<span data-ttu-id="6f735-113">Um valor usado como o mapeamento para o valor de domínio da grade de inteiros i = 0.</span><span class="sxs-lookup"><span data-stu-id="6f735-113">A value used as the mapping for integer grid domain value i = 0.</span></span>

</dd> <dt>

<span data-ttu-id="6f735-114">*U2*</span><span class="sxs-lookup"><span data-stu-id="6f735-114">*u2*</span></span> 
</dt> <dd>

<span data-ttu-id="6f735-115">Um valor usado como o mapeamento para o valor de domínio da grade de inteiros i = un.</span><span class="sxs-lookup"><span data-stu-id="6f735-115">A value used as the mapping for integer grid domain value i = un.</span></span>

</dd> <dt>

<span data-ttu-id="6f735-116">*vn*</span><span class="sxs-lookup"><span data-stu-id="6f735-116">*vn*</span></span> 
</dt> <dd>

<span data-ttu-id="6f735-117">O número de partições no intervalo de intervalo de grade \[ v1, v2 \] .</span><span class="sxs-lookup"><span data-stu-id="6f735-117">The number of partitions in the grid range interval \[v1, v2\].</span></span>

</dd> <dt>

<span data-ttu-id="6f735-118">*v1*</span><span class="sxs-lookup"><span data-stu-id="6f735-118">*v1*</span></span> 
</dt> <dd>

<span data-ttu-id="6f735-119">Um valor usado como o mapeamento para o valor de domínio da grade de inteiros j = 0.</span><span class="sxs-lookup"><span data-stu-id="6f735-119">A value used as the mapping for integer grid domain value j = 0.</span></span>

</dd> <dt>

<span data-ttu-id="6f735-120">*v2*</span><span class="sxs-lookup"><span data-stu-id="6f735-120">*v2*</span></span> 
</dt> <dd>

<span data-ttu-id="6f735-121">Um valor usado como o mapeamento para o valor de domínio da grade de inteiros j = vn.</span><span class="sxs-lookup"><span data-stu-id="6f735-121">A value used as the mapping for integer grid domain value j = vn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f735-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6f735-122">Return value</span></span>

<span data-ttu-id="6f735-123">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6f735-123">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6f735-124">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="6f735-124">Error codes</span></span>

<span data-ttu-id="6f735-125">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="6f735-125">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="6f735-126">Nome</span><span class="sxs-lookup"><span data-stu-id="6f735-126">Name</span></span>                                                                                                  | <span data-ttu-id="6f735-127">Significado</span><span class="sxs-lookup"><span data-stu-id="6f735-127">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6f735-128"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6f735-128"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="6f735-129">O  *vn* não era positivo.</span><span class="sxs-lookup"><span data-stu-id="6f735-129">Either *un* or *vn* was not positive.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="6f735-130"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6f735-130"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="6f735-131">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="6f735-131">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6f735-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f735-132">Remarks</span></span>

<span data-ttu-id="6f735-133">As funções **glMapGrid** e [glEvalMesh](glevalmesh-functions.md) são usadas em conjunto para gerar e avaliar com eficiência uma série de valores de domínio de mapa com espaçamento uniforme.</span><span class="sxs-lookup"><span data-stu-id="6f735-133">The **glMapGrid** and [glEvalMesh](glevalmesh-functions.md) functions are used in tandem to efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="6f735-134">A função glEvalMesh percorre o domínio inteiro de uma grade de uma ou duas dimensões, cujo intervalo é o domínio dos mapas de avaliação especificados por [**glMap1**](glmap1.md) e [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="6f735-134">The glEvalMesh function steps through the integer domain of a one- or two-dimensional grid, whose range is the domain of the evaluation maps specified by [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span>

<span data-ttu-id="6f735-135">As funções [**glMapGrid1**](glmapgrid1d.md) e **glMapGrid2** especificam os mapeamentos de grade linear entre as coordenadas de grade de inteiros i (ou i e j) para as coordenadas de mapa de avaliação de ponto flutuante u (ou você e v).</span><span class="sxs-lookup"><span data-stu-id="6f735-135">The [**glMapGrid1**](glmapgrid1d.md) and **glMapGrid2** functions specify the linear grid mappings between the i (or i and j) integer grid coordinates, to the u (or u and v) floating-point evaluation map coordinates.</span></span> <span data-ttu-id="6f735-136">Consulte [**glMap1**](glmap1.md) e [**glMap2**](glmap2.md) para obter detalhes de como você e as coordenadas v são avaliados.</span><span class="sxs-lookup"><span data-stu-id="6f735-136">See [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md) for details of how u and v coordinates are evaluated.</span></span>

<span data-ttu-id="6f735-137">A função [**glMapGrid1**](glmapgrid1d.md) especifica um mapeamento linear único, de modo que *a coordenada* de grade de inteiros 0 é mapeada exatamente para U1, e a coordenada de grade de inteiros remapeia exatamente para *U2*.</span><span class="sxs-lookup"><span data-stu-id="6f735-137">The [**glMapGrid1**](glmapgrid1d.md) function specifies a single linear mapping such that integer grid coordinate 0 maps exactly to u1, and integer grid coordinate *un* maps exactly to *u2*.</span></span> <span data-ttu-id="6f735-138">Todas as outras coordenadas de grade de *inteiros que são* mapeadas de modo que:</span><span class="sxs-lookup"><span data-stu-id="6f735-138">All other integer grid coordinates *i* are mapped such that:</span></span>

<span data-ttu-id="6f735-139">*u = i (U2 U1)/un + U1*</span><span class="sxs-lookup"><span data-stu-id="6f735-139">*u = i(u2 u1)/un + u1*</span></span>

<span data-ttu-id="6f735-140">A função **glMapGrid2** especifica dois mapeamentos lineares.</span><span class="sxs-lookup"><span data-stu-id="6f735-140">The **glMapGrid2** function specifies two such linear mappings.</span></span> <span data-ttu-id="6f735-141">Um mapeia a coordenada de grade de inteiros *i = 0* exatamente para *U1* e a coordenada de grade de inteiros *i =* não exatamente como *U2*.</span><span class="sxs-lookup"><span data-stu-id="6f735-141">One maps integer grid coordinate *i = 0* exactly to *u1*, and integer grid coordinate *i = un* exactly to *u2*.</span></span> <span data-ttu-id="6f735-142">A outra coordenada de grade de inteiros de mapas *j = 0* exatamente para *v1* e a coordenada de grade de inteiros *j = vn* exatamente para *v2*.</span><span class="sxs-lookup"><span data-stu-id="6f735-142">The other maps integer grid coordinate *j = 0* exactly to *v1*, and integer grid coordinate *j = vn* exactly to *v2*.</span></span> <span data-ttu-id="6f735-143">Outras coordenadas de grade de inteiros i e j são mapeadas de modo que</span><span class="sxs-lookup"><span data-stu-id="6f735-143">Other integer grid coordinates i and j are mapped such that</span></span>

<span data-ttu-id="6f735-144">*u = i (U2 U1)/un + U1*</span><span class="sxs-lookup"><span data-stu-id="6f735-144">*u = i(u2 u1)/un + u1*</span></span>

<span data-ttu-id="6f735-145">*v = j (v2 v1)/VN + v1*</span><span class="sxs-lookup"><span data-stu-id="6f735-145">*v = j (v2 v1)/vn + v1*</span></span>

<span data-ttu-id="6f735-146">Os mapeamentos especificados por [**glMapGrid**](glmapgrid1d.md) são usados de forma idêntica por [glEvalMesh](glevalmesh-functions.md) e [**glEvalPoint**](glevalpoint.md).</span><span class="sxs-lookup"><span data-stu-id="6f735-146">The mappings specified by [**glMapGrid**](glmapgrid1d.md) are used identically by [glEvalMesh](glevalmesh-functions.md) and [**glEvalPoint**](glevalpoint.md).</span></span>

<span data-ttu-id="6f735-147">As funções a seguir recuperam informações relacionadas ao [**glMapGrid**](glmapgrid1d.md):</span><span class="sxs-lookup"><span data-stu-id="6f735-147">The following functions retrieve information related to [**glMapGrid**](glmapgrid1d.md):</span></span>

<dl>

<span data-ttu-id="6f735-148">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ MAP1 \_ grade \_ Domain</span><span class="sxs-lookup"><span data-stu-id="6f735-148">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_DOMAIN</span></span>  
<span data-ttu-id="6f735-149">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ map2 \_ grade \_ Domain</span><span class="sxs-lookup"><span data-stu-id="6f735-149">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_DOMAIN</span></span>  
<span data-ttu-id="6f735-150">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com os segmentos de grade Argument GL \_ MAP1 \_ \_</span><span class="sxs-lookup"><span data-stu-id="6f735-150">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_SEGMENTS</span></span>  
<span data-ttu-id="6f735-151">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com os segmentos de grade Argument GL \_ map2 \_ \_</span><span class="sxs-lookup"><span data-stu-id="6f735-151">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_SEGMENTS</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="6f735-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f735-152">Requirements</span></span>



| <span data-ttu-id="6f735-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f735-153">Requirement</span></span> | <span data-ttu-id="6f735-154">Valor</span><span class="sxs-lookup"><span data-stu-id="6f735-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f735-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f735-155">Minimum supported client</span></span><br/> | <span data-ttu-id="6f735-156">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6f735-156">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6f735-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f735-157">Minimum supported server</span></span><br/> | <span data-ttu-id="6f735-158">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6f735-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6f735-159">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6f735-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f735-160"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f735-160"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6f735-161">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6f735-161">Library</span></span><br/>                  | <dl> <span data-ttu-id="6f735-162"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f735-162"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6f735-163">DLL</span><span class="sxs-lookup"><span data-stu-id="6f735-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f735-164"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f735-164"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f735-165">Confira também</span><span class="sxs-lookup"><span data-stu-id="6f735-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f735-166">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="6f735-166">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="6f735-167">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="6f735-167">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="6f735-168">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="6f735-168">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="6f735-169">glEvalMesh</span><span class="sxs-lookup"><span data-stu-id="6f735-169">glEvalMesh</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="6f735-170">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="6f735-170">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="6f735-171">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="6f735-171">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="6f735-172">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="6f735-172">**glMap2**</span></span>](glmap2.md)
</dt> </dl>

 

 





