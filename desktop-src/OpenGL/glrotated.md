---
title: função glRotated (GL. h)
description: A função glRotated multiplica a matriz atual por uma matriz de rotação.
ms.assetid: 9adfeb5b-8c2a-4acf-a251-6ba23cc4c3a6
keywords:
- função glRotated OpenGL
topic_type:
- apiref
api_name:
- glRotated
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d0678e9da6f0b68047708f45fda1c9da66d8139
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499792"
---
# <a name="glrotated-function"></a><span data-ttu-id="63596-104">função glRotated</span><span class="sxs-lookup"><span data-stu-id="63596-104">glRotated function</span></span>

<span data-ttu-id="63596-105">A função **glRotated** multiplica a matriz atual por uma matriz de rotação.</span><span class="sxs-lookup"><span data-stu-id="63596-105">The **glRotated** function multiplies the current matrix by a rotation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="63596-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63596-106">Syntax</span></span>


```C++
void WINAPI glRotated(
   GLdouble angle,
   GLdouble x,
   GLdouble y,
   GLdouble z
);
```



## <a name="parameters"></a><span data-ttu-id="63596-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="63596-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63596-108">*angle*</span><span class="sxs-lookup"><span data-stu-id="63596-108">*angle*</span></span> 
</dt> <dd>

<span data-ttu-id="63596-109">O ângulo de rotação, em graus.</span><span class="sxs-lookup"><span data-stu-id="63596-109">The angle of rotation, in degrees.</span></span>

</dd> <dt>

<span data-ttu-id="63596-110">*x*</span><span class="sxs-lookup"><span data-stu-id="63596-110">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="63596-111">A coordenada *x* de um vetor.</span><span class="sxs-lookup"><span data-stu-id="63596-111">The *x* coordinate of a vector.</span></span>

</dd> <dt>

<span data-ttu-id="63596-112">*y*</span><span class="sxs-lookup"><span data-stu-id="63596-112">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="63596-113">A coordenada *y* de um vetor.</span><span class="sxs-lookup"><span data-stu-id="63596-113">The *y* coordinate of a vector.</span></span>

</dd> <dt>

<span data-ttu-id="63596-114">*z*</span><span class="sxs-lookup"><span data-stu-id="63596-114">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="63596-115">A coordenada *z* de um vetor.</span><span class="sxs-lookup"><span data-stu-id="63596-115">The *z* coordinate of a vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63596-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="63596-116">Return value</span></span>

<span data-ttu-id="63596-117">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="63596-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="63596-118">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="63596-118">Error codes</span></span>

<span data-ttu-id="63596-119">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="63596-119">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="63596-120">Nome</span><span class="sxs-lookup"><span data-stu-id="63596-120">Name</span></span>                                                                                                  | <span data-ttu-id="63596-121">Significado</span><span class="sxs-lookup"><span data-stu-id="63596-121">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="63596-122"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="63596-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="63596-123">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="63596-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="63596-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="63596-124">Remarks</span></span>

<span data-ttu-id="63596-125">A função **glRotated** computa uma matriz que executa uma rotação no sentido anti-horário de graus de *ângulo* sobre o vetor da origem por meio do ponto (*x*, *y*, *z*).</span><span class="sxs-lookup"><span data-stu-id="63596-125">The **glRotated** function computes a matrix that performs a counterclockwise rotation of *angle* degrees about the vector from the origin through the point (*x*, *y*, *z*).</span></span>

<span data-ttu-id="63596-126">A matriz atual (consulte [**glMatrixMode**](glmatrixmode.md)) é multiplicada por essa matriz de rotação, com o produto que substitui a matriz atual.</span><span class="sxs-lookup"><span data-stu-id="63596-126">The current matrix (see [**glMatrixMode**](glmatrixmode.md)) is multiplied by this rotation matrix, with the product replacing the current matrix.</span></span> <span data-ttu-id="63596-127">Ou seja, se M for a matriz atual e o R for a matriz de conversão, M será substituído por M R.</span><span class="sxs-lookup"><span data-stu-id="63596-127">That is, if M is the current matrix and R is the translation matrix, then M is replaced with M   R.</span></span>

<span data-ttu-id="63596-128">Se o modo de matriz for uma \_ projeção GL MODELVIEW ou GL \_ , todos os objetos desenhados depois de **glRotated** serão girados.</span><span class="sxs-lookup"><span data-stu-id="63596-128">If the matrix mode is either GL\_MODELVIEW or GL\_PROJECTION, all objects drawn after **glRotated** is called are rotated.</span></span> <span data-ttu-id="63596-129">Use [**glPushMatrix**](glpushmatrix.md) e [**glPopMatrix**](glpopmatrix.md) para salvar e restaurar o sistema de coordenadas não girado.</span><span class="sxs-lookup"><span data-stu-id="63596-129">Use [**glPushMatrix**](glpushmatrix.md) and [**glPopMatrix**](glpopmatrix.md) to save and restore the unrotated coordinate system.</span></span>

<span data-ttu-id="63596-130">As funções a seguir recuperam informações relacionadas ao **glRotated**:</span><span class="sxs-lookup"><span data-stu-id="63596-130">The following functions retrieve information related to **glRotated**:</span></span>

<span data-ttu-id="63596-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ modo de renderização Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="63596-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_RENDER\_MODE</span></span>

<span data-ttu-id="63596-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ modo de matriz GL de argumento \_</span><span class="sxs-lookup"><span data-stu-id="63596-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="63596-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ MODELVIEW \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="63596-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="63596-134">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) \_ matriz de projeção GLGET com Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="63596-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="63596-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com matriz de \_ textura Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="63596-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="63596-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63596-136">Requirements</span></span>



| <span data-ttu-id="63596-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="63596-137">Requirement</span></span> | <span data-ttu-id="63596-138">Valor</span><span class="sxs-lookup"><span data-stu-id="63596-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63596-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63596-139">Minimum supported client</span></span><br/> | <span data-ttu-id="63596-140">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="63596-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="63596-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63596-141">Minimum supported server</span></span><br/> | <span data-ttu-id="63596-142">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="63596-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="63596-143">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="63596-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="63596-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="63596-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="63596-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="63596-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="63596-146"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63596-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="63596-147">DLL</span><span class="sxs-lookup"><span data-stu-id="63596-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63596-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63596-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63596-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="63596-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63596-150">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="63596-150">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="63596-151">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="63596-151">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="63596-152">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="63596-152">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="63596-153">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="63596-153">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="63596-154">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="63596-154">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="63596-155">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="63596-155">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="63596-156">**glScale**</span><span class="sxs-lookup"><span data-stu-id="63596-156">**glScale**</span></span>](glscale.md)
</dt> <dt>

[<span data-ttu-id="63596-157">**glTranslate**</span><span class="sxs-lookup"><span data-stu-id="63596-157">**glTranslate**</span></span>](gltranslate.md)
</dt> </dl>

 

 





