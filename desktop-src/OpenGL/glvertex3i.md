---
title: função glVertex3i (GL. h)
description: Especifica um vértice. | função glVertex3i (GL. h)
ms.assetid: 5f757065-cbe9-401a-855b-f0a9308ae204
keywords:
- função glVertex3i OpenGL
topic_type:
- apiref
api_name:
- glVertex3i
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4e216c35a354daead228d6043d2129f6d30d400
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930336"
---
# <a name="glvertex3i-function"></a><span data-ttu-id="22e30-105">função glVertex3i</span><span class="sxs-lookup"><span data-stu-id="22e30-105">glVertex3i function</span></span>

<span data-ttu-id="22e30-106">Especifica um vértice.</span><span class="sxs-lookup"><span data-stu-id="22e30-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="22e30-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="22e30-107">Syntax</span></span>


```C++
void WINAPI glVertex3i(
   GLint x,
   GLint y,
   GLint z
);
```



## <a name="parameters"></a><span data-ttu-id="22e30-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="22e30-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22e30-109">*x*</span><span class="sxs-lookup"><span data-stu-id="22e30-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="22e30-110">Especifica a coordenada x de um vértice.</span><span class="sxs-lookup"><span data-stu-id="22e30-110">Specifies the x-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="22e30-111">*y*</span><span class="sxs-lookup"><span data-stu-id="22e30-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="22e30-112">Especifica a coordenada y de um vértice.</span><span class="sxs-lookup"><span data-stu-id="22e30-112">Specifies the y-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="22e30-113">*z*</span><span class="sxs-lookup"><span data-stu-id="22e30-113">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="22e30-114">Especifica a coordenada z de um vértice.</span><span class="sxs-lookup"><span data-stu-id="22e30-114">Specifies the z-coordinate of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22e30-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="22e30-115">Return value</span></span>

<span data-ttu-id="22e30-116">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="22e30-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="22e30-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="22e30-117">Remarks</span></span>

<span data-ttu-id="22e30-118">Os comandos de função glVertex são usados em pares [**glBegin**](glbegin.md) / [**glEnd**](glend.md) para especificar vértices de ponto, linha e polígono.</span><span class="sxs-lookup"><span data-stu-id="22e30-118">The glVertex function commands are used within [**glBegin**](glbegin.md)/[**glEnd**](glend.md) pairs to specify point, line, and polygon vertices.</span></span> <span data-ttu-id="22e30-119">As coordenadas de cor atual, normal e de textura são associadas ao vértice quando glVertex é chamado.</span><span class="sxs-lookup"><span data-stu-id="22e30-119">The current color, normal, and texture coordinates are associated with the vertex when glVertex is called.</span></span> <span data-ttu-id="22e30-120">Quando apenas *x* e *y* são especificados, *z* usa como padrão 0,0 e *w* é o padrão de 1,0.</span><span class="sxs-lookup"><span data-stu-id="22e30-120">When only *x* and *y* are specified, *z* defaults to 0.0 and *w* defaults to 1.0.</span></span> <span data-ttu-id="22e30-121">Quando *x*, *y* e *z* são especificados, *w* assume o padrão de 1,0.</span><span class="sxs-lookup"><span data-stu-id="22e30-121">When *x*, *y*, and *z* are specified, *w* defaults to 1.0.</span></span> <span data-ttu-id="22e30-122">Invocar glVertex fora de um par **glBegin** / **glEnd** resulta em um comportamento indefinido.</span><span class="sxs-lookup"><span data-stu-id="22e30-122">Invoking glVertex outside of a **glBegin**/**glEnd** pair results in undefined behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="22e30-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22e30-123">Requirements</span></span>



| <span data-ttu-id="22e30-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="22e30-124">Requirement</span></span> | <span data-ttu-id="22e30-125">Valor</span><span class="sxs-lookup"><span data-stu-id="22e30-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22e30-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22e30-126">Minimum supported client</span></span><br/> | <span data-ttu-id="22e30-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="22e30-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="22e30-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22e30-128">Minimum supported server</span></span><br/> | <span data-ttu-id="22e30-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="22e30-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="22e30-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="22e30-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="22e30-131"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="22e30-131"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="22e30-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="22e30-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="22e30-133"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22e30-133"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="22e30-134">DLL</span><span class="sxs-lookup"><span data-stu-id="22e30-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22e30-135"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22e30-135"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22e30-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="22e30-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22e30-137">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="22e30-137">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="22e30-138">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="22e30-138">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="22e30-139">**glColor**</span><span class="sxs-lookup"><span data-stu-id="22e30-139">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="22e30-140">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="22e30-140">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="22e30-141">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="22e30-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="22e30-142">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="22e30-142">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="22e30-143">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="22e30-143">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="22e30-144">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="22e30-144">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="22e30-145">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="22e30-145">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="22e30-146">**glRect**</span><span class="sxs-lookup"><span data-stu-id="22e30-146">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="22e30-147">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="22e30-147">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





