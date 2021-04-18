---
title: função glVertex3iv (GL. h)
description: Especifica um vértice. | função glVertex3iv (GL. h)
ms.assetid: db7e6a93-aaa2-402b-acd5-971c17451314
keywords:
- função glVertex3iv OpenGL
topic_type:
- apiref
api_name:
- glVertex3iv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bb0a5db3ebf30722573c9f7d0143b92046c8cb6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105770463"
---
# <a name="glvertex3iv-function"></a><span data-ttu-id="5e943-105">função glVertex3iv</span><span class="sxs-lookup"><span data-stu-id="5e943-105">glVertex3iv function</span></span>

<span data-ttu-id="5e943-106">Especifica um vértice.</span><span class="sxs-lookup"><span data-stu-id="5e943-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e943-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e943-107">Syntax</span></span>


```C++
void WINAPI glVertex3iv(
   const GLint *v
);
```



## <a name="parameters"></a><span data-ttu-id="5e943-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e943-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e943-109">*l*</span><span class="sxs-lookup"><span data-stu-id="5e943-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="5e943-110">Um ponteiro para uma matriz de três elementos.</span><span class="sxs-lookup"><span data-stu-id="5e943-110">A pointer to an array of three elements.</span></span> <span data-ttu-id="5e943-111">Os elementos são as coordenadas x, y e z de um vértice.</span><span class="sxs-lookup"><span data-stu-id="5e943-111">The elements are the x, y, and z coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e943-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5e943-112">Return value</span></span>

<span data-ttu-id="5e943-113">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="5e943-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e943-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e943-114">Requirements</span></span>



| <span data-ttu-id="5e943-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e943-115">Requirement</span></span> | <span data-ttu-id="5e943-116">Valor</span><span class="sxs-lookup"><span data-stu-id="5e943-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e943-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e943-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5e943-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5e943-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5e943-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e943-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5e943-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5e943-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5e943-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5e943-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e943-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e943-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="5e943-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5e943-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="5e943-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e943-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5e943-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5e943-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e943-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e943-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e943-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e943-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e943-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="5e943-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="5e943-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="5e943-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="5e943-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="5e943-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="5e943-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="5e943-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="5e943-132">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="5e943-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="5e943-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="5e943-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="5e943-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="5e943-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="5e943-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="5e943-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="5e943-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="5e943-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="5e943-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="5e943-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="5e943-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="5e943-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





