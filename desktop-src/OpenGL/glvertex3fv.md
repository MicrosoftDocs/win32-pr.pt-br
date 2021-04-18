---
title: função glVertex3fv (GL. h)
description: Especifica um vértice. | função glVertex3fv (GL. h)
ms.assetid: d8790ffe-73b1-49d8-a7f5-2117177573ac
keywords:
- função glVertex3fv OpenGL
topic_type:
- apiref
api_name:
- glVertex3fv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f3bcbe73d071bc18e3a1a58ef2f505fa9bd6a3b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105760031"
---
# <a name="glvertex3fv-function"></a><span data-ttu-id="b2635-105">função glVertex3fv</span><span class="sxs-lookup"><span data-stu-id="b2635-105">glVertex3fv function</span></span>

<span data-ttu-id="b2635-106">Especifica um vértice.</span><span class="sxs-lookup"><span data-stu-id="b2635-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2635-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b2635-107">Syntax</span></span>


```C++
void WINAPI glVertex3fv(
   const GLfloat *v
);
```



## <a name="parameters"></a><span data-ttu-id="b2635-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b2635-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2635-109">*l*</span><span class="sxs-lookup"><span data-stu-id="b2635-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="b2635-110">Um ponteiro para uma matriz de três elementos.</span><span class="sxs-lookup"><span data-stu-id="b2635-110">A pointer to an array of three elements.</span></span> <span data-ttu-id="b2635-111">Os elementos são as coordenadas x, y e z de um vértice.</span><span class="sxs-lookup"><span data-stu-id="b2635-111">The elements are the x, y, and z coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2635-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b2635-112">Return value</span></span>

<span data-ttu-id="b2635-113">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b2635-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2635-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2635-114">Requirements</span></span>



| <span data-ttu-id="b2635-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2635-115">Requirement</span></span> | <span data-ttu-id="b2635-116">Valor</span><span class="sxs-lookup"><span data-stu-id="b2635-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2635-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b2635-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b2635-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b2635-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b2635-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b2635-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b2635-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b2635-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b2635-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b2635-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2635-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2635-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b2635-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b2635-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="b2635-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2635-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b2635-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b2635-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2635-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2635-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2635-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2635-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2635-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b2635-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b2635-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="b2635-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="b2635-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="b2635-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="b2635-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="b2635-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="b2635-132">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b2635-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b2635-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="b2635-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="b2635-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="b2635-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="b2635-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="b2635-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="b2635-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="b2635-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="b2635-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="b2635-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="b2635-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="b2635-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





