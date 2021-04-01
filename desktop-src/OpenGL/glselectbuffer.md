---
title: função glSelectBuffer (GL. h)
description: A função glSelectBuffer estabelece um buffer para valores do modo de seleção.
ms.assetid: b5c64364-1f47-4281-96b5-95c3f5c8e753
keywords:
- função glSelectBuffer OpenGL
topic_type:
- apiref
api_name:
- glSelectBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efa5b97abad6575de77a760c72e3eb05e90461c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644284"
---
# <a name="glselectbuffer-function"></a><span data-ttu-id="914b4-104">função glSelectBuffer</span><span class="sxs-lookup"><span data-stu-id="914b4-104">glSelectBuffer function</span></span>

<span data-ttu-id="914b4-105">A função **glSelectBuffer** estabelece um buffer para valores do modo de seleção.</span><span class="sxs-lookup"><span data-stu-id="914b4-105">The **glSelectBuffer** function establishes a buffer for selection mode values.</span></span>

## <a name="syntax"></a><span data-ttu-id="914b4-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="914b4-106">Syntax</span></span>


```C++
void WINAPI glSelectBuffer(
   GLsizei size,
   GLuint  *buffer
);
```



## <a name="parameters"></a><span data-ttu-id="914b4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="914b4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="914b4-108">*size*</span><span class="sxs-lookup"><span data-stu-id="914b4-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="914b4-109">O tamanho do *buffer*.</span><span class="sxs-lookup"><span data-stu-id="914b4-109">The size of *buffer*.</span></span>

</dd> <dt>

<span data-ttu-id="914b4-110">*completo*</span><span class="sxs-lookup"><span data-stu-id="914b4-110">*buffer*</span></span> 
</dt> <dd>

<span data-ttu-id="914b4-111">Retorna os dados de seleção.</span><span class="sxs-lookup"><span data-stu-id="914b4-111">Returns the selection data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="914b4-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="914b4-112">Return value</span></span>

<span data-ttu-id="914b4-113">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="914b4-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="914b4-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="914b4-114">Error codes</span></span>

<span data-ttu-id="914b4-115">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="914b4-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="914b4-116">Nome</span><span class="sxs-lookup"><span data-stu-id="914b4-116">Name</span></span>                                                                                                  | <span data-ttu-id="914b4-117">Significado</span><span class="sxs-lookup"><span data-stu-id="914b4-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="914b4-118"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="914b4-118"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="914b4-119">o *tamanho* era negativo.</span><span class="sxs-lookup"><span data-stu-id="914b4-119">*size* was negative.</span></span><br/>                                                                                                       |
| <dl> <span data-ttu-id="914b4-120"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="914b4-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="914b4-121">A função foi chamada enquanto o modo de renderização era GL \_ Select.</span><span class="sxs-lookup"><span data-stu-id="914b4-121">The function was called while the render mode was GL\_SELECT.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="914b4-122"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="914b4-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="914b4-123">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="914b4-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="914b4-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="914b4-124">Remarks</span></span>

<span data-ttu-id="914b4-125">A função **glSelectBuffer** tem dois parâmetros: *buffer* é um ponteiro para uma matriz de inteiros sem sinal e *size* indica o tamanho da matriz.</span><span class="sxs-lookup"><span data-stu-id="914b4-125">The **glSelectBuffer** function has two parameters: *buffer* is a pointer to an array of unsigned integers, and *size* indicates the size of the array.</span></span> <span data-ttu-id="914b4-126">O parâmetro *buffer* retorna valores da pilha de nomes (consulte [**glInitNames**](glinitnames.md), [**glLoadName**](glloadname.md), [**glPushName**](glpushname.md)) quando o modo de renderização é GL \_ Select (consulte [**glRenderMode**](glrendermode.md)).</span><span class="sxs-lookup"><span data-stu-id="914b4-126">The *buffer* parameter returns values from the name stack (see [**glInitNames**](glinitnames.md), [**glLoadName**](glloadname.md), [**glPushName**](glpushname.md)) when the rendering mode is GL\_SELECT (see [**glRenderMode**](glrendermode.md)).</span></span> <span data-ttu-id="914b4-127">A função **glSelectBuffer** deve ser emitida antes de o modo de seleção ser habilitado e não deve ser emitida enquanto o modo de RENDERIZAÇÃO é GL \_ Select.</span><span class="sxs-lookup"><span data-stu-id="914b4-127">The **glSelectBuffer** function must be issued before selection mode is enabled, and it must not be issued while the rendering mode is GL\_SELECT.</span></span>

<span data-ttu-id="914b4-128">A seleção é usada por um programador para determinar quais primitivos são desenhados em alguma região de uma janela.</span><span class="sxs-lookup"><span data-stu-id="914b4-128">Selection is used by a programmer to determine which primitives are drawn into some region of a window.</span></span> <span data-ttu-id="914b4-129">A região é definida pelas matrizes modelview e Perspective atuais.</span><span class="sxs-lookup"><span data-stu-id="914b4-129">The region is defined by the current modelview and perspective matrices.</span></span>

<span data-ttu-id="914b4-130">No modo de seleção, nenhum fragmento de pixel é produzido da rasterização.</span><span class="sxs-lookup"><span data-stu-id="914b4-130">In selection mode, no pixel fragments are produced from rasterization.</span></span> <span data-ttu-id="914b4-131">Em vez disso, se um primitivo interceptar o volume de clipe definido pelos frustum de exibição e os planos de recorte definidos pelo usuário, esse primitivo causará uma visita de seleção.</span><span class="sxs-lookup"><span data-stu-id="914b4-131">Instead, if a primitive intersects the clip volume defined by the viewing frustum and the user-defined clipping planes, this primitive causes a selection hit.</span></span> <span data-ttu-id="914b4-132">(Com polígonos, nenhuma ocorrência ocorrerá se o polígono for refeito.) Quando uma alteração é feita na pilha de nomes, ou quando [**glRenderMode**](glrendermode.md) é chamado, um registro de ocorrência é copiado para *buffer* se qualquer ocorrência ocorreu desde o último evento (uma alteração de pilha de nome ou uma chamada **glRenderMode** ).</span><span class="sxs-lookup"><span data-stu-id="914b4-132">(With polygons, no hit occurs if the polygon is culled.) When a change is made to the name stack, or when [**glRenderMode**](glrendermode.md) is called, a hit record is copied to *buffer* if any hits have occurred since the last such event (either a name stack change or a **glRenderMode** call).</span></span> <span data-ttu-id="914b4-133">O registro de acesso consiste no número de nomes na pilha de nomes no momento do evento; seguido pelos valores mínimo e máximo de profundidade de todos os vértices que atingiram desde o evento anterior; seguido pelo conteúdo da pilha de nome, primeiro o nome inferior.</span><span class="sxs-lookup"><span data-stu-id="914b4-133">The hit record consists of the number of names in the name stack at the time of the event; followed by the minimum and maximum depth values of all vertices that hit since the previous event; followed by the name stack contents, bottom name first.</span></span>

<span data-ttu-id="914b4-134">Os valores de profundidade retornados são mapeados de modo que o maior valor inteiro não assinado corresponde à profundidade da coordenada da janela 1,0 e zero corresponde à profundidade da coordenada da janela 0,0.</span><span class="sxs-lookup"><span data-stu-id="914b4-134">Returned depth values are mapped such that the largest unsigned integer value corresponds to window coordinate depth 1.0, and zero corresponds to window coordinate depth 0.0.</span></span>

<span data-ttu-id="914b4-135">Um índice interno no *buffer* é redefinido para zero sempre que o modo de seleção é inserido.</span><span class="sxs-lookup"><span data-stu-id="914b4-135">An internal index into *buffer* is reset to zero whenever selection mode is entered.</span></span> <span data-ttu-id="914b4-136">Cada vez que um registro de acesso é copiado no *buffer*, o índice é incrementado para apontar para a célula logo após o final do bloco de namesthat, para a próxima célula disponível.</span><span class="sxs-lookup"><span data-stu-id="914b4-136">Each time a hit record is copied into *buffer*, the index is incremented to point to the cell just past the end of the block of namesthat is, to the next available cell.</span></span> <span data-ttu-id="914b4-137">Se o registro de acesso for maior do que o número de localizações restantes no *buffer*, a quantidade de dados que puder ajustar será copiada e o sinalizador de estouro será definido.</span><span class="sxs-lookup"><span data-stu-id="914b4-137">If the hit record is larger than the number of remaining locations in *buffer*, as much data as can fit is copied, and the overflow flag is set.</span></span> <span data-ttu-id="914b4-138">Se a pilha de nomes estiver vazia quando um registro de acesso for copiado, esse registro consistirá em zero seguido dos valores mínimo e máximo de profundidade.</span><span class="sxs-lookup"><span data-stu-id="914b4-138">If the name stack is empty when a hit record is copied, that record consists of zero followed by the minimum and maximum depth values.</span></span>

<span data-ttu-id="914b4-139">O modo de seleção é encerrado chamando **glRenderMode** com um argumento diferente de GL \_ Select.</span><span class="sxs-lookup"><span data-stu-id="914b4-139">Selection mode is exited by calling **glRenderMode** with an argument other than GL\_SELECT.</span></span> <span data-ttu-id="914b4-140">Sempre que **glRenderMode** for chamado enquanto o modo de RENDERIZAÇÃO for GL \_ Select, ele retornará o número de registros de acesso copiados para *buffer*, redefinirá o sinalizador de estouro e o ponteiro de buffer de seleção e inicializará a pilha de nomes como vazia.</span><span class="sxs-lookup"><span data-stu-id="914b4-140">Whenever **glRenderMode** is called while the render mode is GL\_SELECT, it returns the number of hit records copied to *buffer*, resets the overflow flag and the selection buffer pointer, and initializes the name stack to be empty.</span></span> <span data-ttu-id="914b4-141">Se o bit de estouro tiver sido definido quando **glRenderMode** foi chamado, uma contagem de registros de impacto negativo será retornada.</span><span class="sxs-lookup"><span data-stu-id="914b4-141">If the overflow bit was set when **glRenderMode** was called, a negative hit record count is returned.</span></span>

<span data-ttu-id="914b4-142">O conteúdo do *buffer* é indefinido até que [**glRenderMode**](glrendermode.md) seja chamado com um argumento diferente de GL \_ Select.</span><span class="sxs-lookup"><span data-stu-id="914b4-142">The contents of *buffer* are undefined until [**glRenderMode**](glrendermode.md) is called with an argument other than GL\_SELECT.</span></span>

<span data-ttu-id="914b4-143">Os  / primitivos glBegin **glEnd** e chamadas para [**glRasterPos**](glrasterpos-functions.md) podem resultar em ocorrências.</span><span class="sxs-lookup"><span data-stu-id="914b4-143">The **glBegin**/**glEnd** primitives and calls to [**glRasterPos**](glrasterpos-functions.md) can result in hits.</span></span>

<span data-ttu-id="914b4-144">A função a seguir recupera informações relacionadas a **glSelectBuffer**:</span><span class="sxs-lookup"><span data-stu-id="914b4-144">The following function retrieves information related to **glSelectBuffer**:</span></span>

<span data-ttu-id="914b4-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento \_ GL \_ profundidade da pilha de nome \_</span><span class="sxs-lookup"><span data-stu-id="914b4-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NAME\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="914b4-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="914b4-146">Requirements</span></span>



| <span data-ttu-id="914b4-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="914b4-147">Requirement</span></span> | <span data-ttu-id="914b4-148">Valor</span><span class="sxs-lookup"><span data-stu-id="914b4-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="914b4-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="914b4-149">Minimum supported client</span></span><br/> | <span data-ttu-id="914b4-150">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="914b4-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="914b4-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="914b4-151">Minimum supported server</span></span><br/> | <span data-ttu-id="914b4-152">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="914b4-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="914b4-153">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="914b4-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="914b4-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="914b4-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="914b4-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="914b4-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="914b4-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="914b4-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="914b4-157">DLL</span><span class="sxs-lookup"><span data-stu-id="914b4-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="914b4-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="914b4-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="914b4-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="914b4-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="914b4-160">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="914b4-160">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="914b4-161">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="914b4-161">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="914b4-162">**glFeedbackBuffer**</span><span class="sxs-lookup"><span data-stu-id="914b4-162">**glFeedbackBuffer**</span></span>](glfeedbackbuffer.md)
</dt> <dt>

[<span data-ttu-id="914b4-163">**glInitNames**</span><span class="sxs-lookup"><span data-stu-id="914b4-163">**glInitNames**</span></span>](glinitnames.md)
</dt> <dt>

[<span data-ttu-id="914b4-164">**glLoadName**</span><span class="sxs-lookup"><span data-stu-id="914b4-164">**glLoadName**</span></span>](glloadname.md)
</dt> <dt>

[<span data-ttu-id="914b4-165">**glPushName**</span><span class="sxs-lookup"><span data-stu-id="914b4-165">**glPushName**</span></span>](glpushname.md)
</dt> <dt>

[<span data-ttu-id="914b4-166">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="914b4-166">**glRenderMode**</span></span>](glrendermode.md)
</dt> </dl>

 

 





