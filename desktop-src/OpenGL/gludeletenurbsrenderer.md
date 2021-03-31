---
title: função gluDeleteNurbsRenderer (Glu. h)
description: A função gluDeleteNurbsRenderer destrói um objeto B-spline racional não uniforme (NURBS).
ms.assetid: 77063dcb-90b8-47e4-8b00-e1c46cf4f712
keywords:
- função gluDeleteNurbsRenderer OpenGL
topic_type:
- apiref
api_name:
- gluDeleteNurbsRenderer
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fb6ecf0bbb7076d4d6292676d3d358586d0986c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644629"
---
# <a name="gludeletenurbsrenderer-function"></a><span data-ttu-id="1c60f-104">função gluDeleteNurbsRenderer</span><span class="sxs-lookup"><span data-stu-id="1c60f-104">gluDeleteNurbsRenderer function</span></span>

<span data-ttu-id="1c60f-105">A função **gluDeleteNurbsRenderer** destrói um objeto B-spline racional não uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="1c60f-105">The **gluDeleteNurbsRenderer** function destroys a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c60f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1c60f-106">Syntax</span></span>


```C++
void WINAPI gluDeleteNurbsRenderer(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a><span data-ttu-id="1c60f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1c60f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c60f-108">*nobj*</span><span class="sxs-lookup"><span data-stu-id="1c60f-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="1c60f-109">O objeto NURBS a ser destruído (criado com **gluNewNurbsRenderer**).</span><span class="sxs-lookup"><span data-stu-id="1c60f-109">The NURBS object to be destroyed (created with **gluNewNurbsRenderer**).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c60f-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1c60f-110">Return value</span></span>

<span data-ttu-id="1c60f-111">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1c60f-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c60f-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="1c60f-112">Remarks</span></span>

<span data-ttu-id="1c60f-113">A função **gluDeleteNurbsRenderer** destrói o objeto NURBS e libera qualquer memória usada.</span><span class="sxs-lookup"><span data-stu-id="1c60f-113">The **gluDeleteNurbsRenderer** function destroys the NURBS object and frees any memory that it used.</span></span> <span data-ttu-id="1c60f-114">Depois de ter chamado **gluDeleteNurbsRenderer**, você não poderá usar o *nobj* novamente.</span><span class="sxs-lookup"><span data-stu-id="1c60f-114">After you have called **gluDeleteNurbsRenderer**, you cannot use *nobj* again.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c60f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c60f-115">Requirements</span></span>



| <span data-ttu-id="1c60f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c60f-116">Requirement</span></span> | <span data-ttu-id="1c60f-117">Valor</span><span class="sxs-lookup"><span data-stu-id="1c60f-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1c60f-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1c60f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1c60f-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1c60f-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1c60f-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1c60f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1c60f-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1c60f-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1c60f-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1c60f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c60f-123"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c60f-123"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="1c60f-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1c60f-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="1c60f-125"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c60f-125"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1c60f-126">DLL</span><span class="sxs-lookup"><span data-stu-id="1c60f-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c60f-127"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c60f-127"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c60f-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="1c60f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c60f-129">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="1c60f-129">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> </dl>

 

 





