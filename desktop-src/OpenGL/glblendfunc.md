---
title: função glBlendFunc (GL. h)
description: A função glBlendFunc especifica a aritmética de pixel.
ms.assetid: 6756774b-5eef-419a-a653-0b251aed65a0
keywords:
- função glBlendFunc OpenGL
topic_type:
- apiref
api_name:
- glBlendFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6300543bbf589c704da6d941bd743f693e0ed5fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105800102"
---
# <a name="glblendfunc-function"></a><span data-ttu-id="b029d-104">função glBlendFunc</span><span class="sxs-lookup"><span data-stu-id="b029d-104">glBlendFunc function</span></span>

<span data-ttu-id="b029d-105">A função **glBlendFunc** especifica a aritmética de pixel.</span><span class="sxs-lookup"><span data-stu-id="b029d-105">The **glBlendFunc** function specifies pixel arithmetic.</span></span>

## <a name="syntax"></a><span data-ttu-id="b029d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b029d-106">Syntax</span></span>


```C++
void WINAPI glBlendFunc(
   GLenum sfactor,
   GLenum dfactor
);
```



## <a name="parameters"></a><span data-ttu-id="b029d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b029d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b029d-108">*sfactor*</span><span class="sxs-lookup"><span data-stu-id="b029d-108">*sfactor*</span></span> 
</dt> <dd>

<span data-ttu-id="b029d-109">Especifica como os fatores de mistura de origem em vermelho, verde, azul e alfa são computados.</span><span class="sxs-lookup"><span data-stu-id="b029d-109">Specifies how the red, green, blue, and alpha source-blending factors are computed.</span></span> <span data-ttu-id="b029d-110">Nove constantes simbólicas são aceitas: GL \_ zero, GL \_ One, GL \_ DST \_ Color, GL \_ um \_ menos a \_ \_ cor de DST, GL \_ src \_ alfa, GL \_ um \_ menos \_ src \_ Alpha, GL \_ DST \_ Alpha, GL \_ um \_ menos \_ DST \_ alfa e GL \_ src \_ Alpha \_ saturação.</span><span class="sxs-lookup"><span data-stu-id="b029d-110">Nine symbolic constants are accepted: GL\_ZERO, GL\_ONE, GL\_DST\_COLOR, GL\_ONE\_MINUS\_DST\_COLOR, GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA, GL\_DST\_ALPHA, GL\_ONE\_MINUS\_DST\_ALPHA, and GL\_SRC\_ALPHA\_SATURATE.</span></span>

</dd> <dt>

<span data-ttu-id="b029d-111">*dfactor*</span><span class="sxs-lookup"><span data-stu-id="b029d-111">*dfactor*</span></span> 
</dt> <dd>

<span data-ttu-id="b029d-112">Especifica como os fatores de mesclagem de destino vermelho, verde, azul e alfa são computados.</span><span class="sxs-lookup"><span data-stu-id="b029d-112">Specifies how the red, green, blue, and alpha destination-blending factors are computed.</span></span> <span data-ttu-id="b029d-113">Oito constantes simbólicas são aceitas: GL \_ zero, GL \_ One, GL \_ src \_ Color, GL \_ um \_ menos a \_ \_ cor src, GL \_ src \_ alfa, GL \_ um \_ menos \_ src \_ Alpha, GL \_ DST \_ Alpha e GL \_ um \_ menos \_ DST \_ Alpha.</span><span class="sxs-lookup"><span data-stu-id="b029d-113">Eight symbolic constants are accepted: GL\_ZERO, GL\_ONE, GL\_SRC\_COLOR, GL\_ONE\_MINUS\_SRC\_COLOR, GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA, GL\_DST\_ALPHA, and GL\_ONE\_MINUS\_DST\_ALPHA.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b029d-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b029d-114">Return value</span></span>

<span data-ttu-id="b029d-115">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b029d-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b029d-116">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="b029d-116">Error codes</span></span>

<span data-ttu-id="b029d-117">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="b029d-117">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b029d-118">Nome</span><span class="sxs-lookup"><span data-stu-id="b029d-118">Name</span></span>                                                                                                  | <span data-ttu-id="b029d-119">Significado</span><span class="sxs-lookup"><span data-stu-id="b029d-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b029d-120"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="b029d-120"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="b029d-121">*Sfactor* ou *dfactor* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="b029d-121">Either *sfactor* or *dfactor* was not an accepted value.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="b029d-122"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b029d-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b029d-123">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="b029d-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b029d-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="b029d-124">Remarks</span></span>

<span data-ttu-id="b029d-125">No modo RGB, os pixels podem ser desenhados usando uma função que combina os valores de RGBA de entrada (origem) com os valores RGBA que já estão no framebuffer (os valores de destino).</span><span class="sxs-lookup"><span data-stu-id="b029d-125">In RGB mode, pixels can be drawn using a function that blends the incoming (source) RGBA values with the RGBA values that are already in the framebuffer (the destination values).</span></span> <span data-ttu-id="b029d-126">Por padrão, a mesclagem está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="b029d-126">By default, blending is disabled.</span></span> <span data-ttu-id="b029d-127">Use [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) com o \_ argumento GL Blend para habilitar e desabilitar a mesclagem.</span><span class="sxs-lookup"><span data-stu-id="b029d-127">Use [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the GL\_BLEND argument to enable and disable blending.</span></span>

<span data-ttu-id="b029d-128">Quando habilitado, **glBlendFunc** define a operação de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="b029d-128">When enabled, **glBlendFunc** defines the operation of blending.</span></span> <span data-ttu-id="b029d-129">O parâmetro *sfactor* especifica qual dos nove métodos é usado para dimensionar os componentes de cor de origem.</span><span class="sxs-lookup"><span data-stu-id="b029d-129">The *sfactor* parameter specifies which of nine methods is used to scale the source color components.</span></span> <span data-ttu-id="b029d-130">O parâmetro *dfactor* especifica qual dos oito métodos é usado para dimensionar os componentes de cor de destino.</span><span class="sxs-lookup"><span data-stu-id="b029d-130">The *dfactor* parameter specifies which of eight methods is used to scale the destination color components.</span></span> <span data-ttu-id="b029d-131">Os onze métodos possíveis são descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b029d-131">The eleven possible methods are described in the following table.</span></span> <span data-ttu-id="b029d-132">Cada método define quatro fatores de escala, um para vermelho, verde, azul e alfa.</span><span class="sxs-lookup"><span data-stu-id="b029d-132">Each method defines four scale factors one each for red, green, blue, and alpha.</span></span>

<span data-ttu-id="b029d-133">Na tabela e nas equações subsequentes, os componentes de cor de origem e de destino são chamados de (*R*?</span><span class="sxs-lookup"><span data-stu-id="b029d-133">In the table and in subsequent equations, source and destination color components are referred to as (*R*?</span></span> <span data-ttu-id="b029d-134">, *G*?</span><span class="sxs-lookup"><span data-stu-id="b029d-134">, *G*?</span></span> <span data-ttu-id="b029d-135">, *B*?</span><span class="sxs-lookup"><span data-stu-id="b029d-135">, *B*?</span></span> <span data-ttu-id="b029d-136">, *Um*?</span><span class="sxs-lookup"><span data-stu-id="b029d-136">, *A*?</span></span> <span data-ttu-id="b029d-137">) e (*R*<sub>d</sub> , *G*<sub>d</sub> , *B*<sub>d</sub> , *A*<sub>d</sub> ).</span><span class="sxs-lookup"><span data-stu-id="b029d-137">) and (*R*<sub>d</sub> , *G*<sub>d</sub> , *B*<sub>d</sub> , *A*<sub>d</sub> ).</span></span> <span data-ttu-id="b029d-138">Eles são compreendidos para ter valores inteiros entre zero e (*k*<sub>r</sub> , *k*<sub>G</sub> , *k*<sub>r</sub> , *k*<sub>A</sub> ), em que</span><span class="sxs-lookup"><span data-stu-id="b029d-138">They are understood to have integer values between zero and (*k*<sub>R</sub> , *k*<sub>G</sub> , *k*<sub>R</sub> , *k*<sub>A</sub> ), where</span></span>

<span data-ttu-id="b029d-139">*k*<sub>r</sub> = 2 <sup>m</sup>*r* -1</span><span class="sxs-lookup"><span data-stu-id="b029d-139">*k*<sub>R</sub> = 2 <sup>m</sup>*R* - 1</span></span>

<span data-ttu-id="b029d-140">*k*<sub>g</sub> = 2 <sup>m</sup>*G* -1</span><span class="sxs-lookup"><span data-stu-id="b029d-140">*k*<sub>G</sub> = 2 <sup>m</sup>*G* - 1</span></span>

<span data-ttu-id="b029d-141">*k*<sub>b</sub> = 2 <sup>m</sup>*B* -1</span><span class="sxs-lookup"><span data-stu-id="b029d-141">*k*<sub>B</sub> = 2 <sup>m</sup>*B* - 1</span></span>

<span data-ttu-id="b029d-142">*k*<sub>a</sub> = 2 <sup>m</sup>*a* -1</span><span class="sxs-lookup"><span data-stu-id="b029d-142">*k*<sub>A</sub> = 2 <sup>m</sup>*A* - 1</span></span>

<span data-ttu-id="b029d-143">e (*m*<sub>R</sub> , *m*<sub>G</sub> , *m*<sub>B</sub> , *m*<sub>a</sub> ) é o número de bitplanes vermelho, verde, azul e alfa.</span><span class="sxs-lookup"><span data-stu-id="b029d-143">and (*m*<sub>R</sub> , *m*<sub>G</sub> , *m*<sub>B</sub> , *m*<sub>A</sub> ) is the number of red, green, blue, and alpha bitplanes.</span></span>

<span data-ttu-id="b029d-144">Os fatores de escala de origem e destino são referidos como (*s*<sub>r</sub> , *s*<sub>G</sub> , *s*<sub>B</sub> , *s*<sub>a</sub> ) e (*d*<sub>R</sub> , *d*<sub>G</sub> , *d*<sub>B</sub> , *d*<sub>a</sub> ).</span><span class="sxs-lookup"><span data-stu-id="b029d-144">Source and destination scale factors are referred to as (*s*<sub>R</sub> , *s*<sub>G</sub> , *s*<sub>B</sub> , *s*<sub>A</sub> ) and (*d*<sub>R</sub> , *d*<sub>G</sub> , *d*<sub>B</sub> , *d*<sub>A</sub> ).</span></span> <span data-ttu-id="b029d-145">Os fatores de escala descritos na tabela, denotados (*f*<sub>R</sub> , *f*<sub>G</sub> , *f*<sub>B</sub> , *f*<sub>A</sub> ), representam fatores de origem ou de destino.</span><span class="sxs-lookup"><span data-stu-id="b029d-145">The scale factors described in the table, denoted (*f*<sub>R</sub> , *f*<sub>G</sub> , *f*<sub>B</sub> , *f*<sub>A</sub> ), represent either source or destination factors.</span></span> <span data-ttu-id="b029d-146">Todos os fatores de escala têm o intervalo \[ de 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="b029d-146">All scale factors have range \[0,1\].</span></span>



| <span data-ttu-id="b029d-147">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="b029d-147">Parameter</span></span>                  | <span data-ttu-id="b029d-148">(*f*<sub>R</sub>  , *f*<sub>G</sub>  , *f*<sub>B</sub>  , *f*<sub>A</sub>  )</span><span class="sxs-lookup"><span data-stu-id="b029d-148">(*f*<sub>R</sub>  , *f*<sub>G</sub>  , *f*<sub>B</sub>  , *f*<sub>A</sub>  )</span></span>                                                                                 |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b029d-149">GL \_ zero</span><span class="sxs-lookup"><span data-stu-id="b029d-149">GL\_ZERO</span></span>                   | <span data-ttu-id="b029d-150">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="b029d-150">(0,0,0,0)</span></span>                                                                                                                                                    |
| <span data-ttu-id="b029d-151">GL \_ um</span><span class="sxs-lookup"><span data-stu-id="b029d-151">GL\_ONE</span></span>                    | <span data-ttu-id="b029d-152">(1, 1, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="b029d-152">(1,1,1,1)</span></span>                                                                                                                                                    |
| <span data-ttu-id="b029d-153">\_cor de src GL \_</span><span class="sxs-lookup"><span data-stu-id="b029d-153">GL\_SRC\_COLOR</span></span>             | <span data-ttu-id="b029d-154">(*R*?</span><span class="sxs-lookup"><span data-stu-id="b029d-154">(*R*?</span></span><span data-ttu-id="b029d-155"> / *k*<sub>R</sub> , *G*?</span><span class="sxs-lookup"><span data-stu-id="b029d-155"> / *k*<sub>R</sub> , *G*?</span></span><span data-ttu-id="b029d-156"> / *k*<sub>G</sub> , *B*?</span><span class="sxs-lookup"><span data-stu-id="b029d-156"> / *k*<sub>G</sub> , *B*?</span></span><span data-ttu-id="b029d-157"> / *k*<sub>B</sub> , *A*?</span><span class="sxs-lookup"><span data-stu-id="b029d-157"> / *k*<sub>B</sub> , *A*?</span></span><span data-ttu-id="b029d-158"> / *k*<sub>A</sub> )</span><span class="sxs-lookup"><span data-stu-id="b029d-158"> / *k*<sub>A</sub> )</span></span>                                                         |
| <span data-ttu-id="b029d-159">GL \_ um \_ menos \_ cor de src \_</span><span class="sxs-lookup"><span data-stu-id="b029d-159">GL\_ONE\_MINUS\_SRC\_COLOR</span></span> | <span data-ttu-id="b029d-160">(1, 1, 1, 1)-(*R*?</span><span class="sxs-lookup"><span data-stu-id="b029d-160">(1,1,1,1) - (*R*?</span></span><span data-ttu-id="b029d-161"> / *k*<sub>R</sub> , *G*?</span><span class="sxs-lookup"><span data-stu-id="b029d-161"> / *k*<sub>R</sub> , *G*?</span></span><span data-ttu-id="b029d-162"> / *k*<sub>G</sub> , *B*?</span><span class="sxs-lookup"><span data-stu-id="b029d-162"> / *k*<sub>G</sub> , *B*?</span></span><span data-ttu-id="b029d-163"> / *k*<sub>B</sub> , *A*?</span><span class="sxs-lookup"><span data-stu-id="b029d-163"> / *k*<sub>B</sub> , *A*?</span></span><span data-ttu-id="b029d-164"> / *k*<sub>A</sub> )</span><span class="sxs-lookup"><span data-stu-id="b029d-164"> / *k*<sub>A</sub> )</span></span>                                             |
| <span data-ttu-id="b029d-165">\_cor de DST do GL \_</span><span class="sxs-lookup"><span data-stu-id="b029d-165">GL\_DST\_COLOR</span></span>             | <span data-ttu-id="b029d-166">(*R*<sub>d</sub>  /  *k*<sub>R</sub> , *g*<sub>d</sub>  /  *k*<sub>G</sub> , *b*<sub>d</sub>  /  *k*<sub>b</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> )</span><span class="sxs-lookup"><span data-stu-id="b029d-166">(*R*<sub>d</sub> / *k*<sub>R</sub> , *G*<sub>d</sub> / *k*<sub>G</sub> , *B*<sub>d</sub> / *k*<sub>B</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> )</span></span>             |
| <span data-ttu-id="b029d-167">GL \_ um \_ menos \_ cor do DST \_</span><span class="sxs-lookup"><span data-stu-id="b029d-167">GL\_ONE\_MINUS\_DST\_COLOR</span></span> | <span data-ttu-id="b029d-168">(1, 1, 1, 1)-(*r*<sub>d</sub>  /  *k*<sub>r</sub> , *g*<sub>d</sub>  /  *k*<sub>g</sub> , *B*<sub>d</sub>  /  *k*<sub>B</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> )</span><span class="sxs-lookup"><span data-stu-id="b029d-168">(1,1,1,1) - (*R*<sub>d</sub> / *k*<sub>R</sub> , *G*<sub>d</sub> / *k*<sub>G</sub> , *B*<sub>d</sub> / *k*<sub>B</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> )</span></span> |
| <span data-ttu-id="b029d-169">\_origem GL \_ alfa</span><span class="sxs-lookup"><span data-stu-id="b029d-169">GL\_SRC\_ALPHA</span></span>             | <span data-ttu-id="b029d-170">(*A*?</span><span class="sxs-lookup"><span data-stu-id="b029d-170">(*A*?</span></span><span data-ttu-id="b029d-171"> / *k*<sub>a</sub> , *A*?</span><span class="sxs-lookup"><span data-stu-id="b029d-171"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="b029d-172"> / *k*<sub>a</sub> , *A*?</span><span class="sxs-lookup"><span data-stu-id="b029d-172"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="b029d-173"> / *k*<sub>a</sub> , *A*?</span><span class="sxs-lookup"><span data-stu-id="b029d-173"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="b029d-174"> / *k*<sub>A</sub> )</span><span class="sxs-lookup"><span data-stu-id="b029d-174"> / *k*<sub>A</sub> )</span></span>                                                         |
| <span data-ttu-id="b029d-175">GL \_ um \_ menos \_ src \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="b029d-175">GL\_ONE\_MINUS\_SRC\_ALPHA</span></span> | <span data-ttu-id="b029d-176">(1, 1, 1, 1)-(*A*?</span><span class="sxs-lookup"><span data-stu-id="b029d-176">(1,1,1,1) - (*A*?</span></span><span data-ttu-id="b029d-177"> / *k*<sub>a</sub> , *A*?</span><span class="sxs-lookup"><span data-stu-id="b029d-177"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="b029d-178"> / *k*<sub>a</sub> , *A*?</span><span class="sxs-lookup"><span data-stu-id="b029d-178"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="b029d-179"> / *k*<sub>a</sub> , *A*?</span><span class="sxs-lookup"><span data-stu-id="b029d-179"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="b029d-180"> / *k*<sub>A</sub> )</span><span class="sxs-lookup"><span data-stu-id="b029d-180"> / *k*<sub>A</sub> )</span></span>                                             |
| <span data-ttu-id="b029d-181">GL \_ DST \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="b029d-181">GL\_DST\_ALPHA</span></span>             | <span data-ttu-id="b029d-182">(*A*<sub>d</sub>  /  *k*<sub>a</sub> , *a d* k a, a <sub>d k a</sub>  /  <sub></sub> <sub></sub>  /  <sub></sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> )</span><span class="sxs-lookup"><span data-stu-id="b029d-182">(*A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> )</span></span>             |
| <span data-ttu-id="b029d-183">GL \_ um \_ menos o \_ DST \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="b029d-183">GL\_ONE\_MINUS\_DST\_ALPHA</span></span> | <span data-ttu-id="b029d-184">(1, 1, 1, 1)-(*a*<sub>d</sub>  /  *k*<sub>a</sub> , *a d k*<sub></sub>  /  <sub></sub> <sub></sub>  /  <sub></sub> <sub></sub>  /  <sub></sub> a, a d k a)</span><span class="sxs-lookup"><span data-stu-id="b029d-184">(1,1,1,1) - (*A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> )</span></span> |
| <span data-ttu-id="b029d-185">GL \_ src \_ alfa \_ saturado</span><span class="sxs-lookup"><span data-stu-id="b029d-185">GL\_SRC\_ALPHA\_SATURATE</span></span>   | <span data-ttu-id="b029d-186">(*i, i, i,* 1)</span><span class="sxs-lookup"><span data-stu-id="b029d-186">(*i,i,i,* 1)</span></span>                                                                                                                                                 |



 

<span data-ttu-id="b029d-187">Na tabela,</span><span class="sxs-lookup"><span data-stu-id="b029d-187">In the table,</span></span>

<span data-ttu-id="b029d-188">*i* = min (*A*?</span><span class="sxs-lookup"><span data-stu-id="b029d-188">*i* = min (*A*?</span></span> <span data-ttu-id="b029d-189">, *k*<sub>a</sub>   -  <sub>d</sub> )/ *k*<sub>A</sub></span><span class="sxs-lookup"><span data-stu-id="b029d-189">, *k*<sub>A</sub>  - *A*<sub>d</sub> ) / *k*<sub>A</sub></span></span>

<span data-ttu-id="b029d-190">Para determinar os valores de RGBA misturados de um pixel ao desenhar no modo RGBA, o sistema usa as seguintes equações:</span><span class="sxs-lookup"><span data-stu-id="b029d-190">To determine the blended RGBA values of a pixel when drawing in RGBA mode, the system uses the following equations:</span></span>

<span data-ttu-id="b029d-191">*R* (*d*) = min ( *k*<sub>r</sub> , *r*? *s*<sub>r r</sub>  +  <sub>d</sub> <sub></sub> r)</span><span class="sxs-lookup"><span data-stu-id="b029d-191">*R* (*d*) = min( *k*<sub>R</sub> , *R*? *s*<sub>R</sub> + *R*<sub>d</sub> *d*<sub>R</sub> )</span></span>

<span data-ttu-id="b029d-192">*G* (*d*) = min ( *k*<sub>g</sub> , *g*? *s*<sub>g</sub>  +  *g*<sub>d</sub> <sub>g</sub> )</span><span class="sxs-lookup"><span data-stu-id="b029d-192">*G* (*d*) = min( *k*<sub>G</sub> , *G*? *s*<sub>G</sub> + *G*<sub>d</sub> *d*<sub>G</sub>  )</span></span>

<span data-ttu-id="b029d-193">*B* (*d*) = min ( *k*<sub>b</sub> *, B*? *s*<sub>b</sub>  +  *b*<sub>d</sub> *b*<sub></sub> )</span><span class="sxs-lookup"><span data-stu-id="b029d-193">*B* (*d*) = min( *k*<sub>B</sub> *, B*? *s*<sub>B</sub> + *B*<sub>d</sub> *d*<sub>B</sub>  )</span></span>

<span data-ttu-id="b029d-194">*A* (*d*) = min ( *k*<sub>A</sub> , *A*? *a*<sub></sub>  +  <sub>d</sub> *d*<sub></sub> a)</span><span class="sxs-lookup"><span data-stu-id="b029d-194">*A* (*d*) = min( *k*<sub>A</sub> , *A*? *s*<sub>A</sub> + *A*<sub>d</sub> *d*<sub>A</sub>  )</span></span>

<span data-ttu-id="b029d-195">Apesar da precisão aparente das equações acima, a aritmética de mistura não é exatamente especificada, pois a mesclagem opera com valores de cor de inteiros imprecisos.</span><span class="sxs-lookup"><span data-stu-id="b029d-195">Despite the apparent precision of the above equations, blending arithmetic is not exactly specified, because blending operates with imprecise integer color values.</span></span> <span data-ttu-id="b029d-196">No entanto, um fator de mistura que deve ser igual a um está garantido para não modificar seu multiplicando, e um fator de mistura igual a zero reduz seu multiplicando para zero.</span><span class="sxs-lookup"><span data-stu-id="b029d-196">However, a blend factor that should be equal to one is guaranteed not to modify its multiplicand, and a blend factor equal to zero reduces its multiplicand to zero.</span></span> <span data-ttu-id="b029d-197">Portanto, por exemplo, quando *sfactor* é GL \_ src \_ Alpha, *dfactor* é GL \_ um \_ menos \_ src \_ alfa e *a*? é igual a *k*<sub>a</sub>, as equações são reduzidas para substituição simples:</span><span class="sxs-lookup"><span data-stu-id="b029d-197">Thus, for example, when *sfactor* is GL\_SRC\_ALPHA, *dfactor* is GL\_ONE\_MINUS\_SRC\_ALPHA, and *A*? is equal to *k*<sub>A</sub>, the equations reduce to simple replacement:</span></span>

<span data-ttu-id="b029d-198">*R*<sub>d</sub>  =  *r*?</span><span class="sxs-lookup"><span data-stu-id="b029d-198">*R*<sub>d</sub> = *R*?</span></span>

<span data-ttu-id="b029d-199">*G*<sub>d</sub>  =  *g*?</span><span class="sxs-lookup"><span data-stu-id="b029d-199">*G*<sub>d</sub> = *G*?</span></span>

<span data-ttu-id="b029d-200">B <sub>d</sub>  =  *b*?</span><span class="sxs-lookup"><span data-stu-id="b029d-200">B <sub>d</sub> = *B*?</span></span>

<span data-ttu-id="b029d-201">*R*<sub>d</sub>  =  *a*?</span><span class="sxs-lookup"><span data-stu-id="b029d-201">*A*<sub>d</sub> = *A*?</span></span>

## <a name="examples"></a><span data-ttu-id="b029d-202">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b029d-202">Examples</span></span>

<span data-ttu-id="b029d-203">A transparência é melhor implementada usando **glBlendFunc**(GL \_ src \_ Alpha, GL \_ um \_ menos \_ src \_ Alpha) com primitivos classificados do mais distante para o mais próximo.</span><span class="sxs-lookup"><span data-stu-id="b029d-203">Transparency is best implemented using **glBlendFunc**(GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA) with primitives sorted from farthest to nearest.</span></span> <span data-ttu-id="b029d-204">Observe que esse cálculo de transparência não requer a presença de bitplanes alfa no framebuffer.</span><span class="sxs-lookup"><span data-stu-id="b029d-204">Note that this transparency calculation does not require the presence of alpha bitplanes in the framebuffer.</span></span>

<span data-ttu-id="b029d-205">Você também pode usar **glBlendFunc**(GL \_ src \_ alfa, GL \_ um \_ menos \_ src \_ Alpha) para renderizar pontos e linhas AntiAlias em ordem arbitrária.</span><span class="sxs-lookup"><span data-stu-id="b029d-205">You can also use **glBlendFunc**(GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA) for rendering antialiased points and lines in arbitrary order.</span></span>

<span data-ttu-id="b029d-206">Para otimizar a suavização do polígono, use **glBlendFunc**(GL \_ src \_ Alpha \_ saturação, GL \_ One) com polígonos classificados do mais próximo ao mais distante.</span><span class="sxs-lookup"><span data-stu-id="b029d-206">To optimize polygon antialiasing, use **glBlendFunc**(GL\_SRC\_ALPHA\_SATURATE, GL\_ONE) with polygons sorted from nearest to farthest.</span></span> <span data-ttu-id="b029d-207">(Consulte o GL \_ \_Argumento Smooth de Polygon em [**glEnable**](glenable.md) para obter informações sobre a anti-aliasing no polígono.) Bitplanes alfa de destino, que deve estar presente para que essa função Blend opere corretamente, armazene a cobertura acumulada.</span><span class="sxs-lookup"><span data-stu-id="b029d-207">(See the GL\_POLYGON\_SMOOTH argument in [**glEnable**](glenable.md) for information on polygon antialiasing.) Destination alpha bitplanes, which must be present for this blend function to operate correctly, store the accumulated coverage.</span></span>

<span data-ttu-id="b029d-208">O alfa de entrada (origem) é uma opacidade de material, variando de 1,0 (*K*<sub>a</sub> ), representando a opacidade completa, para 0,0 (0), representando a transparência completa.</span><span class="sxs-lookup"><span data-stu-id="b029d-208">Incoming (source) alpha is a material opacity, ranging from 1.0 (*K*<sub>A</sub> ), representing complete opacity, to 0.0 (0), representing complete transparency.</span></span>

<span data-ttu-id="b029d-209">Quando você habilita mais de um buffer de cores para o desenho, cada buffer habilitado é mesclado separadamente e o conteúdo do buffer é usado para a cor de destino.</span><span class="sxs-lookup"><span data-stu-id="b029d-209">When you enable more than one color buffer for drawing, each enabled buffer is blended separately, and the contents of the buffer is used for destination color.</span></span> <span data-ttu-id="b029d-210">(Consulte [**glDrawBuffer**](gldrawbuffer.md).)</span><span class="sxs-lookup"><span data-stu-id="b029d-210">(See [**glDrawBuffer**](gldrawbuffer.md).)</span></span>

<span data-ttu-id="b029d-211">A mesclagem afeta apenas a renderização RGBA.</span><span class="sxs-lookup"><span data-stu-id="b029d-211">Blending affects only RGBA rendering.</span></span> <span data-ttu-id="b029d-212">Ele é ignorado por renderizadores de índice de cor.</span><span class="sxs-lookup"><span data-stu-id="b029d-212">It is ignored by color-index renderers.</span></span>

<span data-ttu-id="b029d-213">As funções a seguir recuperam informações relacionadas ao **glBlendFunc**:</span><span class="sxs-lookup"><span data-stu-id="b029d-213">The following functions retrieve information related to **glBlendFunc**:</span></span>

<span data-ttu-id="b029d-214">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ Blend \_ src</span><span class="sxs-lookup"><span data-stu-id="b029d-214">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_BLEND\_SRC</span></span>

<span data-ttu-id="b029d-215">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com Argument GL \_ Blend \_ DST</span><span class="sxs-lookup"><span data-stu-id="b029d-215">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_BLEND\_DST</span></span>

<span data-ttu-id="b029d-216">[**glIsEnabled**](glisenabled.md) com Argument GL \_ Blend</span><span class="sxs-lookup"><span data-stu-id="b029d-216">[**glIsEnabled**](glisenabled.md) with argument GL\_BLEND</span></span>

## <a name="requirements"></a><span data-ttu-id="b029d-217">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b029d-217">Requirements</span></span>



| <span data-ttu-id="b029d-218">Requisito</span><span class="sxs-lookup"><span data-stu-id="b029d-218">Requirement</span></span> | <span data-ttu-id="b029d-219">Valor</span><span class="sxs-lookup"><span data-stu-id="b029d-219">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b029d-220">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b029d-220">Minimum supported client</span></span><br/> | <span data-ttu-id="b029d-221">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b029d-221">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b029d-222">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b029d-222">Minimum supported server</span></span><br/> | <span data-ttu-id="b029d-223">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b029d-223">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b029d-224">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b029d-224">Header</span></span><br/>                   | <dl> <span data-ttu-id="b029d-225"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b029d-225"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b029d-226">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b029d-226">Library</span></span><br/>                  | <dl> <span data-ttu-id="b029d-227"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b029d-227"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b029d-228">DLL</span><span class="sxs-lookup"><span data-stu-id="b029d-228">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b029d-229"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b029d-229"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b029d-230">Confira também</span><span class="sxs-lookup"><span data-stu-id="b029d-230">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b029d-231">**glAlphaFunc**</span><span class="sxs-lookup"><span data-stu-id="b029d-231">**glAlphaFunc**</span></span>](glalphafunc.md)
</dt> <dt>

[<span data-ttu-id="b029d-232">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b029d-232">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b029d-233">**glClear**</span><span class="sxs-lookup"><span data-stu-id="b029d-233">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="b029d-234">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="b029d-234">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="b029d-235">**glDrawBuffer**</span><span class="sxs-lookup"><span data-stu-id="b029d-235">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="b029d-236">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="b029d-236">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="b029d-237">**glGet**</span><span class="sxs-lookup"><span data-stu-id="b029d-237">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="b029d-238">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="b029d-238">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="b029d-239">**glLogicOp**</span><span class="sxs-lookup"><span data-stu-id="b029d-239">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="b029d-240">**glStencilFunc**</span><span class="sxs-lookup"><span data-stu-id="b029d-240">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> </dl>

 

 





