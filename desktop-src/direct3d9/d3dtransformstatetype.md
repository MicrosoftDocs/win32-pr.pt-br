---
description: Define constantes que descrevem valores de estado de transformação.
ms.assetid: 53535d9f-246a-42cf-82a2-fb3cf6d4ebac
title: Enumeração D3DTRANSFORMSTATETYPE (D3D9Types.h)
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
ms.openlocfilehash: 022aa20fab0739b32aa75eb5f4bc575c0a8ad853
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342991"
---
# <a name="d3dtransformstatetype-enumeration"></a><span data-ttu-id="0b28e-103">Enumeração D3DTRANSFORMSTATETYPE</span><span class="sxs-lookup"><span data-stu-id="0b28e-103">D3DTRANSFORMSTATETYPE enumeration</span></span>

<span data-ttu-id="0b28e-104">Define constantes que descrevem valores de estado de transformação.</span><span class="sxs-lookup"><span data-stu-id="0b28e-104">Defines constants that describe transformation state values.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b28e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b28e-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="0b28e-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="0b28e-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0b28e-107"><span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**EXIBIÇÃO D3DTS \_**</span><span class="sxs-lookup"><span data-stu-id="0b28e-107"><span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**D3DTS\_VIEW**</span></span>
</dt> <dd>

<span data-ttu-id="0b28e-108">Identifica a matriz de transformação que está sendo definida como a matriz de transformação de exibição.</span><span class="sxs-lookup"><span data-stu-id="0b28e-108">Identifies the transformation matrix being set as the view transformation matrix.</span></span> <span data-ttu-id="0b28e-109">O valor padrão é **NULL** (a matriz de identidade).</span><span class="sxs-lookup"><span data-stu-id="0b28e-109">The default value is **NULL** (the identity matrix).</span></span>

</dd> <dt>

<span data-ttu-id="0b28e-110"><span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**PROJEÇÃO DE D3DTS \_**</span><span class="sxs-lookup"><span data-stu-id="0b28e-110"><span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**D3DTS\_PROJECTION**</span></span>
</dt> <dd>

<span data-ttu-id="0b28e-111">Identifica a matriz de transformação que está sendo definida como a matriz de transformação de projeção.</span><span class="sxs-lookup"><span data-stu-id="0b28e-111">Identifies the transformation matrix being set as the projection transformation matrix.</span></span> <span data-ttu-id="0b28e-112">O valor padrão é **NULL** (a matriz de identidade).</span><span class="sxs-lookup"><span data-stu-id="0b28e-112">The default value is **NULL** (the identity matrix).</span></span>

</dd> <dt>

<span data-ttu-id="0b28e-113"><span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**TEXTURA DE \_ D3DTS0**</span><span class="sxs-lookup"><span data-stu-id="0b28e-113"><span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**D3DTS\_TEXTURE0**</span></span>
</dt> <dd>

<span data-ttu-id="0b28e-114">Identifica a matriz de transformação que está sendo definida para o estágio de textura especificado.</span><span class="sxs-lookup"><span data-stu-id="0b28e-114">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="0b28e-115"><span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**TEXTURA DE \_ D3DTS1**</span><span class="sxs-lookup"><span data-stu-id="0b28e-115"><span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**D3DTS\_TEXTURE1**</span></span>
</dt> <dd>

<span data-ttu-id="0b28e-116">Identifica a matriz de transformação que está sendo definida para o estágio de textura especificado.</span><span class="sxs-lookup"><span data-stu-id="0b28e-116">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="0b28e-117"><span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**TEXTURA DE \_ D3DTS2**</span><span class="sxs-lookup"><span data-stu-id="0b28e-117"><span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**D3DTS\_TEXTURE2**</span></span>
</dt> <dd>

<span data-ttu-id="0b28e-118">Identifica a matriz de transformação que está sendo definida para o estágio de textura especificado.</span><span class="sxs-lookup"><span data-stu-id="0b28e-118">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="0b28e-119"><span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**TEXTURA DE \_ D3DTS3**</span><span class="sxs-lookup"><span data-stu-id="0b28e-119"><span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**D3DTS\_TEXTURE3**</span></span>
</dt> <dd>

<span data-ttu-id="0b28e-120">Identifica a matriz de transformação que está sendo definida para o estágio de textura especificado.</span><span class="sxs-lookup"><span data-stu-id="0b28e-120">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="0b28e-121"><span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**TEXTURA DE \_ D3DTS4**</span><span class="sxs-lookup"><span data-stu-id="0b28e-121"><span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**D3DTS\_TEXTURE4**</span></span>
</dt> <dd>

<span data-ttu-id="0b28e-122">Identifica a matriz de transformação que está sendo definida para o estágio de textura especificado.</span><span class="sxs-lookup"><span data-stu-id="0b28e-122">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="0b28e-123"><span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**D3DTS \_ TEXTURE5**</span><span class="sxs-lookup"><span data-stu-id="0b28e-123"><span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**D3DTS\_TEXTURE5**</span></span>
</dt> <dd>

<span data-ttu-id="0b28e-124">Identifica a matriz de transformação que está sendo definida para o estágio de textura especificado.</span><span class="sxs-lookup"><span data-stu-id="0b28e-124">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="0b28e-125"><span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**D3DTS \_ TEXTURE6**</span><span class="sxs-lookup"><span data-stu-id="0b28e-125"><span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**D3DTS\_TEXTURE6**</span></span>
</dt> <dd>

<span data-ttu-id="0b28e-126">Identifica a matriz de transformação que está sendo definida para o estágio de textura especificado.</span><span class="sxs-lookup"><span data-stu-id="0b28e-126">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="0b28e-127"><span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**D3DTS \_ TEXTURE7**</span><span class="sxs-lookup"><span data-stu-id="0b28e-127"><span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**D3DTS\_TEXTURE7**</span></span>
</dt> <dd>

<span data-ttu-id="0b28e-128">Identifica a matriz de transformação que está sendo definida para o estágio de textura especificado.</span><span class="sxs-lookup"><span data-stu-id="0b28e-128">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="0b28e-129"><span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="0b28e-129"><span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="0b28e-130">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="0b28e-130">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="0b28e-131">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="0b28e-131">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="0b28e-132">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="0b28e-132">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b28e-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b28e-133">Remarks</span></span>

<span data-ttu-id="0b28e-134">Os Estados de transformação no intervalo de 256 a 511 são reservados para armazenar até 256 matrizes mundiais que podem ser indexadas usando as \_ macros D3DTS WORLDMATRIX e D3DTS \_ World.</span><span class="sxs-lookup"><span data-stu-id="0b28e-134">The transform states in the range 256 through 511 are reserved to store up to 256 world matrices that can be indexed using the D3DTS\_WORLDMATRIX and D3DTS\_WORLD macros.</span></span>



| <span data-ttu-id="0b28e-135">Macros</span><span class="sxs-lookup"><span data-stu-id="0b28e-135">Macros</span></span>                                                  | <span data-ttu-id="0b28e-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="0b28e-136">Description</span></span>                                                                                                                                                                      |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b28e-137">**D3DTS \_ World**</span><span class="sxs-lookup"><span data-stu-id="0b28e-137">**D3DTS\_WORLD**</span></span>](d3dts-world.md)                     | <span data-ttu-id="0b28e-138">Equivalente a D3DTS \_ WORLDMATRIX (0).</span><span class="sxs-lookup"><span data-stu-id="0b28e-138">Equivalent to D3DTS\_WORLDMATRIX(0).</span></span>                                                                                                                                  |
| <span data-ttu-id="0b28e-139">[**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) (índice)</span><span class="sxs-lookup"><span data-stu-id="0b28e-139">[**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) (index)</span></span> | <span data-ttu-id="0b28e-140">Identifica a matriz de transformação a ser definida para a matriz mundial no índice.</span><span class="sxs-lookup"><span data-stu-id="0b28e-140">Identifies the transform matrix to set for the world matrix at index.</span></span> <span data-ttu-id="0b28e-141">Várias matrizes mundiais são usadas apenas para mesclagem de vértice.</span><span class="sxs-lookup"><span data-stu-id="0b28e-141">Multiple world matrices are used only for vertex blending.</span></span> <span data-ttu-id="0b28e-142">Caso contrário, somente D3DTS \_ World será usado.</span><span class="sxs-lookup"><span data-stu-id="0b28e-142">Otherwise only D3DTS\_WORLD is used.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="0b28e-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b28e-143">Requirements</span></span>



| <span data-ttu-id="0b28e-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b28e-144">Requirement</span></span> | <span data-ttu-id="0b28e-145">Valor</span><span class="sxs-lookup"><span data-stu-id="0b28e-145">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b28e-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0b28e-146">Header</span></span><br/> | <dl> <span data-ttu-id="0b28e-147"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b28e-147"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b28e-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b28e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b28e-149">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="0b28e-149">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="0b28e-150">**IDirect3DDevice9:: GetTransform**</span><span class="sxs-lookup"><span data-stu-id="0b28e-150">**IDirect3DDevice9::GetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettransform)
</dt> <dt>

[<span data-ttu-id="0b28e-151">**IDirect3DDevice9::MultiplyTransform**</span><span class="sxs-lookup"><span data-stu-id="0b28e-151">**IDirect3DDevice9::MultiplyTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-multiplytransform)
</dt> <dt>

[<span data-ttu-id="0b28e-152">**IDirect3DDevice9::SetTransform**</span><span class="sxs-lookup"><span data-stu-id="0b28e-152">**IDirect3DDevice9::SetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

[<span data-ttu-id="0b28e-153">**D3DTS \_ WORLD**</span><span class="sxs-lookup"><span data-stu-id="0b28e-153">**D3DTS\_WORLD**</span></span>](d3dts-world.md)
</dt> <dt>

[<span data-ttu-id="0b28e-154">**D3DTS \_ WORLDn**</span><span class="sxs-lookup"><span data-stu-id="0b28e-154">**D3DTS\_WORLDn**</span></span>](d3dts-worldn.md)
</dt> <dt>

[<span data-ttu-id="0b28e-155">**D3DTS \_ WORLDMATRIX**</span><span class="sxs-lookup"><span data-stu-id="0b28e-155">**D3DTS\_WORLDMATRIX**</span></span>](d3dts-worldmatrix.md)
</dt> </dl>

 

 
