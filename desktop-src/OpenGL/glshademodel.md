---
title: função glShadeModel (GL. h)
description: A função glShadeModel seleciona sombreamento simples ou suave.
ms.assetid: 52985ad7-1d6c-48fc-8f1e-4eb2c0324c8e
keywords:
- função glShadeModel OpenGL
topic_type:
- apiref
api_name:
- glShadeModel
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 142ac518c91c6378f1606235e25502be8c06dd6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754312"
---
# <a name="glshademodel-function"></a><span data-ttu-id="4dba9-104">função glShadeModel</span><span class="sxs-lookup"><span data-stu-id="4dba9-104">glShadeModel function</span></span>

<span data-ttu-id="4dba9-105">A função **glShadeModel** seleciona sombreamento simples ou suave.</span><span class="sxs-lookup"><span data-stu-id="4dba9-105">The **glShadeModel** function selects flat or smooth shading.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dba9-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4dba9-106">Syntax</span></span>


```C++
void WINAPI glShadeModel(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="4dba9-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4dba9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4dba9-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="4dba9-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="4dba9-109">Um valor simbólico que representa uma técnica de sombreamento.</span><span class="sxs-lookup"><span data-stu-id="4dba9-109">A symbolic value representing a shading technique.</span></span> <span data-ttu-id="4dba9-110">Os valores aceitos são o GL \_ Flat e GL \_ Smooth.</span><span class="sxs-lookup"><span data-stu-id="4dba9-110">Accepted values are GL\_FLAT and GL\_SMOOTH.</span></span> <span data-ttu-id="4dba9-111">O padrão é o GL \_ Smooth.</span><span class="sxs-lookup"><span data-stu-id="4dba9-111">The default is GL\_SMOOTH.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4dba9-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4dba9-112">Return value</span></span>

<span data-ttu-id="4dba9-113">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4dba9-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4dba9-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="4dba9-114">Error codes</span></span>

<span data-ttu-id="4dba9-115">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="4dba9-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="4dba9-116">Nome</span><span class="sxs-lookup"><span data-stu-id="4dba9-116">Name</span></span>                                                                                                  | <span data-ttu-id="4dba9-117">Significado</span><span class="sxs-lookup"><span data-stu-id="4dba9-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4dba9-118"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="4dba9-118"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="4dba9-119">o *modo* era um valor diferente de GL \_ GLAT ou GL \_ Smooth.</span><span class="sxs-lookup"><span data-stu-id="4dba9-119">*mode* was a value other than GL\_GLAT or GL\_SMOOTH.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="4dba9-120"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4dba9-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="4dba9-121">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="4dba9-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4dba9-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="4dba9-122">Remarks</span></span>

<span data-ttu-id="4dba9-123">Os primitivos OpenGL podem ter um sombreamento simples ou suave.</span><span class="sxs-lookup"><span data-stu-id="4dba9-123">OpenGL primitives can have either flat or smooth shading.</span></span> <span data-ttu-id="4dba9-124">O sombreamento suave, o padrão, faz com que as cores computadas dos vértices sejam interpoladas conforme o primitivo é rasterizado, normalmente atribuindo cores diferentes a cada fragmento de pixel resultante.</span><span class="sxs-lookup"><span data-stu-id="4dba9-124">Smooth shading, the default, causes the computed colors of vertices to be interpolated as the primitive is rasterized, typically assigning different colors to each resulting pixel fragment.</span></span> <span data-ttu-id="4dba9-125">O sombreamento simples seleciona a cor computada de apenas um vértice e o atribui a todos os fragmentos de pixel gerados pela rasterização de um único primitivo.</span><span class="sxs-lookup"><span data-stu-id="4dba9-125">Flat shading selects the computed color of just one vertex and assigns it to all the pixel fragments generated by rasterizing a single primitive.</span></span> <span data-ttu-id="4dba9-126">Em ambos os casos, a cor computada de um vértice é o resultado da iluminação, se a iluminação estiver habilitada ou se for a cor atual no momento em que o vértice foi especificado, se a iluminação estiver desabilitada.</span><span class="sxs-lookup"><span data-stu-id="4dba9-126">In either case, the computed color of a vertex is the result of lighting, if lighting is enabled, or it is the current color at the time the vertex was specified, if lighting is disabled.</span></span>

<span data-ttu-id="4dba9-127">Sombreamento simples e suaves são indistinguíveis para pontos.</span><span class="sxs-lookup"><span data-stu-id="4dba9-127">Flat and smooth shading are indistinguishable for points.</span></span> <span data-ttu-id="4dba9-128">Contando vértices e primitivas de um, iniciando quando [**glBegin**](glbegin.md) é emitido, cada segmento de linha com sombreamento simples *que* recebe a cor computada do vértice *i* + 1, seu segundo vértice.</span><span class="sxs-lookup"><span data-stu-id="4dba9-128">Counting vertices and primitives from one, starting when [**glBegin**](glbegin.md) is issued, each flat-shaded line segment *i* is given the computed color of vertex *i* + 1, its second vertex.</span></span> <span data-ttu-id="4dba9-129">Contando de forma semelhante a uma, cada polígono com sombreamento simples recebe a cor computada do vértice listado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4dba9-129">Counting similarly from one, each flat-shaded polygon is given the computed color of the vertex listed in the following table.</span></span> <span data-ttu-id="4dba9-130">Este é o último vértice para especificar o polígono em todos os casos, exceto polígonos únicos, em que o primeiro vértice especifica a cor de sombreamento simples.</span><span class="sxs-lookup"><span data-stu-id="4dba9-130">This is the last vertex to specify the polygon in all cases except single polygons, where the first vertex specifies the flat-shaded color.</span></span>



| <span data-ttu-id="4dba9-131">Tipo primitivo de polígono i</span><span class="sxs-lookup"><span data-stu-id="4dba9-131">Primitive type of polygon i</span></span> | <span data-ttu-id="4dba9-132">Vértice</span><span class="sxs-lookup"><span data-stu-id="4dba9-132">Vertex</span></span>   |
|-----------------------------|----------|
| <span data-ttu-id="4dba9-133">Polígono único (*I*= 1)</span><span class="sxs-lookup"><span data-stu-id="4dba9-133">Single polygon (*I*=1)</span></span>      | <span data-ttu-id="4dba9-134">1</span><span class="sxs-lookup"><span data-stu-id="4dba9-134">1</span></span>        |
| <span data-ttu-id="4dba9-135">Faixa de triângulo</span><span class="sxs-lookup"><span data-stu-id="4dba9-135">Triangle strip</span></span>              | <span data-ttu-id="4dba9-136">*i* + 2</span><span class="sxs-lookup"><span data-stu-id="4dba9-136">*i* + 2</span></span>  |
| <span data-ttu-id="4dba9-137">Ventilador de triângulo</span><span class="sxs-lookup"><span data-stu-id="4dba9-137">Triangle fan</span></span>                | <span data-ttu-id="4dba9-138">*i* + 2</span><span class="sxs-lookup"><span data-stu-id="4dba9-138">*i* + 2</span></span>  |
| <span data-ttu-id="4dba9-139">Triângulo independente</span><span class="sxs-lookup"><span data-stu-id="4dba9-139">Independent triangle</span></span>        | <span data-ttu-id="4dba9-140">3 *I*</span><span class="sxs-lookup"><span data-stu-id="4dba9-140">3 *I*</span></span>     |
| <span data-ttu-id="4dba9-141">Faixa quádrupla</span><span class="sxs-lookup"><span data-stu-id="4dba9-141">Quad strip</span></span>                  | <span data-ttu-id="4dba9-142">2 *i* + 2</span><span class="sxs-lookup"><span data-stu-id="4dba9-142">2 *i* + 2</span></span> |
| <span data-ttu-id="4dba9-143">Quádruplo independente</span><span class="sxs-lookup"><span data-stu-id="4dba9-143">Independent quad</span></span>            | <span data-ttu-id="4dba9-144">4 *I*</span><span class="sxs-lookup"><span data-stu-id="4dba9-144">4 *I*</span></span>     |



 

<span data-ttu-id="4dba9-145">Sombreamento simples e suaves são especificados por **glShadeModel** com o *modo* definido como GL \_ Flat e GL \_ Smooth, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="4dba9-145">Flat and smooth shading are specified by **glShadeModel** with *mode* set to GL\_FLAT and GL\_SMOOTH, respectively.</span></span>

<span data-ttu-id="4dba9-146">A função a seguir recupera informações relacionadas a **glShadeModel**:</span><span class="sxs-lookup"><span data-stu-id="4dba9-146">The following function retrieves information related to **glShadeModel**:</span></span>

<span data-ttu-id="4dba9-147">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ modelo de sombra do argumento GL \_</span><span class="sxs-lookup"><span data-stu-id="4dba9-147">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_SHADE\_MODEL</span></span>

## <a name="requirements"></a><span data-ttu-id="4dba9-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4dba9-148">Requirements</span></span>



| <span data-ttu-id="4dba9-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="4dba9-149">Requirement</span></span> | <span data-ttu-id="4dba9-150">Valor</span><span class="sxs-lookup"><span data-stu-id="4dba9-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4dba9-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4dba9-151">Minimum supported client</span></span><br/> | <span data-ttu-id="4dba9-152">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4dba9-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4dba9-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4dba9-153">Minimum supported server</span></span><br/> | <span data-ttu-id="4dba9-154">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4dba9-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4dba9-155">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4dba9-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="4dba9-156"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="4dba9-156"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="4dba9-157">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4dba9-157">Library</span></span><br/>                  | <dl> <span data-ttu-id="4dba9-158"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4dba9-158"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4dba9-159">DLL</span><span class="sxs-lookup"><span data-stu-id="4dba9-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4dba9-160"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4dba9-160"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4dba9-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="4dba9-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dba9-162">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="4dba9-162">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="4dba9-163">**glColor**</span><span class="sxs-lookup"><span data-stu-id="4dba9-163">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="4dba9-164">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="4dba9-164">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="4dba9-165">**glLight**</span><span class="sxs-lookup"><span data-stu-id="4dba9-165">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="4dba9-166">**glLightModel**</span><span class="sxs-lookup"><span data-stu-id="4dba9-166">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> </dl>

 

 





