---
title: função gluOrtho2D (Glu. h)
description: A função gluOrtho2D define uma matriz de projeção ortográfica 2D.
ms.assetid: ba83fb5c-e5c7-4486-a815-a1aff0469757
keywords:
- função gluOrtho2D OpenGL
topic_type:
- apiref
api_name:
- gluOrtho2D
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf07fea583c5ae46680d888f6bf6c0a9c5aa9a0
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/19/2021
ms.locfileid: "110153549"
---
# <a name="gluortho2d-function"></a><span data-ttu-id="280dc-104">função gluOrtho2D</span><span class="sxs-lookup"><span data-stu-id="280dc-104">gluOrtho2D function</span></span>

<span data-ttu-id="280dc-105">A função **gluOrtho2D** define uma matriz de projeção ortográfica 2D.</span><span class="sxs-lookup"><span data-stu-id="280dc-105">The **gluOrtho2D** function defines a 2-D orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="280dc-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="280dc-106">Syntax</span></span>


```C++
void WINAPI gluOrtho2D(
   GLdouble left,
   GLdouble right,
   GLdouble top,
   GLdouble bottom
);
```



## <a name="parameters"></a><span data-ttu-id="280dc-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="280dc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="280dc-108">*esquerda*</span><span class="sxs-lookup"><span data-stu-id="280dc-108">*left*</span></span> 
</dt> <dd>

<span data-ttu-id="280dc-109">A coordenada para o plano de recorte vertical esquerdo.</span><span class="sxs-lookup"><span data-stu-id="280dc-109">The coordinate for the left vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="280dc-110">*direita*</span><span class="sxs-lookup"><span data-stu-id="280dc-110">*right*</span></span> 
</dt> <dd>

<span data-ttu-id="280dc-111">A coordenada para o plano de recorte vertical direito.</span><span class="sxs-lookup"><span data-stu-id="280dc-111">The coordinate for the right vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="280dc-112">*início*</span><span class="sxs-lookup"><span data-stu-id="280dc-112">*top*</span></span> 
</dt> <dd>

<span data-ttu-id="280dc-113">A coordenada para o plano de recorte horizontal superior.</span><span class="sxs-lookup"><span data-stu-id="280dc-113">The coordinate for the top horizontal clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="280dc-114">*parte inferior*</span><span class="sxs-lookup"><span data-stu-id="280dc-114">*bottom*</span></span> 
</dt> <dd>

<span data-ttu-id="280dc-115">A coordenada para o plano de recorte horizontal inferior.</span><span class="sxs-lookup"><span data-stu-id="280dc-115">The coordinate for the bottom horizontal clipping plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="280dc-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="280dc-116">Return value</span></span>

<span data-ttu-id="280dc-117">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="280dc-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="280dc-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="280dc-118">Remarks</span></span>

<span data-ttu-id="280dc-119">A função **gluOrtho2D** configura uma região de exibição ortográfica bidimensional.</span><span class="sxs-lookup"><span data-stu-id="280dc-119">The **gluOrtho2D** function sets up a two-dimensional orthographic viewing region.</span></span> <span data-ttu-id="280dc-120">Isso é equivalente a chamar [**glOrtho**](glortho.md) com zNear =-1 e zFar = 1.</span><span class="sxs-lookup"><span data-stu-id="280dc-120">This is equivalent to calling [**glOrtho**](glortho.md) with zNear = -1 and zFar = 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="280dc-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="280dc-121">Requirements</span></span>



| <span data-ttu-id="280dc-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="280dc-122">Requirement</span></span> | <span data-ttu-id="280dc-123">Valor</span><span class="sxs-lookup"><span data-stu-id="280dc-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="280dc-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="280dc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="280dc-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="280dc-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="280dc-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="280dc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="280dc-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="280dc-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="280dc-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="280dc-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="280dc-129"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="280dc-129"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="280dc-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="280dc-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="280dc-131"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="280dc-131"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="280dc-132">DLL</span><span class="sxs-lookup"><span data-stu-id="280dc-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="280dc-133"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="280dc-133"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="280dc-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="280dc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="280dc-135">**glOrtho**</span><span class="sxs-lookup"><span data-stu-id="280dc-135">**glOrtho**</span></span>](glortho.md)
</dt> <dt>

[<span data-ttu-id="280dc-136">**gluPerspective**</span><span class="sxs-lookup"><span data-stu-id="280dc-136">**gluPerspective**</span></span>](gluperspective.md)
</dt> </dl>

 

 





