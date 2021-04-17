---
description: Define o modo de compactação usado para armazenar dados de conjunto de animação compactados.
ms.assetid: 41592b71-52ba-4727-a885-fb10fc23c5f8
title: Enumeração de D3DXCOMPRESSION_FLAGS (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCOMPRESSION_FLAGS
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 6f912c44659d418d543194ba82a9d82f31e7ef08
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105762515"
---
# <a name="d3dxcompression_flags-enumeration"></a><span data-ttu-id="8c568-103">\_Enumeração de sinalizadores D3DXCOMPRESSION</span><span class="sxs-lookup"><span data-stu-id="8c568-103">D3DXCOMPRESSION\_FLAGS enumeration</span></span>

<span data-ttu-id="8c568-104">Define o modo de compactação usado para armazenar dados de conjunto de animação compactados.</span><span class="sxs-lookup"><span data-stu-id="8c568-104">Defines the compression mode used for storing compressed animation set data.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c568-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8c568-105">Syntax</span></span>


```C++
typedef enum D3DXCOMPRESSION_FLAGS { 
  D3DXCOMPRESS_DEFAULT      = 0,
  D3DXCOMPRESS_STRONG       = 1,
  D3DXCOMPRESS_FORCE_DWORD  = 0x7fffffff
} D3DXCOMPRESSION_FLAGS, *LPD3DXCOMPRESSION_FLAGS;
```



## <a name="constants"></a><span data-ttu-id="8c568-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="8c568-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8c568-107"><span id="D3DXCOMPRESS_DEFAULT"></span><span id="d3dxcompress_default"></span>**D3DXCOMPRESS \_ padrão**</span><span class="sxs-lookup"><span data-stu-id="8c568-107"><span id="D3DXCOMPRESS_DEFAULT"></span><span id="d3dxcompress_default"></span>**D3DXCOMPRESS\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="8c568-108">Implementa a compactação rápida.</span><span class="sxs-lookup"><span data-stu-id="8c568-108">Implements fast compression.</span></span>

</dd> <dt>

<span data-ttu-id="8c568-109"><span id="D3DXCOMPRESS_STRONG"></span><span id="d3dxcompress_strong"></span>**D3DXCOMPRESS \_ Strong**</span><span class="sxs-lookup"><span data-stu-id="8c568-109"><span id="D3DXCOMPRESS_STRONG"></span><span id="d3dxcompress_strong"></span>**D3DXCOMPRESS\_STRONG**</span></span>
</dt> <dd>

<span data-ttu-id="8c568-110">Implementa a compactação lenta.</span><span class="sxs-lookup"><span data-stu-id="8c568-110">Implements slow compression.</span></span> <span data-ttu-id="8c568-111">Normalmente resulta em um conjunto de animação melhor com qualidade compactada do que se D3DXCOMPRESS \_ padrão for usado.</span><span class="sxs-lookup"><span data-stu-id="8c568-111">Typically results in a better quality compressed animation set than if D3DXCOMPRESS\_DEFAULT is used.</span></span>

</dd> <dt>

<span data-ttu-id="8c568-112"><span id="D3DXCOMPRESS_FORCE_DWORD"></span><span id="d3dxcompress_force_dword"></span>**D3DXCOMPRESS \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="8c568-112"><span id="D3DXCOMPRESS_FORCE_DWORD"></span><span id="d3dxcompress_force_dword"></span>**D3DXCOMPRESS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="8c568-113">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="8c568-113">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="8c568-114">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="8c568-114">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="8c568-115">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="8c568-115">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8c568-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c568-116">Requirements</span></span>



| <span data-ttu-id="8c568-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c568-117">Requirement</span></span> | <span data-ttu-id="8c568-118">Valor</span><span class="sxs-lookup"><span data-stu-id="8c568-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c568-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8c568-119">Header</span></span><br/> | <dl> <span data-ttu-id="8c568-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c568-120"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c568-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c568-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c568-122">Enumerações D3DX</span><span class="sxs-lookup"><span data-stu-id="8c568-122">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




