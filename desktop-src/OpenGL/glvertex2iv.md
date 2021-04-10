---
title: função glVertex2iv (GL. h)
description: Especifica um vértice. | função glVertex2iv (GL. h)
ms.assetid: 3b88bf7d-5743-4ac0-a79f-5f450b488bd2
keywords:
- função glVertex2iv OpenGL
topic_type:
- apiref
api_name:
- glVertex2iv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 594c50ff1e30184d5a7292c5b639f16a48f0820b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104012050"
---
# <a name="glvertex2iv-function"></a><span data-ttu-id="8f365-105">função glVertex2iv</span><span class="sxs-lookup"><span data-stu-id="8f365-105">glVertex2iv function</span></span>

<span data-ttu-id="8f365-106">Especifica um vértice.</span><span class="sxs-lookup"><span data-stu-id="8f365-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f365-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f365-107">Syntax</span></span>


```C++
void WINAPI glVertex2iv(
   const GLint *v
);
```



## <a name="parameters"></a><span data-ttu-id="8f365-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f365-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f365-109">*l*</span><span class="sxs-lookup"><span data-stu-id="8f365-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="8f365-110">Um ponteiro para uma matriz de dois elementos.</span><span class="sxs-lookup"><span data-stu-id="8f365-110">A pointer to an array of two elements.</span></span> <span data-ttu-id="8f365-111">Os elementos são as coordenadas x e y de um vértice.</span><span class="sxs-lookup"><span data-stu-id="8f365-111">The elements are the x and y coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f365-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8f365-112">Return value</span></span>

<span data-ttu-id="8f365-113">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8f365-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f365-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f365-114">Requirements</span></span>



| <span data-ttu-id="8f365-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f365-115">Requirement</span></span> | <span data-ttu-id="8f365-116">Valor</span><span class="sxs-lookup"><span data-stu-id="8f365-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f365-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f365-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8f365-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8f365-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8f365-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f365-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8f365-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8f365-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8f365-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8f365-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f365-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f365-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="8f365-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8f365-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="8f365-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f365-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8f365-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8f365-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f365-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f365-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f365-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f365-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f365-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="8f365-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="8f365-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="8f365-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="8f365-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="8f365-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="8f365-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="8f365-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="8f365-132">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="8f365-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="8f365-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="8f365-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="8f365-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="8f365-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="8f365-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="8f365-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="8f365-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="8f365-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="8f365-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="8f365-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="8f365-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="8f365-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





