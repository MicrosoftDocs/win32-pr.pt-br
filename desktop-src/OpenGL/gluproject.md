---
title: função gluProject (Glu. h)
description: A função gluProject mapeia coordenadas de objeto para coordenadas de janela.
ms.assetid: cfd8bc5b-b684-4207-8bdb-bf086858da13
keywords:
- função gluProject OpenGL
topic_type:
- apiref
api_name:
- gluProject
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84972d95d381a630bf6caf7f0099ce740a4f2741
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455582"
---
# <a name="gluproject-function"></a><span data-ttu-id="6736c-104">função gluProject</span><span class="sxs-lookup"><span data-stu-id="6736c-104">gluProject function</span></span>

<span data-ttu-id="6736c-105">A função **gluProject** mapeia coordenadas de objeto para coordenadas de janela.</span><span class="sxs-lookup"><span data-stu-id="6736c-105">The **gluProject** function maps object coordinates to window coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="6736c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6736c-106">Syntax</span></span>


```C++
int WINAPI gluProject(
         GLdouble objx,
         GLdouble objy,
         GLdouble objz,
   const GLdouble modelMatrix[16],
   const GLdouble projMatrix[16],
   const GLint    viewport[4],
         GLdouble *winx,
         GLdouble *winy,
         GLdouble *winz
);
```



## <a name="parameters"></a><span data-ttu-id="6736c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6736c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6736c-108">*objx*</span><span class="sxs-lookup"><span data-stu-id="6736c-108">*objx*</span></span> 
</dt> <dd>

<span data-ttu-id="6736c-109">A coordenada x objeto.</span><span class="sxs-lookup"><span data-stu-id="6736c-109">The x object coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="6736c-110">*objy*</span><span class="sxs-lookup"><span data-stu-id="6736c-110">*objy*</span></span> 
</dt> <dd>

<span data-ttu-id="6736c-111">A coordenada do objeto y.</span><span class="sxs-lookup"><span data-stu-id="6736c-111">The y object coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="6736c-112">*objz*</span><span class="sxs-lookup"><span data-stu-id="6736c-112">*objz*</span></span> 
</dt> <dd>

<span data-ttu-id="6736c-113">A coordenada de objeto z.</span><span class="sxs-lookup"><span data-stu-id="6736c-113">The z object coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="6736c-114">*modelMatrix*</span><span class="sxs-lookup"><span data-stu-id="6736c-114">*modelMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="6736c-115">A matriz modelview atual (como a partir de uma chamada [**glGetDoublev**](glgetdoublev.md) ).</span><span class="sxs-lookup"><span data-stu-id="6736c-115">The current modelview matrix (as from a [**glGetDoublev**](glgetdoublev.md) call).</span></span>

</dd> <dt>

<span data-ttu-id="6736c-116">*projMatrix*</span><span class="sxs-lookup"><span data-stu-id="6736c-116">*projMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="6736c-117">A matriz de projeção atual (como a partir de uma chamada **glGetDoublev** ).</span><span class="sxs-lookup"><span data-stu-id="6736c-117">The current projection matrix (as from a **glGetDoublev** call).</span></span>

</dd> <dt>

<span data-ttu-id="6736c-118">*visor*</span><span class="sxs-lookup"><span data-stu-id="6736c-118">*viewport*</span></span> 
</dt> <dd>

<span data-ttu-id="6736c-119">O visor atual (como de uma chamada [**glGetIntegerv**](glgetintegerv.md) ).</span><span class="sxs-lookup"><span data-stu-id="6736c-119">The current viewport (as from a [**glGetIntegerv**](glgetintegerv.md) call).</span></span>

</dd> <dt>

<span data-ttu-id="6736c-120">*winx*</span><span class="sxs-lookup"><span data-stu-id="6736c-120">*winx*</span></span> 
</dt> <dd>

<span data-ttu-id="6736c-121">A coordenada da janela x computada.</span><span class="sxs-lookup"><span data-stu-id="6736c-121">The computed x window coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="6736c-122">*winy*</span><span class="sxs-lookup"><span data-stu-id="6736c-122">*winy*</span></span> 
</dt> <dd>

<span data-ttu-id="6736c-123">A coordenada da janela y computada.</span><span class="sxs-lookup"><span data-stu-id="6736c-123">The computed y window coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="6736c-124">*winz*</span><span class="sxs-lookup"><span data-stu-id="6736c-124">*winz*</span></span> 
</dt> <dd>

<span data-ttu-id="6736c-125">A coordenada de janela z computada.</span><span class="sxs-lookup"><span data-stu-id="6736c-125">The computed z window coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6736c-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6736c-126">Return value</span></span>

<span data-ttu-id="6736c-127">Se a função for realizada com sucesso, o valor de retorno será GL \_ verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="6736c-127">If the function succeeds, the return value is GL\_TRUE.</span></span>

<span data-ttu-id="6736c-128">Se a função falhar, o valor de retorno será GL \_ false.</span><span class="sxs-lookup"><span data-stu-id="6736c-128">If the function fails, the return value is GL\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="6736c-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="6736c-129">Remarks</span></span>

<span data-ttu-id="6736c-130">A função **gluProject** transforma as coordenadas do objeto especificado em coordenadas de janela usando *modelMatrix*, *projMatrix* e *viewport*.</span><span class="sxs-lookup"><span data-stu-id="6736c-130">The **gluProject** function transforms the specified object coordinates into window coordinates using *modelMatrix*, *projMatrix*, and *viewport*.</span></span> <span data-ttu-id="6736c-131">O resultado é armazenado em *Winx*, *winy* e *WINZ*.</span><span class="sxs-lookup"><span data-stu-id="6736c-131">The result is stored in *winx*, *winy*, and *winz*.</span></span>

## <a name="requirements"></a><span data-ttu-id="6736c-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6736c-132">Requirements</span></span>



| <span data-ttu-id="6736c-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="6736c-133">Requirement</span></span> | <span data-ttu-id="6736c-134">Valor</span><span class="sxs-lookup"><span data-stu-id="6736c-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6736c-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6736c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="6736c-136">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6736c-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="6736c-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6736c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="6736c-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6736c-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6736c-139">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6736c-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="6736c-140"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="6736c-140"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="6736c-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6736c-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="6736c-142"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6736c-142"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6736c-143">DLL</span><span class="sxs-lookup"><span data-stu-id="6736c-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6736c-144"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6736c-144"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6736c-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="6736c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6736c-146">**glGetDoublev**</span><span class="sxs-lookup"><span data-stu-id="6736c-146">**glGetDoublev**</span></span>](glgetdoublev.md)
</dt> <dt>

[<span data-ttu-id="6736c-147">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="6736c-147">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="6736c-148">**gluUnProject**</span><span class="sxs-lookup"><span data-stu-id="6736c-148">**gluUnProject**</span></span>](gluunproject.md)
</dt> </dl>

 

 





