---
title: função gluNewQuadric (Glu. h)
description: A função gluNewQuadric cria um objeto Quadric.
ms.assetid: 5a4289bf-b57a-4c74-b0e3-b7536671e4df
keywords:
- função gluNewQuadric OpenGL
topic_type:
- apiref
api_name:
- gluNewQuadric
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: affedc7dcebd2b7925449e22cc1b902e88d936f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918677"
---
# <a name="glunewquadric-function"></a><span data-ttu-id="1932e-104">função gluNewQuadric</span><span class="sxs-lookup"><span data-stu-id="1932e-104">gluNewQuadric function</span></span>

<span data-ttu-id="1932e-105">A função **gluNewQuadric** cria um objeto Quadric.</span><span class="sxs-lookup"><span data-stu-id="1932e-105">The **gluNewQuadric** function creates a quadric object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1932e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1932e-106">Syntax</span></span>


```C++
GLUquadric* WINAPI gluNewQuadric(void);
```



## <a name="parameters"></a><span data-ttu-id="1932e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1932e-107">Parameters</span></span>

<span data-ttu-id="1932e-108">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="1932e-108">This function has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="1932e-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="1932e-109">Remarks</span></span>

<span data-ttu-id="1932e-110">A função **gluNewQuadric** cria e retorna um ponteiro para um novo objeto Quadric.</span><span class="sxs-lookup"><span data-stu-id="1932e-110">The **gluNewQuadric** function creates and returns a pointer to a new quadric object.</span></span> <span data-ttu-id="1932e-111">Consulte este objeto ao chamar funções de controle e processamento de Quadric.</span><span class="sxs-lookup"><span data-stu-id="1932e-111">Refer to this object when calling quadric rendering and control functions.</span></span> <span data-ttu-id="1932e-112">Um valor de retorno igual a zero significa que não há memória suficiente para alocar para o objeto.</span><span class="sxs-lookup"><span data-stu-id="1932e-112">A return value of zero means there is not enough memory to allocate to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="1932e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1932e-113">Requirements</span></span>



| <span data-ttu-id="1932e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1932e-114">Requirement</span></span> | <span data-ttu-id="1932e-115">Valor</span><span class="sxs-lookup"><span data-stu-id="1932e-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1932e-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1932e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1932e-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1932e-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1932e-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1932e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1932e-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1932e-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1932e-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1932e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1932e-121"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="1932e-121"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="1932e-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1932e-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="1932e-123"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1932e-123"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1932e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="1932e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1932e-125"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1932e-125"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1932e-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="1932e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1932e-127">**gluCylinder**</span><span class="sxs-lookup"><span data-stu-id="1932e-127">**gluCylinder**</span></span>](glucylinder.md)
</dt> <dt>

[<span data-ttu-id="1932e-128">**gluDeleteQuadric**</span><span class="sxs-lookup"><span data-stu-id="1932e-128">**gluDeleteQuadric**</span></span>](gludeletequadric.md)
</dt> <dt>

[<span data-ttu-id="1932e-129">**gluDisk**</span><span class="sxs-lookup"><span data-stu-id="1932e-129">**gluDisk**</span></span>](gludisk.md)
</dt> <dt>

[<span data-ttu-id="1932e-130">**gluPartialDisk**</span><span class="sxs-lookup"><span data-stu-id="1932e-130">**gluPartialDisk**</span></span>](glupartialdisk.md)
</dt> <dt>

[<span data-ttu-id="1932e-131">*gluQuadricCallback*</span><span class="sxs-lookup"><span data-stu-id="1932e-131">*gluQuadricCallback*</span></span>](gluquadric.md)
</dt> <dt>

[<span data-ttu-id="1932e-132">**gluQuadricDrawStyle**</span><span class="sxs-lookup"><span data-stu-id="1932e-132">**gluQuadricDrawStyle**</span></span>](gluquadricdrawstyle.md)
</dt> <dt>

[<span data-ttu-id="1932e-133">**gluQuadricNormals**</span><span class="sxs-lookup"><span data-stu-id="1932e-133">**gluQuadricNormals**</span></span>](gluquadricnormals.md)
</dt> <dt>

[<span data-ttu-id="1932e-134">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="1932e-134">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="1932e-135">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="1932e-135">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> <dt>

[<span data-ttu-id="1932e-136">**gluSphere**</span><span class="sxs-lookup"><span data-stu-id="1932e-136">**gluSphere**</span></span>](glusphere.md)
</dt> </dl>

 

 





