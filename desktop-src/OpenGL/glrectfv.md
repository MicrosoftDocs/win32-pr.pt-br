---
title: função glRectfv (GL. h)
description: A função glRectfv desenha um retângulo.
ms.assetid: 2053890e-bae7-4c06-98e7-5ce4314fe95c
keywords:
- função glRectfv OpenGL
topic_type:
- apiref
api_name:
- glRectfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 871cd3edc44598ba66fb686d9957af7322d77730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369240"
---
# <a name="glrectfv-function"></a><span data-ttu-id="18071-104">função glRectfv</span><span class="sxs-lookup"><span data-stu-id="18071-104">glRectfv function</span></span>

<span data-ttu-id="18071-105">A função [**glRectfv**](glrectdv.md) desenha um retângulo.</span><span class="sxs-lookup"><span data-stu-id="18071-105">The [**glRectfv**](glrectdv.md) function draws a rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="18071-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="18071-106">Syntax</span></span>


```C++
void WINAPI glRectfv(
   const GLfloat *v1,
   const GLfloat *v2
);
```



## <a name="parameters"></a><span data-ttu-id="18071-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18071-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18071-108">*v1*</span><span class="sxs-lookup"><span data-stu-id="18071-108">*v1*</span></span> 
</dt> <dd>

<span data-ttu-id="18071-109">Um ponteiro para um vértice de um retângulo.</span><span class="sxs-lookup"><span data-stu-id="18071-109">A pointer to one vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="18071-110">*v2*</span><span class="sxs-lookup"><span data-stu-id="18071-110">*v2*</span></span> 
</dt> <dd>

<span data-ttu-id="18071-111">um ponteiro para o vértice oposto do retângulo.</span><span class="sxs-lookup"><span data-stu-id="18071-111">a pointer to the opposite vertex of the rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18071-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="18071-112">Return value</span></span>

<span data-ttu-id="18071-113">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="18071-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="18071-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="18071-114">Error codes</span></span>

<span data-ttu-id="18071-115">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="18071-115">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="18071-116">Nome</span><span class="sxs-lookup"><span data-stu-id="18071-116">Name</span></span>                                                                                                  | <span data-ttu-id="18071-117">Significado</span><span class="sxs-lookup"><span data-stu-id="18071-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="18071-118"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="18071-118"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="18071-119">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="18071-119">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="18071-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="18071-120">Remarks</span></span>

<span data-ttu-id="18071-121">A função **glRectf** dá suporte à especificação eficiente de retângulos como dois pontos de canto.</span><span class="sxs-lookup"><span data-stu-id="18071-121">The **glRectf** function supports efficient specification of rectangles as two corner points.</span></span> <span data-ttu-id="18071-122">Cada comando de retângulo usa quatro argumentos, organizados como dois pares consecutivos de coordenadas (*x*, *y*) ou como dois ponteiros para matrizes, cada um contendo um par (*x*, *y*).</span><span class="sxs-lookup"><span data-stu-id="18071-122">Each rectangle command takes four arguments, organized either as two consecutive pairs of (*x*, *y*) coordinates, or as two pointers to arrays, each containing an (*x*, *y*) pair.</span></span> <span data-ttu-id="18071-123">O retângulo resultante é definido no plano *z* = 0.</span><span class="sxs-lookup"><span data-stu-id="18071-123">The resulting rectangle is defined in the *z* = 0 plane.</span></span>

<span data-ttu-id="18071-124">A função **glRectf**(*X1,* *Y1,* *X2,* *Y2*) é exatamente equivalente à seguinte sequência:</span><span class="sxs-lookup"><span data-stu-id="18071-124">The **glRectf**(*x1,* *y1,* *x2,* *y2*) function is exactly equivalent to the following sequence:</span></span>

<span data-ttu-id="18071-125">**glBegin**( \_ polígono GL);</span><span class="sxs-lookup"><span data-stu-id="18071-125">**glBegin**(GL\_POLYGON);</span></span>

<span data-ttu-id="18071-126">**glVertex2**( *X1,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="18071-126">**glVertex2**( *x1,* *y1* );</span></span>

<span data-ttu-id="18071-127">**glVertex2**( *X2,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="18071-127">**glVertex2**( *x2,* *y1* );</span></span>

<span data-ttu-id="18071-128">**glVertex2**( *X2,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="18071-128">**glVertex2**( *x2,* *y2* );</span></span>

<span data-ttu-id="18071-129">**glVertex2**( *X1,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="18071-129">**glVertex2**( *x1,* *y2* );</span></span>

<span data-ttu-id="18071-130">**glEnd**();</span><span class="sxs-lookup"><span data-stu-id="18071-130">**glEnd**( );</span></span>

<span data-ttu-id="18071-131">Observe que, se o segundo vértice estiver acima e à direita do primeiro vértice, o retângulo será construído com um retrocesso anti-horário.</span><span class="sxs-lookup"><span data-stu-id="18071-131">Notice that if the second vertex is above and to the right of the first vertex, the rectangle is constructed with a counterclockwise winding.</span></span>

## <a name="requirements"></a><span data-ttu-id="18071-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18071-132">Requirements</span></span>



| <span data-ttu-id="18071-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="18071-133">Requirement</span></span> | <span data-ttu-id="18071-134">Valor</span><span class="sxs-lookup"><span data-stu-id="18071-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18071-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18071-135">Minimum supported client</span></span><br/> | <span data-ttu-id="18071-136">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="18071-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="18071-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18071-137">Minimum supported server</span></span><br/> | <span data-ttu-id="18071-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="18071-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="18071-139">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="18071-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="18071-140"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="18071-140"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="18071-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="18071-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="18071-142"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="18071-142"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="18071-143">DLL</span><span class="sxs-lookup"><span data-stu-id="18071-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18071-144"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18071-144"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18071-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="18071-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18071-146">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="18071-146">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="18071-147">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="18071-147">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="18071-148">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="18071-148">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





