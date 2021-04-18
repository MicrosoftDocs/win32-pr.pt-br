---
title: função gluUnProject (Glu. h)
description: A função gluUnProject mapeia as coordenadas de janela para as coordenadas de objeto.
ms.assetid: 6a719fc2-ad40-4b22-9c99-5753f5dbb8a0
keywords:
- função gluUnProject OpenGL
topic_type:
- apiref
api_name:
- gluUnProject
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f45311171dd3d71c9e699953c049e0813f2df361
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761879"
---
# <a name="gluunproject-function"></a><span data-ttu-id="957a4-104">função gluUnProject</span><span class="sxs-lookup"><span data-stu-id="957a4-104">gluUnProject function</span></span>

<span data-ttu-id="957a4-105">A função **gluUnProject** mapeia as coordenadas de janela para as coordenadas de objeto.</span><span class="sxs-lookup"><span data-stu-id="957a4-105">The **gluUnProject** function maps window coordinates to object coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="957a4-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="957a4-106">Syntax</span></span>


```C++
int WINAPI gluUnProject(
         GLdouble winx,
         GLdouble winy,
         GLdouble winz,
   const GLdouble modelMatrix[16],
   const GLdouble projMatrix[16],
   const GLint    viewport[4],
         GLdouble *objx,
         GLdouble *objy,
         GLdouble *objz
);
```



## <a name="parameters"></a><span data-ttu-id="957a4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="957a4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="957a4-108">*winx*</span><span class="sxs-lookup"><span data-stu-id="957a4-108">*winx*</span></span> 
</dt> <dd>

<span data-ttu-id="957a4-109">A coordenada x da janela a ser mapeada.</span><span class="sxs-lookup"><span data-stu-id="957a4-109">The x window coordinate to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="957a4-110">*winy*</span><span class="sxs-lookup"><span data-stu-id="957a4-110">*winy*</span></span> 
</dt> <dd>

<span data-ttu-id="957a4-111">A coordenada da janela y a ser mapeada.</span><span class="sxs-lookup"><span data-stu-id="957a4-111">The y window coordinate to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="957a4-112">*winz*</span><span class="sxs-lookup"><span data-stu-id="957a4-112">*winz*</span></span> 
</dt> <dd>

<span data-ttu-id="957a4-113">A coordenada da janela z a ser mapeada.</span><span class="sxs-lookup"><span data-stu-id="957a4-113">The z window coordinate to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="957a4-114">*modelMatrix*</span><span class="sxs-lookup"><span data-stu-id="957a4-114">*modelMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="957a4-115">A matriz modelview (como de uma chamada [**glGetDoublev**](glgetdoublev.md) ).</span><span class="sxs-lookup"><span data-stu-id="957a4-115">The modelview matrix (as from a [**glGetDoublev**](glgetdoublev.md) call).</span></span>

</dd> <dt>

<span data-ttu-id="957a4-116">*projMatrix*</span><span class="sxs-lookup"><span data-stu-id="957a4-116">*projMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="957a4-117">A matriz de projeção (como a partir de uma chamada **glGetDoublev** ).</span><span class="sxs-lookup"><span data-stu-id="957a4-117">The projection matrix (as from a **glGetDoublev** call).</span></span>

</dd> <dt>

<span data-ttu-id="957a4-118">*visor*</span><span class="sxs-lookup"><span data-stu-id="957a4-118">*viewport*</span></span> 
</dt> <dd>

<span data-ttu-id="957a4-119">O visor (como de uma chamada [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ).</span><span class="sxs-lookup"><span data-stu-id="957a4-119">The viewport (as from a [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) call).</span></span>

</dd> <dt>

<span data-ttu-id="957a4-120">*objx*</span><span class="sxs-lookup"><span data-stu-id="957a4-120">*objx*</span></span> 
</dt> <dd>

<span data-ttu-id="957a4-121">A coordenada de objeto x computada.</span><span class="sxs-lookup"><span data-stu-id="957a4-121">The computed x object coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="957a4-122">*objy*</span><span class="sxs-lookup"><span data-stu-id="957a4-122">*objy*</span></span> 
</dt> <dd>

<span data-ttu-id="957a4-123">A coordenada de objeto y computada.</span><span class="sxs-lookup"><span data-stu-id="957a4-123">The computed y object coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="957a4-124">*objz*</span><span class="sxs-lookup"><span data-stu-id="957a4-124">*objz*</span></span> 
</dt> <dd>

<span data-ttu-id="957a4-125">A coordenada de objeto z computada.</span><span class="sxs-lookup"><span data-stu-id="957a4-125">The computed z object coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="957a4-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="957a4-126">Return value</span></span>

<span data-ttu-id="957a4-127">Se a função for realizada com sucesso, o valor de retorno será GL \_ verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="957a4-127">If the function succeeds, the return value is GL\_TRUE.</span></span>

<span data-ttu-id="957a4-128">Se a função falhar, o valor de retorno será GL \_ false.</span><span class="sxs-lookup"><span data-stu-id="957a4-128">If the function fails, the return value is GL\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="957a4-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="957a4-129">Remarks</span></span>

<span data-ttu-id="957a4-130">A função **gluUnProject** mapeia as coordenadas de janela especificadas em coordenadas de objeto usando *modelMatrix*, *projMatrix* e *viewport*.</span><span class="sxs-lookup"><span data-stu-id="957a4-130">The **gluUnProject** function maps the specified window coordinates into object coordinates using *modelMatrix*, *projMatrix*, and *viewport*.</span></span> <span data-ttu-id="957a4-131">O resultado é armazenado em *objx*, *objy* e *objz*.</span><span class="sxs-lookup"><span data-stu-id="957a4-131">The result is stored in *objx*, *objy*, and *objz*.</span></span>

## <a name="requirements"></a><span data-ttu-id="957a4-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="957a4-132">Requirements</span></span>



| <span data-ttu-id="957a4-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="957a4-133">Requirement</span></span> | <span data-ttu-id="957a4-134">Valor</span><span class="sxs-lookup"><span data-stu-id="957a4-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="957a4-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="957a4-135">Minimum supported client</span></span><br/> | <span data-ttu-id="957a4-136">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="957a4-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="957a4-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="957a4-137">Minimum supported server</span></span><br/> | <span data-ttu-id="957a4-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="957a4-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="957a4-139">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="957a4-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="957a4-140"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="957a4-140"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="957a4-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="957a4-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="957a4-142"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="957a4-142"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="957a4-143">DLL</span><span class="sxs-lookup"><span data-stu-id="957a4-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="957a4-144"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="957a4-144"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="957a4-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="957a4-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="957a4-146">**glGet**</span><span class="sxs-lookup"><span data-stu-id="957a4-146">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="957a4-147">**glGetDoublev**</span><span class="sxs-lookup"><span data-stu-id="957a4-147">**glGetDoublev**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="957a4-148">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="957a4-148">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="957a4-149">**gluProject**</span><span class="sxs-lookup"><span data-stu-id="957a4-149">**gluProject**</span></span>](gluproject.md)
</dt> </dl>

 

 





