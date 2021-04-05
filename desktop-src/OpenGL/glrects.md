---
title: função glRects (GL. h)
description: A função glRects desenha um retângulo.
ms.assetid: cf56352a-3396-4061-aa5e-dada986cf4ca
keywords:
- função glRects OpenGL
topic_type:
- apiref
api_name:
- glRects
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcaa60d87c85001120da3a12005ca147b684b7a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086463"
---
# <a name="glrects-function"></a><span data-ttu-id="d9206-104">função glRects</span><span class="sxs-lookup"><span data-stu-id="d9206-104">glRects function</span></span>

<span data-ttu-id="d9206-105">A função **glRects** desenha um retângulo.</span><span class="sxs-lookup"><span data-stu-id="d9206-105">The **glRects** function draws a rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9206-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d9206-106">Syntax</span></span>


```C++
void WINAPI glRects(
   GLshort x1,
   GLshort y1,
   GLshort x2,
   GLshort y2
);
```



## <a name="parameters"></a><span data-ttu-id="d9206-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d9206-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9206-108">*X1*</span><span class="sxs-lookup"><span data-stu-id="d9206-108">*x1*</span></span> 
</dt> <dd>

<span data-ttu-id="d9206-109">A coordenada *x* do vértice de um retângulo.</span><span class="sxs-lookup"><span data-stu-id="d9206-109">The *x* coordinate of the vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="d9206-110">*Y1*</span><span class="sxs-lookup"><span data-stu-id="d9206-110">*y1*</span></span> 
</dt> <dd>

<span data-ttu-id="d9206-111">A coordenada *y* do vértice de um retângulo.</span><span class="sxs-lookup"><span data-stu-id="d9206-111">The *y* coordinate of the vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="d9206-112">*X2*</span><span class="sxs-lookup"><span data-stu-id="d9206-112">*x2*</span></span> 
</dt> <dd>

<span data-ttu-id="d9206-113">A coordenada *x* do vértice oposto do retângulo.</span><span class="sxs-lookup"><span data-stu-id="d9206-113">The *x* coordinate of the opposite vertex of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="d9206-114">*Y2*</span><span class="sxs-lookup"><span data-stu-id="d9206-114">*y2*</span></span> 
</dt> <dd>

<span data-ttu-id="d9206-115">A coordenada *y* do vértice oposto do retângulo.</span><span class="sxs-lookup"><span data-stu-id="d9206-115">The *y* coordinate of the opposite vertex of the rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9206-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d9206-116">Return value</span></span>

<span data-ttu-id="d9206-117">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d9206-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d9206-118">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="d9206-118">Error codes</span></span>

<span data-ttu-id="d9206-119">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="d9206-119">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="d9206-120">Nome</span><span class="sxs-lookup"><span data-stu-id="d9206-120">Name</span></span>                                                                                                  | <span data-ttu-id="d9206-121">Significado</span><span class="sxs-lookup"><span data-stu-id="d9206-121">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d9206-122"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d9206-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d9206-123">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="d9206-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d9206-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="d9206-124">Remarks</span></span>

<span data-ttu-id="d9206-125">A função **glRects** dá suporte à especificação eficiente de retângulos como dois pontos de canto.</span><span class="sxs-lookup"><span data-stu-id="d9206-125">The **glRects** function supports efficient specification of rectangles as two corner points.</span></span> <span data-ttu-id="d9206-126">Cada comando de retângulo usa quatro argumentos, organizados como dois pares consecutivos de coordenadas (x, *y*) ou como dois ponteiros para matrizes, cada um contendo um par (*x*, *y*).</span><span class="sxs-lookup"><span data-stu-id="d9206-126">Each rectangle command takes four arguments, organized either as two consecutive pairs of (x, *y*) coordinates, or as two pointers to arrays, each containing an (*x*, *y*) pair.</span></span> <span data-ttu-id="d9206-127">O retângulo resultante é definido no plano *z* = 0.</span><span class="sxs-lookup"><span data-stu-id="d9206-127">The resulting rectangle is defined in the *z* = 0 plane.</span></span>

<span data-ttu-id="d9206-128">A função **glRects**(*X1,* *Y1,* *X2,* *Y2*) é exatamente equivalente à seguinte sequência:</span><span class="sxs-lookup"><span data-stu-id="d9206-128">The **glRects**(*x1,* *y1,* *x2,* *y2*) function is exactly equivalent to the following sequence:</span></span>

<span data-ttu-id="d9206-129">**glBegin**( \_ polígono GL);</span><span class="sxs-lookup"><span data-stu-id="d9206-129">**glBegin**(GL\_POLYGON);</span></span>

<span data-ttu-id="d9206-130">**glVertex2**( *X1,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="d9206-130">**glVertex2**( *x1,* *y1* );</span></span>

<span data-ttu-id="d9206-131">**glVertex2**( *X2,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="d9206-131">**glVertex2**( *x2,* *y1* );</span></span>

<span data-ttu-id="d9206-132">**glVertex2**( *X2,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="d9206-132">**glVertex2**( *x2,* *y2* );</span></span>

<span data-ttu-id="d9206-133">**glVertex2**( *X1,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="d9206-133">**glVertex2**( *x1,* *y2* );</span></span>

<span data-ttu-id="d9206-134">**glEnd**();</span><span class="sxs-lookup"><span data-stu-id="d9206-134">**glEnd**( );</span></span>

<span data-ttu-id="d9206-135">Observe que, se o segundo vértice estiver acima e à direita do primeiro vértice, o retângulo será construído com um retrocesso anti-horário.</span><span class="sxs-lookup"><span data-stu-id="d9206-135">Notice that if the second vertex is above and to the right of the first vertex, the rectangle is constructed with a counterclockwise winding.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9206-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9206-136">Requirements</span></span>



| <span data-ttu-id="d9206-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9206-137">Requirement</span></span> | <span data-ttu-id="d9206-138">Valor</span><span class="sxs-lookup"><span data-stu-id="d9206-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9206-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d9206-139">Minimum supported client</span></span><br/> | <span data-ttu-id="d9206-140">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d9206-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d9206-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d9206-141">Minimum supported server</span></span><br/> | <span data-ttu-id="d9206-142">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d9206-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d9206-143">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d9206-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9206-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9206-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="d9206-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d9206-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="d9206-146"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9206-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d9206-147">DLL</span><span class="sxs-lookup"><span data-stu-id="d9206-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9206-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9206-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9206-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="d9206-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9206-150">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="d9206-150">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="d9206-151">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="d9206-151">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="d9206-152">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="d9206-152">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





