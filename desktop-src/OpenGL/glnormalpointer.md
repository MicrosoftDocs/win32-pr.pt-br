---
title: função glNormalPointer (GL. h)
description: A função glNormalPointer define uma matriz de Normals.
ms.assetid: 6ffb0522-87cc-4be1-a5b1-f6fd30e04b43
keywords:
- função glNormalPointer OpenGL
topic_type:
- apiref
api_name:
- glNormalPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c2f3abbfbd989351af647557ec64f8ee3172dc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919188"
---
# <a name="glnormalpointer-function"></a><span data-ttu-id="986a4-104">função glNormalPointer</span><span class="sxs-lookup"><span data-stu-id="986a4-104">glNormalPointer function</span></span>

<span data-ttu-id="986a4-105">A função **glNormalPointer** define uma matriz de Normals.</span><span class="sxs-lookup"><span data-stu-id="986a4-105">The **glNormalPointer** function defines an array of normals.</span></span>

## <a name="syntax"></a><span data-ttu-id="986a4-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="986a4-106">Syntax</span></span>


```C++
void WINAPI glNormalPointer(
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="986a4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="986a4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="986a4-108">*tipo*</span><span class="sxs-lookup"><span data-stu-id="986a4-108">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="986a4-109">O tipo de dados de cada coordenada na matriz usando as seguintes constantes simbólicas: GL \_ byte, GL \_ short, GL \_ int, GL \_ float e GL \_ Double.</span><span class="sxs-lookup"><span data-stu-id="986a4-109">The data type of each coordinate in the array using the following symbolic constants: GL\_BYTE, GL\_SHORT, GL\_INT, GL\_FLOAT, and GL\_DOUBLE.</span></span>

</dd> <dt>

<span data-ttu-id="986a4-110">*Stride*</span><span class="sxs-lookup"><span data-stu-id="986a4-110">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="986a4-111">O deslocamento de byte entre os Normals consecutivos.</span><span class="sxs-lookup"><span data-stu-id="986a4-111">The byte offset between consecutive normals.</span></span> <span data-ttu-id="986a4-112">Quando *Stride* é zero, os normais são empacotados rigidamente na matriz.</span><span class="sxs-lookup"><span data-stu-id="986a4-112">When *stride* is zero, the normals are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="986a4-113">*ponteiro*</span><span class="sxs-lookup"><span data-stu-id="986a4-113">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="986a4-114">Um ponteiro para o primeiro normal na matriz.</span><span class="sxs-lookup"><span data-stu-id="986a4-114">A pointer to the first normal in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="986a4-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="986a4-115">Return value</span></span>

<span data-ttu-id="986a4-116">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="986a4-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="986a4-117">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="986a4-117">Error codes</span></span>

<span data-ttu-id="986a4-118">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="986a4-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="986a4-119">Nome</span><span class="sxs-lookup"><span data-stu-id="986a4-119">Name</span></span>                                                                                                  | <span data-ttu-id="986a4-120">Significado</span><span class="sxs-lookup"><span data-stu-id="986a4-120">Meaning</span></span>                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="986a4-121"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="986a4-121"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="986a4-122">o *tipo* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="986a4-122">*type* was not an accepted value.</span></span><br/> |
| <dl> <span data-ttu-id="986a4-123"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="986a4-123"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="986a4-124">*Stride* ou *Count* era negativo.</span><span class="sxs-lookup"><span data-stu-id="986a4-124">*stride* or *count* was negative.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="986a4-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="986a4-125">Remarks</span></span>

<span data-ttu-id="986a4-126">A função **glNormalPointer** especifica o local e os dados de uma matriz de Normals a serem usados durante a renderização.</span><span class="sxs-lookup"><span data-stu-id="986a4-126">The **glNormalPointer** function specifies the location and data of an array of normals to use when rendering.</span></span> <span data-ttu-id="986a4-127">O parâmetro de *tipo* especifica o tipo de dados de cada coordenada normal.</span><span class="sxs-lookup"><span data-stu-id="986a4-127">The *type* parameter specifies the data type of each normal coordinate.</span></span> <span data-ttu-id="986a4-128">O parâmetro *Stride* determina o deslocamento de bytes de um normal para o próximo, habilitando a embalagem de vértices e atributos em uma única matriz ou armazenamento em matrizes separadas.</span><span class="sxs-lookup"><span data-stu-id="986a4-128">The *stride* parameter determines the byte offset from one normal to the next, enabling the packing of vertices and attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="986a4-129">Em algumas implementações, armazenar os vértices e os atributos em uma única matriz pode ser mais eficiente do que usar matrizes separadas; consulte [**glInterleavedArrays**](glinterleavedarrays.md) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="986a4-129">In some implementations storing the vertices and attributes in a single array can be more efficient than using separate arrays; see [**glInterleavedArrays**](glinterleavedarrays.md) for details.</span></span>

<span data-ttu-id="986a4-130">Uma matriz normal é habilitada quando você especifica a \_ constante de matriz do GL normal \_ com [**glEnableClientState**](glenableclientstate.md).</span><span class="sxs-lookup"><span data-stu-id="986a4-130">A normal array is enabled when you specify the GL\_NORMAL\_ARRAY constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="986a4-131">Quando habilitado, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md) e [**glArrayElement**](glarrayelement.md) usam a matriz normal.</span><span class="sxs-lookup"><span data-stu-id="986a4-131">When enabled, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md) and [**glArrayElement**](glarrayelement.md) use the normal array.</span></span> <span data-ttu-id="986a4-132">Por padrão, a matriz normal está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="986a4-132">By default the normal array is disabled.</span></span>

<span data-ttu-id="986a4-133">Você não pode incluir **glNormalPointer** em listas de exibição.</span><span class="sxs-lookup"><span data-stu-id="986a4-133">You cannot include **glNormalPointer** in display lists.</span></span>

<span data-ttu-id="986a4-134">Quando você especifica uma matriz normal usando **glNormalPointer**, os valores de todos os parâmetros de matriz normais da função são salvos em um estado do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="986a4-134">When you specify a normal array using **glNormalPointer**, the values of all the function's normal array parameters are saved in a client-side state.</span></span> <span data-ttu-id="986a4-135">Como os parâmetros de matriz normais são salvos em um estado do lado do cliente, seus valores não são salvos nem restaurados por [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="986a4-135">Because the normal array parameters are saved in a client-side state, their values are not saved or restored by [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md).</span></span>

<span data-ttu-id="986a4-136">Embora nenhum erro seja gerado quando você chama **glNormalPointer** nos pares [**glBegin**](glbegin.md) e [**glEnd**](glend.md) , os resultados são indefinidos.</span><span class="sxs-lookup"><span data-stu-id="986a4-136">Although no error is generated when you call **glNormalPointer** within [**glBegin**](glbegin.md) and [**glEnd**](glend.md) pairs, the results are undefined.</span></span>

<span data-ttu-id="986a4-137">As funções a seguir estão associadas a **glNormalPointer**:</span><span class="sxs-lookup"><span data-stu-id="986a4-137">The following functions are associated with **glNormalPointer**:</span></span>

<span data-ttu-id="986a4-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL a \_ \_ matriz normal \_ Stride</span><span class="sxs-lookup"><span data-stu-id="986a4-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NORMAL\_ARRAY\_STRIDE</span></span>

<span data-ttu-id="986a4-139"> \_ \_ contagem de matrizes glGet com Argument GL normal \_</span><span class="sxs-lookup"><span data-stu-id="986a4-139">**glGet** with argument GL\_NORMAL\_ARRAY\_COUNT</span></span>

<span data-ttu-id="986a4-140">**glGet** com o argumento \_ GL \_ normal \_ tipo de matriz</span><span class="sxs-lookup"><span data-stu-id="986a4-140">**glGet** with argument GL\_NORMAL\_ARRAY\_TYPE</span></span>

<span data-ttu-id="986a4-141"> \_ \_ ponteiro de matriz normal glGetPointerv com Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="986a4-141">**glGetPointerv** with argument GL\_NORMAL\_ARRAY\_POINTER</span></span>

<span data-ttu-id="986a4-142">[**glIsEnabled**](glisenabled.md) com o Argument GL \_ normal \_ array</span><span class="sxs-lookup"><span data-stu-id="986a4-142">[**glIsEnabled**](glisenabled.md) with argument GL\_NORMAL\_ARRAY</span></span>

## <a name="requirements"></a><span data-ttu-id="986a4-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="986a4-143">Requirements</span></span>



| <span data-ttu-id="986a4-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="986a4-144">Requirement</span></span> | <span data-ttu-id="986a4-145">Valor</span><span class="sxs-lookup"><span data-stu-id="986a4-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="986a4-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="986a4-146">Minimum supported client</span></span><br/> | <span data-ttu-id="986a4-147">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="986a4-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="986a4-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="986a4-148">Minimum supported server</span></span><br/> | <span data-ttu-id="986a4-149">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="986a4-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="986a4-150">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="986a4-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="986a4-151"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="986a4-151"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="986a4-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="986a4-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="986a4-153"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="986a4-153"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="986a4-154">DLL</span><span class="sxs-lookup"><span data-stu-id="986a4-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="986a4-155"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="986a4-155"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="986a4-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="986a4-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="986a4-157">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="986a4-157">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="986a4-158">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="986a4-158">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="986a4-159">**glDrawElements**</span><span class="sxs-lookup"><span data-stu-id="986a4-159">**glDrawElements**</span></span>](gldrawelements.md)
</dt> <dt>

[<span data-ttu-id="986a4-160">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="986a4-160">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="986a4-161">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="986a4-161">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="986a4-162">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="986a4-162">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="986a4-163">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="986a4-163">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="986a4-164">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="986a4-164">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="986a4-165">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="986a4-165">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="986a4-166">**glInterleavedArrays**</span><span class="sxs-lookup"><span data-stu-id="986a4-166">**glInterleavedArrays**</span></span>](glinterleavedarrays.md)
</dt> <dt>

[<span data-ttu-id="986a4-167">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="986a4-167">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="986a4-168">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="986a4-168">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> <dt>

[<span data-ttu-id="986a4-169">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="986a4-169">**glGetString**</span></span>](glgetstring.md)
</dt> </dl>

 

 





