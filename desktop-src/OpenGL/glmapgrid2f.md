---
title: função glMapGrid2f (GL. h)
description: Define uma malha unidimensional. | função glMapGrid2f (GL. h)
ms.assetid: f9bc2b0c-dec5-4762-8c99-46546a81893e
keywords:
- função glMapGrid2f OpenGL
topic_type:
- apiref
api_name:
- glMapGrid2f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 087e42aa3d490ec605b4478d5691b256271268f5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172627"
---
# <a name="glmapgrid2f-function"></a><span data-ttu-id="39b89-105">função glMapGrid2f</span><span class="sxs-lookup"><span data-stu-id="39b89-105">glMapGrid2f function</span></span>

<span data-ttu-id="39b89-106">Define uma malha unidimensional.</span><span class="sxs-lookup"><span data-stu-id="39b89-106">Defines a one-dimensional mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="39b89-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="39b89-107">Syntax</span></span>


```C++
void WINAPI glMapGrid2f(
   GLint   un,
   GLfloat u1,
   GLfloat u2,
   GLint   vn,
   GLfloat v1,
   GLfloat v2
);
```



## <a name="parameters"></a><span data-ttu-id="39b89-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39b89-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39b89-109">*anula*</span><span class="sxs-lookup"><span data-stu-id="39b89-109">*un*</span></span> 
</dt> <dd>

<span data-ttu-id="39b89-110">O número de partições no intervalo de intervalo de grade \[ U1, U2 \] .</span><span class="sxs-lookup"><span data-stu-id="39b89-110">The number of partitions in the grid range interval \[u1, u2\].</span></span> <span data-ttu-id="39b89-111">Esse valor deve ser positivo.</span><span class="sxs-lookup"><span data-stu-id="39b89-111">This value must be positive.</span></span>

</dd> <dt>

<span data-ttu-id="39b89-112">*U1*</span><span class="sxs-lookup"><span data-stu-id="39b89-112">*u1*</span></span> 
</dt> <dd>

<span data-ttu-id="39b89-113">Um valor usado como o mapeamento para o valor de domínio da grade de inteiros i = 0.</span><span class="sxs-lookup"><span data-stu-id="39b89-113">A value used as the mapping for integer grid domain value i = 0.</span></span>

</dd> <dt>

<span data-ttu-id="39b89-114">*U2*</span><span class="sxs-lookup"><span data-stu-id="39b89-114">*u2*</span></span> 
</dt> <dd>

<span data-ttu-id="39b89-115">Um valor usado como o mapeamento para o valor de domínio da grade de inteiros i = un.</span><span class="sxs-lookup"><span data-stu-id="39b89-115">A value used as the mapping for integer grid domain value i = un.</span></span>

</dd> <dt>

<span data-ttu-id="39b89-116">*vn*</span><span class="sxs-lookup"><span data-stu-id="39b89-116">*vn*</span></span> 
</dt> <dd>

<span data-ttu-id="39b89-117">O número de partições no intervalo de intervalo de grade \[ v1, v2 \] .</span><span class="sxs-lookup"><span data-stu-id="39b89-117">The number of partitions in the grid range interval \[v1, v2\].</span></span>

</dd> <dt>

<span data-ttu-id="39b89-118">*v1*</span><span class="sxs-lookup"><span data-stu-id="39b89-118">*v1*</span></span> 
</dt> <dd>

<span data-ttu-id="39b89-119">Um valor usado como o mapeamento para o valor de domínio da grade de inteiros j = 0.</span><span class="sxs-lookup"><span data-stu-id="39b89-119">A value used as the mapping for integer grid domain value j = 0.</span></span>

</dd> <dt>

<span data-ttu-id="39b89-120">*v2*</span><span class="sxs-lookup"><span data-stu-id="39b89-120">*v2*</span></span> 
</dt> <dd>

<span data-ttu-id="39b89-121">Um valor usado como o mapeamento para o valor de domínio da grade de inteiros j = vn.</span><span class="sxs-lookup"><span data-stu-id="39b89-121">A value used as the mapping for integer grid domain value j = vn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39b89-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="39b89-122">Return value</span></span>

<span data-ttu-id="39b89-123">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="39b89-123">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="39b89-124">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="39b89-124">Error codes</span></span>

<span data-ttu-id="39b89-125">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="39b89-125">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="39b89-126">Nome</span><span class="sxs-lookup"><span data-stu-id="39b89-126">Name</span></span>                                                                                                  | <span data-ttu-id="39b89-127">Significado</span><span class="sxs-lookup"><span data-stu-id="39b89-127">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="39b89-128"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="39b89-128"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="39b89-129">O  *vn* não era positivo.</span><span class="sxs-lookup"><span data-stu-id="39b89-129">Either *un* or *vn* was not positive.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="39b89-130"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="39b89-130"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="39b89-131">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="39b89-131">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="39b89-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="39b89-132">Remarks</span></span>

<span data-ttu-id="39b89-133">As funções **glMapGrid** e [glEvalMesh](glevalmesh-functions.md) são usadas em conjunto para gerar e avaliar com eficiência uma série de valores de domínio de mapa com espaçamento uniforme.</span><span class="sxs-lookup"><span data-stu-id="39b89-133">The **glMapGrid** and [glEvalMesh](glevalmesh-functions.md) functions are used in tandem to efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="39b89-134">A função glEvalMesh percorre o domínio inteiro de uma grade de uma ou duas dimensões, cujo intervalo é o domínio dos mapas de avaliação especificados por [**glMap1**](glmap1.md) e [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="39b89-134">The glEvalMesh function steps through the integer domain of a one- or two-dimensional grid, whose range is the domain of the evaluation maps specified by [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span>

<span data-ttu-id="39b89-135">As funções [**glMapGrid1**](glmapgrid1d.md) e [**glMapGrid2**](glmapgrid2d.md) especificam os mapeamentos de grade linear entre as coordenadas de grade de inteiros i (ou i e j) para as coordenadas de mapa de avaliação de ponto flutuante u (ou você e v).</span><span class="sxs-lookup"><span data-stu-id="39b89-135">The [**glMapGrid1**](glmapgrid1d.md) and [**glMapGrid2**](glmapgrid2d.md) functions specify the linear grid mappings between the i (or i and j) integer grid coordinates, to the u (or u and v) floating-point evaluation map coordinates.</span></span> <span data-ttu-id="39b89-136">Consulte [**glMap1**](glmap1.md) e [**glMap2**](glmap2.md) para obter detalhes de como você e as coordenadas v são avaliados.</span><span class="sxs-lookup"><span data-stu-id="39b89-136">See [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md) for details of how u and v coordinates are evaluated.</span></span>

<span data-ttu-id="39b89-137">A função [**glMapGrid1**](glmapgrid1d.md) especifica um mapeamento linear único, de modo que *a coordenada* de grade de inteiros 0 é mapeada exatamente para U1, e a coordenada de grade de inteiros remapeia exatamente para *U2*.</span><span class="sxs-lookup"><span data-stu-id="39b89-137">The [**glMapGrid1**](glmapgrid1d.md) function specifies a single linear mapping such that integer grid coordinate 0 maps exactly to u1, and integer grid coordinate *un* maps exactly to *u2*.</span></span> <span data-ttu-id="39b89-138">Todas as outras coordenadas de grade de *inteiros que são* mapeadas de modo que:</span><span class="sxs-lookup"><span data-stu-id="39b89-138">All other integer grid coordinates *i* are mapped such that:</span></span>

<span data-ttu-id="39b89-139">*u = i (U2 U1)/un + U1*</span><span class="sxs-lookup"><span data-stu-id="39b89-139">*u = i(u2 u1)/un + u1*</span></span>

<span data-ttu-id="39b89-140">A função [**glMapGrid2**](glmapgrid2d.md) especifica dois mapeamentos lineares.</span><span class="sxs-lookup"><span data-stu-id="39b89-140">The [**glMapGrid2**](glmapgrid2d.md) function specifies two such linear mappings.</span></span> <span data-ttu-id="39b89-141">Um mapeia a coordenada de grade de inteiros *i = 0* exatamente para *U1* e a coordenada de grade de inteiros *i =* não exatamente como *U2*.</span><span class="sxs-lookup"><span data-stu-id="39b89-141">One maps integer grid coordinate *i = 0* exactly to *u1*, and integer grid coordinate *i = un* exactly to *u2*.</span></span> <span data-ttu-id="39b89-142">A outra coordenada de grade de inteiros de mapas *j = 0* exatamente para *v1* e a coordenada de grade de inteiros *j = vn* exatamente para *v2*.</span><span class="sxs-lookup"><span data-stu-id="39b89-142">The other maps integer grid coordinate *j = 0* exactly to *v1*, and integer grid coordinate *j = vn* exactly to *v2*.</span></span> <span data-ttu-id="39b89-143">Outras coordenadas de grade de inteiros i e j são mapeadas de modo que</span><span class="sxs-lookup"><span data-stu-id="39b89-143">Other integer grid coordinates i and j are mapped such that</span></span>

<span data-ttu-id="39b89-144">*u = i (U2 U1)/un + U1*</span><span class="sxs-lookup"><span data-stu-id="39b89-144">*u = i(u2 u1)/un + u1*</span></span>

<span data-ttu-id="39b89-145">*v = j (v2 v1)/VN + v1*</span><span class="sxs-lookup"><span data-stu-id="39b89-145">*v = j (v2 v1)/vn + v1*</span></span>

<span data-ttu-id="39b89-146">Os mapeamentos especificados por [**glMapGrid**](glmapgrid1d.md) são usados de forma idêntica por [glEvalMesh](glevalmesh-functions.md) e [**glEvalPoint**](glevalpoint.md).</span><span class="sxs-lookup"><span data-stu-id="39b89-146">The mappings specified by [**glMapGrid**](glmapgrid1d.md) are used identically by [glEvalMesh](glevalmesh-functions.md) and [**glEvalPoint**](glevalpoint.md).</span></span>

<span data-ttu-id="39b89-147">As funções a seguir recuperam informações relacionadas ao [**glMapGrid**](glmapgrid1d.md):</span><span class="sxs-lookup"><span data-stu-id="39b89-147">The following functions retrieve information related to [**glMapGrid**](glmapgrid1d.md):</span></span>

<dl>

<span data-ttu-id="39b89-148">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ MAP1 \_ grade \_ Domain</span><span class="sxs-lookup"><span data-stu-id="39b89-148">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_DOMAIN</span></span>  
<span data-ttu-id="39b89-149">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ map2 \_ grade \_ Domain</span><span class="sxs-lookup"><span data-stu-id="39b89-149">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_DOMAIN</span></span>  
<span data-ttu-id="39b89-150">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com os segmentos de grade Argument GL \_ MAP1 \_ \_</span><span class="sxs-lookup"><span data-stu-id="39b89-150">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_SEGMENTS</span></span>  
<span data-ttu-id="39b89-151">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com os segmentos de grade Argument GL \_ map2 \_ \_</span><span class="sxs-lookup"><span data-stu-id="39b89-151">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_SEGMENTS</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="39b89-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39b89-152">Requirements</span></span>



| <span data-ttu-id="39b89-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="39b89-153">Requirement</span></span> | <span data-ttu-id="39b89-154">Valor</span><span class="sxs-lookup"><span data-stu-id="39b89-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39b89-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39b89-155">Minimum supported client</span></span><br/> | <span data-ttu-id="39b89-156">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="39b89-156">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="39b89-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39b89-157">Minimum supported server</span></span><br/> | <span data-ttu-id="39b89-158">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="39b89-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="39b89-159">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="39b89-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="39b89-160"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="39b89-160"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="39b89-161">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="39b89-161">Library</span></span><br/>                  | <dl> <span data-ttu-id="39b89-162"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="39b89-162"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="39b89-163">DLL</span><span class="sxs-lookup"><span data-stu-id="39b89-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39b89-164"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39b89-164"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39b89-165">Confira também</span><span class="sxs-lookup"><span data-stu-id="39b89-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39b89-166">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="39b89-166">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="39b89-167">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="39b89-167">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="39b89-168">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="39b89-168">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="39b89-169">glEvalMesh</span><span class="sxs-lookup"><span data-stu-id="39b89-169">glEvalMesh</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="39b89-170">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="39b89-170">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="39b89-171">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="39b89-171">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="39b89-172">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="39b89-172">**glMap2**</span></span>](glmap2.md)
</dt> </dl>

 

 





