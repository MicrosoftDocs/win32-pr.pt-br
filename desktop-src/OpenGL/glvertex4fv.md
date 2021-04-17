---
title: função glVertex4fv (GL. h)
description: Especifica um vértice. | função glVertex4fv (GL. h)
ms.assetid: c2a766fd-3ad8-463b-8f09-36d0673e6716
keywords:
- função glVertex4fv OpenGL
topic_type:
- apiref
api_name:
- glVertex4fv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e05551268b697ba4444c29d5f2b9bdfb0e832e4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105762036"
---
# <a name="glvertex4fv-function"></a><span data-ttu-id="76c69-105">função glVertex4fv</span><span class="sxs-lookup"><span data-stu-id="76c69-105">glVertex4fv function</span></span>

<span data-ttu-id="76c69-106">Especifica um vértice.</span><span class="sxs-lookup"><span data-stu-id="76c69-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="76c69-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="76c69-107">Syntax</span></span>


```C++
void WINAPI glVertex4fv(
   const GLfloat *v
);
```



## <a name="parameters"></a><span data-ttu-id="76c69-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76c69-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76c69-109">*l*</span><span class="sxs-lookup"><span data-stu-id="76c69-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="76c69-110">Um ponteiro para uma matriz de quatro elementos.</span><span class="sxs-lookup"><span data-stu-id="76c69-110">A pointer to an array of four elements.</span></span> <span data-ttu-id="76c69-111">Os elementos são as coordenadas x, y, z e w de um vértice.</span><span class="sxs-lookup"><span data-stu-id="76c69-111">The elements are the x, y, z, and w coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76c69-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="76c69-112">Return value</span></span>

<span data-ttu-id="76c69-113">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="76c69-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="76c69-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76c69-114">Requirements</span></span>



| <span data-ttu-id="76c69-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="76c69-115">Requirement</span></span> | <span data-ttu-id="76c69-116">Valor</span><span class="sxs-lookup"><span data-stu-id="76c69-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="76c69-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76c69-117">Minimum supported client</span></span><br/> | <span data-ttu-id="76c69-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="76c69-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="76c69-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76c69-119">Minimum supported server</span></span><br/> | <span data-ttu-id="76c69-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="76c69-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="76c69-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="76c69-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="76c69-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="76c69-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="76c69-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="76c69-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="76c69-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="76c69-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="76c69-125">DLL</span><span class="sxs-lookup"><span data-stu-id="76c69-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76c69-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76c69-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76c69-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="76c69-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76c69-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="76c69-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="76c69-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="76c69-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="76c69-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="76c69-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="76c69-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="76c69-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="76c69-132">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="76c69-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="76c69-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="76c69-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="76c69-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="76c69-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="76c69-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="76c69-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="76c69-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="76c69-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="76c69-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="76c69-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="76c69-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="76c69-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





