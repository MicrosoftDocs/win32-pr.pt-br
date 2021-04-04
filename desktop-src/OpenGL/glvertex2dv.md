---
title: função glVertex2dv (GL. h)
description: Especifica um vértice. | função glVertex2dv (GL. h)
ms.assetid: b685d0aa-2874-4ad9-a20c-86823e9ad00b
keywords:
- função glVertex2dv OpenGL
topic_type:
- apiref
api_name:
- glVertex2dv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4839fa650302a67c98a0aef3d227dfafa8ddb688
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930351"
---
# <a name="glvertex2dv-function"></a><span data-ttu-id="3313e-105">função glVertex2dv</span><span class="sxs-lookup"><span data-stu-id="3313e-105">glVertex2dv function</span></span>

<span data-ttu-id="3313e-106">Especifica um vértice.</span><span class="sxs-lookup"><span data-stu-id="3313e-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="3313e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3313e-107">Syntax</span></span>


```C++
void WINAPI glVertex2dv(
   const GLdouble *v
);
```



## <a name="parameters"></a><span data-ttu-id="3313e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3313e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3313e-109">*l*</span><span class="sxs-lookup"><span data-stu-id="3313e-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="3313e-110">Um ponteiro para uma matriz de dois elementos.</span><span class="sxs-lookup"><span data-stu-id="3313e-110">A pointer to an array of two elements.</span></span> <span data-ttu-id="3313e-111">Os elementos são as coordenadas x e y de um vértice.</span><span class="sxs-lookup"><span data-stu-id="3313e-111">The elements are the x and y coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3313e-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3313e-112">Return value</span></span>

<span data-ttu-id="3313e-113">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3313e-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3313e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3313e-114">Requirements</span></span>



| <span data-ttu-id="3313e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3313e-115">Requirement</span></span> | <span data-ttu-id="3313e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="3313e-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3313e-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3313e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3313e-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3313e-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3313e-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3313e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3313e-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3313e-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3313e-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3313e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3313e-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3313e-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3313e-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3313e-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="3313e-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3313e-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3313e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3313e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3313e-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3313e-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3313e-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="3313e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3313e-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="3313e-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3313e-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="3313e-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="3313e-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="3313e-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="3313e-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="3313e-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="3313e-132">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="3313e-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3313e-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="3313e-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="3313e-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="3313e-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="3313e-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="3313e-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="3313e-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="3313e-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="3313e-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="3313e-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="3313e-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="3313e-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





