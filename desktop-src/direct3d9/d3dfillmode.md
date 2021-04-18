---
description: Define constantes que descrevem o modo de preenchimento.
ms.assetid: be835432-e8d5-4afb-a810-2dac25bdc9dc
title: Enumeração D3DFILLMODE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DFILLMODE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 33cf03258933055aa18aecb42fffe4d8f33b1e51
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105760659"
---
# <a name="d3dfillmode-enumeration"></a><span data-ttu-id="f2f1a-103">Enumeração D3DFILLMODE</span><span class="sxs-lookup"><span data-stu-id="f2f1a-103">D3DFILLMODE enumeration</span></span>

<span data-ttu-id="f2f1a-104">Define constantes que descrevem o modo de preenchimento.</span><span class="sxs-lookup"><span data-stu-id="f2f1a-104">Defines constants describing the fill mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2f1a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2f1a-105">Syntax</span></span>


```C++
typedef enum D3DFILLMODE { 
  D3DFILL_POINT        = 1,
  D3DFILL_WIREFRAME    = 2,
  D3DFILL_SOLID        = 3,
  D3DFILL_FORCE_DWORD  = 0x7fffffff
} D3DFILLMODE, *LPD3DFILLMODE;
```



## <a name="constants"></a><span data-ttu-id="f2f1a-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="f2f1a-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f2f1a-107"><span id="D3DFILL_POINT"></span><span id="d3dfill_point"></span>**Ponto de D3DFILL \_**</span><span class="sxs-lookup"><span data-stu-id="f2f1a-107"><span id="D3DFILL_POINT"></span><span id="d3dfill_point"></span>**D3DFILL\_POINT**</span></span>
</dt> <dd>

<span data-ttu-id="f2f1a-108">Pontos de preenchimento.</span><span class="sxs-lookup"><span data-stu-id="f2f1a-108">Fill points.</span></span>

</dd> <dt>

<span data-ttu-id="f2f1a-109"><span id="D3DFILL_WIREFRAME"></span><span id="d3dfill_wireframe"></span>**\_WIREFRAME D3DFILL**</span><span class="sxs-lookup"><span data-stu-id="f2f1a-109"><span id="D3DFILL_WIREFRAME"></span><span id="d3dfill_wireframe"></span>**D3DFILL\_WIREFRAME**</span></span>
</dt> <dd>

<span data-ttu-id="f2f1a-110">Preencha os wireframes.</span><span class="sxs-lookup"><span data-stu-id="f2f1a-110">Fill wireframes.</span></span>

</dd> <dt>

<span data-ttu-id="f2f1a-111"><span id="D3DFILL_SOLID"></span><span id="d3dfill_solid"></span>**D3DFILL \_ sólido**</span><span class="sxs-lookup"><span data-stu-id="f2f1a-111"><span id="D3DFILL_SOLID"></span><span id="d3dfill_solid"></span>**D3DFILL\_SOLID**</span></span>
</dt> <dd>

<span data-ttu-id="f2f1a-112">Preencha os sólidos.</span><span class="sxs-lookup"><span data-stu-id="f2f1a-112">Fill solids.</span></span>

</dd> <dt>

<span data-ttu-id="f2f1a-113"><span id="D3DFILL_FORCE_DWORD"></span><span id="d3dfill_force_dword"></span>**D3DFILL \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f2f1a-113"><span id="D3DFILL_FORCE_DWORD"></span><span id="d3dfill_force_dword"></span>**D3DFILL\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="f2f1a-114">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="f2f1a-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="f2f1a-115">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="f2f1a-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="f2f1a-116">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="f2f1a-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f2f1a-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2f1a-117">Remarks</span></span>

<span data-ttu-id="f2f1a-118">Os valores neste tipo enumerado são usados pelo \_ estado de RENDERIZAÇÃO D3DRS FillMode.</span><span class="sxs-lookup"><span data-stu-id="f2f1a-118">The values in this enumerated type are used by the D3DRS\_FILLMODE render state.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2f1a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2f1a-119">Requirements</span></span>



| <span data-ttu-id="f2f1a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2f1a-120">Requirement</span></span> | <span data-ttu-id="f2f1a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="f2f1a-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2f1a-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f2f1a-122">Header</span></span><br/> | <dl> <span data-ttu-id="f2f1a-123"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2f1a-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2f1a-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2f1a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2f1a-125">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="f2f1a-125">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="f2f1a-126">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="f2f1a-126">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
