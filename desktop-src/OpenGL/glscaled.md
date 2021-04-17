---
title: função glScaled (GL. h)
description: As funções glScaled e glScalef multiplicam a matriz atual por uma matriz de dimensionamento geral. | função glScaled (GL. h)
ms.assetid: 3846289f-5c7b-4bb6-95a8-90a58dd8b9d9
keywords:
- função glScaled OpenGL
topic_type:
- apiref
api_name:
- glScaled
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba2655924f5716e142832882441066d4772d0e63
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104566104"
---
# <a name="glscaled-function"></a><span data-ttu-id="7c3ac-105">função glScaled</span><span class="sxs-lookup"><span data-stu-id="7c3ac-105">glScaled function</span></span>

<span data-ttu-id="7c3ac-106">As funções **glScaled** e [**glScalef**](glscalef.md) multiplicam a matriz atual por uma matriz de dimensionamento geral.</span><span class="sxs-lookup"><span data-stu-id="7c3ac-106">The **glScaled** and [**glScalef**](glscalef.md) functions multiply the current matrix by a general scaling matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c3ac-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7c3ac-107">Syntax</span></span>


```C++
void WINAPI glScaled(
   GLdouble x,
   GLdouble y,
   GLdouble z
);
```



## <a name="parameters"></a><span data-ttu-id="7c3ac-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c3ac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c3ac-109">*x*</span><span class="sxs-lookup"><span data-stu-id="7c3ac-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="7c3ac-110">Fatores de escala ao longo do eixo *x* .</span><span class="sxs-lookup"><span data-stu-id="7c3ac-110">Scale factors along the *x* axis.</span></span>

</dd> <dt>

<span data-ttu-id="7c3ac-111">*y*</span><span class="sxs-lookup"><span data-stu-id="7c3ac-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="7c3ac-112">Fatores de escala ao longo do eixo *y* .</span><span class="sxs-lookup"><span data-stu-id="7c3ac-112">Scale factors along the *y* axis.</span></span>

</dd> <dt>

<span data-ttu-id="7c3ac-113">*z*</span><span class="sxs-lookup"><span data-stu-id="7c3ac-113">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="7c3ac-114">Fatores de escala ao longo do eixo *z* .</span><span class="sxs-lookup"><span data-stu-id="7c3ac-114">Scale factors along the *z* axis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c3ac-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7c3ac-115">Return value</span></span>

<span data-ttu-id="7c3ac-116">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7c3ac-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7c3ac-117">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="7c3ac-117">Error codes</span></span>

<span data-ttu-id="7c3ac-118">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="7c3ac-118">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="7c3ac-119">Nome</span><span class="sxs-lookup"><span data-stu-id="7c3ac-119">Name</span></span>                                                                                                  | <span data-ttu-id="7c3ac-120">Significado</span><span class="sxs-lookup"><span data-stu-id="7c3ac-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7c3ac-121"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7c3ac-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="7c3ac-122">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="7c3ac-122">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7c3ac-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c3ac-123">Remarks</span></span>

<span data-ttu-id="7c3ac-124">A função **glScaled** produz um dimensionamento geral ao longo dos eixos *x*, *y* e *z* .</span><span class="sxs-lookup"><span data-stu-id="7c3ac-124">The **glScaled** function produces a general scaling along the *x*, *y*, and *z* axes.</span></span> <span data-ttu-id="7c3ac-125">Os três argumentos indicam os fatores de escala desejados ao longo de cada um dos três eixos.</span><span class="sxs-lookup"><span data-stu-id="7c3ac-125">The three arguments indicate the desired scale factors along each of the three axes.</span></span> <span data-ttu-id="7c3ac-126">A matriz resultante é</span><span class="sxs-lookup"><span data-stu-id="7c3ac-126">The resulting matrix is</span></span>

![Diagrama mostrando a matriz de fatores de escala ao longo dos eixos x, y e z.](images/scale01.png)

<span data-ttu-id="7c3ac-128">A matriz atual (consulte [**glMatrixMode**](glmatrixmode.md)) é multiplicada por essa matriz de escala, com o produto que substitui a matriz atual.</span><span class="sxs-lookup"><span data-stu-id="7c3ac-128">The current matrix (see [**glMatrixMode**](glmatrixmode.md)) is multiplied by this scale matrix, with the product replacing the current matrix.</span></span> <span data-ttu-id="7c3ac-129">Ou seja, se M for a matriz atual e S for a matriz de escala, M será substituído por M S.</span><span class="sxs-lookup"><span data-stu-id="7c3ac-129">That is, if M is the current matrix and S is the scale matrix, then M is replaced with M   S.</span></span>

<span data-ttu-id="7c3ac-130">Se o modo de matriz for uma \_ projeção GL MODELVIEW ou GL \_ , todos os objetos desenhados após o **glScaled** são chamados são dimensionados.</span><span class="sxs-lookup"><span data-stu-id="7c3ac-130">If the matrix mode is either GL\_MODELVIEW or GL\_PROJECTION, all objects drawn after **glScaled** is called are scaled.</span></span> <span data-ttu-id="7c3ac-131">Use [**glPushMatrix**](glpushmatrix.md) e [**glPopMatrix**](glpopmatrix.md) para salvar e restaurar o sistema de coordenadas não dimensionada.</span><span class="sxs-lookup"><span data-stu-id="7c3ac-131">Use [**glPushMatrix**](glpushmatrix.md) and [**glPopMatrix**](glpopmatrix.md) to save and restore the unscaled coordinate system.</span></span>

<span data-ttu-id="7c3ac-132">Se fatores de escala diferentes de 1,0 forem aplicados à matriz modelview e a iluminação estiver habilitada, a normalização automática de Normals provavelmente também deverá ser habilitada ([**glEnable**](glenable.md) e [**GLDISABLE**](gldisable.md) com Argument GL \_ NORMALIZE).</span><span class="sxs-lookup"><span data-stu-id="7c3ac-132">If scale factors other than 1.0 are applied to the modelview matrix and lighting is enabled, automatic normalization of normals should probably also be enabled ([**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with argument GL\_NORMALIZE).</span></span>

<span data-ttu-id="7c3ac-133">As funções a seguir recuperam informações relacionadas ao **glScaled**:</span><span class="sxs-lookup"><span data-stu-id="7c3ac-133">The following functions retrieve information related to **glScaled**:</span></span>

<span data-ttu-id="7c3ac-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ modo de matriz GL de argumento \_</span><span class="sxs-lookup"><span data-stu-id="7c3ac-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="7c3ac-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ MODELVIEW \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="7c3ac-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="7c3ac-136">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) \_ matriz de projeção GLGET com Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="7c3ac-136">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="7c3ac-137">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com matriz de \_ textura Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="7c3ac-137">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="7c3ac-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c3ac-138">Requirements</span></span>



| <span data-ttu-id="7c3ac-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c3ac-139">Requirement</span></span> | <span data-ttu-id="7c3ac-140">Valor</span><span class="sxs-lookup"><span data-stu-id="7c3ac-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c3ac-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c3ac-141">Minimum supported client</span></span><br/> | <span data-ttu-id="7c3ac-142">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7c3ac-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7c3ac-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c3ac-143">Minimum supported server</span></span><br/> | <span data-ttu-id="7c3ac-144">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7c3ac-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7c3ac-145">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7c3ac-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c3ac-146"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c3ac-146"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="7c3ac-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7c3ac-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="7c3ac-148"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c3ac-148"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7c3ac-149">DLL</span><span class="sxs-lookup"><span data-stu-id="7c3ac-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c3ac-150"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c3ac-150"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c3ac-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c3ac-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c3ac-152">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="7c3ac-152">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="7c3ac-153">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="7c3ac-153">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="7c3ac-154">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="7c3ac-154">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="7c3ac-155">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="7c3ac-155">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="7c3ac-156">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="7c3ac-156">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="7c3ac-157">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="7c3ac-157">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="7c3ac-158">**glRotated**</span><span class="sxs-lookup"><span data-stu-id="7c3ac-158">**glRotated**</span></span>](glrotated.md)
</dt> <dt>

[<span data-ttu-id="7c3ac-159">**glRotatef**</span><span class="sxs-lookup"><span data-stu-id="7c3ac-159">**glRotatef**</span></span>](glrotatef.md)
</dt> <dt>

[<span data-ttu-id="7c3ac-160">**glTranslate**</span><span class="sxs-lookup"><span data-stu-id="7c3ac-160">**glTranslate**</span></span>](gltranslate.md)
</dt> </dl>

 

 





