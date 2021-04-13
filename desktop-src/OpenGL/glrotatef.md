---
title: função glRotatef (GL. h)
description: A função glRotatef multiplica a matriz atual por uma matriz de rotação.
ms.assetid: 8216a125-de8c-44e5-afb3-3d4e5ffc600d
keywords:
- função glRotatef OpenGL
topic_type:
- apiref
api_name:
- glRotatef
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 953b8ffc5f89e5a4cf9901e4cb5fb5afb4c8dfdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104456017"
---
# <a name="glrotatef-function"></a><span data-ttu-id="c8cda-104">função glRotatef</span><span class="sxs-lookup"><span data-stu-id="c8cda-104">glRotatef function</span></span>

<span data-ttu-id="c8cda-105">A função **glRotatef** multiplica a matriz atual por uma matriz de rotação.</span><span class="sxs-lookup"><span data-stu-id="c8cda-105">The **glRotatef** function multiplies the current matrix by a rotation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8cda-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c8cda-106">Syntax</span></span>


```C++
void WINAPI glRotatef(
   GLfloat angle,
   GLfloat x,
   GLfloat y,
   GLfloat z
);
```



## <a name="parameters"></a><span data-ttu-id="c8cda-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c8cda-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8cda-108">*angle*</span><span class="sxs-lookup"><span data-stu-id="c8cda-108">*angle*</span></span> 
</dt> <dd>

<span data-ttu-id="c8cda-109">O ângulo de rotação, em graus.</span><span class="sxs-lookup"><span data-stu-id="c8cda-109">The angle of rotation, in degrees.</span></span>

</dd> <dt>

<span data-ttu-id="c8cda-110">*x*</span><span class="sxs-lookup"><span data-stu-id="c8cda-110">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="c8cda-111">A coordenada *x* de um vetor.</span><span class="sxs-lookup"><span data-stu-id="c8cda-111">The *x* coordinate of a vector.</span></span>

</dd> <dt>

<span data-ttu-id="c8cda-112">*y*</span><span class="sxs-lookup"><span data-stu-id="c8cda-112">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="c8cda-113">A coordenada *y* de um vetor.</span><span class="sxs-lookup"><span data-stu-id="c8cda-113">The *y* coordinate of a vector.</span></span>

</dd> <dt>

<span data-ttu-id="c8cda-114">*z*</span><span class="sxs-lookup"><span data-stu-id="c8cda-114">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="c8cda-115">A coordenada *z* de um vetor.</span><span class="sxs-lookup"><span data-stu-id="c8cda-115">The *z* coordinate of a vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8cda-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c8cda-116">Return value</span></span>

<span data-ttu-id="c8cda-117">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c8cda-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c8cda-118">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="c8cda-118">Error codes</span></span>

<span data-ttu-id="c8cda-119">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="c8cda-119">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="c8cda-120">Nome</span><span class="sxs-lookup"><span data-stu-id="c8cda-120">Name</span></span>                                                                                                  | <span data-ttu-id="c8cda-121">Significado</span><span class="sxs-lookup"><span data-stu-id="c8cda-121">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c8cda-122"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c8cda-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="c8cda-123">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="c8cda-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c8cda-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="c8cda-124">Remarks</span></span>

<span data-ttu-id="c8cda-125">A função **glRotatef** computa uma matriz que executa uma rotação no sentido anti-horário de graus de *ângulo* sobre o vetor da origem por meio do ponto (*x*, *y*, *z*).</span><span class="sxs-lookup"><span data-stu-id="c8cda-125">The **glRotatef** function computes a matrix that performs a counterclockwise rotation of *angle* degrees about the vector from the origin through the point (*x*, *y*, *z*).</span></span>

<span data-ttu-id="c8cda-126">A matriz atual (consulte [**glMatrixMode**](glmatrixmode.md)) é multiplicada por essa matriz de rotação, com o produto que substitui a matriz atual.</span><span class="sxs-lookup"><span data-stu-id="c8cda-126">The current matrix (see [**glMatrixMode**](glmatrixmode.md)) is multiplied by this rotation matrix, with the product replacing the current matrix.</span></span> <span data-ttu-id="c8cda-127">Ou seja, se M for a matriz atual e o R for a matriz de conversão, M será substituído por M R.</span><span class="sxs-lookup"><span data-stu-id="c8cda-127">That is, if M is the current matrix and R is the translation matrix, then M is replaced with M   R.</span></span>

<span data-ttu-id="c8cda-128">Se o modo de matriz for uma \_ projeção GL MODELVIEW ou GL \_ , todos os objetos desenhados depois de **glRotatef** serão girados.</span><span class="sxs-lookup"><span data-stu-id="c8cda-128">If the matrix mode is either GL\_MODELVIEW or GL\_PROJECTION, all objects drawn after **glRotatef** is called are rotated.</span></span> <span data-ttu-id="c8cda-129">Use [**glPushMatrix**](glpushmatrix.md) e [**glPopMatrix**](glpopmatrix.md) para salvar e restaurar o sistema de coordenadas não girado.</span><span class="sxs-lookup"><span data-stu-id="c8cda-129">Use [**glPushMatrix**](glpushmatrix.md) and [**glPopMatrix**](glpopmatrix.md) to save and restore the unrotated coordinate system.</span></span>

<span data-ttu-id="c8cda-130">As funções a seguir recuperam informações relacionadas ao **glRotatef**:</span><span class="sxs-lookup"><span data-stu-id="c8cda-130">The following functions retrieve information related to **glRotatef**:</span></span>

<span data-ttu-id="c8cda-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ modo de renderização Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="c8cda-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_RENDER\_MODE</span></span>

<span data-ttu-id="c8cda-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ modo de matriz GL de argumento \_</span><span class="sxs-lookup"><span data-stu-id="c8cda-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="c8cda-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ MODELVIEW \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="c8cda-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="c8cda-134">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) \_ matriz de projeção GLGET com Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="c8cda-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="c8cda-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com matriz de \_ textura Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="c8cda-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="c8cda-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8cda-136">Requirements</span></span>



| <span data-ttu-id="c8cda-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8cda-137">Requirement</span></span> | <span data-ttu-id="c8cda-138">Valor</span><span class="sxs-lookup"><span data-stu-id="c8cda-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8cda-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c8cda-139">Minimum supported client</span></span><br/> | <span data-ttu-id="c8cda-140">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c8cda-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c8cda-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c8cda-141">Minimum supported server</span></span><br/> | <span data-ttu-id="c8cda-142">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c8cda-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c8cda-143">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c8cda-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8cda-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8cda-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c8cda-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c8cda-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="c8cda-146"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8cda-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c8cda-147">DLL</span><span class="sxs-lookup"><span data-stu-id="c8cda-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8cda-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8cda-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8cda-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="c8cda-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8cda-150">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="c8cda-150">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="c8cda-151">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="c8cda-151">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="c8cda-152">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="c8cda-152">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="c8cda-153">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="c8cda-153">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="c8cda-154">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="c8cda-154">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="c8cda-155">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="c8cda-155">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="c8cda-156">**glScale**</span><span class="sxs-lookup"><span data-stu-id="c8cda-156">**glScale**</span></span>](glscale.md)
</dt> <dt>

[<span data-ttu-id="c8cda-157">**glTranslate**</span><span class="sxs-lookup"><span data-stu-id="c8cda-157">**glTranslate**</span></span>](gltranslate.md)
</dt> </dl>

 

 





