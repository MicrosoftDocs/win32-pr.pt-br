---
title: função glDrawElements (GL. h)
description: A função glDrawElements processa primitivos dos dados da matriz.
ms.assetid: fb433294-106e-48d5-ad49-4434934fe072
keywords:
- função glDrawElements OpenGL
topic_type:
- apiref
api_name:
- glDrawElements
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976e779235dc330467d610406156534b5e72841d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499482"
---
# <a name="gldrawelements-function"></a><span data-ttu-id="e61ed-104">função glDrawElements</span><span class="sxs-lookup"><span data-stu-id="e61ed-104">glDrawElements function</span></span>

<span data-ttu-id="e61ed-105">A função **glDrawElements** processa primitivos dos dados da matriz.</span><span class="sxs-lookup"><span data-stu-id="e61ed-105">The **glDrawElements** function renders primitives from array data.</span></span>

## <a name="syntax"></a><span data-ttu-id="e61ed-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e61ed-106">Syntax</span></span>


```C++
void WINAPI glDrawElements(
         GLenum  mode,
         GLsizei count,
         GLenum  type,
   const GLvoid  *indices
);
```



## <a name="parameters"></a><span data-ttu-id="e61ed-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e61ed-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e61ed-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="e61ed-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="e61ed-109">O tipo de primitivas a ser renderizada.</span><span class="sxs-lookup"><span data-stu-id="e61ed-109">The kind of primitives to render.</span></span> <span data-ttu-id="e61ed-110">Ele pode assumir um dos seguintes valores simbólicos: os \_ pontos GL, a \_ faixa de linha gl, o \_ \_ \_ loop de linha gl, \_ as linhas GL, a \_ \_ faixa de triângulo GL, o \_ \_ ventilador do triângulo GL, os \_ triângulos GL, o GL \_ Quad strip, o GL \_ \_ quads e o \_ Polygon GL.</span><span class="sxs-lookup"><span data-stu-id="e61ed-110">It can assume one of the following symbolic values: GL\_POINTS, GL\_LINE\_STRIP, GL\_LINE\_LOOP, GL\_LINES, GL\_TRIANGLE\_STRIP, GL\_TRIANGLE\_FAN, GL\_TRIANGLES, GL\_QUAD\_STRIP, GL\_QUADS, and GL\_POLYGON.</span></span>

</dd> <dt>

<span data-ttu-id="e61ed-111">*contagem*</span><span class="sxs-lookup"><span data-stu-id="e61ed-111">*count*</span></span> 
</dt> <dd>

<span data-ttu-id="e61ed-112">O número de elementos a serem renderizados.</span><span class="sxs-lookup"><span data-stu-id="e61ed-112">The number of elements to be rendered.</span></span>

</dd> <dt>

<span data-ttu-id="e61ed-113">*tipo*</span><span class="sxs-lookup"><span data-stu-id="e61ed-113">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="e61ed-114">O tipo dos valores em índices.</span><span class="sxs-lookup"><span data-stu-id="e61ed-114">The type of the values in indices.</span></span> <span data-ttu-id="e61ed-115">Deve ser um de GL \_ não assinado, GL não \_ assinado, \_ \_ curto ou GL \_ não assinado \_ int.</span><span class="sxs-lookup"><span data-stu-id="e61ed-115">Must be one of GL\_UNSIGNED\_BYTE, GL\_UNSIGNED\_SHORT, or GL\_UNSIGNED\_INT.</span></span>

</dd> <dt>

<span data-ttu-id="e61ed-116">*índices*</span><span class="sxs-lookup"><span data-stu-id="e61ed-116">*indices*</span></span> 
</dt> <dd>

<span data-ttu-id="e61ed-117">Um ponteiro para o local onde os índices são armazenados.</span><span class="sxs-lookup"><span data-stu-id="e61ed-117">A pointer to the location where the indices are stored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e61ed-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e61ed-118">Return value</span></span>

<span data-ttu-id="e61ed-119">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e61ed-119">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e61ed-120">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="e61ed-120">Error codes</span></span>

<span data-ttu-id="e61ed-121">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="e61ed-121">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e61ed-122">Nome</span><span class="sxs-lookup"><span data-stu-id="e61ed-122">Name</span></span>                                                                                                  | <span data-ttu-id="e61ed-123">Significado</span><span class="sxs-lookup"><span data-stu-id="e61ed-123">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e61ed-124"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="e61ed-124"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="e61ed-125">o *modo* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="e61ed-125">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="e61ed-126"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e61ed-126"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="e61ed-127">*Count* era um valor negativo.</span><span class="sxs-lookup"><span data-stu-id="e61ed-127">*count* was a negative value.</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="e61ed-128"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e61ed-128"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="e61ed-129">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="e61ed-129">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e61ed-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="e61ed-130">Remarks</span></span>

<span data-ttu-id="e61ed-131">A função **glDrawElements** permite que você especifique vários primitivos geométricos com muito poucas chamadas de função.</span><span class="sxs-lookup"><span data-stu-id="e61ed-131">The **glDrawElements** function enables you to specify multiple geometric primitives with very few function calls.</span></span> <span data-ttu-id="e61ed-132">Em vez de chamar uma função OpenGL para passar cada vértice, normal ou cor individual, você pode especificar matrizes separadas de vértices, normais e cores com antecedência e usá-las para definir uma sequência de primitivas (todas do mesmo tipo) com uma única chamada para **glDrawElements**.</span><span class="sxs-lookup"><span data-stu-id="e61ed-132">Instead of calling an OpenGL function to pass each individual vertex, normal, or color, you can specify separate arrays of vertices, normals, and colors beforehand and use them to define a sequence of primitives (all of the same type) with a single call to **glDrawElements**.</span></span>

<span data-ttu-id="e61ed-133">Quando você chama a função **glDrawElements** , ela usa elementos sequenciais de *contagem* de *índices* para construir uma sequência de primitivos geométricos.</span><span class="sxs-lookup"><span data-stu-id="e61ed-133">When you call the **glDrawElements** function, it uses *count* sequential elements from *indices* to construct a sequence of geometric primitives.</span></span> <span data-ttu-id="e61ed-134">O parâmetro *Mode* especifica que tipo de primitivas são construídos e como os elementos de matriz são usados para construir esses primitivos.</span><span class="sxs-lookup"><span data-stu-id="e61ed-134">The *mode* parameter specifies what kind of primitives are constructed, and how the array elements are used to construct these primitives.</span></span> <span data-ttu-id="e61ed-135">Se a \_ matriz de vértice GL \_ não estiver habilitada, nenhum primitivo Geométrico será gerado.</span><span class="sxs-lookup"><span data-stu-id="e61ed-135">If GL\_VERTEX\_ARRAY is not enabled, no geometric primitives are generated.</span></span>

<span data-ttu-id="e61ed-136">Os atributos de vértice que são modificados por **glDrawElements** têm um valor não especificado após o retorno de **glDrawElements** .</span><span class="sxs-lookup"><span data-stu-id="e61ed-136">Vertex attributes that are modified by **glDrawElements** have an unspecified value after **glDrawElements** returns.</span></span> <span data-ttu-id="e61ed-137">Por exemplo, se a \_ \_ matriz de cores GL estiver habilitada, o valor da cor atual será indefinido depois que **glDrawElements** for executado.</span><span class="sxs-lookup"><span data-stu-id="e61ed-137">For example, if GL\_COLOR\_ARRAY is enabled, the value of the current color is undefined after **glDrawElements** executes.</span></span> <span data-ttu-id="e61ed-138">Os atributos que não são modificados permanecem inalterados.</span><span class="sxs-lookup"><span data-stu-id="e61ed-138">Attributes that aren't modified remain unchanged.</span></span>

<span data-ttu-id="e61ed-139">Você pode incluir a função **glDrawElements** em listas de exibição.</span><span class="sxs-lookup"><span data-stu-id="e61ed-139">You can include the **glDrawElements** function in display lists.</span></span> <span data-ttu-id="e61ed-140">Quando **glDrawElements** é incluído em uma lista de exibição, os dados de matriz necessários (determinados pelos ponteiros de matriz e ativações) também são inseridos na lista de exibição.</span><span class="sxs-lookup"><span data-stu-id="e61ed-140">When **glDrawElements** is included in a display list, the necessary array data (determined by the array pointers and enables) is also entered into the display list.</span></span> <span data-ttu-id="e61ed-141">Como os ponteiros de matriz e ativações são variáveis de estado do lado do cliente, seus valores afetam as listas de exibição quando as listas são criadas, não quando as listas são executadas.</span><span class="sxs-lookup"><span data-stu-id="e61ed-141">Because the array pointers and enables are client-side state variables, their values affect display lists when the lists are created, not when the lists are executed.</span></span>

> [!Note]  
> <span data-ttu-id="e61ed-142">A função **glDrawElements** só está disponível no OpenGL versão 1,1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e61ed-142">The **glDrawElements** function is only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e61ed-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e61ed-143">Requirements</span></span>



| <span data-ttu-id="e61ed-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="e61ed-144">Requirement</span></span> | <span data-ttu-id="e61ed-145">Valor</span><span class="sxs-lookup"><span data-stu-id="e61ed-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e61ed-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e61ed-146">Minimum supported client</span></span><br/> | <span data-ttu-id="e61ed-147">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e61ed-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e61ed-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e61ed-148">Minimum supported server</span></span><br/> | <span data-ttu-id="e61ed-149">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e61ed-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e61ed-150">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e61ed-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="e61ed-151"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e61ed-151"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e61ed-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e61ed-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="e61ed-153"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e61ed-153"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e61ed-154">DLL</span><span class="sxs-lookup"><span data-stu-id="e61ed-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e61ed-155"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e61ed-155"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e61ed-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="e61ed-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e61ed-157">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="e61ed-157">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="e61ed-158">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e61ed-158">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e61ed-159">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="e61ed-159">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="e61ed-160">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="e61ed-160">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="e61ed-161">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="e61ed-161">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="e61ed-162">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="e61ed-162">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e61ed-163">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="e61ed-163">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="e61ed-164">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="e61ed-164">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="e61ed-165">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="e61ed-165">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="e61ed-166">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="e61ed-166">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="e61ed-167">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="e61ed-167">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





