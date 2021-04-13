---
title: função glRectsv (GL. h)
description: A função glRectsv desenha um retângulo.
ms.assetid: 0f7dc4fc-b6ce-4240-89d9-69f54c0c9f2b
keywords:
- função glRectsv OpenGL
topic_type:
- apiref
api_name:
- glRectsv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90bdf6ce7d882db9c7cc1f78deddc3ca651a2c6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455993"
---
# <a name="glrectsv-function"></a><span data-ttu-id="c614c-104">função glRectsv</span><span class="sxs-lookup"><span data-stu-id="c614c-104">glRectsv function</span></span>

<span data-ttu-id="c614c-105">A função **glRectsv** desenha um retângulo.</span><span class="sxs-lookup"><span data-stu-id="c614c-105">The **glRectsv** function draws a rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="c614c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c614c-106">Syntax</span></span>


```C++
void WINAPI glRectsv(
   const GLshort *v1,
   const GLshort *v2
);
```



## <a name="parameters"></a><span data-ttu-id="c614c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c614c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c614c-108">*v1*</span><span class="sxs-lookup"><span data-stu-id="c614c-108">*v1*</span></span> 
</dt> <dd>

<span data-ttu-id="c614c-109">Um ponteiro para um vértice de um retângulo.</span><span class="sxs-lookup"><span data-stu-id="c614c-109">A pointer to one vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="c614c-110">*v2*</span><span class="sxs-lookup"><span data-stu-id="c614c-110">*v2*</span></span> 
</dt> <dd>

<span data-ttu-id="c614c-111">um ponteiro para o vértice oposto do retângulo.</span><span class="sxs-lookup"><span data-stu-id="c614c-111">a pointer to the opposite vertex of the rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c614c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c614c-112">Return value</span></span>

<span data-ttu-id="c614c-113">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c614c-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c614c-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="c614c-114">Error codes</span></span>

<span data-ttu-id="c614c-115">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="c614c-115">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="c614c-116">Nome</span><span class="sxs-lookup"><span data-stu-id="c614c-116">Name</span></span>                                                                                                  | <span data-ttu-id="c614c-117">Significado</span><span class="sxs-lookup"><span data-stu-id="c614c-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c614c-118"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c614c-118"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="c614c-119">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="c614c-119">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c614c-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="c614c-120">Remarks</span></span>

<span data-ttu-id="c614c-121">A função **glRects** dá suporte à especificação eficiente de retângulos como dois pontos de canto.</span><span class="sxs-lookup"><span data-stu-id="c614c-121">The **glRects** function supports efficient specification of rectangles as two corner points.</span></span> <span data-ttu-id="c614c-122">Cada comando de retângulo usa quatro argumentos, organizados como dois pares consecutivos de coordenadas (*x*, *y*) ou como dois ponteiros para matrizes, cada um contendo um par (*x,* *y*).</span><span class="sxs-lookup"><span data-stu-id="c614c-122">Each rectangle command takes four arguments, organized either as two consecutive pairs of (*x*, *y*) coordinates, or as two pointers to arrays, each containing an (*x,* *y*) pair.</span></span> <span data-ttu-id="c614c-123">O retângulo resultante é definido no plano *z* = 0.</span><span class="sxs-lookup"><span data-stu-id="c614c-123">The resulting rectangle is defined in the *z* = 0 plane.</span></span>

<span data-ttu-id="c614c-124">A função **glRects**(*X1,* *Y1,* *X2,* *Y2*) é exatamente equivalente à seguinte sequência:</span><span class="sxs-lookup"><span data-stu-id="c614c-124">The **glRects**(*x1,* *y1,* *x2,* *y2*) function is exactly equivalent to the following sequence:</span></span>

<span data-ttu-id="c614c-125">**glBegin**( \_ polígono GL);</span><span class="sxs-lookup"><span data-stu-id="c614c-125">**glBegin**(GL\_POLYGON);</span></span>

<span data-ttu-id="c614c-126">**glVertex2**( *X1,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="c614c-126">**glVertex2**( *x1,* *y1* );</span></span>

<span data-ttu-id="c614c-127">**glVertex2**( *X2,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="c614c-127">**glVertex2**( *x2,* *y1* );</span></span>

<span data-ttu-id="c614c-128">**glVertex2**( *X2,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="c614c-128">**glVertex2**( *x2,* *y2* );</span></span>

<span data-ttu-id="c614c-129">**glVertex2**( *X1,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="c614c-129">**glVertex2**( *x1,* *y2* );</span></span>

<span data-ttu-id="c614c-130">**glEnd**();</span><span class="sxs-lookup"><span data-stu-id="c614c-130">**glEnd**( );</span></span>

<span data-ttu-id="c614c-131">Observe que, se o segundo vértice estiver acima e à direita do primeiro vértice, o retângulo será construído com um retrocesso anti-horário.</span><span class="sxs-lookup"><span data-stu-id="c614c-131">Notice that if the second vertex is above and to the right of the first vertex, the rectangle is constructed with a counterclockwise winding.</span></span>

## <a name="requirements"></a><span data-ttu-id="c614c-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c614c-132">Requirements</span></span>



| <span data-ttu-id="c614c-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="c614c-133">Requirement</span></span> | <span data-ttu-id="c614c-134">Valor</span><span class="sxs-lookup"><span data-stu-id="c614c-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c614c-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c614c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="c614c-136">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c614c-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c614c-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c614c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="c614c-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c614c-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c614c-139">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c614c-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="c614c-140"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c614c-140"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c614c-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c614c-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="c614c-142"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c614c-142"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c614c-143">DLL</span><span class="sxs-lookup"><span data-stu-id="c614c-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c614c-144"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c614c-144"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c614c-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="c614c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c614c-146">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="c614c-146">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="c614c-147">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="c614c-147">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="c614c-148">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="c614c-148">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





