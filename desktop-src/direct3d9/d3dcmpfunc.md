---
description: Define as funções de comparação com suporte.
ms.assetid: 999af3eb-a208-4312-acee-373192ea69e4
title: Enumeração D3DCMPFUNC (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCMPFUNC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e49f0e058e795e00349020619f1e6d6310dfd94f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837925"
---
# <a name="d3dcmpfunc-enumeration"></a><span data-ttu-id="7be09-103">Enumeração D3DCMPFUNC</span><span class="sxs-lookup"><span data-stu-id="7be09-103">D3DCMPFUNC enumeration</span></span>

<span data-ttu-id="7be09-104">Define as funções de comparação com suporte.</span><span class="sxs-lookup"><span data-stu-id="7be09-104">Defines the supported compare functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="7be09-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7be09-105">Syntax</span></span>


```C++
typedef enum D3DCMPFUNC { 
  D3DCMP_NEVER         = 1,
  D3DCMP_LESS          = 2,
  D3DCMP_EQUAL         = 3,
  D3DCMP_LESSEQUAL     = 4,
  D3DCMP_GREATER       = 5,
  D3DCMP_NOTEQUAL      = 6,
  D3DCMP_GREATEREQUAL  = 7,
  D3DCMP_ALWAYS        = 8,
  D3DCMP_FORCE_DWORD   = 0x7fffffff
} D3DCMPFUNC, *LPD3DCMPFUNC;
```



## <a name="constants"></a><span data-ttu-id="7be09-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="7be09-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7be09-107"><span id="D3DCMP_NEVER"></span><span id="d3dcmp_never"></span>**D3DCMP \_ nunca**</span><span class="sxs-lookup"><span data-stu-id="7be09-107"><span id="D3DCMP_NEVER"></span><span id="d3dcmp_never"></span>**D3DCMP\_NEVER**</span></span>
</dt> <dd>

<span data-ttu-id="7be09-108">Sempre falha no teste.</span><span class="sxs-lookup"><span data-stu-id="7be09-108">Always fail the test.</span></span>

</dd> <dt>

<span data-ttu-id="7be09-109"><span id="D3DCMP_LESS"></span><span id="d3dcmp_less"></span>**D3DCMP \_ menos**</span><span class="sxs-lookup"><span data-stu-id="7be09-109"><span id="D3DCMP_LESS"></span><span id="d3dcmp_less"></span>**D3DCMP\_LESS**</span></span>
</dt> <dd>

<span data-ttu-id="7be09-110">Aceite o novo pixel se seu valor for menor que o valor do pixel atual.</span><span class="sxs-lookup"><span data-stu-id="7be09-110">Accept the new pixel if its value is less than the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="7be09-111"><span id="D3DCMP_EQUAL"></span><span id="d3dcmp_equal"></span>**D3DCMP \_ igual**</span><span class="sxs-lookup"><span data-stu-id="7be09-111"><span id="D3DCMP_EQUAL"></span><span id="d3dcmp_equal"></span>**D3DCMP\_EQUAL**</span></span>
</dt> <dd>

<span data-ttu-id="7be09-112">Aceite o novo pixel se seu valor for igual ao valor do pixel atual.</span><span class="sxs-lookup"><span data-stu-id="7be09-112">Accept the new pixel if its value equals the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="7be09-113"><span id="D3DCMP_LESSEQUAL"></span><span id="d3dcmp_lessequal"></span>**D3DCMP \_ LESSEQUAL**</span><span class="sxs-lookup"><span data-stu-id="7be09-113"><span id="D3DCMP_LESSEQUAL"></span><span id="d3dcmp_lessequal"></span>**D3DCMP\_LESSEQUAL**</span></span>
</dt> <dd>

<span data-ttu-id="7be09-114">Aceite o novo pixel se seu valor for menor ou igual ao valor do pixel atual.</span><span class="sxs-lookup"><span data-stu-id="7be09-114">Accept the new pixel if its value is less than or equal to the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="7be09-115"><span id="D3DCMP_GREATER"></span><span id="d3dcmp_greater"></span>**D3DCMP \_ maior**</span><span class="sxs-lookup"><span data-stu-id="7be09-115"><span id="D3DCMP_GREATER"></span><span id="d3dcmp_greater"></span>**D3DCMP\_GREATER**</span></span>
</dt> <dd>

<span data-ttu-id="7be09-116">Aceite o novo pixel se seu valor for maior que o valor do pixel atual.</span><span class="sxs-lookup"><span data-stu-id="7be09-116">Accept the new pixel if its value is greater than the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="7be09-117"><span id="D3DCMP_NOTEQUAL"></span><span id="d3dcmp_notequal"></span>**D3DCMP não \_ igual a**</span><span class="sxs-lookup"><span data-stu-id="7be09-117"><span id="D3DCMP_NOTEQUAL"></span><span id="d3dcmp_notequal"></span>**D3DCMP\_NOTEQUAL**</span></span>
</dt> <dd>

<span data-ttu-id="7be09-118">Aceite o novo pixel se seu valor não for igual ao valor do pixel atual.</span><span class="sxs-lookup"><span data-stu-id="7be09-118">Accept the new pixel if its value does not equal the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="7be09-119"><span id="D3DCMP_GREATEREQUAL"></span><span id="d3dcmp_greaterequal"></span>**D3DCMP \_ GREATEREQUAL**</span><span class="sxs-lookup"><span data-stu-id="7be09-119"><span id="D3DCMP_GREATEREQUAL"></span><span id="d3dcmp_greaterequal"></span>**D3DCMP\_GREATEREQUAL**</span></span>
</dt> <dd>

<span data-ttu-id="7be09-120">Aceite o novo pixel se seu valor for maior ou igual ao valor do pixel atual.</span><span class="sxs-lookup"><span data-stu-id="7be09-120">Accept the new pixel if its value is greater than or equal to the value of the current pixel.</span></span>

</dd> <dt>

<span data-ttu-id="7be09-121"><span id="D3DCMP_ALWAYS"></span><span id="d3dcmp_always"></span>**D3DCMP \_ sempre**</span><span class="sxs-lookup"><span data-stu-id="7be09-121"><span id="D3DCMP_ALWAYS"></span><span id="d3dcmp_always"></span>**D3DCMP\_ALWAYS**</span></span>
</dt> <dd>

<span data-ttu-id="7be09-122">Sempre passe o teste.</span><span class="sxs-lookup"><span data-stu-id="7be09-122">Always pass the test.</span></span>

</dd> <dt>

<span data-ttu-id="7be09-123"><span id="D3DCMP_FORCE_DWORD"></span><span id="d3dcmp_force_dword"></span>**D3DCMP \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="7be09-123"><span id="D3DCMP_FORCE_DWORD"></span><span id="d3dcmp_force_dword"></span>**D3DCMP\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="7be09-124">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="7be09-124">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="7be09-125">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="7be09-125">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="7be09-126">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="7be09-126">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7be09-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="7be09-127">Remarks</span></span>

<span data-ttu-id="7be09-128">Os valores neste tipo enumerado definem as funções de comparação com suporte para os \_ Estados de RENDERIZAÇÃO D3DRS ZFUNC, D3DRS \_ ALPHAFUNC e D3DRS \_ STENCILFUNC.</span><span class="sxs-lookup"><span data-stu-id="7be09-128">The values in this enumerated type define the supported compare functions for the D3DRS\_ZFUNC, D3DRS\_ALPHAFUNC, and D3DRS\_STENCILFUNC render states.</span></span>

## <a name="requirements"></a><span data-ttu-id="7be09-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7be09-129">Requirements</span></span>



| <span data-ttu-id="7be09-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="7be09-130">Requirement</span></span> | <span data-ttu-id="7be09-131">Valor</span><span class="sxs-lookup"><span data-stu-id="7be09-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7be09-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7be09-132">Header</span></span><br/> | <dl> <span data-ttu-id="7be09-133"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="7be09-133"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7be09-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="7be09-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7be09-135">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="7be09-135">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="7be09-136">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="7be09-136">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
