---
title: função glLineWidth (GL. h)
description: A função glLineWidth especifica a largura das linhas rasterizadas.
ms.assetid: 13a69fd7-5eee-42ec-bd05-5bd3c838d4d7
keywords:
- função glLineWidth OpenGL
topic_type:
- apiref
api_name:
- glLineWidth
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa4cecafc9e5d8e0f55c6e9d0dbfe49924d54f14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753955"
---
# <a name="gllinewidth-function"></a><span data-ttu-id="4515c-104">função glLineWidth</span><span class="sxs-lookup"><span data-stu-id="4515c-104">glLineWidth function</span></span>

<span data-ttu-id="4515c-105">A função **glLineWidth** especifica a largura das linhas rasterizadas.</span><span class="sxs-lookup"><span data-stu-id="4515c-105">The **glLineWidth** function specifies the width of rasterized lines.</span></span>

## <a name="syntax"></a><span data-ttu-id="4515c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4515c-106">Syntax</span></span>


```C++
void WINAPI glLineWidth(
   GLfloat width
);
```



## <a name="parameters"></a><span data-ttu-id="4515c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4515c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4515c-108">*width*</span><span class="sxs-lookup"><span data-stu-id="4515c-108">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="4515c-109">A largura das linhas rasterizadas.</span><span class="sxs-lookup"><span data-stu-id="4515c-109">The width of rasterized lines.</span></span> <span data-ttu-id="4515c-110">O padrão é 1.0.</span><span class="sxs-lookup"><span data-stu-id="4515c-110">The default is 1.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4515c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4515c-111">Return value</span></span>

<span data-ttu-id="4515c-112">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4515c-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4515c-113">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="4515c-113">Error codes</span></span>

<span data-ttu-id="4515c-114">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="4515c-114">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="4515c-115">Nome</span><span class="sxs-lookup"><span data-stu-id="4515c-115">Name</span></span>                                                                                                  | <span data-ttu-id="4515c-116">Significado</span><span class="sxs-lookup"><span data-stu-id="4515c-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4515c-117"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4515c-117"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="4515c-118">a *largura* era menor ou igual a zero.</span><span class="sxs-lookup"><span data-stu-id="4515c-118">*width* was less than or equal to zero.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="4515c-119"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4515c-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="4515c-120">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="4515c-120">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4515c-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="4515c-121">Remarks</span></span>

<span data-ttu-id="4515c-122">A função **glLineWidth** especifica a largura rasterizada das linhas com alias e com suavização de alias.</span><span class="sxs-lookup"><span data-stu-id="4515c-122">The **glLineWidth** function specifies the rasterized width of both aliased and antialiased lines.</span></span> <span data-ttu-id="4515c-123">O uso de uma largura de linha diferente de 1,0 tem efeitos diferentes, dependendo se a suavização de linha está habilitada.</span><span class="sxs-lookup"><span data-stu-id="4515c-123">Using a line width other than 1.0 has different effects, depending on whether line antialiasing is enabled.</span></span> <span data-ttu-id="4515c-124">A suavização de linha é controlada chamando [**glEnable**](glenable.md) e **glDisable** com a linha de argumento GL \_ \_ suave.</span><span class="sxs-lookup"><span data-stu-id="4515c-124">Line antialiasing is controlled by calling [**glEnable**](glenable.md) and **glDisable** with argument GL\_LINE\_SMOOTH.</span></span>

<span data-ttu-id="4515c-125">Se a suavização de linha estiver desabilitada, a largura real será determinada arredondando a largura fornecida para o número inteiro mais próximo.</span><span class="sxs-lookup"><span data-stu-id="4515c-125">If line antialiasing is disabled, the actual width is determined by rounding the supplied width to the nearest integer.</span></span> <span data-ttu-id="4515c-126">(Se o arredondamento resultar no valor 0,0, é como se a largura da linha fosse 1,0) Se \| ?</span><span class="sxs-lookup"><span data-stu-id="4515c-126">(If the rounding results in the value 0.0, it is as if the line width were 1.0) If \| ?</span></span> <span data-ttu-id="4515c-127">x \|  =  \| ?</span><span class="sxs-lookup"><span data-stu-id="4515c-127">x \| = \| ?</span></span> <span data-ttu-id="4515c-128">y \| , *i* pixels são preenchidos em cada coluna que é rasterizada, onde *eu* é o valor arredondado da *largura*.</span><span class="sxs-lookup"><span data-stu-id="4515c-128">y \|, *i* pixels are filled in each column that is rasterized, where *i* is the rounded value of *width*.</span></span> <span data-ttu-id="4515c-129">Caso contrário, os pixels de *i* são preenchidos em cada linha rasterizada.</span><span class="sxs-lookup"><span data-stu-id="4515c-129">Otherwise, *i* pixels are filled in each row that is rasterized.</span></span>

<span data-ttu-id="4515c-130">Se a suavização estiver habilitada, a rasterização de linha produzirá um fragmento para cada quadrado de pixel que Interseccionar a região na parte do retângulo com largura igual à largura da linha atual, comprimento igual ao comprimento real da linha e centralizado no segmento de linha matemática.</span><span class="sxs-lookup"><span data-stu-id="4515c-130">If antialiasing is enabled, line rasterization produces a fragment for each pixel square that intersects the region lying within the rectangle having width equal to the current line width, length equal to the actual length of the line, and centered on the mathematical line segment.</span></span> <span data-ttu-id="4515c-131">O valor de cobertura para cada fragmento é a área de coordenadas da janela da interseção da região retangular com o quadrado de pixel correspondente.</span><span class="sxs-lookup"><span data-stu-id="4515c-131">The coverage value for each fragment is the window coordinate area of the intersection of the rectangular region with the corresponding pixel square.</span></span> <span data-ttu-id="4515c-132">Esse valor é salvo e usado na etapa de rasterização final.</span><span class="sxs-lookup"><span data-stu-id="4515c-132">This value is saved and used in the final rasterization step.</span></span>

<span data-ttu-id="4515c-133">Nem todas as larguras podem ter suporte quando a suavização de linha está habilitada.</span><span class="sxs-lookup"><span data-stu-id="4515c-133">Not all widths can be supported when line antialiasing is enabled.</span></span> <span data-ttu-id="4515c-134">Se uma largura sem suporte for solicitada, a largura com suporte mais próxima será usada.</span><span class="sxs-lookup"><span data-stu-id="4515c-134">If an unsupported width is requested, the nearest supported width is used.</span></span> <span data-ttu-id="4515c-135">Há garantia de suporte apenas para a largura 1,0; outras dependem da implementação.</span><span class="sxs-lookup"><span data-stu-id="4515c-135">Only width 1.0 is guaranteed to be supported; others depend on the implementation.</span></span> <span data-ttu-id="4515c-136">O intervalo de larguras com suporte e a diferença de tamanho entre as larguras com suporte dentro do intervalo pode ser consultado chamando **glGet** com Arguments \_ \_ \_ e \_ granularidade de largura da linha gl \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4515c-136">The range of supported widths and the size difference between supported widths within the range can be queried by calling **glGet** with arguments GL\_LINE\_WIDTH\_RANGE and GL\_LINE\_WIDTH\_GRANULARITY.</span></span>

<span data-ttu-id="4515c-137">A largura da linha especificada por **glLineWidth** sempre é retornada quando a \_ largura da linha gl \_ é consultada.</span><span class="sxs-lookup"><span data-stu-id="4515c-137">The line width specified by **glLineWidth** is always returned when GL\_LINE\_WIDTH is queried.</span></span> <span data-ttu-id="4515c-138">Fixação MSS e arredondamento para linhas com alias e sem alias não têm efeito sobre o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="4515c-138">Clamping and rounding for aliased and antialiased lines have no effect on the specified value.</span></span>

<span data-ttu-id="4515c-139">A largura de linha sem alias pode ser clamped para um máximo dependente de implementação.</span><span class="sxs-lookup"><span data-stu-id="4515c-139">Non-antialiased line width may be clamped to an implementation-dependent maximum.</span></span> <span data-ttu-id="4515c-140">Embora esse máximo não possa ser consultado, ele não deve ser menor que o valor máximo para linhas AntiAlias, arredondado para o valor inteiro mais próximo.</span><span class="sxs-lookup"><span data-stu-id="4515c-140">Although this maximum cannot be queried, it must be no less than the maximum value for antialiased lines, rounded to the nearest integer value.</span></span>

<span data-ttu-id="4515c-141">As funções a seguir recuperam informações relacionadas ao **glLineWidth**:</span><span class="sxs-lookup"><span data-stu-id="4515c-141">The following functions retrieve information related to **glLineWidth**:</span></span>

<span data-ttu-id="4515c-142">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com largura de linha do argumento GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="4515c-142">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LINE\_WIDTH</span></span>

<span data-ttu-id="4515c-143">**glGet** com intervalo de \_ largura de linha do argumento GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="4515c-143">**glGet** with argument GL\_LINE\_WIDTH\_RANGE</span></span>

<span data-ttu-id="4515c-144">**glGet** com granularidade de \_ largura de linha do argumento GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="4515c-144">**glGet** with argument GL\_LINE\_WIDTH\_GRANULARITY</span></span>

<span data-ttu-id="4515c-145">[**glIsEnabled**](glisenabled.md) com linha de argumento GL \_ \_ suave</span><span class="sxs-lookup"><span data-stu-id="4515c-145">[**glIsEnabled**](glisenabled.md) with argument GL\_LINE\_SMOOTH</span></span>

## <a name="requirements"></a><span data-ttu-id="4515c-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4515c-146">Requirements</span></span>



| <span data-ttu-id="4515c-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="4515c-147">Requirement</span></span> | <span data-ttu-id="4515c-148">Valor</span><span class="sxs-lookup"><span data-stu-id="4515c-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4515c-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4515c-149">Minimum supported client</span></span><br/> | <span data-ttu-id="4515c-150">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4515c-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4515c-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4515c-151">Minimum supported server</span></span><br/> | <span data-ttu-id="4515c-152">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4515c-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4515c-153">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4515c-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="4515c-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="4515c-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="4515c-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4515c-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="4515c-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4515c-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4515c-157">DLL</span><span class="sxs-lookup"><span data-stu-id="4515c-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4515c-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4515c-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4515c-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="4515c-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4515c-160">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="4515c-160">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="4515c-161">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="4515c-161">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="4515c-162">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="4515c-162">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="4515c-163">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="4515c-163">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





