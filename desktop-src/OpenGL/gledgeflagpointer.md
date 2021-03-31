---
title: função glEdgeFlagPointer (GL. h)
description: A função glEdgeFlagPointer define uma matriz de sinalizadores de borda.
ms.assetid: e0e7e442-533d-4c41-addd-a215ce0b1c56
keywords:
- função glEdgeFlagPointer OpenGL
topic_type:
- apiref
api_name:
- glEdgeFlagPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4390a9838fef418763aa4bcafbf815ab0cdf3466
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644826"
---
# <a name="gledgeflagpointer-function"></a><span data-ttu-id="3bebd-104">função glEdgeFlagPointer</span><span class="sxs-lookup"><span data-stu-id="3bebd-104">glEdgeFlagPointer function</span></span>

<span data-ttu-id="3bebd-105">A função **glEdgeFlagPointer** define uma matriz de sinalizadores de borda.</span><span class="sxs-lookup"><span data-stu-id="3bebd-105">The **glEdgeFlagPointer** function defines an array of edge flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bebd-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3bebd-106">Syntax</span></span>


```C++
void WINAPI glEdgeFlagPointer(
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="3bebd-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3bebd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bebd-108">*Stride*</span><span class="sxs-lookup"><span data-stu-id="3bebd-108">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="3bebd-109">O deslocamento de byte entre sinalizadores de borda consecutivos.</span><span class="sxs-lookup"><span data-stu-id="3bebd-109">The byte offset between consecutive edge flags.</span></span> <span data-ttu-id="3bebd-110">Quando *Stride* é zero, os sinalizadores de borda são totalmente empacotados na matriz.</span><span class="sxs-lookup"><span data-stu-id="3bebd-110">When *stride* is zero, the edge flags are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="3bebd-111">*ponteiro*</span><span class="sxs-lookup"><span data-stu-id="3bebd-111">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="3bebd-112">Um ponteiro para o primeiro sinalizador de borda na matriz.</span><span class="sxs-lookup"><span data-stu-id="3bebd-112">A pointer to the first edge flag in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bebd-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3bebd-113">Return value</span></span>

<span data-ttu-id="3bebd-114">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3bebd-114">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3bebd-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="3bebd-115">Error codes</span></span>

<span data-ttu-id="3bebd-116">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="3bebd-116">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="3bebd-117">Nome</span><span class="sxs-lookup"><span data-stu-id="3bebd-117">Name</span></span>                                                                                             | <span data-ttu-id="3bebd-118">Significado</span><span class="sxs-lookup"><span data-stu-id="3bebd-118">Meaning</span></span>                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="3bebd-119"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="3bebd-119"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl> | <span data-ttu-id="3bebd-120">*Stride* ou *Count* era negativo.</span><span class="sxs-lookup"><span data-stu-id="3bebd-120">*stride* or *count* was negative.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3bebd-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="3bebd-121">Remarks</span></span>

<span data-ttu-id="3bebd-122">A função **glEdgeFlagPointer** especifica o local e os dados de uma matriz de sinalizadores de borda boolianos a serem usados durante a renderização.</span><span class="sxs-lookup"><span data-stu-id="3bebd-122">The **glEdgeFlagPointer** function specifies the location and data of an array of Boolean edge flags to use when rendering.</span></span> <span data-ttu-id="3bebd-123">O parâmetro *Stride* determina o deslocamento de bytes de um sinalizador de borda para o próximo, que habilita a embalagem de vértices e atributos em uma única matriz ou armazenamento em matrizes separadas.</span><span class="sxs-lookup"><span data-stu-id="3bebd-123">The *stride* parameter determines the byte offset from one edge flag to the next, which enables the packing of vertices and attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="3bebd-124">Em algumas implementações, armazenar os vértices e os atributos em uma única matriz pode ser mais eficiente do que usar matrizes separadas.</span><span class="sxs-lookup"><span data-stu-id="3bebd-124">In some implementations, storing the vertices and attributes in a single array can be more efficient than using separate arrays.</span></span>

<span data-ttu-id="3bebd-125">Uma matriz de sinalizador de borda é habilitada quando você especifica a \_ constante de matriz do sinalizador de borda GL \_ \_ com [**glEnableClientState**](glenableclientstate.md).</span><span class="sxs-lookup"><span data-stu-id="3bebd-125">An edge-flag array is enabled when you specify the GL\_EDGE\_FLAG\_ARRAY constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="3bebd-126">Quando habilitado, [**glDrawArrays**](gldrawarrays.md) ou [**glArrayElement**](glarrayelement.md) usa a matriz de sinalizador de borda.</span><span class="sxs-lookup"><span data-stu-id="3bebd-126">When enabled, [**glDrawArrays**](gldrawarrays.md) or [**glArrayElement**](glarrayelement.md) uses the edge-flag array.</span></span> <span data-ttu-id="3bebd-127">Por padrão, a matriz de sinalizador de borda é desabilitada.</span><span class="sxs-lookup"><span data-stu-id="3bebd-127">By default the edge-flag array is disabled.</span></span>

<span data-ttu-id="3bebd-128">Use **glDrawArrays** para construir uma sequência de primitivos (todos do mesmo tipo) de um vértice predefinido e matrizes de atributo de vértice.</span><span class="sxs-lookup"><span data-stu-id="3bebd-128">Use **glDrawArrays** to construct a sequence of primitives (all of the same type) from prespecified vertex and vertex attribute arrays.</span></span> <span data-ttu-id="3bebd-129">Use **glArrayElement** para especificar primitivos indexando vértices e atributos de vértice, e [**glDrawElements**](gldrawelements.md) para construir uma sequência de primitivos indexando vértices e atributos de vértice.</span><span class="sxs-lookup"><span data-stu-id="3bebd-129">Use **glArrayElement** to specify primitives by indexing vertices and vertex attributes, and [**glDrawElements**](gldrawelements.md) to construct a sequence of primitives by indexing vertices and vertex attributes.</span></span>

<span data-ttu-id="3bebd-130">Você não pode incluir **glEdgeFlagPointer** em listas de exibição.</span><span class="sxs-lookup"><span data-stu-id="3bebd-130">You cannot include **glEdgeFlagPointer** in display lists.</span></span>

<span data-ttu-id="3bebd-131">Quando você especifica uma matriz de sinalizador de borda usando **glEdgeFlagPointer**, os valores de todos os parâmetros de matriz do sinalizador de borda da função são salvos em um estado do lado do cliente e os elementos estáticos da matriz podem ser armazenados em cache.</span><span class="sxs-lookup"><span data-stu-id="3bebd-131">When you specify an edge-flag array using **glEdgeFlagPointer**, the values of all the function's edge-flag array parameters are saved in a client-side state and static array elements can be cached.</span></span> <span data-ttu-id="3bebd-132">Como os parâmetros de matriz de sinalizador de borda estão em um estado do lado do cliente, [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md) não salvam nem restauram seus valores.</span><span class="sxs-lookup"><span data-stu-id="3bebd-132">Because the edge-flag array parameters are in a client-side state, [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) do not save or restore their values.</span></span>

<span data-ttu-id="3bebd-133">Embora chamar **glEdgeFlagPointer** em um par [**glBegin**](glbegin.md) / [**glend**](glend.md) não gere um erro, os resultados são indefinidos.</span><span class="sxs-lookup"><span data-stu-id="3bebd-133">Although calling **glEdgeFlagPointer** within a [**glBegin**](glbegin.md)/[**glend**](glend.md) pair does not generate an error, the results are undefined.</span></span>

<span data-ttu-id="3bebd-134">As funções a seguir recuperam informações relacionadas à função **glEdgeFlagPointer** :</span><span class="sxs-lookup"><span data-stu-id="3bebd-134">The following functions retrieve information related to the **glEdgeFlagPointer** function:</span></span>

<span data-ttu-id="3bebd-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ Edge \_ flag de \_ matriz \_ Stride</span><span class="sxs-lookup"><span data-stu-id="3bebd-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_EDGE\_FLAG\_ARRAY\_STRIDE</span></span>

<span data-ttu-id="3bebd-136"> contagem de matriz de \_ sinalizador de borda GLGET com Argument GL \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="3bebd-136">**glGet** with argument GL\_EDGE\_FLAG\_ARRAY\_COUNT</span></span>

<span data-ttu-id="3bebd-137">[](glgetpointerv.md) ponteiro de matriz do \_ sinalizador de borda GLGETPOINTERV com Argument GL \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="3bebd-137">[**glGetPointerv**](glgetpointerv.md) with argument GL\_EDGE\_FLAG\_ARRAY\_POINTER</span></span>

<span data-ttu-id="3bebd-138">[](glisenabled.md) matriz de sinalizador de borda glIsEnabled com Argument GL \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="3bebd-138">[**glIsEnabled**](glisenabled.md) with argument GL\_EDGE\_FLAG\_ARRAY</span></span>

## <a name="requirements"></a><span data-ttu-id="3bebd-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3bebd-139">Requirements</span></span>



| <span data-ttu-id="3bebd-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bebd-140">Requirement</span></span> | <span data-ttu-id="3bebd-141">Valor</span><span class="sxs-lookup"><span data-stu-id="3bebd-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3bebd-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3bebd-142">Minimum supported client</span></span><br/> | <span data-ttu-id="3bebd-143">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3bebd-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3bebd-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3bebd-144">Minimum supported server</span></span><br/> | <span data-ttu-id="3bebd-145">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3bebd-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3bebd-146">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3bebd-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bebd-147"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bebd-147"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3bebd-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3bebd-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="3bebd-149"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3bebd-149"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3bebd-150">DLL</span><span class="sxs-lookup"><span data-stu-id="3bebd-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3bebd-151"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3bebd-151"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bebd-152">Consulte também</span><span class="sxs-lookup"><span data-stu-id="3bebd-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bebd-153">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="3bebd-153">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="3bebd-154">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="3bebd-154">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3bebd-155">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="3bebd-155">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="3bebd-156">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="3bebd-156">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="3bebd-157">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="3bebd-157">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="3bebd-158">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="3bebd-158">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3bebd-159">**glGet**</span><span class="sxs-lookup"><span data-stu-id="3bebd-159">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="3bebd-160">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="3bebd-160">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="3bebd-161">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="3bebd-161">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="3bebd-162">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="3bebd-162">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="3bebd-163">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="3bebd-163">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="3bebd-164">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="3bebd-164">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="3bebd-165">**glPopAttrib**</span><span class="sxs-lookup"><span data-stu-id="3bebd-165">**glPopAttrib**</span></span>](glpopattrib.md)
</dt> <dt>

[<span data-ttu-id="3bebd-166">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="3bebd-166">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="3bebd-167">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="3bebd-167">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="3bebd-168">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="3bebd-168">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





