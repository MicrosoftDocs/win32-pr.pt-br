---
title: função glInitNames (GL. h)
description: A função glInitNames Inicializa a pilha de nomes.
ms.assetid: 26c134f5-c17c-4637-93b6-5293f316dd6c
keywords:
- função glInitNames OpenGL
topic_type:
- apiref
api_name:
- glInitNames
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9ebdb9d19f6c88340fd53162febe694e3566408
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085195"
---
# <a name="glinitnames-function"></a><span data-ttu-id="e0b2f-104">função glInitNames</span><span class="sxs-lookup"><span data-stu-id="e0b2f-104">glInitNames function</span></span>

<span data-ttu-id="e0b2f-105">A função **glInitNames** Inicializa a pilha de nomes.</span><span class="sxs-lookup"><span data-stu-id="e0b2f-105">The **glInitNames** function initializes the name stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0b2f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0b2f-106">Syntax</span></span>


```C++
void WINAPI glInitNames(void);
```



## <a name="parameters"></a><span data-ttu-id="e0b2f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0b2f-107">Parameters</span></span>

<span data-ttu-id="e0b2f-108">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e0b2f-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e0b2f-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e0b2f-109">Return value</span></span>

<span data-ttu-id="e0b2f-110">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e0b2f-110">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e0b2f-111">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="e0b2f-111">Error codes</span></span>

<span data-ttu-id="e0b2f-112">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="e0b2f-112">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e0b2f-113">Nome</span><span class="sxs-lookup"><span data-stu-id="e0b2f-113">Name</span></span>                                                                                                  | <span data-ttu-id="e0b2f-114">Significado</span><span class="sxs-lookup"><span data-stu-id="e0b2f-114">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e0b2f-115"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e0b2f-115"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="e0b2f-116">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="e0b2f-116">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e0b2f-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0b2f-117">Remarks</span></span>

<span data-ttu-id="e0b2f-118">A função **glInitNames** faz com que a pilha de nomes seja inicializada para seu estado vazio padrão.</span><span class="sxs-lookup"><span data-stu-id="e0b2f-118">The **glInitNames** function causes the name stack to be initialized to its default empty state.</span></span> <span data-ttu-id="e0b2f-119">A pilha de nomes é usada durante o modo de seleção para permitir que conjuntos de comandos de renderização sejam identificados exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="e0b2f-119">The name stack is used during selection mode to allow sets of rendering commands to be uniquely identified.</span></span> <span data-ttu-id="e0b2f-120">Ele consiste em um conjunto ordenado de inteiros não assinados.</span><span class="sxs-lookup"><span data-stu-id="e0b2f-120">It consists of an ordered set of unsigned integers.</span></span>

<span data-ttu-id="e0b2f-121">A pilha de nomes está sempre vazia enquanto o modo de renderização não é GL \_ Select.</span><span class="sxs-lookup"><span data-stu-id="e0b2f-121">The name stack is always empty while the render mode is not GL\_SELECT.</span></span> <span data-ttu-id="e0b2f-122">As chamadas para **glInitNames** enquanto o modo de renderização não é GL \_ Select são ignoradas.</span><span class="sxs-lookup"><span data-stu-id="e0b2f-122">Calls to **glInitNames** while the render mode is not GL\_SELECT are ignored.</span></span>

<span data-ttu-id="e0b2f-123">As funções a seguir recuperam informações relacionadas ao **glInitNames**:</span><span class="sxs-lookup"><span data-stu-id="e0b2f-123">The following functions retrieve information related to **glInitNames**:</span></span>

<span data-ttu-id="e0b2f-124">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento \_ GL \_ profundidade da pilha de nome \_</span><span class="sxs-lookup"><span data-stu-id="e0b2f-124">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NAME\_STACK\_DEPTH</span></span>

<span data-ttu-id="e0b2f-125">**glGet** com Argument GL \_ Max \_ name \_ pilha \_ Depth</span><span class="sxs-lookup"><span data-stu-id="e0b2f-125">**glGet** with argument GL\_MAX\_NAME\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="e0b2f-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0b2f-126">Requirements</span></span>



| <span data-ttu-id="e0b2f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0b2f-127">Requirement</span></span> | <span data-ttu-id="e0b2f-128">Valor</span><span class="sxs-lookup"><span data-stu-id="e0b2f-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0b2f-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0b2f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e0b2f-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e0b2f-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e0b2f-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0b2f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e0b2f-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e0b2f-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e0b2f-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e0b2f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0b2f-134"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0b2f-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e0b2f-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e0b2f-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="e0b2f-136"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0b2f-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e0b2f-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e0b2f-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0b2f-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0b2f-138"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0b2f-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0b2f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0b2f-140">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e0b2f-140">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e0b2f-141">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="e0b2f-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e0b2f-142">**glLoadName**</span><span class="sxs-lookup"><span data-stu-id="e0b2f-142">**glLoadName**</span></span>](glloadname.md)
</dt> <dt>

[<span data-ttu-id="e0b2f-143">**glPushName**</span><span class="sxs-lookup"><span data-stu-id="e0b2f-143">**glPushName**</span></span>](glpushname.md)
</dt> <dt>

[<span data-ttu-id="e0b2f-144">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="e0b2f-144">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="e0b2f-145">**glSelectBuffer**</span><span class="sxs-lookup"><span data-stu-id="e0b2f-145">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





