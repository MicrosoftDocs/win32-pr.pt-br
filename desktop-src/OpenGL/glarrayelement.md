---
title: função glArrayElement (GL. h)
description: A função glArrayElement especifica os elementos de matriz usados para renderizar um vértice.
ms.assetid: 2c4d76bb-e4c9-4baa-a190-66298b8a4335
keywords:
- função glArrayElement OpenGL
topic_type:
- apiref
api_name:
- glArrayElement
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a20aff9fcaa5bf922bc9447f7b7022a8cd1a9c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105784168"
---
# <a name="glarrayelement-function"></a><span data-ttu-id="1a6b9-104">função glArrayElement</span><span class="sxs-lookup"><span data-stu-id="1a6b9-104">glArrayElement function</span></span>

<span data-ttu-id="1a6b9-105">A função **glArrayElement** especifica os elementos de matriz usados para renderizar um vértice.</span><span class="sxs-lookup"><span data-stu-id="1a6b9-105">The **glArrayElement** function specifies the array elements used to render a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a6b9-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a6b9-106">Syntax</span></span>


```C++
void WINAPI glArrayElement(
   GLint index
);
```



## <a name="parameters"></a><span data-ttu-id="1a6b9-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a6b9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a6b9-108">*index*</span><span class="sxs-lookup"><span data-stu-id="1a6b9-108">*index*</span></span> 
</dt> <dd>

<span data-ttu-id="1a6b9-109">Um índice nas matrizes habilitadas.</span><span class="sxs-lookup"><span data-stu-id="1a6b9-109">An index in the enabled arrays.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a6b9-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1a6b9-110">Return value</span></span>

<span data-ttu-id="1a6b9-111">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1a6b9-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a6b9-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a6b9-112">Remarks</span></span>

<span data-ttu-id="1a6b9-113">Use a função **glArrayElement** nos pares [**glBegin**](glbegin.md) e [**glEnd**](glend.md) para especificar os dados de vértice e de atributo para primitivas de ponto, linha e polígono.</span><span class="sxs-lookup"><span data-stu-id="1a6b9-113">Use the **glArrayElement** function within [**glBegin**](glbegin.md) and [**glEnd**](glend.md) pairs to specify vertex and attribute data for point, line, and polygon primitives.</span></span> <span data-ttu-id="1a6b9-114">A função **glArrayElement** especifica os dados de um único vértice usando vértice e dados de atributo localizados no *índice* das matrizes de vértice habilitadas.</span><span class="sxs-lookup"><span data-stu-id="1a6b9-114">The **glArrayElement** function specifies the data for a single vertex using vertex and attribute data located at the *index* of the enabled vertex arrays.</span></span>

<span data-ttu-id="1a6b9-115">Você pode usar **glArrayElement** para construir primitivos indexando dados de vértice, em vez de transmitir por meio de matrizes de dados na primeira a última ordem.</span><span class="sxs-lookup"><span data-stu-id="1a6b9-115">You can use **glArrayElement** to construct primitives by indexing vertex data, rather than by streaming through arrays of data in first-to-last order.</span></span> <span data-ttu-id="1a6b9-116">Como **glArrayElement** especifica apenas um único vértice, você pode especificar explicitamente atributos para primitivos individuais.</span><span class="sxs-lookup"><span data-stu-id="1a6b9-116">Because **glArrayElement** specifies a single vertex only, you can explicitly specify attributes for individual primitives.</span></span> <span data-ttu-id="1a6b9-117">Por exemplo, você pode definir um único normal para cada triângulo individual.</span><span class="sxs-lookup"><span data-stu-id="1a6b9-117">For example, you can set a single normal for each individual triangle.</span></span>

<span data-ttu-id="1a6b9-118">Quando você inclui chamadas para **glArrayElement** em listas de exibição, os dados de matriz necessários, determinados pelos ponteiros de matriz e os valores de Enable, também são inseridos na lista de exibição.</span><span class="sxs-lookup"><span data-stu-id="1a6b9-118">When you include calls to **glArrayElement** in display lists, the necessary array data, determined by the array pointers and enable values, is entered in the display list also.</span></span> <span data-ttu-id="1a6b9-119">Os valores de ponteiro de matriz e de habilitação são determinados quando as listas de exibição são criadas, não quando as listas de exibição são executadas.</span><span class="sxs-lookup"><span data-stu-id="1a6b9-119">Array pointer and enable values are determined when display lists are created, not when display lists are executed.</span></span>

<span data-ttu-id="1a6b9-120">Você pode ler e armazenar em cache os dados estáticos da matriz a qualquer momento com o **glArrayElement**.</span><span class="sxs-lookup"><span data-stu-id="1a6b9-120">You can read and cache static array data at any time with **glArrayElement**.</span></span> <span data-ttu-id="1a6b9-121">Quando você modifica os elementos de uma matriz estática sem especificar a matriz novamente, os resultados de todas as chamadas subsequentes para **glArrayElement** são indefinidos.</span><span class="sxs-lookup"><span data-stu-id="1a6b9-121">When you modify the elements of a static array without specifying the array again, the results of any subsequent calls to **glArrayElement** are undefined.</span></span>

<span data-ttu-id="1a6b9-122">Quando você chama **glArrayElement** sem primeiro chamar **glEnableClientState**( \_ matriz de vértice GL \_ ), nenhum desenho ocorre, mas os atributos correspondentes a matrizes habilitadas são modificados.</span><span class="sxs-lookup"><span data-stu-id="1a6b9-122">When you call **glArrayElement** without first calling **glEnableClientState**(GL\_VERTEX\_ARRAY), no drawing occurs, but the attributes corresponding to enabled arrays are modified.</span></span> <span data-ttu-id="1a6b9-123">Embora nenhum erro seja gerado quando você especifica uma matriz nos pares **glBegin** e **glEnd** , os resultados são indefinidos.</span><span class="sxs-lookup"><span data-stu-id="1a6b9-123">Although no error is generated when you specify an array within **glBegin** and **glEnd** pairs, the results are undefined.</span></span>

> [!Note]  
> <span data-ttu-id="1a6b9-124">A função **glArrayElement** só está disponível no OpenGL versão 1,1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="1a6b9-124">The **glArrayElement** function is only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1a6b9-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a6b9-125">Requirements</span></span>



| <span data-ttu-id="1a6b9-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a6b9-126">Requirement</span></span> | <span data-ttu-id="1a6b9-127">Valor</span><span class="sxs-lookup"><span data-stu-id="1a6b9-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a6b9-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a6b9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1a6b9-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1a6b9-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1a6b9-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a6b9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1a6b9-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1a6b9-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1a6b9-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1a6b9-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a6b9-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a6b9-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1a6b9-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1a6b9-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="1a6b9-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a6b9-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1a6b9-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1a6b9-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a6b9-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a6b9-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a6b9-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a6b9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a6b9-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="1a6b9-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="1a6b9-140">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="1a6b9-140">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="1a6b9-141">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="1a6b9-141">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="1a6b9-142">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="1a6b9-142">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="1a6b9-143">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="1a6b9-143">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="1a6b9-144">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="1a6b9-144">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="1a6b9-145">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="1a6b9-145">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="1a6b9-146">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="1a6b9-146">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="1a6b9-147">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="1a6b9-147">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="1a6b9-148">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="1a6b9-148">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="1a6b9-149">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="1a6b9-149">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="1a6b9-150">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="1a6b9-150">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





