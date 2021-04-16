---
title: função glVertexPointer (GL. h)
description: A função glVertexPointer define uma matriz de dados de vértice.
ms.assetid: e5f97fdc-9448-4389-8533-3855a3213feb
keywords:
- função glVertexPointer OpenGL
topic_type:
- apiref
api_name:
- glVertexPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 422dd1a7938cc5adb183ff7e17c59a8f52eb4909
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455650"
---
# <a name="glvertexpointer-function"></a><span data-ttu-id="6bf02-104">função glVertexPointer</span><span class="sxs-lookup"><span data-stu-id="6bf02-104">glVertexPointer function</span></span>

<span data-ttu-id="6bf02-105">A função **glVertexPointer** define uma matriz de dados de vértice.</span><span class="sxs-lookup"><span data-stu-id="6bf02-105">The **glVertexPointer** function defines an array of vertex data.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bf02-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6bf02-106">Syntax</span></span>


```C++
void WINAPI glVertexPointer(
         GLint   size,
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="6bf02-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6bf02-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bf02-108">*size*</span><span class="sxs-lookup"><span data-stu-id="6bf02-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="6bf02-109">O número de coordenadas por vértice.</span><span class="sxs-lookup"><span data-stu-id="6bf02-109">The number of coordinates per vertex.</span></span> <span data-ttu-id="6bf02-110">O valor do *tamanho* deve ser 2, 3 ou 4.</span><span class="sxs-lookup"><span data-stu-id="6bf02-110">The value of *size* must be 2, 3, or 4.</span></span>

</dd> <dt>

<span data-ttu-id="6bf02-111">*tipo*</span><span class="sxs-lookup"><span data-stu-id="6bf02-111">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="6bf02-112">O tipo de dados de cada coordenada na matriz usando as seguintes constantes simbólicas: GL \_ short, GL \_ int, GL \_ float e GL \_ Double.</span><span class="sxs-lookup"><span data-stu-id="6bf02-112">The data type of each coordinate in the array using the following symbolic constants: GL\_SHORT, GL\_INT, GL\_FLOAT, and GL\_DOUBLE.</span></span>

</dd> <dt>

<span data-ttu-id="6bf02-113">*Stride*</span><span class="sxs-lookup"><span data-stu-id="6bf02-113">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="6bf02-114">O deslocamento de bytes entre vértices consecutivos.</span><span class="sxs-lookup"><span data-stu-id="6bf02-114">The byte offset between consecutive vertices.</span></span> <span data-ttu-id="6bf02-115">Quando *Stride* é zero, os vértices são totalmente empacotados na matriz.</span><span class="sxs-lookup"><span data-stu-id="6bf02-115">When *stride* is zero, the vertices are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="6bf02-116">*ponteiro*</span><span class="sxs-lookup"><span data-stu-id="6bf02-116">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="6bf02-117">Um ponteiro para a primeira coordenada do primeiro vértice na matriz.</span><span class="sxs-lookup"><span data-stu-id="6bf02-117">A pointer to the first coordinate of the first vertex in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bf02-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6bf02-118">Return value</span></span>

<span data-ttu-id="6bf02-119">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6bf02-119">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6bf02-120">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="6bf02-120">Error codes</span></span>

<span data-ttu-id="6bf02-121">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="6bf02-121">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="6bf02-122">Nome</span><span class="sxs-lookup"><span data-stu-id="6bf02-122">Name</span></span>                                                                                              | <span data-ttu-id="6bf02-123">Significado</span><span class="sxs-lookup"><span data-stu-id="6bf02-123">Meaning</span></span>                                       |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="6bf02-124"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6bf02-124"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="6bf02-125">o *tamanho* não era 2, 3 ou 4.</span><span class="sxs-lookup"><span data-stu-id="6bf02-125">*size* was not 2, 3, or 4.</span></span> <br/>        |
| <dl> <span data-ttu-id="6bf02-126"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="6bf02-126"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="6bf02-127">o *tipo* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="6bf02-127">*type* was not an accepted value.</span></span><br/>  |
| <dl> <span data-ttu-id="6bf02-128"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6bf02-128"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="6bf02-129">*Stride* ou *Count* era negativo.</span><span class="sxs-lookup"><span data-stu-id="6bf02-129">*stride* or *count* was negative.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="6bf02-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="6bf02-130">Remarks</span></span>

<span data-ttu-id="6bf02-131">A função **glVertexPointer** especifica o local e os dados de uma matriz de coordenadas de vértice a ser usada durante a renderização.</span><span class="sxs-lookup"><span data-stu-id="6bf02-131">The **glVertexPointer** function specifies the location and data of an array of vertex coordinates to use when rendering.</span></span> <span data-ttu-id="6bf02-132">O parâmetro *size* especifica o número de coordenadas por vértice.</span><span class="sxs-lookup"><span data-stu-id="6bf02-132">The *size* parameter specifies the number of coordinates per vertex.</span></span> <span data-ttu-id="6bf02-133">O parâmetro de *tipo* especifica o tipo de dados de cada coordenada de vértice.</span><span class="sxs-lookup"><span data-stu-id="6bf02-133">The *type* parameter specifies the data type of each vertex coordinate.</span></span> <span data-ttu-id="6bf02-134">O parâmetro *Stride* determina o deslocamento de bytes de um vértice para o próximo, habilitando a embalagem de vértices e atributos em uma única matriz ou armazenamento em matrizes separadas.</span><span class="sxs-lookup"><span data-stu-id="6bf02-134">The *stride* parameter determines the byte offset from one vertex to the next, enabling the packing of vertices and attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="6bf02-135">Em algumas implementações, armazenar os vértices e atributos em uma única matriz pode ser mais eficiente do que usar matrizes separadas (consulte [**glInterleavedArrays**](glinterleavedarrays.md)).</span><span class="sxs-lookup"><span data-stu-id="6bf02-135">In some implementations, storing the vertices and attributes in a single array can be more efficient than using separate arrays (see [**glInterleavedArrays**](glinterleavedarrays.md)).</span></span>

<span data-ttu-id="6bf02-136">Uma matriz de vértice é habilitada quando você especifica a \_ constante de matriz de vértice GL \_ com [**glEnableClientState**](glenableclientstate.md).</span><span class="sxs-lookup"><span data-stu-id="6bf02-136">A vertex array is enabled when you specify the GL\_VERTEX\_ARRAY constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="6bf02-137">Quando habilitado, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md)e [**glArrayElement**](glarrayelement.md) usam a matriz de vértice.</span><span class="sxs-lookup"><span data-stu-id="6bf02-137">When enabled, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md), and [**glArrayElement**](glarrayelement.md) use the vertex array.</span></span> <span data-ttu-id="6bf02-138">Por padrão, a matriz de vértices está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="6bf02-138">By default, the vertex array is disabled.</span></span>

<span data-ttu-id="6bf02-139">Você não pode incluir **glVertexPointer** em listas de exibição.</span><span class="sxs-lookup"><span data-stu-id="6bf02-139">You cannot include **glVertexPointer** in display lists.</span></span>

<span data-ttu-id="6bf02-140">Quando você especifica uma matriz de vértice usando **glVertexPointer**, os valores de todos os parâmetros de matriz de vértice da função são salvos em um estado do lado do cliente e os elementos estáticos da matriz podem ser armazenados em cache.</span><span class="sxs-lookup"><span data-stu-id="6bf02-140">When you specify a vertex array using **glVertexPointer**, the values of all the function's vertex array parameters are saved in a client-side state, and static array elements can be cached.</span></span> <span data-ttu-id="6bf02-141">Como os parâmetros de matriz de vértice são um estado do lado do cliente, seus valores não são salvos nem restaurados por [**glPushAttrib**](glpushattrib.md) e **glPopAttrib**.</span><span class="sxs-lookup"><span data-stu-id="6bf02-141">Because the vertex array parameters are client-side state, their values are not saved or restored by [**glPushAttrib**](glpushattrib.md) and **glPopAttrib**.</span></span>

<span data-ttu-id="6bf02-142">Embora nenhum erro seja gerado se você chamar **glVertexPointer** nos pares [**glBegin**](glbegin.md) e [**glEnd**](glend.md) , os resultados serão indefinidos.</span><span class="sxs-lookup"><span data-stu-id="6bf02-142">Although no error is generated if you call **glVertexPointer** within [**glBegin**](glbegin.md) and [**glEnd**](glend.md) pairs, the results are undefined.</span></span>

<span data-ttu-id="6bf02-143">As funções a seguir recuperam informações relacionadas ao **glVertexPointer**:</span><span class="sxs-lookup"><span data-stu-id="6bf02-143">The following functions retrieve information related to **glVertexPointer**:</span></span>

<span data-ttu-id="6bf02-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ tamanho da \_ matriz de vértice GL do argumento \_</span><span class="sxs-lookup"><span data-stu-id="6bf02-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_VERTEX\_ARRAY\_SIZE</span></span>

<span data-ttu-id="6bf02-145">**glGet** com Stride de \_ matriz de vértice do Argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="6bf02-145">**glGet** with argument GL\_VERTEX\_ARRAY\_STRIDE</span></span>

<span data-ttu-id="6bf02-146"> \_ \_ contagem de matrizes de vértice glGet com Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="6bf02-146">**glGet** with argument GL\_VERTEX\_ARRAY\_COUNT</span></span>

<span data-ttu-id="6bf02-147">**glGet** com tipo de \_ matriz de vértice GL do argumento \_ \_</span><span class="sxs-lookup"><span data-stu-id="6bf02-147">**glGet** with argument GL\_VERTEX\_ARRAY\_TYPE</span></span>

<span data-ttu-id="6bf02-148">[](glgetpointerv.md) ponteiro de matriz de vértice glGetPointerv com Argument GL \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="6bf02-148">[**glGetPointerv**](glgetpointerv.md) with argument GL\_VERTEX\_ARRAY\_POINTER</span></span>

<span data-ttu-id="6bf02-149">[**glIsEnabled**](glisenabled.md) com matriz de vértice do Argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="6bf02-149">[**glIsEnabled**](glisenabled.md) with argument GL\_VERTEX\_ARRAY</span></span>

## <a name="requirements"></a><span data-ttu-id="6bf02-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6bf02-150">Requirements</span></span>



| <span data-ttu-id="6bf02-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bf02-151">Requirement</span></span> | <span data-ttu-id="6bf02-152">Valor</span><span class="sxs-lookup"><span data-stu-id="6bf02-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6bf02-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6bf02-153">Minimum supported client</span></span><br/> | <span data-ttu-id="6bf02-154">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6bf02-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6bf02-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6bf02-155">Minimum supported server</span></span><br/> | <span data-ttu-id="6bf02-156">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6bf02-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6bf02-157">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6bf02-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bf02-158"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bf02-158"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6bf02-159">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6bf02-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="6bf02-160"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6bf02-160"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6bf02-161">DLL</span><span class="sxs-lookup"><span data-stu-id="6bf02-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6bf02-162"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6bf02-162"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bf02-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="6bf02-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bf02-164">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="6bf02-164">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="6bf02-165">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="6bf02-165">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="6bf02-166">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="6bf02-166">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="6bf02-167">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="6bf02-167">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="6bf02-168">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="6bf02-168">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="6bf02-169">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="6bf02-169">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="6bf02-170">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="6bf02-170">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="6bf02-171">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="6bf02-171">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="6bf02-172">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="6bf02-172">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="6bf02-173">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="6bf02-173">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="6bf02-174">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="6bf02-174">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> </dl>

 

 





