---
title: função glGetMapiv (GL. h)
description: As funções glGetMapdv, glGetMapfv e glGetMapiv retornam parâmetros do avaliador. | função glGetMapiv (GL. h)
ms.assetid: bc055451-7c20-4a8a-96dd-55c877700714
keywords:
- função glGetMapiv OpenGL
topic_type:
- apiref
api_name:
- glGetMapiv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fc8bf74a80916434f806e2e1f46b633b7243e61
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105755983"
---
# <a name="glgetmapiv-function"></a><span data-ttu-id="56fb7-105">função glGetMapiv</span><span class="sxs-lookup"><span data-stu-id="56fb7-105">glGetMapiv function</span></span>

<span data-ttu-id="56fb7-106">As funções [**glGetMapdv**](glgetmapdv.md), [**glGetMapfv**](glgetmapfv.md)e **glGetMapiv** retornam parâmetros do avaliador.</span><span class="sxs-lookup"><span data-stu-id="56fb7-106">The [**glGetMapdv**](glgetmapdv.md), [**glGetMapfv**](glgetmapfv.md), and **glGetMapiv** functions return evaluator parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="56fb7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="56fb7-107">Syntax</span></span>


```C++
void WINAPI glGetMapiv(
   GLenum target,
   GLenum query,
   GLint  *v
);
```



## <a name="parameters"></a><span data-ttu-id="56fb7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="56fb7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56fb7-109">*destino*</span><span class="sxs-lookup"><span data-stu-id="56fb7-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="56fb7-110">O nome simbólico de um mapa.</span><span class="sxs-lookup"><span data-stu-id="56fb7-110">The symbolic name of a map.</span></span> <span data-ttu-id="56fb7-111">Estes são os valores aceitos: GL \_ MAP1 \_ Color \_ 4, GL \_ MAP1 \_ index, GL \_ MAP1 \_ normal, GL \_ MAP1 \_ Texture \_ coord \_ 1, GL \_ MAP1 \_ textura \_ coord \_ 2, GL \_ MAP1 \_ textura \_ coord \_ 3, GL MAP1 de \_ \_ textura \_ coord \_ 4, GL \_ MAP1 \_ vértice \_ 3, GL \_ MAP1 \_ vértice \_ 4, GL \_ map2 \_ cor \_ 4, GL \_ map2 \_ index, GL \_ map2 \_ normal, GL map2 Texture coord 1, GL map2 de \_ \_ \_ \_ \_ \_ textura \_ coord \_ 2, GL map2 de textura coord \_ \_ \_ \_ 3, GL \_ map2 \_ Texture \_ coord 4, GL map2 \_ \_ \_ vértice 3 e \_ GL \_ map2 \_ vértice \_ 4.</span><span class="sxs-lookup"><span data-stu-id="56fb7-111">The following are accepted values: GL\_MAP1\_COLOR\_4, GL\_MAP1\_INDEX, GL\_MAP1\_NORMAL, GL\_MAP1\_TEXTURE\_COORD\_1, GL\_MAP1\_TEXTURE\_COORD\_2, GL\_MAP1\_TEXTURE\_COORD\_3, GL\_MAP1\_TEXTURE\_COORD\_4, GL\_MAP1\_VERTEX\_3, GL\_MAP1\_VERTEX\_4, GL\_MAP2\_COLOR\_4, GL\_MAP2\_INDEX, GL\_MAP2\_NORMAL, GL\_MAP2\_TEXTURE\_COORD\_1, GL\_MAP2\_TEXTURE\_COORD\_2, GL\_MAP2\_TEXTURE\_COORD\_3, GL\_MAP2\_TEXTURE\_COORD\_4, GL\_MAP2\_VERTEX\_3, and GL\_MAP2\_VERTEX\_4.</span></span>

</dd> <dt>

<span data-ttu-id="56fb7-112">*consulta*</span><span class="sxs-lookup"><span data-stu-id="56fb7-112">*query*</span></span> 
</dt> <dd>

<span data-ttu-id="56fb7-113">Especifica qual parâmetro retornar.</span><span class="sxs-lookup"><span data-stu-id="56fb7-113">Specifies which parameter to return.</span></span> <span data-ttu-id="56fb7-114">Os nomes simbólicos a seguir são aceitos.</span><span class="sxs-lookup"><span data-stu-id="56fb7-114">The following symbolic names are accepted.</span></span>



| <span data-ttu-id="56fb7-115">Valor</span><span class="sxs-lookup"><span data-stu-id="56fb7-115">Value</span></span>                                                                                                                                             | <span data-ttu-id="56fb7-116">Significado</span><span class="sxs-lookup"><span data-stu-id="56fb7-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COEFF"></span><span id="gl_coeff"></span><dl> <span data-ttu-id="56fb7-117"><dt>**\_COEFF GL**</dt></span><span class="sxs-lookup"><span data-stu-id="56fb7-117"><dt>**GL\_COEFF**</dt></span></span> </dl>    | <span data-ttu-id="56fb7-118">O parâmetro *v* retorna os pontos de controle para a função do avaliador.</span><span class="sxs-lookup"><span data-stu-id="56fb7-118">The *v* parameter returns the control points for the evaluator function.</span></span> <span data-ttu-id="56fb7-119">Os avaliadores unidimensionais retornam pontos de controle de *ordem* e avaliadores bidimensionais retornam pontos de controle *uorder* *x* *Vorder* .</span><span class="sxs-lookup"><span data-stu-id="56fb7-119">One-dimensional evaluators return *order* control points, and two-dimensional evaluators return *uorder* *x* *vorder* control points.</span></span> <span data-ttu-id="56fb7-120">Cada ponto de controle consiste em um, dois, três ou quatro valores inteiros, de ponto flutuante de precisão simples ou de ponto flutuante de precisão dupla, dependendo do tipo do avaliador.</span><span class="sxs-lookup"><span data-stu-id="56fb7-120">Each control point consists of one, two, three, or four integer, single-precision floating-point, or double-precision floating-point values, depending on the type of the evaluator.</span></span> <span data-ttu-id="56fb7-121">Pontos de controle bidimensionais são retornados em ordem de linha principal, incrementando o índice *uorder* rapidamente e o índice *Vorder* após cada linha.</span><span class="sxs-lookup"><span data-stu-id="56fb7-121">Two-dimensional control points are returned in row-major order, incrementing the *uorder* index quickly, and the *vorder* index after each row.</span></span> <span data-ttu-id="56fb7-122">Os valores inteiros, quando solicitados, são calculados arredondando os valores de ponto flutuante internos para os valores inteiros mais próximos.</span><span class="sxs-lookup"><span data-stu-id="56fb7-122">Integer values, when requested, are computed by rounding the internal floating-point values to the nearest integer values.</span></span><br/> |
| <span id="GL_ORDER"></span><span id="gl_order"></span><dl> <span data-ttu-id="56fb7-123"><dt>**\_ordem GL**</dt></span><span class="sxs-lookup"><span data-stu-id="56fb7-123"><dt>**GL\_ORDER**</dt></span></span> </dl>    | <span data-ttu-id="56fb7-124">O parâmetro *v* retorna a ordem da função do avaliador.</span><span class="sxs-lookup"><span data-stu-id="56fb7-124">The *v* parameter returns the order of the evaluator function.</span></span> <span data-ttu-id="56fb7-125">Os avaliadores unidimensionais retornam um único valor, *ordem*.</span><span class="sxs-lookup"><span data-stu-id="56fb7-125">One-dimensional evaluators return a single value, *order*.</span></span> <span data-ttu-id="56fb7-126">Os avaliadores bidimensionais retornam dois valores, *uorder* e *Vorder*.</span><span class="sxs-lookup"><span data-stu-id="56fb7-126">Two-dimensional evaluators return two values, *uorder* and *vorder*.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_DOMAIN"></span><span id="gl_domain"></span><dl> <span data-ttu-id="56fb7-127"><dt>**\_domínio GL**</dt></span><span class="sxs-lookup"><span data-stu-id="56fb7-127"><dt>**GL\_DOMAIN**</dt></span></span> </dl> | <span data-ttu-id="56fb7-128">O parâmetro *v* retorna os parâmetros lineares de mapeamento *u* e *v* .</span><span class="sxs-lookup"><span data-stu-id="56fb7-128">The *v* parameter returns the linear *u* and *v* mapping parameters.</span></span> <span data-ttu-id="56fb7-129">Os avaliadores unidimensionais retornam dois valores, *u* 1 e *u* 2, conforme especificado por [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="56fb7-129">One-dimensional evaluators return two values, *u* 1 and *u* 2, as specified by [**glMap1**](glmap1.md).</span></span> <span data-ttu-id="56fb7-130">Os avaliadores bidimensionais retornam quatro valores (*U1*, *U2*, *v1* e *v2*), conforme especificado por [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="56fb7-130">Two-dimensional evaluators return four values (*u1*, *u2*, *v1*, and *v2*) as specified by [**glMap2**](glmap2.md).</span></span> <span data-ttu-id="56fb7-131">Os valores inteiros, quando solicitados, são calculados arredondando os valores de ponto flutuante internos para os valores inteiros mais próximos.</span><span class="sxs-lookup"><span data-stu-id="56fb7-131">Integer values, when requested, are computed by rounding the internal floating-point values to the nearest integer values.</span></span><br/>                                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="56fb7-132">*l*</span><span class="sxs-lookup"><span data-stu-id="56fb7-132">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="56fb7-133">Retorna os dados solicitados.</span><span class="sxs-lookup"><span data-stu-id="56fb7-133">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56fb7-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="56fb7-134">Return value</span></span>

<span data-ttu-id="56fb7-135">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="56fb7-135">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="56fb7-136">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="56fb7-136">Error codes</span></span>

<span data-ttu-id="56fb7-137">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="56fb7-137">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="56fb7-138">Nome</span><span class="sxs-lookup"><span data-stu-id="56fb7-138">Name</span></span>                                                                                                  | <span data-ttu-id="56fb7-139">Significado</span><span class="sxs-lookup"><span data-stu-id="56fb7-139">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="56fb7-140"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="56fb7-140"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="56fb7-141">o *destino* ou a *consulta* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="56fb7-141">*target* or *query* was not an accepted value.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="56fb7-142"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="56fb7-142"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="56fb7-143">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="56fb7-143">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="56fb7-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="56fb7-144">Remarks</span></span>

<span data-ttu-id="56fb7-145">As funções **glGetMap** retornam parâmetros do avaliador.</span><span class="sxs-lookup"><span data-stu-id="56fb7-145">The **glGetMap** functions return evaluator parameters.</span></span> <span data-ttu-id="56fb7-146">(As funções **glMap1** e **glMap2** definem avaliadores.) O parâmetro de *destino* especifica um mapa, a *consulta* seleciona um parâmetro específico e o *v* aponta para o armazenamento onde os valores serão retornados.</span><span class="sxs-lookup"><span data-stu-id="56fb7-146">(The **glMap1** and **glMap2** functions define evaluators.) The *target* parameter specifies a map, *query* selects a specific parameter, and *v* points to storage where the values will be returned.</span></span>

<span data-ttu-id="56fb7-147">Os valores aceitáveis para o parâmetro de *destino* são descritos em [**glMap1**](glmap1.md) e [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="56fb7-147">The acceptable values for the *target* parameter are described in [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span>

<span data-ttu-id="56fb7-148">Se um erro for gerado, nenhuma alteração será feita no conteúdo de *v*.</span><span class="sxs-lookup"><span data-stu-id="56fb7-148">If an error is generated, no change is made to the contents of *v*.</span></span>

## <a name="requirements"></a><span data-ttu-id="56fb7-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56fb7-149">Requirements</span></span>



| <span data-ttu-id="56fb7-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="56fb7-150">Requirement</span></span> | <span data-ttu-id="56fb7-151">Valor</span><span class="sxs-lookup"><span data-stu-id="56fb7-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56fb7-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="56fb7-152">Minimum supported client</span></span><br/> | <span data-ttu-id="56fb7-153">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="56fb7-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="56fb7-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="56fb7-154">Minimum supported server</span></span><br/> | <span data-ttu-id="56fb7-155">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="56fb7-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="56fb7-156">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="56fb7-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="56fb7-157"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="56fb7-157"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="56fb7-158">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="56fb7-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="56fb7-159"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="56fb7-159"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="56fb7-160">DLL</span><span class="sxs-lookup"><span data-stu-id="56fb7-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56fb7-161"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56fb7-161"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56fb7-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="56fb7-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56fb7-163">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="56fb7-163">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="56fb7-164">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="56fb7-164">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="56fb7-165">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="56fb7-165">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="56fb7-166">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="56fb7-166">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="56fb7-167">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="56fb7-167">**glMap2**</span></span>](glmap2.md)
</dt> </dl>

 

 





