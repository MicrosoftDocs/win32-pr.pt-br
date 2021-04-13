---
title: função glRectdv (GL. h)
description: A função glRectdv desenha um retângulo.
ms.assetid: 53000734-bfc3-42c3-aa80-0a54e3dd36ec
keywords:
- função glRectdv OpenGL
topic_type:
- apiref
api_name:
- glRectdv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de2956a1f658101a384ae69b05ed50418492d264
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369241"
---
# <a name="glrectdv-function"></a><span data-ttu-id="b39b7-104">função glRectdv</span><span class="sxs-lookup"><span data-stu-id="b39b7-104">glRectdv function</span></span>

<span data-ttu-id="b39b7-105">A função **glRectdv** desenha um retângulo.</span><span class="sxs-lookup"><span data-stu-id="b39b7-105">The **glRectdv** function draws a rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="b39b7-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b39b7-106">Syntax</span></span>


```C++
void WINAPI glRectdv(
   const GLdouble *v1,
   const GLdouble *v2
);
```



## <a name="parameters"></a><span data-ttu-id="b39b7-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b39b7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b39b7-108">*v1*</span><span class="sxs-lookup"><span data-stu-id="b39b7-108">*v1*</span></span> 
</dt> <dd>

<span data-ttu-id="b39b7-109">Um ponteiro para um vértice de um retângulo.</span><span class="sxs-lookup"><span data-stu-id="b39b7-109">A pointer to one vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="b39b7-110">*v2*</span><span class="sxs-lookup"><span data-stu-id="b39b7-110">*v2*</span></span> 
</dt> <dd>

<span data-ttu-id="b39b7-111">um ponteiro para o vértice oposto do retângulo.</span><span class="sxs-lookup"><span data-stu-id="b39b7-111">a pointer to the opposite vertex of the rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b39b7-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b39b7-112">Return value</span></span>

<span data-ttu-id="b39b7-113">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b39b7-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b39b7-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="b39b7-114">Error codes</span></span>

<span data-ttu-id="b39b7-115">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="b39b7-115">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b39b7-116">Nome</span><span class="sxs-lookup"><span data-stu-id="b39b7-116">Name</span></span>                                                                                                  | <span data-ttu-id="b39b7-117">Significado</span><span class="sxs-lookup"><span data-stu-id="b39b7-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b39b7-118"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b39b7-118"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b39b7-119">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="b39b7-119">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b39b7-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="b39b7-120">Remarks</span></span>

<span data-ttu-id="b39b7-121">A função **glRectd** dá suporte à especificação eficiente de retângulos como dois pontos de canto.</span><span class="sxs-lookup"><span data-stu-id="b39b7-121">The **glRectd** function supports efficient specification of rectangles as two corner points.</span></span> <span data-ttu-id="b39b7-122">Cada comando de retângulo usa quatro argumentos, organizados como dois pares consecutivos de coordenadas (*x*, *y*) ou como dois ponteiros para matrizes, cada um contendo um par (*x*, *y*).</span><span class="sxs-lookup"><span data-stu-id="b39b7-122">Each rectangle command takes four arguments, organized either as two consecutive pairs of (*x*, *y*) coordinates, or as two pointers to arrays, each containing an (*x*, *y*) pair.</span></span> <span data-ttu-id="b39b7-123">O retângulo resultante é definido no plano *z* = 0.</span><span class="sxs-lookup"><span data-stu-id="b39b7-123">The resulting rectangle is defined in the *z* = 0 plane.</span></span>

<span data-ttu-id="b39b7-124">A função **glRectd**(*X1,* *Y1,* *X2,* *Y2*) é exatamente equivalente à seguinte sequência:</span><span class="sxs-lookup"><span data-stu-id="b39b7-124">The **glRectd**(*x1,* *y1,* *x2,* *y2*) function is exactly equivalent to the following sequence:</span></span>

<span data-ttu-id="b39b7-125">**glBegin**( \_ polígono GL);</span><span class="sxs-lookup"><span data-stu-id="b39b7-125">**glBegin**(GL\_POLYGON);</span></span>

<span data-ttu-id="b39b7-126">**glVertex2**( *X1,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="b39b7-126">**glVertex2**( *x1,* *y1* );</span></span>

<span data-ttu-id="b39b7-127">**glVertex2**( *X2,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="b39b7-127">**glVertex2**( *x2,* *y1* );</span></span>

<span data-ttu-id="b39b7-128">**glVertex2**( *X2,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="b39b7-128">**glVertex2**( *x2,* *y2* );</span></span>

<span data-ttu-id="b39b7-129">**glVertex2**( *X1,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="b39b7-129">**glVertex2**( *x1,* *y2* );</span></span>

<span data-ttu-id="b39b7-130">**glEnd**();</span><span class="sxs-lookup"><span data-stu-id="b39b7-130">**glEnd**( );</span></span>

<span data-ttu-id="b39b7-131">Observe que, se o segundo vértice estiver acima e à direita do primeiro vértice, o retângulo será construído com um retrocesso anti-horário.</span><span class="sxs-lookup"><span data-stu-id="b39b7-131">Notice that if the second vertex is above and to the right of the first vertex, the rectangle is constructed with a counterclockwise winding.</span></span>

## <a name="requirements"></a><span data-ttu-id="b39b7-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b39b7-132">Requirements</span></span>



| <span data-ttu-id="b39b7-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="b39b7-133">Requirement</span></span> | <span data-ttu-id="b39b7-134">Valor</span><span class="sxs-lookup"><span data-stu-id="b39b7-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b39b7-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b39b7-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b39b7-136">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b39b7-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b39b7-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b39b7-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b39b7-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b39b7-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b39b7-139">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b39b7-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="b39b7-140"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b39b7-140"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b39b7-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b39b7-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="b39b7-142"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b39b7-142"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b39b7-143">DLL</span><span class="sxs-lookup"><span data-stu-id="b39b7-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b39b7-144"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b39b7-144"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b39b7-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="b39b7-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b39b7-146">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b39b7-146">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b39b7-147">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b39b7-147">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b39b7-148">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="b39b7-148">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





