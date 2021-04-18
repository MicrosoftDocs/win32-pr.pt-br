---
title: função glVertex2f (GL. h)
description: Especifica um vértice. | função glVertex2f (GL. h)
ms.assetid: d351cdc1-efaa-4c06-96d9-c4ef613c64df
keywords:
- função glVertex2f OpenGL
topic_type:
- apiref
api_name:
- glVertex2f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b2610b4d0498a5a623372ba5f28ee4feea7b40d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105800097"
---
# <a name="glvertex2f-function"></a><span data-ttu-id="3f4e2-105">função glVertex2f</span><span class="sxs-lookup"><span data-stu-id="3f4e2-105">glVertex2f function</span></span>

<span data-ttu-id="3f4e2-106">Especifica um vértice.</span><span class="sxs-lookup"><span data-stu-id="3f4e2-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f4e2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f4e2-107">Syntax</span></span>


```C++
void WINAPI glVertex2f(
   GLfloat x,
   GLfloat y
);
```



## <a name="parameters"></a><span data-ttu-id="3f4e2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f4e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f4e2-109">*x*</span><span class="sxs-lookup"><span data-stu-id="3f4e2-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="3f4e2-110">Especifica a coordenada x de um vértice.</span><span class="sxs-lookup"><span data-stu-id="3f4e2-110">Specifies the x-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="3f4e2-111">*y*</span><span class="sxs-lookup"><span data-stu-id="3f4e2-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="3f4e2-112">Especifica a coordenada y de um vértice.</span><span class="sxs-lookup"><span data-stu-id="3f4e2-112">Specifies the y-coordinate of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f4e2-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3f4e2-113">Return value</span></span>

<span data-ttu-id="3f4e2-114">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3f4e2-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f4e2-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="3f4e2-115">Remarks</span></span>

<span data-ttu-id="3f4e2-116">Os comandos de função glVertex são usados em pares [**glBegin**](glbegin.md) / [**glEnd**](glend.md) para especificar vértices de ponto, linha e polígono.</span><span class="sxs-lookup"><span data-stu-id="3f4e2-116">The glVertex function commands are used within [**glBegin**](glbegin.md)/[**glEnd**](glend.md) pairs to specify point, line, and polygon vertices.</span></span> <span data-ttu-id="3f4e2-117">As coordenadas de cor atual, normal e de textura são associadas ao vértice quando glVertex é chamado.</span><span class="sxs-lookup"><span data-stu-id="3f4e2-117">The current color, normal, and texture coordinates are associated with the vertex when glVertex is called.</span></span> <span data-ttu-id="3f4e2-118">Quando apenas *x* e *y* são especificados, *z* usa como padrão 0,0 e *w* é o padrão de 1,0.</span><span class="sxs-lookup"><span data-stu-id="3f4e2-118">When only *x* and *y* are specified, *z* defaults to 0.0 and *w* defaults to 1.0.</span></span> <span data-ttu-id="3f4e2-119">Quando *x*, *y* e *z* são especificados, *w* assume o padrão de 1,0.</span><span class="sxs-lookup"><span data-stu-id="3f4e2-119">When *x*, *y*, and *z* are specified, *w* defaults to 1.0.</span></span> <span data-ttu-id="3f4e2-120">Invocar glVertex fora de um par **glBegin** / **glEnd** resulta em um comportamento indefinido.</span><span class="sxs-lookup"><span data-stu-id="3f4e2-120">Invoking glVertex outside of a **glBegin**/**glEnd** pair results in undefined behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f4e2-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f4e2-121">Requirements</span></span>



| <span data-ttu-id="3f4e2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f4e2-122">Requirement</span></span> | <span data-ttu-id="3f4e2-123">Valor</span><span class="sxs-lookup"><span data-stu-id="3f4e2-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f4e2-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f4e2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3f4e2-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3f4e2-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3f4e2-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f4e2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3f4e2-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3f4e2-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3f4e2-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3f4e2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f4e2-129"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f4e2-129"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3f4e2-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3f4e2-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="3f4e2-131"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f4e2-131"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3f4e2-132">DLL</span><span class="sxs-lookup"><span data-stu-id="3f4e2-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f4e2-133"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f4e2-133"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f4e2-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f4e2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f4e2-135">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="3f4e2-135">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3f4e2-136">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="3f4e2-136">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="3f4e2-137">**glColor**</span><span class="sxs-lookup"><span data-stu-id="3f4e2-137">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="3f4e2-138">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="3f4e2-138">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="3f4e2-139">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="3f4e2-139">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3f4e2-140">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="3f4e2-140">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="3f4e2-141">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="3f4e2-141">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="3f4e2-142">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="3f4e2-142">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="3f4e2-143">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="3f4e2-143">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="3f4e2-144">**glRect**</span><span class="sxs-lookup"><span data-stu-id="3f4e2-144">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="3f4e2-145">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="3f4e2-145">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





