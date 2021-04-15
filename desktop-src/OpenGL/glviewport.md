---
title: função glViewport (GL. h)
description: A função glViewport define o visor.
ms.assetid: 11816b2f-ee18-42ef-a782-2e96699dd087
keywords:
- função glViewport OpenGL
topic_type:
- apiref
api_name:
- glViewport
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5e8eedb9c66211deda92ef6a84e8c1dd2073362
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104570400"
---
# <a name="glviewport-function"></a><span data-ttu-id="acd2a-104">função glViewport</span><span class="sxs-lookup"><span data-stu-id="acd2a-104">glViewport function</span></span>

<span data-ttu-id="acd2a-105">A função **glViewport** define o visor.</span><span class="sxs-lookup"><span data-stu-id="acd2a-105">The **glViewport** function sets the viewport.</span></span>

## <a name="syntax"></a><span data-ttu-id="acd2a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="acd2a-106">Syntax</span></span>


```C++
void WINAPI glViewport(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a><span data-ttu-id="acd2a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="acd2a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acd2a-108">*x*</span><span class="sxs-lookup"><span data-stu-id="acd2a-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="acd2a-109">O canto inferior esquerdo do retângulo do visor, em pixels.</span><span class="sxs-lookup"><span data-stu-id="acd2a-109">The lower-left corner of the viewport rectangle, in pixels.</span></span> <span data-ttu-id="acd2a-110">O padrão é (0, 0).</span><span class="sxs-lookup"><span data-stu-id="acd2a-110">The default is (0,0).</span></span>

</dd> <dt>

<span data-ttu-id="acd2a-111">*y*</span><span class="sxs-lookup"><span data-stu-id="acd2a-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="acd2a-112">O canto inferior esquerdo do retângulo do visor, em pixels.</span><span class="sxs-lookup"><span data-stu-id="acd2a-112">The lower-left corner of the viewport rectangle, in pixels.</span></span> <span data-ttu-id="acd2a-113">O padrão é (0, 0).</span><span class="sxs-lookup"><span data-stu-id="acd2a-113">The default is (0,0).</span></span>

</dd> <dt>

<span data-ttu-id="acd2a-114">*width*</span><span class="sxs-lookup"><span data-stu-id="acd2a-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="acd2a-115">A largura do visor.</span><span class="sxs-lookup"><span data-stu-id="acd2a-115">The width of the viewport.</span></span> <span data-ttu-id="acd2a-116">Quando um contexto OpenGL é anexado pela primeira vez a uma janela, a *largura* e a *altura* são definidas para as dimensões dessa janela.</span><span class="sxs-lookup"><span data-stu-id="acd2a-116">When an OpenGL context is first attached to a window, *width* and *height* are set to the dimensions of that window.</span></span>

</dd> <dt>

<span data-ttu-id="acd2a-117">*altura*</span><span class="sxs-lookup"><span data-stu-id="acd2a-117">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="acd2a-118">A altura do visor.</span><span class="sxs-lookup"><span data-stu-id="acd2a-118">The height of the viewport.</span></span> <span data-ttu-id="acd2a-119">Quando um contexto OpenGL é anexado pela primeira vez a uma janela, a *largura* e a *altura* são definidas para as dimensões dessa janela.</span><span class="sxs-lookup"><span data-stu-id="acd2a-119">When an OpenGL context is first attached to a window, *width* and *height* are set to the dimensions of that window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acd2a-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="acd2a-120">Return value</span></span>

<span data-ttu-id="acd2a-121">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="acd2a-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="acd2a-122">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="acd2a-122">Error codes</span></span>

<span data-ttu-id="acd2a-123">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="acd2a-123">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="acd2a-124">Nome</span><span class="sxs-lookup"><span data-stu-id="acd2a-124">Name</span></span>                                                                                                  | <span data-ttu-id="acd2a-125">Significado</span><span class="sxs-lookup"><span data-stu-id="acd2a-125">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="acd2a-126"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="acd2a-126"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="acd2a-127">A *largura* ou a *altura* era negativa.</span><span class="sxs-lookup"><span data-stu-id="acd2a-127">Either *width* or *height* was negative.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="acd2a-128"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="acd2a-128"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="acd2a-129">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="acd2a-129">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="acd2a-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="acd2a-130">Remarks</span></span>

<span data-ttu-id="acd2a-131">A função **glViewport** especifica a transformação afim de *x* e *y* de coordenadas de dispositivo normalizadas para coordenadas de janela.</span><span class="sxs-lookup"><span data-stu-id="acd2a-131">The **glViewport** function specifies the affine transformation of *x* and *y* from normalized device coordinates to window coordinates.</span></span> <span data-ttu-id="acd2a-132">Deixe que (*x*<sub>ND</sub> , *y*<sub>ND</sub> ) sejam coordenadas de dispositivo normalizadas.</span><span class="sxs-lookup"><span data-stu-id="acd2a-132">Let (*x*<sub>nd</sub> , *y*<sub>nd</sub> ) be normalized device coordinates.</span></span> <span data-ttu-id="acd2a-133">As coordenadas da janela (*x*<sub>w</sub> , *y*<sub>w</sub> ) são computadas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="acd2a-133">The window coordinates (*x*<sub>w</sub> , *y*<sub>w</sub> ) are then computed as follows:</span></span>

![Equação mostrando a computação das coordenadas da janela.](images/view01.png)

<span data-ttu-id="acd2a-135">A largura e a altura do visor são silenciosamente clamped a um intervalo que depende da implementação.</span><span class="sxs-lookup"><span data-stu-id="acd2a-135">Viewport width and height are silently clamped to a range that depends on the implementation.</span></span> <span data-ttu-id="acd2a-136">Esse intervalo é consultado chamando **glGet** com o argumento GL \_ Max \_ viewport \_ esmaece.</span><span class="sxs-lookup"><span data-stu-id="acd2a-136">This range is queried by calling **glGet** with argument GL\_MAX\_VIEWPORT\_DIMS.</span></span>

<span data-ttu-id="acd2a-137">As funções a seguir recuperam informações relacionadas ao **glViewport**:</span><span class="sxs-lookup"><span data-stu-id="acd2a-137">The following functions retrieve information related to **glViewport**:</span></span>

<span data-ttu-id="acd2a-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com visor do Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="acd2a-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_VIEWPORT</span></span>

<span data-ttu-id="acd2a-139">**glGet** com Argument GL \_ Max \_ viewport \_ escurece</span><span class="sxs-lookup"><span data-stu-id="acd2a-139">**glGet** with argument GL\_MAX\_VIEWPORT\_DIMS</span></span>

## <a name="requirements"></a><span data-ttu-id="acd2a-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="acd2a-140">Requirements</span></span>



| <span data-ttu-id="acd2a-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="acd2a-141">Requirement</span></span> | <span data-ttu-id="acd2a-142">Valor</span><span class="sxs-lookup"><span data-stu-id="acd2a-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="acd2a-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="acd2a-143">Minimum supported client</span></span><br/> | <span data-ttu-id="acd2a-144">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="acd2a-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="acd2a-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="acd2a-145">Minimum supported server</span></span><br/> | <span data-ttu-id="acd2a-146">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="acd2a-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="acd2a-147">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="acd2a-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="acd2a-148"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="acd2a-148"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="acd2a-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="acd2a-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="acd2a-150"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="acd2a-150"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="acd2a-151">DLL</span><span class="sxs-lookup"><span data-stu-id="acd2a-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="acd2a-152"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="acd2a-152"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acd2a-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="acd2a-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acd2a-154">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="acd2a-154">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="acd2a-155">**glDepthRange**</span><span class="sxs-lookup"><span data-stu-id="acd2a-155">**glDepthRange**</span></span>](gldepthrange.md)
</dt> </dl>

 

 





