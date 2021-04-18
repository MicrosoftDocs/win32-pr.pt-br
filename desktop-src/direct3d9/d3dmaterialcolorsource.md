---
description: Define o local no qual um componente de cor ou cor deve ser acessado para cálculos de iluminação.
ms.assetid: 76061d47-a31c-4008-aa8d-a0464dd3423f
title: Enumeração D3DMATERIALCOLORSOURCE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATERIALCOLORSOURCE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 8877eece8e33c6508768b22c989e992cf8178823
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793323"
---
# <a name="d3dmaterialcolorsource-enumeration"></a><span data-ttu-id="435bd-103">Enumeração D3DMATERIALCOLORSOURCE</span><span class="sxs-lookup"><span data-stu-id="435bd-103">D3DMATERIALCOLORSOURCE enumeration</span></span>

<span data-ttu-id="435bd-104">Define o local no qual um componente de cor ou cor deve ser acessado para cálculos de iluminação.</span><span class="sxs-lookup"><span data-stu-id="435bd-104">Defines the location at which a color or color component must be accessed for lighting calculations.</span></span>

## <a name="syntax"></a><span data-ttu-id="435bd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="435bd-105">Syntax</span></span>


```C++
typedef enum D3DMATERIALCOLORSOURCE { 
  D3DMCS_MATERIAL     = 0,
  D3DMCS_COLOR1       = 1,
  D3DMCS_COLOR2       = 2,
  D3DMCS_FORCE_DWORD  = 0x7fffffff
} D3DMATERIALCOLORSOURCE, *LPD3DMATERIALCOLORSOURCE;
```



## <a name="constants"></a><span data-ttu-id="435bd-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="435bd-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="435bd-107"><span id="D3DMCS_MATERIAL"></span><span id="d3dmcs_material"></span>**MATERIAL de D3DMCS \_**</span><span class="sxs-lookup"><span data-stu-id="435bd-107"><span id="D3DMCS_MATERIAL"></span><span id="d3dmcs_material"></span>**D3DMCS\_MATERIAL**</span></span>
</dt> <dd>

<span data-ttu-id="435bd-108">Use a cor do material atual.</span><span class="sxs-lookup"><span data-stu-id="435bd-108">Use the color from the current material.</span></span>

</dd> <dt>

<span data-ttu-id="435bd-109"><span id="D3DMCS_COLOR1"></span><span id="d3dmcs_color1"></span>**D3DMCS \_ COLOR1**</span><span class="sxs-lookup"><span data-stu-id="435bd-109"><span id="D3DMCS_COLOR1"></span><span id="d3dmcs_color1"></span>**D3DMCS\_COLOR1**</span></span>
</dt> <dd>

<span data-ttu-id="435bd-110">Use a cor do vértice difuso.</span><span class="sxs-lookup"><span data-stu-id="435bd-110">Use the diffuse vertex color.</span></span>

</dd> <dt>

<span data-ttu-id="435bd-111"><span id="D3DMCS_COLOR2"></span><span id="d3dmcs_color2"></span>**D3DMCS \_ COLOR2**</span><span class="sxs-lookup"><span data-stu-id="435bd-111"><span id="D3DMCS_COLOR2"></span><span id="d3dmcs_color2"></span>**D3DMCS\_COLOR2**</span></span>
</dt> <dd>

<span data-ttu-id="435bd-112">Use a cor do vértice especular.</span><span class="sxs-lookup"><span data-stu-id="435bd-112">Use the specular vertex color.</span></span>

</dd> <dt>

<span data-ttu-id="435bd-113"><span id="D3DMCS_FORCE_DWORD"></span><span id="d3dmcs_force_dword"></span>**D3DMCS \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="435bd-113"><span id="D3DMCS_FORCE_DWORD"></span><span id="d3dmcs_force_dword"></span>**D3DMCS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="435bd-114">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="435bd-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="435bd-115">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="435bd-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="435bd-116">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="435bd-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="435bd-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="435bd-117">Remarks</span></span>

<span data-ttu-id="435bd-118">Esses sinalizadores são usados para definir o valor dos seguintes Estados de renderização no tipo enumerado [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) .</span><span class="sxs-lookup"><span data-stu-id="435bd-118">These flags are used to set the value of the following render states in the [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) enumerated type.</span></span>

-   <span data-ttu-id="435bd-119">D3DRS \_ AMBIENTMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="435bd-119">D3DRS\_AMBIENTMATERIALSOURCE</span></span>
-   <span data-ttu-id="435bd-120">D3DRS \_ DiffuseMaterialSource</span><span class="sxs-lookup"><span data-stu-id="435bd-120">D3DRS\_DIFFUSEMATERIALSOURCE</span></span>
-   <span data-ttu-id="435bd-121">D3DRS \_ EMISSIVEMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="435bd-121">D3DRS\_EMISSIVEMATERIALSOURCE</span></span>
-   <span data-ttu-id="435bd-122">D3DRS \_ SPECULARMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="435bd-122">D3DRS\_SPECULARMATERIALSOURCE</span></span>

## <a name="requirements"></a><span data-ttu-id="435bd-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="435bd-123">Requirements</span></span>



| <span data-ttu-id="435bd-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="435bd-124">Requirement</span></span> | <span data-ttu-id="435bd-125">Valor</span><span class="sxs-lookup"><span data-stu-id="435bd-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="435bd-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="435bd-126">Header</span></span><br/> | <dl> <span data-ttu-id="435bd-127"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="435bd-127"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="435bd-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="435bd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="435bd-129">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="435bd-129">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="435bd-130">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="435bd-130">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
