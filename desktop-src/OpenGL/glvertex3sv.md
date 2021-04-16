---
title: função glVertex3sv (GL. h)
description: Especifica um vértice. | função glVertex3sv (GL. h)
ms.assetid: 8b819a95-f834-4c6e-b88a-a96ae9b36c71
keywords:
- função glVertex3sv OpenGL
topic_type:
- apiref
api_name:
- glVertex3sv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa808f76beefa440c3fa4a93a2301cf8b40dfcb2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105758029"
---
# <a name="glvertex3sv-function"></a><span data-ttu-id="e4793-105">função glVertex3sv</span><span class="sxs-lookup"><span data-stu-id="e4793-105">glVertex3sv function</span></span>

<span data-ttu-id="e4793-106">Especifica um vértice.</span><span class="sxs-lookup"><span data-stu-id="e4793-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4793-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4793-107">Syntax</span></span>


```C++
void WINAPI glVertex3sv(
   const GLshort *v
);
```



## <a name="parameters"></a><span data-ttu-id="e4793-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4793-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4793-109">*l*</span><span class="sxs-lookup"><span data-stu-id="e4793-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="e4793-110">Um ponteiro para uma matriz de três elementos.</span><span class="sxs-lookup"><span data-stu-id="e4793-110">A pointer to an array of three elements.</span></span> <span data-ttu-id="e4793-111">Os elementos são as coordenadas x, y e z de um vértice.</span><span class="sxs-lookup"><span data-stu-id="e4793-111">The elements are the x, y, and z coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4793-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e4793-112">Return value</span></span>

<span data-ttu-id="e4793-113">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e4793-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4793-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4793-114">Requirements</span></span>



| <span data-ttu-id="e4793-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4793-115">Requirement</span></span> | <span data-ttu-id="e4793-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e4793-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4793-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4793-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e4793-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e4793-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e4793-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4793-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e4793-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e4793-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e4793-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e4793-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4793-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4793-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e4793-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e4793-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="e4793-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4793-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e4793-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e4793-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4793-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4793-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4793-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4793-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4793-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e4793-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e4793-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="e4793-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="e4793-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="e4793-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="e4793-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="e4793-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="e4793-132">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="e4793-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e4793-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="e4793-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="e4793-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="e4793-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="e4793-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="e4793-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="e4793-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="e4793-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="e4793-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="e4793-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="e4793-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="e4793-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





