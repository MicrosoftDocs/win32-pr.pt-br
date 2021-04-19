---
title: função glEndList (GL. h)
description: As funções glNewList e glEndList criam ou substituem uma lista de exibição. | função glEndList (GL. h)
ms.assetid: dd749932-7b3c-47e5-8d91-90d272a7dc41
keywords:
- função glEndList OpenGL
topic_type:
- apiref
api_name:
- glEndList
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59f8db8c2abea44d678268f804159b60fe695f96
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105780196"
---
# <a name="glendlist-function"></a><span data-ttu-id="07e83-105">função glEndList</span><span class="sxs-lookup"><span data-stu-id="07e83-105">glEndList function</span></span>

<span data-ttu-id="07e83-106">As funções [**glNewList**](glnewlist.md) e **glEndList** criam ou substituem uma lista de exibição.</span><span class="sxs-lookup"><span data-stu-id="07e83-106">The [**glNewList**](glnewlist.md) and **glEndList** functions create or replace a display list.</span></span>

## <a name="syntax"></a><span data-ttu-id="07e83-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07e83-107">Syntax</span></span>


```C++
void WINAPI glEndList(void);
```



## <a name="parameters"></a><span data-ttu-id="07e83-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="07e83-108">Parameters</span></span>

<span data-ttu-id="07e83-109">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="07e83-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="07e83-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="07e83-110">Return value</span></span>

<span data-ttu-id="07e83-111">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="07e83-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="07e83-112">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="07e83-112">Error codes</span></span>

<span data-ttu-id="07e83-113">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="07e83-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="07e83-114">Name</span><span class="sxs-lookup"><span data-stu-id="07e83-114">Name</span></span>                                                                                                  | <span data-ttu-id="07e83-115">Significado</span><span class="sxs-lookup"><span data-stu-id="07e83-115">Meaning</span></span>                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="07e83-116"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="07e83-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="07e83-117">**glEndList** foi chamado sem um **glNewList** anterior ou se **glNewList** foi chamado enquanto uma lista de exibição estava sendo definida.</span><span class="sxs-lookup"><span data-stu-id="07e83-117">**glEndList** was called without a preceding **glNewList**, or if **glnewlist** was called while a display list was being defined.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="07e83-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="07e83-118">Remarks</span></span>

<span data-ttu-id="07e83-119">As listas de exibição são grupos de comandos OpenGL que foram armazenados para execução subsequente.</span><span class="sxs-lookup"><span data-stu-id="07e83-119">Display lists are groups of OpenGL commands that have been stored for subsequent execution.</span></span> <span data-ttu-id="07e83-120">As listas de exibição são criadas com [**glNewList**](glnewlist.md).</span><span class="sxs-lookup"><span data-stu-id="07e83-120">The display lists are created with [**glNewList**](glnewlist.md).</span></span> <span data-ttu-id="07e83-121">Todos os comandos subsequentes são colocados na lista de exibição, na ordem emitida, até que **glEndList** seja chamado.</span><span class="sxs-lookup"><span data-stu-id="07e83-121">All subsequent commands are placed in the display list, in the order issued, until **glEndList** is called.</span></span>

<span data-ttu-id="07e83-122">A função [**glNewList**](glnewlist.md) tem dois parâmetros.</span><span class="sxs-lookup"><span data-stu-id="07e83-122">The [**glNewList**](glnewlist.md) function has two parameters.</span></span> <span data-ttu-id="07e83-123">O primeiro parâmetro, *lista*, é um inteiro positivo que se torna o nome exclusivo da lista de exibição.</span><span class="sxs-lookup"><span data-stu-id="07e83-123">The first parameter, *list*, is a positive integer that becomes the unique name for the display list.</span></span> <span data-ttu-id="07e83-124">Os nomes podem ser criados e reservados com [**glGenLists**](glgenlists.md) e testados para exclusividade com [**glIsList**](glislist.md).</span><span class="sxs-lookup"><span data-stu-id="07e83-124">Names can be created and reserved with [**glGenLists**](glgenlists.md) and tested for uniqueness with [**glIsList**](glislist.md).</span></span> <span data-ttu-id="07e83-125">O segundo parâmetro, *Mode*, é uma constante simbólica que pode assumir um dos dois valores anteriores.</span><span class="sxs-lookup"><span data-stu-id="07e83-125">The second parameter, *mode*, is a symbolic constant that can assume one of the two preceding values.</span></span>

<span data-ttu-id="07e83-126">Determinados comandos não são compilados na lista de exibição, mas são executados imediatamente, independentemente do modo da lista de exibição.</span><span class="sxs-lookup"><span data-stu-id="07e83-126">Certain commands are not compiled into the display list, but are executed immediately, regardless of the display list mode.</span></span> <span data-ttu-id="07e83-127">Esses comandos são [**glColorPointer**](glcolorpointer.md), [**glDeleteLists**](gldeletelists.md), [**glDisableClientState**](gldisableclientstate.md), [**glEdgeFlagPointer**](gledgeflagpointer.md), [**glEnableClientState**](glenableclientstate.md), [**glFeedbackBuffer**](glfeedbackbuffer.md), [**glFinish**](glfinish.md), [**glFlush**](glflush.md), [**glGenLists**](glgenlists.md), [**glIndexPointer**](glindexpointer.md), [**glInterleavedArrays**](glinterleavedarrays.md), [**glIsEnabled**](glisenabled.md), [**GlIsList**](glislist.md), [**glNormalPointer**](glnormalpointer.md), [**glPopClientAttrib**](glpopclientattrib.md), [**glPixelStore**](glpixelstore-functions.md), [**glPushClientAttrib**](glpushclientattrib.md), [**glReadPixels**](glreadpixels.md), [**glRenderMode**](glrendermode.md), [**glSelectBuffer**](glselectbuffer.md), [**glTexCoordPointer**](gltexcoordpointer.md), [**glVertexPointer**](glvertexpointer.md)e todas as rotinas de [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) .</span><span class="sxs-lookup"><span data-stu-id="07e83-127">These commands are [**glColorPointer**](glcolorpointer.md), [**glDeleteLists**](gldeletelists.md), [**glDisableClientState**](gldisableclientstate.md), [**glEdgeFlagPointer**](gledgeflagpointer.md), [**glEnableClientState**](glenableclientstate.md), [**glFeedbackBuffer**](glfeedbackbuffer.md), [**glFinish**](glfinish.md), [**glFlush**](glflush.md), [**glGenLists**](glgenlists.md), [**glIndexPointer**](glindexpointer.md), [**glInterleavedArrays**](glinterleavedarrays.md), [**glIsEnabled**](glisenabled.md), [**glIsList**](glislist.md), [**glNormalPointer**](glnormalpointer.md), [**glPopClientAttrib**](glpopclientattrib.md), [**glPixelStore**](glpixelstore-functions.md), [**glPushClientAttrib**](glpushclientattrib.md), [**glReadPixels**](glreadpixels.md), [**glRenderMode**](glrendermode.md), [**glSelectBuffer**](glselectbuffer.md), [**glTexCoordPointer**](gltexcoordpointer.md), [**glVertexPointer**](glvertexpointer.md), and all of the [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) routines.</span></span>

<span data-ttu-id="07e83-128">Da mesma forma, [**glTexImage2D**](glteximage2d.md) e [**glTexImage1D**](glteximage1d.md) são executados imediatamente e não são compilados na lista de exibição quando seu primeiro argumento \_ é GL de proxy \_ \_ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="07e83-128">Similarly, [**glTexImage2D**](glteximage2d.md) and [**glTexImage1D**](glteximage1d.md) are executed immediately and not compiled into the display list when their first argument is GL\_PROXY\_TEXTURE\_2D or GL\_PROXY\_TEXTURE\_1D, respectively.</span></span>

<span data-ttu-id="07e83-129">Quando a função **glEndList** é encontrada, a definição da lista de exibição é concluída pela Associação da lista com a *lista* de nomes exclusivas (especificada no comando [**glNewList**](glnewlist.md) ).</span><span class="sxs-lookup"><span data-stu-id="07e83-129">When the **glEndList** function is encountered, the display list definition is completed by associating the list with the unique name *list* (specified in the [**glNewList**](glnewlist.md) command).</span></span> <span data-ttu-id="07e83-130">Se já existir uma lista de exibição com a *lista* de nomes, ela será substituída somente quando **glEndList** for chamado.</span><span class="sxs-lookup"><span data-stu-id="07e83-130">If a display list with name *list* already exists, it is replaced only when **glEndList** is called.</span></span>

<span data-ttu-id="07e83-131">As funções [**glCallList**](glcalllist.md) e [**glCallLists**](glcalllists.md) podem ser inseridas em listas de exibição.</span><span class="sxs-lookup"><span data-stu-id="07e83-131">The [**glCallList**](glcalllist.md) and [**glCallLists**](glcalllists.md) functions can be entered into display lists.</span></span> <span data-ttu-id="07e83-132">Os comandos na lista de exibição ou listas executadas por **glCallList** ou **glCallLists** não são incluídos na lista de exibição que está sendo criada, mesmo que o modo de criação de lista seja GL \_ Compilar \_ e \_ executar.</span><span class="sxs-lookup"><span data-stu-id="07e83-132">The commands in the display list or lists executed by **glCallList** or **glCallLists** are not included in the display list being created, even if the list creation mode is GL\_COMPILE\_AND\_EXECUTE.</span></span>

<span data-ttu-id="07e83-133">A função a seguir recupera informações relacionadas a [**glNewList**](glnewlist.md):</span><span class="sxs-lookup"><span data-stu-id="07e83-133">The following function retrieves information related to [**glNewList**](glnewlist.md):</span></span>

<span data-ttu-id="07e83-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ modo de matriz GL de argumento \_</span><span class="sxs-lookup"><span data-stu-id="07e83-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="07e83-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07e83-135">Requirements</span></span>



| <span data-ttu-id="07e83-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="07e83-136">Requirement</span></span> | <span data-ttu-id="07e83-137">Valor</span><span class="sxs-lookup"><span data-stu-id="07e83-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07e83-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07e83-138">Minimum supported client</span></span><br/> | <span data-ttu-id="07e83-139">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="07e83-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="07e83-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07e83-140">Minimum supported server</span></span><br/> | <span data-ttu-id="07e83-141">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="07e83-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="07e83-142">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="07e83-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="07e83-143"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="07e83-143"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="07e83-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="07e83-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="07e83-145"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07e83-145"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="07e83-146">DLL</span><span class="sxs-lookup"><span data-stu-id="07e83-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07e83-147"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07e83-147"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07e83-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="07e83-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07e83-149">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="07e83-149">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="07e83-150">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="07e83-150">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="07e83-151">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="07e83-151">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="07e83-152">**glDeleteLists**</span><span class="sxs-lookup"><span data-stu-id="07e83-152">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="07e83-153">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="07e83-153">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="07e83-154">**glGenLists**</span><span class="sxs-lookup"><span data-stu-id="07e83-154">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="07e83-155">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="07e83-155">**glIsList**</span></span>](glislist.md)
</dt> <dt>

[<span data-ttu-id="07e83-156">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="07e83-156">**glNewList**</span></span>](glnewlist.md)
</dt> </dl>

 

 





