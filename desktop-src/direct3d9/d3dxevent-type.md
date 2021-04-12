---
description: Descreve o tipo de eventos que podem ser codificados pelo controlador de animação.
ms.assetid: d98b398e-29e1-41b5-84eb-37983bac8d0a
title: Enumeração de D3DXEVENT_TYPE (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEVENT_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 97219478b898dc47e385e8e00a5cc9b5484730ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298625"
---
# <a name="d3dxevent_type-enumeration"></a><span data-ttu-id="23e3c-103">\_Enumeração de tipo D3DXEVENT</span><span class="sxs-lookup"><span data-stu-id="23e3c-103">D3DXEVENT\_TYPE enumeration</span></span>

<span data-ttu-id="23e3c-104">Descreve o tipo de eventos que podem ser codificados pelo controlador de animação.</span><span class="sxs-lookup"><span data-stu-id="23e3c-104">Describes the type of events that can be keyed by the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="23e3c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="23e3c-105">Syntax</span></span>


```C++
typedef enum D3DXEVENT_TYPE { 
  D3DXEVENT_TRACKSPEED     = 0,
  D3DXEVENT_TRACKWEIGHT    = 1,
  D3DXEVENT_TRACKPOSITION  = 2,
  D3DXEVENT_TRACKENABLE    = 3,
  D3DXEVENT_PRIORITYBLEND  = 4,
  D3DXEVENT_FORCE_DWORD    = 0x7fffffff
} D3DXEVENT_TYPE, *LPD3DXEVENT_TYPE;
```



## <a name="constants"></a><span data-ttu-id="23e3c-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="23e3c-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="23e3c-107"><span id="D3DXEVENT_TRACKSPEED"></span><span id="d3dxevent_trackspeed"></span>**D3DXEVENT \_ TRACKSPEED**</span><span class="sxs-lookup"><span data-stu-id="23e3c-107"><span id="D3DXEVENT_TRACKSPEED"></span><span id="d3dxevent_trackspeed"></span>**D3DXEVENT\_TRACKSPEED**</span></span>
</dt> <dd>

<span data-ttu-id="23e3c-108">Controlar a velocidade.</span><span class="sxs-lookup"><span data-stu-id="23e3c-108">Track speed.</span></span>

</dd> <dt>

<span data-ttu-id="23e3c-109"><span id="D3DXEVENT_TRACKWEIGHT"></span><span id="d3dxevent_trackweight"></span>**D3DXEVENT \_ TRACKWEIGHT**</span><span class="sxs-lookup"><span data-stu-id="23e3c-109"><span id="D3DXEVENT_TRACKWEIGHT"></span><span id="d3dxevent_trackweight"></span>**D3DXEVENT\_TRACKWEIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="23e3c-110">Alcance da faixa.</span><span class="sxs-lookup"><span data-stu-id="23e3c-110">Track weight.</span></span>

</dd> <dt>

<span data-ttu-id="23e3c-111"><span id="D3DXEVENT_TRACKPOSITION"></span><span id="d3dxevent_trackposition"></span>**D3DXEVENT \_ TRACKPOSITION**</span><span class="sxs-lookup"><span data-stu-id="23e3c-111"><span id="D3DXEVENT_TRACKPOSITION"></span><span id="d3dxevent_trackposition"></span>**D3DXEVENT\_TRACKPOSITION**</span></span>
</dt> <dd>

<span data-ttu-id="23e3c-112">Posição da faixa.</span><span class="sxs-lookup"><span data-stu-id="23e3c-112">Track position.</span></span>

</dd> <dt>

<span data-ttu-id="23e3c-113"><span id="D3DXEVENT_TRACKENABLE"></span><span id="d3dxevent_trackenable"></span>**D3DXEVENT \_ TRACKENABLE**</span><span class="sxs-lookup"><span data-stu-id="23e3c-113"><span id="D3DXEVENT_TRACKENABLE"></span><span id="d3dxevent_trackenable"></span>**D3DXEVENT\_TRACKENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="23e3c-114">Habilitar sinalizador.</span><span class="sxs-lookup"><span data-stu-id="23e3c-114">Enable flag.</span></span>

</dd> <dt>

<span data-ttu-id="23e3c-115"><span id="D3DXEVENT_PRIORITYBLEND"></span><span id="d3dxevent_priorityblend"></span>**D3DXEVENT \_ PRIORITYBLEND**</span><span class="sxs-lookup"><span data-stu-id="23e3c-115"><span id="D3DXEVENT_PRIORITYBLEND"></span><span id="d3dxevent_priorityblend"></span>**D3DXEVENT\_PRIORITYBLEND**</span></span>
</dt> <dd>

<span data-ttu-id="23e3c-116">Valor de mesclagem de prioridade.</span><span class="sxs-lookup"><span data-stu-id="23e3c-116">Priority blend value.</span></span>

</dd> <dt>

<span data-ttu-id="23e3c-117"><span id="D3DXEVENT_FORCE_DWORD"></span><span id="d3dxevent_force_dword"></span>**D3DXEVENT \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="23e3c-117"><span id="D3DXEVENT_FORCE_DWORD"></span><span id="d3dxevent_force_dword"></span>**D3DXEVENT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="23e3c-118">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="23e3c-118">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="23e3c-119">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="23e3c-119">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="23e3c-120">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="23e3c-120">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="23e3c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23e3c-121">Requirements</span></span>



| <span data-ttu-id="23e3c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="23e3c-122">Requirement</span></span> | <span data-ttu-id="23e3c-123">Valor</span><span class="sxs-lookup"><span data-stu-id="23e3c-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="23e3c-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="23e3c-124">Header</span></span><br/> | <dl> <span data-ttu-id="23e3c-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="23e3c-125"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23e3c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="23e3c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23e3c-127">Enumerações D3DX</span><span class="sxs-lookup"><span data-stu-id="23e3c-127">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




