---
description: Calcula o IMT por triângulo de uma textura mapeada em uma malha, a ser usada opcionalmente como entrada para as funções UVAtlas do D3DX.
ms.assetid: 6671edc4-e494-4847-ae99-b9e56651a875
title: Função D3DXComputeIMTFromTexture (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2fbed0411f3562e3a05ec2ec4df99dfad6d8c902
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012146"
---
# <a name="d3dxcomputeimtfromtexture-function"></a><span data-ttu-id="dae0a-103">Função D3DXComputeIMTFromTexture</span><span class="sxs-lookup"><span data-stu-id="dae0a-103">D3DXComputeIMTFromTexture function</span></span>

<span data-ttu-id="dae0a-104">Calcula o IMT por triângulo de uma textura mapeada em uma malha, a ser usada opcionalmente como entrada para as [funções UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)do D3DX.</span><span class="sxs-lookup"><span data-stu-id="dae0a-104">Calculates per-triangle IMT's from a texture mapped onto a mesh, to be used optionally as input to the D3DX [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="dae0a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dae0a-105">Syntax</span></span>


```C++
HRESULT D3DXComputeIMTFromTexture(
  _In_  LPD3DXMESH         pMesh,
  _In_  LPDIRECT3DTEXTURE9 pTexture,
  _In_  DWORD              dwTextureIndex,
  _In_  DWORD              dwOptions,
        LPD3DXUVATLASCB    pStatusCallback,
        LPVOID             pUserContext,
  _Out_ LPD3DXBUFFER       *ppIMTData
);
```



## <a name="parameters"></a><span data-ttu-id="dae0a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dae0a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dae0a-107">*pMesh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dae0a-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dae0a-108">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="dae0a-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="dae0a-109">Um ponteiro para uma malha de entrada (consulte [**ID3DXMesh**](id3dxmesh.md)) que contém a geometria do objeto para calcular o IMT.</span><span class="sxs-lookup"><span data-stu-id="dae0a-109">A pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the IMT.</span></span>

</dd> <dt>

<span data-ttu-id="dae0a-110">*pTexture* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dae0a-110">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dae0a-111">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="dae0a-111">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="dae0a-112">Um ponteiro para a textura (consulte [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)) que é mapeado para a malha.</span><span class="sxs-lookup"><span data-stu-id="dae0a-112">A pointer to the texture (see [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)) that is mapped to the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="dae0a-113">*dwTextureIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dae0a-113">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dae0a-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dae0a-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dae0a-115">Índice de coordenadas de textura baseado em zero que identifica o conjunto de coordenadas de textura a ser usado.</span><span class="sxs-lookup"><span data-stu-id="dae0a-115">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="dae0a-116">*dwOptions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dae0a-116">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dae0a-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dae0a-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dae0a-118">Opções de quebra automática de textura.</span><span class="sxs-lookup"><span data-stu-id="dae0a-118">Texture wrap options.</span></span> <span data-ttu-id="dae0a-119">Essa é uma combinação de um ou mais [**sinalizadores D3DXIMT**](./d3dximt-flags.md).</span><span class="sxs-lookup"><span data-stu-id="dae0a-119">This is a combination of one or more [**D3DXIMT FLAGS**](./d3dximt-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="dae0a-120">*pStatusCallback*</span><span class="sxs-lookup"><span data-stu-id="dae0a-120">*pStatusCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="dae0a-121">Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="dae0a-121">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="dae0a-122">Um ponteiro para uma função de retorno de chamada para monitorar o progresso da computação IMT.</span><span class="sxs-lookup"><span data-stu-id="dae0a-122">A pointer to a callback function to monitor IMT computation progress.</span></span>

</dd> <dt>

<span data-ttu-id="dae0a-123">*pUserContext*</span><span class="sxs-lookup"><span data-stu-id="dae0a-123">*pUserContext*</span></span> 
</dt> <dd>

<span data-ttu-id="dae0a-124">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dae0a-124">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dae0a-125">Um ponteiro para uma variável definida pelo usuário que é passada para a função de retorno de chamada de status.</span><span class="sxs-lookup"><span data-stu-id="dae0a-125">A pointer to a user-defined variable which is passed to the status callback function.</span></span> <span data-ttu-id="dae0a-126">Normalmente usado por um aplicativo para passar um ponteiro para uma estrutura de dados que fornece informações de contexto para a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="dae0a-126">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="dae0a-127">*ppIMTData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="dae0a-127">*ppIMTData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dae0a-128">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="dae0a-128">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="dae0a-129">Um ponteiro para o buffer (consulte [**ID3DXBuffer**](id3dxbuffer.md)) que contém a matriz IMT retornada.</span><span class="sxs-lookup"><span data-stu-id="dae0a-129">A pointer to the buffer (see [**ID3DXBuffer**](id3dxbuffer.md)) containing the returned IMT array.</span></span> <span data-ttu-id="dae0a-130">Essa matriz pode ser fornecida como entrada para as [funções D3DX UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md) para priorizar a alocação de espaço de textura na parametrização de textura.</span><span class="sxs-lookup"><span data-stu-id="dae0a-130">This array can be provided as input to the D3DX [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md) to prioritize texture-space allocation in the texture parameterization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dae0a-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dae0a-131">Return value</span></span>

<span data-ttu-id="dae0a-132">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dae0a-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dae0a-133">Se a função for realizada com sucesso, o valor de retorno será D3D \_ OK; caso contrário, o valor será D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="dae0a-133">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="dae0a-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="dae0a-134">Remarks</span></span>

<span data-ttu-id="dae0a-135">Dada uma textura que mapeia sobre a superfície da malha, o algoritmo computa o IMT para cada face.</span><span class="sxs-lookup"><span data-stu-id="dae0a-135">Given a texture that maps over the surface of the mesh, the algorithm computes the IMT for each face.</span></span> <span data-ttu-id="dae0a-136">Isso fará com que os triângulos que contêm dados de sinal de baixa frequência contenham menos espaço no Atlas de textura final quando parametrizados com as funções UVAtlas.</span><span class="sxs-lookup"><span data-stu-id="dae0a-136">This will cause triangles containing lower-frequency signal data to take up less space in the final texture atlas when parameterized with the UVAtlas functions.</span></span> <span data-ttu-id="dae0a-137">Pressupõe-se que a textura seja interpolada na malha bilinearmente.</span><span class="sxs-lookup"><span data-stu-id="dae0a-137">The texture is assumed to be interpolated over the mesh bilinearly.</span></span>

## <a name="requirements"></a><span data-ttu-id="dae0a-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dae0a-138">Requirements</span></span>



| <span data-ttu-id="dae0a-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="dae0a-139">Requirement</span></span> | <span data-ttu-id="dae0a-140">Valor</span><span class="sxs-lookup"><span data-stu-id="dae0a-140">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dae0a-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dae0a-141">Header</span></span><br/>  | <dl> <span data-ttu-id="dae0a-142"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="dae0a-142"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="dae0a-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dae0a-143">Library</span></span><br/> | <dl> <span data-ttu-id="dae0a-144"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dae0a-144"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dae0a-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="dae0a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dae0a-146">Funções UVAtlas</span><span class="sxs-lookup"><span data-stu-id="dae0a-146">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[<span data-ttu-id="dae0a-147">Usando o UVAtlas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="dae0a-147">Using UVAtlas (Direct3D 9)</span></span>](using-uvatlas.md)
</dt> </dl>

 

 
