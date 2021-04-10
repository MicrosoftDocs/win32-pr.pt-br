---
title: função glVertex3s (GL. h)
description: Especifica um vértice. | função glVertex3s (GL. h)
ms.assetid: ee970440-3eb3-46d6-80d2-e23649585510
keywords:
- função glVertex3s OpenGL
topic_type:
- apiref
api_name:
- glVertex3s
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a167ded1510c0c5d9b430e59fb81b1625d5c199f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104012029"
---
# <a name="glvertex3s-function"></a><span data-ttu-id="88c65-105">função glVertex3s</span><span class="sxs-lookup"><span data-stu-id="88c65-105">glVertex3s function</span></span>

<span data-ttu-id="88c65-106">Especifica um vértice.</span><span class="sxs-lookup"><span data-stu-id="88c65-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="88c65-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="88c65-107">Syntax</span></span>


```C++
void WINAPI glVertex3s(
   GLshort x,
   GLshort y,
   GLshort z
);
```



## <a name="parameters"></a><span data-ttu-id="88c65-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="88c65-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88c65-109">*x*</span><span class="sxs-lookup"><span data-stu-id="88c65-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="88c65-110">Especifica a coordenada x de um vértice.</span><span class="sxs-lookup"><span data-stu-id="88c65-110">Specifies the x-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="88c65-111">*y*</span><span class="sxs-lookup"><span data-stu-id="88c65-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="88c65-112">Especifica a coordenada y de um vértice.</span><span class="sxs-lookup"><span data-stu-id="88c65-112">Specifies the y-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="88c65-113">*z*</span><span class="sxs-lookup"><span data-stu-id="88c65-113">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="88c65-114">Especifica a coordenada z de um vértice.</span><span class="sxs-lookup"><span data-stu-id="88c65-114">Specifies the z-coordinate of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88c65-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="88c65-115">Return value</span></span>

<span data-ttu-id="88c65-116">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="88c65-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="88c65-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="88c65-117">Remarks</span></span>

<span data-ttu-id="88c65-118">Os comandos de função glVertex são usados em pares [**glBegin**](glbegin.md) / [**glEnd**](glend.md) para especificar vértices de ponto, linha e polígono.</span><span class="sxs-lookup"><span data-stu-id="88c65-118">The glVertex function commands are used within [**glBegin**](glbegin.md)/[**glEnd**](glend.md) pairs to specify point, line, and polygon vertices.</span></span> <span data-ttu-id="88c65-119">As coordenadas de cor atual, normal e de textura são associadas ao vértice quando glVertex é chamado.</span><span class="sxs-lookup"><span data-stu-id="88c65-119">The current color, normal, and texture coordinates are associated with the vertex when glVertex is called.</span></span> <span data-ttu-id="88c65-120">Quando apenas *x* e *y* são especificados, *z* usa como padrão 0,0 e *w* é o padrão de 1,0.</span><span class="sxs-lookup"><span data-stu-id="88c65-120">When only *x* and *y* are specified, *z* defaults to 0.0 and *w* defaults to 1.0.</span></span> <span data-ttu-id="88c65-121">Quando *x*, *y* e *z* são especificados, *w* assume o padrão de 1,0.</span><span class="sxs-lookup"><span data-stu-id="88c65-121">When *x*, *y*, and *z* are specified, *w* defaults to 1.0.</span></span> <span data-ttu-id="88c65-122">Invocar glVertex fora de um par **glBegin** / **glEnd** resulta em um comportamento indefinido.</span><span class="sxs-lookup"><span data-stu-id="88c65-122">Invoking glVertex outside of a **glBegin**/**glEnd** pair results in undefined behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="88c65-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88c65-123">Requirements</span></span>



| <span data-ttu-id="88c65-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="88c65-124">Requirement</span></span> | <span data-ttu-id="88c65-125">Valor</span><span class="sxs-lookup"><span data-stu-id="88c65-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88c65-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88c65-126">Minimum supported client</span></span><br/> | <span data-ttu-id="88c65-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="88c65-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="88c65-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88c65-128">Minimum supported server</span></span><br/> | <span data-ttu-id="88c65-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="88c65-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="88c65-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="88c65-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="88c65-131"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="88c65-131"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="88c65-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="88c65-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="88c65-133"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="88c65-133"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="88c65-134">DLL</span><span class="sxs-lookup"><span data-stu-id="88c65-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88c65-135"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88c65-135"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88c65-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="88c65-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88c65-137">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="88c65-137">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="88c65-138">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="88c65-138">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="88c65-139">**glColor**</span><span class="sxs-lookup"><span data-stu-id="88c65-139">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="88c65-140">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="88c65-140">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="88c65-141">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="88c65-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="88c65-142">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="88c65-142">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="88c65-143">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="88c65-143">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="88c65-144">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="88c65-144">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="88c65-145">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="88c65-145">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="88c65-146">**glRect**</span><span class="sxs-lookup"><span data-stu-id="88c65-146">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="88c65-147">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="88c65-147">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





