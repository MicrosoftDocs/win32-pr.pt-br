---
title: função glEvalPoint1 (GL. h)
description: As funções glEvalPoint1 e glEvalPoint2 geram e avaliam um único ponto em uma malha. | função glEvalPoint1 (GL. h)
ms.assetid: 5ef1d2f0-d77b-4bb8-a0d4-45c1a6a91c18
keywords:
- função glEvalPoint1 OpenGL
topic_type:
- apiref
api_name:
- glEvalPoint1
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34b9c3b8e17f5a0554c1864a401ecf49343806c7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103837882"
---
# <a name="glevalpoint1-function"></a><span data-ttu-id="791a6-105">função glEvalPoint1</span><span class="sxs-lookup"><span data-stu-id="791a6-105">glEvalPoint1 function</span></span>

<span data-ttu-id="791a6-106">As funções [**glEvalPoint1**](glevalpoint.md) e **glEvalPoint2** geram e avaliam um único ponto em uma malha.</span><span class="sxs-lookup"><span data-stu-id="791a6-106">The [**glEvalPoint1**](glevalpoint.md) and **glEvalPoint2** functions generate and evaluate a single point in a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="791a6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="791a6-107">Syntax</span></span>


```C++
void glEvalPoint1(
   GLint i
);
```



## <a name="parameters"></a><span data-ttu-id="791a6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="791a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="791a6-109">*i*</span><span class="sxs-lookup"><span data-stu-id="791a6-109">*i*</span></span> 
</dt> <dd>

<span data-ttu-id="791a6-110">O valor inteiro para a variável de domínio de grade *i*.</span><span class="sxs-lookup"><span data-stu-id="791a6-110">The integer value for grid domain variable *i*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="791a6-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="791a6-111">Return value</span></span>

<span data-ttu-id="791a6-112">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="791a6-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="791a6-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="791a6-113">Remarks</span></span>

<span data-ttu-id="791a6-114">As funções [**glMapGrid**](glmapgrid-functions.md) e [**glEvalMesh**](glevalmesh-functions.md) são usadas em conjunto para gerar e avaliar com eficiência uma série de valores de domínio de mapa com espaçamento uniforme.</span><span class="sxs-lookup"><span data-stu-id="791a6-114">The [**glMapGrid**](glmapgrid-functions.md) and [**glEvalMesh**](glevalmesh-functions.md) functions are used in tandem to efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="791a6-115">Você pode usar **glEvalPoint** para avaliar um único ponto de grade no mesmo gridspace que é percorrido pelo **glEvalMesh**.</span><span class="sxs-lookup"><span data-stu-id="791a6-115">You can use **glEvalPoint** to evaluate a single grid point in the same gridspace that is traversed by **glEvalMesh**.</span></span> <span data-ttu-id="791a6-116">Chamar [**glEvalPoint1**](glevalpoint.md) é equivalente a chamar</span><span class="sxs-lookup"><span data-stu-id="791a6-116">Calling [**glEvalPoint1**](glevalpoint.md) is equivalent to calling</span></span>

<span data-ttu-id="791a6-117">**glEvalCoord1** (*i* ?*u*  + *u* 1);</span><span class="sxs-lookup"><span data-stu-id="791a6-117">**glEvalCoord1** (*i* ?*u* +*u* 1 );</span></span>

<span data-ttu-id="791a6-118">onde</span><span class="sxs-lookup"><span data-stu-id="791a6-118">where</span></span>

<span data-ttu-id="791a6-119">? *u* = (*u* 2 *u* 1)/*n*</span><span class="sxs-lookup"><span data-stu-id="791a6-119">?*u* = (*u* 2 *u* 1 )/*n*</span></span>

<span data-ttu-id="791a6-120">e *n*, *u* 1 e *u* 2 são os argumentos para a função **glMapGrid1** mais recente.</span><span class="sxs-lookup"><span data-stu-id="791a6-120">and *n*, *u* 1 , and *u* 2 are the arguments to the most recent **glMapGrid1** function.</span></span> <span data-ttu-id="791a6-121">O requisito numérico absoluto é que, se *eu*  =  *n*, o valor calculado de (*i* ?*u* + U1) é exatamente *u* 2.</span><span class="sxs-lookup"><span data-stu-id="791a6-121">The one absolute numeric requirement is that if *i* = *n*, then the value computed from (*i* ?*u* + u1 ) is exactly *u* 2 .</span></span>

<span data-ttu-id="791a6-122">No caso bidimensional, **glEvalPoint2**, Let</span><span class="sxs-lookup"><span data-stu-id="791a6-122">In the two-dimensional case, **glEvalPoint2**, let</span></span>

<span data-ttu-id="791a6-123">? *u* = (*u* 2 *u* 1)/*n*</span><span class="sxs-lookup"><span data-stu-id="791a6-123">?*u* = (*u* 2 *u* 1 )/*n*</span></span>

<span data-ttu-id="791a6-124">? *v* = (*v* 2 *v* 1)/*m*</span><span class="sxs-lookup"><span data-stu-id="791a6-124">?*v* = (*v* 2 *v* 1 )/*m*</span></span>

<span data-ttu-id="791a6-125">onde *n*, *u* 1, *u* 2, *m*, *v* 1 e *v* 2 são os argumentos para a função **glMapGrid2** mais recente.</span><span class="sxs-lookup"><span data-stu-id="791a6-125">where *n*, *u* 1 , *u* 2 , *m*, *v* 1 , and *v* 2  are the arguments to the most recent **glMapGrid2** function.</span></span> <span data-ttu-id="791a6-126">Em seguida, a função **glEvalPoint2** é equivalente a chamar</span><span class="sxs-lookup"><span data-stu-id="791a6-126">Then the **glEvalPoint2** function is equivalent to calling</span></span>

<span data-ttu-id="791a6-127">**glEvalCoord2** (*i* ?*u*  +  *u* 1, *j* ?*v*  +  *v* 1);</span><span class="sxs-lookup"><span data-stu-id="791a6-127">**glEvalCoord2** (*i* ?*u* + *u* 1 , *j* ?*v* + *v* 1 );</span></span>

<span data-ttu-id="791a6-128">Os únicos requisitos numéricos absolutos são que, se *eu* = *n*, o valor calculado de (*i* ?*u*  +  *u* 1) é exatamente U2 e, se *j*  =  *m*, o valor calculado de (*j* ?*v*  +  *v* 1) é exatamente *v* 2.</span><span class="sxs-lookup"><span data-stu-id="791a6-128">The only absolute numeric requirements are that if *i*=*n*, then the value computed from (*i* ?*u* + *u* 1 ) is exactly u2 , and if *j* = *m*, then the value computed from (*j* ?*v* + *v* 1  ) is exactly *v* 2 .</span></span>

<span data-ttu-id="791a6-129">As funções a seguir recuperam informações relacionadas a [**glEvalPoint1**](glevalpoint.md) e **glEvalPoint2**:</span><span class="sxs-lookup"><span data-stu-id="791a6-129">The following functions retrieve information relating to [**glEvalPoint1**](glevalpoint.md) and **glEvalPoint2**:</span></span>

<span data-ttu-id="791a6-130">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ MAP1 \_ grade \_ Domain</span><span class="sxs-lookup"><span data-stu-id="791a6-130">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_DOMAIN</span></span>

<span data-ttu-id="791a6-131">**glGet** com o argumento GL \_ map2 \_ grade \_ Domain</span><span class="sxs-lookup"><span data-stu-id="791a6-131">**glGet** with argument GL\_MAP2\_GRID\_DOMAIN</span></span>

<span data-ttu-id="791a6-132">**glGet** com os segmentos de grade Argument GL \_ MAP1 \_ \_</span><span class="sxs-lookup"><span data-stu-id="791a6-132">**glGet** with argument GL\_MAP1\_GRID\_SEGMENTS</span></span>

<span data-ttu-id="791a6-133">**glGet** com os segmentos de grade Argument GL \_ map2 \_ \_</span><span class="sxs-lookup"><span data-stu-id="791a6-133">**glGet** with argument GL\_MAP2\_GRID\_SEGMENTS</span></span>

## <a name="requirements"></a><span data-ttu-id="791a6-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="791a6-134">Requirements</span></span>



| <span data-ttu-id="791a6-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="791a6-135">Requirement</span></span> | <span data-ttu-id="791a6-136">Valor</span><span class="sxs-lookup"><span data-stu-id="791a6-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="791a6-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="791a6-137">Minimum supported client</span></span><br/> | <span data-ttu-id="791a6-138">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="791a6-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="791a6-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="791a6-139">Minimum supported server</span></span><br/> | <span data-ttu-id="791a6-140">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="791a6-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="791a6-141">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="791a6-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="791a6-142"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="791a6-142"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="791a6-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="791a6-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="791a6-144"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="791a6-144"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="791a6-145">DLL</span><span class="sxs-lookup"><span data-stu-id="791a6-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="791a6-146"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="791a6-146"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="791a6-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="791a6-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="791a6-148">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="791a6-148">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="791a6-149">**glEvalMesh**</span><span class="sxs-lookup"><span data-stu-id="791a6-149">**glEvalMesh**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="791a6-150">**glGet**</span><span class="sxs-lookup"><span data-stu-id="791a6-150">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="791a6-151">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="791a6-151">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="791a6-152">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="791a6-152">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="791a6-153">**glMapGrid**</span><span class="sxs-lookup"><span data-stu-id="791a6-153">**glMapGrid**</span></span>](glmapgrid-functions.md)
</dt> </dl>

 

 





