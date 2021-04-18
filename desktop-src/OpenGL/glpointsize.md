---
title: função glPointSize (GL. h)
description: A função glPointSize especifica o diâmetro de pontos rasterizados.
ms.assetid: efa35fa8-721a-48e5-bf59-d33b9bbe7f73
keywords:
- função glPointSize OpenGL
topic_type:
- apiref
api_name:
- glPointSize
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e6b9525e302cad1eb940184eb5eb83e11744bba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756395"
---
# <a name="glpointsize-function"></a><span data-ttu-id="dddb2-104">função glPointSize</span><span class="sxs-lookup"><span data-stu-id="dddb2-104">glPointSize function</span></span>

<span data-ttu-id="dddb2-105">A função **glPointSize** especifica o diâmetro de pontos rasterizados.</span><span class="sxs-lookup"><span data-stu-id="dddb2-105">The **glPointSize** function specifies the diameter of rasterized points.</span></span>

## <a name="syntax"></a><span data-ttu-id="dddb2-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dddb2-106">Syntax</span></span>


```C++
void WINAPI glPointSize(
   GLfloat size
);
```



## <a name="parameters"></a><span data-ttu-id="dddb2-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dddb2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dddb2-108">*size*</span><span class="sxs-lookup"><span data-stu-id="dddb2-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="dddb2-109">O diâmetro de pontos rasterizados.</span><span class="sxs-lookup"><span data-stu-id="dddb2-109">The diameter of rasterized points.</span></span> <span data-ttu-id="dddb2-110">O padrão é 1.0.</span><span class="sxs-lookup"><span data-stu-id="dddb2-110">The default is 1.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dddb2-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dddb2-111">Return value</span></span>

<span data-ttu-id="dddb2-112">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="dddb2-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="dddb2-113">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="dddb2-113">Error codes</span></span>

<span data-ttu-id="dddb2-114">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="dddb2-114">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="dddb2-115">Nome</span><span class="sxs-lookup"><span data-stu-id="dddb2-115">Name</span></span>                                                                                                  | <span data-ttu-id="dddb2-116">Significado</span><span class="sxs-lookup"><span data-stu-id="dddb2-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dddb2-117"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dddb2-117"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="dddb2-118">o *tamanho* era menor ou igual a zero.</span><span class="sxs-lookup"><span data-stu-id="dddb2-118">*size* was less than or equal to zero.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="dddb2-119"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dddb2-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="dddb2-120">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="dddb2-120">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="dddb2-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="dddb2-121">Remarks</span></span>

<span data-ttu-id="dddb2-122">A função **glPointSize** especifica o diâmetro rasterizado de pontos com alias e com alias.</span><span class="sxs-lookup"><span data-stu-id="dddb2-122">The **glPointSize** function specifies the rasterized diameter of both aliased and antialiased points.</span></span> <span data-ttu-id="dddb2-123">O uso de um tamanho de ponto diferente de 1,0 tem efeitos diferentes, dependendo se a suavização de ponto está habilitada.</span><span class="sxs-lookup"><span data-stu-id="dddb2-123">Using a point size other than 1.0 has different effects, depending on whether point antialiasing is enabled.</span></span> <span data-ttu-id="dddb2-124">A suavização de ponto é controlada chamando [**glEnable**](glenable.md) e **glDisable** com o argumento GL de \_ ponto \_ .</span><span class="sxs-lookup"><span data-stu-id="dddb2-124">Point antialiasing is controlled by calling [**glEnable**](glenable.md) and **glDisable** with argument GL\_POINT\_SMOOTH.</span></span>

<span data-ttu-id="dddb2-125">Se a suavização de ponto estiver desabilitada, o tamanho real será determinado arredondando o tamanho fornecido para o número inteiro mais próximo.</span><span class="sxs-lookup"><span data-stu-id="dddb2-125">If point antialiasing is disabled, the actual size is determined by rounding the supplied size to the nearest integer.</span></span> <span data-ttu-id="dddb2-126">(Se o arredondamento resultar no valor 0, será como se o tamanho do ponto fosse 1.) Se o tamanho arredondado for ímpar, o ponto central (*x*,*y*) do fragmento de pixel que representa o ponto será computado como</span><span class="sxs-lookup"><span data-stu-id="dddb2-126">(If the rounding results in the value 0, it is as if the point size were 1.) If the rounded size is odd, then the center point (*x*,*y*) of the pixel fragment that represents the point is computed as</span></span>

<span data-ttu-id="dddb2-127">(*x*<sub>w</sub> + 0,5, *y*<sub>w</sub> +. 5)</span><span class="sxs-lookup"><span data-stu-id="dddb2-127">(*x*<sub>w</sub> + .5, *y*<sub>w</sub> + .5)</span></span>

<span data-ttu-id="dddb2-128">onde *os* subscritos indicam as coordenadas da janela.</span><span class="sxs-lookup"><span data-stu-id="dddb2-128">where *w* subscripts indicate window coordinates.</span></span> <span data-ttu-id="dddb2-129">Todos os pixels que estão dentro da grade quadrada do tamanho arredondado em (*x*,*y*) compõem o fragmento.</span><span class="sxs-lookup"><span data-stu-id="dddb2-129">All pixels that lie within the square grid of the rounded size centered at (*x*,*y*) make up the fragment.</span></span> <span data-ttu-id="dddb2-130">Se o tamanho for par, o ponto central será</span><span class="sxs-lookup"><span data-stu-id="dddb2-130">If the size is even, the center point is</span></span>

<span data-ttu-id="dddb2-131">(*x*<sub>w</sub> + 0,5, *y*<sub>w</sub> +. 5)</span><span class="sxs-lookup"><span data-stu-id="dddb2-131">(*x*<sub>w</sub> + .5, *y*<sub>w</sub> + .5)</span></span>

<span data-ttu-id="dddb2-132">e os centros do fragmento rasterizado são as coordenadas da janela de metade do inteiro dentro do quadrado do tamanho arredondado centralizado em (*x*,*y*).</span><span class="sxs-lookup"><span data-stu-id="dddb2-132">and the rasterized fragment's centers are the half-integer window coordinates within the square of the rounded size centered at (*x*,*y*).</span></span> <span data-ttu-id="dddb2-133">Todos os fragmentos de pixel produzidos na rasterização de um ponto de nonantialiased são atribuídos aos mesmos dados associados; o do vértice correspondente ao ponto.</span><span class="sxs-lookup"><span data-stu-id="dddb2-133">All pixel fragments produced in rasterizing a nonantialiased point are assigned the same associated data; that of the vertex corresponding to the point.</span></span>

<span data-ttu-id="dddb2-134">Se a suavização estiver habilitada, a rasterização de ponto produzirá um fragmento para cada quadrado de pixel que interseccionará a região em que o círculo tem o diâmetro igual ao tamanho do ponto atual e centralizado nos pontos (*x*<sub>w</sub> ,*y*<sub>w</sub> ).</span><span class="sxs-lookup"><span data-stu-id="dddb2-134">If antialiasing is enabled, then point rasterization produces a fragment for each pixel square that intersects the region lying within the circle having diameter equal to the current point size and centered at the points (*x*<sub>w</sub> ,*y*<sub>w</sub> ).</span></span> <span data-ttu-id="dddb2-135">O valor de cobertura para cada fragmento é a área de coordenadas da janela da interseção da região circular com o quadrado de pixel correspondente.</span><span class="sxs-lookup"><span data-stu-id="dddb2-135">The coverage value for each fragment is the window coordinate area of the intersection of the circular region with the corresponding pixel square.</span></span> <span data-ttu-id="dddb2-136">Esse valor é salvo e usado na etapa de rasterização final.</span><span class="sxs-lookup"><span data-stu-id="dddb2-136">This value is saved and used in the final rasterization step.</span></span> <span data-ttu-id="dddb2-137">Os dados associados a cada fragmento são os dados associados ao ponto que está sendo rasterizado.</span><span class="sxs-lookup"><span data-stu-id="dddb2-137">The data associated with each fragment is the data associated with the point being rasterized.</span></span>

<span data-ttu-id="dddb2-138">Nem todos os tamanhos têm suporte quando a suavização de ponto está habilitada.</span><span class="sxs-lookup"><span data-stu-id="dddb2-138">Not all sizes are supported when point antialiasing is enabled.</span></span> <span data-ttu-id="dddb2-139">Se um tamanho sem suporte for solicitado, o tamanho mais próximo com suporte será usado.</span><span class="sxs-lookup"><span data-stu-id="dddb2-139">If an unsupported size is requested, the nearest supported size is used.</span></span> <span data-ttu-id="dddb2-140">Há garantia de suporte apenas para o tamanho 1,0; outras dependem da implementação.</span><span class="sxs-lookup"><span data-stu-id="dddb2-140">Only size 1.0 is guaranteed to be supported; others depend on the implementation.</span></span> <span data-ttu-id="dddb2-141">O intervalo de tamanhos com suporte e a diferença de tamanho entre os tamanhos com suporte dentro do intervalo pode ser consultado chamando [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com Arguments GL \_ \_ \_ intervalo de tamanho de ponto e \_ granularidade de tamanho de ponto GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="dddb2-141">The range of supported sizes and the size difference between supported sizes within the range can be queried by calling [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with arguments GL\_POINT\_SIZE\_RANGE and GL\_POINT\_SIZE\_GRANULARITY.</span></span>

<span data-ttu-id="dddb2-142">O tamanho do ponto especificado por **glPointSize** sempre é retornado quando o \_ tamanho do ponto GL \_ é consultado.</span><span class="sxs-lookup"><span data-stu-id="dddb2-142">The point size specified by **glPointSize** is always returned when GL\_POINT\_SIZE is queried.</span></span> <span data-ttu-id="dddb2-143">Fixação MSS e arredondamento para pontos com alias e sem alias não têm efeito sobre o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="dddb2-143">Clamping and rounding for aliased and antialiased points have no effect on the specified value.</span></span>

<span data-ttu-id="dddb2-144">O tamanho de ponto sem alias pode ser clamped a um máximo dependente de implementação.</span><span class="sxs-lookup"><span data-stu-id="dddb2-144">Non-antialiased point size may be clamped to an implementation-dependent maximum.</span></span> <span data-ttu-id="dddb2-145">Embora esse máximo não possa ser consultado, ele não deve ser menor que o valor máximo para pontos AntiAlias, arredondado para o valor inteiro mais próximo.</span><span class="sxs-lookup"><span data-stu-id="dddb2-145">Although this maximum cannot be queried, it must be no less than the maximum value for antialiased points, rounded to the nearest integer value.</span></span>

<span data-ttu-id="dddb2-146">As funções a seguir recuperam informações relacionadas ao **glPointSize**:</span><span class="sxs-lookup"><span data-stu-id="dddb2-146">The following functions retrieve information related to **glPointSize**:</span></span>

<span data-ttu-id="dddb2-147">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ tamanho do ponto GL do argumento \_</span><span class="sxs-lookup"><span data-stu-id="dddb2-147">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_POINT\_SIZE</span></span>

<span data-ttu-id="dddb2-148">intervalo de tamanho de ponto de **glGet** com Argument GL \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="dddb2-148">**glGet** with argument GL\_POINT\_SIZE\_RANGE</span></span>

<span data-ttu-id="dddb2-149">**glGet** com a \_ granularidade do \_ tamanho do ponto GL do argumento \_</span><span class="sxs-lookup"><span data-stu-id="dddb2-149">**glGet** with argument GL\_POINT\_SIZE\_GRANULARITY</span></span>

<span data-ttu-id="dddb2-150">[**glIsEnabled**](glisenabled.md) com o argumento GL \_ Point \_ suavizar</span><span class="sxs-lookup"><span data-stu-id="dddb2-150">[**glIsEnabled**](glisenabled.md) with argument GL\_POINT\_SMOOTH</span></span>

## <a name="requirements"></a><span data-ttu-id="dddb2-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dddb2-151">Requirements</span></span>



| <span data-ttu-id="dddb2-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="dddb2-152">Requirement</span></span> | <span data-ttu-id="dddb2-153">Valor</span><span class="sxs-lookup"><span data-stu-id="dddb2-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dddb2-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dddb2-154">Minimum supported client</span></span><br/> | <span data-ttu-id="dddb2-155">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dddb2-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="dddb2-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dddb2-156">Minimum supported server</span></span><br/> | <span data-ttu-id="dddb2-157">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dddb2-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dddb2-158">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="dddb2-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="dddb2-159"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="dddb2-159"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="dddb2-160">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dddb2-160">Library</span></span><br/>                  | <dl> <span data-ttu-id="dddb2-161"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dddb2-161"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="dddb2-162">DLL</span><span class="sxs-lookup"><span data-stu-id="dddb2-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dddb2-163"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dddb2-163"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dddb2-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="dddb2-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dddb2-165">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="dddb2-165">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="dddb2-166">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="dddb2-166">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="dddb2-167">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="dddb2-167">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="dddb2-168">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="dddb2-168">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





