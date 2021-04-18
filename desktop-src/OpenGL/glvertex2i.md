---
title: função glVertex2i (GL. h)
description: Especifica um vértice. | função glVertex2i (GL. h)
ms.assetid: 13dc175b-9382-4266-962d-6dcf23ff5949
keywords:
- função glVertex2i OpenGL
topic_type:
- apiref
api_name:
- glVertex2i
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f810083c61fbd04d1c61349d57e7abd72ab95a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105760401"
---
# <a name="glvertex2i-function"></a><span data-ttu-id="3f587-105">função glVertex2i</span><span class="sxs-lookup"><span data-stu-id="3f587-105">glVertex2i function</span></span>

<span data-ttu-id="3f587-106">Especifica um vértice.</span><span class="sxs-lookup"><span data-stu-id="3f587-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f587-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f587-107">Syntax</span></span>


```C++
void WINAPI glVertex2i(
   GLint x,
   GLint y
);
```



## <a name="parameters"></a><span data-ttu-id="3f587-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f587-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f587-109">*x*</span><span class="sxs-lookup"><span data-stu-id="3f587-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="3f587-110">Especifica a coordenada x de um vértice.</span><span class="sxs-lookup"><span data-stu-id="3f587-110">Specifies the x-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="3f587-111">*y*</span><span class="sxs-lookup"><span data-stu-id="3f587-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="3f587-112">Especifica a coordenada y de um vértice.</span><span class="sxs-lookup"><span data-stu-id="3f587-112">Specifies the y-coordinate of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f587-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3f587-113">Return value</span></span>

<span data-ttu-id="3f587-114">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3f587-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f587-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="3f587-115">Remarks</span></span>

<span data-ttu-id="3f587-116">Os comandos de função glVertex são usados em pares [**glBegin**](glbegin.md) / [**glEnd**](glend.md) para especificar vértices de ponto, linha e polígono.</span><span class="sxs-lookup"><span data-stu-id="3f587-116">The glVertex function commands are used within [**glBegin**](glbegin.md)/[**glEnd**](glend.md) pairs to specify point, line, and polygon vertices.</span></span> <span data-ttu-id="3f587-117">As coordenadas de cor atual, normal e de textura são associadas ao vértice quando glVertex é chamado.</span><span class="sxs-lookup"><span data-stu-id="3f587-117">The current color, normal, and texture coordinates are associated with the vertex when glVertex is called.</span></span> <span data-ttu-id="3f587-118">Quando apenas *x* e *y* são especificados, *z* usa como padrão 0,0 e *w* é o padrão de 1,0.</span><span class="sxs-lookup"><span data-stu-id="3f587-118">When only *x* and *y* are specified, *z* defaults to 0.0 and *w* defaults to 1.0.</span></span> <span data-ttu-id="3f587-119">Quando *x*, *y* e *z* são especificados, *w* assume o padrão de 1,0.</span><span class="sxs-lookup"><span data-stu-id="3f587-119">When *x*, *y*, and *z* are specified, *w* defaults to 1.0.</span></span> <span data-ttu-id="3f587-120">Invocar glVertex fora de um par **glBegin** / **glEnd** resulta em um comportamento indefinido.</span><span class="sxs-lookup"><span data-stu-id="3f587-120">Invoking glVertex outside of a **glBegin**/**glEnd** pair results in undefined behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f587-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f587-121">Requirements</span></span>



| <span data-ttu-id="3f587-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f587-122">Requirement</span></span> | <span data-ttu-id="3f587-123">Valor</span><span class="sxs-lookup"><span data-stu-id="3f587-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f587-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f587-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3f587-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3f587-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3f587-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f587-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3f587-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3f587-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3f587-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3f587-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f587-129"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f587-129"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3f587-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3f587-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="3f587-131"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f587-131"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3f587-132">DLL</span><span class="sxs-lookup"><span data-stu-id="3f587-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f587-133"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f587-133"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f587-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f587-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f587-135">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="3f587-135">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3f587-136">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="3f587-136">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="3f587-137">**glColor**</span><span class="sxs-lookup"><span data-stu-id="3f587-137">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="3f587-138">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="3f587-138">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="3f587-139">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="3f587-139">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3f587-140">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="3f587-140">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="3f587-141">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="3f587-141">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="3f587-142">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="3f587-142">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="3f587-143">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="3f587-143">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="3f587-144">**glRect**</span><span class="sxs-lookup"><span data-stu-id="3f587-144">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="3f587-145">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="3f587-145">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





