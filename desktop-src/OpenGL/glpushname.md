---
title: função glPushName (GL. h)
description: As funções glPushName e glPopName enviam por push e pop a pilha de nomes. | função glPushName (GL. h)
ms.assetid: e4319018-42c0-4567-b67f-31dbdbee9b13
keywords:
- função glPushName OpenGL
topic_type:
- apiref
api_name:
- glPushName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ff783a108f5cb1ac34141c6c57f47b16e23531a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105782960"
---
# <a name="glpushname-function"></a><span data-ttu-id="b81f4-105">função glPushName</span><span class="sxs-lookup"><span data-stu-id="b81f4-105">glPushName function</span></span>

<span data-ttu-id="b81f4-106">As funções **glPushName** e [**glPopName**](glpopname.md) enviam por push e pop a pilha de nomes.</span><span class="sxs-lookup"><span data-stu-id="b81f4-106">The **glPushName** and [**glPopName**](glpopname.md) functions push and pop the name stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="b81f4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b81f4-107">Syntax</span></span>


```C++
void WINAPI glPushName(
   GLuint name
);
```



## <a name="parameters"></a><span data-ttu-id="b81f4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b81f4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b81f4-109">*name*</span><span class="sxs-lookup"><span data-stu-id="b81f4-109">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="b81f4-110">Um nome que será enviado para a pilha de nomes.</span><span class="sxs-lookup"><span data-stu-id="b81f4-110">A name that will be pushed onto the name stack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b81f4-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b81f4-111">Return value</span></span>

<span data-ttu-id="b81f4-112">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b81f4-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b81f4-113">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="b81f4-113">Error codes</span></span>

<span data-ttu-id="b81f4-114">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="b81f4-114">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b81f4-115">Name</span><span class="sxs-lookup"><span data-stu-id="b81f4-115">Name</span></span>                                                                                                  | <span data-ttu-id="b81f4-116">Significado</span><span class="sxs-lookup"><span data-stu-id="b81f4-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b81f4-117"><dt>**\_estouro de pilha GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b81f4-117"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="b81f4-118">A função foi chamada enquanto a pilha de matriz atual estava cheia.</span><span class="sxs-lookup"><span data-stu-id="b81f4-118">The function was called while the current matrix stack was full.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="b81f4-119"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b81f4-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b81f4-120">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="b81f4-120">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b81f4-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="b81f4-121">Remarks</span></span>

<span data-ttu-id="b81f4-122">A função **glPushName** faz com que o nome seja enviado por push para a pilha de nomes, que inicialmente está vazia.</span><span class="sxs-lookup"><span data-stu-id="b81f4-122">The **glPushName** function causes name to be pushed onto the name stack, which is initially empty.</span></span> <span data-ttu-id="b81f4-123">A função [**glPopName**](glpopname.md) exibe um nome fora do topo da pilha.</span><span class="sxs-lookup"><span data-stu-id="b81f4-123">The [**glPopName**](glpopname.md) function pops one name off the top of the stack.</span></span> <span data-ttu-id="b81f4-124">A pilha de nomes é usada durante o modo de seleção para permitir que conjuntos de comandos de renderização sejam identificados exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="b81f4-124">The name stack is used during selection mode to allow sets of rendering commands to be uniquely identified.</span></span> <span data-ttu-id="b81f4-125">Ele consiste em um conjunto ordenado de inteiros não assinados.</span><span class="sxs-lookup"><span data-stu-id="b81f4-125">It consists of an ordered set of unsigned integers.</span></span>

<span data-ttu-id="b81f4-126">A pilha de nomes está sempre vazia enquanto o modo de renderização não é GL \_ Select.</span><span class="sxs-lookup"><span data-stu-id="b81f4-126">The name stack is always empty while the render mode is not GL\_SELECT.</span></span> <span data-ttu-id="b81f4-127">Chamadas para **glPushName** ou [**glPopName**](glpopname.md) enquanto o modo render não é GL \_ Select são ignoradas.</span><span class="sxs-lookup"><span data-stu-id="b81f4-127">Calls to **glPushName** or [**glPopName**](glpopname.md) while the render mode is not GL\_SELECT are ignored.</span></span>

<span data-ttu-id="b81f4-128">As funções a seguir recuperam informações relacionadas a **glPushName** e [**glPopName**](glpopname.md):</span><span class="sxs-lookup"><span data-stu-id="b81f4-128">The following functions retrieve information related to **glPushName** and [**glPopName**](glpopname.md):</span></span>

<span data-ttu-id="b81f4-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento \_ GL \_ profundidade da pilha de nome \_</span><span class="sxs-lookup"><span data-stu-id="b81f4-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NAME\_STACK\_DEPTH</span></span>

<span data-ttu-id="b81f4-130">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com Argument GL \_ Max \_ name \_ pilha \_ Depth</span><span class="sxs-lookup"><span data-stu-id="b81f4-130">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_NAME\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="b81f4-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b81f4-131">Requirements</span></span>



| <span data-ttu-id="b81f4-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="b81f4-132">Requirement</span></span> | <span data-ttu-id="b81f4-133">Valor</span><span class="sxs-lookup"><span data-stu-id="b81f4-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b81f4-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b81f4-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b81f4-135">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b81f4-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b81f4-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b81f4-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b81f4-137">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b81f4-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b81f4-138">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b81f4-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="b81f4-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b81f4-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b81f4-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b81f4-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="b81f4-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b81f4-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b81f4-142">DLL</span><span class="sxs-lookup"><span data-stu-id="b81f4-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b81f4-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b81f4-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b81f4-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="b81f4-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b81f4-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b81f4-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b81f4-146">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b81f4-146">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b81f4-147">**glInitNames**</span><span class="sxs-lookup"><span data-stu-id="b81f4-147">**glInitNames**</span></span>](glinitnames.md)
</dt> <dt>

[<span data-ttu-id="b81f4-148">**glLoadName**</span><span class="sxs-lookup"><span data-stu-id="b81f4-148">**glLoadName**</span></span>](glloadname.md)
</dt> <dt>

[<span data-ttu-id="b81f4-149">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="b81f4-149">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="b81f4-150">**glSelectBuffer**</span><span class="sxs-lookup"><span data-stu-id="b81f4-150">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





