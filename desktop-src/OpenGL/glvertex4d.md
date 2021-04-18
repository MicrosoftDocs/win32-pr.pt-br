---
title: função glVertex4d (GL. h)
description: Especifica um vértice. | função glVertex4d (GL. h)
ms.assetid: d9203e4f-5ed2-41e7-b619-65cee3132ed9
keywords:
- função glVertex4d OpenGL
topic_type:
- apiref
api_name:
- glVertex4d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a28a64c35ff30cc668839899dca4f3dc2958ff9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105770270"
---
# <a name="glvertex4d-function"></a><span data-ttu-id="a4f40-105">função glVertex4d</span><span class="sxs-lookup"><span data-stu-id="a4f40-105">glVertex4d function</span></span>

<span data-ttu-id="a4f40-106">Especifica um vértice.</span><span class="sxs-lookup"><span data-stu-id="a4f40-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4f40-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4f40-107">Syntax</span></span>


```C++
void WINAPI glVertex4d(
   GLdouble x,
   GLdouble y,
   GLdouble z,
   GLdouble w
);
```



## <a name="parameters"></a><span data-ttu-id="a4f40-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4f40-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4f40-109">*x*</span><span class="sxs-lookup"><span data-stu-id="a4f40-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="a4f40-110">Especifica a coordenada x de um vértice.</span><span class="sxs-lookup"><span data-stu-id="a4f40-110">Specifies the x-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="a4f40-111">*y*</span><span class="sxs-lookup"><span data-stu-id="a4f40-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="a4f40-112">Especifica a coordenada y de um vértice.</span><span class="sxs-lookup"><span data-stu-id="a4f40-112">Specifies the y-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="a4f40-113">*z*</span><span class="sxs-lookup"><span data-stu-id="a4f40-113">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="a4f40-114">Especifica a coordenada z de um vértice.</span><span class="sxs-lookup"><span data-stu-id="a4f40-114">Specifies the z-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="a4f40-115">*w*</span><span class="sxs-lookup"><span data-stu-id="a4f40-115">*w*</span></span> 
</dt> <dd>

<span data-ttu-id="a4f40-116">Especifica a coordenada w de um vértice.</span><span class="sxs-lookup"><span data-stu-id="a4f40-116">Specifies the w-coordinate of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4f40-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a4f40-117">Return value</span></span>

<span data-ttu-id="a4f40-118">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a4f40-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4f40-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4f40-119">Remarks</span></span>

<span data-ttu-id="a4f40-120">Os comandos de função glVertex são usados em pares [**glBegin**](glbegin.md) / [**glEnd**](glend.md) para especificar vértices de ponto, linha e polígono.</span><span class="sxs-lookup"><span data-stu-id="a4f40-120">The glVertex function commands are used within [**glBegin**](glbegin.md)/[**glEnd**](glend.md) pairs to specify point, line, and polygon vertices.</span></span> <span data-ttu-id="a4f40-121">As coordenadas de cor atual, normal e de textura são associadas ao vértice quando glVertex é chamado.</span><span class="sxs-lookup"><span data-stu-id="a4f40-121">The current color, normal, and texture coordinates are associated with the vertex when glVertex is called.</span></span> <span data-ttu-id="a4f40-122">Quando apenas *x* e *y* são especificados, *z* usa como padrão 0,0 e *w* é o padrão de 1,0.</span><span class="sxs-lookup"><span data-stu-id="a4f40-122">When only *x* and *y* are specified, *z* defaults to 0.0 and *w* defaults to 1.0.</span></span> <span data-ttu-id="a4f40-123">Quando *x*, *y* e *z* são especificados, *w* assume o padrão de 1,0.</span><span class="sxs-lookup"><span data-stu-id="a4f40-123">When *x*, *y*, and *z* are specified, *w* defaults to 1.0.</span></span> <span data-ttu-id="a4f40-124">Invocar glVertex fora de um par **glBegin** / **glEnd** resulta em um comportamento indefinido.</span><span class="sxs-lookup"><span data-stu-id="a4f40-124">Invoking glVertex outside of a **glBegin**/**glEnd** pair results in undefined behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4f40-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4f40-125">Requirements</span></span>



| <span data-ttu-id="a4f40-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4f40-126">Requirement</span></span> | <span data-ttu-id="a4f40-127">Valor</span><span class="sxs-lookup"><span data-stu-id="a4f40-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4f40-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4f40-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a4f40-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a4f40-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a4f40-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4f40-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a4f40-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a4f40-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a4f40-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a4f40-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4f40-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4f40-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a4f40-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a4f40-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="a4f40-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a4f40-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a4f40-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a4f40-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4f40-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4f40-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4f40-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4f40-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4f40-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a4f40-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a4f40-140">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="a4f40-140">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="a4f40-141">**glColor**</span><span class="sxs-lookup"><span data-stu-id="a4f40-141">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="a4f40-142">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="a4f40-142">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="a4f40-143">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="a4f40-143">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a4f40-144">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="a4f40-144">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="a4f40-145">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="a4f40-145">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="a4f40-146">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="a4f40-146">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="a4f40-147">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="a4f40-147">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="a4f40-148">**glRect**</span><span class="sxs-lookup"><span data-stu-id="a4f40-148">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="a4f40-149">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="a4f40-149">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





