---
description: Descreve uma chave do Quaternion para uso na animação do quadro chave. Uma chave Quaternion é um valor de Quaternion em um determinado momento.
ms.assetid: 8f5b74a3-f712-40ac-942c-a2189c2327c8
title: Estrutura de D3DXKEY_QUATERNION (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_QUATERNION
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 12e4deead606c1a2c5b103ed9fd0e31e23515982
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298611"
---
# <a name="d3dxkey_quaternion-structure"></a><span data-ttu-id="693c7-104">\_Estrutura de QUATERNION D3DXKEY</span><span class="sxs-lookup"><span data-stu-id="693c7-104">D3DXKEY\_QUATERNION structure</span></span>

<span data-ttu-id="693c7-105">Descreve uma chave do Quaternion para uso na animação do quadro chave.</span><span class="sxs-lookup"><span data-stu-id="693c7-105">Describes a quaternion key for use in key frame animation.</span></span> <span data-ttu-id="693c7-106">Uma chave Quaternion é um valor de Quaternion em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="693c7-106">A quaternion key is a quaternion value at a given time.</span></span>

## <a name="syntax"></a><span data-ttu-id="693c7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="693c7-107">Syntax</span></span>


```C++
typedef struct D3DXKEY_QUATERNION {
  FLOAT          Time;
  D3DXQUATERNION Value;
} D3DXKEY_QUATERNION, *LPD3DXKEY_QUATERNION;
```



## <a name="members"></a><span data-ttu-id="693c7-108">Membros</span><span class="sxs-lookup"><span data-stu-id="693c7-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="693c7-109">**Hora**</span><span class="sxs-lookup"><span data-stu-id="693c7-109">**Time**</span></span>
</dt> <dd>

<span data-ttu-id="693c7-110">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="693c7-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="693c7-111">O valor temporal.</span><span class="sxs-lookup"><span data-stu-id="693c7-111">Time value.</span></span>

</dd> <dt>

<span data-ttu-id="693c7-112">**Valor**</span><span class="sxs-lookup"><span data-stu-id="693c7-112">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="693c7-113">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)**</span><span class="sxs-lookup"><span data-stu-id="693c7-113">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)**</span></span>

</dd> <dd>

<span data-ttu-id="693c7-114">[**D3DXQUATERNION**](d3dxquaternion.md) Quaternion que fornece valores de rotação.</span><span class="sxs-lookup"><span data-stu-id="693c7-114">[**D3DXQUATERNION**](d3dxquaternion.md) quaternion that supplies rotation values.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="693c7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="693c7-115">Requirements</span></span>



| <span data-ttu-id="693c7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="693c7-116">Requirement</span></span> | <span data-ttu-id="693c7-117">Valor</span><span class="sxs-lookup"><span data-stu-id="693c7-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="693c7-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="693c7-118">Header</span></span><br/> | <dl> <span data-ttu-id="693c7-119"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="693c7-119"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="693c7-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="693c7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="693c7-121">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="693c7-121">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
