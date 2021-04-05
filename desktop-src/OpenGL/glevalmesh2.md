---
title: função glEvalMesh2 (GL. h)
description: Computa uma grade bidimensional de pontos ou linhas.
ms.assetid: 21e94388-903e-4b9d-8e54-9c914d0ce372
keywords:
- função glEvalMesh2 OpenGL
topic_type:
- apiref
api_name:
- glEvalMesh2
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 531e9f1f6288116d052c728654cd2cf03f38550a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644442"
---
# <a name="glevalmesh2-function"></a><span data-ttu-id="5653d-104">função glEvalMesh2</span><span class="sxs-lookup"><span data-stu-id="5653d-104">glEvalMesh2 function</span></span>

<span data-ttu-id="5653d-105">Computa uma grade bidimensional de pontos ou linhas.</span><span class="sxs-lookup"><span data-stu-id="5653d-105">Computes a two-dimensional grid of points or lines.</span></span>

## <a name="syntax"></a><span data-ttu-id="5653d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5653d-106">Syntax</span></span>


```C++
void WINAPI glEvalMesh2(
   GLenum mode,
   GLint  i1,
   GLint  i2,
   GLint  j1,
   GLint  j2
);
```



## <a name="parameters"></a><span data-ttu-id="5653d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5653d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5653d-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="5653d-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="5653d-109">Um valor que especifica se deve-se computar uma malha bidimensional de pontos, linhas ou polígonos.</span><span class="sxs-lookup"><span data-stu-id="5653d-109">A value that specifies whether to compute a two-dimensional mesh of points, lines, or polygons.</span></span> <span data-ttu-id="5653d-110">As seguintes constantes simbólicas são aceitas: GL \_ Point, GL \_ line e GL \_ Fill.</span><span class="sxs-lookup"><span data-stu-id="5653d-110">The following symbolic constants are accepted: GL\_POINT, GL\_LINE, and GL\_FILL.</span></span>

</dd> <dt>

<span data-ttu-id="5653d-111">*I1*</span><span class="sxs-lookup"><span data-stu-id="5653d-111">*i1*</span></span> 
</dt> <dd>

<span data-ttu-id="5653d-112">O primeiro valor inteiro para a variável de domínio de grade i.</span><span class="sxs-lookup"><span data-stu-id="5653d-112">The first integer value for grid domain variable i.</span></span>

</dd> <dt>

<span data-ttu-id="5653d-113">*i2*</span><span class="sxs-lookup"><span data-stu-id="5653d-113">*i2*</span></span> 
</dt> <dd>

<span data-ttu-id="5653d-114">O último valor inteiro para a variável de domínio de grade i.</span><span class="sxs-lookup"><span data-stu-id="5653d-114">The last integer value for grid domain variable i.</span></span>

</dd> <dt>

<span data-ttu-id="5653d-115">*j1*</span><span class="sxs-lookup"><span data-stu-id="5653d-115">*j1*</span></span> 
</dt> <dd>

<span data-ttu-id="5653d-116">O primeiro valor inteiro para a variável de domínio de grade j.</span><span class="sxs-lookup"><span data-stu-id="5653d-116">The first integer value for grid domain variable j.</span></span>

</dd> <dt>

<span data-ttu-id="5653d-117">*j2*</span><span class="sxs-lookup"><span data-stu-id="5653d-117">*j2*</span></span> 
</dt> <dd>

<span data-ttu-id="5653d-118">O último valor inteiro para a variável de domínio de grade j.</span><span class="sxs-lookup"><span data-stu-id="5653d-118">The last integer value for grid domain variable j.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5653d-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5653d-119">Return value</span></span>

<span data-ttu-id="5653d-120">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="5653d-120">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5653d-121">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="5653d-121">Error codes</span></span>

<span data-ttu-id="5653d-122">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="5653d-122">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="5653d-123">Nome</span><span class="sxs-lookup"><span data-stu-id="5653d-123">Name</span></span>                                                                                                  | <span data-ttu-id="5653d-124">Significado</span><span class="sxs-lookup"><span data-stu-id="5653d-124">Meaning</span></span>                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5653d-125"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="5653d-125"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="5653d-126">Indica que o *modo* não é um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="5653d-126">Indicates that *mode* is not an accepted value.</span></span> <br/>                                                                            |
| <dl> <span data-ttu-id="5653d-127"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5653d-127"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="5653d-128">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="5653d-128">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="5653d-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="5653d-129">Remarks</span></span>

<span data-ttu-id="5653d-130">Use [**glMapGrid**](glmapgrid-functions.md) e [**glEvalMesh**](glevalmesh-functions.md) em tandem para gerar e avaliar com eficiência uma série de valores de domínio de mapa com espaçamento uniforme.</span><span class="sxs-lookup"><span data-stu-id="5653d-130">Use [**glMapGrid**](glmapgrid-functions.md) and [**glEvalMesh**](glevalmesh-functions.md) in tandem to efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="5653d-131">A função **glEvalMesh** percorre o domínio inteiro de uma grade de uma ou duas dimensões, cujo intervalo é o domínio dos mapas de avaliação especificados por [**glMap1**](glmap1.md) e [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="5653d-131">The **glEvalMesh** function steps through the integer domain of a one- or two-dimensional grid, whose range is the domain of the evaluation maps specified by [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span> <span data-ttu-id="5653d-132">O parâmetro mode determina se os vértices resultantes são conectados como pontos, linhas ou polígonos preenchidos.</span><span class="sxs-lookup"><span data-stu-id="5653d-132">The mode parameter determines whether the resulting vertices are connected as points, lines, or filled polygons.</span></span>

<span data-ttu-id="5653d-133">No caso bidimensional, **glEvalMesh2**, Let</span><span class="sxs-lookup"><span data-stu-id="5653d-133">In the two-dimensional case, **glEvalMesh2**, let</span></span>

<span data-ttu-id="5653d-134">?</span><span class="sxs-lookup"><span data-stu-id="5653d-134">?</span></span> <span data-ttu-id="5653d-135">u = (U2 U1)/n</span><span class="sxs-lookup"><span data-stu-id="5653d-135">u = (u2 u1)/n</span></span>

<span data-ttu-id="5653d-136">?</span><span class="sxs-lookup"><span data-stu-id="5653d-136">?</span></span> <span data-ttu-id="5653d-137">v = (v2 v1)/m,</span><span class="sxs-lookup"><span data-stu-id="5653d-137">v = (v2 v1)/m,</span></span>

<span data-ttu-id="5653d-138">em que n, U1, U2, m, v1 e v2 são os argumentos para a função [**glMapGrid2**](glmapgrid-functions.md) mais recente.</span><span class="sxs-lookup"><span data-stu-id="5653d-138">where n, u1, u2, m, v1, and v2 are the arguments to the most recent [**glMapGrid2**](glmapgrid-functions.md) function.</span></span> <span data-ttu-id="5653d-139">Em seguida, se *Mode* for GL \_ Fill, **glEvalMesh2** será equivalente a:</span><span class="sxs-lookup"><span data-stu-id="5653d-139">Then, if *mode* is GL\_FILL, **glEvalMesh2** is equivalent to:</span></span>

<span data-ttu-id="5653d-140">para (j = J1; j < J2; j + = 1)</span><span class="sxs-lookup"><span data-stu-id="5653d-140">for (j = j1; j < j2; j += 1)</span></span>

<span data-ttu-id="5653d-141">{</span><span class="sxs-lookup"><span data-stu-id="5653d-141">{</span></span>

<span data-ttu-id="5653d-142">[**glBegin**](glbegin.md)(GL \_ Quad \_ strip);</span><span class="sxs-lookup"><span data-stu-id="5653d-142">[**glBegin**](glbegin.md)(GL\_QUAD\_STRIP);</span></span>

<span data-ttu-id="5653d-143">for (i = i1; i <= i2; i + = 1)</span><span class="sxs-lookup"><span data-stu-id="5653d-143">for (i = i1; i <= i2; i += 1)</span></span>

<span data-ttu-id="5653d-144">{</span><span class="sxs-lookup"><span data-stu-id="5653d-144">{</span></span>

<span data-ttu-id="5653d-145">[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1 (), j?</span><span class="sxs-lookup"><span data-stu-id="5653d-145">[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1 ( ) , j ?</span></span> <span data-ttu-id="5653d-146">v + v1);</span><span class="sxs-lookup"><span data-stu-id="5653d-146">v + v1);</span></span>

<span data-ttu-id="5653d-147">[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1 (), (j + 1)?</span><span class="sxs-lookup"><span data-stu-id="5653d-147">[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1 ( ) , (j+1) ?</span></span> <span data-ttu-id="5653d-148">v + v1);</span><span class="sxs-lookup"><span data-stu-id="5653d-148">v + v1);</span></span>

<span data-ttu-id="5653d-149">}</span><span class="sxs-lookup"><span data-stu-id="5653d-149">}</span></span>

<span data-ttu-id="5653d-150">[**glEnd**](glend.md)(); }</span><span class="sxs-lookup"><span data-stu-id="5653d-150">[**glEnd**](glend.md)( ); }</span></span>

<span data-ttu-id="5653d-151">Se *Mode* for uma \_ linha gl, uma chamada para **glEvalMesh2** será equivalente a:</span><span class="sxs-lookup"><span data-stu-id="5653d-151">If *mode* is GL\_LINE, then a call to **glEvalMesh2** is equivalent to:</span></span>

<span data-ttu-id="5653d-152">para (j = J1; j <= J2; j + = 1)</span><span class="sxs-lookup"><span data-stu-id="5653d-152">for (j = j1; j <= j2; j += 1)</span></span>

<span data-ttu-id="5653d-153">{</span><span class="sxs-lookup"><span data-stu-id="5653d-153">{</span></span>

<span data-ttu-id="5653d-154">[**glBegin**](glbegin.md)( \_ faixa de linha gl \_ );</span><span class="sxs-lookup"><span data-stu-id="5653d-154">[**glBegin**](glbegin.md)(GL\_LINE\_STRIP);</span></span>

<span data-ttu-id="5653d-155">for (i = i1; i <= i2; i + = 1)</span><span class="sxs-lookup"><span data-stu-id="5653d-155">for (i = i1; i <= i2; i += 1)</span></span>

<span data-ttu-id="5653d-156">{</span><span class="sxs-lookup"><span data-stu-id="5653d-156">{</span></span>

<span data-ttu-id="5653d-157">[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1, j? v + v1);</span><span class="sxs-lookup"><span data-stu-id="5653d-157">[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1, j? v + v1);</span></span>

<span data-ttu-id="5653d-158">}</span><span class="sxs-lookup"><span data-stu-id="5653d-158">}</span></span>

<span data-ttu-id="5653d-159">[**glEnd**](glend.md)();</span><span class="sxs-lookup"><span data-stu-id="5653d-159">[**glEnd**](glend.md)( );</span></span>

<span data-ttu-id="5653d-160">}</span><span class="sxs-lookup"><span data-stu-id="5653d-160">}</span></span>

<span data-ttu-id="5653d-161">for (i = i1; i <= i2; i + = 1)</span><span class="sxs-lookup"><span data-stu-id="5653d-161">for (i = i1; i <= i2; i += 1)</span></span>

<span data-ttu-id="5653d-162">{</span><span class="sxs-lookup"><span data-stu-id="5653d-162">{</span></span>

<span data-ttu-id="5653d-163">[**glBegin**](glbegin.md)( \_ faixa de linha gl \_ );</span><span class="sxs-lookup"><span data-stu-id="5653d-163">[**glBegin**](glbegin.md)(GL\_LINE\_STRIP);</span></span>

<span data-ttu-id="5653d-164">para (j = J1; j <= J1; j + = 1)</span><span class="sxs-lookup"><span data-stu-id="5653d-164">for (j = j1; j <= j1; j += 1)</span></span>

<span data-ttu-id="5653d-165">{</span><span class="sxs-lookup"><span data-stu-id="5653d-165">{</span></span>

<span data-ttu-id="5653d-166">[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1, j? v + v1);</span><span class="sxs-lookup"><span data-stu-id="5653d-166">[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1, j? v + v1);</span></span>

<span data-ttu-id="5653d-167">}</span><span class="sxs-lookup"><span data-stu-id="5653d-167">}</span></span>

<span data-ttu-id="5653d-168">glEnd( );</span><span class="sxs-lookup"><span data-stu-id="5653d-168">glEnd( );</span></span>

<span data-ttu-id="5653d-169">}</span><span class="sxs-lookup"><span data-stu-id="5653d-169">}</span></span>

<span data-ttu-id="5653d-170">E, finalmente, se *Mode* for um \_ ponto GL, uma chamada para **glEvalMesh2** será equivalente a:</span><span class="sxs-lookup"><span data-stu-id="5653d-170">And finally, if *mode* is GL\_POINT, then a call to **glEvalMesh2** is equivalent to:</span></span>

<span data-ttu-id="5653d-171">[**glBegin**](glbegin.md)( \_ pontos GL);</span><span class="sxs-lookup"><span data-stu-id="5653d-171">[**glBegin**](glbegin.md)(GL\_POINTS);</span></span>

<span data-ttu-id="5653d-172">para (j = J1; j <= J2; j + = 1)</span><span class="sxs-lookup"><span data-stu-id="5653d-172">for (j = j1; j <= j2; j += 1)</span></span>

<span data-ttu-id="5653d-173">{</span><span class="sxs-lookup"><span data-stu-id="5653d-173">{</span></span>

<span data-ttu-id="5653d-174">for (i = i1; i <= i2; i + = 1)</span><span class="sxs-lookup"><span data-stu-id="5653d-174">for (i = i1; i <= i2; i += 1)</span></span>

<span data-ttu-id="5653d-175">{</span><span class="sxs-lookup"><span data-stu-id="5653d-175">{</span></span>

<span data-ttu-id="5653d-176">[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1, j? v + v1);</span><span class="sxs-lookup"><span data-stu-id="5653d-176">[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1, j? v + v1);</span></span>

<span data-ttu-id="5653d-177">}</span><span class="sxs-lookup"><span data-stu-id="5653d-177">}</span></span>

<span data-ttu-id="5653d-178">}</span><span class="sxs-lookup"><span data-stu-id="5653d-178">}</span></span>

<span data-ttu-id="5653d-179">[**glEnd**](glend.md)();</span><span class="sxs-lookup"><span data-stu-id="5653d-179">[**glEnd**](glend.md)( );</span></span>

<span data-ttu-id="5653d-180">Em todos os três casos, os únicos requisitos numéricos absolutos são que, se eu = n, o valor calculado a partir de i? u + U1 é exatamente U2 e, se j = m, o valor calculado a partir de j? o v + v1 é exatamente v2.</span><span class="sxs-lookup"><span data-stu-id="5653d-180">In all three cases, the only absolute numeric requirements are that if i = n, then the value computed from i? u + u1 is exactly u2, and if j = m, then the value computed from j? v + v1 is exactly v2.</span></span> <span data-ttu-id="5653d-181">As funções a seguir recuperam informações relacionadas a **glEvalMesh**:</span><span class="sxs-lookup"><span data-stu-id="5653d-181">The following functions retrieve information relating to **glEvalMesh**:</span></span>

<span data-ttu-id="5653d-182">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ MAP1 \_ grade \_ Domain</span><span class="sxs-lookup"><span data-stu-id="5653d-182">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_DOMAIN</span></span>

<span data-ttu-id="5653d-183">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ map2 \_ grade \_ Domain</span><span class="sxs-lookup"><span data-stu-id="5653d-183">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_DOMAIN</span></span>

<span data-ttu-id="5653d-184">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com os segmentos de grade Argument GL \_ MAP1 \_ \_</span><span class="sxs-lookup"><span data-stu-id="5653d-184">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_SEGMENTS</span></span>

<span data-ttu-id="5653d-185">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com os segmentos de grade Argument GL \_ map2 \_ \_</span><span class="sxs-lookup"><span data-stu-id="5653d-185">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_SEGMENTS</span></span>

## <a name="requirements"></a><span data-ttu-id="5653d-186">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5653d-186">Requirements</span></span>



| <span data-ttu-id="5653d-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="5653d-187">Requirement</span></span> | <span data-ttu-id="5653d-188">Valor</span><span class="sxs-lookup"><span data-stu-id="5653d-188">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5653d-189">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5653d-189">Minimum supported client</span></span><br/> | <span data-ttu-id="5653d-190">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5653d-190">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5653d-191">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5653d-191">Minimum supported server</span></span><br/> | <span data-ttu-id="5653d-192">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5653d-192">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5653d-193">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5653d-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="5653d-194"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5653d-194"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="5653d-195">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5653d-195">Library</span></span><br/>                  | <dl> <span data-ttu-id="5653d-196"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5653d-196"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5653d-197">DLL</span><span class="sxs-lookup"><span data-stu-id="5653d-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5653d-198"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5653d-198"><dt>Opengl32.dll</dt></span></span> </dl> |



 

 





