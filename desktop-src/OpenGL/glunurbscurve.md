---
title: função gluNurbsCurve (Glu. h)
description: A função gluNurbsCurve define a forma de uma curva de B-spline racional não uniforme (NURBS).
ms.assetid: d03064a5-26f5-487f-877f-3748646bcb2f
keywords:
- função gluNurbsCurve OpenGL
topic_type:
- apiref
api_name:
- gluNurbsCurve
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c38e3d5fe35e994afa4b5d8b91c4244573132c5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758580"
---
# <a name="glunurbscurve-function"></a><span data-ttu-id="8256a-104">função gluNurbsCurve</span><span class="sxs-lookup"><span data-stu-id="8256a-104">gluNurbsCurve function</span></span>

<span data-ttu-id="8256a-105">A função **gluNurbsCurve** define a forma de uma curva de B-spline racional não uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="8256a-105">The **gluNurbsCurve** function defines the shape of a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) curve.</span></span>

## <a name="syntax"></a><span data-ttu-id="8256a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8256a-106">Syntax</span></span>


```C++
void WINAPI gluNurbsCurve(
   GLUnurbs *nobj,
   GLint    nknots,
   GLfloat  *knot,
   GLint    stride,
   GLfloat  *ctlarray,
   GLint    order,
   GLenum   type
);
```



## <a name="parameters"></a><span data-ttu-id="8256a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8256a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8256a-108">*nobj*</span><span class="sxs-lookup"><span data-stu-id="8256a-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="8256a-109">O objeto NURBS (criado com [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="8256a-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="8256a-110">*nknots*</span><span class="sxs-lookup"><span data-stu-id="8256a-110">*nknots*</span></span> 
</dt> <dd>

<span data-ttu-id="8256a-111">O número de nós no *nó*.</span><span class="sxs-lookup"><span data-stu-id="8256a-111">The number of knots in *knot*.</span></span> <span data-ttu-id="8256a-112">O parâmetro *nknots* é igual ao número de pontos de controle mais o pedido.</span><span class="sxs-lookup"><span data-stu-id="8256a-112">The *nknots* parameter equals the number of control points plus the order.</span></span>

</dd> <dt>

<span data-ttu-id="8256a-113">*crescente*</span><span class="sxs-lookup"><span data-stu-id="8256a-113">*knot*</span></span> 
</dt> <dd>

<span data-ttu-id="8256a-114">Uma matriz de valores de nó *nknots* nondecreasing.</span><span class="sxs-lookup"><span data-stu-id="8256a-114">An array of *nknots* nondecreasing knot values.</span></span>

</dd> <dt>

<span data-ttu-id="8256a-115">*Stride*</span><span class="sxs-lookup"><span data-stu-id="8256a-115">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="8256a-116">O deslocamento (como um número de valores de ponto flutuante de precisão simples) entre pontos de controle de curva sucessivos.</span><span class="sxs-lookup"><span data-stu-id="8256a-116">The offset (as a number of single-precision floating-point values) between successive curve control points.</span></span>

</dd> <dt>

<span data-ttu-id="8256a-117">*ctlarray*</span><span class="sxs-lookup"><span data-stu-id="8256a-117">*ctlarray*</span></span> 
</dt> <dd>

<span data-ttu-id="8256a-118">Um ponteiro para uma matriz de pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="8256a-118">A pointer to an array of control points.</span></span> <span data-ttu-id="8256a-119">As coordenadas devem concordar com o *tipo*.</span><span class="sxs-lookup"><span data-stu-id="8256a-119">The coordinates must agree with *type*.</span></span>

</dd> <dt>

<span data-ttu-id="8256a-120">*order*</span><span class="sxs-lookup"><span data-stu-id="8256a-120">*order*</span></span> 
</dt> <dd>

<span data-ttu-id="8256a-121">A ordem da curva NURBS.</span><span class="sxs-lookup"><span data-stu-id="8256a-121">The order of the NURBS curve.</span></span> <span data-ttu-id="8256a-122">O parâmetro *Order* é igual a grau + 1; Portanto, uma curva cúbica tem uma ordem de 4.</span><span class="sxs-lookup"><span data-stu-id="8256a-122">The *order* parameter equals degree + 1; hence a cubic curve has an order of 4.</span></span>

</dd> <dt>

<span data-ttu-id="8256a-123">*tipo*</span><span class="sxs-lookup"><span data-stu-id="8256a-123">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="8256a-124">O tipo da curva.</span><span class="sxs-lookup"><span data-stu-id="8256a-124">The type of the curve.</span></span> <span data-ttu-id="8256a-125">Se essa curva for definida em um par [**gluBeginCurve**](glubegincurve.md) / [**gluEndCurve**](gluendcurve.md) , o tipo poderá ser qualquer um dos tipos de avaliadores unidimensionais válidos (como GL \_ MAP1 \_ Vertex \_ 3 ou GL \_ MAP1 \_ Color \_ 4).</span><span class="sxs-lookup"><span data-stu-id="8256a-125">If this curve is defined within a [**gluBeginCurve**](glubegincurve.md)/[**gluEndCurve**](gluendcurve.md) pair, then the type can be any of the valid one-dimensional evaluator types (such as GL\_MAP1\_VERTEX\_3 or GL\_MAP1\_COLOR\_4).</span></span> <span data-ttu-id="8256a-126">Entre um par [**gluBeginTrim**](glubegintrim.md) / [**gluEndTrim**](gluendtrim.md) , os únicos tipos válidos são Glu \_ MAP1 \_ Trim \_ 2 e Glu \_ MAP1 \_ Trim \_ 3.</span><span class="sxs-lookup"><span data-stu-id="8256a-126">Between a [**gluBeginTrim**](glubegintrim.md)/[**gluEndTrim**](gluendtrim.md) pair, the only valid types are GLU\_MAP1\_TRIM\_2 and GLU\_MAP1\_TRIM\_3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8256a-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8256a-127">Return value</span></span>

<span data-ttu-id="8256a-128">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8256a-128">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8256a-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="8256a-129">Remarks</span></span>

<span data-ttu-id="8256a-130">Quando **gluNurbsCurve** aparece entre um  / par de **gluEndCurve** gluBeginCurve, ele descreve uma curva a ser renderizada.</span><span class="sxs-lookup"><span data-stu-id="8256a-130">When **gluNurbsCurve** appears between a **gluBeginCurve**/**gluEndCurve** pair, it describes a curve to be rendered.</span></span> <span data-ttu-id="8256a-131">Você associa as coordenadas posicionais, de textura e de cores, apresentando cada uma delas como um **gluNurbsCurve** separado entre um par **gluBeginCurve** / **gluEndCurve** .</span><span class="sxs-lookup"><span data-stu-id="8256a-131">You associate positional, texture, and color coordinates by presenting each as a separate **gluNurbsCurve** between a **gluBeginCurve**/**gluEndCurve** pair.</span></span> <span data-ttu-id="8256a-132">Não faça mais de uma chamada para **gluNurbsCurve** para cor, posição e dados de textura em um único par **gluBeginCurve** / **gluEndCurve** .</span><span class="sxs-lookup"><span data-stu-id="8256a-132">Do not make more than one call to **gluNurbsCurve** for color, position, and texture data within a single **gluBeginCurve**/**gluEndCurve** pair.</span></span> <span data-ttu-id="8256a-133">Faça exatamente uma chamada para descrever a posição da curva (um *tipo* de GL \_ MAP1 \_ Vertex \_ 3 ou GL \_ MAP1 \_ Vertex \_ 4).</span><span class="sxs-lookup"><span data-stu-id="8256a-133">Make exactly one call to describe the position of the curve (a *type* of GL\_MAP1\_VERTEX\_3 or GL\_MAP1\_VERTEX\_4).</span></span>

<span data-ttu-id="8256a-134">Quando **gluNurbsCurve** aparece entre um [](glubegintrim.md) / par de [**gluEndTrim**](gluendtrim.md) gluBeginTrim, ele descreve uma curva de corte em uma superfície NURBS.</span><span class="sxs-lookup"><span data-stu-id="8256a-134">When **gluNurbsCurve** appears between a [**gluBeginTrim**](glubegintrim.md)/[**gluEndTrim**](gluendtrim.md) pair, it describes a trimming curve on a NURBS surface.</span></span> <span data-ttu-id="8256a-135">Se *Type* for Glu \_ MAP1 \_ Trim \_ 2, ele descreve uma curva no espaço de parâmetro bidimensional (*u* e *v*).</span><span class="sxs-lookup"><span data-stu-id="8256a-135">If *type* is GLU\_MAP1\_TRIM\_2, it describes a curve in two-dimensional (*u* and *v*) parameter space.</span></span> <span data-ttu-id="8256a-136">Se for GLU \_ MAP1 \_ Trim \_ 3, ele descreve uma curva no espaço de parâmetro bidimensional homogêneo (*u*, *v* e *w*).</span><span class="sxs-lookup"><span data-stu-id="8256a-136">If it is GLU\_MAP1\_TRIM\_3, it describes a curve in two-dimensional homogeneous (*u*, *v*, and *w*) parameter space.</span></span> <span data-ttu-id="8256a-137">Para obter mais discussões sobre corte de curvas, consulte **gluBeginTrim**.</span><span class="sxs-lookup"><span data-stu-id="8256a-137">For more discussion about trimming curves, see **gluBeginTrim**.</span></span>

## <a name="examples"></a><span data-ttu-id="8256a-138">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8256a-138">Examples</span></span>

<span data-ttu-id="8256a-139">As funções a seguir renderizam uma curva NURBS texturizada com Normals:</span><span class="sxs-lookup"><span data-stu-id="8256a-139">The following functions render a textured NURBS curve with normals:</span></span>

``` syntax
gluBeginCurve(nobj); 
    gluNurbsCurve(nobj, ..., GL_MAP1_TEXTURE_COORD_2); 
    gluNurbsCurve(nobj, ..., GL_MAP1_NORMAL); 
    gluNurbsCurve(nobj, ..., GL_MAP1_VERTEX_4);  
gluEndCurve(nobj); 
```

## <a name="requirements"></a><span data-ttu-id="8256a-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8256a-140">Requirements</span></span>



| <span data-ttu-id="8256a-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="8256a-141">Requirement</span></span> | <span data-ttu-id="8256a-142">Valor</span><span class="sxs-lookup"><span data-stu-id="8256a-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8256a-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8256a-143">Minimum supported client</span></span><br/> | <span data-ttu-id="8256a-144">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8256a-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8256a-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8256a-145">Minimum supported server</span></span><br/> | <span data-ttu-id="8256a-146">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8256a-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8256a-147">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8256a-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="8256a-148"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="8256a-148"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="8256a-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8256a-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="8256a-150"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8256a-150"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8256a-151">DLL</span><span class="sxs-lookup"><span data-stu-id="8256a-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8256a-152"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8256a-152"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8256a-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="8256a-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8256a-154">**gluBeginCurve**</span><span class="sxs-lookup"><span data-stu-id="8256a-154">**gluBeginCurve**</span></span>](glubegincurve.md)
</dt> <dt>

[<span data-ttu-id="8256a-155">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="8256a-155">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="8256a-156">**gluEndCurve**</span><span class="sxs-lookup"><span data-stu-id="8256a-156">**gluEndCurve**</span></span>](gluendcurve.md)
</dt> <dt>

[<span data-ttu-id="8256a-157">**gluEndTrim**</span><span class="sxs-lookup"><span data-stu-id="8256a-157">**gluEndTrim**</span></span>](gluendtrim.md)
</dt> <dt>

[<span data-ttu-id="8256a-158">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="8256a-158">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="8256a-159">**gluPwlCurve**</span><span class="sxs-lookup"><span data-stu-id="8256a-159">**gluPwlCurve**</span></span>](glupwlcurve.md)
</dt> </dl>

 

 





