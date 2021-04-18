---
title: função glPopMatrix (GL. h)
description: As funções glPushMatrix e glPopMatrix enviam por push e pop a pilha de matriz atual. | função glPopMatrix (GL. h)
ms.assetid: 7b4fc26e-36c8-4252-aba7-2e8ec6b34f91
keywords:
- função glPopMatrix OpenGL
topic_type:
- apiref
api_name:
- glPopMatrix
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41424a8af3ca6599edc7a66f9e498632640022c5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105771833"
---
# <a name="glpopmatrix-function"></a><span data-ttu-id="ba378-105">função glPopMatrix</span><span class="sxs-lookup"><span data-stu-id="ba378-105">glPopMatrix function</span></span>

<span data-ttu-id="ba378-106">As funções [**glPushMatrix**](glpushmatrix.md) e **glPopMatrix** enviam por push e pop a pilha de matriz atual.</span><span class="sxs-lookup"><span data-stu-id="ba378-106">The [**glPushMatrix**](glpushmatrix.md) and **glPopMatrix** functions push and pop the current matrix stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba378-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba378-107">Syntax</span></span>


```C++
void WINAPI glPopMatrix(void);
```



## <a name="parameters"></a><span data-ttu-id="ba378-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba378-108">Parameters</span></span>

<span data-ttu-id="ba378-109">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ba378-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ba378-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ba378-110">Return value</span></span>

<span data-ttu-id="ba378-111">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ba378-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ba378-112">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="ba378-112">Error codes</span></span>

<span data-ttu-id="ba378-113">É um erro enviar por push uma pilha de matriz completa ou exibir uma pilha de matriz que contém apenas uma única matriz.</span><span class="sxs-lookup"><span data-stu-id="ba378-113">It is an error to push a full matrix stack, or to pop a matrix stack that contains only a single matrix.</span></span> <span data-ttu-id="ba378-114">Em ambos os casos, o sinalizador de erro é definido e nenhuma outra alteração é feita no estado OpenGL.</span><span class="sxs-lookup"><span data-stu-id="ba378-114">In either case, the error flag is set and no other change is made to the OpenGL state.</span></span>

<span data-ttu-id="ba378-115">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="ba378-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="ba378-116">Nome</span><span class="sxs-lookup"><span data-stu-id="ba378-116">Name</span></span>                                                                                                  | <span data-ttu-id="ba378-117">Significado</span><span class="sxs-lookup"><span data-stu-id="ba378-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ba378-118"><dt>**\_estouro negativo de pilha GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ba378-118"><dt>**GL\_STACK\_UNDERFLOW**</dt></span></span> </dl>   | <span data-ttu-id="ba378-119">A função foi chamada enquanto a pilha de matriz atual continha apenas uma única matriz.</span><span class="sxs-lookup"><span data-stu-id="ba378-119">The function was called while the current matrix stack contained only a single matrix.</span></span><br/>                                     |
| <dl> <span data-ttu-id="ba378-120"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ba378-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="ba378-121">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="ba378-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ba378-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba378-122">Remarks</span></span>

<span data-ttu-id="ba378-123">Há uma pilha de matrizes para cada um dos modos de matriz.</span><span class="sxs-lookup"><span data-stu-id="ba378-123">There is a stack of matrices for each of the matrix modes.</span></span> <span data-ttu-id="ba378-124">No \_ modo MODELVIEW GL, a profundidade da pilha é de pelo menos 32.</span><span class="sxs-lookup"><span data-stu-id="ba378-124">In GL\_MODELVIEW mode, the stack depth is at least 32.</span></span> <span data-ttu-id="ba378-125">Nos outros dois modos, \_ a projeção GL e \_ a textura GL, a profundidade é pelo menos 2.</span><span class="sxs-lookup"><span data-stu-id="ba378-125">In the other two modes, GL\_PROJECTION and GL\_TEXTURE, the depth is at least 2.</span></span> <span data-ttu-id="ba378-126">A matriz atual em qualquer modo é a matriz na parte superior da pilha para esse modo.</span><span class="sxs-lookup"><span data-stu-id="ba378-126">The current matrix in any mode is the matrix on the top of the stack for that mode.</span></span>

<span data-ttu-id="ba378-127">A função [**glPushMatrix**](glpushmatrix.md) envia por push a pilha da matriz atual por uma, duplicando a matriz atual.</span><span class="sxs-lookup"><span data-stu-id="ba378-127">The [**glPushMatrix**](glpushmatrix.md) function pushes the current matrix stack down by one, duplicating the current matrix.</span></span> <span data-ttu-id="ba378-128">Ou seja, após uma chamada **glPushMatrix** , a matriz na parte superior da pilha é idêntica à seguinte.</span><span class="sxs-lookup"><span data-stu-id="ba378-128">That is, after a **glPushMatrix** call, the matrix on the top of the stack is identical to the one below it.</span></span> <span data-ttu-id="ba378-129">A função **glPopMatrix** exibe a pilha da matriz atual, substituindo a matriz atual pela que está abaixo dela na pilha.</span><span class="sxs-lookup"><span data-stu-id="ba378-129">The **glPopMatrix** function pops the current matrix stack, replacing the current matrix with the one below it on the stack.</span></span> <span data-ttu-id="ba378-130">Inicialmente, cada uma das pilhas contém uma matriz, uma matriz de identidade.</span><span class="sxs-lookup"><span data-stu-id="ba378-130">Initially, each of the stacks contains one matrix, an identity matrix.</span></span>

<span data-ttu-id="ba378-131">As funções a seguir recuperam informações relacionadas a [**glPushMatrix**](glpushmatrix.md) e **glPopMatrix**:</span><span class="sxs-lookup"><span data-stu-id="ba378-131">The following functions retrieve information related to [**glPushMatrix**](glpushmatrix.md) and **glPopMatrix**:</span></span>

<span data-ttu-id="ba378-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ modo de matriz GL de argumento \_</span><span class="sxs-lookup"><span data-stu-id="ba378-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="ba378-133">**glGet** com o argumento GL \_ MODELVIEW \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="ba378-133">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="ba378-134"> \_ matriz de projeção GLGET com Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="ba378-134">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="ba378-135">**glGet** com matriz de \_ textura Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="ba378-135">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

<span data-ttu-id="ba378-136">profundidade de pilha **glGet** com Argument GL \_ MODELVIEW \_ \_</span><span class="sxs-lookup"><span data-stu-id="ba378-136">**glGet** with argument GL\_MODELVIEW\_STACK\_DEPTH</span></span>

<span data-ttu-id="ba378-137"> profundidade da pilha de \_ projeção GLGET com Argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="ba378-137">**glGet** with argument GL\_PROJECTION\_STACK\_DEPTH</span></span>

<span data-ttu-id="ba378-138"> profundidade da pilha de textura glGet com Argument GL \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="ba378-138">**glGet** with argument GL\_TEXTURE\_STACK\_DEPTH</span></span>

<span data-ttu-id="ba378-139">**glGet** com o argumento GL \_ Max \_ MODELVIEW de \_ profundidade de pilha \_</span><span class="sxs-lookup"><span data-stu-id="ba378-139">**glGet** with argument GL\_MAX\_MODELVIEW\_STACK\_DEPTH</span></span>

<span data-ttu-id="ba378-140"> \_ profundidade máxima da pilha de \_ projeção glGet \_ com Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="ba378-140">**glGet** with argument GL\_MAX\_PROJECTION\_STACK\_DEPTH</span></span>

<span data-ttu-id="ba378-141"> \_ profundidade máxima da pilha de \_ textura \_ glGet com Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="ba378-141">**glGet** with argument GL\_MAX\_TEXTURE\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="ba378-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba378-142">Requirements</span></span>



| <span data-ttu-id="ba378-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba378-143">Requirement</span></span> | <span data-ttu-id="ba378-144">Valor</span><span class="sxs-lookup"><span data-stu-id="ba378-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba378-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba378-145">Minimum supported client</span></span><br/> | <span data-ttu-id="ba378-146">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ba378-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ba378-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba378-147">Minimum supported server</span></span><br/> | <span data-ttu-id="ba378-148">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ba378-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ba378-149">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ba378-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba378-150"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba378-150"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ba378-151">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ba378-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="ba378-152"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba378-152"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ba378-153">DLL</span><span class="sxs-lookup"><span data-stu-id="ba378-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba378-154"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba378-154"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba378-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba378-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba378-156">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="ba378-156">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="ba378-157">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="ba378-157">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="ba378-158">**glFrustum**</span><span class="sxs-lookup"><span data-stu-id="ba378-158">**glFrustum**</span></span>](glfrustum.md)
</dt> <dt>

[<span data-ttu-id="ba378-159">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="ba378-159">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="ba378-160">**glLoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="ba378-160">**glLoadMatrix**</span></span>](glloadmatrix.md)
</dt> <dt>

[<span data-ttu-id="ba378-161">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="ba378-161">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="ba378-162">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="ba378-162">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="ba378-163">**glOrtho**</span><span class="sxs-lookup"><span data-stu-id="ba378-163">**glOrtho**</span></span>](glortho.md)
</dt> <dt>

[<span data-ttu-id="ba378-164">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="ba378-164">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="ba378-165">**glRotate**</span><span class="sxs-lookup"><span data-stu-id="ba378-165">**glRotate**</span></span>](glrotate.md)
</dt> <dt>

[<span data-ttu-id="ba378-166">**glScale**</span><span class="sxs-lookup"><span data-stu-id="ba378-166">**glScale**</span></span>](glscale.md)
</dt> <dt>

[<span data-ttu-id="ba378-167">**glTranslate**</span><span class="sxs-lookup"><span data-stu-id="ba378-167">**glTranslate**</span></span>](gltranslate.md)
</dt> <dt>

[<span data-ttu-id="ba378-168">**glViewport**</span><span class="sxs-lookup"><span data-stu-id="ba378-168">**glViewport**</span></span>](glviewport.md)
</dt> </dl>

 

 





