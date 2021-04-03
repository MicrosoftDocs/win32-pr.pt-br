---
title: função glVertex4f (GL. h)
description: Especifica um vértice. | função glVertex4f (GL. h)
ms.assetid: 877fce8c-095e-4ae4-8633-7c84659ee8a6
keywords:
- função glVertex4f OpenGL
topic_type:
- apiref
api_name:
- glVertex4f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b07852c1199338917ca1f29c54923ba6a904f30f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930355"
---
# <a name="glvertex4f-function"></a><span data-ttu-id="4453b-105">função glVertex4f</span><span class="sxs-lookup"><span data-stu-id="4453b-105">glVertex4f function</span></span>

<span data-ttu-id="4453b-106">Especifica um vértice.</span><span class="sxs-lookup"><span data-stu-id="4453b-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="4453b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4453b-107">Syntax</span></span>


```C++
void WINAPI glVertex4f(
   GLfloat x,
   GLfloat y,
   GLfloat z,
   GLfloat w
);
```



## <a name="parameters"></a><span data-ttu-id="4453b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4453b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4453b-109">*x*</span><span class="sxs-lookup"><span data-stu-id="4453b-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="4453b-110">Especifica a coordenada x de um vértice.</span><span class="sxs-lookup"><span data-stu-id="4453b-110">Specifies the x-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="4453b-111">*y*</span><span class="sxs-lookup"><span data-stu-id="4453b-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="4453b-112">Especifica a coordenada y de um vértice.</span><span class="sxs-lookup"><span data-stu-id="4453b-112">Specifies the y-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="4453b-113">*z*</span><span class="sxs-lookup"><span data-stu-id="4453b-113">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="4453b-114">Especifica a coordenada z de um vértice.</span><span class="sxs-lookup"><span data-stu-id="4453b-114">Specifies the z-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="4453b-115">*w*</span><span class="sxs-lookup"><span data-stu-id="4453b-115">*w*</span></span> 
</dt> <dd>

<span data-ttu-id="4453b-116">Especifica a coordenada w de um vértice.</span><span class="sxs-lookup"><span data-stu-id="4453b-116">Specifies the w-coordinate of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4453b-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4453b-117">Return value</span></span>

<span data-ttu-id="4453b-118">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4453b-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4453b-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="4453b-119">Remarks</span></span>

<span data-ttu-id="4453b-120">Os comandos de função glVertex são usados em pares [**glBegin**](glbegin.md) / [**glEnd**](glend.md) para especificar vértices de ponto, linha e polígono.</span><span class="sxs-lookup"><span data-stu-id="4453b-120">The glVertex function commands are used within [**glBegin**](glbegin.md)/[**glEnd**](glend.md) pairs to specify point, line, and polygon vertices.</span></span> <span data-ttu-id="4453b-121">As coordenadas de cor atual, normal e de textura são associadas ao vértice quando glVertex é chamado.</span><span class="sxs-lookup"><span data-stu-id="4453b-121">The current color, normal, and texture coordinates are associated with the vertex when glVertex is called.</span></span> <span data-ttu-id="4453b-122">Quando apenas *x* e *y* são especificados, *z* usa como padrão 0,0 e *w* é o padrão de 1,0.</span><span class="sxs-lookup"><span data-stu-id="4453b-122">When only *x* and *y* are specified, *z* defaults to 0.0 and *w* defaults to 1.0.</span></span> <span data-ttu-id="4453b-123">Quando *x*, *y* e *z* são especificados, *w* assume o padrão de 1,0.</span><span class="sxs-lookup"><span data-stu-id="4453b-123">When *x*, *y*, and *z* are specified, *w* defaults to 1.0.</span></span> <span data-ttu-id="4453b-124">Invocar glVertex fora de um par **glBegin** / **glEnd** resulta em um comportamento indefinido.</span><span class="sxs-lookup"><span data-stu-id="4453b-124">Invoking glVertex outside of a **glBegin**/**glEnd** pair results in undefined behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="4453b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4453b-125">Requirements</span></span>



| <span data-ttu-id="4453b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4453b-126">Requirement</span></span> | <span data-ttu-id="4453b-127">Valor</span><span class="sxs-lookup"><span data-stu-id="4453b-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4453b-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4453b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4453b-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4453b-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4453b-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4453b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4453b-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4453b-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4453b-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4453b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="4453b-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="4453b-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="4453b-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4453b-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="4453b-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4453b-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4453b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="4453b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4453b-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4453b-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4453b-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="4453b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4453b-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="4453b-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="4453b-140">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="4453b-140">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="4453b-141">**glColor**</span><span class="sxs-lookup"><span data-stu-id="4453b-141">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="4453b-142">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="4453b-142">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="4453b-143">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="4453b-143">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="4453b-144">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="4453b-144">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="4453b-145">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="4453b-145">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="4453b-146">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="4453b-146">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="4453b-147">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="4453b-147">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="4453b-148">**glRect**</span><span class="sxs-lookup"><span data-stu-id="4453b-148">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="4453b-149">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="4453b-149">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





