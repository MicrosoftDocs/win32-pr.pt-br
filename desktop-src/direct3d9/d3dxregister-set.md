---
description: Tipo de dados do registro.
ms.assetid: b54530d3-4267-4b41-9a16-59d400ef3e18
title: Enumeração de D3DXREGISTER_SET (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXREGISTER_SET
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 683b13d0b386fcdbc162293455e2beb11bc1ee85
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105814093"
---
# <a name="d3dxregister_set-enumeration"></a><span data-ttu-id="fbd0a-103">Enumeração de conjunto de D3DXREGISTER \_</span><span class="sxs-lookup"><span data-stu-id="fbd0a-103">D3DXREGISTER\_SET enumeration</span></span>

<span data-ttu-id="fbd0a-104">Tipo de dados do registro.</span><span class="sxs-lookup"><span data-stu-id="fbd0a-104">Data type of the register.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbd0a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbd0a-105">Syntax</span></span>


```C++
typedef enum _D3DXREGISTER_SET { 
  D3DXRS_BOOL,
  D3DXRS_INT4,
  D3DXRS_FLOAT4,
  D3DXRS_SAMPLER,
  D3DXRS_FORCE_DWORD  = 0x7fffffff
} D3DXREGISTER_SET, *LPD3DXREGISTER_SET;
```



## <a name="constants"></a><span data-ttu-id="fbd0a-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="fbd0a-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fbd0a-107"><span id="D3DXRS_BOOL"></span><span id="d3dxrs_bool"></span>**\_Bool D3DXRS**</span><span class="sxs-lookup"><span data-stu-id="fbd0a-107"><span id="D3DXRS_BOOL"></span><span id="d3dxrs_bool"></span>**D3DXRS\_BOOL**</span></span>
</dt> <dd>

<span data-ttu-id="fbd0a-108">$True.</span><span class="sxs-lookup"><span data-stu-id="fbd0a-108">Boolean value.</span></span>

</dd> <dt>

<span data-ttu-id="fbd0a-109"><span id="D3DXRS_INT4"></span><span id="d3dxrs_int4"></span>**D3DXRS \_ INT4**</span><span class="sxs-lookup"><span data-stu-id="fbd0a-109"><span id="D3DXRS_INT4"></span><span id="d3dxrs_int4"></span>**D3DXRS\_INT4**</span></span>
</dt> <dd>

<span data-ttu-id="fbd0a-110">número inteiro de 4D.</span><span class="sxs-lookup"><span data-stu-id="fbd0a-110">4D integer number.</span></span>

</dd> <dt>

<span data-ttu-id="fbd0a-111"><span id="D3DXRS_FLOAT4"></span><span id="d3dxrs_float4"></span>**D3DXRS \_ FLOAT4**</span><span class="sxs-lookup"><span data-stu-id="fbd0a-111"><span id="D3DXRS_FLOAT4"></span><span id="d3dxrs_float4"></span>**D3DXRS\_FLOAT4**</span></span>
</dt> <dd>

<span data-ttu-id="fbd0a-112">número de ponto flutuante de 4D.</span><span class="sxs-lookup"><span data-stu-id="fbd0a-112">4D floating-point number.</span></span>

</dd> <dt>

<span data-ttu-id="fbd0a-113"><span id="D3DXRS_SAMPLER"></span><span id="d3dxrs_sampler"></span>**Amostra de D3DXRS \_**</span><span class="sxs-lookup"><span data-stu-id="fbd0a-113"><span id="D3DXRS_SAMPLER"></span><span id="d3dxrs_sampler"></span>**D3DXRS\_SAMPLER**</span></span>
</dt> <dd>

<span data-ttu-id="fbd0a-114">O registro contém dados de amostra de 4D.</span><span class="sxs-lookup"><span data-stu-id="fbd0a-114">The register contains 4D sampler data.</span></span>

</dd> <dt>

<span data-ttu-id="fbd0a-115"><span id="D3DXRS_FORCE_DWORD"></span><span id="d3dxrs_force_dword"></span>**D3DXRS \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fbd0a-115"><span id="D3DXRS_FORCE_DWORD"></span><span id="d3dxrs_force_dword"></span>**D3DXRS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="fbd0a-116">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="fbd0a-116">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="fbd0a-117">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="fbd0a-117">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="fbd0a-118">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="fbd0a-118">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fbd0a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbd0a-119">Requirements</span></span>



| <span data-ttu-id="fbd0a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbd0a-120">Requirement</span></span> | <span data-ttu-id="fbd0a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="fbd0a-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbd0a-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fbd0a-122">Header</span></span><br/> | <dl> <span data-ttu-id="fbd0a-123"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbd0a-123"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbd0a-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="fbd0a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbd0a-125">Enumerações D3DX</span><span class="sxs-lookup"><span data-stu-id="fbd0a-125">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="fbd0a-126">**D3DXSHADER \_ CONSTANTINFO**</span><span class="sxs-lookup"><span data-stu-id="fbd0a-126">**D3DXSHADER\_CONSTANTINFO**</span></span>](d3dxshader-constantinfo.md)
</dt> <dt>

[<span data-ttu-id="fbd0a-127">**D3DXCONSTANT \_ desc**</span><span class="sxs-lookup"><span data-stu-id="fbd0a-127">**D3DXCONSTANT\_DESC**</span></span>](d3dxconstant-desc.md)
</dt> </dl>

 

 




