---
description: Define o grau das variáveis na equação que descreve uma curva.
ms.assetid: 52a9c57e-a48d-4d8a-a208-97a3d09e7abf
title: Enumeração D3DDEGREETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEGREETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 773ef3a8dd8fc5f4657119c2021c5723e54a3bd7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105785157"
---
# <a name="d3ddegreetype-enumeration"></a><span data-ttu-id="1bf00-103">Enumeração D3DDEGREETYPE</span><span class="sxs-lookup"><span data-stu-id="1bf00-103">D3DDEGREETYPE enumeration</span></span>

<span data-ttu-id="1bf00-104">Define o grau das variáveis na equação que descreve uma curva.</span><span class="sxs-lookup"><span data-stu-id="1bf00-104">Defines the degree of the variables in the equation that describes a curve.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bf00-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1bf00-105">Syntax</span></span>


```C++
typedef enum D3DDEGREETYPE { 
  D3DDEGREE_LINEAR     = 1,
  D3DDEGREE_QUADRATIC  = 2,
  D3DDEGREE_CUBIC      = 3,
  D3DDEGREE_QUINTIC    = 5,
  D3DCULL_FORCE_DWORD  = 0x7fffffff
} D3DDEGREETYPE, *LPD3DDEGREETYPE;
```



## <a name="constants"></a><span data-ttu-id="1bf00-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="1bf00-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1bf00-107"><span id="D3DDEGREE_LINEAR"></span><span id="d3ddegree_linear"></span>**D3DDEGREE \_ linear**</span><span class="sxs-lookup"><span data-stu-id="1bf00-107"><span id="D3DDEGREE_LINEAR"></span><span id="d3ddegree_linear"></span>**D3DDEGREE\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="1bf00-108">A curva é descrita por variáveis da primeira ordem.</span><span class="sxs-lookup"><span data-stu-id="1bf00-108">Curve is described by variables of first order.</span></span>

</dd> <dt>

<span data-ttu-id="1bf00-109"><span id="D3DDEGREE_QUADRATIC"></span><span id="d3ddegree_quadratic"></span>**D3DDEGREE \_ quadrática**</span><span class="sxs-lookup"><span data-stu-id="1bf00-109"><span id="D3DDEGREE_QUADRATIC"></span><span id="d3ddegree_quadratic"></span>**D3DDEGREE\_QUADRATIC**</span></span>
</dt> <dd>

<span data-ttu-id="1bf00-110">A curva é descrita por variáveis da segunda ordem.</span><span class="sxs-lookup"><span data-stu-id="1bf00-110">Curve is described by variables of second order.</span></span>

</dd> <dt>

<span data-ttu-id="1bf00-111"><span id="D3DDEGREE_CUBIC"></span><span id="d3ddegree_cubic"></span>**D3DDEGREE \_ cúbico**</span><span class="sxs-lookup"><span data-stu-id="1bf00-111"><span id="D3DDEGREE_CUBIC"></span><span id="d3ddegree_cubic"></span>**D3DDEGREE\_CUBIC**</span></span>
</dt> <dd>

<span data-ttu-id="1bf00-112">A curva é descrita por variáveis da terceira ordem.</span><span class="sxs-lookup"><span data-stu-id="1bf00-112">Curve is described by variables of third order.</span></span>

</dd> <dt>

<span data-ttu-id="1bf00-113"><span id="D3DDEGREE_QUINTIC"></span><span id="d3ddegree_quintic"></span>**D3DDEGREE \_ QUINTIC**</span><span class="sxs-lookup"><span data-stu-id="1bf00-113"><span id="D3DDEGREE_QUINTIC"></span><span id="d3ddegree_quintic"></span>**D3DDEGREE\_QUINTIC**</span></span>
</dt> <dd>

<span data-ttu-id="1bf00-114">A curva é descrita por variáveis da quarta ordem.</span><span class="sxs-lookup"><span data-stu-id="1bf00-114">Curve is described by variables of fourth order.</span></span>

</dd> <dt>

<span data-ttu-id="1bf00-115"><span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="1bf00-115"><span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="1bf00-116">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="1bf00-116">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="1bf00-117">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="1bf00-117">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="1bf00-118">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="1bf00-118">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1bf00-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="1bf00-119">Remarks</span></span>

<span data-ttu-id="1bf00-120">Os valores nessa enumeração são usados para descrever as curvas usadas por patches de retângulo e de triângulo.</span><span class="sxs-lookup"><span data-stu-id="1bf00-120">The values in this enumeration are used to describe the curves used by rectangle and triangle patches.</span></span> <span data-ttu-id="1bf00-121">Para obter mais informações, consulte D3DRS de \_ seleção.</span><span class="sxs-lookup"><span data-stu-id="1bf00-121">For more information, see D3DRS\_CULLMODE.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bf00-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1bf00-122">Requirements</span></span>



| <span data-ttu-id="1bf00-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bf00-123">Requirement</span></span> | <span data-ttu-id="1bf00-124">Valor</span><span class="sxs-lookup"><span data-stu-id="1bf00-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1bf00-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1bf00-125">Header</span></span><br/> | <dl> <span data-ttu-id="1bf00-126"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bf00-126"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bf00-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="1bf00-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bf00-128">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="1bf00-128">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="1bf00-129">**D3DCAPS9**</span><span class="sxs-lookup"><span data-stu-id="1bf00-129">**D3DCAPS9**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[<span data-ttu-id="1bf00-130">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="1bf00-130">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
