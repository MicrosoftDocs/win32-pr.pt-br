---
title: função glRecti (GL. h)
description: A função glRecti desenha um retângulo.
ms.assetid: 8f618b5e-5406-4342-8f7a-83a65bad8a6f
keywords:
- função glRecti OpenGL
topic_type:
- apiref
api_name:
- glRecti
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a17512c9720aea1d2b9dcf5c90b0bde4c67b8fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454657"
---
# <a name="glrecti-function"></a><span data-ttu-id="561db-104">função glRecti</span><span class="sxs-lookup"><span data-stu-id="561db-104">glRecti function</span></span>

<span data-ttu-id="561db-105">A função **glRecti** desenha um retângulo.</span><span class="sxs-lookup"><span data-stu-id="561db-105">The **glRecti** function draws a rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="561db-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="561db-106">Syntax</span></span>


```C++
void WINAPI glRecti(
   GLint x1,
   GLint y1,
   GLint x2,
   GLint y2
);
```



## <a name="parameters"></a><span data-ttu-id="561db-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="561db-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="561db-108">*X1*</span><span class="sxs-lookup"><span data-stu-id="561db-108">*x1*</span></span> 
</dt> <dd>

<span data-ttu-id="561db-109">A coordenada *x* do vértice de um retângulo.</span><span class="sxs-lookup"><span data-stu-id="561db-109">The *x* coordinate of the vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="561db-110">*Y1*</span><span class="sxs-lookup"><span data-stu-id="561db-110">*y1*</span></span> 
</dt> <dd>

<span data-ttu-id="561db-111">A coordenada *y* do vértice de um retângulo.</span><span class="sxs-lookup"><span data-stu-id="561db-111">The *y* coordinate of the vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="561db-112">*X2*</span><span class="sxs-lookup"><span data-stu-id="561db-112">*x2*</span></span> 
</dt> <dd>

<span data-ttu-id="561db-113">A coordenada *x* do vértice oposto do retângulo.</span><span class="sxs-lookup"><span data-stu-id="561db-113">The *x* coordinate of the opposite vertex of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="561db-114">*Y2*</span><span class="sxs-lookup"><span data-stu-id="561db-114">*y2*</span></span> 
</dt> <dd>

<span data-ttu-id="561db-115">A coordenada *y* do vértice oposto do retângulo.</span><span class="sxs-lookup"><span data-stu-id="561db-115">The *y* coordinate of the opposite vertex of the rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="561db-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="561db-116">Return value</span></span>

<span data-ttu-id="561db-117">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="561db-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="561db-118">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="561db-118">Error codes</span></span>

<span data-ttu-id="561db-119">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="561db-119">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="561db-120">Nome</span><span class="sxs-lookup"><span data-stu-id="561db-120">Name</span></span>                                                                                                  | <span data-ttu-id="561db-121">Significado</span><span class="sxs-lookup"><span data-stu-id="561db-121">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="561db-122"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="561db-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="561db-123">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="561db-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="561db-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="561db-124">Remarks</span></span>

<span data-ttu-id="561db-125">A função **glRecti** dá suporte à especificação eficiente de retângulos como dois pontos de canto.</span><span class="sxs-lookup"><span data-stu-id="561db-125">The **glRecti** function supports efficient specification of rectangles as two corner points.</span></span> <span data-ttu-id="561db-126">Cada comando de retângulo usa quatro argumentos, organizados como dois pares consecutivos de coordenadas (*x*, *y*) ou como dois ponteiros para matrizes, cada um contendo um par (*x*, *y*).</span><span class="sxs-lookup"><span data-stu-id="561db-126">Each rectangle command takes four arguments, organized either as two consecutive pairs of (*x*, *y*) coordinates, or as two pointers to arrays, each containing an (*x*, *y*) pair.</span></span> <span data-ttu-id="561db-127">O retângulo resultante é definido no plano *z* = 0.</span><span class="sxs-lookup"><span data-stu-id="561db-127">The resulting rectangle is defined in the *z* = 0 plane.</span></span>

<span data-ttu-id="561db-128">A função **glRecti**(*X1,* *Y1,* *X2,* *Y2*) é exatamente equivalente à seguinte sequência:</span><span class="sxs-lookup"><span data-stu-id="561db-128">The **glRecti**(*x1,* *y1,* *x2,* *y2*) function is exactly equivalent to the following sequence:</span></span>

<span data-ttu-id="561db-129">**glBegin**( \_ polígono GL);</span><span class="sxs-lookup"><span data-stu-id="561db-129">**glBegin**(GL\_POLYGON);</span></span>

<span data-ttu-id="561db-130">**glVertex2**( *X1,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="561db-130">**glVertex2**( *x1,* *y1* );</span></span>

<span data-ttu-id="561db-131">**glVertex2**( *X2,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="561db-131">**glVertex2**( *x2,* *y1* );</span></span>

<span data-ttu-id="561db-132">**glVertex2**( *X2,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="561db-132">**glVertex2**( *x2,* *y2* );</span></span>

<span data-ttu-id="561db-133">**glVertex2**( *X1,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="561db-133">**glVertex2**( *x1,* *y2* );</span></span>

<span data-ttu-id="561db-134">**glEnd**();</span><span class="sxs-lookup"><span data-stu-id="561db-134">**glEnd**( );</span></span>

<span data-ttu-id="561db-135">Observe que, se o segundo vértice estiver acima e à direita do primeiro vértice, o retângulo será construído com um retrocesso anti-horário.</span><span class="sxs-lookup"><span data-stu-id="561db-135">Notice that if the second vertex is above and to the right of the first vertex, the rectangle is constructed with a counterclockwise winding.</span></span>

## <a name="requirements"></a><span data-ttu-id="561db-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="561db-136">Requirements</span></span>



| <span data-ttu-id="561db-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="561db-137">Requirement</span></span> | <span data-ttu-id="561db-138">Valor</span><span class="sxs-lookup"><span data-stu-id="561db-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="561db-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="561db-139">Minimum supported client</span></span><br/> | <span data-ttu-id="561db-140">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="561db-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="561db-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="561db-141">Minimum supported server</span></span><br/> | <span data-ttu-id="561db-142">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="561db-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="561db-143">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="561db-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="561db-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="561db-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="561db-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="561db-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="561db-146"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="561db-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="561db-147">DLL</span><span class="sxs-lookup"><span data-stu-id="561db-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="561db-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="561db-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="561db-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="561db-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="561db-150">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="561db-150">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="561db-151">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="561db-151">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="561db-152">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="561db-152">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





