---
description: Define se o modo de mosaico atual é discreto ou contínuo.
ms.assetid: d8055a25-6a8e-4018-a993-762f6f0e0cd3
title: Enumeração D3DPATCHEDGESTYLE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPATCHEDGESTYLE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e625b7c4ff12f9859efdcc2b10b551a2223adab6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837945"
---
# <a name="d3dpatchedgestyle-enumeration"></a><span data-ttu-id="fb66c-103">Enumeração D3DPATCHEDGESTYLE</span><span class="sxs-lookup"><span data-stu-id="fb66c-103">D3DPATCHEDGESTYLE enumeration</span></span>

<span data-ttu-id="fb66c-104">Define se o modo de mosaico atual é discreto ou contínuo.</span><span class="sxs-lookup"><span data-stu-id="fb66c-104">Defines whether the current tessellation mode is discrete or continuous.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb66c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb66c-105">Syntax</span></span>


```C++
typedef enum D3DPATCHEDGESTYLE { 
  D3DPATCHEDGE_DISCRETE     = 0,
  D3DPATCHEDGE_CONTINUOUS   = 1,
  D3DPATCHEDGE_FORCE_DWORD  = 0x7fffffff
} D3DPATCHEDGESTYLE, *LPD3DPATCHEDGESTYLE;
```



## <a name="constants"></a><span data-ttu-id="fb66c-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="fb66c-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fb66c-107"><span id="D3DPATCHEDGE_DISCRETE"></span><span id="d3dpatchedge_discrete"></span>**D3DPATCHEDGE \_ discreto**</span><span class="sxs-lookup"><span data-stu-id="fb66c-107"><span id="D3DPATCHEDGE_DISCRETE"></span><span id="d3dpatchedge_discrete"></span>**D3DPATCHEDGE\_DISCRETE**</span></span>
</dt> <dd>

<span data-ttu-id="fb66c-108">Estilo de borda discreto.</span><span class="sxs-lookup"><span data-stu-id="fb66c-108">Discrete edge style.</span></span> <span data-ttu-id="fb66c-109">No modo discreto, você pode especificar o mosaico flutuante, mas ele será truncado para inteiros.</span><span class="sxs-lookup"><span data-stu-id="fb66c-109">In discrete mode, you can specify float tessellation but it will be truncated to integers.</span></span>

</dd> <dt>

<span data-ttu-id="fb66c-110"><span id="D3DPATCHEDGE_CONTINUOUS"></span><span id="d3dpatchedge_continuous"></span>**D3DPATCHEDGE \_ contínuo**</span><span class="sxs-lookup"><span data-stu-id="fb66c-110"><span id="D3DPATCHEDGE_CONTINUOUS"></span><span id="d3dpatchedge_continuous"></span>**D3DPATCHEDGE\_CONTINUOUS**</span></span>
</dt> <dd>

<span data-ttu-id="fb66c-111">Estilo de borda contínua.</span><span class="sxs-lookup"><span data-stu-id="fb66c-111">Continuous edge style.</span></span> <span data-ttu-id="fb66c-112">No modo contínuo, o mosaico é especificado como valores float que podem ser tranqüilamente variados para reduzir os artefatos "pop-los".</span><span class="sxs-lookup"><span data-stu-id="fb66c-112">In continuous mode, tessellation is specified as float values that can be smoothly varied to reduce "popping" artifacts.</span></span>

</dd> <dt>

<span data-ttu-id="fb66c-113"><span id="D3DPATCHEDGE_FORCE_DWORD"></span><span id="d3dpatchedge_force_dword"></span>**D3DPATCHEDGE \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fb66c-113"><span id="D3DPATCHEDGE_FORCE_DWORD"></span><span id="d3dpatchedge_force_dword"></span>**D3DPATCHEDGE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="fb66c-114">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="fb66c-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="fb66c-115">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="fb66c-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="fb66c-116">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="fb66c-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fb66c-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb66c-117">Remarks</span></span>

<span data-ttu-id="fb66c-118">Observe que o mosaico contínuo produz um padrão de mosaico completamente diferente do discreto para os mesmos valores de mosaico (isso é mais aparente no modo de wireframe).</span><span class="sxs-lookup"><span data-stu-id="fb66c-118">Note that continuous tessellation produces a completely different tessellation pattern from the discrete one for the same tessellation values (this is more apparent in wireframe mode).</span></span> <span data-ttu-id="fb66c-119">Portanto, 4,0 contínuo não é o mesmo que 4 discretos.</span><span class="sxs-lookup"><span data-stu-id="fb66c-119">Thus, 4.0 continuous is not the same as 4 discrete.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb66c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb66c-120">Requirements</span></span>



| <span data-ttu-id="fb66c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb66c-121">Requirement</span></span> | <span data-ttu-id="fb66c-122">Valor</span><span class="sxs-lookup"><span data-stu-id="fb66c-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb66c-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fb66c-123">Header</span></span><br/> | <dl> <span data-ttu-id="fb66c-124"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb66c-124"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb66c-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb66c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb66c-126">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="fb66c-126">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




