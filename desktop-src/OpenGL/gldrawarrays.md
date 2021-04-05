---
title: função glDrawArrays (GL. h)
description: A função glDrawArrays especifica vários primitivos a serem renderizados.
ms.assetid: 6ebd467b-5a63-43e4-b3fd-242c704d7d13
keywords:
- função glDrawArrays OpenGL
topic_type:
- apiref
api_name:
- glDrawArrays
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88b20cf3a3e3b2c96a8172f53f8126815efe16d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918581"
---
# <a name="gldrawarrays-function"></a><span data-ttu-id="eaef8-104">função glDrawArrays</span><span class="sxs-lookup"><span data-stu-id="eaef8-104">glDrawArrays function</span></span>

<span data-ttu-id="eaef8-105">A função **glDrawArrays** especifica vários primitivos a serem renderizados.</span><span class="sxs-lookup"><span data-stu-id="eaef8-105">The **glDrawArrays** function specifies multiple primitives to render.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaef8-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eaef8-106">Syntax</span></span>


```C++
void WINAPI glDrawArrays(
   GLenum  mode,
   GLint   first,
   GLsizei count
);
```



## <a name="parameters"></a><span data-ttu-id="eaef8-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eaef8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eaef8-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="eaef8-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="eaef8-109">O tipo de primitivas a ser renderizada.</span><span class="sxs-lookup"><span data-stu-id="eaef8-109">The kind of primitives to render.</span></span> <span data-ttu-id="eaef8-110">As constantes a seguir especificam tipos aceitáveis: os \_ pontos GL, a \_ faixa de linha gl, o \_ \_ \_ loop de linha gl, \_ as linhas GL, a \_ \_ faixa de triângulo GL, o \_ \_ ventilador do triângulo GL, os \_ triângulos GL, o GL \_ Quad strip, o GL \_ \_ quads e o \_ Polygon GL.</span><span class="sxs-lookup"><span data-stu-id="eaef8-110">The following constants specify acceptable types of primitives: GL\_POINTS, GL\_LINE\_STRIP, GL\_LINE\_LOOP, GL\_LINES, GL\_TRIANGLE\_STRIP, GL\_TRIANGLE\_FAN, GL\_TRIANGLES, GL\_QUAD\_STRIP, GL\_QUADS, and GL\_POLYGON.</span></span>

</dd> <dt>

<span data-ttu-id="eaef8-111">*first*</span><span class="sxs-lookup"><span data-stu-id="eaef8-111">*first*</span></span> 
</dt> <dd>

<span data-ttu-id="eaef8-112">O índice inicial nas matrizes habilitadas.</span><span class="sxs-lookup"><span data-stu-id="eaef8-112">The starting index in the enabled arrays.</span></span>

</dd> <dt>

<span data-ttu-id="eaef8-113">*contagem*</span><span class="sxs-lookup"><span data-stu-id="eaef8-113">*count*</span></span> 
</dt> <dd>

<span data-ttu-id="eaef8-114">O número de índices a serem renderizados.</span><span class="sxs-lookup"><span data-stu-id="eaef8-114">The number of indexes to render.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eaef8-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eaef8-115">Return value</span></span>

<span data-ttu-id="eaef8-116">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="eaef8-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="eaef8-117">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="eaef8-117">Error codes</span></span>

<span data-ttu-id="eaef8-118">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="eaef8-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="eaef8-119">Nome</span><span class="sxs-lookup"><span data-stu-id="eaef8-119">Name</span></span>                                                                                                  | <span data-ttu-id="eaef8-120">Significado</span><span class="sxs-lookup"><span data-stu-id="eaef8-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="eaef8-121"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="eaef8-121"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="eaef8-122">a *contagem* era negativa.</span><span class="sxs-lookup"><span data-stu-id="eaef8-122">*count* was negative.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="eaef8-123"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="eaef8-123"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="eaef8-124">o *modo* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="eaef8-124">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="eaef8-125"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="eaef8-125"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="eaef8-126">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="eaef8-126">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="eaef8-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="eaef8-127">Remarks</span></span>

<span data-ttu-id="eaef8-128">Com o **glDrawArrays**, você pode especificar vários primitivos geométricos para renderização.</span><span class="sxs-lookup"><span data-stu-id="eaef8-128">With **glDrawArrays**, you can specify multiple geometric primitives to render.</span></span> <span data-ttu-id="eaef8-129">Em vez de chamar funções OpenGL separadas para passar cada vértice, normal ou cor individual, você pode especificar matrizes separadas de vértices, normais e cores para definir uma sequência de primitivas (o mesmo tipo) com uma única chamada para **glDrawArrays**.</span><span class="sxs-lookup"><span data-stu-id="eaef8-129">Instead of calling separate OpenGL functions to pass each individual vertex, normal, or color, you can specify separate arrays of vertices, normals, and colors to define a sequence of primitives (all the same kind) with a single call to **glDrawArrays**.</span></span>

<span data-ttu-id="eaef8-130">Quando você chama **glDrawArrays**, os elementos sequenciais de *contagem* de cada matriz habilitada são usados para construir uma sequência de primitivos geométricos, começando com o *primeiro* elemento.</span><span class="sxs-lookup"><span data-stu-id="eaef8-130">When you call **glDrawArrays**, *count* sequential elements from each enabled array are used to construct a sequence of geometric primitives, beginning with the *first* element.</span></span> <span data-ttu-id="eaef8-131">O parâmetro *Mode* especifica que tipo de primitiva deve ser construída e como usar os elementos da matriz para construir os primitivos.</span><span class="sxs-lookup"><span data-stu-id="eaef8-131">The *mode* parameter specifies what kind of primitive to construct and how to use the array elements to construct the primitives.</span></span>

<span data-ttu-id="eaef8-132">Após o retorno de **glDrawArrays** , os valores dos atributos de vértice que são modificados por **glDrawArrays** são indefinidos.</span><span class="sxs-lookup"><span data-stu-id="eaef8-132">After **glDrawArrays** returns, the values of vertex attributes that are modified by **glDrawArrays** are undefined.</span></span> <span data-ttu-id="eaef8-133">Por exemplo, se a \_ \_ matriz de cores GL estiver habilitada, o valor da cor atual será indefinido após o retorno de **glDrawArrays** .</span><span class="sxs-lookup"><span data-stu-id="eaef8-133">For example, if GL\_COLOR\_ARRAY is enabled, the value of the current color is undefined after **glDrawArrays** returns.</span></span> <span data-ttu-id="eaef8-134">Atributos não modificados por **glDrawArrays** permanecem definidos.</span><span class="sxs-lookup"><span data-stu-id="eaef8-134">Attributes not modified by **glDrawArrays** remain defined.</span></span> <span data-ttu-id="eaef8-135">Quando \_ \_ a matriz de vértice GL não está habilitada, nenhum primitivo Geométrico é gerado, mas os atributos correspondentes às matrizes habilitadas são modificados.</span><span class="sxs-lookup"><span data-stu-id="eaef8-135">When GL\_VERTEX\_ARRAY is not enabled, no geometric primitives are generated but the attributes corresponding to enabled arrays are modified.</span></span>

<span data-ttu-id="eaef8-136">Você pode incluir **glDrawArrays** em listas de exibição.</span><span class="sxs-lookup"><span data-stu-id="eaef8-136">You can include **glDrawArrays** in display lists.</span></span> <span data-ttu-id="eaef8-137">Quando você inclui **glDrawArrays** em uma lista de exibição, os dados de matriz necessários, determinados pelos ponteiros de matriz e os habilitados, são gerados e inseridos na lista de exibição.</span><span class="sxs-lookup"><span data-stu-id="eaef8-137">When you include **glDrawArrays** in a display list, the necessary array data, determined by the array pointers and the enables, are generated and entered in the display list.</span></span> <span data-ttu-id="eaef8-138">Os valores de ponteiros de matriz e de habilitações são determinados durante a criação de listas de exibição.</span><span class="sxs-lookup"><span data-stu-id="eaef8-138">The values of array pointers and enables are determined during the creation of display lists.</span></span>

<span data-ttu-id="eaef8-139">Você pode ler dados de matriz estática a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="eaef8-139">You can read static array data at any time.</span></span> <span data-ttu-id="eaef8-140">Se qualquer elemento estático da matriz for modificado e a matriz não for especificada novamente, os resultados de todas as chamadas subsequentes para **glDrawArrays** serão indefinidos.</span><span class="sxs-lookup"><span data-stu-id="eaef8-140">If any static array elements are modified and the array is not specified again, the results of any subsequent calls to **glDrawArrays** are undefined.</span></span>

<span data-ttu-id="eaef8-141">Embora nenhum erro seja gerado quando você especifica uma matriz mais de uma vez nos pares [**glBegin**](glbegin.md) e [**glend**](glend.md) , os resultados são indefinidos.</span><span class="sxs-lookup"><span data-stu-id="eaef8-141">Although no error is generated when you specify an array more than once within [**glBegin**](glbegin.md) and [**glend**](glend.md) pairs, the results are undefined.</span></span>

## <a name="requirements"></a><span data-ttu-id="eaef8-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eaef8-142">Requirements</span></span>



| <span data-ttu-id="eaef8-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="eaef8-143">Requirement</span></span> | <span data-ttu-id="eaef8-144">Valor</span><span class="sxs-lookup"><span data-stu-id="eaef8-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eaef8-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eaef8-145">Minimum supported client</span></span><br/> | <span data-ttu-id="eaef8-146">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="eaef8-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="eaef8-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eaef8-147">Minimum supported server</span></span><br/> | <span data-ttu-id="eaef8-148">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="eaef8-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="eaef8-149">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="eaef8-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="eaef8-150"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="eaef8-150"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="eaef8-151">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eaef8-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="eaef8-152"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eaef8-152"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="eaef8-153">DLL</span><span class="sxs-lookup"><span data-stu-id="eaef8-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eaef8-154"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eaef8-154"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eaef8-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="eaef8-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaef8-156">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="eaef8-156">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="eaef8-157">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="eaef8-157">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="eaef8-158">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="eaef8-158">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="eaef8-159">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="eaef8-159">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="eaef8-160">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="eaef8-160">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="eaef8-161">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="eaef8-161">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="eaef8-162">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="eaef8-162">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="eaef8-163">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="eaef8-163">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="eaef8-164">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="eaef8-164">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="eaef8-165">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="eaef8-165">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="eaef8-166">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="eaef8-166">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





