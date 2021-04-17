---
title: função glTexCoordPointer (GL. h)
description: A função glTexCoordPointer define uma matriz de coordenadas de textura.
ms.assetid: c3640a1b-ccc7-4f1a-94a5-a164f7377dbc
keywords:
- função glTexCoordPointer OpenGL
topic_type:
- apiref
api_name:
- glTexCoordPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: febc9c79bdbc4a1ed1c14380af47f36309f12662
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105780189"
---
# <a name="gltexcoordpointer-function"></a><span data-ttu-id="1091c-104">função glTexCoordPointer</span><span class="sxs-lookup"><span data-stu-id="1091c-104">glTexCoordPointer function</span></span>

<span data-ttu-id="1091c-105">A função **glTexCoordPointer** define uma matriz de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="1091c-105">The **glTexCoordPointer** function defines an array of texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="1091c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1091c-106">Syntax</span></span>


```C++
void WINAPI glTexCoordPointer(
         GLint   size,
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="1091c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1091c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1091c-108">*size*</span><span class="sxs-lookup"><span data-stu-id="1091c-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="1091c-109">O número de coordenadas por elemento de matriz.</span><span class="sxs-lookup"><span data-stu-id="1091c-109">The number of coordinates per array element.</span></span> <span data-ttu-id="1091c-110">O valor do *tamanho* deve ser 1, 2, 3 ou 4.</span><span class="sxs-lookup"><span data-stu-id="1091c-110">The value of *size* must be 1, 2, 3, or 4.</span></span>

</dd> <dt>

<span data-ttu-id="1091c-111">*tipo*</span><span class="sxs-lookup"><span data-stu-id="1091c-111">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="1091c-112">O tipo de dados de cada coordenada de textura na matriz usando as seguintes constantes simbólicas: **GL \_ Short**, **GL \_ int**, **GL \_ float** e **GL \_ Double**.</span><span class="sxs-lookup"><span data-stu-id="1091c-112">The data type of each texture coordinate in the array using the following symbolic constants: **GL\_SHORT**, **GL\_INT**, **GL\_FLOAT**, and **GL\_DOUBLE**.</span></span>

</dd> <dt>

<span data-ttu-id="1091c-113">*Stride*</span><span class="sxs-lookup"><span data-stu-id="1091c-113">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="1091c-114">O deslocamento de bytes entre elementos de matriz consecutivos.</span><span class="sxs-lookup"><span data-stu-id="1091c-114">The byte offset between consecutive array elements.</span></span> <span data-ttu-id="1091c-115">Quando *Stride* é zero, os elementos da matriz são totalmente empacotados na matriz.</span><span class="sxs-lookup"><span data-stu-id="1091c-115">When *stride* is zero, the array elements are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="1091c-116">*ponteiro*</span><span class="sxs-lookup"><span data-stu-id="1091c-116">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="1091c-117">Um ponteiro para a primeira coordenada do primeiro elemento na matriz.</span><span class="sxs-lookup"><span data-stu-id="1091c-117">A pointer to the first coordinate of the first element in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1091c-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1091c-118">Return value</span></span>

<span data-ttu-id="1091c-119">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1091c-119">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1091c-120">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="1091c-120">Error codes</span></span>

<span data-ttu-id="1091c-121">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="1091c-121">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="1091c-122">Nome</span><span class="sxs-lookup"><span data-stu-id="1091c-122">Name</span></span>                                                                                              | <span data-ttu-id="1091c-123">Significado</span><span class="sxs-lookup"><span data-stu-id="1091c-123">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="1091c-124"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="1091c-124"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="1091c-125">o *tipo* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="1091c-125">*type* was not an accepted value.</span></span><br/> |
| <dl> <span data-ttu-id="1091c-126"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1091c-126"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="1091c-127">o *tamanho* não era 1, 2, 3 ou 4.</span><span class="sxs-lookup"><span data-stu-id="1091c-127">*size* was not 1, 2, 3, or 4.</span></span><br/>     |
| <dl> <span data-ttu-id="1091c-128"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1091c-128"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="1091c-129">o *Stride* era negativo.</span><span class="sxs-lookup"><span data-stu-id="1091c-129">*stride* was negative.</span></span><br/>            |



## <a name="remarks"></a><span data-ttu-id="1091c-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="1091c-130">Remarks</span></span>

<span data-ttu-id="1091c-131">A função **glTexCoordPointer** especifica o local e os dados de uma matriz de coordenadas de textura a serem usadas durante a renderização. O parâmetro *size* especifica o número de coordenadas usadas para cada elemento da matriz. O parâmetro de *tipo* especifica o tipo de dados de cada coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="1091c-131">The **glTexCoordPointer** function specifies the location and data of an array of texture coordinates to use when rendering.The *size* parameter specifies the number of coordinates used for each element of the array.The *type* parameter specifies the data type of each texture coordinate.</span></span> <span data-ttu-id="1091c-132">O parâmetro *Stride* determina o deslocamento de bytes de um elemento de matriz para o seguinte, habilitando a embalagem de vértices e atributos em uma única matriz ou armazenamento em matrizes separadas.</span><span class="sxs-lookup"><span data-stu-id="1091c-132">The *stride* parameter determines the byte offset from one array element to the next, enabling the packing of vertices and attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="1091c-133">Em algumas implementações, armazenar os vértices e os atributos em uma única matriz pode ser mais eficiente do que usar matrizes separadas.</span><span class="sxs-lookup"><span data-stu-id="1091c-133">In some implementations, storing the vertices and attributes in a single array can be more efficient than using separate arrays.</span></span> <span data-ttu-id="1091c-134">Para obter mais informações, consulte [**glInterleavedArrays**](glinterleavedarrays.md).</span><span class="sxs-lookup"><span data-stu-id="1091c-134">For more information, see [**glInterleavedArrays**](glinterleavedarrays.md).</span></span> <span data-ttu-id="1091c-135">Quando uma matriz de coordenadas de textura é especificada, o tamanho, o tipo, o Stride e o ponteiro são salvos no estado do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="1091c-135">When a texture coordinate array is specified, size, type, stride, and pointer are saved client-side state.</span></span>

<span data-ttu-id="1091c-136">Uma matriz de coordenadas de textura é habilitada quando você especifica a constante de **\_ \_ \_ matriz coord de textura GL** com [**glEnableClientState**](glenableclientstate.md).</span><span class="sxs-lookup"><span data-stu-id="1091c-136">A texture coordinate array is enabled when you specify the **GL\_TEXTURE\_COORD\_ARRAY** constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="1091c-137">Quando habilitado, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md)e [**glArrayElement**](glarrayelement.md) usam a matriz de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="1091c-137">When enabled, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md), and [**glArrayElement**](glarrayelement.md) use the texture coordinate array.</span></span> <span data-ttu-id="1091c-138">Por padrão, a matriz de coordenadas de textura está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="1091c-138">By default the texture coordinate array is disabled.</span></span>

<span data-ttu-id="1091c-139">Você não pode incluir **glTexCoordPointer** em listas de exibição.</span><span class="sxs-lookup"><span data-stu-id="1091c-139">You cannot include **glTexCoordPointer** in display lists.</span></span>

<span data-ttu-id="1091c-140">Quando você especifica uma matriz de coordenadas de textura usando **glTexCoordPointer**, os valores de todos os parâmetros de matriz de coordenadas de textura da função são salvos em um estado do lado do cliente e os elementos estáticos da matriz podem ser armazenados em cache.</span><span class="sxs-lookup"><span data-stu-id="1091c-140">When you specify a texture coordinate array using **glTexCoordPointer**, the values of all the function's texture coordinate array parameters are saved in a client-side state, and static array elements can be cached.</span></span> <span data-ttu-id="1091c-141">Como os parâmetros da matriz de coordenadas de textura são o estado do lado do cliente, seus valores não são salvos nem restaurados por [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="1091c-141">Because the texture coordinate array parameters are client-side state, their values are not saved or restored by [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md).</span></span>

<span data-ttu-id="1091c-142">Embora nenhum erro seja gerado quando você chama **glTexCoordPointer** nos pares [**glBegin**](glbegin.md) e [**glEnd**](glend.md) , os resultados são indefinidos.</span><span class="sxs-lookup"><span data-stu-id="1091c-142">Although no error is generated when you call **glTexCoordPointer** within [**glBegin**](glbegin.md) and [**glEnd**](glend.md) pairs, the results are undefined.</span></span>

<span data-ttu-id="1091c-143">As funções a seguir recuperam informações relacionadas ao **glTexCoordPointer**:</span><span class="sxs-lookup"><span data-stu-id="1091c-143">The following functions retrieve information related to **glTexCoordPointer**:</span></span>

<span data-ttu-id="1091c-144">[**glIsEnabled**](glisenabled.md) com a **\_ \_ \_ matriz coord de textura Argument GL**</span><span class="sxs-lookup"><span data-stu-id="1091c-144">[**glIsEnabled**](glisenabled.md) with argument **GL\_TEXTURE\_COORD\_ARRAY**</span></span>

<span data-ttu-id="1091c-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com Argument **GL \_ textura \_ coord da \_ matriz \_ tamanho**</span><span class="sxs-lookup"><span data-stu-id="1091c-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument **GL\_TEXTURE\_COORD\_ARRAY\_SIZE**</span></span>

<span data-ttu-id="1091c-146">**glGet** with argumento **GL \_ Texture \_ coord \_ array \_ Stride**</span><span class="sxs-lookup"><span data-stu-id="1091c-146">**glGet** with argument **GL\_TEXTURE\_COORD\_ARRAY\_STRIDE**</span></span>

<span data-ttu-id="1091c-147"> **\_ \_ \_ \_ contagem de matrizes de coord de textura** glGet com Argument GL</span><span class="sxs-lookup"><span data-stu-id="1091c-147">**glGet** with argument **GL\_TEXTURE\_COORD\_ARRAY\_COUNT**</span></span>

<span data-ttu-id="1091c-148">**glGet** com o **\_ tipo de \_ \_ matriz coord \_ de textura Argument GL**</span><span class="sxs-lookup"><span data-stu-id="1091c-148">**glGet** with argument **GL\_TEXTURE\_COORD\_ARRAY\_TYPE**</span></span>

<span data-ttu-id="1091c-149">[](glgetpointerv.md) **\_ \_ \_ \_ ponteiro de matriz coord de textura** glGetPointerv com Argument GL</span><span class="sxs-lookup"><span data-stu-id="1091c-149">[**glGetPointerv**](glgetpointerv.md) with argument **GL\_TEXTURE\_COORD\_ARRAY\_POINTER**</span></span>

## <a name="requirements"></a><span data-ttu-id="1091c-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1091c-150">Requirements</span></span>



| <span data-ttu-id="1091c-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="1091c-151">Requirement</span></span> | <span data-ttu-id="1091c-152">Valor</span><span class="sxs-lookup"><span data-stu-id="1091c-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1091c-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1091c-153">Minimum supported client</span></span><br/> | <span data-ttu-id="1091c-154">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1091c-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1091c-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1091c-155">Minimum supported server</span></span><br/> | <span data-ttu-id="1091c-156">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1091c-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1091c-157">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1091c-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="1091c-158"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="1091c-158"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1091c-159">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1091c-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="1091c-160"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1091c-160"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1091c-161">DLL</span><span class="sxs-lookup"><span data-stu-id="1091c-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1091c-162"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1091c-162"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1091c-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="1091c-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1091c-164">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="1091c-164">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="1091c-165">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="1091c-165">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="1091c-166">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="1091c-166">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="1091c-167">**glDrawElements**</span><span class="sxs-lookup"><span data-stu-id="1091c-167">**glDrawElements**</span></span>](gldrawelements.md)
</dt> <dt>

[<span data-ttu-id="1091c-168">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="1091c-168">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="1091c-169">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="1091c-169">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="1091c-170">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="1091c-170">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="1091c-171">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="1091c-171">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="1091c-172">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="1091c-172">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="1091c-173">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="1091c-173">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="1091c-174">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="1091c-174">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="1091c-175">**glPopClientAttrib**</span><span class="sxs-lookup"><span data-stu-id="1091c-175">**glPopClientAttrib**</span></span>](glpopclientattrib.md)
</dt> <dt>

[<span data-ttu-id="1091c-176">**glPushClientAttrib**</span><span class="sxs-lookup"><span data-stu-id="1091c-176">**glPushClientAttrib**</span></span>](glpushclientattrib.md)
</dt> <dt>

[<span data-ttu-id="1091c-177">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="1091c-177">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="1091c-178">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="1091c-178">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





