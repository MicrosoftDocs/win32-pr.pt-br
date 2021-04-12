---
title: função glPopClientAttrib (GL. h)
description: As funções glPushClientAttrib e glPopClientAttrib salvam e restauram grupos de variáveis de estado do cliente na pilha de atributos do cliente. | função glPopClientAttrib (GL. h)
ms.assetid: 030a3955-35bf-4862-9691-54b0c24514e8
keywords:
- função glPopClientAttrib OpenGL
topic_type:
- apiref
api_name:
- glPopClientAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e9f09e9c7292754a736594a9bf3d57a70063744
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298319"
---
# <a name="glpopclientattrib-function"></a><span data-ttu-id="95778-105">função glPopClientAttrib</span><span class="sxs-lookup"><span data-stu-id="95778-105">glPopClientAttrib function</span></span>

<span data-ttu-id="95778-106">As funções [**glPushClientAttrib**](glpushclientattrib.md) e **glPopClientAttrib** salvam e restauram grupos de variáveis de estado do cliente na pilha de atributos do cliente.</span><span class="sxs-lookup"><span data-stu-id="95778-106">The [**glPushClientAttrib**](glpushclientattrib.md) and **glPopClientAttrib** functions save and restore groups of client-state variables on the client-attribute stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="95778-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="95778-107">Syntax</span></span>


```C++
void WINAPI glPopClientAttrib(void);
```



## <a name="parameters"></a><span data-ttu-id="95778-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="95778-108">Parameters</span></span>

<span data-ttu-id="95778-109">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="95778-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="95778-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="95778-110">Return value</span></span>

<span data-ttu-id="95778-111">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="95778-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="95778-112">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="95778-112">Error codes</span></span>

<span data-ttu-id="95778-113">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="95778-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="95778-114">Nome</span><span class="sxs-lookup"><span data-stu-id="95778-114">Name</span></span>                                                                                               | <span data-ttu-id="95778-115">Significado</span><span class="sxs-lookup"><span data-stu-id="95778-115">Meaning</span></span>                                                                       |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="95778-116"><dt>**\_estouro de pilha GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="95778-116"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl> | <span data-ttu-id="95778-117">A função foi chamada enquanto a pilha de atributo de cliente estava cheia.</span><span class="sxs-lookup"><span data-stu-id="95778-117">The function was called while the client-attribute stack was full.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="95778-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="95778-118">Remarks</span></span>

<span data-ttu-id="95778-119">A função **glPushClientAttrib** usa seu parâmetro Mask para determinar quais grupos de variáveis de estado do cliente são salvos na pilha de atributos do cliente.</span><span class="sxs-lookup"><span data-stu-id="95778-119">The **glPushClientAttrib** function uses its mask parameter to determine which groups of client-state variables are saved on the client-attribute stack.</span></span> <span data-ttu-id="95778-120">Você pode usar o operador OR bit a bit para unir constantes simbólicas aceitas para definir bits e construir uma máscara.</span><span class="sxs-lookup"><span data-stu-id="95778-120">You can use the bitwise OR operator to join together accepted symbolic constants to set bits and construct a mask.</span></span>

<span data-ttu-id="95778-121">A função **glPopClientAttrib** restaura os valores das variáveis de estado do cliente salvas pela última vez com **glPushclientAttrib**.</span><span class="sxs-lookup"><span data-stu-id="95778-121">The **glPopClientAttrib** function restores the values of the client-state variables last saved with **glPushclientAttrib**.</span></span> <span data-ttu-id="95778-122">As variáveis de estado do cliente não salvas anteriormente permanecem inalteradas.</span><span class="sxs-lookup"><span data-stu-id="95778-122">Client-state variables not previously saved are left unchanged.</span></span> <span data-ttu-id="95778-123">Enviar atributos por push para uma pilha completa do atributo do cliente ou remover atributos de uma pilha vazia define um sinalizador de erro e nenhuma outra alteração é feita no estado OpenGL.</span><span class="sxs-lookup"><span data-stu-id="95778-123">Pushing attributes onto a full client-attribute stack or popping attributes off an empty stack sets an error flag and no other change is made to the OpenGL state.</span></span> <span data-ttu-id="95778-124">Por padrão, a pilha de atributos do cliente está vazia.</span><span class="sxs-lookup"><span data-stu-id="95778-124">By default the client attribute stack is empty.</span></span>

<span data-ttu-id="95778-125">Alguns valores de estado do cliente OpenGL não podem ser salvos na pilha de atributos do cliente.</span><span class="sxs-lookup"><span data-stu-id="95778-125">Some OpenGL client-state values cannot be saved on the client-attribute stack.</span></span> <span data-ttu-id="95778-126">Por exemplo, você não pode salvar os Estados SELECT ou feedback na pilha de atributos do cliente.</span><span class="sxs-lookup"><span data-stu-id="95778-126">For example, you cannot save the select or feedback states on the client-attribute stack.</span></span> <span data-ttu-id="95778-127">A profundidade da pilha de atributos de cliente é pelo menos 16.</span><span class="sxs-lookup"><span data-stu-id="95778-127">The depth of the client-attribute stack is at least 16.</span></span>

<span data-ttu-id="95778-128">As funções **glPushclientAttrib** e **glPopClientAttrib** não são compiladas em listas de exibição, mas são executadas imediatamente.</span><span class="sxs-lookup"><span data-stu-id="95778-128">The **glPushclientAttrib** and **glPopClientAttrib** functions are not compiled into display lists, but are executed immediately.</span></span>

<span data-ttu-id="95778-129">As funções **glPushClientAttrib** e **glPopClientAttrib** podem apenas enviar por push e pop-up modos de armazenamento de pixel e Estados de cliente de matriz de vértice.</span><span class="sxs-lookup"><span data-stu-id="95778-129">The **glPushClientAttrib** and **glPopClientAttrib** functions can only push and pop pixel storage modes and vertex array client states.</span></span> <span data-ttu-id="95778-130">Você deve usar [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md) para enviar e pop os Estados que são mantidos no servidor.</span><span class="sxs-lookup"><span data-stu-id="95778-130">You must use [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) to push and pop states that are kept on the server.</span></span>

> [!Note]  
> <span data-ttu-id="95778-131">As funções **glPushClientAttrib** e **glPopClientAttrib** só estão disponíveis no OpenGL versão 1,1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="95778-131">The **glPushClientAttrib** and **glPopClientAttrib** functions are only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="95778-132">As funções a seguir recuperam informações relacionadas a **glPushClientAttrib** e **glPopClientAttrib**:</span><span class="sxs-lookup"><span data-stu-id="95778-132">The following functions retrieve information related to **glPushClientAttrib** and **glPopClientAttrib**:</span></span>

<span data-ttu-id="95778-133">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) profundidade de pilha de \_ Atrib de cliente GLGET com Argument GL \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="95778-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CLIENT\_ATTRIB\_STACK\_DEPTH</span></span>

<span data-ttu-id="95778-134">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) \_ profundidade máxima de pilha de \_ \_ Atrib de \_ cliente \_ glGet com Argument GL</span><span class="sxs-lookup"><span data-stu-id="95778-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_CLIENT\_ATTRIB\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="95778-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95778-135">Requirements</span></span>



| <span data-ttu-id="95778-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="95778-136">Requirement</span></span> | <span data-ttu-id="95778-137">Valor</span><span class="sxs-lookup"><span data-stu-id="95778-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95778-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95778-138">Minimum supported client</span></span><br/> | <span data-ttu-id="95778-139">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="95778-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="95778-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95778-140">Minimum supported server</span></span><br/> | <span data-ttu-id="95778-141">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="95778-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="95778-142">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="95778-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="95778-143"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="95778-143"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="95778-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="95778-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="95778-145"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95778-145"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="95778-146">DLL</span><span class="sxs-lookup"><span data-stu-id="95778-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95778-147"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95778-147"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95778-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="95778-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95778-149">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="95778-149">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="95778-150">**glDisableClientState**</span><span class="sxs-lookup"><span data-stu-id="95778-150">**glDisableClientState**</span></span>](gldisableclientstate.md)
</dt> <dt>

[<span data-ttu-id="95778-151">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="95778-151">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="95778-152">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="95778-152">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="95778-153">**glGet**</span><span class="sxs-lookup"><span data-stu-id="95778-153">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="95778-154">**glGetError**</span><span class="sxs-lookup"><span data-stu-id="95778-154">**glGetError**</span></span>](glgeterror.md)
</dt> <dt>

[<span data-ttu-id="95778-155">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="95778-155">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="95778-156">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="95778-156">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="95778-157">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="95778-157">**glNewList**</span></span>](glnewlist.md)
</dt> <dt>

[<span data-ttu-id="95778-158">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="95778-158">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="95778-159">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="95778-159">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="95778-160">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="95778-160">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="95778-161">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="95778-161">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





