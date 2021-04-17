---
title: função glVertex4dv (GL. h)
description: Especifica um vértice. | função glVertex4dv (GL. h)
ms.assetid: af0a3c69-0d71-4cbb-9494-561033d99ac1
keywords:
- função glVertex4dv OpenGL
topic_type:
- apiref
api_name:
- glVertex4dv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 532a71c576ca0b49dd645afe8b501f0e718a827b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105811071"
---
# <a name="glvertex4dv-function"></a><span data-ttu-id="c57ac-105">função glVertex4dv</span><span class="sxs-lookup"><span data-stu-id="c57ac-105">glVertex4dv function</span></span>

<span data-ttu-id="c57ac-106">Especifica um vértice.</span><span class="sxs-lookup"><span data-stu-id="c57ac-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="c57ac-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c57ac-107">Syntax</span></span>


```C++
void WINAPI glVertex4dv(
   const GLdouble *v
);
```



## <a name="parameters"></a><span data-ttu-id="c57ac-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c57ac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c57ac-109">*l*</span><span class="sxs-lookup"><span data-stu-id="c57ac-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="c57ac-110">Um ponteiro para uma matriz de quatro elementos.</span><span class="sxs-lookup"><span data-stu-id="c57ac-110">A pointer to an array of four elements.</span></span> <span data-ttu-id="c57ac-111">Os elementos são as coordenadas x, y, z e w de um vértice.</span><span class="sxs-lookup"><span data-stu-id="c57ac-111">The elements are the x, y, z, and w coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c57ac-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c57ac-112">Return value</span></span>

<span data-ttu-id="c57ac-113">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c57ac-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c57ac-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c57ac-114">Requirements</span></span>



| <span data-ttu-id="c57ac-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c57ac-115">Requirement</span></span> | <span data-ttu-id="c57ac-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c57ac-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c57ac-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c57ac-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c57ac-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c57ac-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c57ac-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c57ac-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c57ac-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c57ac-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c57ac-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c57ac-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c57ac-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c57ac-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c57ac-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c57ac-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="c57ac-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c57ac-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c57ac-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c57ac-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c57ac-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c57ac-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c57ac-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="c57ac-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c57ac-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="c57ac-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="c57ac-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="c57ac-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="c57ac-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="c57ac-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="c57ac-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="c57ac-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="c57ac-132">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="c57ac-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="c57ac-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="c57ac-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="c57ac-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="c57ac-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="c57ac-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="c57ac-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="c57ac-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="c57ac-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="c57ac-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="c57ac-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="c57ac-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="c57ac-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





