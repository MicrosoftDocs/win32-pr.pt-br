---
title: função glInterleavedArrays (GL. h)
description: A função glInterleavedArrays especifica e habilita simultaneamente várias matrizes intercaladas em uma matriz agregada maior.
ms.assetid: f1133949-d755-43e3-bf29-8e4c7fb17980
keywords:
- função glInterleavedArrays OpenGL
topic_type:
- apiref
api_name:
- glInterleavedArrays
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41403210e78d1a65dd700561243846d6e45bad67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369346"
---
# <a name="glinterleavedarrays-function"></a><span data-ttu-id="96161-104">função glInterleavedArrays</span><span class="sxs-lookup"><span data-stu-id="96161-104">glInterleavedArrays function</span></span>

<span data-ttu-id="96161-105">A função **glInterleavedArrays** especifica e habilita simultaneamente várias matrizes intercaladas em uma matriz agregada maior.</span><span class="sxs-lookup"><span data-stu-id="96161-105">The **glInterleavedArrays** function simultaneously specifies and enables several interleaved arrays in a larger aggregate array.</span></span>

## <a name="syntax"></a><span data-ttu-id="96161-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="96161-106">Syntax</span></span>


```C++
void WINAPI glInterleavedArrays(
         GLenum  format,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="96161-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96161-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96161-108">*format*</span><span class="sxs-lookup"><span data-stu-id="96161-108">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="96161-109">O tipo de matriz a ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="96161-109">The type of array to enable.</span></span> <span data-ttu-id="96161-110">O parâmetro pode assumir um dos seguintes valores simbólicos: GL \_ V2F, GL \_ V3F, GL \_ C4UB \_ V2F, GL \_ C4UB \_ V3F, GL \_ C3F \_ V3F, GL \_ N3F \_ V3F, GL \_ C4F N3F V3F \_ \_ , GL \_ T2F \_ V3F, GL \_ t4f \_ V4F, GL \_ T2F \_ C4UB \_ V3F, GL \_ T2F \_ C3F V3F \_ , GL \_ T2F \_ N3F V3F \_ , GL \_ T2F \_ C4F \_ N3F V3F \_ ou GL \_ t4f \_ \_ \_ C4F N3F V4F.</span><span class="sxs-lookup"><span data-stu-id="96161-110">The parameter can assume one of the following symbolic values: GL\_V2F, GL\_V3F, GL\_C4UB\_V2F, GL\_C4UB\_V3F, GL\_C3F\_V3F, GL\_N3F\_V3F, GL\_C4F\_N3F\_V3F, GL\_T2F\_V3F, GL\_T4F\_V4F, GL\_T2F\_C4UB\_V3F, GL\_T2F\_C3F\_V3F, GL\_T2F\_N3F\_V3F, GL\_T2F\_C4F\_N3F\_V3F, or GL\_T4F\_C4F\_N3F\_V4F.</span></span>

</dd> <dt>

<span data-ttu-id="96161-111">*Stride*</span><span class="sxs-lookup"><span data-stu-id="96161-111">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="96161-112">O deslocamento em bytes entre cada elemento de matriz agregada.</span><span class="sxs-lookup"><span data-stu-id="96161-112">The offset in bytes between each aggregate array element.</span></span>

</dd> <dt>

<span data-ttu-id="96161-113">*ponteiro*</span><span class="sxs-lookup"><span data-stu-id="96161-113">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="96161-114">Um ponteiro para o primeiro elemento de uma matriz de agregação.</span><span class="sxs-lookup"><span data-stu-id="96161-114">A pointer to the first element of an aggregate array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96161-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="96161-115">Return value</span></span>

<span data-ttu-id="96161-116">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="96161-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="96161-117">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="96161-117">Error codes</span></span>

<span data-ttu-id="96161-118">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="96161-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="96161-119">Nome</span><span class="sxs-lookup"><span data-stu-id="96161-119">Name</span></span>                                                                                                  | <span data-ttu-id="96161-120">Significado</span><span class="sxs-lookup"><span data-stu-id="96161-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="96161-121"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="96161-121"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="96161-122">o *formato* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="96161-122">*format* was not an accepted value.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="96161-123"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="96161-123"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="96161-124">*Stride* era um valor negativo.</span><span class="sxs-lookup"><span data-stu-id="96161-124">*stride* was a negative value.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="96161-125"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="96161-125"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="96161-126">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="96161-126">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="96161-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="96161-127">Remarks</span></span>

<span data-ttu-id="96161-128">Com a função **glInterleavedArrays** , você pode especificar e habilitar simultaneamente várias matrizes de cores intercaladas, normal, de textura e de vértice cujos elementos fazem parte de um elemento de matriz agregada maior.</span><span class="sxs-lookup"><span data-stu-id="96161-128">With the **glInterleavedArrays** function, you can simultaneously specify and enable several interleaved color, normal, texture, and vertex arrays whose elements are part of a larger aggregate array element.</span></span> <span data-ttu-id="96161-129">Para algumas arquiteturas de memória, isso é mais eficiente do que especificar as matrizes separadamente.</span><span class="sxs-lookup"><span data-stu-id="96161-129">For some memory architectures, this is more efficient than specifying the arrays separately.</span></span>

<span data-ttu-id="96161-130">Se o parâmetro *Stride* for zero, os elementos da matriz de agregação serão armazenados consecutivamente; caso contrário, ocorrerão bytes de *Stride* entre os elementos de matriz agregada.</span><span class="sxs-lookup"><span data-stu-id="96161-130">If the *stride* parameter is zero then the aggregate array elements are stored consecutively; otherwise *stride* bytes occur between aggregate array elements.</span></span>

<span data-ttu-id="96161-131">O parâmetro *Format* serve como uma chave que descreve como extrair matrizes individuais da matriz agregada:</span><span class="sxs-lookup"><span data-stu-id="96161-131">The *format* parameter serves as a key that describes how to extract individual arrays from the aggregate array:</span></span>

-   <span data-ttu-id="96161-132">Se o *formato* contiver um T, as coordenadas de textura serão extraídas da matriz intercalada.</span><span class="sxs-lookup"><span data-stu-id="96161-132">If *format* contains a T, then texture coordinates are extracted from the interleaved array.</span></span>
-   <span data-ttu-id="96161-133">Se C estiver presente, os valores de cor serão extraídos.</span><span class="sxs-lookup"><span data-stu-id="96161-133">If C is present, color values are extracted.</span></span>
-   <span data-ttu-id="96161-134">Se N estiver presente, as coordenadas normais serão extraídas.</span><span class="sxs-lookup"><span data-stu-id="96161-134">If N is present, normal coordinates are extracted.</span></span>
-   <span data-ttu-id="96161-135">As coordenadas de vértice são sempre extraídas.</span><span class="sxs-lookup"><span data-stu-id="96161-135">Vertex coordinates are always extracted.</span></span>
-   <span data-ttu-id="96161-136">Os dígitos 2, 3 e 4 denotam quantos valores são extraídos.</span><span class="sxs-lookup"><span data-stu-id="96161-136">The digits 2, 3, and 4 denote how many values are extracted.</span></span>
-   <span data-ttu-id="96161-137">F indica que os valores são extraídos como valores de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="96161-137">F indicates that values are extracted as floating point values.</span></span>
-   <span data-ttu-id="96161-138">Se 4UB seguir a C, as cores também podem ser extraídas como 4 bytes não assinados.</span><span class="sxs-lookup"><span data-stu-id="96161-138">If 4UB follows the C, colors may also be extracted as 4 unsigned bytes.</span></span> <span data-ttu-id="96161-139">Se uma cor for extraída como 4 bytes não assinados, o elemento de matriz de vértices a seguir estará localizado no primeiro endereço alinhado de ponto flutuante possível.</span><span class="sxs-lookup"><span data-stu-id="96161-139">If a color is extracted as 4 unsigned bytes, the vertex array element that follows is located at the first possible floating-point aligned address.</span></span>

<span data-ttu-id="96161-140">Se você chamar **glInterleavedArrays** durante a compilação de uma lista de exibição, ela não será compilada na lista, mas será executada imediatamente.</span><span class="sxs-lookup"><span data-stu-id="96161-140">If you call **glInterleavedArrays** while compiling a display list, it is not compiled into the list but is executed immediately.</span></span>

<span data-ttu-id="96161-141">Você não pode incluir chamadas para **glInterleavedArrays** em **glDisableClientState** entre chamadas para [**glBegin**](glbegin.md) e a chamada correspondente para **glEnd**.</span><span class="sxs-lookup"><span data-stu-id="96161-141">You cannot include calls to **glInterleavedArrays** in **glDisableClientState** between calls to [**glBegin**](glbegin.md) and the corresponding call to **glEnd**.</span></span>

> [!Note]  
> <span data-ttu-id="96161-142">A função **glInterleavedArrays** só está disponível no OpenGL versão 1,1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="96161-142">The **glInterleavedArrays** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="96161-143">A função **glInterleavedArrays** é implementada no lado do cliente sem protocolo.</span><span class="sxs-lookup"><span data-stu-id="96161-143">The **glInterleavedArrays** function is implemented on the client side with no protocol.</span></span> <span data-ttu-id="96161-144">Como os parâmetros de matriz de vértice são um estado do lado do cliente, eles não são salvos nem restaurados por [**glPushAttrib**](glpushattrib.md) e **glPopAttrib**.</span><span class="sxs-lookup"><span data-stu-id="96161-144">Because the vertex array parameters are client-side state, they are not saved or restored by [**glPushAttrib**](glpushattrib.md) and **glPopAttrib**.</span></span> <span data-ttu-id="96161-145">Em vez disso, use [**glPushClientAttrib**](glpushclientattrib.md) e **glPopClientAttrib** .</span><span class="sxs-lookup"><span data-stu-id="96161-145">Use [**glPushClientAttrib**](glpushclientattrib.md) and **glPopClientAttrib** instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="96161-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96161-146">Requirements</span></span>



| <span data-ttu-id="96161-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="96161-147">Requirement</span></span> | <span data-ttu-id="96161-148">Valor</span><span class="sxs-lookup"><span data-stu-id="96161-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96161-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96161-149">Minimum supported client</span></span><br/> | <span data-ttu-id="96161-150">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="96161-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="96161-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96161-151">Minimum supported server</span></span><br/> | <span data-ttu-id="96161-152">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="96161-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="96161-153">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="96161-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="96161-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="96161-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="96161-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="96161-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="96161-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96161-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="96161-157">DLL</span><span class="sxs-lookup"><span data-stu-id="96161-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96161-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96161-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96161-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="96161-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96161-160">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="96161-160">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="96161-161">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="96161-161">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="96161-162">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="96161-162">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="96161-163">**glDrawElements**</span><span class="sxs-lookup"><span data-stu-id="96161-163">**glDrawElements**</span></span>](gldrawelements.md)
</dt> <dt>

[<span data-ttu-id="96161-164">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="96161-164">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="96161-165">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="96161-165">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="96161-166">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="96161-166">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="96161-167">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="96161-167">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="96161-168">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="96161-168">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="96161-169">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="96161-169">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="96161-170">**glPushClientAttrib**</span><span class="sxs-lookup"><span data-stu-id="96161-170">**glPushClientAttrib**</span></span>](glpushclientattrib.md)
</dt> <dt>

[<span data-ttu-id="96161-171">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="96161-171">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="96161-172">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="96161-172">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





