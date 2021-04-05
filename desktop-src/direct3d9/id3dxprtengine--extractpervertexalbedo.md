---
description: Copia valores de albedo por vértice de uma malha.
ms.assetid: 3a6f1cc2-a870-4463-98df-599d9fbd9d78
title: 'Método ID3DXPRTEngine:: ExtractPerVertexAlbedo (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ExtractPerVertexAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ed23b75b3113421b6242f49416e4b54bfce336f4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930728"
---
# <a name="id3dxprtengineextractpervertexalbedo-method"></a><span data-ttu-id="c51a5-103">Método ID3DXPRTEngine:: ExtractPerVertexAlbedo</span><span class="sxs-lookup"><span data-stu-id="c51a5-103">ID3DXPRTEngine::ExtractPerVertexAlbedo method</span></span>

<span data-ttu-id="c51a5-104">Copia valores de albedo por vértice de uma malha.</span><span class="sxs-lookup"><span data-stu-id="c51a5-104">Copies per-vertex albedo values from a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="c51a5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c51a5-105">Syntax</span></span>


```C++
HRESULT ExtractPerVertexAlbedo(
  [in] LPD3DXMESH   pMesh,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         NumChanIn
);
```



## <a name="parameters"></a><span data-ttu-id="c51a5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c51a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c51a5-107">*pMesh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c51a5-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c51a5-108">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="c51a5-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="c51a5-109">Ponteiro para o objeto de malha [**ID3DXMesh**](id3dxmesh.md) usado em [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) para criar o objeto [**ID3DXPRTEngine**](id3dxprtengine.md) .</span><span class="sxs-lookup"><span data-stu-id="c51a5-109">Pointer to the [**ID3DXMesh**](id3dxmesh.md) mesh object used in [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) to create the [**ID3DXPRTEngine**](id3dxprtengine.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="c51a5-110">*Uso* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="c51a5-110">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c51a5-111">Tipo: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**</span><span class="sxs-lookup"><span data-stu-id="c51a5-111">Type: **[**D3DDECLUSAGE**](./d3ddeclusage.md)**</span></span>

<span data-ttu-id="c51a5-112">Descrições de uso de vértice a serem copiadas da malha.</span><span class="sxs-lookup"><span data-stu-id="c51a5-112">Vertex usage descriptions to copy from the mesh.</span></span> <span data-ttu-id="c51a5-113">Consulte [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="c51a5-113">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="c51a5-114">*NumChanIn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c51a5-114">*NumChanIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c51a5-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c51a5-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c51a5-116">Número de canais de cores a serem copiados da malha.</span><span class="sxs-lookup"><span data-stu-id="c51a5-116">Number of color channels to copy from the mesh.</span></span> <span data-ttu-id="c51a5-117">Defina como 1 para especificar os materiais em cinza (R = G = B) ou 3 para habilitar os efeitos de sangramento de cor.</span><span class="sxs-lookup"><span data-stu-id="c51a5-117">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c51a5-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c51a5-118">Return value</span></span>

<span data-ttu-id="c51a5-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c51a5-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c51a5-120">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c51a5-120">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c51a5-121">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="c51a5-121">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="c51a5-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c51a5-122">Requirements</span></span>



| <span data-ttu-id="c51a5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c51a5-123">Requirement</span></span> | <span data-ttu-id="c51a5-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c51a5-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c51a5-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c51a5-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c51a5-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c51a5-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c51a5-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c51a5-127">Library</span></span><br/> | <dl> <span data-ttu-id="c51a5-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c51a5-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c51a5-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="c51a5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c51a5-130">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="c51a5-130">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
