---
title: função gluPerspective (Glu. h)
description: A função gluPerspective configura uma matriz de projeção em perspectiva.
ms.assetid: 125e2828-a2d7-4c6c-9370-eb21a581ced8
keywords:
- função gluPerspective OpenGL
topic_type:
- apiref
api_name:
- gluPerspective
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf30fc7dc4c6ba5a56efd3def6a5a7178f81ed49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369813"
---
# <a name="gluperspective-function"></a><span data-ttu-id="ece83-104">função gluPerspective</span><span class="sxs-lookup"><span data-stu-id="ece83-104">gluPerspective function</span></span>

<span data-ttu-id="ece83-105">A função **gluPerspective** configura uma matriz de projeção em perspectiva.</span><span class="sxs-lookup"><span data-stu-id="ece83-105">The **gluPerspective** function sets up a perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="ece83-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ece83-106">Syntax</span></span>


```C++
void WINAPI gluPerspective(
   GLdouble fovy,
   GLdouble aspect,
   GLdouble zNear,
   GLdouble zFar
);
```



## <a name="parameters"></a><span data-ttu-id="ece83-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ece83-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ece83-108">*fovy*</span><span class="sxs-lookup"><span data-stu-id="ece83-108">*fovy*</span></span> 
</dt> <dd>

<span data-ttu-id="ece83-109">O campo de ângulo de exibição, em graus, na direção y.</span><span class="sxs-lookup"><span data-stu-id="ece83-109">The field of view angle, in degrees, in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="ece83-110">*aspect*</span><span class="sxs-lookup"><span data-stu-id="ece83-110">*aspect*</span></span> 
</dt> <dd>

<span data-ttu-id="ece83-111">A taxa de proporção que determina o campo de exibição na direção x.</span><span class="sxs-lookup"><span data-stu-id="ece83-111">The aspect ratio that determines the field of view in the x-direction.</span></span> <span data-ttu-id="ece83-112">A taxa de proporção é a proporção entre *x* (largura) e *y* (altura).</span><span class="sxs-lookup"><span data-stu-id="ece83-112">The aspect ratio is the ratio of *x* (width) to *y* (height).</span></span>

</dd> <dt>

<span data-ttu-id="ece83-113">*zNear*</span><span class="sxs-lookup"><span data-stu-id="ece83-113">*zNear*</span></span> 
</dt> <dd>

<span data-ttu-id="ece83-114">A distância do visualizador para o plano de recorte próximo (sempre positivo).</span><span class="sxs-lookup"><span data-stu-id="ece83-114">The distance from the viewer to the near clipping plane (always positive).</span></span>

</dd> <dt>

<span data-ttu-id="ece83-115">*zFar*</span><span class="sxs-lookup"><span data-stu-id="ece83-115">*zFar*</span></span> 
</dt> <dd>

<span data-ttu-id="ece83-116">A distância do visualizador até o plano de recorte distante (sempre positivo).</span><span class="sxs-lookup"><span data-stu-id="ece83-116">The distance from the viewer to the far clipping plane (always positive).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ece83-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ece83-117">Return value</span></span>

<span data-ttu-id="ece83-118">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ece83-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ece83-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="ece83-119">Remarks</span></span>

<span data-ttu-id="ece83-120">A função **gluPerspective** especifica um frustum de exibição no sistema de coordenadas mundiais.</span><span class="sxs-lookup"><span data-stu-id="ece83-120">The **gluPerspective** function specifies a viewing frustum into the world coordinate system.</span></span> <span data-ttu-id="ece83-121">Em geral, a taxa de proporção em **gluPerspective** deve corresponder à taxa de proporção do visor associado.</span><span class="sxs-lookup"><span data-stu-id="ece83-121">In general, the aspect ratio in **gluPerspective** should match the aspect ratio of the associated viewport.</span></span> <span data-ttu-id="ece83-122">Por exemplo, *Aspect* = 2,0 significa que o ângulo de exibição do visualizador é duas vezes mais largo em *x* , como em *y*.</span><span class="sxs-lookup"><span data-stu-id="ece83-122">For example, *aspect* = 2.0 means the viewer's angle of view is twice as wide in *x* as it is in *y*.</span></span> <span data-ttu-id="ece83-123">Se o visor for duas vezes maior que o comprimento, ele exibirá a imagem sem distorção.</span><span class="sxs-lookup"><span data-stu-id="ece83-123">If the viewport is twice as wide as it is tall, it displays the image without distortion.</span></span>

<span data-ttu-id="ece83-124">A matriz gerada por **gluPerspective** é multiplicada pela matriz atual, assim como se [**glMultMatrix**](glmultmatrix.md) fosse chamado com a matriz gerada.</span><span class="sxs-lookup"><span data-stu-id="ece83-124">The matrix generated by **gluPerspective** is multiplied by the current matrix, just as if [**glMultMatrix**](glmultmatrix.md) were called with the generated matrix.</span></span> <span data-ttu-id="ece83-125">Para carregar a matriz de perspectiva na pilha da matriz atual, preceda a chamada para **gluPerspective** com uma chamada para [**glLoadIdentity**](glloadidentity.md).</span><span class="sxs-lookup"><span data-stu-id="ece83-125">To load the perspective matrix onto the current matrix stack instead, precede the call to **gluPerspective** with a call to [**glLoadIdentity**](glloadidentity.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ece83-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ece83-126">Requirements</span></span>



| <span data-ttu-id="ece83-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ece83-127">Requirement</span></span> | <span data-ttu-id="ece83-128">Valor</span><span class="sxs-lookup"><span data-stu-id="ece83-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ece83-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ece83-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ece83-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ece83-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ece83-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ece83-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ece83-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ece83-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ece83-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ece83-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="ece83-134"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="ece83-134"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="ece83-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ece83-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="ece83-136"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ece83-136"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ece83-137">DLL</span><span class="sxs-lookup"><span data-stu-id="ece83-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ece83-138"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ece83-138"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ece83-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="ece83-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ece83-140">**glFrustum**</span><span class="sxs-lookup"><span data-stu-id="ece83-140">**glFrustum**</span></span>](glfrustum.md)
</dt> <dt>

[<span data-ttu-id="ece83-141">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="ece83-141">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="ece83-142">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="ece83-142">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="ece83-143">**gluOrtho2D**</span><span class="sxs-lookup"><span data-stu-id="ece83-143">**gluOrtho2D**</span></span>](gluortho2d.md)
</dt> </dl>

 

 





