---
title: função glNewList (GL. h)
description: As funções glNewList e glEndList criam ou substituem uma lista de exibição. | função glNewList (GL. h)
ms.assetid: 9c6556d4-855f-4cba-94cc-27b5f1e4607a
keywords:
- função glNewList OpenGL
topic_type:
- apiref
api_name:
- glNewList
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6135f67c07f69d24df67d4f1899404359efaa7aa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105755980"
---
# <a name="glnewlist-function"></a><span data-ttu-id="4e912-105">função glNewList</span><span class="sxs-lookup"><span data-stu-id="4e912-105">glNewList function</span></span>

<span data-ttu-id="4e912-106">As funções **glNewList** e [**glEndList**](glendlist.md) criam ou substituem uma lista de exibição.</span><span class="sxs-lookup"><span data-stu-id="4e912-106">The **glNewList** and [**glEndList**](glendlist.md) functions create or replace a display list.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e912-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4e912-107">Syntax</span></span>


```C++
void WINAPI glNewList(
   GLuint list,
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="4e912-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e912-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e912-109">*list*</span><span class="sxs-lookup"><span data-stu-id="4e912-109">*list*</span></span> 
</dt> <dd>

<span data-ttu-id="4e912-110">O nome da lista de exibição.</span><span class="sxs-lookup"><span data-stu-id="4e912-110">The display list name.</span></span>

</dd> <dt>

<span data-ttu-id="4e912-111">*mode*</span><span class="sxs-lookup"><span data-stu-id="4e912-111">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="4e912-112">O modo de compilação.</span><span class="sxs-lookup"><span data-stu-id="4e912-112">The compilation mode.</span></span> <span data-ttu-id="4e912-113">Os valores a seguir são aceitos.</span><span class="sxs-lookup"><span data-stu-id="4e912-113">The following values are accepted.</span></span>



| <span data-ttu-id="4e912-114">Valor</span><span class="sxs-lookup"><span data-stu-id="4e912-114">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="4e912-115">Significado</span><span class="sxs-lookup"><span data-stu-id="4e912-115">Meaning</span></span>                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="GL_COMPILE"></span><span id="gl_compile"></span><dl> <span data-ttu-id="4e912-116"><dt>**\_compilação GL**</dt></span><span class="sxs-lookup"><span data-stu-id="4e912-116"><dt>**GL\_COMPILE**</dt></span></span> </dl>                                       | <span data-ttu-id="4e912-117">Os comandos são meramente compilados.</span><span class="sxs-lookup"><span data-stu-id="4e912-117">Commands are merely compiled.</span></span><br/>                                     |
| <span id="GL_COMPILE_AND_EXECUTE"></span><span id="gl_compile_and_execute"></span><dl> <span data-ttu-id="4e912-118"><dt>**GL \_ Compilar \_ e \_ executar**</dt></span><span class="sxs-lookup"><span data-stu-id="4e912-118"><dt>**GL\_COMPILE\_AND\_EXECUTE**</dt></span></span> </dl> | <span data-ttu-id="4e912-119">Os comandos são executados conforme são compilados na lista de exibição.</span><span class="sxs-lookup"><span data-stu-id="4e912-119">Commands are executed as they are compiled into the display list.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e912-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4e912-120">Return value</span></span>

<span data-ttu-id="4e912-121">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4e912-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4e912-122">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="4e912-122">Error codes</span></span>

<span data-ttu-id="4e912-123">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="4e912-123">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="4e912-124">Nome</span><span class="sxs-lookup"><span data-stu-id="4e912-124">Name</span></span>                                                                                                  | <span data-ttu-id="4e912-125">Significado</span><span class="sxs-lookup"><span data-stu-id="4e912-125">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4e912-126"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4e912-126"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="4e912-127">a *lista* era zero.</span><span class="sxs-lookup"><span data-stu-id="4e912-127">*list* was zero.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="4e912-128"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="4e912-128"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="4e912-129">o *modo* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="4e912-129">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="4e912-130"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4e912-130"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="4e912-131">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="4e912-131">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4e912-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e912-132">Remarks</span></span>

<span data-ttu-id="4e912-133">As listas de exibição são grupos de comandos OpenGL que foram armazenados para execução subsequente.</span><span class="sxs-lookup"><span data-stu-id="4e912-133">Display lists are groups of OpenGL commands that have been stored for subsequent execution.</span></span> <span data-ttu-id="4e912-134">As listas de exibição são criadas com **glNewList**.</span><span class="sxs-lookup"><span data-stu-id="4e912-134">The display lists are created with **glNewList**.</span></span> <span data-ttu-id="4e912-135">Todos os comandos subsequentes são colocados na lista de exibição, na ordem emitida, até que **glEndList** seja chamado.</span><span class="sxs-lookup"><span data-stu-id="4e912-135">All subsequent commands are placed in the display list, in the order issued, until **glEndList** is called.</span></span>

<span data-ttu-id="4e912-136">A função **glNewList** tem dois parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4e912-136">The **glNewList** function has two parameters.</span></span> <span data-ttu-id="4e912-137">O primeiro parâmetro, *lista*, é um inteiro positivo que se torna o nome exclusivo da lista de exibição.</span><span class="sxs-lookup"><span data-stu-id="4e912-137">The first parameter, *list*, is a positive integer that becomes the unique name for the display list.</span></span> <span data-ttu-id="4e912-138">Os nomes podem ser criados e reservados com [**glGenLists**](glgenlists.md) e testados para exclusividade com [**glIsList**](glislist.md).</span><span class="sxs-lookup"><span data-stu-id="4e912-138">Names can be created and reserved with [**glGenLists**](glgenlists.md) and tested for uniqueness with [**glIsList**](glislist.md).</span></span> <span data-ttu-id="4e912-139">O segundo parâmetro, *Mode*, é uma constante simbólica que pode assumir um dos dois valores anteriores.</span><span class="sxs-lookup"><span data-stu-id="4e912-139">The second parameter, *mode*, is a symbolic constant that can assume one of the two preceding values.</span></span>

<span data-ttu-id="4e912-140">Determinados comandos não são compilados na lista de exibição, mas são executados imediatamente, independentemente do modo da lista de exibição.</span><span class="sxs-lookup"><span data-stu-id="4e912-140">Certain commands are not compiled into the display list, but are executed immediately, regardless of the display list mode.</span></span> <span data-ttu-id="4e912-141">Esses comandos são [**glColorPointer**](glcolorpointer.md), [**glDeleteLists**](gldeletelists.md), [**glDisableClientState**](gldisableclientstate.md), [**glEdgeFlagPointer**](gledgeflagpointer.md), [**glEnableClientState**](glenableclientstate.md), [**glFeedbackBuffer**](glfeedbackbuffer.md), [**glFinish**](glfinish.md), [**glFlush**](glflush.md), [**glGenLists**](glgenlists.md), [**glIndexPointer**](glindexpointer.md), [**glInterleavedArrays**](glinterleavedarrays.md), [**glIsEnabled**](glisenabled.md), [**GlIsList**](glislist.md), [**glNormalPointer**](glnormalpointer.md), [**glPopClientAttrib**](glpopclientattrib.md), [**glPixelStore**](glpixelstore-functions.md), [**glPushClientAttrib**](glpushclientattrib.md), [**glReadPixels**](glreadpixels.md), [**glRenderMode**](glrendermode.md), [**glSelectBuffer**](glselectbuffer.md), [**glTexCoordPointer**](gltexcoordpointer.md), [**glVertexPointer**](glvertexpointer.md)e todas as rotinas de [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) .</span><span class="sxs-lookup"><span data-stu-id="4e912-141">These commands are [**glColorPointer**](glcolorpointer.md), [**glDeleteLists**](gldeletelists.md), [**glDisableClientState**](gldisableclientstate.md), [**glEdgeFlagPointer**](gledgeflagpointer.md), [**glEnableClientState**](glenableclientstate.md), [**glFeedbackBuffer**](glfeedbackbuffer.md), [**glFinish**](glfinish.md), [**glFlush**](glflush.md), [**glGenLists**](glgenlists.md), [**glIndexPointer**](glindexpointer.md), [**glInterleavedArrays**](glinterleavedarrays.md), [**glIsEnabled**](glisenabled.md), [**glIsList**](glislist.md), [**glNormalPointer**](glnormalpointer.md), [**glPopClientAttrib**](glpopclientattrib.md), [**glPixelStore**](glpixelstore-functions.md), [**glPushClientAttrib**](glpushclientattrib.md), [**glReadPixels**](glreadpixels.md), [**glRenderMode**](glrendermode.md), [**glSelectBuffer**](glselectbuffer.md), [**glTexCoordPointer**](gltexcoordpointer.md), [**glVertexPointer**](glvertexpointer.md), and all of the [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) routines.</span></span>

<span data-ttu-id="4e912-142">Da mesma forma, [**glTexImage2D**](glteximage2d.md) e [**glTexImage1D**](glteximage1d.md) são executados imediatamente e não são compilados na lista de exibição quando seu primeiro argumento \_ é GL de proxy \_ \_ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="4e912-142">Similarly, [**glTexImage2D**](glteximage2d.md) and [**glTexImage1D**](glteximage1d.md) are executed immediately and not compiled into the display list when their first argument is GL\_PROXY\_TEXTURE\_2D or GL\_PROXY\_TEXTURE\_1D, respectively.</span></span>

<span data-ttu-id="4e912-143">Quando a função **glEndList** é encontrada, a definição da lista de exibição é concluída pela Associação da lista com a *lista* de nomes exclusivas (especificada no comando **glNewList** ).</span><span class="sxs-lookup"><span data-stu-id="4e912-143">When the **glEndList** function is encountered, the display list definition is completed by associating the list with the unique name *list* (specified in the **glNewList** command).</span></span> <span data-ttu-id="4e912-144">Se já existir uma lista de exibição com a *lista* de nomes, ela será substituída somente quando **glEndList** for chamado.</span><span class="sxs-lookup"><span data-stu-id="4e912-144">If a display list with name *list* already exists, it is replaced only when **glEndList** is called.</span></span>

<span data-ttu-id="4e912-145">As funções [**glCallList**](glcalllist.md) e [**glCallLists**](glcalllists.md) podem ser inseridas em listas de exibição.</span><span class="sxs-lookup"><span data-stu-id="4e912-145">The [**glCallList**](glcalllist.md) and [**glCallLists**](glcalllists.md) functions can be entered into display lists.</span></span> <span data-ttu-id="4e912-146">Os comandos na lista de exibição ou listas executadas por **glCallList** ou **glCallLists** não são incluídos na lista de exibição que está sendo criada, mesmo que o modo de criação de lista seja GL \_ Compilar \_ e \_ executar.</span><span class="sxs-lookup"><span data-stu-id="4e912-146">The commands in the display list or lists executed by **glCallList** or **glCallLists** are not included in the display list being created, even if the list creation mode is GL\_COMPILE\_AND\_EXECUTE.</span></span>

<span data-ttu-id="4e912-147">A função a seguir recupera informações relacionadas a **glNewList**:</span><span class="sxs-lookup"><span data-stu-id="4e912-147">The following function retrieves information related to **glNewList**:</span></span>

<span data-ttu-id="4e912-148">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ modo de matriz GL de argumento \_</span><span class="sxs-lookup"><span data-stu-id="4e912-148">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="4e912-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e912-149">Requirements</span></span>



| <span data-ttu-id="4e912-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e912-150">Requirement</span></span> | <span data-ttu-id="4e912-151">Valor</span><span class="sxs-lookup"><span data-stu-id="4e912-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e912-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e912-152">Minimum supported client</span></span><br/> | <span data-ttu-id="4e912-153">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4e912-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4e912-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e912-154">Minimum supported server</span></span><br/> | <span data-ttu-id="4e912-155">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4e912-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4e912-156">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4e912-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e912-157"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e912-157"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="4e912-158">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4e912-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="4e912-159"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e912-159"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4e912-160">DLL</span><span class="sxs-lookup"><span data-stu-id="4e912-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e912-161"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e912-161"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e912-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e912-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e912-163">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="4e912-163">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="4e912-164">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="4e912-164">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="4e912-165">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="4e912-165">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="4e912-166">**glDeleteLists**</span><span class="sxs-lookup"><span data-stu-id="4e912-166">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="4e912-167">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="4e912-167">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="4e912-168">**glEndList**</span><span class="sxs-lookup"><span data-stu-id="4e912-168">**glEndList**</span></span>](glendlist.md)
</dt> <dt>

[<span data-ttu-id="4e912-169">**glGenLists**</span><span class="sxs-lookup"><span data-stu-id="4e912-169">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="4e912-170">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="4e912-170">**glIsList**</span></span>](glislist.md)
</dt> </dl>

 

 





