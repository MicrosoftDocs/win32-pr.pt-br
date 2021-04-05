---
title: função gluDeleteTess (Glu. h)
description: A função gluDeleteTess destrói um objeto de mosaico.
ms.assetid: 7e1540f7-5e7d-4a3b-8c94-5a6800b17411
keywords:
- função gluDeleteTess OpenGL
topic_type:
- apiref
api_name:
- gluDeleteTess
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee4625f0a9c2f51e9d7147c9564fcd4fb1fa7117
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644432"
---
# <a name="gludeletetess-function"></a><span data-ttu-id="cda0d-104">função gluDeleteTess</span><span class="sxs-lookup"><span data-stu-id="cda0d-104">gluDeleteTess function</span></span>

<span data-ttu-id="cda0d-105">A função **gluDeleteTess** destrói um objeto de mosaico.</span><span class="sxs-lookup"><span data-stu-id="cda0d-105">The **gluDeleteTess** function destroys a tessellation object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cda0d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cda0d-106">Syntax</span></span>


```C++
void WINAPI gluDeleteTess(
   GLUtesselator *tess
);
```



## <a name="parameters"></a><span data-ttu-id="cda0d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cda0d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cda0d-108">*tess*</span><span class="sxs-lookup"><span data-stu-id="cda0d-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="cda0d-109">O objeto de mosaico a ser destruído (criado com [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="cda0d-109">The tessellation object to destroy (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cda0d-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cda0d-110">Return value</span></span>

<span data-ttu-id="cda0d-111">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="cda0d-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cda0d-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="cda0d-112">Remarks</span></span>

<span data-ttu-id="cda0d-113">A função **gluDeleteTess** destrói o objeto de mosaico indicado e libera a memória que ele usou.</span><span class="sxs-lookup"><span data-stu-id="cda0d-113">The **gluDeleteTess** function destroys the indicated tessellation object and frees any memory that it used.</span></span>

## <a name="requirements"></a><span data-ttu-id="cda0d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cda0d-114">Requirements</span></span>



| <span data-ttu-id="cda0d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cda0d-115">Requirement</span></span> | <span data-ttu-id="cda0d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="cda0d-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cda0d-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cda0d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cda0d-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cda0d-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="cda0d-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cda0d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cda0d-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cda0d-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cda0d-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cda0d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cda0d-122"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="cda0d-122"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="cda0d-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cda0d-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="cda0d-124"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cda0d-124"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="cda0d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="cda0d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cda0d-126"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cda0d-126"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cda0d-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="cda0d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cda0d-128">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="cda0d-128">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="cda0d-129">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="cda0d-129">**gluTessBeginPolygon**</span></span>](glubeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="cda0d-130">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="cda0d-130">*gluTessCallback*</span></span>](glutess.md)
</dt> </dl>

 

 





