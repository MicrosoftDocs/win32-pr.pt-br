---
description: Crie um token de número de versão do sombreador de vértice.
ms.assetid: c3aa6b01-7949-4171-a8b5-2f453fd7a422
title: Macro D3DVS_VERSION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVS_VERSION
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 915d5b843287602c80572d739d8b369d8c301770
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105772634"
---
# <a name="d3dvs_version-macro"></a><span data-ttu-id="4cdf6-103">Macro de versão do D3DVS \_</span><span class="sxs-lookup"><span data-stu-id="4cdf6-103">D3DVS\_VERSION macro</span></span>

<span data-ttu-id="4cdf6-104">Crie um token de número de versão do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="4cdf6-104">Create a vertex shader version number token.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cdf6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4cdf6-105">Syntax</span></span>


```C++
DWORD D3DVS_VERSION(
   int _Major,
   int _Minor
);
```



## <a name="parameters"></a><span data-ttu-id="4cdf6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4cdf6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cdf6-107">*\_Primária*</span><span class="sxs-lookup"><span data-stu-id="4cdf6-107">*\_Major*</span></span> 
</dt> <dd>

<span data-ttu-id="4cdf6-108">A versão principal do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="4cdf6-108">The major vertex shader version.</span></span> <span data-ttu-id="4cdf6-109">Consulte comentários para obter os valores apropriados.</span><span class="sxs-lookup"><span data-stu-id="4cdf6-109">See remarks for appropriate values.</span></span>

</dd> <dt>

<span data-ttu-id="4cdf6-110">*\_Secundária*</span><span class="sxs-lookup"><span data-stu-id="4cdf6-110">*\_Minor*</span></span> 
</dt> <dd>

<span data-ttu-id="4cdf6-111">A versão secundária do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="4cdf6-111">The minor vertex shader version.</span></span> <span data-ttu-id="4cdf6-112">Consulte comentários para obter os valores apropriados.</span><span class="sxs-lookup"><span data-stu-id="4cdf6-112">See remarks for appropriate values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cdf6-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4cdf6-113">Return value</span></span>

<span data-ttu-id="4cdf6-114">Retorna um valor DWORD que é uma versão de sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="4cdf6-114">Returns a DWORD value that is a vertex shader version.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cdf6-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="4cdf6-115">Remarks</span></span>

<span data-ttu-id="4cdf6-116">Números de versão</span><span class="sxs-lookup"><span data-stu-id="4cdf6-116">Version Numbers</span></span>

<span data-ttu-id="4cdf6-117">O número de versão é uma combinação da versão principal e dos números de versão do sombreador de vértice secundário.</span><span class="sxs-lookup"><span data-stu-id="4cdf6-117">The version number is a combination of the major version and the minor vertex shader version numbers.</span></span> <span data-ttu-id="4cdf6-118">Os números válidos são mostrados na tabela.</span><span class="sxs-lookup"><span data-stu-id="4cdf6-118">Valid numbers are shown in the table.</span></span>



| <span data-ttu-id="4cdf6-119">Principal</span><span class="sxs-lookup"><span data-stu-id="4cdf6-119">Major</span></span> | <span data-ttu-id="4cdf6-120">Secundária</span><span class="sxs-lookup"><span data-stu-id="4cdf6-120">Minor</span></span> | <span data-ttu-id="4cdf6-121">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4cdf6-121">Example</span></span>             |
|-------|-------|---------------------|
| <span data-ttu-id="4cdf6-122">1</span><span class="sxs-lookup"><span data-stu-id="4cdf6-122">1</span></span>     | <span data-ttu-id="4cdf6-123">1</span><span class="sxs-lookup"><span data-stu-id="4cdf6-123">1</span></span>     | <span data-ttu-id="4cdf6-124">\_Versão D3DVS (1, 1)</span><span class="sxs-lookup"><span data-stu-id="4cdf6-124">D3DVS\_VERSION(1,1)</span></span> |
| <span data-ttu-id="4cdf6-125">2</span><span class="sxs-lookup"><span data-stu-id="4cdf6-125">2</span></span>     | <span data-ttu-id="4cdf6-126">0</span><span class="sxs-lookup"><span data-stu-id="4cdf6-126">0</span></span>     | <span data-ttu-id="4cdf6-127">\_Versão D3DVS (2, 0)</span><span class="sxs-lookup"><span data-stu-id="4cdf6-127">D3DVS\_VERSION(2,0)</span></span> |
| <span data-ttu-id="4cdf6-128">3</span><span class="sxs-lookup"><span data-stu-id="4cdf6-128">3</span></span>     | <span data-ttu-id="4cdf6-129">0</span><span class="sxs-lookup"><span data-stu-id="4cdf6-129">0</span></span>     | <span data-ttu-id="4cdf6-130">\_Versão D3DVS (3, 0)</span><span class="sxs-lookup"><span data-stu-id="4cdf6-130">D3DVS\_VERSION(3,0)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="4cdf6-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4cdf6-131">Requirements</span></span>



| <span data-ttu-id="4cdf6-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cdf6-132">Requirement</span></span> | <span data-ttu-id="4cdf6-133">Valor</span><span class="sxs-lookup"><span data-stu-id="4cdf6-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4cdf6-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4cdf6-134">Header</span></span><br/> | <dl> <span data-ttu-id="4cdf6-135"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cdf6-135"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cdf6-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="4cdf6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cdf6-137">Macros</span><span class="sxs-lookup"><span data-stu-id="4cdf6-137">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




