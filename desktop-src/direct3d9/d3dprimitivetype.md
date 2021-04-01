---
description: Define os primitivos com suporte do Direct3D.
ms.assetid: 89e697f9-02b9-4ae1-9e86-6178da0cb008
title: Enumeração D3DPRIMITIVETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRIMITIVETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 933bbec72950bd2c73fda8b3781dd46393ca4c96
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104091975"
---
# <a name="d3dprimitivetype-enumeration"></a><span data-ttu-id="801a4-103">Enumeração D3DPRIMITIVETYPE</span><span class="sxs-lookup"><span data-stu-id="801a4-103">D3DPRIMITIVETYPE enumeration</span></span>

<span data-ttu-id="801a4-104">Define os primitivos com suporte do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="801a4-104">Defines the primitives supported by Direct3D.</span></span>

## <a name="syntax"></a><span data-ttu-id="801a4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="801a4-105">Syntax</span></span>


```C++
typedef enum D3DPRIMITIVETYPE { 
  D3DPT_POINTLIST      = 1,
  D3DPT_LINELIST       = 2,
  D3DPT_LINESTRIP      = 3,
  D3DPT_TRIANGLELIST   = 4,
  D3DPT_TRIANGLESTRIP  = 5,
  D3DPT_TRIANGLEFAN    = 6,
  D3DPT_FORCE_DWORD    = 0x7fffffff
} D3DPRIMITIVETYPE, *LPD3DPRIMITIVETYPE;
```



## <a name="constants"></a><span data-ttu-id="801a4-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="801a4-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="801a4-107"><span id="D3DPT_POINTLIST"></span><span id="d3dpt_pointlist"></span>**D3DPT \_ PointList**</span><span class="sxs-lookup"><span data-stu-id="801a4-107"><span id="D3DPT_POINTLIST"></span><span id="d3dpt_pointlist"></span>**D3DPT\_POINTLIST**</span></span>
</dt> <dd>

<span data-ttu-id="801a4-108">Renderiza os vértices como uma coleção de pontos isolados.</span><span class="sxs-lookup"><span data-stu-id="801a4-108">Renders the vertices as a collection of isolated points.</span></span> <span data-ttu-id="801a4-109">Não há suporte para esse valor para primitivos indexados.</span><span class="sxs-lookup"><span data-stu-id="801a4-109">This value is unsupported for indexed primitives.</span></span>

</dd> <dt>

<span data-ttu-id="801a4-110"><span id="D3DPT_LINELIST"></span><span id="d3dpt_linelist"></span>**D3DPT \_ LineList**</span><span class="sxs-lookup"><span data-stu-id="801a4-110"><span id="D3DPT_LINELIST"></span><span id="d3dpt_linelist"></span>**D3DPT\_LINELIST**</span></span>
</dt> <dd>

<span data-ttu-id="801a4-111">Renderiza os vértices como uma lista de segmentos de linha reta isolados.</span><span class="sxs-lookup"><span data-stu-id="801a4-111">Renders the vertices as a list of isolated straight line segments.</span></span>

</dd> <dt>

<span data-ttu-id="801a4-112"><span id="D3DPT_LINESTRIP"></span><span id="d3dpt_linestrip"></span>**D3DPT \_ LINESTRIP**</span><span class="sxs-lookup"><span data-stu-id="801a4-112"><span id="D3DPT_LINESTRIP"></span><span id="d3dpt_linestrip"></span>**D3DPT\_LINESTRIP**</span></span>
</dt> <dd>

<span data-ttu-id="801a4-113">Renderiza os vértices como uma única polilinha.</span><span class="sxs-lookup"><span data-stu-id="801a4-113">Renders the vertices as a single polyline.</span></span>

</dd> <dt>

<span data-ttu-id="801a4-114"><span id="D3DPT_TRIANGLELIST"></span><span id="d3dpt_trianglelist"></span>**D3DPT \_ TRIângulolist**</span><span class="sxs-lookup"><span data-stu-id="801a4-114"><span id="D3DPT_TRIANGLELIST"></span><span id="d3dpt_trianglelist"></span>**D3DPT\_TRIANGLELIST**</span></span>
</dt> <dd>

<span data-ttu-id="801a4-115">Renderiza os vértices especificados como uma sequência de triângulos isolados.</span><span class="sxs-lookup"><span data-stu-id="801a4-115">Renders the specified vertices as a sequence of isolated triangles.</span></span> <span data-ttu-id="801a4-116">Cada grupo de três vértices define um triângulo separado.</span><span class="sxs-lookup"><span data-stu-id="801a4-116">Each group of three vertices defines a separate triangle.</span></span>

<span data-ttu-id="801a4-117">A remoção de face para frente é afetada pelo estado de renderização da ordem de contorno atual.</span><span class="sxs-lookup"><span data-stu-id="801a4-117">Back-face culling is affected by the current winding-order render state.</span></span>

</dd> <dt>

<span data-ttu-id="801a4-118"><span id="D3DPT_TRIANGLESTRIP"></span><span id="d3dpt_trianglestrip"></span>**D3DPT \_ TRIANGLESTRIP**</span><span class="sxs-lookup"><span data-stu-id="801a4-118"><span id="D3DPT_TRIANGLESTRIP"></span><span id="d3dpt_trianglestrip"></span>**D3DPT\_TRIANGLESTRIP**</span></span>
</dt> <dd>

<span data-ttu-id="801a4-119">Renderiza os vértices como uma faixa de triângulo.</span><span class="sxs-lookup"><span data-stu-id="801a4-119">Renders the vertices as a triangle strip.</span></span> <span data-ttu-id="801a4-120">O sinalizador de remoção de backface é automaticamente invertido em triângulos pares.</span><span class="sxs-lookup"><span data-stu-id="801a4-120">The backface-culling flag is automatically flipped on even-numbered triangles.</span></span>

</dd> <dt>

<span data-ttu-id="801a4-121"><span id="D3DPT_TRIANGLEFAN"></span><span id="d3dpt_trianglefan"></span>**D3DPT \_ TRIANGLEFAN**</span><span class="sxs-lookup"><span data-stu-id="801a4-121"><span id="D3DPT_TRIANGLEFAN"></span><span id="d3dpt_trianglefan"></span>**D3DPT\_TRIANGLEFAN**</span></span>
</dt> <dd>

<span data-ttu-id="801a4-122">Renderiza os vértices como um ventilador de triângulo.</span><span class="sxs-lookup"><span data-stu-id="801a4-122">Renders the vertices as a triangle fan.</span></span>

</dd> <dt>

<span data-ttu-id="801a4-123"><span id="D3DPT_FORCE_DWORD"></span><span id="d3dpt_force_dword"></span>**D3DPT \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="801a4-123"><span id="D3DPT_FORCE_DWORD"></span><span id="d3dpt_force_dword"></span>**D3DPT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="801a4-124">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="801a4-124">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="801a4-125">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="801a4-125">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="801a4-126">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="801a4-126">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="801a4-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="801a4-127">Remarks</span></span>

<span data-ttu-id="801a4-128">O uso de [faixas de triângulo](triangle-strips.md) ou [de ventiladores de triângulo (Direct3D 9)](triangle-fans.md) geralmente é mais eficiente do que o uso de listas de triângulo porque menos vértices são duplicados.</span><span class="sxs-lookup"><span data-stu-id="801a4-128">Using [Triangle Strips](triangle-strips.md) or [Triangle Fans (Direct3D 9)](triangle-fans.md) is often more efficient than using triangle lists because fewer vertices are duplicated.</span></span>

## <a name="requirements"></a><span data-ttu-id="801a4-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="801a4-129">Requirements</span></span>



| <span data-ttu-id="801a4-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="801a4-130">Requirement</span></span> | <span data-ttu-id="801a4-131">Valor</span><span class="sxs-lookup"><span data-stu-id="801a4-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="801a4-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="801a4-132">Header</span></span><br/> | <dl> <span data-ttu-id="801a4-133"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="801a4-133"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="801a4-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="801a4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="801a4-135">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="801a4-135">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="801a4-136">**IDirect3DDevice9::DrawIndexedPrimitive**</span><span class="sxs-lookup"><span data-stu-id="801a4-136">**IDirect3DDevice9::DrawIndexedPrimitive**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)
</dt> <dt>

[<span data-ttu-id="801a4-137">**IDirect3DDevice9::DrawIndexedPrimitiveUP**</span><span class="sxs-lookup"><span data-stu-id="801a4-137">**IDirect3DDevice9::DrawIndexedPrimitiveUP**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitiveup)
</dt> <dt>

[<span data-ttu-id="801a4-138">**IDirect3DDevice9::DrawPrimitive**</span><span class="sxs-lookup"><span data-stu-id="801a4-138">**IDirect3DDevice9::DrawPrimitive**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)
</dt> <dt>

[<span data-ttu-id="801a4-139">**IDirect3DDevice9::DrawPrimitiveUP**</span><span class="sxs-lookup"><span data-stu-id="801a4-139">**IDirect3DDevice9::DrawPrimitiveUP**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitiveup)
</dt> </dl>

 

 
