---
title: função glMultMatrixd (GL. h)
description: A função glMultMatrixd multiplica a matriz atual por uma matriz arbitrária. | função glMultMatrixd (GL. h)
ms.assetid: 1f6cf4e4-e7bd-470c-b1f4-b9ccc1fb756e
keywords:
- função glMultMatrixd OpenGL
topic_type:
- apiref
api_name:
- glMultMatrixd
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e24993fe5873be0af8713e3d127b86a7c593cd82
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298406"
---
# <a name="glmultmatrixd-function"></a><span data-ttu-id="443b8-105">função glMultMatrixd</span><span class="sxs-lookup"><span data-stu-id="443b8-105">glMultMatrixd function</span></span>

<span data-ttu-id="443b8-106">As funções **glMultMatrixd** e [**glMultMatrixf**](glmultmatrixf.md) multiplicam a matriz atual por uma matriz arbitrária.</span><span class="sxs-lookup"><span data-stu-id="443b8-106">The **glMultMatrixd** and [**glMultMatrixf**](glmultmatrixf.md) functions multiply the current matrix by an arbitrary matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="443b8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="443b8-107">Syntax</span></span>


```C++
void WINAPI glMultMatrixd(
   const GLdouble *m
);
```



## <a name="parameters"></a><span data-ttu-id="443b8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="443b8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="443b8-109">*m*</span><span class="sxs-lookup"><span data-stu-id="443b8-109">*m*</span></span> 
</dt> <dd>

<span data-ttu-id="443b8-110">Um ponteiro para uma matriz 4x4 armazenada na ordem principal da coluna como 16 valores consecutivos.</span><span class="sxs-lookup"><span data-stu-id="443b8-110">A pointer to a 4x4 matrix stored in column-major order as 16 consecutive values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="443b8-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="443b8-111">Return value</span></span>

<span data-ttu-id="443b8-112">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="443b8-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="443b8-113">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="443b8-113">Error codes</span></span>

<span data-ttu-id="443b8-114">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="443b8-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="443b8-115">Nome</span><span class="sxs-lookup"><span data-stu-id="443b8-115">Name</span></span>                                                                                                  | <span data-ttu-id="443b8-116">Significado</span><span class="sxs-lookup"><span data-stu-id="443b8-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="443b8-117"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="443b8-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="443b8-118">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="443b8-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="443b8-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="443b8-119">Remarks</span></span>

<span data-ttu-id="443b8-120">A função **glMultMatrix** multiplica a matriz atual por aquela especificada em *m*.</span><span class="sxs-lookup"><span data-stu-id="443b8-120">The **glMultMatrix** function multiplies the current matrix by the one specified in *m*.</span></span> <span data-ttu-id="443b8-121">Ou seja, se M for a matriz atual e T for a matriz passada para **glMultMatrix**, M será substituído por m T.</span><span class="sxs-lookup"><span data-stu-id="443b8-121">That is, if M is the current matrix and T is the matrix passed to **glMultMatrix**, then M is replaced with M   T.</span></span>

<span data-ttu-id="443b8-122">A matriz atual é a matriz de projeção, a matriz modelview ou a matriz de textura, determinada pelo modo de matriz atual (consulte [**glMatrixMode**](glmatrixmode.md)).</span><span class="sxs-lookup"><span data-stu-id="443b8-122">The current matrix is the projection matrix, modelview matrix, or texture matrix, determined by the current matrix mode (see [**glMatrixMode**](glmatrixmode.md)).</span></span>

<span data-ttu-id="443b8-123">O parâmetro *m* aponta para uma matriz 4x4 de valores de ponto flutuante de precisão simples ou de precisão dupla armazenados em ordem de coluna principal.</span><span class="sxs-lookup"><span data-stu-id="443b8-123">The *m* parameter points to a 4x4 matrix of single-precision or double-precision floating-point values stored in column-major order.</span></span> <span data-ttu-id="443b8-124">Ou seja, a matriz é armazenada conforme mostrado na imagem a seguir.</span><span class="sxs-lookup"><span data-stu-id="443b8-124">That is, the matrix is stored as shown in the following image.</span></span>

![! [Diagrama mostrando a matriz 4x4 à qual o parâmetro m aponta.]](images/multi01.png)

<span data-ttu-id="443b8-126">As funções a seguir recuperam informações relacionadas ao **glMultMatrix**:</span><span class="sxs-lookup"><span data-stu-id="443b8-126">The following functions retrieve information related to **glMultMatrix**:</span></span>

<span data-ttu-id="443b8-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ modo de matriz GL de argumento \_</span><span class="sxs-lookup"><span data-stu-id="443b8-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="443b8-128">**glGet** com o argumento GL \_ MODELVIEW \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="443b8-128">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="443b8-129"> \_ matriz de projeção GLGET com Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="443b8-129">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="443b8-130">**glGet** com matriz de \_ textura Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="443b8-130">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="443b8-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="443b8-131">Requirements</span></span>



| <span data-ttu-id="443b8-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="443b8-132">Requirement</span></span> | <span data-ttu-id="443b8-133">Valor</span><span class="sxs-lookup"><span data-stu-id="443b8-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="443b8-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="443b8-134">Minimum supported client</span></span><br/> | <span data-ttu-id="443b8-135">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="443b8-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="443b8-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="443b8-136">Minimum supported server</span></span><br/> | <span data-ttu-id="443b8-137">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="443b8-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="443b8-138">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="443b8-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="443b8-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="443b8-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="443b8-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="443b8-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="443b8-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="443b8-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="443b8-142">DLL</span><span class="sxs-lookup"><span data-stu-id="443b8-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="443b8-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="443b8-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="443b8-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="443b8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="443b8-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="443b8-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="443b8-146">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="443b8-146">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="443b8-147">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="443b8-147">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="443b8-148">**glLoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="443b8-148">**glLoadMatrix**</span></span>](glloadmatrix.md)
</dt> <dt>

[<span data-ttu-id="443b8-149">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="443b8-149">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="443b8-150">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="443b8-150">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





