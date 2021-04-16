---
title: função glIndexPointer (GL. h)
description: A função glIndexPointer define uma matriz de índices de cores.
ms.assetid: b435d950-1f87-4041-93e4-f1f8786cabdb
keywords:
- função glIndexPointer OpenGL
topic_type:
- apiref
api_name:
- glIndexPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cca6858d7d1e3f13e4155bd40307a53b22e80a56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454661"
---
# <a name="glindexpointer-function"></a><span data-ttu-id="1e84e-104">função glIndexPointer</span><span class="sxs-lookup"><span data-stu-id="1e84e-104">glIndexPointer function</span></span>

<span data-ttu-id="1e84e-105">A função **glIndexPointer** define uma matriz de índices de cores.</span><span class="sxs-lookup"><span data-stu-id="1e84e-105">The **glIndexPointer** function defines an array of color indexes.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e84e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1e84e-106">Syntax</span></span>


```C++
void WINAPI glIndexPointer(
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="1e84e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1e84e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e84e-108">*tipo*</span><span class="sxs-lookup"><span data-stu-id="1e84e-108">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="1e84e-109">O tipo de dados de cada índice de cor na matriz usando as seguintes constantes simbólicas: GL \_ short, GL \_ int, GL \_ float, GL \_ Double.</span><span class="sxs-lookup"><span data-stu-id="1e84e-109">The data type of each color index in the array using the following symbolic constants: GL\_SHORT, GL\_INT, GL\_FLOAT, GL\_DOUBLE.</span></span>

</dd> <dt>

<span data-ttu-id="1e84e-110">*Stride*</span><span class="sxs-lookup"><span data-stu-id="1e84e-110">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="1e84e-111">O deslocamento de byte entre os índices de cor consecutivos.</span><span class="sxs-lookup"><span data-stu-id="1e84e-111">The byte offset between consecutive color indexes.</span></span> <span data-ttu-id="1e84e-112">Quando *Stride* é zero, os índices de cores são totalmente empacotados na matriz.</span><span class="sxs-lookup"><span data-stu-id="1e84e-112">When *stride* is zero, the color indexes are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="1e84e-113">*ponteiro*</span><span class="sxs-lookup"><span data-stu-id="1e84e-113">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="1e84e-114">Um ponteiro para o primeiro índice de cor na matriz.</span><span class="sxs-lookup"><span data-stu-id="1e84e-114">A pointer to the first color index in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e84e-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1e84e-115">Return value</span></span>

<span data-ttu-id="1e84e-116">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1e84e-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1e84e-117">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="1e84e-117">Error codes</span></span>

<span data-ttu-id="1e84e-118">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="1e84e-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="1e84e-119">Nome</span><span class="sxs-lookup"><span data-stu-id="1e84e-119">Name</span></span>                                                                                              | <span data-ttu-id="1e84e-120">Significado</span><span class="sxs-lookup"><span data-stu-id="1e84e-120">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="1e84e-121"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="1e84e-121"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="1e84e-122">o *tipo* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="1e84e-122">*type* was not an accepted value.</span></span><br/> |
| <dl> <span data-ttu-id="1e84e-123"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1e84e-123"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="1e84e-124">*Stride* ou *Count* era negativo.</span><span class="sxs-lookup"><span data-stu-id="1e84e-124">*stride* or *count* was negative.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1e84e-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="1e84e-125">Remarks</span></span>

<span data-ttu-id="1e84e-126">A função **glIndexPointer** especifica o local e os dados de uma matriz de índices de cores a serem usados durante a renderização.</span><span class="sxs-lookup"><span data-stu-id="1e84e-126">The **glIndexPointer** function specifies the location and data of an array of color indexes to use when rendering.</span></span> <span data-ttu-id="1e84e-127">O parâmetro de *tipo* especifica o tipo de dados de cada índice de cor e *Stride* determina o deslocamento de byte de um índice de cor para o próximo, habilitando a embalagem de vértices e atributos em uma única matriz ou armazenamento em matrizes separadas.</span><span class="sxs-lookup"><span data-stu-id="1e84e-127">The *type* parameter specifies the data type of each color index and *stride* determines the byte offset from one color index to the next, enabling the packing of vertices and attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="1e84e-128">Em algumas implementações, armazenar os vértices e os atributos em uma única matriz pode ser mais eficiente do que usar matrizes separadas.</span><span class="sxs-lookup"><span data-stu-id="1e84e-128">In some implementations, storing the vertices and attributes in a single array can be more efficient than using separate arrays.</span></span> <span data-ttu-id="1e84e-129">Para obter mais informações, consulte [**glInterleavedArrays**](glinterleavedarrays.md).</span><span class="sxs-lookup"><span data-stu-id="1e84e-129">For more information, see [**glInterleavedArrays**](glinterleavedarrays.md).</span></span>

<span data-ttu-id="1e84e-130">Uma matriz de índice de cor é habilitada quando você especifica a \_ constante de matriz de índice GL \_ com [**glEnableClientState**](glenableclientstate.md).</span><span class="sxs-lookup"><span data-stu-id="1e84e-130">A color-index array is enabled when you specify the GL\_INDEX\_ARRAY constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="1e84e-131">Quando habilitado, [**glDrawArrays**](gldrawarrays.md) e [**glArrayElement**](glarrayelement.md) usam a matriz de índice de cor.</span><span class="sxs-lookup"><span data-stu-id="1e84e-131">When enabled, [**glDrawArrays**](gldrawarrays.md) and [**glArrayElement**](glarrayelement.md) use the color-index array.</span></span> <span data-ttu-id="1e84e-132">Por padrão, a matriz de índice de cores está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="1e84e-132">By default the color-index array is disabled.</span></span>

<span data-ttu-id="1e84e-133">Você não pode incluir **glIndexPointer** em listas de exibição.</span><span class="sxs-lookup"><span data-stu-id="1e84e-133">You cannot include **glIndexPointer** in display lists.</span></span>

<span data-ttu-id="1e84e-134">Quando você especifica uma matriz de índice de cor usando **glIndexPointer**, os valores de todos os parâmetros de matriz de índice de cor da função são salvos em um estado do lado do cliente e os elementos estáticos da matriz podem ser armazenados em cache.</span><span class="sxs-lookup"><span data-stu-id="1e84e-134">When you specify a color-index array using **glIndexPointer**, the values of all the function's color-index array parameters are saved in a client-side state and static array elements can be cached.</span></span> <span data-ttu-id="1e84e-135">Como os parâmetros de matriz de índice de cor são o estado do lado do cliente, seus valores não são salvos nem restaurados por [**glPushAttrib**](glpushattrib.md) e **glPopAttrib**.</span><span class="sxs-lookup"><span data-stu-id="1e84e-135">Because the color-index array parameters are client-side state, their values are not saved or restored by [**glPushAttrib**](glpushattrib.md) and **glPopAttrib**.</span></span>

<span data-ttu-id="1e84e-136">Embora nenhum erro seja gerado quando você chama **glIndexPointer** nos pares [**glBegin**](glbegin.md) e **glEnd** , os resultados são indefinidos.</span><span class="sxs-lookup"><span data-stu-id="1e84e-136">Although no error is generated when you call **glIndexPointer** within [**glBegin**](glbegin.md) and **glEnd** pairs, the results are undefined.</span></span>

<span data-ttu-id="1e84e-137">As funções a seguir recuperam informações relacionadas ao **glIndexPointer**:</span><span class="sxs-lookup"><span data-stu-id="1e84e-137">The following functions retrieve information related to **glIndexPointer**:</span></span>

<span data-ttu-id="1e84e-138">[**glIsEnabled**](glisenabled.md) com matriz de índice de argumento GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="1e84e-138">[**glIsEnabled**](glisenabled.md) with argument GL\_INDEX\_ARRAY</span></span>

<span data-ttu-id="1e84e-139">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com a matriz de índice do argumento GL \_ \_ \_ Stride</span><span class="sxs-lookup"><span data-stu-id="1e84e-139">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_INDEX\_ARRAY\_STRIDE</span></span>

<span data-ttu-id="1e84e-140"> \_ \_ contagem de matrizes de índice glGet com Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="1e84e-140">**glGet** with argument GL\_INDEX\_ARRAY\_COUNT</span></span>

<span data-ttu-id="1e84e-141">**glGet** com o \_ tipo de \_ matriz de índice do argumento GL \_</span><span class="sxs-lookup"><span data-stu-id="1e84e-141">**glGet** with argument GL\_INDEX\_ARRAY\_TYPE</span></span>

<span data-ttu-id="1e84e-142">**glGet** com o argumento \_ GL \_ tamanho da matriz de índice \_</span><span class="sxs-lookup"><span data-stu-id="1e84e-142">**glGet** with argument GL\_INDEX\_ARRAY\_SIZE</span></span>

<span data-ttu-id="1e84e-143">[](glgetpointerv.md) ponteiro de matriz de índice glGetPointerv com Argument GL \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="1e84e-143">[**glGetPointerv**](glgetpointerv.md) with argument GL\_INDEX\_ARRAY\_POINTER</span></span>

## <a name="requirements"></a><span data-ttu-id="1e84e-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e84e-144">Requirements</span></span>



| <span data-ttu-id="1e84e-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e84e-145">Requirement</span></span> | <span data-ttu-id="1e84e-146">Valor</span><span class="sxs-lookup"><span data-stu-id="1e84e-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e84e-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e84e-147">Minimum supported client</span></span><br/> | <span data-ttu-id="1e84e-148">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1e84e-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1e84e-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e84e-149">Minimum supported server</span></span><br/> | <span data-ttu-id="1e84e-150">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1e84e-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1e84e-151">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1e84e-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e84e-152"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e84e-152"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1e84e-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1e84e-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="1e84e-154"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e84e-154"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1e84e-155">DLL</span><span class="sxs-lookup"><span data-stu-id="1e84e-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e84e-156"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e84e-156"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e84e-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e84e-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e84e-158">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="1e84e-158">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="1e84e-159">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="1e84e-159">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="1e84e-160">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="1e84e-160">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="1e84e-161">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="1e84e-161">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="1e84e-162">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="1e84e-162">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="1e84e-163">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="1e84e-163">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="1e84e-164">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="1e84e-164">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="1e84e-165">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="1e84e-165">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="1e84e-166">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="1e84e-166">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="1e84e-167">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="1e84e-167">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





