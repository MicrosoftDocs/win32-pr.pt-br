---
title: função glPushMatrix (GL. h)
description: As funções glPushMatrix e glPopMatrix enviam por push e pop a pilha de matriz atual. | função glPushMatrix (GL. h)
ms.assetid: 97d8e644-50bb-4130-b6b7-d87df4468e73
keywords:
- função glPushMatrix OpenGL
topic_type:
- apiref
api_name:
- glPushMatrix
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee62b03e221f44db829a7167d642a766af8e129c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930429"
---
# <a name="glpushmatrix-function"></a><span data-ttu-id="61b05-105">função glPushMatrix</span><span class="sxs-lookup"><span data-stu-id="61b05-105">glPushMatrix function</span></span>

<span data-ttu-id="61b05-106">As funções **glPushMatrix** e [**glPopMatrix**](glpopmatrix.md) enviam por push e pop a pilha de matriz atual.</span><span class="sxs-lookup"><span data-stu-id="61b05-106">The **glPushMatrix** and [**glPopMatrix**](glpopmatrix.md) functions push and pop the current matrix stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="61b05-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61b05-107">Syntax</span></span>


```C++
void WINAPI glPushMatrix(void);
```



## <a name="parameters"></a><span data-ttu-id="61b05-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="61b05-108">Parameters</span></span>

<span data-ttu-id="61b05-109">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="61b05-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="61b05-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="61b05-110">Return value</span></span>

<span data-ttu-id="61b05-111">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="61b05-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="61b05-112">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="61b05-112">Error codes</span></span>

<span data-ttu-id="61b05-113">É um erro enviar por push uma pilha de matriz completa ou exibir uma pilha de matriz que contém apenas uma única matriz.</span><span class="sxs-lookup"><span data-stu-id="61b05-113">It is an error to push a full matrix stack, or to pop a matrix stack that contains only a single matrix.</span></span> <span data-ttu-id="61b05-114">Em ambos os casos, o sinalizador de erro é definido e nenhuma outra alteração é feita no estado OpenGL.</span><span class="sxs-lookup"><span data-stu-id="61b05-114">In either case, the error flag is set and no other change is made to the OpenGL state.</span></span>

<span data-ttu-id="61b05-115">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="61b05-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="61b05-116">Nome</span><span class="sxs-lookup"><span data-stu-id="61b05-116">Name</span></span>                                                                                                  | <span data-ttu-id="61b05-117">Significado</span><span class="sxs-lookup"><span data-stu-id="61b05-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="61b05-118"><dt>**\_estouro de pilha GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="61b05-118"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="61b05-119">A função foi chamada enquanto a pilha de matriz atual estava cheia.</span><span class="sxs-lookup"><span data-stu-id="61b05-119">The function was called while the current matrix stack was full.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="61b05-120"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="61b05-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="61b05-121">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="61b05-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="61b05-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="61b05-122">Remarks</span></span>

<span data-ttu-id="61b05-123">Há uma pilha de matrizes para cada um dos modos de matriz.</span><span class="sxs-lookup"><span data-stu-id="61b05-123">There is a stack of matrices for each of the matrix modes.</span></span> <span data-ttu-id="61b05-124">No \_ modo MODELVIEW GL, a profundidade da pilha é de pelo menos 32.</span><span class="sxs-lookup"><span data-stu-id="61b05-124">In GL\_MODELVIEW mode, the stack depth is at least 32.</span></span> <span data-ttu-id="61b05-125">Nos outros dois modos, \_ a projeção GL e \_ a textura GL, a profundidade é pelo menos 2.</span><span class="sxs-lookup"><span data-stu-id="61b05-125">In the other two modes, GL\_PROJECTION and GL\_TEXTURE, the depth is at least 2.</span></span> <span data-ttu-id="61b05-126">A matriz atual em qualquer modo é a matriz na parte superior da pilha para esse modo.</span><span class="sxs-lookup"><span data-stu-id="61b05-126">The current matrix in any mode is the matrix on the top of the stack for that mode.</span></span>

<span data-ttu-id="61b05-127">A função **glPushMatrix** envia por push a pilha da matriz atual por uma, duplicando a matriz atual.</span><span class="sxs-lookup"><span data-stu-id="61b05-127">The **glPushMatrix** function pushes the current matrix stack down by one, duplicating the current matrix.</span></span> <span data-ttu-id="61b05-128">Ou seja, após uma chamada **glPushMatrix** , a matriz na parte superior da pilha é idêntica à seguinte.</span><span class="sxs-lookup"><span data-stu-id="61b05-128">That is, after a **glPushMatrix** call, the matrix on the top of the stack is identical to the one below it.</span></span> <span data-ttu-id="61b05-129">A função **glPopMatrix** exibe a pilha da matriz atual, substituindo a matriz atual pela que está abaixo dela na pilha.</span><span class="sxs-lookup"><span data-stu-id="61b05-129">The **glPopMatrix** function pops the current matrix stack, replacing the current matrix with the one below it on the stack.</span></span> <span data-ttu-id="61b05-130">Inicialmente, cada uma das pilhas contém uma matriz, uma matriz de identidade.</span><span class="sxs-lookup"><span data-stu-id="61b05-130">Initially, each of the stacks contains one matrix, an identity matrix.</span></span>

<span data-ttu-id="61b05-131">As funções a seguir recuperam informações relacionadas a **glPushMatrix** e **glPopMatrix**:</span><span class="sxs-lookup"><span data-stu-id="61b05-131">The following functions retrieve information related to **glPushMatrix** and **glPopMatrix**:</span></span>

<span data-ttu-id="61b05-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ modo de matriz GL de argumento \_</span><span class="sxs-lookup"><span data-stu-id="61b05-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="61b05-133">**glGet** com o argumento GL \_ MODELVIEW \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="61b05-133">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="61b05-134"> \_ matriz de projeção GLGET com Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="61b05-134">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="61b05-135">**glGet** com matriz de \_ textura Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="61b05-135">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

<span data-ttu-id="61b05-136">profundidade de pilha **glGet** com Argument GL \_ MODELVIEW \_ \_</span><span class="sxs-lookup"><span data-stu-id="61b05-136">**glGet** with argument GL\_MODELVIEW\_STACK\_DEPTH</span></span>

<span data-ttu-id="61b05-137"> profundidade da pilha de \_ projeção GLGET com Argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="61b05-137">**glGet** with argument GL\_PROJECTION\_STACK\_DEPTH</span></span>

<span data-ttu-id="61b05-138"> profundidade da pilha de textura glGet com Argument GL \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="61b05-138">**glGet** with argument GL\_TEXTURE\_STACK\_DEPTH</span></span>

<span data-ttu-id="61b05-139">**glGet** com o argumento GL \_ Max \_ MODELVIEW de \_ profundidade de pilha \_</span><span class="sxs-lookup"><span data-stu-id="61b05-139">**glGet** with argument GL\_MAX\_MODELVIEW\_STACK\_DEPTH</span></span>

<span data-ttu-id="61b05-140"> \_ profundidade máxima da pilha de \_ projeção glGet \_ com Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="61b05-140">**glGet** with argument GL\_MAX\_PROJECTION\_STACK\_DEPTH</span></span>

<span data-ttu-id="61b05-141"> \_ profundidade máxima da pilha de \_ textura \_ glGet com Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="61b05-141">**glGet** with argument GL\_MAX\_TEXTURE\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="61b05-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61b05-142">Requirements</span></span>



| <span data-ttu-id="61b05-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="61b05-143">Requirement</span></span> | <span data-ttu-id="61b05-144">Valor</span><span class="sxs-lookup"><span data-stu-id="61b05-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="61b05-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61b05-145">Minimum supported client</span></span><br/> | <span data-ttu-id="61b05-146">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="61b05-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="61b05-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61b05-147">Minimum supported server</span></span><br/> | <span data-ttu-id="61b05-148">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="61b05-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="61b05-149">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="61b05-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="61b05-150"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="61b05-150"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="61b05-151">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="61b05-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="61b05-152"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="61b05-152"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="61b05-153">DLL</span><span class="sxs-lookup"><span data-stu-id="61b05-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61b05-154"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61b05-154"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61b05-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="61b05-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61b05-156">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="61b05-156">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="61b05-157">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="61b05-157">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="61b05-158">**glFrustum**</span><span class="sxs-lookup"><span data-stu-id="61b05-158">**glFrustum**</span></span>](glfrustum.md)
</dt> <dt>

[<span data-ttu-id="61b05-159">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="61b05-159">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="61b05-160">**glLoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="61b05-160">**glLoadMatrix**</span></span>](glloadmatrix.md)
</dt> <dt>

[<span data-ttu-id="61b05-161">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="61b05-161">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="61b05-162">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="61b05-162">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="61b05-163">**glOrtho**</span><span class="sxs-lookup"><span data-stu-id="61b05-163">**glOrtho**</span></span>](glortho.md)
</dt> <dt>

[<span data-ttu-id="61b05-164">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="61b05-164">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="61b05-165">**glRotate**</span><span class="sxs-lookup"><span data-stu-id="61b05-165">**glRotate**</span></span>](glrotate.md)
</dt> <dt>

[<span data-ttu-id="61b05-166">**glScale**</span><span class="sxs-lookup"><span data-stu-id="61b05-166">**glScale**</span></span>](glscale.md)
</dt> <dt>

[<span data-ttu-id="61b05-167">**glTranslate**</span><span class="sxs-lookup"><span data-stu-id="61b05-167">**glTranslate**</span></span>](gltranslate.md)
</dt> <dt>

[<span data-ttu-id="61b05-168">**glViewport**</span><span class="sxs-lookup"><span data-stu-id="61b05-168">**glViewport**</span></span>](glviewport.md)
</dt> </dl>

 

 





