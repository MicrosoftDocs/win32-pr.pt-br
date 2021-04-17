---
title: função gluBeginTrim (Glu. h)
description: As funções gluBeginTrim e gluEndTrim delimitam uma definição de loop de corte de B-spline racional não uniforme (NURBS). | função gluBeginTrim (Glu. h)
ms.assetid: 636402d0-8f6d-4ad8-84c6-66364025d788
keywords:
- função gluBeginTrim OpenGL
topic_type:
- apiref
api_name:
- gluBeginTrim
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84cbe5c1cd0cc68ee892d42fc60db05b6ae2bea6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105762930"
---
# <a name="glubegintrim-function"></a><span data-ttu-id="22e2f-105">função gluBeginTrim</span><span class="sxs-lookup"><span data-stu-id="22e2f-105">gluBeginTrim function</span></span>

<span data-ttu-id="22e2f-106">As funções **gluBeginTrim** e [**gluEndTrim**](gluendtrim.md) delimitam uma definição de loop de corte de B-spline racional não uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="22e2f-106">The **gluBeginTrim** and [**gluEndTrim**](gluendtrim.md) functions delimit a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) trimming loop definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="22e2f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="22e2f-107">Syntax</span></span>


```C++
void WINAPI gluBeginTrim(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a><span data-ttu-id="22e2f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="22e2f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22e2f-109">*nobj*</span><span class="sxs-lookup"><span data-stu-id="22e2f-109">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="22e2f-110">O objeto NURBS (criado com [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="22e2f-110">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22e2f-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="22e2f-111">Return value</span></span>

<span data-ttu-id="22e2f-112">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="22e2f-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="22e2f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="22e2f-113">Remarks</span></span>

<span data-ttu-id="22e2f-114">Use **gluBeginTrim** para marcar o início de um loop de corte e **gluEndTrim** para marcar o final de um loop de corte.</span><span class="sxs-lookup"><span data-stu-id="22e2f-114">Use **gluBeginTrim** to mark the beginning of a trimming loop, and **gluEndTrim** to mark the end of a trimming loop.</span></span> <span data-ttu-id="22e2f-115">Um loop de corte é um conjunto de segmentos de curva orientados (formando uma curva fechada) que definem limites de uma superfície NURBS.</span><span class="sxs-lookup"><span data-stu-id="22e2f-115">A trimming loop is a set of oriented curve segments (forming a closed curve) that define boundaries of a NURBS surface.</span></span> <span data-ttu-id="22e2f-116">Você inclui esses loops de corte na definição de uma superfície NURBS, entre chamadas para [**gluBeginSurface**](glubeginsurface.md) e [**gluEndSurface**](gluendsurface.md).</span><span class="sxs-lookup"><span data-stu-id="22e2f-116">You include these trimming loops in the definition of a NURBS surface, between calls to [**gluBeginSurface**](glubeginsurface.md) and [**gluEndSurface**](gluendsurface.md).</span></span>

<span data-ttu-id="22e2f-117">A definição de uma superfície NURBS pode conter muitos loops de corte.</span><span class="sxs-lookup"><span data-stu-id="22e2f-117">The definition for a NURBS surface can contain many trimming loops.</span></span> <span data-ttu-id="22e2f-118">Por exemplo, se você escrever uma definição para uma superfície NURBS que se assemelha a um retângulo com uma perfuração perfurada, a definição conteria dois loops de corte.</span><span class="sxs-lookup"><span data-stu-id="22e2f-118">For example, if you write a definition for a NURBS surface that resembles a rectangle with a hole punched out, the definition would contain two trimming loops.</span></span> <span data-ttu-id="22e2f-119">Um loop definiria a borda externa do retângulo; o outro definiria o buraco perfurado.</span><span class="sxs-lookup"><span data-stu-id="22e2f-119">One loop would define the outer edge of the rectangle; the other would define the punched-out hole.</span></span> <span data-ttu-id="22e2f-120">As definições de cada um desses loops de corte seriam enmarcadas por um par **gluBeginTrim**  /  **gluEndTrim** .</span><span class="sxs-lookup"><span data-stu-id="22e2f-120">The definitions of each of these trimming loops would be bracketed by a **gluBeginTrim** / **gluEndTrim** pair.</span></span>

<span data-ttu-id="22e2f-121">A definição de um único loop de corte fechado pode consistir em vários segmentos de curva, cada um descrito como uma série de segmentos de linha que formam uma curva linear (consulte [**gluPwlCurve**](glupwlcurve.md)), como uma curva NURBS única (consulte [**gluNurbsCurve**](glunurbscurve.md)) ou como uma combinação de ambos em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="22e2f-121">The definition of a single closed trimming loop can consist of multiple curve segments, each described as a series of line segments that form a linear curve (see [**gluPwlCurve**](glupwlcurve.md)), as a single NURBS curve (see [**gluNurbsCurve**](glunurbscurve.md)), or as a combination of both in any order.</span></span> <span data-ttu-id="22e2f-122">As únicas chamadas de biblioteca que podem aparecer em uma definição de loop de corte (entre as chamadas para **gluBeginTrim** e **GluEndTrim**) são **gluPwlCurve** e **gluNurbsCurve**.</span><span class="sxs-lookup"><span data-stu-id="22e2f-122">The only library calls that can appear in a trimming-loop definition (between the calls to **gluBeginTrim** and **gluEndTrim**) are **gluPwlCurve** and **gluNurbsCurve**.</span></span>

<span data-ttu-id="22e2f-123">A área exibida da superfície NURBS é a região no domínio à esquerda da curva de corte conforme o parâmetro de curva aumenta.</span><span class="sxs-lookup"><span data-stu-id="22e2f-123">The displayed area of the NURBS surface is the region in the domain to the left of the trimming curve as the curve parameter increases.</span></span> <span data-ttu-id="22e2f-124">Assim, a região retida da superfície NURBS está dentro de um loop de corte no sentido anti-horário e fora de um loop de corte no sentido horário.</span><span class="sxs-lookup"><span data-stu-id="22e2f-124">Thus, the retained region of the NURBS surface is inside a counterclockwise trimming loop and outside a clockwise trimming loop.</span></span> <span data-ttu-id="22e2f-125">Para o retângulo mencionado anteriormente, o loop de corte para a borda externa do retângulo é executado no sentido anti-horário, enquanto o loop de corte para o buraco perfurado é executado no sentido horário.</span><span class="sxs-lookup"><span data-stu-id="22e2f-125">For the rectangle mentioned earlier, the trimming loop for the outer edge of the rectangle runs counterclockwise, while the trimming loop for the punched-out hole runs clockwise.</span></span>

<span data-ttu-id="22e2f-126">Se você usar mais de uma curva para definir um único loop de corte, os segmentos de curva deverão formar um loop fechado (ou seja, o ponto de extremidade de cada curva deverá ser o início da próxima curva e o ponto de extremidade da curva final deverá ser o início da primeira curva).</span><span class="sxs-lookup"><span data-stu-id="22e2f-126">If you use more than one curve to define a single trimming loop, the curve segments must form a closed loop (that is, the endpoint of each curve must be the starting point of the next curve, and the endpoint of the final curve must be the starting point of the first curve).</span></span> <span data-ttu-id="22e2f-127">Se os pontos de extremidade da curva estiverem suficientemente próximos juntos, mas não forem exatamente coincidentes, eles serão forçados a coincidir.</span><span class="sxs-lookup"><span data-stu-id="22e2f-127">If the endpoints of the curve are sufficiently close together but not exactly coincident, they will be forced to match.</span></span> <span data-ttu-id="22e2f-128">Se os pontos de extremidade não estiverem suficientemente fechados, ocorrerá um erro (consulte [*gluNurbsCallback*](glunurbs.md)).</span><span class="sxs-lookup"><span data-stu-id="22e2f-128">If the endpoints are not sufficiently close, an error results (see [*gluNurbsCallback*](glunurbs.md)).</span></span>

<span data-ttu-id="22e2f-129">Se uma definição de loop de corte contiver várias curvas, a direção das curvas deverá ser consistente (ou seja, o interior deve estar à esquerda de todas as curvas).</span><span class="sxs-lookup"><span data-stu-id="22e2f-129">If a trimming-loop definition contains multiple curves, the direction of the curves must be consistent (that is, the inside must be to the left of all of the curves).</span></span> <span data-ttu-id="22e2f-130">Você pode usar loops de corte aninhados, desde que as orientações de curva sejam alternadas corretamente.</span><span class="sxs-lookup"><span data-stu-id="22e2f-130">You can use nested trimming loops as long as the curve orientations alternate correctly.</span></span> <span data-ttu-id="22e2f-131">As curvas de corte não podem ser interseccionadas automaticamente nem se interseccionam uma com a outra (ou um resultado de erro).</span><span class="sxs-lookup"><span data-stu-id="22e2f-131">Trimming curves cannot be self-intersecting, nor can they intersect one another (or an error results).</span></span>

<span data-ttu-id="22e2f-132">Se nenhuma informação de corte for fornecida para uma superfície NURBS, toda a superfície será desenhada.</span><span class="sxs-lookup"><span data-stu-id="22e2f-132">If no trimming information is given for a NURBS surface, the entire surface is drawn.</span></span>

## <a name="examples"></a><span data-ttu-id="22e2f-133">Exemplos</span><span class="sxs-lookup"><span data-stu-id="22e2f-133">Examples</span></span>

<span data-ttu-id="22e2f-134">Este fragmento de código define um loop de corte que consiste em uma curva linear piecewise e duas curvas NURBS:</span><span class="sxs-lookup"><span data-stu-id="22e2f-134">This code fragment defines a trimming loop that consists of one piecewise linear curve and two NURBS curves:</span></span>

``` syntax
gluBeginTrim(nobj); 
    gluPwlCurve(. . ., GLU_MAP1_TRIM_2); 
    gluNurbsCurve(. . ., GLU_MAP1_TRIM_2); 
    gluNurbsCurve(. . ., GLU_MAP1_TRIM_3);  
gluEndTrim(nobj);
```

## <a name="requirements"></a><span data-ttu-id="22e2f-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22e2f-135">Requirements</span></span>



| <span data-ttu-id="22e2f-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="22e2f-136">Requirement</span></span> | <span data-ttu-id="22e2f-137">Valor</span><span class="sxs-lookup"><span data-stu-id="22e2f-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="22e2f-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22e2f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="22e2f-139">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="22e2f-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="22e2f-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22e2f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="22e2f-141">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="22e2f-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="22e2f-142">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="22e2f-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="22e2f-143"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="22e2f-143"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="22e2f-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="22e2f-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="22e2f-145"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22e2f-145"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="22e2f-146">DLL</span><span class="sxs-lookup"><span data-stu-id="22e2f-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22e2f-147"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22e2f-147"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22e2f-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="22e2f-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22e2f-149">**gluBeginSurface**</span><span class="sxs-lookup"><span data-stu-id="22e2f-149">**gluBeginSurface**</span></span>](glubeginsurface.md)
</dt> <dt>

[<span data-ttu-id="22e2f-150">**gluEndSurface**</span><span class="sxs-lookup"><span data-stu-id="22e2f-150">**gluEndSurface**</span></span>](gluendsurface.md)
</dt> <dt>

[<span data-ttu-id="22e2f-151">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="22e2f-151">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="22e2f-152">*gluNurbsCallback*</span><span class="sxs-lookup"><span data-stu-id="22e2f-152">*gluNurbsCallback*</span></span>](glunurbs.md)
</dt> <dt>

[<span data-ttu-id="22e2f-153">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="22e2f-153">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> <dt>

[<span data-ttu-id="22e2f-154">**gluPwlCurve**</span><span class="sxs-lookup"><span data-stu-id="22e2f-154">**gluPwlCurve**</span></span>](glupwlcurve.md)
</dt> </dl>

 

 





