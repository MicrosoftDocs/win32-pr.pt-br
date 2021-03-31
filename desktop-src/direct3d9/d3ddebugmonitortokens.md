---
description: Define os tokens do monitor de depuração.
ms.assetid: c0df4c9f-a232-45cf-b543-e95ee84a4a8d
title: Enumeração D3DDEBUGMONITORTOKENS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEBUGMONITORTOKENS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 82c3ecfa7d197e1ab912dbafe0d26fcb2281e605
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930558"
---
# <a name="d3ddebugmonitortokens-enumeration"></a><span data-ttu-id="366a6-103">Enumeração D3DDEBUGMONITORTOKENS</span><span class="sxs-lookup"><span data-stu-id="366a6-103">D3DDEBUGMONITORTOKENS enumeration</span></span>

<span data-ttu-id="366a6-104">Define os tokens do monitor de depuração.</span><span class="sxs-lookup"><span data-stu-id="366a6-104">Defines the debug monitor tokens.</span></span>

## <a name="syntax"></a><span data-ttu-id="366a6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="366a6-105">Syntax</span></span>


```C++
typedef enum D3DDEBUGMONITORTOKENS { 
  D3DDMT_ENABLE       = 0,
  D3DDMT_DISABLE      = 1,
  D3DDMT_FORCE_DWORD  = 0x7fffffff
} D3DDEBUGMONITORTOKENS, *LPD3DDEBUGMONITORTOKENS;
```



## <a name="constants"></a><span data-ttu-id="366a6-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="366a6-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="366a6-107"><span id="D3DDMT_ENABLE"></span><span id="d3ddmt_enable"></span>**D3DDMT \_ habilitar**</span><span class="sxs-lookup"><span data-stu-id="366a6-107"><span id="D3DDMT_ENABLE"></span><span id="d3ddmt_enable"></span>**D3DDMT\_ENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="366a6-108">Habilite o monitor de depuração.</span><span class="sxs-lookup"><span data-stu-id="366a6-108">Enable the debug monitor.</span></span>

</dd> <dt>

<span data-ttu-id="366a6-109"><span id="D3DDMT_DISABLE"></span><span id="d3ddmt_disable"></span>**D3DDMT \_ desabilitar**</span><span class="sxs-lookup"><span data-stu-id="366a6-109"><span id="D3DDMT_DISABLE"></span><span id="d3ddmt_disable"></span>**D3DDMT\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="366a6-110">Desabilite o monitor de depuração.</span><span class="sxs-lookup"><span data-stu-id="366a6-110">Disable the debug monitor.</span></span>

</dd> <dt>

<span data-ttu-id="366a6-111"><span id="D3DDMT_FORCE_DWORD"></span><span id="d3ddmt_force_dword"></span>**D3DDMT \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="366a6-111"><span id="D3DDMT_FORCE_DWORD"></span><span id="d3ddmt_force_dword"></span>**D3DDMT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="366a6-112">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="366a6-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="366a6-113">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="366a6-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="366a6-114">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="366a6-114">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="366a6-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="366a6-115">Remarks</span></span>

<span data-ttu-id="366a6-116">Os valores nesse tipo enumerado são usados pelo \_ estado de RENDERIZAÇÃO D3DRS DEBUGMONITORTOKEN e são relevantes apenas para compilações de depuração.</span><span class="sxs-lookup"><span data-stu-id="366a6-116">The values in this enumerated type are used by the D3DRS\_DEBUGMONITORTOKEN render state and are only relevant for debug builds.</span></span>

## <a name="requirements"></a><span data-ttu-id="366a6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="366a6-117">Requirements</span></span>



| <span data-ttu-id="366a6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="366a6-118">Requirement</span></span> | <span data-ttu-id="366a6-119">Valor</span><span class="sxs-lookup"><span data-stu-id="366a6-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="366a6-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="366a6-120">Header</span></span><br/> | <dl> <span data-ttu-id="366a6-121"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="366a6-121"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="366a6-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="366a6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="366a6-123">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="366a6-123">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="366a6-124">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="366a6-124">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
