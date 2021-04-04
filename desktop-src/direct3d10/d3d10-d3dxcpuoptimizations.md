---
description: Habilita ou desabilita otimizações de CPU.
ms.assetid: 6f73df12-f2fc-4651-b0f7-f7a55e534d3d
title: Função D3DXCpuOptimizations (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCpuOptimizations
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a0ef276e6d3303acd77c9580b55a9aa49dbe2087
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664056"
---
# <a name="d3dxcpuoptimizations-function"></a><span data-ttu-id="23a7c-103">Função D3DXCpuOptimizations</span><span class="sxs-lookup"><span data-stu-id="23a7c-103">D3DXCpuOptimizations function</span></span>

<span data-ttu-id="23a7c-104">Habilita ou desabilita otimizações de CPU.</span><span class="sxs-lookup"><span data-stu-id="23a7c-104">Enables or disables CPU optimizations.</span></span>

## <a name="syntax"></a><span data-ttu-id="23a7c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="23a7c-105">Syntax</span></span>


```C++
D3DX_CPU_OPTIMIZATION D3DXCpuOptimizations(
  _In_ BOOL Enable
);
```



## <a name="parameters"></a><span data-ttu-id="23a7c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="23a7c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23a7c-107">*Habilitar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="23a7c-107">*Enable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23a7c-108">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="23a7c-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="23a7c-109">**True** para habilitar otimizações de CPU; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="23a7c-109">**TRUE** to enable CPU optimizations; otherwise **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23a7c-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="23a7c-110">Return value</span></span>

<span data-ttu-id="23a7c-111">Tipo: **[ **\_ \_ otimização da CPU D3DX**](d3dx-cpu-optimization.md)**</span><span class="sxs-lookup"><span data-stu-id="23a7c-111">Type: **[**D3DX\_CPU\_OPTIMIZATION**](d3dx-cpu-optimization.md)**</span></span>

<span data-ttu-id="23a7c-112">Retorna o tipo de CPU detectada e para quais otimizações existem (consulte [**D3DX \_ CPU \_ Optimization**](d3dx-cpu-optimization.md)).</span><span class="sxs-lookup"><span data-stu-id="23a7c-112">Returns the type of CPU detected, and for which optimizations exist (see [**D3DX\_CPU\_OPTIMIZATION**](d3dx-cpu-optimization.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="23a7c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23a7c-113">Requirements</span></span>



| <span data-ttu-id="23a7c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="23a7c-114">Requirement</span></span> | <span data-ttu-id="23a7c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="23a7c-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23a7c-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="23a7c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="23a7c-117"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="23a7c-117"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="23a7c-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="23a7c-118">Library</span></span><br/> | <dl> <span data-ttu-id="23a7c-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23a7c-119"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="23a7c-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="23a7c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23a7c-121">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="23a7c-121">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
