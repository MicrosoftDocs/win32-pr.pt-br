---
title: função glVertex4iv (GL. h)
description: Especifica um vértice. | função glVertex4iv (GL. h)
ms.assetid: 7b56777a-f904-4a9d-8d3d-84a38cbf0b45
keywords:
- função glVertex4iv OpenGL
topic_type:
- apiref
api_name:
- glVertex4iv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ff55c5534245843d5caa8797b2b529c7cfe00f9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103837912"
---
# <a name="glvertex4iv-function"></a><span data-ttu-id="cef0e-105">função glVertex4iv</span><span class="sxs-lookup"><span data-stu-id="cef0e-105">glVertex4iv function</span></span>

<span data-ttu-id="cef0e-106">Especifica um vértice.</span><span class="sxs-lookup"><span data-stu-id="cef0e-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="cef0e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cef0e-107">Syntax</span></span>


```C++
void WINAPI glVertex4iv(
   const GLint *v
);
```



## <a name="parameters"></a><span data-ttu-id="cef0e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cef0e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cef0e-109">*l*</span><span class="sxs-lookup"><span data-stu-id="cef0e-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="cef0e-110">Um ponteiro para uma matriz de quatro elementos.</span><span class="sxs-lookup"><span data-stu-id="cef0e-110">A pointer to an array of four elements.</span></span> <span data-ttu-id="cef0e-111">Os elementos são as coordenadas x, y, z e w de um vértice.</span><span class="sxs-lookup"><span data-stu-id="cef0e-111">The elements are the x, y, z, and w coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cef0e-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cef0e-112">Return value</span></span>

<span data-ttu-id="cef0e-113">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="cef0e-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cef0e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cef0e-114">Requirements</span></span>



| <span data-ttu-id="cef0e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cef0e-115">Requirement</span></span> | <span data-ttu-id="cef0e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="cef0e-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cef0e-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cef0e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cef0e-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cef0e-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="cef0e-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cef0e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cef0e-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cef0e-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cef0e-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cef0e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cef0e-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="cef0e-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="cef0e-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cef0e-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="cef0e-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cef0e-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="cef0e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="cef0e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cef0e-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cef0e-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cef0e-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="cef0e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cef0e-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="cef0e-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="cef0e-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="cef0e-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="cef0e-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="cef0e-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="cef0e-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="cef0e-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="cef0e-132">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="cef0e-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="cef0e-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="cef0e-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="cef0e-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="cef0e-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="cef0e-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="cef0e-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="cef0e-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="cef0e-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="cef0e-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="cef0e-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="cef0e-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="cef0e-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





