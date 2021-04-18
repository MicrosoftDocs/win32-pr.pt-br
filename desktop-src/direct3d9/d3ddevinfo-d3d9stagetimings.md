---
description: Porcentagem de tempo de processamento de dados do sombreador.
ms.assetid: 388bb943-c25f-4b50-b7e4-d6259f1186c2
title: Estrutura de D3DDEVINFO_D3D9STAGETIMINGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9STAGETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: cf8c9522decfcbb09a60aff0bee65ca05a0f5eeb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781011"
---
# <a name="d3ddevinfo_d3d9stagetimings-structure"></a><span data-ttu-id="c64d0-103">\_Estrutura D3DDEVINFO D3D9STAGETIMINGS</span><span class="sxs-lookup"><span data-stu-id="c64d0-103">D3DDEVINFO\_D3D9STAGETIMINGS structure</span></span>

<span data-ttu-id="c64d0-104">Porcentagem de tempo de processamento de dados do sombreador.</span><span class="sxs-lookup"><span data-stu-id="c64d0-104">Percent of time processing shader data.</span></span>

## <a name="syntax"></a><span data-ttu-id="c64d0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c64d0-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_D3D9STAGETIMINGS {
  FLOAT MemoryProcessingPercent;
  FLOAT ComputationProcessingPercent;
} D3DDEVINFO_D3D9STAGETIMINGS, *LPD3DDEVINFO_D3D9STAGETIMINGS;
```



## <a name="members"></a><span data-ttu-id="c64d0-106">Membros</span><span class="sxs-lookup"><span data-stu-id="c64d0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c64d0-107">**MemoryProcessingPercent**</span><span class="sxs-lookup"><span data-stu-id="c64d0-107">**MemoryProcessingPercent**</span></span>
</dt> <dd>

<span data-ttu-id="c64d0-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c64d0-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c64d0-109">Porcentagem de tempo no sombreador gasto em acessos à memória.</span><span class="sxs-lookup"><span data-stu-id="c64d0-109">Percent of time in shader spent on memory accesses.</span></span>

</dd> <dt>

<span data-ttu-id="c64d0-110">**ComputationProcessingPercent**</span><span class="sxs-lookup"><span data-stu-id="c64d0-110">**ComputationProcessingPercent**</span></span>
</dt> <dd>

<span data-ttu-id="c64d0-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c64d0-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c64d0-112">Porcentagem de processamento de tempo (movendo dados em registros ou fazendo operações matemáticas).</span><span class="sxs-lookup"><span data-stu-id="c64d0-112">Percent of time processing (moving data around in registers or doing mathematical operations).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c64d0-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="c64d0-113">Remarks</span></span>

<span data-ttu-id="c64d0-114">Para obter um melhor desempenho, é recomendável uma carga equilibrada.</span><span class="sxs-lookup"><span data-stu-id="c64d0-114">For best performance, a balanced load is recommended.</span></span>

## <a name="requirements"></a><span data-ttu-id="c64d0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c64d0-115">Requirements</span></span>



| <span data-ttu-id="c64d0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c64d0-116">Requirement</span></span> | <span data-ttu-id="c64d0-117">Valor</span><span class="sxs-lookup"><span data-stu-id="c64d0-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c64d0-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c64d0-118">Header</span></span><br/> | <dl> <span data-ttu-id="c64d0-119"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="c64d0-119"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c64d0-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="c64d0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c64d0-121">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="c64d0-121">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="c64d0-122">**GetData**</span><span class="sxs-lookup"><span data-stu-id="c64d0-122">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
