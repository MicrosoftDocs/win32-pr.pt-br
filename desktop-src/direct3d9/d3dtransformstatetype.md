---
description: Define constantes que descrevem valores de estado de transformação.
ms.assetid: 53535d9f-246a-42cf-82a2-fb3cf6d4ebac
title: Enumeração D3DTRANSFORMSTATETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTRANSFORMSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: c618e0e19bf7dd01dec73d35436f23189f9e78a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105789406"
---
# <a name="d3dtransformstatetype-enumeration"></a><span data-ttu-id="595e9-103">Enumeração D3DTRANSFORMSTATETYPE</span><span class="sxs-lookup"><span data-stu-id="595e9-103">D3DTRANSFORMSTATETYPE enumeration</span></span>

<span data-ttu-id="595e9-104">Define constantes que descrevem valores de estado de transformação.</span><span class="sxs-lookup"><span data-stu-id="595e9-104">Defines constants that describe transformation state values.</span></span>

## <a name="syntax"></a><span data-ttu-id="595e9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="595e9-105">Syntax</span></span>


```C++
typedef enum D3DTRANSFORMSTATETYPE { 
  D3DTS_VIEW         = 2,
  D3DTS_PROJECTION   = 3,
  D3DTS_TEXTURE0     = 16,
  D3DTS_TEXTURE1     = 17,
  D3DTS_TEXTURE2     = 18,
  D3DTS_TEXTURE3     = 19,
  D3DTS_TEXTURE4     = 20,
  D3DTS_TEXTURE5     = 21,
  D3DTS_TEXTURE6     = 22,
  D3DTS_TEXTURE7     = 23,
  D3DTS_FORCE_DWORD  = 0x7fffffff
} D3DTRANSFORMSTATETYPE, *LPD3DTRANSFORMSTATETYPE;
```



## <a name="constants"></a><span data-ttu-id="595e9-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="595e9-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="595e9-107"><span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**Exibição de D3DTS \_**</span><span class="sxs-lookup"><span data-stu-id="595e9-107"><span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**D3DTS\_VIEW**</span></span>
</dt> <dd>

<span data-ttu-id="595e9-108">Identifica a matriz de transformação que está sendo definida como a matriz de transformação View.</span><span class="sxs-lookup"><span data-stu-id="595e9-108">Identifies the transformation matrix being set as the view transformation matrix.</span></span> <span data-ttu-id="595e9-109">O valor padrão é **NULL** (a matriz de identidade).</span><span class="sxs-lookup"><span data-stu-id="595e9-109">The default value is **NULL** (the identity matrix).</span></span>

</dd> <dt>

<span data-ttu-id="595e9-110"><span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**\_Projeção D3DTS**</span><span class="sxs-lookup"><span data-stu-id="595e9-110"><span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**D3DTS\_PROJECTION**</span></span>
</dt> <dd>

<span data-ttu-id="595e9-111">Identifica a matriz de transformação que está sendo definida como a matriz de transformação projeção.</span><span class="sxs-lookup"><span data-stu-id="595e9-111">Identifies the transformation matrix being set as the projection transformation matrix.</span></span> <span data-ttu-id="595e9-112">O valor padrão é **NULL** (a matriz de identidade).</span><span class="sxs-lookup"><span data-stu-id="595e9-112">The default value is **NULL** (the identity matrix).</span></span>

</dd> <dt>

<span data-ttu-id="595e9-113"><span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**D3DTS \_ TEXTURE0**</span><span class="sxs-lookup"><span data-stu-id="595e9-113"><span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**D3DTS\_TEXTURE0**</span></span>
</dt> <dd>

<span data-ttu-id="595e9-114">Identifica a matriz de transformação que está sendo definida para o estágio de textura especificado.</span><span class="sxs-lookup"><span data-stu-id="595e9-114">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="595e9-115"><span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**D3DTS \_ TEXTURE1**</span><span class="sxs-lookup"><span data-stu-id="595e9-115"><span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**D3DTS\_TEXTURE1**</span></span>
</dt> <dd>

<span data-ttu-id="595e9-116">Identifica a matriz de transformação que está sendo definida para o estágio de textura especificado.</span><span class="sxs-lookup"><span data-stu-id="595e9-116">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="595e9-117"><span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**D3DTS \_ TEXTURE2**</span><span class="sxs-lookup"><span data-stu-id="595e9-117"><span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**D3DTS\_TEXTURE2**</span></span>
</dt> <dd>

<span data-ttu-id="595e9-118">Identifica a matriz de transformação que está sendo definida para o estágio de textura especificado.</span><span class="sxs-lookup"><span data-stu-id="595e9-118">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="595e9-119"><span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**D3DTS \_ TEXTURE3**</span><span class="sxs-lookup"><span data-stu-id="595e9-119"><span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**D3DTS\_TEXTURE3**</span></span>
</dt> <dd>

<span data-ttu-id="595e9-120">Identifica a matriz de transformação que está sendo definida para o estágio de textura especificado.</span><span class="sxs-lookup"><span data-stu-id="595e9-120">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="595e9-121"><span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**D3DTS \_ TEXTURE4**</span><span class="sxs-lookup"><span data-stu-id="595e9-121"><span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**D3DTS\_TEXTURE4**</span></span>
</dt> <dd>

<span data-ttu-id="595e9-122">Identifica a matriz de transformação que está sendo definida para o estágio de textura especificado.</span><span class="sxs-lookup"><span data-stu-id="595e9-122">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="595e9-123"><span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**D3DTS \_ TEXTURE5**</span><span class="sxs-lookup"><span data-stu-id="595e9-123"><span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**D3DTS\_TEXTURE5**</span></span>
</dt> <dd>

<span data-ttu-id="595e9-124">Identifica a matriz de transformação que está sendo definida para o estágio de textura especificado.</span><span class="sxs-lookup"><span data-stu-id="595e9-124">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="595e9-125"><span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**D3DTS \_ TEXTURE6**</span><span class="sxs-lookup"><span data-stu-id="595e9-125"><span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**D3DTS\_TEXTURE6**</span></span>
</dt> <dd>

<span data-ttu-id="595e9-126">Identifica a matriz de transformação que está sendo definida para o estágio de textura especificado.</span><span class="sxs-lookup"><span data-stu-id="595e9-126">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="595e9-127"><span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**D3DTS \_ TEXTURE7**</span><span class="sxs-lookup"><span data-stu-id="595e9-127"><span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**D3DTS\_TEXTURE7**</span></span>
</dt> <dd>

<span data-ttu-id="595e9-128">Identifica a matriz de transformação que está sendo definida para o estágio de textura especificado.</span><span class="sxs-lookup"><span data-stu-id="595e9-128">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="595e9-129"><span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="595e9-129"><span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="595e9-130">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="595e9-130">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="595e9-131">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="595e9-131">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="595e9-132">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="595e9-132">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="595e9-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="595e9-133">Remarks</span></span>

<span data-ttu-id="595e9-134">Os Estados de transformação no intervalo de 256 a 511 são reservados para armazenar até 256 matrizes mundiais que podem ser indexadas usando as \_ macros D3DTS WORLDMATRIX e D3DTS \_ World.</span><span class="sxs-lookup"><span data-stu-id="595e9-134">The transform states in the range 256 through 511 are reserved to store up to 256 world matrices that can be indexed using the D3DTS\_WORLDMATRIX and D3DTS\_WORLD macros.</span></span>



| <span data-ttu-id="595e9-135">Macros</span><span class="sxs-lookup"><span data-stu-id="595e9-135">Macros</span></span>                                                  |                                                                                                                                                                       |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="595e9-136">**D3DTS \_ World**</span><span class="sxs-lookup"><span data-stu-id="595e9-136">**D3DTS\_WORLD**</span></span>](d3dts-world.md)                     | <span data-ttu-id="595e9-137">Equivalente a D3DTS \_ WORLDMATRIX (0).</span><span class="sxs-lookup"><span data-stu-id="595e9-137">Equivalent to D3DTS\_WORLDMATRIX(0).</span></span>                                                                                                                                  |
| <span data-ttu-id="595e9-138">[**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) (índice)</span><span class="sxs-lookup"><span data-stu-id="595e9-138">[**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) (index)</span></span> | <span data-ttu-id="595e9-139">Identifica a matriz de transformação a ser definida para a matriz mundial no índice.</span><span class="sxs-lookup"><span data-stu-id="595e9-139">Identifies the transform matrix to set for the world matrix at index.</span></span> <span data-ttu-id="595e9-140">Várias matrizes mundiais são usadas apenas para mesclagem de vértice.</span><span class="sxs-lookup"><span data-stu-id="595e9-140">Multiple world matrices are used only for vertex blending.</span></span> <span data-ttu-id="595e9-141">Caso contrário, somente D3DTS \_ World será usado.</span><span class="sxs-lookup"><span data-stu-id="595e9-141">Otherwise only D3DTS\_WORLD is used.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="595e9-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="595e9-142">Requirements</span></span>



| <span data-ttu-id="595e9-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="595e9-143">Requirement</span></span> | <span data-ttu-id="595e9-144">Valor</span><span class="sxs-lookup"><span data-stu-id="595e9-144">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="595e9-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="595e9-145">Header</span></span><br/> | <dl> <span data-ttu-id="595e9-146"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="595e9-146"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="595e9-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="595e9-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="595e9-148">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="595e9-148">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="595e9-149">**IDirect3DDevice9:: GetTransform**</span><span class="sxs-lookup"><span data-stu-id="595e9-149">**IDirect3DDevice9::GetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettransform)
</dt> <dt>

[<span data-ttu-id="595e9-150">**IDirect3DDevice9::MultiplyTransform**</span><span class="sxs-lookup"><span data-stu-id="595e9-150">**IDirect3DDevice9::MultiplyTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-multiplytransform)
</dt> <dt>

[<span data-ttu-id="595e9-151">**IDirect3DDevice9:: SetTransform**</span><span class="sxs-lookup"><span data-stu-id="595e9-151">**IDirect3DDevice9::SetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

[<span data-ttu-id="595e9-152">**D3DTS \_ World**</span><span class="sxs-lookup"><span data-stu-id="595e9-152">**D3DTS\_WORLD**</span></span>](d3dts-world.md)
</dt> <dt>

[<span data-ttu-id="595e9-153">**D3DTS \_ worldn**</span><span class="sxs-lookup"><span data-stu-id="595e9-153">**D3DTS\_WORLDn**</span></span>](d3dts-worldn.md)
</dt> <dt>

[<span data-ttu-id="595e9-154">**D3DTS \_ WORLDMATRIX**</span><span class="sxs-lookup"><span data-stu-id="595e9-154">**D3DTS\_WORLDMATRIX**</span></span>](d3dts-worldmatrix.md)
</dt> </dl>

 

 
