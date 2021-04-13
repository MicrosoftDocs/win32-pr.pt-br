---
title: função glPolygonOffset (GL. h)
description: A função glPolygonOffset define a escala e as unidades que o OpenGL usa para calcular os valores de profundidade.
ms.assetid: 06bc1aba-1692-40f0-8535-2cb65b487490
keywords:
- função glPolygonOffset OpenGL
topic_type:
- apiref
api_name:
- glPolygonOffset
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84fa7d130fcc300fc1ebe33d091253e33f2d1e03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369693"
---
# <a name="glpolygonoffset-function"></a><span data-ttu-id="e1759-104">função glPolygonOffset</span><span class="sxs-lookup"><span data-stu-id="e1759-104">glPolygonOffset function</span></span>

<span data-ttu-id="e1759-105">A função **glPolygonOffset** define a escala e as unidades que o OpenGL usa para calcular os valores de profundidade.</span><span class="sxs-lookup"><span data-stu-id="e1759-105">The **glPolygonOffset** function sets the scale and units OpenGL uses to calculate depth values.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1759-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e1759-106">Syntax</span></span>


```C++
void WINAPI glPolygonOffset(
   GLfloat factor,
   GLfloat units
);
```



## <a name="parameters"></a><span data-ttu-id="e1759-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e1759-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1759-108">*multi-fator*</span><span class="sxs-lookup"><span data-stu-id="e1759-108">*factor*</span></span> 
</dt> <dd>

<span data-ttu-id="e1759-109">Especifica um fator de escala que é usado para criar um deslocamento de profundidade variável para cada polígono.</span><span class="sxs-lookup"><span data-stu-id="e1759-109">Specifies a scale factor that is used to create a variable depth offset for each polygon.</span></span> <span data-ttu-id="e1759-110">O valor inicial é zero.</span><span class="sxs-lookup"><span data-stu-id="e1759-110">The initial value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="e1759-111">*Unit*</span><span class="sxs-lookup"><span data-stu-id="e1759-111">*units*</span></span> 
</dt> <dd>

<span data-ttu-id="e1759-112">Especifica um valor que é multiplicado por um valor específico de implementação para criar um deslocamento de profundidade constante.</span><span class="sxs-lookup"><span data-stu-id="e1759-112">Specifies a value that is multiplied by an implementation-specific value to create a constant depth offset.</span></span> <span data-ttu-id="e1759-113">O valor inicial é 0.</span><span class="sxs-lookup"><span data-stu-id="e1759-113">The initial value is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1759-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e1759-114">Return value</span></span>

<span data-ttu-id="e1759-115">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e1759-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e1759-116">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="e1759-116">Error codes</span></span>

<span data-ttu-id="e1759-117">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="e1759-117">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e1759-118">Nome</span><span class="sxs-lookup"><span data-stu-id="e1759-118">Name</span></span>                                                                                                  | <span data-ttu-id="e1759-119">Significado</span><span class="sxs-lookup"><span data-stu-id="e1759-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e1759-120"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e1759-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="e1759-121">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="e1759-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e1759-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1759-122">Remarks</span></span>

<span data-ttu-id="e1759-123">Quando o \_ \_ deslocamento do polígono do GL estiver habilitado, o valor de profundidade de cada fragmento será deslocado após ser interpolado dos valores de profundidade dos vértices apropriados.</span><span class="sxs-lookup"><span data-stu-id="e1759-123">When GL\_POLYGON\_OFFSET is enabled, each fragment's depth value will be offset after it is interpolated from the depth values of the appropriate vertices.</span></span> <span data-ttu-id="e1759-124">O valor do deslocamento é *fator* \* ? unidades z + r \* , em que? z é uma medida da alteração em relação à área da tela do polígono, e r é o menor valor que é garantido para produzir um deslocamento resolvido para uma determinada implementação.</span><span class="sxs-lookup"><span data-stu-id="e1759-124">The value of the offset is *factor* \* ?z + r \**units*, where ?z is a measurement of the change in depth relative to the screen area of the polygon, and r is the smallest value that is guaranteed to produce a resolvable offset for a given implementation.</span></span> <span data-ttu-id="e1759-125">O deslocamento é adicionado antes que o teste de profundidade seja executado e antes que o valor seja gravado no buffer de profundidade.</span><span class="sxs-lookup"><span data-stu-id="e1759-125">The offset is added before the depth test is performed and before the value is written into the depth buffer.</span></span>

<span data-ttu-id="e1759-126">A função **glPolygonOffset** é útil para renderizar imagens de linha oculta, para aplicar decals a superfícies e para renderizar sólidos com bordas realçadas.</span><span class="sxs-lookup"><span data-stu-id="e1759-126">The **glPolygonOffset** function is useful for rendering hidden-line images, for applying decals to surfaces, and for rendering solids with highlighted edges.</span></span>

<span data-ttu-id="e1759-127">A função **glPolygonOffset** não tem efeito sobre as coordenadas de profundidade colocadas no buffer de comentários.</span><span class="sxs-lookup"><span data-stu-id="e1759-127">The **glPolygonOffset** function has no effect on depth coordinates placed in the feedback buffer.</span></span> <span data-ttu-id="e1759-128">Ele também não tem nenhum efeito na seleção.</span><span class="sxs-lookup"><span data-stu-id="e1759-128">It also has no effect on selection.</span></span>

<span data-ttu-id="e1759-129">As funções a seguir recuperam informações relacionadas ao **glPolygonOffset**:</span><span class="sxs-lookup"><span data-stu-id="e1759-129">The following functions retrieve information related to **glPolygonOffset**:</span></span>

-   <span data-ttu-id="e1759-130">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com fator de \_ deslocamento do polígono GL do argumento \_ \_</span><span class="sxs-lookup"><span data-stu-id="e1759-130">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_POLYGON\_OFFSET\_FACTOR</span></span>
-   <span data-ttu-id="e1759-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com as \_ unidades de \_ deslocamento do polígono do Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="e1759-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_POLYGON\_OFFSET\_UNITS</span></span>
-   <span data-ttu-id="e1759-132">[**glIsEnabled**](glisenabled.md) com argumento de \_ preenchimento de polígono do Argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="e1759-132">[**glIsEnabled**](glisenabled.md) with argument GL\_POLYGON\_OFFSET\_FILL</span></span>
-   <span data-ttu-id="e1759-133">[**glIsEnabled**](glisenabled.md) com linha de \_ deslocamento do polígono do Argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="e1759-133">[**glIsEnabled**](glisenabled.md) with argument GL\_POLYGON\_OFFSET\_LINE</span></span>
-   <span data-ttu-id="e1759-134">[**glIsEnabled**](glisenabled.md) com ponto de \_ deslocamento do polígono do Argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="e1759-134">[**glIsEnabled**](glisenabled.md) with argument GL\_POLYGON\_OFFSET\_POINT</span></span>

> [!Note]  
> <span data-ttu-id="e1759-135">A função **glPolygonOffset** só está disponível no OpenGl versão 1,1 ou superior.</span><span class="sxs-lookup"><span data-stu-id="e1759-135">The **glPolygonOffset** function is only available in OpenGl version 1.1 or greater.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e1759-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1759-136">Requirements</span></span>



| <span data-ttu-id="e1759-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1759-137">Requirement</span></span> | <span data-ttu-id="e1759-138">Valor</span><span class="sxs-lookup"><span data-stu-id="e1759-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1759-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1759-139">Minimum supported client</span></span><br/> | <span data-ttu-id="e1759-140">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e1759-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e1759-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1759-141">Minimum supported server</span></span><br/> | <span data-ttu-id="e1759-142">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e1759-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e1759-143">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e1759-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1759-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1759-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e1759-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e1759-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="e1759-146"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e1759-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e1759-147">DLL</span><span class="sxs-lookup"><span data-stu-id="e1759-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1759-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1759-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1759-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1759-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1759-150">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="e1759-150">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="e1759-151">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="e1759-151">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="e1759-152">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="e1759-152">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="e1759-153">**glGet**</span><span class="sxs-lookup"><span data-stu-id="e1759-153">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="e1759-154">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="e1759-154">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="e1759-155">**glLineWidth**</span><span class="sxs-lookup"><span data-stu-id="e1759-155">**glLineWidth**</span></span>](gllinewidth.md)
</dt> <dt>

[<span data-ttu-id="e1759-156">**glStencilOp**</span><span class="sxs-lookup"><span data-stu-id="e1759-156">**glStencilOp**</span></span>](glstencilop.md)
</dt> <dt>

[<span data-ttu-id="e1759-157">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="e1759-157">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> </dl>

 

 





