---
title: função gluPickMatrix (Glu. h)
description: A função gluPickMatrix define uma região de separação.
ms.assetid: 2f57345c-17a0-4716-8ab8-170aaed2b4f9
keywords:
- função gluPickMatrix OpenGL
topic_type:
- apiref
api_name:
- gluPickMatrix
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c54e62f82f52fedc7de7c7c4af1cd3ed1ccdf149
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917962"
---
# <a name="glupickmatrix-function"></a><span data-ttu-id="e6948-104">função gluPickMatrix</span><span class="sxs-lookup"><span data-stu-id="e6948-104">gluPickMatrix function</span></span>

<span data-ttu-id="e6948-105">A função **gluPickMatrix** define uma região de separação.</span><span class="sxs-lookup"><span data-stu-id="e6948-105">The **gluPickMatrix** function defines a picking region.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6948-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6948-106">Syntax</span></span>


```C++
void WINAPI gluPickMatrix(
   GLdouble x,
   GLdouble y,
   GLdouble height,
   GLdouble width,
   GLint    viewport[4]
);
```



## <a name="parameters"></a><span data-ttu-id="e6948-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6948-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6948-108">*x*</span><span class="sxs-lookup"><span data-stu-id="e6948-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="e6948-109">A coordenada x da janela de uma região de separação.</span><span class="sxs-lookup"><span data-stu-id="e6948-109">The x window coordinate of a picking region.</span></span>

</dd> <dt>

<span data-ttu-id="e6948-110">*y*</span><span class="sxs-lookup"><span data-stu-id="e6948-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="e6948-111">A coordenada de janela y de uma região de separação.</span><span class="sxs-lookup"><span data-stu-id="e6948-111">The y window coordinate of a picking region.</span></span>

</dd> <dt>

<span data-ttu-id="e6948-112">*altura*</span><span class="sxs-lookup"><span data-stu-id="e6948-112">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="e6948-113">A altura da região de separação em coordenadas da janela.</span><span class="sxs-lookup"><span data-stu-id="e6948-113">The height of the picking region in window coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="e6948-114">*width*</span><span class="sxs-lookup"><span data-stu-id="e6948-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="e6948-115">A largura da região de separação em coordenadas da janela.</span><span class="sxs-lookup"><span data-stu-id="e6948-115">The width of the picking region in window coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="e6948-116">*visor*</span><span class="sxs-lookup"><span data-stu-id="e6948-116">*viewport*</span></span> 
</dt> <dd>

<span data-ttu-id="e6948-117">O visor atual (como de uma chamada [**glGetIntegerv**](glgetintegerv.md) ).</span><span class="sxs-lookup"><span data-stu-id="e6948-117">The current viewport (as from a [**glGetIntegerv**](glgetintegerv.md) call).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6948-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e6948-118">Return value</span></span>

<span data-ttu-id="e6948-119">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e6948-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6948-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6948-120">Remarks</span></span>

<span data-ttu-id="e6948-121">A função **gluPickMatrix** cria uma matriz de projeção que você pode usar para restringir o desenho a uma pequena região do visor.</span><span class="sxs-lookup"><span data-stu-id="e6948-121">The **gluPickMatrix** function creates a projection matrix you can use to restrict drawing to a small region of the viewport.</span></span>

1.  <span data-ttu-id="e6948-122">Use **gluPickMatrix** para restringir o desenho a uma região pequena ao seu cursor.</span><span class="sxs-lookup"><span data-stu-id="e6948-122">Use **gluPickMatrix** to restrict drawing to a small region around the cursor.</span></span>
2.  <span data-ttu-id="e6948-123">Insira o modo de seleção (com [**glRenderMode**](glrendermode.md)) e, em seguida, retorne a cena.</span><span class="sxs-lookup"><span data-stu-id="e6948-123">Enter selection mode (with [**glRenderMode**](glrendermode.md)), and then rerender the scene.</span></span>

    <span data-ttu-id="e6948-124">Todos os primitivos que teriam sido desenhados perto do cursor são identificados e armazenados no buffer de seleção.</span><span class="sxs-lookup"><span data-stu-id="e6948-124">All primitives that would have been drawn near the cursor are identified and stored in the selection buffer.</span></span>

<span data-ttu-id="e6948-125">A matriz criada por **gluPickMatrix** é multiplicada pela matriz atual, assim como se [**glMultMatrix**](glmultmatrix.md) fosse chamado com a matriz gerada.</span><span class="sxs-lookup"><span data-stu-id="e6948-125">The matrix created by **gluPickMatrix** is multiplied by the current matrix just as if [**glMultMatrix**](glmultmatrix.md) were called with the generated matrix.</span></span>

1.  <span data-ttu-id="e6948-126">Chame [**glLoadIdentity**](glloadidentity.md) para carregar uma matriz de identidade na pilha de matriz de perspectiva.</span><span class="sxs-lookup"><span data-stu-id="e6948-126">Call [**glLoadIdentity**](glloadidentity.md) to load an identity matrix onto the perspective matrix stack.</span></span>
2.  <span data-ttu-id="e6948-127">Chame **gluPickMatrix**.</span><span class="sxs-lookup"><span data-stu-id="e6948-127">Call **gluPickMatrix**.</span></span>
3.  <span data-ttu-id="e6948-128">Chame uma função (como [**gluPerspective**](gluperspective.md)) para multiplicar a matriz de perspectiva pela matriz de seleção.</span><span class="sxs-lookup"><span data-stu-id="e6948-128">Call a function (such as [**gluPerspective**](gluperspective.md)) to multiply the perspective matrix by the pick matrix.</span></span>

<span data-ttu-id="e6948-129">Ao usar **gluPickMatrix** para escolher B-spline racional não uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)), tenha cuidado para desativar a propriedade NURBS, a matriz de \_ carga automática Glu \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e6948-129">When using **gluPickMatrix** to pick Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)), be careful to turn off the NURBS property, GLU\_AUTO\_LOAD\_MATRIX.</span></span> <span data-ttu-id="e6948-130">Se a \_ \_ matriz de carga automática Glu não estiver desativada \_ , qualquer superfície NURBS renderizada será subdividida de forma diferente com a matriz de seleção de como ela foi subdividida sem a matriz de seleção.</span><span class="sxs-lookup"><span data-stu-id="e6948-130">If GLU\_AUTO\_LOAD\_MATRIX is not turned off, any NURBS surface rendered is subdivided differently with the pick matrix from how it was subdivided without the pick matrix.</span></span>

## <a name="examples"></a><span data-ttu-id="e6948-131">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e6948-131">Examples</span></span>

<span data-ttu-id="e6948-132">Ao renderizar uma cena da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e6948-132">When rendering a scene as follows:</span></span>


```
glMatrixMode(GL_PROJECTION);  
glLoadIdentity( );  
gluPerspective(. . .);  
glMatrixMode(GL_MODELVIEW);  
/* Draw the scene */
```



<span data-ttu-id="e6948-133">o código a seguir seleciona uma parte do visor:</span><span class="sxs-lookup"><span data-stu-id="e6948-133">the following code selects a portion of the viewport:</span></span>


```
glMatrixMode(GL_PROJECTION);  
glLoadIdentity( );  
gluPickMatrix(x, y, width, height, viewport);  
gluPerspective(. . .);  
glMatrixMode(GL_MODELVIEW);  
/* Draw the scene */
```



## <a name="requirements"></a><span data-ttu-id="e6948-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6948-134">Requirements</span></span>



| <span data-ttu-id="e6948-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6948-135">Requirement</span></span> | <span data-ttu-id="e6948-136">Valor</span><span class="sxs-lookup"><span data-stu-id="e6948-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e6948-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6948-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e6948-138">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e6948-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e6948-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6948-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e6948-140">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e6948-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e6948-141">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e6948-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6948-142"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6948-142"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="e6948-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e6948-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="e6948-144"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6948-144"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e6948-145">DLL</span><span class="sxs-lookup"><span data-stu-id="e6948-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6948-146"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6948-146"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6948-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6948-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6948-148">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="e6948-148">**glGetIntegerv**</span></span>](glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="e6948-149">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="e6948-149">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="e6948-150">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="e6948-150">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="e6948-151">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="e6948-151">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="e6948-152">**gluPerspective**</span><span class="sxs-lookup"><span data-stu-id="e6948-152">**gluPerspective**</span></span>](gluperspective.md)
</dt> </dl>

 

 





