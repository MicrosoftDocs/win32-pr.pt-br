---
description: Define constantes que descrevem o modo de neblina.
ms.assetid: cd83c914-bc1d-4f66-b5a6-7984b7ec52cd
title: Enumeração D3DFOGMODE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFOGMODE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 8436a52edbb9460c6945c1526513629939ec444b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298697"
---
# <a name="d3dfogmode-enumeration"></a><span data-ttu-id="eb302-103">Enumeração D3DFOGMODE</span><span class="sxs-lookup"><span data-stu-id="eb302-103">D3DFOGMODE enumeration</span></span>

<span data-ttu-id="eb302-104">Define constantes que descrevem o modo de neblina.</span><span class="sxs-lookup"><span data-stu-id="eb302-104">Defines constants that describe the fog mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb302-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb302-105">Syntax</span></span>


```C++
typedef enum D3DFOGMODE { 
  D3DFOG_NONE         = 0,
  D3DFOG_EXP          = 1,
  D3DFOG_EXP2         = 2,
  D3DFOG_LINEAR       = 3,
  D3DFOG_FORCE_DWORD  = 0x7fffffff
} D3DFOGMODE, *LPD3DFOGMODE;
```



## <a name="constants"></a><span data-ttu-id="eb302-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="eb302-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="eb302-107"><span id="D3DFOG_NONE"></span><span id="d3dfog_none"></span>**D3DFOG \_ nenhum**</span><span class="sxs-lookup"><span data-stu-id="eb302-107"><span id="D3DFOG_NONE"></span><span id="d3dfog_none"></span>**D3DFOG\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="eb302-108">Nenhum efeito de neblina.</span><span class="sxs-lookup"><span data-stu-id="eb302-108">No fog effect.</span></span>

</dd> <dt>

<span data-ttu-id="eb302-109"><span id="D3DFOG_EXP"></span><span id="d3dfog_exp"></span>**D3DFOG \_ exp**</span><span class="sxs-lookup"><span data-stu-id="eb302-109"><span id="D3DFOG_EXP"></span><span id="d3dfog_exp"></span>**D3DFOG\_EXP**</span></span>
</dt> <dd>

<span data-ttu-id="eb302-110">O efeito de neblina intensifica exponencialmente, de acordo com a fórmula a seguir.</span><span class="sxs-lookup"><span data-stu-id="eb302-110">Fog effect intensifies exponentially, according to the following formula.</span></span>

![fórmula de intensidade de efeito de neblina](images/fogexp.png)

</dd> <dt>

<span data-ttu-id="eb302-112"><span id="D3DFOG_EXP2"></span><span id="d3dfog_exp2"></span>**D3DFOG \_ EXP2**</span><span class="sxs-lookup"><span data-stu-id="eb302-112"><span id="D3DFOG_EXP2"></span><span id="d3dfog_exp2"></span>**D3DFOG\_EXP2**</span></span>
</dt> <dd>

<span data-ttu-id="eb302-113">O efeito de neblina intensifica exponencialmente com o quadrado da distância, de acordo com a fórmula a seguir.</span><span class="sxs-lookup"><span data-stu-id="eb302-113">Fog effect intensifies exponentially with the square of the distance, according to the following formula.</span></span>

![fórmula da intensidade do efeito de neblina com base no quadrado de distância](images/fogexp2.png)

</dd> <dt>

<span data-ttu-id="eb302-115"><span id="D3DFOG_LINEAR"></span><span id="d3dfog_linear"></span>**D3DFOG \_ linear**</span><span class="sxs-lookup"><span data-stu-id="eb302-115"><span id="D3DFOG_LINEAR"></span><span id="d3dfog_linear"></span>**D3DFOG\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="eb302-116">O efeito de neblina intensifica linearmente entre os pontos inicial e final, de acordo com a fórmula a seguir.</span><span class="sxs-lookup"><span data-stu-id="eb302-116">Fog effect intensifies linearly between the start and end points, according to the following formula.</span></span>

![fórmula da intensidade do efeito de neblina com base nos pontos inicial e final](images/fogliner.png)

<span data-ttu-id="eb302-118">Esse é o único modo de neblina com suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="eb302-118">This is the only fog mode currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="eb302-119"><span id="D3DFOG_FORCE_DWORD"></span><span id="d3dfog_force_dword"></span>**D3DFOG \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="eb302-119"><span id="D3DFOG_FORCE_DWORD"></span><span id="d3dfog_force_dword"></span>**D3DFOG\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="eb302-120">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="eb302-120">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="eb302-121">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="eb302-121">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="eb302-122">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="eb302-122">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb302-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb302-123">Remarks</span></span>

<span data-ttu-id="eb302-124">Os valores neste tipo enumerado são usados pelos \_ Estados de RENDERIZAÇÃO D3DRS FOGTABLEMODE e \_ D3DRS FOGVERTEXMODE.</span><span class="sxs-lookup"><span data-stu-id="eb302-124">The values in this enumerated type are used by the D3DRS\_FOGTABLEMODE and D3DRS\_FOGVERTEXMODE render states.</span></span>

<span data-ttu-id="eb302-125">A neblina pode ser considerada uma medida de visibilidade: quanto menor o valor de neblina produzido por uma equação de neblina, menos visível é um objeto.</span><span class="sxs-lookup"><span data-stu-id="eb302-125">Fog can be considered a measure of visibility: the lower the fog value produced by a fog equation, the less visible an object is.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb302-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb302-126">Requirements</span></span>



| <span data-ttu-id="eb302-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb302-127">Requirement</span></span> | <span data-ttu-id="eb302-128">Valor</span><span class="sxs-lookup"><span data-stu-id="eb302-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb302-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eb302-129">Header</span></span><br/> | <dl> <span data-ttu-id="eb302-130"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb302-130"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb302-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb302-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb302-132">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="eb302-132">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="eb302-133">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="eb302-133">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
