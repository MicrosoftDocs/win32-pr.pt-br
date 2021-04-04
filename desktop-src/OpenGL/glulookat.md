---
title: função gluLookAt (Glu. h)
description: A função gluLookAt define uma transformação de exibição.
ms.assetid: 1fd87701-19c2-49b9-99ac-10e70aaedbfd
keywords:
- função gluLookAt OpenGL
topic_type:
- apiref
api_name:
- gluLookAt
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5866f3c06ef6969c95eeef4b23fff7a4e7852eb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824815"
---
# <a name="glulookat-function"></a><span data-ttu-id="3d054-104">função gluLookAt</span><span class="sxs-lookup"><span data-stu-id="3d054-104">gluLookAt function</span></span>

<span data-ttu-id="3d054-105">A função **gluLookAt** define uma transformação de exibição.</span><span class="sxs-lookup"><span data-stu-id="3d054-105">The **gluLookAt** function defines a viewing transformation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d054-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3d054-106">Syntax</span></span>


```C++
void WINAPI gluLookAt(
   GLdouble eyex,
   GLdouble eyey,
   GLdouble eyez,
   GLdouble centerx,
   GLdouble centery,
   GLdouble centerz,
   GLdouble upx,
   GLdouble upy,
   GLdouble upz
);
```



## <a name="parameters"></a><span data-ttu-id="3d054-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3d054-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d054-108">*eyex*</span><span class="sxs-lookup"><span data-stu-id="3d054-108">*eyex*</span></span> 
</dt> <dd>

<span data-ttu-id="3d054-109">A posição do ponto de olho.</span><span class="sxs-lookup"><span data-stu-id="3d054-109">The position of the eye point.</span></span>

</dd> <dt>

<span data-ttu-id="3d054-110">*eyey*</span><span class="sxs-lookup"><span data-stu-id="3d054-110">*eyey*</span></span> 
</dt> <dd>

<span data-ttu-id="3d054-111">A posição do ponto de olho.</span><span class="sxs-lookup"><span data-stu-id="3d054-111">The position of the eye point.</span></span>

</dd> <dt>

<span data-ttu-id="3d054-112">*eyez*</span><span class="sxs-lookup"><span data-stu-id="3d054-112">*eyez*</span></span> 
</dt> <dd>

<span data-ttu-id="3d054-113">A posição do ponto de olho.</span><span class="sxs-lookup"><span data-stu-id="3d054-113">The position of the eye point.</span></span>

</dd> <dt>

<span data-ttu-id="3d054-114">*CenterX*</span><span class="sxs-lookup"><span data-stu-id="3d054-114">*centerx*</span></span> 
</dt> <dd>

<span data-ttu-id="3d054-115">A posição do ponto de referência.</span><span class="sxs-lookup"><span data-stu-id="3d054-115">The position of the reference point.</span></span>

</dd> <dt>

<span data-ttu-id="3d054-116">*CenterY*</span><span class="sxs-lookup"><span data-stu-id="3d054-116">*centery*</span></span> 
</dt> <dd>

<span data-ttu-id="3d054-117">A posição do ponto de referência.</span><span class="sxs-lookup"><span data-stu-id="3d054-117">The position of the reference point.</span></span>

</dd> <dt>

<span data-ttu-id="3d054-118">*centerz*</span><span class="sxs-lookup"><span data-stu-id="3d054-118">*centerz*</span></span> 
</dt> <dd>

<span data-ttu-id="3d054-119">A posição do ponto de referência.</span><span class="sxs-lookup"><span data-stu-id="3d054-119">The position of the reference point.</span></span>

</dd> <dt>

<span data-ttu-id="3d054-120">*upx*</span><span class="sxs-lookup"><span data-stu-id="3d054-120">*upx*</span></span> 
</dt> <dd>

<span data-ttu-id="3d054-121">A direção do vetor para cima.</span><span class="sxs-lookup"><span data-stu-id="3d054-121">The direction of the up vector.</span></span>

</dd> <dt>

<span data-ttu-id="3d054-122">*upy*</span><span class="sxs-lookup"><span data-stu-id="3d054-122">*upy*</span></span> 
</dt> <dd>

<span data-ttu-id="3d054-123">A direção do vetor para cima.</span><span class="sxs-lookup"><span data-stu-id="3d054-123">The direction of the up vector.</span></span>

</dd> <dt>

<span data-ttu-id="3d054-124">*upz*</span><span class="sxs-lookup"><span data-stu-id="3d054-124">*upz*</span></span> 
</dt> <dd>

<span data-ttu-id="3d054-125">A direção do vetor para cima.</span><span class="sxs-lookup"><span data-stu-id="3d054-125">The direction of the up vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d054-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3d054-126">Return value</span></span>

<span data-ttu-id="3d054-127">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3d054-127">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d054-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="3d054-128">Remarks</span></span>

<span data-ttu-id="3d054-129">A função **gluLookAt** cria uma matriz de exibição derivada de um ponto de olho, um ponto de referência que indica o centro da cena e um vetor superior.</span><span class="sxs-lookup"><span data-stu-id="3d054-129">The **gluLookAt** function creates a viewing matrix derived from an eye point, a reference point indicating the center of the scene, and an up vector.</span></span> <span data-ttu-id="3d054-130">A matriz mapeia o ponto de referência para o eixo z negativo e o ponto de olho para a origem, de modo que, quando você usa uma matriz de projeção típica, o centro da cena é mapeado para o centro do visor.</span><span class="sxs-lookup"><span data-stu-id="3d054-130">The matrix maps the reference point to the negative z-axis and the eye point to the origin, so that when you use a typical projection matrix, the center of the scene maps to the center of the viewport.</span></span> <span data-ttu-id="3d054-131">Da mesma forma, a direção descrita pelo vetor de cima projetado no plano de exibição é mapeada para o eixo y positivo para que ele aponte para cima no visor.</span><span class="sxs-lookup"><span data-stu-id="3d054-131">Similarly, the direction described by the up vector projected onto the viewing plane is mapped to the positive y-axis so that it points upward in the viewport.</span></span> <span data-ttu-id="3d054-132">O vetor acima não deve ser paralelo à linha de visão do olho para o ponto de referência.</span><span class="sxs-lookup"><span data-stu-id="3d054-132">The up vector must not be parallel to the line of sight from the eye to the reference point.</span></span>

<span data-ttu-id="3d054-133">A matriz gerada por **gluLookAt** é multiplicada pela matriz atual.</span><span class="sxs-lookup"><span data-stu-id="3d054-133">The matrix generated by **gluLookAt** postmultiplies the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d054-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d054-134">Requirements</span></span>



| <span data-ttu-id="3d054-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d054-135">Requirement</span></span> | <span data-ttu-id="3d054-136">Valor</span><span class="sxs-lookup"><span data-stu-id="3d054-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3d054-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d054-137">Minimum supported client</span></span><br/> | <span data-ttu-id="3d054-138">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3d054-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="3d054-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d054-139">Minimum supported server</span></span><br/> | <span data-ttu-id="3d054-140">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3d054-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3d054-141">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3d054-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d054-142"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d054-142"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="3d054-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3d054-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="3d054-144"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d054-144"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3d054-145">DLL</span><span class="sxs-lookup"><span data-stu-id="3d054-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d054-146"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d054-146"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d054-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="3d054-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d054-148">**glFrustum**</span><span class="sxs-lookup"><span data-stu-id="3d054-148">**glFrustum**</span></span>](glfrustum.md)
</dt> <dt>

[<span data-ttu-id="3d054-149">**gluPerspective**</span><span class="sxs-lookup"><span data-stu-id="3d054-149">**gluPerspective**</span></span>](gluperspective.md)
</dt> </dl>

 

 





