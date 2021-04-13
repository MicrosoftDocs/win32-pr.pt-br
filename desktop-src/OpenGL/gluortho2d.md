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
ms.openlocfilehash: a36b321f312a074a5dd78340968f1c9b2b844c6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369204"
---
# <a name="gluortho2d-function"></a><span data-ttu-id="ece02-104">função gluOrtho2D</span><span class="sxs-lookup"><span data-stu-id="ece02-104">gluOrtho2D function</span></span>

<span data-ttu-id="ece02-105">A função **gluOrtho2D** define uma matriz de projeção ortográfica 2D.</span><span class="sxs-lookup"><span data-stu-id="ece02-105">The **gluOrtho2D** function defines a 2-D orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="ece02-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ece02-106">Syntax</span></span>


```C++
void WINAPI gluOrtho2D(
   GLdouble left,
   GLdouble right,
   GLdouble top,
   GLdouble bottom
);
```



## <a name="parameters"></a><span data-ttu-id="ece02-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ece02-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ece02-108">*esquerda*</span><span class="sxs-lookup"><span data-stu-id="ece02-108">*left*</span></span> 
</dt> <dd>

<span data-ttu-id="ece02-109">A coordenada para o plano de recorte vertical esquerdo.</span><span class="sxs-lookup"><span data-stu-id="ece02-109">The coordinate for the left vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="ece02-110">*direita*</span><span class="sxs-lookup"><span data-stu-id="ece02-110">*right*</span></span> 
</dt> <dd>

<span data-ttu-id="ece02-111">A coordenada para o plano de recorte vertical direito.</span><span class="sxs-lookup"><span data-stu-id="ece02-111">The coordinate for the right vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="ece02-112">*início*</span><span class="sxs-lookup"><span data-stu-id="ece02-112">*top*</span></span> 
</dt> <dd>

<span data-ttu-id="ece02-113">A coordenada para o plano de recorte horizontal superior.</span><span class="sxs-lookup"><span data-stu-id="ece02-113">The coordinate for the top horizontal clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="ece02-114">*parte inferior*</span><span class="sxs-lookup"><span data-stu-id="ece02-114">*bottom*</span></span> 
</dt> <dd>

<span data-ttu-id="ece02-115">A coordenada para o plano de recorte horizontal inferior.</span><span class="sxs-lookup"><span data-stu-id="ece02-115">The coordinate for the bottom horizontal clipping plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ece02-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ece02-116">Return value</span></span>

<span data-ttu-id="ece02-117">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ece02-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ece02-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="ece02-118">Remarks</span></span>

<span data-ttu-id="ece02-119">A função **gluOrtho2D** configura uma região de exibição ortográfica bidimensional.</span><span class="sxs-lookup"><span data-stu-id="ece02-119">The **gluOrtho2D** function sets up a two-dimensional orthographic viewing region.</span></span> <span data-ttu-id="ece02-120">Isso é equivalente a chamar [**glOrtho**](glortho.md) com near = 1 e far = 1.</span><span class="sxs-lookup"><span data-stu-id="ece02-120">This is equivalent to calling [**glOrtho**](glortho.md) with near =  1 and far = 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="ece02-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ece02-121">Requirements</span></span>



| <span data-ttu-id="ece02-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ece02-122">Requirement</span></span> | <span data-ttu-id="ece02-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ece02-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ece02-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ece02-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ece02-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ece02-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ece02-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ece02-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ece02-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ece02-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ece02-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ece02-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ece02-129"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="ece02-129"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="ece02-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ece02-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="ece02-131"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ece02-131"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ece02-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ece02-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ece02-133"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ece02-133"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ece02-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="ece02-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ece02-135">**glOrtho**</span><span class="sxs-lookup"><span data-stu-id="ece02-135">**glOrtho**</span></span>](glortho.md)
</dt> <dt>

[<span data-ttu-id="ece02-136">**gluPerspective**</span><span class="sxs-lookup"><span data-stu-id="ece02-136">**gluPerspective**</span></span>](gluperspective.md)
</dt> </dl>

 

 





