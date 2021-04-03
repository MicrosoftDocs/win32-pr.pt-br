---
title: função gluNewNurbsRenderer (Glu. h)
description: A função gluNewNurbsRenderer cria um objeto B-spline racional não uniforme (NURBS).
ms.assetid: f47badb0-6b75-4bfd-9771-516668d9e255
keywords:
- função gluNewNurbsRenderer OpenGL
topic_type:
- apiref
api_name:
- gluNewNurbsRenderer
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b6e35df5abd9fb9e7757dd79066fbbe7efe8680
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918678"
---
# <a name="glunewnurbsrenderer-function"></a><span data-ttu-id="eb24e-104">função gluNewNurbsRenderer</span><span class="sxs-lookup"><span data-stu-id="eb24e-104">gluNewNurbsRenderer function</span></span>

<span data-ttu-id="eb24e-105">A função **gluNewNurbsRenderer** cria um objeto B-spline racional não uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="eb24e-105">The **gluNewNurbsRenderer** function creates a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb24e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb24e-106">Syntax</span></span>


```C++
GLUnurbs* WINAPI gluNewNurbsRenderer(void);
```



## <a name="parameters"></a><span data-ttu-id="eb24e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb24e-107">Parameters</span></span>

<span data-ttu-id="eb24e-108">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="eb24e-108">This function has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb24e-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb24e-109">Remarks</span></span>

<span data-ttu-id="eb24e-110">A função **gluNewNurbsRenderer** cria e retorna um ponteiro para um novo objeto NURBS.</span><span class="sxs-lookup"><span data-stu-id="eb24e-110">The **gluNewNurbsRenderer** function creates and returns a pointer to a new NURBS object.</span></span> <span data-ttu-id="eb24e-111">Consulte este objeto ao chamar funções de controle e renderização NURBS.</span><span class="sxs-lookup"><span data-stu-id="eb24e-111">Refer to this object when calling NURBS rendering and control functions.</span></span> <span data-ttu-id="eb24e-112">Um valor de retorno igual a zero significa que não há memória suficiente para alocar para o objeto.</span><span class="sxs-lookup"><span data-stu-id="eb24e-112">A return value of zero means there is not enough memory to allocate to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb24e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb24e-113">Requirements</span></span>



| <span data-ttu-id="eb24e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb24e-114">Requirement</span></span> | <span data-ttu-id="eb24e-115">Valor</span><span class="sxs-lookup"><span data-stu-id="eb24e-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="eb24e-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb24e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="eb24e-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="eb24e-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="eb24e-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eb24e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="eb24e-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="eb24e-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="eb24e-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="eb24e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb24e-121"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb24e-121"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="eb24e-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eb24e-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="eb24e-123"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb24e-123"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="eb24e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="eb24e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb24e-125"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb24e-125"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb24e-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb24e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb24e-127">**gluBeginCurve**</span><span class="sxs-lookup"><span data-stu-id="eb24e-127">**gluBeginCurve**</span></span>](glubegincurve.md)
</dt> <dt>

[<span data-ttu-id="eb24e-128">**gluBeginSurface**</span><span class="sxs-lookup"><span data-stu-id="eb24e-128">**gluBeginSurface**</span></span>](glubeginsurface.md)
</dt> <dt>

[<span data-ttu-id="eb24e-129">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="eb24e-129">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="eb24e-130">**gluDeleteNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="eb24e-130">**gluDeleteNurbsRenderer**</span></span>](gludeletenurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="eb24e-131">*gluNurbsCallback*</span><span class="sxs-lookup"><span data-stu-id="eb24e-131">*gluNurbsCallback*</span></span>](glunurbs.md)
</dt> <dt>

[<span data-ttu-id="eb24e-132">**gluNurbsProperty**</span><span class="sxs-lookup"><span data-stu-id="eb24e-132">**gluNurbsProperty**</span></span>](glunurbsproperty.md)
</dt> </dl>

 

 





