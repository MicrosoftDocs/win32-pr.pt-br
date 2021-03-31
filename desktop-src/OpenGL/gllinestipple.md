---
title: função glLineStipple (GL. h)
description: A função glLineStipple especifica o padrão de linha Stipple.
ms.assetid: 256d968c-9e72-4aec-9faf-afe70f1087a8
keywords:
- função glLineStipple OpenGL
topic_type:
- apiref
api_name:
- glLineStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b47202b25c0779a3daa0bd801900b1d29e0b37b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644224"
---
# <a name="gllinestipple-function"></a><span data-ttu-id="24699-104">função glLineStipple</span><span class="sxs-lookup"><span data-stu-id="24699-104">glLineStipple function</span></span>

<span data-ttu-id="24699-105">A função **glLineStipple** especifica o padrão de linha Stipple.</span><span class="sxs-lookup"><span data-stu-id="24699-105">The **glLineStipple** function specifies the line stipple pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="24699-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="24699-106">Syntax</span></span>


```C++
void WINAPI glLineStipple(
   GLint    factor,
   GLushort pattern
);
```



## <a name="parameters"></a><span data-ttu-id="24699-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24699-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24699-108">*multi-fator*</span><span class="sxs-lookup"><span data-stu-id="24699-108">*factor*</span></span> 
</dt> <dd>

<span data-ttu-id="24699-109">Um multiplicador para cada bit no padrão de linha Stipple.</span><span class="sxs-lookup"><span data-stu-id="24699-109">A multiplier for each bit in the line stipple pattern.</span></span> <span data-ttu-id="24699-110">Se o *fator* for 3, por exemplo, cada bit no padrão será usado três vezes antes de o próximo bit no padrão ser usado.</span><span class="sxs-lookup"><span data-stu-id="24699-110">If *factor* is 3, for example, each bit in the pattern will be used three times before the next bit in the pattern is used.</span></span> <span data-ttu-id="24699-111">O parâmetro *factor* é clamped para o intervalo de \[ 1, 256 \] e, por padrão, é um.</span><span class="sxs-lookup"><span data-stu-id="24699-111">The *factor* parameter is clamped to the range \[1, 256\] and defaults to one.</span></span>

</dd> <dt>

<span data-ttu-id="24699-112">*padrão*</span><span class="sxs-lookup"><span data-stu-id="24699-112">*pattern*</span></span> 
</dt> <dd>

<span data-ttu-id="24699-113">Um inteiro de 16 bits cujo padrão de bit determina quais fragmentos de uma linha serão desenhados quando a linha for rasterizada.</span><span class="sxs-lookup"><span data-stu-id="24699-113">A 16-bit integer whose bit pattern determines which fragments of a line will be drawn when the line is rasterized.</span></span> <span data-ttu-id="24699-114">O bit zero é usado primeiro e o padrão padrão é todos.</span><span class="sxs-lookup"><span data-stu-id="24699-114">Bit zero is used first, and the default pattern is all ones.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24699-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="24699-115">Return value</span></span>

<span data-ttu-id="24699-116">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="24699-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="24699-117">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="24699-117">Error codes</span></span>

<span data-ttu-id="24699-118">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="24699-118">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="24699-119">Name</span><span class="sxs-lookup"><span data-stu-id="24699-119">Name</span></span>                                                                                                  | <span data-ttu-id="24699-120">Significado</span><span class="sxs-lookup"><span data-stu-id="24699-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="24699-121"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="24699-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="24699-122">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="24699-122">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="24699-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="24699-123">Remarks</span></span>

<span data-ttu-id="24699-124">A função **glLineStipple** especifica o padrão de linha Stipple.</span><span class="sxs-lookup"><span data-stu-id="24699-124">The **glLineStipple** function specifies the line stipple pattern.</span></span> <span data-ttu-id="24699-125">A linha stippling mascara alguns fragmentos produzidos pela rasterização; esses fragmentos não serão desenhados.</span><span class="sxs-lookup"><span data-stu-id="24699-125">Line stippling masks out certain fragments produced by rasterization; those fragments will not be drawn.</span></span> <span data-ttu-id="24699-126">O mascaramento é obtido usando três parâmetros: o *padrão* de Stipple de linha de 16 bits, o *fator* de contagem de repetição e um número inteiro de Stipple contador *s*.</span><span class="sxs-lookup"><span data-stu-id="24699-126">The masking is achieved by using three parameters: the 16-bit line stipple pattern *pattern*, the repeat count *factor*, and an integer stipple counter *s*.</span></span>

<span data-ttu-id="24699-127">O contador *s* é redefinido para zero sempre que [**glBegin**](glbegin.md) é chamado e antes de cada segmento de linha de uma sequência de **glBegin**( \_ linhas GL)/**glEnd** ser gerada.</span><span class="sxs-lookup"><span data-stu-id="24699-127">Counter *s* is reset to zero whenever [**glBegin**](glbegin.md) is called, and before each line segment of a **glBegin**(GL\_LINES)/**glEnd** sequence is generated.</span></span> <span data-ttu-id="24699-128">Ele é incrementado após a geração *de cada fragmento* de um segmento de linha com alias de largura de unidade, ou após cada um dos fragmentos de um segmento de linha *de largura,* são gerados.</span><span class="sxs-lookup"><span data-stu-id="24699-128">It is incremented after each fragment of a unit width aliased line segment is generated, or after each *i* fragments of an *i* width line segment are generated.</span></span> <span data-ttu-id="24699-129">Os fragmentos de *i* associados à contagem *s* são mascarados se o bit (*s* factor) do *padrão*  /  mod 16 for zero.</span><span class="sxs-lookup"><span data-stu-id="24699-129">The *i* fragments associated with count *s* are masked out if *pattern* bit (*s* / *factor*) mod 16 is zero.</span></span> <span data-ttu-id="24699-130">Caso contrário, esses fragmentos serão enviados para o framebuffer.</span><span class="sxs-lookup"><span data-stu-id="24699-130">Otherwise these fragments are sent to the framebuffer.</span></span> <span data-ttu-id="24699-131">O bit zero do *padrão* é o bit menos significativo.</span><span class="sxs-lookup"><span data-stu-id="24699-131">Bit zero of *pattern* is the least significant bit.</span></span>

<span data-ttu-id="24699-132">Linhas AntiAlias são tratadas como uma sequência de retângulos de *largura* 1x para fins de stippling.</span><span class="sxs-lookup"><span data-stu-id="24699-132">Antialiased lines are treated as a sequence of 1x *width* rectangles for purposes of stippling.</span></span> <span data-ttu-id="24699-133">Os *s* de retângulo são rasterizados ou não com base na regra de fragmento descrita para linhas com alias; Ele conta retângulos em vez de grupos de fragmentos.</span><span class="sxs-lookup"><span data-stu-id="24699-133">Rectangle *s* is rasterized or not based on the fragment rule described for aliased lines; it counts rectangles rather than groups of fragments.</span></span>

<span data-ttu-id="24699-134">A linha stippling é habilitada ou desabilitada usando [**glEnable**](glenable.md) e **glDisable** com a linha de argumento GL \_ \_ STIPPLE.</span><span class="sxs-lookup"><span data-stu-id="24699-134">Line stippling is enabled or disabled using [**glEnable**](glenable.md) and **glDisable** with argument GL\_LINE\_STIPPLE.</span></span> <span data-ttu-id="24699-135">Quando habilitado, o padrão de linha Stipple é aplicado conforme descrito acima.</span><span class="sxs-lookup"><span data-stu-id="24699-135">When enabled, the line stipple pattern is applied as described above.</span></span> <span data-ttu-id="24699-136">Quando desabilitado, é como se o padrão fosse todos.</span><span class="sxs-lookup"><span data-stu-id="24699-136">When disabled, it is as if the pattern were all ones.</span></span> <span data-ttu-id="24699-137">Inicialmente, a linha stippling está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="24699-137">Initially, line stippling is disabled.</span></span>

<span data-ttu-id="24699-138">As funções a seguir recuperam informações relacionadas ao **glLineStipple**:</span><span class="sxs-lookup"><span data-stu-id="24699-138">The following functions retrieve information related to **glLineStipple**:</span></span>

<span data-ttu-id="24699-139">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com \_ \_ STIPPLE padrão de linha de argumento GL \_</span><span class="sxs-lookup"><span data-stu-id="24699-139">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LINE\_STIPPLE\_PATTERN</span></span>

<span data-ttu-id="24699-140">**glGet** com Argument GL \_ linha \_ STIPPLE \_ REPEAT</span><span class="sxs-lookup"><span data-stu-id="24699-140">**glGet** with argument GL\_LINE\_STIPPLE\_REPEAT</span></span>

<span data-ttu-id="24699-141">[**glIsEnabled**](glisenabled.md) com o argumento GL \_ linha \_ STIPPLE</span><span class="sxs-lookup"><span data-stu-id="24699-141">[**glIsEnabled**](glisenabled.md) with argument GL\_LINE\_STIPPLE</span></span>

## <a name="requirements"></a><span data-ttu-id="24699-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24699-142">Requirements</span></span>



| <span data-ttu-id="24699-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="24699-143">Requirement</span></span> | <span data-ttu-id="24699-144">Valor</span><span class="sxs-lookup"><span data-stu-id="24699-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24699-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24699-145">Minimum supported client</span></span><br/> | <span data-ttu-id="24699-146">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="24699-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="24699-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24699-147">Minimum supported server</span></span><br/> | <span data-ttu-id="24699-148">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="24699-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="24699-149">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="24699-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="24699-150"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="24699-150"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="24699-151">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="24699-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="24699-152"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="24699-152"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="24699-153">DLL</span><span class="sxs-lookup"><span data-stu-id="24699-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24699-154"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24699-154"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24699-155">Consulte também</span><span class="sxs-lookup"><span data-stu-id="24699-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24699-156">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="24699-156">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="24699-157">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="24699-157">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="24699-158">**glLineWidth**</span><span class="sxs-lookup"><span data-stu-id="24699-158">**glLineWidth**</span></span>](gllinewidth.md)
</dt> <dt>

[<span data-ttu-id="24699-159">**glPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="24699-159">**glPolygonStipple**</span></span>](glpolygonstipple.md)
</dt> </dl>

 

 





