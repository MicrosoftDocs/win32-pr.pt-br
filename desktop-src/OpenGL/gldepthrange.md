---
title: função glDepthRange (GL. h)
description: A função glDepthRange especifica o mapeamento de valores z de coordenadas de dispositivo normalizadas para coordenadas de janela.
ms.assetid: 44aed5e5-4bd2-4e7f-ad05-1cf4be5254a5
keywords:
- função glDepthRange OpenGL
topic_type:
- apiref
api_name:
- glDepthRange
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0bd6a22ae91877c9b20fa5387edd9438942a07d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369414"
---
# <a name="gldepthrange-function"></a><span data-ttu-id="73c90-104">função glDepthRange</span><span class="sxs-lookup"><span data-stu-id="73c90-104">glDepthRange function</span></span>

<span data-ttu-id="73c90-105">A função **glDepthRange** especifica o mapeamento de valores *z* de coordenadas de dispositivo normalizadas para coordenadas de janela.</span><span class="sxs-lookup"><span data-stu-id="73c90-105">The **glDepthRange** function specifies the mapping of *z* values from normalized device coordinates to window coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="73c90-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73c90-106">Syntax</span></span>


```C++
void WINAPI glDepthRange(
   GLclampd zNear,
   GLclampd zFar
);
```



## <a name="parameters"></a><span data-ttu-id="73c90-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73c90-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73c90-108">*zNear*</span><span class="sxs-lookup"><span data-stu-id="73c90-108">*zNear*</span></span> 
</dt> <dd>

<span data-ttu-id="73c90-109">O mapeamento do plano de recorte Near para as coordenadas da janela.</span><span class="sxs-lookup"><span data-stu-id="73c90-109">The mapping of the near clipping plane to window coordinates.</span></span> <span data-ttu-id="73c90-110">O valor padrão é zero.</span><span class="sxs-lookup"><span data-stu-id="73c90-110">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="73c90-111">*zFar*</span><span class="sxs-lookup"><span data-stu-id="73c90-111">*zFar*</span></span> 
</dt> <dd>

<span data-ttu-id="73c90-112">O mapeamento do plano de recorte distante para as coordenadas da janela.</span><span class="sxs-lookup"><span data-stu-id="73c90-112">The mapping of the far clipping plane to window coordinates.</span></span> <span data-ttu-id="73c90-113">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="73c90-113">The default value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73c90-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="73c90-114">Return value</span></span>

<span data-ttu-id="73c90-115">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="73c90-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="73c90-116">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="73c90-116">Error codes</span></span>

<span data-ttu-id="73c90-117">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="73c90-117">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="73c90-118">Nome</span><span class="sxs-lookup"><span data-stu-id="73c90-118">Name</span></span>                                                                                                  | <span data-ttu-id="73c90-119">Significado</span><span class="sxs-lookup"><span data-stu-id="73c90-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="73c90-120"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="73c90-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="73c90-121">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="73c90-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="73c90-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="73c90-122">Remarks</span></span>

<span data-ttu-id="73c90-123">Após recorte e divisão por *w*, as coordenadas *z* variam de 0,0 a 1,0, correspondentes aos planos de recorte próximo e longe.</span><span class="sxs-lookup"><span data-stu-id="73c90-123">After clipping and division by *w*, *z* -coordinates range from 0.0 to 1.0, corresponding to the near and far clipping planes.</span></span> <span data-ttu-id="73c90-124">A função **glDepthRange** especifica um mapeamento linear das coordenadas *z* normalizadas neste intervalo para coordenadas *z* de janela.</span><span class="sxs-lookup"><span data-stu-id="73c90-124">The **glDepthRange** function specifies a linear mapping of the normalized *z*-coordinates in this range to window *z*-coordinates.</span></span> <span data-ttu-id="73c90-125">Independentemente da implementação do buffer de profundidade real, os valores de profundidade de janela de coordenadas são tratados como se estivessem de 0,0 a 1,0 (como componentes de cores).</span><span class="sxs-lookup"><span data-stu-id="73c90-125">Regardless of the actual depth buffer implementation, window coordinate depth values are treated as though they range from 0.0 through 1.0 (like color components).</span></span> <span data-ttu-id="73c90-126">Assim, os valores aceitos por **glDepthRange** são clamped para esse intervalo antes de serem aceitos.</span><span class="sxs-lookup"><span data-stu-id="73c90-126">Thus, the values accepted by **glDepthRange** are both clamped to this range before they are accepted.</span></span>

<span data-ttu-id="73c90-127">O mapeamento padrão de (0, 1) mapeia o plano próximo para 0 e o plano distante para 1.</span><span class="sxs-lookup"><span data-stu-id="73c90-127">The default mapping of (0,1) maps the near plane to 0 and the far plane to 1.</span></span> <span data-ttu-id="73c90-128">Com esse mapeamento, o intervalo de buffer de profundidade é totalmente utilizado.</span><span class="sxs-lookup"><span data-stu-id="73c90-128">With this mapping, the depth buffer range is fully utilized.</span></span>

<span data-ttu-id="73c90-129">Não é necessário que *zNear* seja menor que *zFar*.</span><span class="sxs-lookup"><span data-stu-id="73c90-129">It is not necessary that *zNear* be less than *zFar*.</span></span> <span data-ttu-id="73c90-130">Mapeamentos inversos como (1, 0) são aceitáveis.</span><span class="sxs-lookup"><span data-stu-id="73c90-130">Reverse mappings such as (1,0) are acceptable.</span></span>

<span data-ttu-id="73c90-131">A função a seguir recupera informações relacionadas a **glDepthRange**:</span><span class="sxs-lookup"><span data-stu-id="73c90-131">The following function retrieves information related to **glDepthRange**:</span></span>

<span data-ttu-id="73c90-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com intervalo de profundidade do argumento GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="73c90-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_DEPTH\_RANGE</span></span>

## <a name="requirements"></a><span data-ttu-id="73c90-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73c90-133">Requirements</span></span>



| <span data-ttu-id="73c90-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="73c90-134">Requirement</span></span> | <span data-ttu-id="73c90-135">Valor</span><span class="sxs-lookup"><span data-stu-id="73c90-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73c90-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="73c90-136">Minimum supported client</span></span><br/> | <span data-ttu-id="73c90-137">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="73c90-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="73c90-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="73c90-138">Minimum supported server</span></span><br/> | <span data-ttu-id="73c90-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="73c90-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="73c90-140">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="73c90-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="73c90-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="73c90-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="73c90-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="73c90-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="73c90-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73c90-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="73c90-144">DLL</span><span class="sxs-lookup"><span data-stu-id="73c90-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73c90-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73c90-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73c90-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="73c90-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73c90-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="73c90-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="73c90-148">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="73c90-148">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="73c90-149">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="73c90-149">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="73c90-150">**glGet**</span><span class="sxs-lookup"><span data-stu-id="73c90-150">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="73c90-151">**glViewport**</span><span class="sxs-lookup"><span data-stu-id="73c90-151">**glViewport**</span></span>](glviewport.md)
</dt> </dl>

 

 





