---
description: Define o tipo de animação conjunto de modos de loop usados para reprodução.
ms.assetid: 2ce26bf0-2b33-4193-a58f-03493a051351
title: Enumeração de D3DXPLAYBACK_TYPE (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPLAYBACK_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 0ce95b4765ec678c43c8e0ed92008deeb9927298
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837929"
---
# <a name="d3dxplayback_type-enumeration"></a><span data-ttu-id="242b0-103">\_Enumeração de tipo D3DXPLAYBACK</span><span class="sxs-lookup"><span data-stu-id="242b0-103">D3DXPLAYBACK\_TYPE enumeration</span></span>

<span data-ttu-id="242b0-104">Define o tipo de animação conjunto de modos de loop usados para reprodução.</span><span class="sxs-lookup"><span data-stu-id="242b0-104">Defines the type of animation set looping modes used for playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="242b0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="242b0-105">Syntax</span></span>


```C++
typedef enum D3DXPLAYBACK_TYPE { 
  D3DXPLAY_LOOP         = 0,
  D3DXPLAY_ONCE         = 1,
  D3DXPLAY_PINGPONG     = 2,
  D3DXPLAY_FORCE_DWORD  = 0x7fffffff
} D3DXPLAYBACK_TYPE, *LPD3DXPLAYBACK_TYPE;
```



## <a name="constants"></a><span data-ttu-id="242b0-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="242b0-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="242b0-107"><span id="D3DXPLAY_LOOP"></span><span id="d3dxplay_loop"></span>**\_Loop D3DXPLAY**</span><span class="sxs-lookup"><span data-stu-id="242b0-107"><span id="D3DXPLAY_LOOP"></span><span id="d3dxplay_loop"></span>**D3DXPLAY\_LOOP**</span></span>
</dt> <dd>

<span data-ttu-id="242b0-108">A animação se repete inparadamente.</span><span class="sxs-lookup"><span data-stu-id="242b0-108">The animation repeats endlessly.</span></span>

</dd> <dt>

<span data-ttu-id="242b0-109"><span id="D3DXPLAY_ONCE"></span><span id="d3dxplay_once"></span>**D3DXPLAY \_ uma vez**</span><span class="sxs-lookup"><span data-stu-id="242b0-109"><span id="D3DXPLAY_ONCE"></span><span id="d3dxplay_once"></span>**D3DXPLAY\_ONCE**</span></span>
</dt> <dd>

<span data-ttu-id="242b0-110">A animação é reproduzida uma vez e, em seguida, é interrompida no último quadro.</span><span class="sxs-lookup"><span data-stu-id="242b0-110">The animation plays once, and then it stops on the last frame.</span></span>

</dd> <dt>

<span data-ttu-id="242b0-111"><span id="D3DXPLAY_PINGPONG"></span><span id="d3dxplay_pingpong"></span>**D3DXPLAY \_ PINGPONG**</span><span class="sxs-lookup"><span data-stu-id="242b0-111"><span id="D3DXPLAY_PINGPONG"></span><span id="d3dxplay_pingpong"></span>**D3DXPLAY\_PINGPONG**</span></span>
</dt> <dd>

<span data-ttu-id="242b0-112">A animação alterna perversamente entre a reprodução e a reprodução.</span><span class="sxs-lookup"><span data-stu-id="242b0-112">The animation alternates endlessly between playing forward and playing backward.</span></span>

</dd> <dt>

<span data-ttu-id="242b0-113"><span id="D3DXPLAY_FORCE_DWORD"></span><span id="d3dxplay_force_dword"></span>**D3DXPLAY \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="242b0-113"><span id="D3DXPLAY_FORCE_DWORD"></span><span id="d3dxplay_force_dword"></span>**D3DXPLAY\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="242b0-114">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="242b0-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="242b0-115">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="242b0-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="242b0-116">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="242b0-116">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="242b0-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="242b0-117">Requirements</span></span>



| <span data-ttu-id="242b0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="242b0-118">Requirement</span></span> | <span data-ttu-id="242b0-119">Valor</span><span class="sxs-lookup"><span data-stu-id="242b0-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="242b0-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="242b0-120">Header</span></span><br/> | <dl> <span data-ttu-id="242b0-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="242b0-121"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="242b0-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="242b0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="242b0-123">Enumerações D3DX</span><span class="sxs-lookup"><span data-stu-id="242b0-123">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




