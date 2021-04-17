---
title: função glLoadMatrixd (GL. h)
description: A função glLoadMatrixd substitui a matriz atual por uma matriz arbitrária. | função glLoadMatrixd (GL. h)
ms.assetid: 66c499f7-3f55-4de2-b67b-5b775b5854e0
keywords:
- função glLoadMatrixd OpenGL
topic_type:
- apiref
api_name:
- glLoadMatrixd
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4715da159dff60024adb3c7331cbf03c7c3759ce
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105760039"
---
# <a name="glloadmatrixd-function"></a><span data-ttu-id="e4f28-105">função glLoadMatrixd</span><span class="sxs-lookup"><span data-stu-id="e4f28-105">glLoadMatrixd function</span></span>

<span data-ttu-id="e4f28-106">As funções **glLoadMatrixd** e [**glLoadMatrixf**](glloadmatrixf.md) substituem a matriz atual por uma matriz arbitrária.</span><span class="sxs-lookup"><span data-stu-id="e4f28-106">The **glLoadMatrixd** and [**glLoadMatrixf**](glloadmatrixf.md) functions replace the current matrix with an arbitrary matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4f28-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4f28-107">Syntax</span></span>


```C++
void WINAPI glLoadMatrixd(
   const GLdouble *m
);
```



## <a name="parameters"></a><span data-ttu-id="e4f28-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4f28-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4f28-109">*m*</span><span class="sxs-lookup"><span data-stu-id="e4f28-109">*m*</span></span> 
</dt> <dd>

<span data-ttu-id="e4f28-110">Um ponteiro para uma matriz 4x4 armazenada na ordem principal da coluna como 16 valores consecutivos.</span><span class="sxs-lookup"><span data-stu-id="e4f28-110">A pointer to a 4x4 matrix stored in column-major order as 16 consecutive values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4f28-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e4f28-111">Return value</span></span>

<span data-ttu-id="e4f28-112">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e4f28-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e4f28-113">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="e4f28-113">Error codes</span></span>

<span data-ttu-id="e4f28-114">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="e4f28-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e4f28-115">Nome</span><span class="sxs-lookup"><span data-stu-id="e4f28-115">Name</span></span>                                                                                                  | <span data-ttu-id="e4f28-116">Significado</span><span class="sxs-lookup"><span data-stu-id="e4f28-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e4f28-117"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e4f28-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="e4f28-118">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="e4f28-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e4f28-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4f28-119">Remarks</span></span>

<span data-ttu-id="e4f28-120">A função **glLoadMatrix** substitui a matriz atual por aquela especificada em *m*.</span><span class="sxs-lookup"><span data-stu-id="e4f28-120">The **glLoadMatrix** function replaces the current matrix with the one specified in *m*.</span></span> <span data-ttu-id="e4f28-121">A matriz atual é a matriz de projeção, a matriz modelview ou a matriz de textura, determinada pelo modo de matriz atual (consulte [**glMatrixMode**](glmatrixmode.md)).</span><span class="sxs-lookup"><span data-stu-id="e4f28-121">The current matrix is the projection matrix, modelview matrix, or texture matrix, determined by the current matrix mode (see [**glMatrixMode**](glmatrixmode.md)).</span></span>

<span data-ttu-id="e4f28-122">O parâmetro *m* aponta para uma matriz 4x4 de valores de ponto flutuante de precisão simples ou de precisão dupla armazenados em ordem de coluna principal.</span><span class="sxs-lookup"><span data-stu-id="e4f28-122">The *m* parameter points to a 4x4 matrix of single-precision or double-precision floating-point values stored in column-major order.</span></span> <span data-ttu-id="e4f28-123">Ou seja, a matriz é armazenada conforme mostrado na imagem a seguir.</span><span class="sxs-lookup"><span data-stu-id="e4f28-123">That is, the matrix is stored as shown in the following image.</span></span>

![Diagrama que mostra a matriz 4x4 à qual o parâmetro m aponta.](images/load02.png)

<span data-ttu-id="e4f28-125">As funções a seguir recuperam informações relacionadas ao **glLoadMatrix**:</span><span class="sxs-lookup"><span data-stu-id="e4f28-125">The following functions retrieve information related to **glLoadMatrix**:</span></span>

<span data-ttu-id="e4f28-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ modo de matriz GL de argumento \_</span><span class="sxs-lookup"><span data-stu-id="e4f28-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="e4f28-127">**glGet** com o argumento GL \_ MODELVIEW \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="e4f28-127">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="e4f28-128"> \_ matriz de projeção GLGET com Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="e4f28-128">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="e4f28-129">**glGet** com matriz de \_ textura Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="e4f28-129">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="e4f28-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4f28-130">Requirements</span></span>



| <span data-ttu-id="e4f28-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4f28-131">Requirement</span></span> | <span data-ttu-id="e4f28-132">Valor</span><span class="sxs-lookup"><span data-stu-id="e4f28-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4f28-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4f28-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e4f28-134">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e4f28-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e4f28-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4f28-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e4f28-136">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e4f28-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e4f28-137">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e4f28-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4f28-138"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4f28-138"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e4f28-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e4f28-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="e4f28-140"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4f28-140"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e4f28-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e4f28-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4f28-142"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4f28-142"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4f28-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4f28-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4f28-144">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e4f28-144">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e4f28-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="e4f28-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e4f28-146">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="e4f28-146">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="e4f28-147">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="e4f28-147">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="e4f28-148">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="e4f28-148">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="e4f28-149">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="e4f28-149">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





