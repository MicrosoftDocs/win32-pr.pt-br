---
title: função gluDeleteQuadric (Glu. h)
description: A função gluDeleteQuadric destrói um objeto Quadric.
ms.assetid: 09efd887-0fe8-4a56-bc6f-2177a4930035
keywords:
- função gluDeleteQuadric OpenGL
topic_type:
- apiref
api_name:
- gluDeleteQuadric
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b5ee85e943cd958e394efb191932393d228d948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644832"
---
# <a name="gludeletequadric-function"></a><span data-ttu-id="9eb44-104">função gluDeleteQuadric</span><span class="sxs-lookup"><span data-stu-id="9eb44-104">gluDeleteQuadric function</span></span>

<span data-ttu-id="9eb44-105">A função **gluDeleteQuadric** destrói um objeto Quadric.</span><span class="sxs-lookup"><span data-stu-id="9eb44-105">The **gluDeleteQuadric** function destroys a quadric object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eb44-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9eb44-106">Syntax</span></span>


```C++
void WINAPI gluDeleteQuadric(
   GLUquadricObj *state
);
```



## <a name="parameters"></a><span data-ttu-id="9eb44-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9eb44-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9eb44-108">*state*</span><span class="sxs-lookup"><span data-stu-id="9eb44-108">*state*</span></span> 
</dt> <dd>

<span data-ttu-id="9eb44-109">O objeto Quadric a ser destruído (criado com [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="9eb44-109">The quadric object to be destroyed (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9eb44-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9eb44-110">Return value</span></span>

<span data-ttu-id="9eb44-111">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9eb44-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9eb44-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="9eb44-112">Remarks</span></span>

<span data-ttu-id="9eb44-113">A função **gluDeleteQuadric** destrói o objeto Quadric e libera a memória que ele usou.</span><span class="sxs-lookup"><span data-stu-id="9eb44-113">The **gluDeleteQuadric** function destroys the quadric object and frees any memory that it used.</span></span> <span data-ttu-id="9eb44-114">Depois de ter chamado **gluDeleteQuadric**, você não poderá usar o *estado* novamente.</span><span class="sxs-lookup"><span data-stu-id="9eb44-114">After you have called **gluDeleteQuadric**, you cannot use *state* again.</span></span>

## <a name="requirements"></a><span data-ttu-id="9eb44-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9eb44-115">Requirements</span></span>



| <span data-ttu-id="9eb44-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9eb44-116">Requirement</span></span> | <span data-ttu-id="9eb44-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9eb44-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9eb44-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9eb44-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9eb44-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9eb44-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9eb44-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9eb44-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9eb44-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9eb44-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9eb44-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9eb44-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9eb44-123"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="9eb44-123"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="9eb44-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9eb44-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="9eb44-125"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9eb44-125"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9eb44-126">DLL</span><span class="sxs-lookup"><span data-stu-id="9eb44-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9eb44-127"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9eb44-127"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9eb44-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="9eb44-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eb44-129">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="9eb44-129">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> </dl>

 

 





