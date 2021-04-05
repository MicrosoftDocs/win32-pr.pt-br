---
title: função gluGetNurbsProperty (Glu. h)
description: A função gluGetNurbsProperty Obtém uma propriedade B-spline racional não uniforme (NURBS).
ms.assetid: 7dbc75a0-d04e-4794-b3dd-a602addf9dfa
keywords:
- função gluGetNurbsProperty OpenGL
topic_type:
- apiref
api_name:
- gluGetNurbsProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 583da688e3495ebc2eb9d6f71972658c6426469c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085436"
---
# <a name="glugetnurbsproperty-function"></a><span data-ttu-id="40602-104">função gluGetNurbsProperty</span><span class="sxs-lookup"><span data-stu-id="40602-104">gluGetNurbsProperty function</span></span>

<span data-ttu-id="40602-105">A função **gluGetNurbsProperty** Obtém uma propriedade B-spline racional não uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="40602-105">The **gluGetNurbsProperty** function gets a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="40602-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="40602-106">Syntax</span></span>


```C++
void WINAPI gluGetNurbsProperty(
   GLUnurbs *nobj,
   GLenum   property,
   GLfloat  *value
);
```



## <a name="parameters"></a><span data-ttu-id="40602-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="40602-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40602-108">*nobj*</span><span class="sxs-lookup"><span data-stu-id="40602-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="40602-109">O objeto NURBS (criado com [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="40602-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="40602-110">*property*</span><span class="sxs-lookup"><span data-stu-id="40602-110">*property*</span></span> 
</dt> <dd>

<span data-ttu-id="40602-111">A propriedade cujo valor deve ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="40602-111">The property whose value is to be retrieved.</span></span> <span data-ttu-id="40602-112">Os seguintes valores são válidos: tolerância de amostragem de GLU \_ \_ , \_ modo de exibição Glu \_ , glu \_ de remoção, matriz de \_ carga automática Glu \_ \_ , \_ tolerância paramétrica Glu \_ , \_ \_ método de amostragem glu, \_ etapa Glu U \_ e \_ etapa Glu V \_ .</span><span class="sxs-lookup"><span data-stu-id="40602-112">The following values are valid: GLU\_SAMPLING\_TOLERANCE, GLU\_DISPLAY\_MODE, GLU\_CULLING, GLU\_AUTO\_LOAD\_MATRIX, GLU\_PARAMETRIC\_TOLERANCE, GLU\_SAMPLING\_METHOD, GLU\_U\_STEP, and GLU\_V\_STEP.</span></span>

</dd> <dt>

<span data-ttu-id="40602-113">*value*</span><span class="sxs-lookup"><span data-stu-id="40602-113">*value*</span></span> 
</dt> <dd>

<span data-ttu-id="40602-114">Um ponteiro para o local no qual o valor da propriedade nomeada é gravado.</span><span class="sxs-lookup"><span data-stu-id="40602-114">A pointer to the location into which the value of the named property is written.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40602-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="40602-115">Return value</span></span>

<span data-ttu-id="40602-116">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="40602-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="40602-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="40602-117">Remarks</span></span>

<span data-ttu-id="40602-118">Use **gluGetNurbsProperty** para recuperar as propriedades armazenadas em um objeto NURBS.</span><span class="sxs-lookup"><span data-stu-id="40602-118">Use **gluGetNurbsProperty** to retrieve properties stored in a NURBS object.</span></span> <span data-ttu-id="40602-119">Essas propriedades afetam a maneira como as curvas NURBS e as superfícies são renderizadas.</span><span class="sxs-lookup"><span data-stu-id="40602-119">These properties affect the way NURBS curves and surfaces are rendered.</span></span> <span data-ttu-id="40602-120">Para obter informações sobre as propriedades NURBS, consulte [**gluNurbsProperty**](glunurbsproperty.md).</span><span class="sxs-lookup"><span data-stu-id="40602-120">For information about NURBS properties, see [**gluNurbsProperty**](glunurbsproperty.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="40602-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40602-121">Requirements</span></span>



| <span data-ttu-id="40602-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="40602-122">Requirement</span></span> | <span data-ttu-id="40602-123">Valor</span><span class="sxs-lookup"><span data-stu-id="40602-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="40602-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40602-124">Minimum supported client</span></span><br/> | <span data-ttu-id="40602-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="40602-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="40602-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40602-126">Minimum supported server</span></span><br/> | <span data-ttu-id="40602-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="40602-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="40602-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="40602-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="40602-129"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="40602-129"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="40602-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="40602-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="40602-131"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="40602-131"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="40602-132">DLL</span><span class="sxs-lookup"><span data-stu-id="40602-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40602-133"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40602-133"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40602-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="40602-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40602-135">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="40602-135">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="40602-136">**gluNurbsProperty**</span><span class="sxs-lookup"><span data-stu-id="40602-136">**gluNurbsProperty**</span></span>](glunurbsproperty.md)
</dt> </dl>

 

 





