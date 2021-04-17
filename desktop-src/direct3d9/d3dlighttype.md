---
description: Define o tipo de luz.
ms.assetid: 90ad82d3-ffa8-42bb-9d9c-cf28a416c32d
title: Enumeração D3DLIGHTTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLIGHTTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 83c94db3126443f757f01a69d7d773417f70683a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105813727"
---
# <a name="d3dlighttype-enumeration"></a><span data-ttu-id="c5190-103">Enumeração D3DLIGHTTYPE</span><span class="sxs-lookup"><span data-stu-id="c5190-103">D3DLIGHTTYPE enumeration</span></span>

<span data-ttu-id="c5190-104">Define o tipo de luz.</span><span class="sxs-lookup"><span data-stu-id="c5190-104">Defines the light type.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5190-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5190-105">Syntax</span></span>


```C++
typedef enum D3DLIGHTTYPE { 
  D3DLIGHT_POINT        = 1,
  D3DLIGHT_SPOT         = 2,
  D3DLIGHT_DIRECTIONAL  = 3,
  D3DLIGHT_FORCE_DWORD  = 0x7fffffff
} D3DLIGHTTYPE, *LPD3DLIGHTTYPE;
```



## <a name="constants"></a><span data-ttu-id="c5190-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="c5190-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c5190-107"><span id="D3DLIGHT_POINT"></span><span id="d3dlight_point"></span>**Ponto de D3DLIGHT \_**</span><span class="sxs-lookup"><span data-stu-id="c5190-107"><span id="D3DLIGHT_POINT"></span><span id="d3dlight_point"></span>**D3DLIGHT\_POINT**</span></span>
</dt> <dd>

<span data-ttu-id="c5190-108">Light é uma fonte de ponto.</span><span class="sxs-lookup"><span data-stu-id="c5190-108">Light is a point source.</span></span> <span data-ttu-id="c5190-109">A luz tem uma posição em espaço e radia a luz em todas as direções.</span><span class="sxs-lookup"><span data-stu-id="c5190-109">The light has a position in space and radiates light in all directions.</span></span>

</dd> <dt>

<span data-ttu-id="c5190-110"><span id="D3DLIGHT_SPOT"></span><span id="d3dlight_spot"></span>**Ponto de D3DLIGHT \_**</span><span class="sxs-lookup"><span data-stu-id="c5190-110"><span id="D3DLIGHT_SPOT"></span><span id="d3dlight_spot"></span>**D3DLIGHT\_SPOT**</span></span>
</dt> <dd>

<span data-ttu-id="c5190-111">Light é uma fonte de destaque.</span><span class="sxs-lookup"><span data-stu-id="c5190-111">Light is a spotlight source.</span></span> <span data-ttu-id="c5190-112">Essa luz é como uma luz pontual, exceto que a iluminação é limitada a um cone.</span><span class="sxs-lookup"><span data-stu-id="c5190-112">This light is like a point light, except that the illumination is limited to a cone.</span></span> <span data-ttu-id="c5190-113">Esse tipo de luz tem uma direção e vários outros parâmetros que determinam a forma do cone que ele produz.</span><span class="sxs-lookup"><span data-stu-id="c5190-113">This light type has a direction and several other parameters that determine the shape of the cone it produces.</span></span> <span data-ttu-id="c5190-114">Para obter informações sobre esses parâmetros, consulte a estrutura [**D3DLIGHT9**](d3dlight9.md) .</span><span class="sxs-lookup"><span data-stu-id="c5190-114">For information about these parameters, see the [**D3DLIGHT9**](d3dlight9.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c5190-115"><span id="D3DLIGHT_DIRECTIONAL"></span><span id="d3dlight_directional"></span>**D3DLIGHT \_ direcional**</span><span class="sxs-lookup"><span data-stu-id="c5190-115"><span id="D3DLIGHT_DIRECTIONAL"></span><span id="d3dlight_directional"></span>**D3DLIGHT\_DIRECTIONAL**</span></span>
</dt> <dd>

<span data-ttu-id="c5190-116">Light é uma fonte de luz direcional.</span><span class="sxs-lookup"><span data-stu-id="c5190-116">Light is a directional light source.</span></span> <span data-ttu-id="c5190-117">Isso é equivalente a usar uma fonte de luz pontual em uma distância infinita.</span><span class="sxs-lookup"><span data-stu-id="c5190-117">This is equivalent to using a point light source at an infinite distance.</span></span>

</dd> <dt>

<span data-ttu-id="c5190-118"><span id="D3DLIGHT_FORCE_DWORD"></span><span id="d3dlight_force_dword"></span>**D3DLIGHT \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="c5190-118"><span id="D3DLIGHT_FORCE_DWORD"></span><span id="d3dlight_force_dword"></span>**D3DLIGHT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="c5190-119">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="c5190-119">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="c5190-120">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c5190-120">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="c5190-121">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="c5190-121">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c5190-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="c5190-122">Remarks</span></span>

<span data-ttu-id="c5190-123">As luzes direcionais são ligeiramente mais rápidas que as fontes de luz do ponto, mas as luzes do ponto parecem um pouco melhores.</span><span class="sxs-lookup"><span data-stu-id="c5190-123">Directional lights are slightly faster than point light sources, but point lights look a little better.</span></span> <span data-ttu-id="c5190-124">Os destaques oferecem efeitos visuais interessantes, mas são demorados computacionalmente.</span><span class="sxs-lookup"><span data-stu-id="c5190-124">Spotlights offer interesting visual effects but are computationally time-consuming.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5190-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5190-125">Requirements</span></span>



| <span data-ttu-id="c5190-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5190-126">Requirement</span></span> | <span data-ttu-id="c5190-127">Valor</span><span class="sxs-lookup"><span data-stu-id="c5190-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5190-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c5190-128">Header</span></span><br/> | <dl> <span data-ttu-id="c5190-129"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5190-129"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5190-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5190-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5190-131">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="c5190-131">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="c5190-132">**D3DLIGHT9**</span><span class="sxs-lookup"><span data-stu-id="c5190-132">**D3DLIGHT9**</span></span>](d3dlight9.md)
</dt> </dl>

 

 




