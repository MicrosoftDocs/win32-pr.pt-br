---
title: função glGetPixelMapusv (GL. h)
description: As funções glGetPixelMapfv, glGetPixelMapuiv e glGetPixelMapusv retornam o mapa de pixel especificado. | função glGetPixelMapusv (GL. h)
ms.assetid: 68b71f9b-5666-4183-aeb8-4c9f09bc5d9c
keywords:
- função glGetPixelMapusv OpenGL
topic_type:
- apiref
api_name:
- glGetPixelMapusv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a91d7784288c7a98b82814cdaadb352e7ff5b5c3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105756397"
---
# <a name="glgetpixelmapusv-function"></a><span data-ttu-id="aa996-105">função glGetPixelMapusv</span><span class="sxs-lookup"><span data-stu-id="aa996-105">glGetPixelMapusv function</span></span>

<span data-ttu-id="aa996-106">As funções [**glGetPixelMapfv**](glgetpixelmapfv.md), [**glGetPixelMapuiv**](glgetpixelmapuiv.md)e **glGetPixelMapusv** retornam o mapa de pixel especificado.</span><span class="sxs-lookup"><span data-stu-id="aa996-106">The [**glGetPixelMapfv**](glgetpixelmapfv.md), [**glGetPixelMapuiv**](glgetpixelmapuiv.md), and **glGetPixelMapusv** functions return the specified pixel map.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa996-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa996-107">Syntax</span></span>


```C++
void WINAPI glGetPixelMapusv(
   GLenum   map,
   GLushort *values
);
```



## <a name="parameters"></a><span data-ttu-id="aa996-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa996-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa996-109">*map*</span><span class="sxs-lookup"><span data-stu-id="aa996-109">*map*</span></span> 
</dt> <dd>

<span data-ttu-id="aa996-110">O nome do mapa de pixel a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="aa996-110">The name of the pixel map to return.</span></span> <span data-ttu-id="aa996-111">Os valores aceitos são o mapa do pixel GL i, o mapa de \_ \_ \_ \_ \_ \_ pixel GL \_ \_ s \_ para \_ s, o \_ \_ \_ RESIDER pixel MAP i \_ para \_ R, GL \_ pixel \_ map \_ i para G, GL pixel MAP i para b, GL pixel MAP i para \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ a, GL pixel map \_ \_ \_ R \_ para \_ r, GL pixel \_ \_ map \_ G \_ to \_ G, GL pixel \_ \_ map \_ B \_ para \_ b \_ \_ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="aa996-111">Accepted values are GL\_PIXEL\_MAP\_I\_TO\_I, GL\_PIXEL\_MAP\_S\_TO\_S, GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, GL\_PIXEL\_MAP\_I\_TO\_A, GL\_PIXEL\_MAP\_R\_TO\_R, GL\_PIXEL\_MAP\_G\_TO\_G, GL\_PIXEL\_MAP\_B\_TO\_B, and GL\_PIXEL\_MAP\_A\_TO\_A.</span></span>

</dd> <dt>

<span data-ttu-id="aa996-112">*os*</span><span class="sxs-lookup"><span data-stu-id="aa996-112">*values*</span></span> 
</dt> <dd>

<span data-ttu-id="aa996-113">Retorna o conteúdo do mapa de pixel.</span><span class="sxs-lookup"><span data-stu-id="aa996-113">Returns the pixel map contents.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa996-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aa996-114">Return value</span></span>

<span data-ttu-id="aa996-115">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="aa996-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="aa996-116">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="aa996-116">Error codes</span></span>

<span data-ttu-id="aa996-117">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="aa996-117">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="aa996-118">Nome</span><span class="sxs-lookup"><span data-stu-id="aa996-118">Name</span></span>                                                                                                  | <span data-ttu-id="aa996-119">Significado</span><span class="sxs-lookup"><span data-stu-id="aa996-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="aa996-120"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="aa996-120"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="aa996-121">o *mapa* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="aa996-121">*map* was not an accepted value.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="aa996-122"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="aa996-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="aa996-123">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="aa996-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="aa996-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa996-124">Remarks</span></span>

<span data-ttu-id="aa996-125">Consulte [**glPixelMap**](glpixelmap.md) para obter uma descrição dos valores aceitáveis para o parâmetro *MAP* .</span><span class="sxs-lookup"><span data-stu-id="aa996-125">See [**glPixelMap**](glpixelmap.md) for a description of the acceptable values for the *map* parameter.</span></span> <span data-ttu-id="aa996-126">A função **glGetPixelMap** retorna em *valores* o conteúdo do mapa de pixel especificado no *mapa*.</span><span class="sxs-lookup"><span data-stu-id="aa996-126">The **glGetPixelMap** function returns in *values* the contents of the pixel map specified in *map*.</span></span> <span data-ttu-id="aa996-127">Use mapas de pixel durante a execução de [**glReadPixels**](glreadpixels.md), [**glDrawPixels**](gldrawpixels.md), [**glCopyPixels**](glcopypixels.md), [**glTexImage1D**](glteximage1d.md)e [**glTexImage2D**](glteximage2d.md) para mapear índices de cores, índices de estêncil, componentes de cores e componentes de profundidade para outros valores.</span><span class="sxs-lookup"><span data-stu-id="aa996-127">Use pixel maps during the execution of [**glReadPixels**](glreadpixels.md), [**glDrawPixels**](gldrawpixels.md), [**glCopyPixels**](glcopypixels.md), [**glTexImage1D**](glteximage1d.md), and [**glTexImage2D**](glteximage2d.md) to map color indexes, stencil indexes, color components, and depth components to other values.</span></span>

<span data-ttu-id="aa996-128">Valores inteiros não assinados, se solicitados, são mapeados linearmente da representação interna fixa ou de ponto flutuante, de modo que 1,0 é mapeado para o maior valor inteiro representável e 0,0 é mapeado para zero.</span><span class="sxs-lookup"><span data-stu-id="aa996-128">Unsigned integer values, if requested, are linearly mapped from the internal fixed or floating-point representation such that 1.0 maps to the largest representable integer value, and 0.0 maps to zero.</span></span> <span data-ttu-id="aa996-129">Os valores inteiros sem sinal de retorno serão indefinidos se o valor do mapa não estava no intervalo de \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="aa996-129">Return unsigned integer values are undefined if the map value was not in the range \[0,1\].</span></span>

<span data-ttu-id="aa996-130">Para determinar o tamanho necessário do *mapa*, chame [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com a constante simbólica apropriada.</span><span class="sxs-lookup"><span data-stu-id="aa996-130">To determine the required size of *map*, call [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with the appropriate symbolic constant.</span></span>

<span data-ttu-id="aa996-131">Se um erro for gerado, nenhuma alteração será feita no conteúdo dos *valores*.</span><span class="sxs-lookup"><span data-stu-id="aa996-131">If an error is generated, no change is made to the contents of *values*.</span></span>

<span data-ttu-id="aa996-132">As funções a seguir recuperam informações relacionadas ao **glGetPixelMap**:</span><span class="sxs-lookup"><span data-stu-id="aa996-132">The following functions retrieve information related to **glGetPixelMap**:</span></span>

<span data-ttu-id="aa996-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com Argument GL \_ pixel \_ mapa \_ i \_ i \_ \_ size</span><span class="sxs-lookup"><span data-stu-id="aa996-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PIXEL\_MAP\_I\_TO\_I\_SIZE</span></span>

<span data-ttu-id="aa996-134">**glGet** com o argumento GL \_ pixel \_ mapa \_ S para o \_ \_ \_ tamanho s</span><span class="sxs-lookup"><span data-stu-id="aa996-134">**glGet** with argument GL\_PIXEL\_MAP\_S\_TO\_S\_SIZE</span></span>

<span data-ttu-id="aa996-135">**glGet** com Argument GL \_ pixel \_ mapa \_ I \_ para \_ R \_ tamanho</span><span class="sxs-lookup"><span data-stu-id="aa996-135">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_R\_SIZE</span></span>

<span data-ttu-id="aa996-136">**glGet** com Argument GL \_ pixel \_ mapa \_ I \_ para \_ G \_ tamanho</span><span class="sxs-lookup"><span data-stu-id="aa996-136">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_G\_SIZE</span></span>

<span data-ttu-id="aa996-137">**glGet** com Argument GL \_ pixel \_ mapa \_ I \_ para \_ o \_ tamanho B</span><span class="sxs-lookup"><span data-stu-id="aa996-137">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_B\_SIZE</span></span>

<span data-ttu-id="aa996-138">**glGet** com Argument GL \_ pixel \_ mapa \_ I \_ para \_ um \_ tamanho</span><span class="sxs-lookup"><span data-stu-id="aa996-138">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_A\_SIZE</span></span>

<span data-ttu-id="aa996-139">**glGet** com argumento GL \_ pixel \_ mapa \_ r \_ para \_ r \_ tamanho</span><span class="sxs-lookup"><span data-stu-id="aa996-139">**glGet** with argument GL\_PIXEL\_MAP\_R\_TO\_R\_SIZE</span></span>

<span data-ttu-id="aa996-140">**glGet** com Argument GL \_ o \_ mapa \_ \_ de pixel de tamanho de g a \_ G \_</span><span class="sxs-lookup"><span data-stu-id="aa996-140">**glGet** with argument GL\_PIXEL\_MAP\_G\_TO\_G\_SIZE</span></span>

<span data-ttu-id="aa996-141">**glGet** com Argument GL \_ pixel \_ mapa \_ b \_ para \_ B \_ tamanho</span><span class="sxs-lookup"><span data-stu-id="aa996-141">**glGet** with argument GL\_PIXEL\_MAP\_B\_TO\_B\_SIZE</span></span>

<span data-ttu-id="aa996-142">**glGet** com Argument GL \_ pixel \_ Mapear \_ um \_ para \_ um \_ tamanho</span><span class="sxs-lookup"><span data-stu-id="aa996-142">**glGet** with argument GL\_PIXEL\_MAP\_A\_TO\_A\_SIZE</span></span>

<span data-ttu-id="aa996-143">tabela de mapa de pixels de **glGet** com Argument GL \_ Max \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="aa996-143">**glGet** with argument GL\_MAX\_PIXEL\_MAP\_TABLE</span></span>

## <a name="requirements"></a><span data-ttu-id="aa996-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa996-144">Requirements</span></span>



| <span data-ttu-id="aa996-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa996-145">Requirement</span></span> | <span data-ttu-id="aa996-146">Valor</span><span class="sxs-lookup"><span data-stu-id="aa996-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa996-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa996-147">Minimum supported client</span></span><br/> | <span data-ttu-id="aa996-148">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="aa996-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="aa996-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa996-149">Minimum supported server</span></span><br/> | <span data-ttu-id="aa996-150">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="aa996-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="aa996-151">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="aa996-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa996-152"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa996-152"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="aa996-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aa996-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="aa996-154"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aa996-154"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="aa996-155">DLL</span><span class="sxs-lookup"><span data-stu-id="aa996-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa996-156"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa996-156"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa996-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa996-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa996-158">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="aa996-158">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="aa996-159">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="aa996-159">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="aa996-160">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="aa996-160">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="aa996-161">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="aa996-161">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="aa996-162">**glGet**</span><span class="sxs-lookup"><span data-stu-id="aa996-162">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="aa996-163">**glPixelMap**</span><span class="sxs-lookup"><span data-stu-id="aa996-163">**glPixelMap**</span></span>](glpixelmap.md)
</dt> <dt>

[<span data-ttu-id="aa996-164">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="aa996-164">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="aa996-165">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="aa996-165">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="aa996-166">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="aa996-166">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="aa996-167">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="aa996-167">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> </dl>

 

 





