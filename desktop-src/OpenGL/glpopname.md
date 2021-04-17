---
title: função glPopName (GL. h)
description: As funções glPushName e glPopName enviam por push e pop a pilha de nomes. | função glPopName (GL. h)
ms.assetid: ee741188-b275-4839-a89d-4d988c547d07
keywords:
- função glPopName OpenGL
topic_type:
- apiref
api_name:
- glPopName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 830c4937b30cca64de3063b42ad16dd3adc87c89
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105760216"
---
# <a name="glpopname-function"></a><span data-ttu-id="50e42-105">função glPopName</span><span class="sxs-lookup"><span data-stu-id="50e42-105">glPopName function</span></span>

<span data-ttu-id="50e42-106">As funções [**glPushName**](glpushname.md) e **glPopName** enviam por push e pop a pilha de nomes.</span><span class="sxs-lookup"><span data-stu-id="50e42-106">The [**glPushName**](glpushname.md) and **glPopName** functions push and pop the name stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="50e42-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="50e42-107">Syntax</span></span>


```C++
void WINAPI glPopName(void);
```



## <a name="parameters"></a><span data-ttu-id="50e42-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50e42-108">Parameters</span></span>

<span data-ttu-id="50e42-109">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="50e42-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="50e42-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="50e42-110">Return value</span></span>

<span data-ttu-id="50e42-111">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="50e42-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="50e42-112">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="50e42-112">Error codes</span></span>

<span data-ttu-id="50e42-113">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="50e42-113">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="50e42-114">Nome</span><span class="sxs-lookup"><span data-stu-id="50e42-114">Name</span></span>                                                                                                  | <span data-ttu-id="50e42-115">Significado</span><span class="sxs-lookup"><span data-stu-id="50e42-115">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="50e42-116"><dt>**\_estouro negativo de pilha GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="50e42-116"><dt>**GL\_STACK\_UNDERFLOW**</dt></span></span> </dl>   | <span data-ttu-id="50e42-117">A função foi chamada enquanto a pilha de matriz atual continha apenas uma única matriz.</span><span class="sxs-lookup"><span data-stu-id="50e42-117">The function was called while the current matrix stack contained only a single matrix.</span></span><br/>                                     |
| <dl> <span data-ttu-id="50e42-118"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="50e42-118"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="50e42-119">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="50e42-119">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="50e42-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="50e42-120">Remarks</span></span>

<span data-ttu-id="50e42-121">A função [**glPushName**](glpushname.md) faz com que o nome seja enviado por push para a pilha de nomes, que inicialmente está vazia.</span><span class="sxs-lookup"><span data-stu-id="50e42-121">The [**glPushName**](glpushname.md) function causes name to be pushed onto the name stack, which is initially empty.</span></span> <span data-ttu-id="50e42-122">A função **glPopName** exibe um nome fora do topo da pilha.</span><span class="sxs-lookup"><span data-stu-id="50e42-122">The **glPopName** function pops one name off the top of the stack.</span></span> <span data-ttu-id="50e42-123">A pilha de nomes é usada durante o modo de seleção para permitir que conjuntos de comandos de renderização sejam identificados exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="50e42-123">The name stack is used during selection mode to allow sets of rendering commands to be uniquely identified.</span></span> <span data-ttu-id="50e42-124">Ele consiste em um conjunto ordenado de inteiros não assinados.</span><span class="sxs-lookup"><span data-stu-id="50e42-124">It consists of an ordered set of unsigned integers.</span></span>

<span data-ttu-id="50e42-125">A pilha de nomes está sempre vazia enquanto o modo de renderização não é GL \_ Select.</span><span class="sxs-lookup"><span data-stu-id="50e42-125">The name stack is always empty while the render mode is not GL\_SELECT.</span></span> <span data-ttu-id="50e42-126">Chamadas para [**glPushName**](glpushname.md) ou **glPopName** enquanto o modo render não é GL \_ Select são ignoradas.</span><span class="sxs-lookup"><span data-stu-id="50e42-126">Calls to [**glPushName**](glpushname.md) or **glPopName** while the render mode is not GL\_SELECT are ignored.</span></span>

<span data-ttu-id="50e42-127">As funções a seguir recuperam informações relacionadas a [**glPushName**](glpushname.md) e **glPopName**:</span><span class="sxs-lookup"><span data-stu-id="50e42-127">The following functions retrieve information related to [**glPushName**](glpushname.md) and **glPopName**:</span></span>

<span data-ttu-id="50e42-128">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento \_ GL \_ profundidade da pilha de nome \_</span><span class="sxs-lookup"><span data-stu-id="50e42-128">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NAME\_STACK\_DEPTH</span></span>

<span data-ttu-id="50e42-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com Argument GL \_ Max \_ name \_ pilha \_ Depth</span><span class="sxs-lookup"><span data-stu-id="50e42-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_NAME\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="50e42-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50e42-130">Requirements</span></span>



| <span data-ttu-id="50e42-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="50e42-131">Requirement</span></span> | <span data-ttu-id="50e42-132">Valor</span><span class="sxs-lookup"><span data-stu-id="50e42-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50e42-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50e42-133">Minimum supported client</span></span><br/> | <span data-ttu-id="50e42-134">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="50e42-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="50e42-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50e42-135">Minimum supported server</span></span><br/> | <span data-ttu-id="50e42-136">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="50e42-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="50e42-137">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="50e42-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="50e42-138"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="50e42-138"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="50e42-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="50e42-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="50e42-140"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50e42-140"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="50e42-141">DLL</span><span class="sxs-lookup"><span data-stu-id="50e42-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50e42-142"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50e42-142"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50e42-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="50e42-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50e42-144">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="50e42-144">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="50e42-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="50e42-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="50e42-146">**glInitNames**</span><span class="sxs-lookup"><span data-stu-id="50e42-146">**glInitNames**</span></span>](glinitnames.md)
</dt> <dt>

[<span data-ttu-id="50e42-147">**glLoadName**</span><span class="sxs-lookup"><span data-stu-id="50e42-147">**glLoadName**</span></span>](glloadname.md)
</dt> <dt>

[<span data-ttu-id="50e42-148">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="50e42-148">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="50e42-149">**glSelectBuffer**</span><span class="sxs-lookup"><span data-stu-id="50e42-149">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





