---
title: função gluQuadricNormals (Glu. h)
description: A função gluQuadricNormals especifica que tipo de Normals deve ser usado para quadrics.
ms.assetid: 945759ec-ed4a-480f-8243-49fc785867c1
keywords:
- função gluQuadricNormals OpenGL
topic_type:
- apiref
api_name:
- gluQuadricNormals
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f11f9d8cd1884d7a5d1bc4cd03797517ba484126
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455580"
---
# <a name="gluquadricnormals-function"></a><span data-ttu-id="010b0-104">função gluQuadricNormals</span><span class="sxs-lookup"><span data-stu-id="010b0-104">gluQuadricNormals function</span></span>

<span data-ttu-id="010b0-105">A função **gluQuadricNormals** especifica que tipo de Normals deve ser usado para quadrics.</span><span class="sxs-lookup"><span data-stu-id="010b0-105">The **gluQuadricNormals** function specifies what kind of normals are to be used for quadrics.</span></span>

## <a name="syntax"></a><span data-ttu-id="010b0-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="010b0-106">Syntax</span></span>


```C++
void WINAPI gluQuadricNormals(
   GLUquadric *quadObject,
   GLenum     normals
);
```



## <a name="parameters"></a><span data-ttu-id="010b0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="010b0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="010b0-108">*quádruplo*</span><span class="sxs-lookup"><span data-stu-id="010b0-108">*quadObject*</span></span> 
</dt> <dd>

<span data-ttu-id="010b0-109">O objeto Quadric (criado com [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="010b0-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="010b0-110">*Normals*</span><span class="sxs-lookup"><span data-stu-id="010b0-110">*normals*</span></span> 
</dt> <dd>

<span data-ttu-id="010b0-111">O tipo desejado de Normals.</span><span class="sxs-lookup"><span data-stu-id="010b0-111">The desired type of normals.</span></span> <span data-ttu-id="010b0-112">Os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="010b0-112">The following values are valid.</span></span>



| <span data-ttu-id="010b0-113">Valor</span><span class="sxs-lookup"><span data-stu-id="010b0-113">Value</span></span>                                                                                                                                                | <span data-ttu-id="010b0-114">Significado</span><span class="sxs-lookup"><span data-stu-id="010b0-114">Meaning</span></span>                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="GLU_NONE"></span><span id="glu_none"></span><dl> <span data-ttu-id="010b0-115"><dt>**GLU \_ nenhum**</dt></span><span class="sxs-lookup"><span data-stu-id="010b0-115"><dt>**GLU\_NONE**</dt></span></span> </dl>       | <span data-ttu-id="010b0-116">Nenhum normal é gerado.</span><span class="sxs-lookup"><span data-stu-id="010b0-116">No normals are generated.</span></span><br/>                                                         |
| <span id="GLU_FLAT"></span><span id="glu_flat"></span><dl> <span data-ttu-id="010b0-117"><dt>**GLU \_ simples**</dt></span><span class="sxs-lookup"><span data-stu-id="010b0-117"><dt>**GLU\_FLAT**</dt></span></span> </dl>       | <span data-ttu-id="010b0-118">Um normal é gerado para cada faceta de um Quadric.</span><span class="sxs-lookup"><span data-stu-id="010b0-118">One normal is generated for every facet of a quadric.</span></span><br/>                             |
| <span id="GLU_SMOOTH"></span><span id="glu_smooth"></span><dl> <span data-ttu-id="010b0-119"><dt>**\_Smooth Glu**</dt></span><span class="sxs-lookup"><span data-stu-id="010b0-119"><dt>**GLU\_SMOOTH**</dt></span></span> </dl> | <span data-ttu-id="010b0-120">Um normal é gerado para cada vértice de um Quadric.</span><span class="sxs-lookup"><span data-stu-id="010b0-120">One normal is generated for every vertex of a quadric.</span></span> <span data-ttu-id="010b0-121">Esse é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="010b0-121">This is the default value.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="010b0-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="010b0-122">Return value</span></span>

<span data-ttu-id="010b0-123">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="010b0-123">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="010b0-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="010b0-124">Remarks</span></span>

<span data-ttu-id="010b0-125">A função **gluQuadricNormals** especifica que tipo de Normals deve ser usado para quadrics renderizado com o **quadobject**.</span><span class="sxs-lookup"><span data-stu-id="010b0-125">The **gluQuadricNormals** function specifies what kind of normals are to be used for quadrics rendered with **quadObject**.</span></span>

## <a name="requirements"></a><span data-ttu-id="010b0-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="010b0-126">Requirements</span></span>



| <span data-ttu-id="010b0-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="010b0-127">Requirement</span></span> | <span data-ttu-id="010b0-128">Valor</span><span class="sxs-lookup"><span data-stu-id="010b0-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="010b0-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="010b0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="010b0-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="010b0-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="010b0-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="010b0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="010b0-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="010b0-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="010b0-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="010b0-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="010b0-134"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="010b0-134"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="010b0-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="010b0-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="010b0-136"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="010b0-136"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="010b0-137">DLL</span><span class="sxs-lookup"><span data-stu-id="010b0-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="010b0-138"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="010b0-138"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="010b0-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="010b0-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="010b0-140">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="010b0-140">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="010b0-141">**gluQuadricDrawStyle**</span><span class="sxs-lookup"><span data-stu-id="010b0-141">**gluQuadricDrawStyle**</span></span>](gluquadricdrawstyle.md)
</dt> <dt>

[<span data-ttu-id="010b0-142">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="010b0-142">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="010b0-143">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="010b0-143">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> </dl>

 

 





