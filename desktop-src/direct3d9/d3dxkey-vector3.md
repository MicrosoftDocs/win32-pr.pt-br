---
description: Descreve uma chave de vetor para uso na animação de quadro chave. Ele especifica um vetor em um determinado momento. Isso é usado para chaves de escala e de tradução.
ms.assetid: 7a7ba2ce-c9f3-4a04-b865-39de9070868b
title: Estrutura de D3DXKEY_VECTOR3 (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_VECTOR3
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 41aec16da30a6e8742290b747b844b7fb22f6650
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793993"
---
# <a name="d3dxkey_vector3-structure"></a><span data-ttu-id="47618-105">\_Estrutura D3DXKEY VECTOR3</span><span class="sxs-lookup"><span data-stu-id="47618-105">D3DXKEY\_VECTOR3 structure</span></span>

<span data-ttu-id="47618-106">Descreve uma chave de vetor para uso na animação de quadro chave.</span><span class="sxs-lookup"><span data-stu-id="47618-106">Describes a vector key for use in key frame animation.</span></span> <span data-ttu-id="47618-107">Ele especifica um vetor em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="47618-107">It specifies a vector at a given time.</span></span> <span data-ttu-id="47618-108">Isso é usado para chaves de escala e de tradução.</span><span class="sxs-lookup"><span data-stu-id="47618-108">This is used for scale and translation keys.</span></span>

## <a name="syntax"></a><span data-ttu-id="47618-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47618-109">Syntax</span></span>


```C++
typedef struct D3DXKEY_VECTOR3 {
  FLOAT       Time;
  D3DXVECTOR3 Value;
} D3DXKEY_VECTOR3, *LPD3DXKEY_VECTOR3;
```



## <a name="members"></a><span data-ttu-id="47618-110">Membros</span><span class="sxs-lookup"><span data-stu-id="47618-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="47618-111">**Hora**</span><span class="sxs-lookup"><span data-stu-id="47618-111">**Time**</span></span>
</dt> <dd>

<span data-ttu-id="47618-112">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="47618-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="47618-113">Carimbo de data/hora do quadro principal.</span><span class="sxs-lookup"><span data-stu-id="47618-113">Key frame time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="47618-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="47618-114">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="47618-115">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)**</span><span class="sxs-lookup"><span data-stu-id="47618-115">Type: **[**D3DXVECTOR3**](d3dxvector3.md)**</span></span>

</dd> <dd>

<span data-ttu-id="47618-116">Vetor 3D [**D3DXVECTOR3**](d3dxvector3.md) que fornece valores de escala e/ou translação.</span><span class="sxs-lookup"><span data-stu-id="47618-116">[**D3DXVECTOR3**](d3dxvector3.md) 3D vector that supplies scale and/or translation values.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="47618-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47618-117">Requirements</span></span>



| <span data-ttu-id="47618-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="47618-118">Requirement</span></span> | <span data-ttu-id="47618-119">Valor</span><span class="sxs-lookup"><span data-stu-id="47618-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="47618-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="47618-120">Header</span></span><br/> | <dl> <span data-ttu-id="47618-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="47618-121"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47618-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="47618-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47618-123">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="47618-123">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
