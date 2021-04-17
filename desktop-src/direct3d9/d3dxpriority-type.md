---
description: Define o tipo de prioridade ao qual uma faixa de animação é atribuída.
ms.assetid: 7bd83e31-09c4-4376-a22d-ed8023b78e84
title: Enumeração de D3DXPRIORITY_TYPE (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPRIORITY_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 5e6d82807cbd0e93e7a1127db80726c0ec06b5da
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370945"
---
# <a name="d3dxpriority_type-enumeration"></a><span data-ttu-id="968c0-103">\_Enumeração de tipo D3DXPRIORITY</span><span class="sxs-lookup"><span data-stu-id="968c0-103">D3DXPRIORITY\_TYPE enumeration</span></span>

<span data-ttu-id="968c0-104">Define o tipo de prioridade ao qual uma faixa de animação é atribuída.</span><span class="sxs-lookup"><span data-stu-id="968c0-104">Defines the priority type to which an animation track is assigned.</span></span>

## <a name="syntax"></a><span data-ttu-id="968c0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="968c0-105">Syntax</span></span>


```C++
typedef enum D3DXPRIORITY_TYPE { 
  D3DXPRIORITY_LOW          = 0,
  D3DXPRIORITY_HIGH         = 1,
  D3DXPRIORITY_FORCE_DWORD  = 0x7fffffff
} D3DXPRIORITY_TYPE, *LPD3DXPRIORITY_TYPE;
```



## <a name="constants"></a><span data-ttu-id="968c0-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="968c0-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="968c0-107"><span id="D3DXPRIORITY_LOW"></span><span id="d3dxpriority_low"></span>**D3DXPRIORITY \_ baixo**</span><span class="sxs-lookup"><span data-stu-id="968c0-107"><span id="D3DXPRIORITY_LOW"></span><span id="d3dxpriority_low"></span>**D3DXPRIORITY\_LOW**</span></span>
</dt> <dd>

<span data-ttu-id="968c0-108">O controle deve ser combinado com todas as faixas de baixa prioridade antes que a mistura de baixa prioridade seja misturada com o Blend de alta prioridade.</span><span class="sxs-lookup"><span data-stu-id="968c0-108">Track should be blended with all the low-priority tracks before the low-priority blend is mixed with the high-priority blend.</span></span>

</dd> <dt>

<span data-ttu-id="968c0-109"><span id="D3DXPRIORITY_HIGH"></span><span id="d3dxpriority_high"></span>**D3DXPRIORITY \_ alto**</span><span class="sxs-lookup"><span data-stu-id="968c0-109"><span id="D3DXPRIORITY_HIGH"></span><span id="d3dxpriority_high"></span>**D3DXPRIORITY\_HIGH**</span></span>
</dt> <dd>

<span data-ttu-id="968c0-110">A faixa deve ser combinada com todas as faixas de alta prioridade antes que a mistura de alta prioridade seja misturada com a mistura de baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="968c0-110">Track should be blended with all the high-priority tracks before the high-priority blend is mixed with the low-priority blend.</span></span>

</dd> <dt>

<span data-ttu-id="968c0-111"><span id="D3DXPRIORITY_FORCE_DWORD"></span><span id="d3dxpriority_force_dword"></span>**D3DXPRIORITY \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="968c0-111"><span id="D3DXPRIORITY_FORCE_DWORD"></span><span id="d3dxpriority_force_dword"></span>**D3DXPRIORITY\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="968c0-112">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="968c0-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="968c0-113">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="968c0-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="968c0-114">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="968c0-114">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="968c0-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="968c0-115">Remarks</span></span>

<span data-ttu-id="968c0-116">As faixas com a mesma prioridade são mescladas e os dois valores resultantes são mesclados usando o fator de mesclagem de prioridade.</span><span class="sxs-lookup"><span data-stu-id="968c0-116">Tracks with the same priority are blended together, and the two resulting values are then blended using the priority blend factor.</span></span>

## <a name="requirements"></a><span data-ttu-id="968c0-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="968c0-117">Requirements</span></span>



| <span data-ttu-id="968c0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="968c0-118">Requirement</span></span> | <span data-ttu-id="968c0-119">Valor</span><span class="sxs-lookup"><span data-stu-id="968c0-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="968c0-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="968c0-120">Header</span></span><br/> | <dl> <span data-ttu-id="968c0-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="968c0-121"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="968c0-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="968c0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="968c0-123">Enumerações D3DX</span><span class="sxs-lookup"><span data-stu-id="968c0-123">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




