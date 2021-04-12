---
title: função glColorPointer (GL. h)
description: A função glColorPointer define uma matriz de cores.
ms.assetid: 4d9d05fb-691d-4b71-b079-c42dc7103055
keywords:
- função glColorPointer OpenGL
topic_type:
- apiref
api_name:
- glColorPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9abced52f0d0664e998ad8380e33d43d4af36bcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454856"
---
# <a name="glcolorpointer-function"></a><span data-ttu-id="4e4ac-104">função glColorPointer</span><span class="sxs-lookup"><span data-stu-id="4e4ac-104">glColorPointer function</span></span>

<span data-ttu-id="4e4ac-105">A função **glColorPointer** define uma matriz de cores.</span><span class="sxs-lookup"><span data-stu-id="4e4ac-105">The **glColorPointer** function defines an array of colors.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e4ac-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4e4ac-106">Syntax</span></span>


```C++
void WINAPI glColorPointer(
         GLint   size,
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="4e4ac-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e4ac-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e4ac-108">*size*</span><span class="sxs-lookup"><span data-stu-id="4e4ac-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="4e4ac-109">O número de componentes por cor.</span><span class="sxs-lookup"><span data-stu-id="4e4ac-109">The number of components per color.</span></span> <span data-ttu-id="4e4ac-110">O valor deve ser 3 ou 4.</span><span class="sxs-lookup"><span data-stu-id="4e4ac-110">The value must be either 3 or 4.</span></span>

</dd> <dt>

<span data-ttu-id="4e4ac-111">*tipo*</span><span class="sxs-lookup"><span data-stu-id="4e4ac-111">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="4e4ac-112">O tipo de dados de cada componente de cor em uma matriz de cores.</span><span class="sxs-lookup"><span data-stu-id="4e4ac-112">The data type of each color component in a color array.</span></span> <span data-ttu-id="4e4ac-113">Tipos de dados aceitáveis são especificados com as seguintes constantes: GL \_ byte, GL \_ não assinado \_ byte, GL \_ short, GL \_ não assinado \_ curto, GL \_ int, GL \_ não assinado \_ int, GL \_ float ou GL \_ Double.</span><span class="sxs-lookup"><span data-stu-id="4e4ac-113">Acceptable data types are specified with the following constants: GL\_BYTE, GL\_UNSIGNED\_BYTE, GL\_SHORT, GL\_UNSIGNED\_SHORT, GL\_INT, GL\_UNSIGNED\_INT, GL\_FLOAT, or GL\_DOUBLE.</span></span>

</dd> <dt>

<span data-ttu-id="4e4ac-114">*Stride*</span><span class="sxs-lookup"><span data-stu-id="4e4ac-114">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="4e4ac-115">O deslocamento de bytes entre as cores consecutivas.</span><span class="sxs-lookup"><span data-stu-id="4e4ac-115">The byte offset between consecutive colors.</span></span> <span data-ttu-id="4e4ac-116">Quando *Stride* é zero, as cores são totalmente empacotadas na matriz.</span><span class="sxs-lookup"><span data-stu-id="4e4ac-116">When *stride* is zero, the colors are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="4e4ac-117">*ponteiro*</span><span class="sxs-lookup"><span data-stu-id="4e4ac-117">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="4e4ac-118">Um ponteiro para o primeiro componente do primeiro elemento Color em uma matriz Color.</span><span class="sxs-lookup"><span data-stu-id="4e4ac-118">A pointer to the first component of the first color element in a color array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e4ac-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4e4ac-119">Return value</span></span>

<span data-ttu-id="4e4ac-120">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4e4ac-120">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4e4ac-121">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="4e4ac-121">Error codes</span></span>

<span data-ttu-id="4e4ac-122">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="4e4ac-122">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="4e4ac-123">Nome</span><span class="sxs-lookup"><span data-stu-id="4e4ac-123">Name</span></span>                                                                                              | <span data-ttu-id="4e4ac-124">Significado</span><span class="sxs-lookup"><span data-stu-id="4e4ac-124">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="4e4ac-125"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4e4ac-125"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="4e4ac-126">o *tamanho* não era 3 ou 4.</span><span class="sxs-lookup"><span data-stu-id="4e4ac-126">*size* was not 3 or 4.</span></span><br/>            |
| <dl> <span data-ttu-id="4e4ac-127"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="4e4ac-127"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="4e4ac-128">o *tipo* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="4e4ac-128">*type* was not an accepted value.</span></span><br/> |
| <dl> <span data-ttu-id="4e4ac-129"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4e4ac-129"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="4e4ac-130">*Stride* ou *Count* era negativo.</span><span class="sxs-lookup"><span data-stu-id="4e4ac-130">*stride* or *count* was negative.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4e4ac-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e4ac-131">Remarks</span></span>

<span data-ttu-id="4e4ac-132">A função **glColorPointer** especifica o local e o formato de dados de uma matriz de componentes de cor a serem usados durante a renderização.</span><span class="sxs-lookup"><span data-stu-id="4e4ac-132">The **glColorPointer** function specifies the location and data format of an array of color components to use when rendering.</span></span> <span data-ttu-id="4e4ac-133">O parâmetro *Stride* determina o deslocamento de bytes de uma cor para a próxima, habilitando a embalagem de atributos de vértice em uma única matriz ou armazenamento em matrizes separadas.</span><span class="sxs-lookup"><span data-stu-id="4e4ac-133">The *stride* parameter determines the byte offset from one color to the next, enabling the packing of vertex attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="4e4ac-134">Em algumas implementações, armazenar atributos de vértice em uma única matriz pode ser mais eficiente do que o uso de matrizes separadas.</span><span class="sxs-lookup"><span data-stu-id="4e4ac-134">In some implementations, storing vertex attributes in a single array can be more efficient than the use of separate arrays.</span></span>

<span data-ttu-id="4e4ac-135">Habilitada a matriz de cores especificando a \_ constante de matriz de cores GL \_ com [**glEnableClientState**](glenableclientstate.md).</span><span class="sxs-lookup"><span data-stu-id="4e4ac-135">Enabled the color array by specifying the GL\_COLOR\_ARRAY constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="4e4ac-136">Chamar [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)ou [**glDrawArrays**](gldrawarrays.md) usa a matriz de cores que, portanto, é habilitada.</span><span class="sxs-lookup"><span data-stu-id="4e4ac-136">Calling [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md) uses the color array that is thus enabled.</span></span> <span data-ttu-id="4e4ac-137">Por padrão, a matriz de cores está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="4e4ac-137">By default, the color array is disabled.</span></span> <span data-ttu-id="4e4ac-138">As chamadas **glColorPointer** não podem ser inseridas em listas de exibição.</span><span class="sxs-lookup"><span data-stu-id="4e4ac-138">The **glColorPointer** calls cannot by entered in display lists.</span></span>

<span data-ttu-id="4e4ac-139">Quando você especifica uma matriz de cores usando **glColorPointer**, os valores de todos os parâmetros de matriz de cor da função são salvos em um estado do lado do cliente e você pode armazenar em cache elementos estáticos da matriz.</span><span class="sxs-lookup"><span data-stu-id="4e4ac-139">When you specify a color array using **glColorPointer**, the values of all the function's color array parameters are saved in a client-side state, and you can cache static array elements.</span></span> <span data-ttu-id="4e4ac-140">Como os parâmetros de matriz de cor estão em um estado do lado do cliente, [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md) não salvam nem restauram os valores dos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4e4ac-140">Because the color array parameters are in a client-side state, [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) do not save or restore the parameters' values.</span></span>

<span data-ttu-id="4e4ac-141">Embora a especificação da matriz de cores nos pares [**glBegin**](glbegin.md) e [**glend**](glend.md) não gere um erro, os resultados são indefinidos.</span><span class="sxs-lookup"><span data-stu-id="4e4ac-141">Although specifying the color array within [**glBegin**](glbegin.md) and [**glend**](glend.md) pairs does not generate an error, the results are undefined.</span></span>

<span data-ttu-id="4e4ac-142">As funções a seguir recuperam informações relacionadas à função **glColorPointer** :</span><span class="sxs-lookup"><span data-stu-id="4e4ac-142">The following functions retrieve information related to the **glColorPointer** function:</span></span>

<span data-ttu-id="4e4ac-143">matriz de cores [**glIsEnabled**](glisenabled.md) com Argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="4e4ac-143">[**glIsEnabled**](glisenabled.md) with argument GL\_COLOR\_ARRAY</span></span>

<span data-ttu-id="4e4ac-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ tamanho da \_ matriz de cores do argumento GL \_</span><span class="sxs-lookup"><span data-stu-id="4e4ac-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_COLOR\_ARRAY\_SIZE</span></span>

<span data-ttu-id="4e4ac-145"> tipo de matriz de cores glGet com Argument GL \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="4e4ac-145">**glGet** with argument GL\_COLOR\_ARRAY\_TYPE</span></span>

<span data-ttu-id="4e4ac-146">**glGet** com Stride de \_ matriz de cores do argumento GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="4e4ac-146">**glGet** with argument GL\_COLOR\_ARRAY\_STRIDE</span></span>

<span data-ttu-id="4e4ac-147"> \_ \_ contagem de matrizes de cores glGet com Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="4e4ac-147">**glGet** with argument GL\_COLOR\_ARRAY\_COUNT</span></span>

<span data-ttu-id="4e4ac-148">[](glgetpointerv.md) ponteiro de matriz de cores glGetPointerv com Argument GL \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="4e4ac-148">[**glGetPointerv**](glgetpointerv.md) with argument GL\_COLOR\_ARRAY\_POINTER</span></span>

## <a name="requirements"></a><span data-ttu-id="4e4ac-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e4ac-149">Requirements</span></span>



| <span data-ttu-id="4e4ac-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e4ac-150">Requirement</span></span> | <span data-ttu-id="4e4ac-151">Valor</span><span class="sxs-lookup"><span data-stu-id="4e4ac-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e4ac-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e4ac-152">Minimum supported client</span></span><br/> | <span data-ttu-id="4e4ac-153">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4e4ac-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4e4ac-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e4ac-154">Minimum supported server</span></span><br/> | <span data-ttu-id="4e4ac-155">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4e4ac-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4e4ac-156">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4e4ac-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e4ac-157"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e4ac-157"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="4e4ac-158">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4e4ac-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="4e4ac-159"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e4ac-159"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4e4ac-160">DLL</span><span class="sxs-lookup"><span data-stu-id="4e4ac-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e4ac-161"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e4ac-161"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e4ac-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e4ac-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e4ac-163">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="4e4ac-163">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="4e4ac-164">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="4e4ac-164">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="4e4ac-165">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="4e4ac-165">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="4e4ac-166">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="4e4ac-166">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="4e4ac-167">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="4e4ac-167">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="4e4ac-168">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="4e4ac-168">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="4e4ac-169">**glGet**</span><span class="sxs-lookup"><span data-stu-id="4e4ac-169">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="4e4ac-170">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="4e4ac-170">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="4e4ac-171">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="4e4ac-171">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="4e4ac-172">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="4e4ac-172">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="4e4ac-173">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="4e4ac-173">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="4e4ac-174">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="4e4ac-174">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="4e4ac-175">**glPopAttrib**</span><span class="sxs-lookup"><span data-stu-id="4e4ac-175">**glPopAttrib**</span></span>](glpopattrib.md)
</dt> <dt>

[<span data-ttu-id="4e4ac-176">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="4e4ac-176">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="4e4ac-177">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="4e4ac-177">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="4e4ac-178">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="4e4ac-178">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





