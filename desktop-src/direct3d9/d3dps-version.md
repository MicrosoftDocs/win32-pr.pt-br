---
description: Crie um token de versão do sombreador de pixel.
ms.assetid: 70089a93-83df-4ac4-8d98-4e1bb6ad2581
title: Macro D3DPS_VERSION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPS_VERSION
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: c3f30d673145ec9dfe38bd8e2a636ac04c9a195a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298659"
---
# <a name="d3dps_version-macro"></a><span data-ttu-id="54fac-103">Macro de versão do D3DPS \_</span><span class="sxs-lookup"><span data-stu-id="54fac-103">D3DPS\_VERSION macro</span></span>

<span data-ttu-id="54fac-104">Crie um token de versão do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="54fac-104">Create a pixel shader version token.</span></span>

## <a name="syntax"></a><span data-ttu-id="54fac-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="54fac-105">Syntax</span></span>


```C++
DWORD D3DPS_VERSION(
   int _Major,
   int _Minor
);
```



## <a name="parameters"></a><span data-ttu-id="54fac-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="54fac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54fac-107">*\_Primária*</span><span class="sxs-lookup"><span data-stu-id="54fac-107">*\_Major*</span></span> 
</dt> <dd>

<span data-ttu-id="54fac-108">A versão principal do sombreador de pixels.</span><span class="sxs-lookup"><span data-stu-id="54fac-108">The major pixel shader version.</span></span>

</dd> <dt>

<span data-ttu-id="54fac-109">*\_Secundária*</span><span class="sxs-lookup"><span data-stu-id="54fac-109">*\_Minor*</span></span> 
</dt> <dd>

<span data-ttu-id="54fac-110">A versão do sombreador de pixel secundário.</span><span class="sxs-lookup"><span data-stu-id="54fac-110">The minor pixel shader version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54fac-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="54fac-111">Return value</span></span>

<span data-ttu-id="54fac-112">Retorna um valor DWORD que é uma versão do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="54fac-112">Returns a DWORD value that is a pixel shader version.</span></span>

## <a name="remarks"></a><span data-ttu-id="54fac-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="54fac-113">Remarks</span></span>

<span data-ttu-id="54fac-114">Números de versão</span><span class="sxs-lookup"><span data-stu-id="54fac-114">Version Numbers</span></span>

<span data-ttu-id="54fac-115">O número de versão é uma combinação da versão principal e dos números de versão do sombreador de vértice secundário.</span><span class="sxs-lookup"><span data-stu-id="54fac-115">The version number is a combination of the major version and the minor vertex shader version numbers.</span></span> <span data-ttu-id="54fac-116">Os números válidos são mostrados na tabela.</span><span class="sxs-lookup"><span data-stu-id="54fac-116">Valid numbers are shown in the table.</span></span>



| <span data-ttu-id="54fac-117">Principal</span><span class="sxs-lookup"><span data-stu-id="54fac-117">Major</span></span> | <span data-ttu-id="54fac-118">Secundária</span><span class="sxs-lookup"><span data-stu-id="54fac-118">Minor</span></span> | <span data-ttu-id="54fac-119">Exemplo</span><span class="sxs-lookup"><span data-stu-id="54fac-119">Example</span></span>             |
|-------|-------|---------------------|
| <span data-ttu-id="54fac-120">1</span><span class="sxs-lookup"><span data-stu-id="54fac-120">1</span></span>     | <span data-ttu-id="54fac-121">1</span><span class="sxs-lookup"><span data-stu-id="54fac-121">1</span></span>     | <span data-ttu-id="54fac-122">\_Versão D3DPS (1, 1)</span><span class="sxs-lookup"><span data-stu-id="54fac-122">D3DPS\_VERSION(1,1)</span></span> |
| <span data-ttu-id="54fac-123">1</span><span class="sxs-lookup"><span data-stu-id="54fac-123">1</span></span>     | <span data-ttu-id="54fac-124">2</span><span class="sxs-lookup"><span data-stu-id="54fac-124">2</span></span>     | <span data-ttu-id="54fac-125">\_Versão D3DPS (1, 2)</span><span class="sxs-lookup"><span data-stu-id="54fac-125">D3DPS\_VERSION(1,2)</span></span> |
| <span data-ttu-id="54fac-126">1</span><span class="sxs-lookup"><span data-stu-id="54fac-126">1</span></span>     | <span data-ttu-id="54fac-127">3</span><span class="sxs-lookup"><span data-stu-id="54fac-127">3</span></span>     | <span data-ttu-id="54fac-128">\_Versão D3DPS (1, 3)</span><span class="sxs-lookup"><span data-stu-id="54fac-128">D3DPS\_VERSION(1,3)</span></span> |
| <span data-ttu-id="54fac-129">1</span><span class="sxs-lookup"><span data-stu-id="54fac-129">1</span></span>     | <span data-ttu-id="54fac-130">4</span><span class="sxs-lookup"><span data-stu-id="54fac-130">4</span></span>     | <span data-ttu-id="54fac-131">\_Versão D3DPS (1, 4)</span><span class="sxs-lookup"><span data-stu-id="54fac-131">D3DPS\_VERSION(1,4)</span></span> |
| <span data-ttu-id="54fac-132">2</span><span class="sxs-lookup"><span data-stu-id="54fac-132">2</span></span>     | <span data-ttu-id="54fac-133">0</span><span class="sxs-lookup"><span data-stu-id="54fac-133">0</span></span>     | <span data-ttu-id="54fac-134">\_Versão D3DPS (2, 0)</span><span class="sxs-lookup"><span data-stu-id="54fac-134">D3DPS\_VERSION(2,0)</span></span> |
| <span data-ttu-id="54fac-135">3</span><span class="sxs-lookup"><span data-stu-id="54fac-135">3</span></span>     | <span data-ttu-id="54fac-136">0</span><span class="sxs-lookup"><span data-stu-id="54fac-136">0</span></span>     | <span data-ttu-id="54fac-137">\_Versão D3DPS (3, 0)</span><span class="sxs-lookup"><span data-stu-id="54fac-137">D3DPS\_VERSION(3,0)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="54fac-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54fac-138">Requirements</span></span>



| <span data-ttu-id="54fac-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="54fac-139">Requirement</span></span> | <span data-ttu-id="54fac-140">Valor</span><span class="sxs-lookup"><span data-stu-id="54fac-140">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="54fac-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="54fac-141">Header</span></span><br/> | <dl> <span data-ttu-id="54fac-142"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="54fac-142"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54fac-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="54fac-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54fac-144">Macros</span><span class="sxs-lookup"><span data-stu-id="54fac-144">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="54fac-145">D3DCAPS9</span><span class="sxs-lookup"><span data-stu-id="54fac-145">D3DCAPS9</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> </dl>

 

 




