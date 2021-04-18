---
title: função gluLoadSamplingMatrices (Glu. h)
description: A função gluLoadSamplingMatrices carrega as matrizes de amostragem de B-spline racional não uniforme (NURBS) e de remoção.
ms.assetid: 7fdbc4e2-a037-4f07-bb03-e51feea42775
keywords:
- função gluLoadSamplingMatrices OpenGL
topic_type:
- apiref
api_name:
- gluLoadSamplingMatrices
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 293b8bace0dff7d89bfcffa2af33738e0e59de7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105762929"
---
# <a name="gluloadsamplingmatrices-function"></a><span data-ttu-id="0685e-104">função gluLoadSamplingMatrices</span><span class="sxs-lookup"><span data-stu-id="0685e-104">gluLoadSamplingMatrices function</span></span>

<span data-ttu-id="0685e-105">A função **gluLoadSamplingMatrices** carrega as matrizes de amostragem de B-spline racional não uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)) e de remoção.</span><span class="sxs-lookup"><span data-stu-id="0685e-105">The **gluLoadSamplingMatrices** function loads Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) sampling and culling matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="0685e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0685e-106">Syntax</span></span>


```C++
void WINAPI gluLoadSamplingMatrices(
         GLUnurbs *nobj,
   const GLfloat  modelMatrix[16],
   const GLfloat  projMatrix[16],
   const GLint    viewport[4]
);
```



## <a name="parameters"></a><span data-ttu-id="0685e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0685e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0685e-108">*nobj*</span><span class="sxs-lookup"><span data-stu-id="0685e-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="0685e-109">O objeto NURBS (criado com [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="0685e-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="0685e-110">*modelMatrix*</span><span class="sxs-lookup"><span data-stu-id="0685e-110">*modelMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="0685e-111">Uma matriz modelview (como a partir de uma chamada [**glGetFloatv**](glgetfloatv.md) ).</span><span class="sxs-lookup"><span data-stu-id="0685e-111">A modelview matrix (as from a [**glGetFloatv**](glgetfloatv.md) call).</span></span>

</dd> <dt>

<span data-ttu-id="0685e-112">*projMatrix*</span><span class="sxs-lookup"><span data-stu-id="0685e-112">*projMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="0685e-113">Uma matriz de projeção (como a partir de uma chamada **glGetFloatv** ).</span><span class="sxs-lookup"><span data-stu-id="0685e-113">A projection matrix (as from a **glGetFloatv** call).</span></span>

</dd> <dt>

<span data-ttu-id="0685e-114">*visor*</span><span class="sxs-lookup"><span data-stu-id="0685e-114">*viewport*</span></span> 
</dt> <dd>

<span data-ttu-id="0685e-115">Um visor (como de uma chamada [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ).</span><span class="sxs-lookup"><span data-stu-id="0685e-115">A viewport (as from a [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) call).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0685e-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0685e-116">Return value</span></span>

<span data-ttu-id="0685e-117">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="0685e-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0685e-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="0685e-118">Remarks</span></span>

<span data-ttu-id="0685e-119">A função **gluLoadSamplingMatrices** usa *modelMatrix*, *projMatrix* e *viewport* para recalcular a amostragem e a remoção de matrizes armazenadas no *nobj*.</span><span class="sxs-lookup"><span data-stu-id="0685e-119">The **gluLoadSamplingMatrices** function uses *modelMatrix*, *projMatrix*, and *viewport* to recompute the sampling and culling matrices stored in *nobj*.</span></span> <span data-ttu-id="0685e-120">A matriz de amostragem determina quão fino uma curva NURBS ou uma superfície deve ser mosaico para satisfazer a tolerância de amostragem (conforme determinado pela \_ propriedade de tolerância de amostragem Glu \_ ).</span><span class="sxs-lookup"><span data-stu-id="0685e-120">The sampling matrix determines how finely a NURBS curve or surface must be tessellated to satisfy the sampling tolerance (as determined by the GLU\_SAMPLING\_TOLERANCE property).</span></span> <span data-ttu-id="0685e-121">A matriz de remoção é usada para decidir se uma curva ou uma superfície NURBS deve ser reutilizada antes da renderização (quando a propriedade de remoção de GLU \_ está ativada).</span><span class="sxs-lookup"><span data-stu-id="0685e-121">The culling matrix is used in deciding if a NURBS curve or surface should be culled before rendering (when the GLU\_CULLING property is turned on).</span></span>

<span data-ttu-id="0685e-122">A função **gluLoadSamplingMatrices** será necessária somente se a \_ propriedade da matriz de carga automática Glu \_ \_ estiver desativada (consulte [**gluNurbsProperty**](glunurbsproperty.md)).</span><span class="sxs-lookup"><span data-stu-id="0685e-122">The **gluLoadSamplingMatrices** function is necessary only if the GLU\_AUTO\_LOAD\_MATRIX property is turned off (see [**gluNurbsProperty**](glunurbsproperty.md)).</span></span> <span data-ttu-id="0685e-123">Embora possa ser conveniente deixar a \_ propriedade da matriz de carregamento automático do Glu \_ \_ ativada, isso exige uma viagem de ida e volta ao servidor OpenGL para obter os valores atuais da matriz modelview, da matriz de projeção e do visor.)</span><span class="sxs-lookup"><span data-stu-id="0685e-123">Although it can be convenient to leave the GLU\_AUTO\_LOAD\_MATRIX property turned on, doing so necessitates a round trip to the OpenGL server to get the current values of the modelview matrix, projection matrix, and viewport.)</span></span>

## <a name="requirements"></a><span data-ttu-id="0685e-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0685e-124">Requirements</span></span>



| <span data-ttu-id="0685e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0685e-125">Requirement</span></span> | <span data-ttu-id="0685e-126">Valor</span><span class="sxs-lookup"><span data-stu-id="0685e-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0685e-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0685e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0685e-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0685e-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="0685e-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0685e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0685e-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0685e-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0685e-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0685e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0685e-132"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="0685e-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="0685e-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0685e-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="0685e-134"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0685e-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="0685e-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0685e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0685e-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0685e-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0685e-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="0685e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0685e-138">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="0685e-138">**glGetFloatv**</span></span>](glgetfloatv.md)
</dt> <dt>

[<span data-ttu-id="0685e-139">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="0685e-139">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="0685e-140">**gluGetNurbsProperty**</span><span class="sxs-lookup"><span data-stu-id="0685e-140">**gluGetNurbsProperty**</span></span>](glugetnurbsproperty.md)
</dt> <dt>

[<span data-ttu-id="0685e-141">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="0685e-141">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> </dl>

 

 





