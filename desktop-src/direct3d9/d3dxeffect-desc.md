---
description: Descreve um objeto Effect.
ms.assetid: 161d3e7a-213a-4a83-a1b5-837b0aab96bf
title: Estrutura de D3DXEFFECT_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: c8e7a3a2adf19514e2e4d1c6f61dbea888ce033d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664007"
---
# <a name="d3dxeffect_desc-structure"></a><span data-ttu-id="360c1-103">\_Estrutura desc de D3DXEFFECT</span><span class="sxs-lookup"><span data-stu-id="360c1-103">D3DXEFFECT\_DESC structure</span></span>

<span data-ttu-id="360c1-104">Descreve um objeto Effect.</span><span class="sxs-lookup"><span data-stu-id="360c1-104">Describes an effect object.</span></span>

## <a name="syntax"></a><span data-ttu-id="360c1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="360c1-105">Syntax</span></span>


```C++
typedef struct D3DXEFFECT_DESC {
  LPCSTR Creator;
  UINT   Parameters;
  UINT   Techniques;
  UINT   Functions;
} D3DXEFFECT_DESC, *LPD3DXEFFECT_DESC;
```



## <a name="members"></a><span data-ttu-id="360c1-106">Membros</span><span class="sxs-lookup"><span data-stu-id="360c1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="360c1-107">**Criador**</span><span class="sxs-lookup"><span data-stu-id="360c1-107">**Creator**</span></span>
</dt> <dd>

<span data-ttu-id="360c1-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="360c1-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="360c1-109">Cadeia de caracteres que contém o nome do criador de efeito.</span><span class="sxs-lookup"><span data-stu-id="360c1-109">String that contains the name of the effect creator.</span></span>

</dd> <dt>

<span data-ttu-id="360c1-110">**Parâmetros**</span><span class="sxs-lookup"><span data-stu-id="360c1-110">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="360c1-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="360c1-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="360c1-112">Número de parâmetros usados para efeito.</span><span class="sxs-lookup"><span data-stu-id="360c1-112">Number of parameters used for effect.</span></span>

</dd> <dt>

<span data-ttu-id="360c1-113">**Técnicas**</span><span class="sxs-lookup"><span data-stu-id="360c1-113">**Techniques**</span></span>
</dt> <dd>

<span data-ttu-id="360c1-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="360c1-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="360c1-115">Número de técnicas que podem renderizar o efeito.</span><span class="sxs-lookup"><span data-stu-id="360c1-115">Number of techniques that can render the effect.</span></span>

</dd> <dt>

<span data-ttu-id="360c1-116">**Funções**</span><span class="sxs-lookup"><span data-stu-id="360c1-116">**Functions**</span></span>
</dt> <dd>

<span data-ttu-id="360c1-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="360c1-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="360c1-118">Número de funções que podem renderizar o efeito.</span><span class="sxs-lookup"><span data-stu-id="360c1-118">Number of functions that can render the effect.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="360c1-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="360c1-119">Remarks</span></span>

<span data-ttu-id="360c1-120">Um objeto Effect pode conter várias técnicas de renderização e parâmetros para o mesmo efeito.</span><span class="sxs-lookup"><span data-stu-id="360c1-120">An effect object can contain multiple rendering techniques and parameters for the same effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="360c1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="360c1-121">Requirements</span></span>



| <span data-ttu-id="360c1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="360c1-122">Requirement</span></span> | <span data-ttu-id="360c1-123">Valor</span><span class="sxs-lookup"><span data-stu-id="360c1-123">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="360c1-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="360c1-124">Header</span></span><br/> | <dl> <span data-ttu-id="360c1-125"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="360c1-125"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="360c1-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="360c1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="360c1-127">Estruturas de efeito</span><span class="sxs-lookup"><span data-stu-id="360c1-127">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
