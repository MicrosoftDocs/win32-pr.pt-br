---
description: Define constantes que descrevem os formatos de buffer de profundidade.
ms.assetid: 5e5ce48b-8859-43e0-a9b4-5972cf6bf781
title: Enumeração D3DZBUFFERTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DZBUFFERTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 271a278f48c10a89fa6f552c3e1a7b4a83f274f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105815600"
---
# <a name="d3dzbuffertype-enumeration"></a><span data-ttu-id="57563-103">Enumeração D3DZBUFFERTYPE</span><span class="sxs-lookup"><span data-stu-id="57563-103">D3DZBUFFERTYPE enumeration</span></span>

<span data-ttu-id="57563-104">Define constantes que descrevem os formatos de buffer de profundidade.</span><span class="sxs-lookup"><span data-stu-id="57563-104">Defines constants that describe depth-buffer formats.</span></span>

## <a name="syntax"></a><span data-ttu-id="57563-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="57563-105">Syntax</span></span>


```C++
typedef enum D3DZBUFFERTYPE { 
  D3DZB_FALSE        = 0,
  D3DZB_TRUE         = 1,
  D3DZB_USEW         = 2,
  D3DZB_FORCE_DWORD  = 0x7fffffff
} D3DZBUFFERTYPE, *LPD3DZBUFFERTYPE;
```



## <a name="constants"></a><span data-ttu-id="57563-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="57563-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="57563-107"><span id="D3DZB_FALSE"></span><span id="d3dzb_false"></span>**D3DZB \_ false**</span><span class="sxs-lookup"><span data-stu-id="57563-107"><span id="D3DZB_FALSE"></span><span id="d3dzb_false"></span>**D3DZB\_FALSE**</span></span>
</dt> <dd>

<span data-ttu-id="57563-108">Desabilite o buffer de profundidade.</span><span class="sxs-lookup"><span data-stu-id="57563-108">Disable depth buffering.</span></span>

</dd> <dt>

<span data-ttu-id="57563-109"><span id="D3DZB_TRUE"></span><span id="d3dzb_true"></span>**D3DZB \_ true**</span><span class="sxs-lookup"><span data-stu-id="57563-109"><span id="D3DZB_TRUE"></span><span id="d3dzb_true"></span>**D3DZB\_TRUE**</span></span>
</dt> <dd>

<span data-ttu-id="57563-110">Habilite o z-buffering.</span><span class="sxs-lookup"><span data-stu-id="57563-110">Enable z-buffering.</span></span>

</dd> <dt>

<span data-ttu-id="57563-111"><span id="D3DZB_USEW"></span><span id="d3dzb_usew"></span>**D3DZB \_ USEW**</span><span class="sxs-lookup"><span data-stu-id="57563-111"><span id="D3DZB_USEW"></span><span id="d3dzb_usew"></span>**D3DZB\_USEW**</span></span>
</dt> <dd>

<span data-ttu-id="57563-112">Habilite o w-buffer.</span><span class="sxs-lookup"><span data-stu-id="57563-112">Enable w-buffering.</span></span>

</dd> <dt>

<span data-ttu-id="57563-113"><span id="D3DZB_FORCE_DWORD"></span><span id="d3dzb_force_dword"></span>**D3DZB \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="57563-113"><span id="D3DZB_FORCE_DWORD"></span><span id="d3dzb_force_dword"></span>**D3DZB\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="57563-114">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="57563-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="57563-115">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="57563-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="57563-116">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="57563-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="57563-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="57563-117">Remarks</span></span>

<span data-ttu-id="57563-118">Os membros desse tipo enumerado são usados com o \_ estado de RENDERIZAÇÃO D3DRS ZENABLE.</span><span class="sxs-lookup"><span data-stu-id="57563-118">Members of this enumerated type are used with the D3DRS\_ZENABLE render state.</span></span>

## <a name="requirements"></a><span data-ttu-id="57563-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57563-119">Requirements</span></span>



| <span data-ttu-id="57563-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="57563-120">Requirement</span></span> | <span data-ttu-id="57563-121">Valor</span><span class="sxs-lookup"><span data-stu-id="57563-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="57563-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="57563-122">Header</span></span><br/> | <dl> <span data-ttu-id="57563-123"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="57563-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57563-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="57563-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57563-125">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="57563-125">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="57563-126">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="57563-126">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
