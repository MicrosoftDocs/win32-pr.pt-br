---
description: Define um vetor normal para cada Texel em um objeto de textura. Esse método é usado para armazenar vetores normais de vértice de uma malha (ou um vértice interpolado Normals se a transferência de radiante (PRT) baseada em pixels estiver sendo computada).
ms.assetid: 165a3ef6-c142-4988-b4fb-5aafd8ff11fe
title: 'Método ID3DXPRTEngine:: SetPerTexelNormal (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerTexelNormal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5220ad500312792cd158967e9502381f49b0e3e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370973"
---
# <a name="id3dxprtenginesetpertexelnormal-method"></a><span data-ttu-id="301a9-104">Método ID3DXPRTEngine:: SetPerTexelNormal</span><span class="sxs-lookup"><span data-stu-id="301a9-104">ID3DXPRTEngine::SetPerTexelNormal method</span></span>

<span data-ttu-id="301a9-105">Define um vetor normal para cada Texel em um objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="301a9-105">Sets a normal vector for each texel in a texture object.</span></span> <span data-ttu-id="301a9-106">Esse método é usado para armazenar vetores normais de vértice de uma malha (ou um vértice interpolado Normals se a transferência de radiante (PRT) baseada em pixels estiver sendo computada).</span><span class="sxs-lookup"><span data-stu-id="301a9-106">This method is used to store vertex normal vectors from a mesh (or interpolated vertex normals if pixel-based precomputed radiance transfer (PRT) is being computed).</span></span>

## <a name="syntax"></a><span data-ttu-id="301a9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="301a9-107">Syntax</span></span>


```C++
HRESULT SetPerTexelNormal(
  [in] LPDIRECT3DTEXTURE9 pNormalTexture
);
```



## <a name="parameters"></a><span data-ttu-id="301a9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="301a9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="301a9-109">*pNormalTexture* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="301a9-109">*pNormalTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="301a9-110">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="301a9-110">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="301a9-111">Ponteiro para um objeto de textura [**IDirect3DTexture9**](/windows/desktop/api) que serve como um mapa normal de espaço de objeto no qual armazenar vetores normais.</span><span class="sxs-lookup"><span data-stu-id="301a9-111">Pointer to an [**IDirect3DTexture9**](/windows/desktop/api) texture object that serves as an object space normal map in which to store normal vectors.</span></span> <span data-ttu-id="301a9-112">A textura deve ter as mesmas dimensões que [**ID3DXPRTBuffer**](id3dxprtbuffer.md) e deve ser capaz de armazenar formatos de textura assinados.</span><span class="sxs-lookup"><span data-stu-id="301a9-112">The texture must have the same dimensions as [**ID3DXPRTBuffer**](id3dxprtbuffer.md) and must be able to store signed texture formats.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="301a9-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="301a9-113">Return value</span></span>

<span data-ttu-id="301a9-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="301a9-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="301a9-115">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="301a9-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="301a9-116">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="301a9-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="301a9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="301a9-117">Requirements</span></span>



| <span data-ttu-id="301a9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="301a9-118">Requirement</span></span> | <span data-ttu-id="301a9-119">Valor</span><span class="sxs-lookup"><span data-stu-id="301a9-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="301a9-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="301a9-120">Header</span></span><br/>  | <dl> <span data-ttu-id="301a9-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="301a9-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="301a9-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="301a9-122">Library</span></span><br/> | <dl> <span data-ttu-id="301a9-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="301a9-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="301a9-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="301a9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="301a9-125">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="301a9-125">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
