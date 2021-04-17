---
title: função glVertex2fv (GL. h)
description: Especifica um vértice. | função glVertex2fv (GL. h)
ms.assetid: bae32d27-2a19-40d5-a3f7-0e7a41918034
keywords:
- função glVertex2fv OpenGL
topic_type:
- apiref
api_name:
- glVertex2fv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ecd7a57aff2166f3605d7007cd194f5cff04784
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105755974"
---
# <a name="glvertex2fv-function"></a><span data-ttu-id="9f5ff-105">função glVertex2fv</span><span class="sxs-lookup"><span data-stu-id="9f5ff-105">glVertex2fv function</span></span>

<span data-ttu-id="9f5ff-106">Especifica um vértice.</span><span class="sxs-lookup"><span data-stu-id="9f5ff-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f5ff-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f5ff-107">Syntax</span></span>


```C++
void WINAPI glVertex2fv(
   const GLfloat *v
);
```



## <a name="parameters"></a><span data-ttu-id="9f5ff-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f5ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f5ff-109">*l*</span><span class="sxs-lookup"><span data-stu-id="9f5ff-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="9f5ff-110">Um ponteiro para uma matriz de dois elementos.</span><span class="sxs-lookup"><span data-stu-id="9f5ff-110">A pointer to an array of two elements.</span></span> <span data-ttu-id="9f5ff-111">Os elementos são as coordenadas x e y de um vértice.</span><span class="sxs-lookup"><span data-stu-id="9f5ff-111">The elements are the x and y coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f5ff-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9f5ff-112">Return value</span></span>

<span data-ttu-id="9f5ff-113">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9f5ff-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f5ff-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f5ff-114">Requirements</span></span>



| <span data-ttu-id="9f5ff-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f5ff-115">Requirement</span></span> | <span data-ttu-id="9f5ff-116">Valor</span><span class="sxs-lookup"><span data-stu-id="9f5ff-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f5ff-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f5ff-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9f5ff-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9f5ff-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9f5ff-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f5ff-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9f5ff-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9f5ff-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9f5ff-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9f5ff-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f5ff-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f5ff-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9f5ff-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9f5ff-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="9f5ff-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f5ff-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9f5ff-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9f5ff-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f5ff-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f5ff-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f5ff-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f5ff-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f5ff-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="9f5ff-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="9f5ff-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="9f5ff-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="9f5ff-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="9f5ff-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="9f5ff-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="9f5ff-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="9f5ff-132">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="9f5ff-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="9f5ff-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="9f5ff-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="9f5ff-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="9f5ff-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="9f5ff-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="9f5ff-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="9f5ff-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="9f5ff-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="9f5ff-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="9f5ff-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="9f5ff-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="9f5ff-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





