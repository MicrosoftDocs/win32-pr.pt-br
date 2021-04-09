---
description: Sinalizadores usados para obter informações de retorno de chamada.
ms.assetid: e8126ff0-db23-4da6-a999-0efb8c2647da
title: Enumeração de D3DXCALLBACK_SEARCH_FLAGS (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCALLBACK_SEARCH_FLAGS
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: d3302b79734557a5c1f2082ec2a4e95c03790f4a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012112"
---
# <a name="d3dxcallback_search_flags-enumeration"></a><span data-ttu-id="06a0d-103">Enumeração de sinalizadores de \_ pesquisa do D3DXCALLBACK \_</span><span class="sxs-lookup"><span data-stu-id="06a0d-103">D3DXCALLBACK\_SEARCH\_FLAGS enumeration</span></span>

<span data-ttu-id="06a0d-104">Sinalizadores usados para obter informações de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="06a0d-104">Flags used to obtain callback information.</span></span>

## <a name="syntax"></a><span data-ttu-id="06a0d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="06a0d-105">Syntax</span></span>


```C++
typedef enum D3DXCALLBACK_SEARCH_FLAGS { 
  D3DXCALLBACK_SEARCH_EXCLUDING_INITIAL_POSITION  = 1,
  D3DXCALLBACK_SEARCH_BEHIND_INITIAL_POSITION     = 2,
  D3DXCALLBACK_SEARCH_FORCE_DWORD                 = 0x7fffffff
} D3DXCALLBACK_SEARCH_FLAGS, *LPD3DXCALLBACK_SEARCH_FLAGS;
```



## <a name="constants"></a><span data-ttu-id="06a0d-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="06a0d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="06a0d-107"><span id="D3DXCALLBACK_SEARCH_EXCLUDING_INITIAL_POSITION"></span><span id="d3dxcallback_search_excluding_initial_position"></span>**Pesquisa do D3DXCALLBACK \_ \_ excluindo a \_ \_ posição inicial**</span><span class="sxs-lookup"><span data-stu-id="06a0d-107"><span id="D3DXCALLBACK_SEARCH_EXCLUDING_INITIAL_POSITION"></span><span id="d3dxcallback_search_excluding_initial_position"></span>**D3DXCALLBACK\_SEARCH\_EXCLUDING\_INITIAL\_POSITION**</span></span>
</dt> <dd>

<span data-ttu-id="06a0d-108">Exclua os retornos de chamada localizados na posição inicial da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="06a0d-108">Exclude callbacks located at the initial position from the search.</span></span>

</dd> <dt>

<span data-ttu-id="06a0d-109"><span id="D3DXCALLBACK_SEARCH_BEHIND_INITIAL_POSITION"></span><span id="d3dxcallback_search_behind_initial_position"></span>**D3DXCALLBACK \_ pesquisa \_ por trás da \_ \_ posição inicial**</span><span class="sxs-lookup"><span data-stu-id="06a0d-109"><span id="D3DXCALLBACK_SEARCH_BEHIND_INITIAL_POSITION"></span><span id="d3dxcallback_search_behind_initial_position"></span>**D3DXCALLBACK\_SEARCH\_BEHIND\_INITIAL\_POSITION**</span></span>
</dt> <dd>

<span data-ttu-id="06a0d-110">Inverta a direção da pesquisa de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="06a0d-110">Reverse the callback search direction.</span></span>

</dd> <dt>

<span data-ttu-id="06a0d-111"><span id="D3DXCALLBACK_SEARCH_FORCE_DWORD"></span><span id="d3dxcallback_search_force_dword"></span>**\_DWORD de \_ forçar \_ pesquisa D3DXCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="06a0d-111"><span id="D3DXCALLBACK_SEARCH_FORCE_DWORD"></span><span id="d3dxcallback_search_force_dword"></span>**D3DXCALLBACK\_SEARCH\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="06a0d-112">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="06a0d-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="06a0d-113">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="06a0d-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="06a0d-114">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="06a0d-114">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="06a0d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06a0d-115">Requirements</span></span>



| <span data-ttu-id="06a0d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="06a0d-116">Requirement</span></span> | <span data-ttu-id="06a0d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="06a0d-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="06a0d-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="06a0d-118">Header</span></span><br/> | <dl> <span data-ttu-id="06a0d-119"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="06a0d-119"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06a0d-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="06a0d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06a0d-121">Enumerações D3DX</span><span class="sxs-lookup"><span data-stu-id="06a0d-121">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




