---
title: função glLoadName (GL. h)
description: A função glLoadName carrega um nome na pilha de nomes.
ms.assetid: 8d7d582b-3743-401e-af71-28034e49f3c2
keywords:
- função glLoadName OpenGL
topic_type:
- apiref
api_name:
- glLoadName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb47a0389cda13523104ee429bca46838970e15a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086466"
---
# <a name="glloadname-function"></a><span data-ttu-id="1661d-104">função glLoadName</span><span class="sxs-lookup"><span data-stu-id="1661d-104">glLoadName function</span></span>

<span data-ttu-id="1661d-105">A função **glLoadName** carrega um nome na pilha de nomes.</span><span class="sxs-lookup"><span data-stu-id="1661d-105">The **glLoadName** function loads a name onto the name stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="1661d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1661d-106">Syntax</span></span>


```C++
void WINAPI glLoadName(
   GLuint name
);
```



## <a name="parameters"></a><span data-ttu-id="1661d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1661d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1661d-108">*name*</span><span class="sxs-lookup"><span data-stu-id="1661d-108">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="1661d-109">Um nome que substituirá o valor superior na pilha de nomes.</span><span class="sxs-lookup"><span data-stu-id="1661d-109">A name that will replace the top value on the name stack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1661d-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1661d-110">Return value</span></span>

<span data-ttu-id="1661d-111">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1661d-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1661d-112">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="1661d-112">Error codes</span></span>

<span data-ttu-id="1661d-113">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="1661d-113">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="1661d-114">Nome</span><span class="sxs-lookup"><span data-stu-id="1661d-114">Name</span></span>                                                                                                  | <span data-ttu-id="1661d-115">Significado</span><span class="sxs-lookup"><span data-stu-id="1661d-115">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1661d-116"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1661d-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="1661d-117">A função foi chamada enquanto a pilha de nomes estava vazia.</span><span class="sxs-lookup"><span data-stu-id="1661d-117">The function was called while the name stack was empty.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="1661d-118"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1661d-118"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="1661d-119">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="1661d-119">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1661d-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="1661d-120">Remarks</span></span>

<span data-ttu-id="1661d-121">A função **glLoadName** faz com que o *nome* substitua o valor na parte superior da pilha de nomes, que está inicialmente vazia.</span><span class="sxs-lookup"><span data-stu-id="1661d-121">The **glLoadName** function causes *name* to replace the value on the top of the name stack, which is initially empty.</span></span> <span data-ttu-id="1661d-122">A pilha de nomes é usada durante o modo de seleção para permitir que conjuntos de comandos de renderização sejam identificados exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="1661d-122">The name stack is used during selection mode to allow sets of rendering commands to be uniquely identified.</span></span> <span data-ttu-id="1661d-123">Ele consiste em um conjunto ordenado de inteiros não assinados.</span><span class="sxs-lookup"><span data-stu-id="1661d-123">It consists of an ordered set of unsigned integers.</span></span>

<span data-ttu-id="1661d-124">A pilha de nomes está sempre vazia enquanto o modo de renderização não é GL \_ Select.</span><span class="sxs-lookup"><span data-stu-id="1661d-124">The name stack is always empty while the render mode is not GL\_SELECT.</span></span> <span data-ttu-id="1661d-125">As chamadas para **glLoadName** enquanto o modo de renderização não é GL \_ Select são ignoradas.</span><span class="sxs-lookup"><span data-stu-id="1661d-125">Calls to **glLoadName** while the render mode is not GL\_SELECT are ignored.</span></span>

<span data-ttu-id="1661d-126">As funções a seguir recuperam informações relacionadas ao **glLoadName**:</span><span class="sxs-lookup"><span data-stu-id="1661d-126">The following functions retrieve information related to **glLoadName**:</span></span>

<span data-ttu-id="1661d-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento \_ GL \_ profundidade da pilha de nome \_</span><span class="sxs-lookup"><span data-stu-id="1661d-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NAME\_STACK\_DEPTH</span></span>

<span data-ttu-id="1661d-128">**glGet** com Argument GL \_ Max \_ name \_ pilha \_ Depth</span><span class="sxs-lookup"><span data-stu-id="1661d-128">**glGet** with argument GL\_MAX\_NAME\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="1661d-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1661d-129">Requirements</span></span>



| <span data-ttu-id="1661d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1661d-130">Requirement</span></span> | <span data-ttu-id="1661d-131">Valor</span><span class="sxs-lookup"><span data-stu-id="1661d-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1661d-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1661d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1661d-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1661d-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1661d-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1661d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1661d-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1661d-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1661d-136">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1661d-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="1661d-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="1661d-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1661d-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1661d-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="1661d-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1661d-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1661d-140">DLL</span><span class="sxs-lookup"><span data-stu-id="1661d-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1661d-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1661d-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1661d-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="1661d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1661d-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="1661d-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="1661d-144">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="1661d-144">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="1661d-145">**glInitNames**</span><span class="sxs-lookup"><span data-stu-id="1661d-145">**glInitNames**</span></span>](glinitnames.md)
</dt> <dt>

[<span data-ttu-id="1661d-146">**glPushName**</span><span class="sxs-lookup"><span data-stu-id="1661d-146">**glPushName**</span></span>](glpushname.md)
</dt> <dt>

[<span data-ttu-id="1661d-147">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="1661d-147">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="1661d-148">**glSelectBuffer**</span><span class="sxs-lookup"><span data-stu-id="1661d-148">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





