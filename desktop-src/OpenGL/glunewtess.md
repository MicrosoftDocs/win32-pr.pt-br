---
title: função gluNewTess (Glu. h)
description: A função gluNewTess cria um objeto de mosaico.
ms.assetid: dfc9fce8-ecab-493b-85ee-6d7487814186
keywords:
- função gluNewTess OpenGL
topic_type:
- apiref
api_name:
- gluNewTess
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0573ead0cf9b81568c4bf2101e317bef7faf148
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755329"
---
# <a name="glunewtess-function"></a><span data-ttu-id="99b3a-104">função gluNewTess</span><span class="sxs-lookup"><span data-stu-id="99b3a-104">gluNewTess function</span></span>

<span data-ttu-id="99b3a-105">A função **gluNewTess** cria um objeto de mosaico.</span><span class="sxs-lookup"><span data-stu-id="99b3a-105">The **gluNewTess** function creates a tessellation object.</span></span>

## <a name="syntax"></a><span data-ttu-id="99b3a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="99b3a-106">Syntax</span></span>


```C++
GLUtesselator* WINAPI gluNewTess(void);
```



## <a name="parameters"></a><span data-ttu-id="99b3a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="99b3a-107">Parameters</span></span>

<span data-ttu-id="99b3a-108">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="99b3a-108">This function has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="99b3a-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="99b3a-109">Remarks</span></span>

<span data-ttu-id="99b3a-110">A função **gluNewTess** cria e retorna um ponteiro para um novo objeto de mosaico.</span><span class="sxs-lookup"><span data-stu-id="99b3a-110">The **gluNewTess** function creates and returns a pointer to a new tessellation object.</span></span> <span data-ttu-id="99b3a-111">Consulte este objeto ao chamar funções de mosaico.</span><span class="sxs-lookup"><span data-stu-id="99b3a-111">Refer to this object when calling tessellation functions.</span></span> <span data-ttu-id="99b3a-112">Um valor de retorno igual a zero significa que não há memória suficiente para alocar para o objeto.</span><span class="sxs-lookup"><span data-stu-id="99b3a-112">A return value of zero means there is not enough memory to allocate to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="99b3a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99b3a-113">Requirements</span></span>



| <span data-ttu-id="99b3a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="99b3a-114">Requirement</span></span> | <span data-ttu-id="99b3a-115">Valor</span><span class="sxs-lookup"><span data-stu-id="99b3a-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="99b3a-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99b3a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="99b3a-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="99b3a-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="99b3a-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99b3a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="99b3a-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="99b3a-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="99b3a-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="99b3a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="99b3a-121"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="99b3a-121"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="99b3a-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="99b3a-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="99b3a-123"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99b3a-123"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="99b3a-124">DLL</span><span class="sxs-lookup"><span data-stu-id="99b3a-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99b3a-125"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99b3a-125"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99b3a-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="99b3a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99b3a-127">**gluDeleteTess**</span><span class="sxs-lookup"><span data-stu-id="99b3a-127">**gluDeleteTess**</span></span>](gludeletetess.md)
</dt> <dt>

[<span data-ttu-id="99b3a-128">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="99b3a-128">**gluTessBeginPolygon**</span></span>](glubeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="99b3a-129">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="99b3a-129">*gluTessCallback*</span></span>](glutess.md)
</dt> </dl>

 

 





