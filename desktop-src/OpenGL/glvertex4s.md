---
title: função glVertex4s (GL. h)
description: Especifica um vértice. | função glVertex4s (GL. h)
ms.assetid: 5030e0dd-9a81-482d-8d87-bfc9355a3c92
keywords:
- função glVertex4s OpenGL
topic_type:
- apiref
api_name:
- glVertex4s
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efcf64b6864d27e8df77056db14e9132cfbaaf5e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105811822"
---
# <a name="glvertex4s-function"></a><span data-ttu-id="f7267-105">função glVertex4s</span><span class="sxs-lookup"><span data-stu-id="f7267-105">glVertex4s function</span></span>

<span data-ttu-id="f7267-106">Especifica um vértice.</span><span class="sxs-lookup"><span data-stu-id="f7267-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7267-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f7267-107">Syntax</span></span>


```C++
void WINAPI glVertex4s(
   GLshort x,
   GLshort y,
   GLshort z,
   GLshort w
);
```



## <a name="parameters"></a><span data-ttu-id="f7267-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f7267-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7267-109">*x*</span><span class="sxs-lookup"><span data-stu-id="f7267-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="f7267-110">Especifica a coordenada x de um vértice.</span><span class="sxs-lookup"><span data-stu-id="f7267-110">Specifies the x-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="f7267-111">*y*</span><span class="sxs-lookup"><span data-stu-id="f7267-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="f7267-112">Especifica a coordenada y de um vértice.</span><span class="sxs-lookup"><span data-stu-id="f7267-112">Specifies the y-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="f7267-113">*z*</span><span class="sxs-lookup"><span data-stu-id="f7267-113">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="f7267-114">Especifica a coordenada z de um vértice.</span><span class="sxs-lookup"><span data-stu-id="f7267-114">Specifies the z-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="f7267-115">*w*</span><span class="sxs-lookup"><span data-stu-id="f7267-115">*w*</span></span> 
</dt> <dd>

<span data-ttu-id="f7267-116">Especifica a coordenada w de um vértice.</span><span class="sxs-lookup"><span data-stu-id="f7267-116">Specifies the w-coordinate of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7267-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f7267-117">Return value</span></span>

<span data-ttu-id="f7267-118">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f7267-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7267-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="f7267-119">Remarks</span></span>

<span data-ttu-id="f7267-120">Os comandos de função glVertex são usados em pares [**glBegin**](glbegin.md) / [**glEnd**](glend.md) para especificar vértices de ponto, linha e polígono.</span><span class="sxs-lookup"><span data-stu-id="f7267-120">The glVertex function commands are used within [**glBegin**](glbegin.md)/[**glEnd**](glend.md) pairs to specify point, line, and polygon vertices.</span></span> <span data-ttu-id="f7267-121">As coordenadas de cor atual, normal e de textura são associadas ao vértice quando glVertex é chamado.</span><span class="sxs-lookup"><span data-stu-id="f7267-121">The current color, normal, and texture coordinates are associated with the vertex when glVertex is called.</span></span> <span data-ttu-id="f7267-122">Quando apenas *x* e *y* são especificados, *z* usa como padrão 0,0 e *w* é o padrão de 1,0.</span><span class="sxs-lookup"><span data-stu-id="f7267-122">When only *x* and *y* are specified, *z* defaults to 0.0 and *w* defaults to 1.0.</span></span> <span data-ttu-id="f7267-123">Quando *x*, *y* e *z* são especificados, *w* assume o padrão de 1,0.</span><span class="sxs-lookup"><span data-stu-id="f7267-123">When *x*, *y*, and *z* are specified, *w* defaults to 1.0.</span></span> <span data-ttu-id="f7267-124">Invocar glVertex fora de um par **glBegin** / **glEnd** resulta em um comportamento indefinido.</span><span class="sxs-lookup"><span data-stu-id="f7267-124">Invoking glVertex outside of a **glBegin**/**glEnd** pair results in undefined behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7267-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7267-125">Requirements</span></span>



| <span data-ttu-id="f7267-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7267-126">Requirement</span></span> | <span data-ttu-id="f7267-127">Valor</span><span class="sxs-lookup"><span data-stu-id="f7267-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7267-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7267-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f7267-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f7267-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f7267-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7267-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f7267-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f7267-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f7267-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f7267-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7267-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7267-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f7267-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f7267-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="f7267-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f7267-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f7267-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f7267-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7267-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7267-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7267-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="f7267-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7267-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f7267-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f7267-140">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="f7267-140">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="f7267-141">**glColor**</span><span class="sxs-lookup"><span data-stu-id="f7267-141">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="f7267-142">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="f7267-142">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="f7267-143">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="f7267-143">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f7267-144">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="f7267-144">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="f7267-145">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="f7267-145">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="f7267-146">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="f7267-146">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="f7267-147">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="f7267-147">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="f7267-148">**glRect**</span><span class="sxs-lookup"><span data-stu-id="f7267-148">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="f7267-149">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="f7267-149">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





