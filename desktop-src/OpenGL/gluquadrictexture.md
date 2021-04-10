---
title: função gluQuadricTexture (Glu. h)
description: A função gluQuadricTexture especifica se quadrics deve ser texturizado.
ms.assetid: 11681497-f099-4856-a0ac-6a44abd3e1a1
keywords:
- função gluQuadricTexture OpenGL
topic_type:
- apiref
api_name:
- gluQuadricTexture
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cc395564b6c6f30f38a8c5129c489d0bfca6b80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085972"
---
# <a name="gluquadrictexture-function"></a><span data-ttu-id="d578c-104">função gluQuadricTexture</span><span class="sxs-lookup"><span data-stu-id="d578c-104">gluQuadricTexture function</span></span>

<span data-ttu-id="d578c-105">A função **gluQuadricTexture** especifica se quadrics deve ser texturizado.</span><span class="sxs-lookup"><span data-stu-id="d578c-105">The **gluQuadricTexture** function specifies whether quadrics are to be textured.</span></span>

## <a name="syntax"></a><span data-ttu-id="d578c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d578c-106">Syntax</span></span>


```C++
void WINAPI gluQuadricTexture(
   GLUquadric *quadObject,
   GLboolean  textureCoords
);
```



## <a name="parameters"></a><span data-ttu-id="d578c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d578c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d578c-108">*quádruplo*</span><span class="sxs-lookup"><span data-stu-id="d578c-108">*quadObject*</span></span> 
</dt> <dd>

<span data-ttu-id="d578c-109">O objeto Quadric (criado com [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="d578c-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="d578c-110">*textureCoords*</span><span class="sxs-lookup"><span data-stu-id="d578c-110">*textureCoords*</span></span> 
</dt> <dd>

<span data-ttu-id="d578c-111">Um sinalizador que indica se as coordenadas de textura devem ser geradas.</span><span class="sxs-lookup"><span data-stu-id="d578c-111">A flag indicating whether texture coordinates are to be generated.</span></span> <span data-ttu-id="d578c-112">Os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="d578c-112">The following values are valid.</span></span>



| <span data-ttu-id="d578c-113">Valor</span><span class="sxs-lookup"><span data-stu-id="d578c-113">Value</span></span>                                                                                                                                          | <span data-ttu-id="d578c-114">Significado</span><span class="sxs-lookup"><span data-stu-id="d578c-114">Meaning</span></span>                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="GL_TRUE"></span><span id="gl_true"></span><dl> <span data-ttu-id="d578c-115"><dt>**GL \_ verdadeiro**</dt></span><span class="sxs-lookup"><span data-stu-id="d578c-115"><dt>**GL\_TRUE**</dt></span></span> </dl>    | <span data-ttu-id="d578c-116">Gerar coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="d578c-116">Generate texture coordinates.</span></span><br/>                                   |
| <span id="GL_FALSE"></span><span id="gl_false"></span><dl> <span data-ttu-id="d578c-117"><dt>**GL \_ falso**</dt></span><span class="sxs-lookup"><span data-stu-id="d578c-117"><dt>**GL\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="d578c-118">Não gere coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="d578c-118">Do not generate texture coordinates.</span></span> <span data-ttu-id="d578c-119">Esse é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="d578c-119">This is the default value.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d578c-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d578c-120">Return value</span></span>

<span data-ttu-id="d578c-121">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d578c-121">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d578c-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="d578c-122">Remarks</span></span>

<span data-ttu-id="d578c-123">A função **gluQuadricTexture** especifica se as coordenadas de textura devem ser geradas para quadrics renderizado com o **quadobject**.</span><span class="sxs-lookup"><span data-stu-id="d578c-123">The **gluQuadricTexture** function specifies whether texture coordinates are to be generated for quadrics rendered with **quadObject**.</span></span>

<span data-ttu-id="d578c-124">A maneira como as coordenadas de textura são geradas depende do Quadric específico renderizado.</span><span class="sxs-lookup"><span data-stu-id="d578c-124">The manner in which texture coordinates are generated depends upon the specific quadric rendered.</span></span>

## <a name="requirements"></a><span data-ttu-id="d578c-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d578c-125">Requirements</span></span>



| <span data-ttu-id="d578c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d578c-126">Requirement</span></span> | <span data-ttu-id="d578c-127">Valor</span><span class="sxs-lookup"><span data-stu-id="d578c-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d578c-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d578c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d578c-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d578c-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d578c-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d578c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d578c-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d578c-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d578c-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d578c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d578c-133"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="d578c-133"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="d578c-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d578c-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="d578c-135"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d578c-135"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d578c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d578c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d578c-137"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d578c-137"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d578c-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="d578c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d578c-139">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="d578c-139">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="d578c-140">**gluQuadricDrawStyle**</span><span class="sxs-lookup"><span data-stu-id="d578c-140">**gluQuadricDrawStyle**</span></span>](gluquadricdrawstyle.md)
</dt> <dt>

[<span data-ttu-id="d578c-141">**gluQuadricNormals**</span><span class="sxs-lookup"><span data-stu-id="d578c-141">**gluQuadricNormals**</span></span>](gluquadricnormals.md)
</dt> </dl>

 

 





