---
description: Dimensiona todos os exemplos associados a uma determinada submalha. O método é útil para computar a dispersão da subsuperfície.
ms.assetid: abb9ca6a-5fc2-4986-8a38-29998fe5e537
title: 'Método ID3DXPRTEngine:: ScaleMeshChunk (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ScaleMeshChunk
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f688a5175e7b50c33dd93d06a4f988a14c062c86
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105811617"
---
# <a name="id3dxprtenginescalemeshchunk-method"></a><span data-ttu-id="d2c55-104">Método ID3DXPRTEngine:: ScaleMeshChunk</span><span class="sxs-lookup"><span data-stu-id="d2c55-104">ID3DXPRTEngine::ScaleMeshChunk method</span></span>

<span data-ttu-id="d2c55-105">Dimensiona todos os exemplos associados a uma determinada submalha.</span><span class="sxs-lookup"><span data-stu-id="d2c55-105">Scales all the samples associated with a given submesh.</span></span> <span data-ttu-id="d2c55-106">O método é útil para computar a dispersão da subsuperfície.</span><span class="sxs-lookup"><span data-stu-id="d2c55-106">The method is useful for computing subsurface scattering.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2c55-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2c55-107">Syntax</span></span>


```C++
HRESULT ScaleMeshChunk(
  [in]      UINT            uMeshChunk,
  [in]      FLOAT           fScale,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="d2c55-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2c55-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2c55-109">*uMeshChunk* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d2c55-109">*uMeshChunk* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2c55-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d2c55-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d2c55-111">Local na malha na qual começar a dimensionar amostras.</span><span class="sxs-lookup"><span data-stu-id="d2c55-111">Location in the mesh at which to start scaling samples.</span></span>

</dd> <dt>

<span data-ttu-id="d2c55-112">*fScale* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d2c55-112">*fScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2c55-113">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d2c55-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d2c55-114">Valor pelo qual multiplicar cada vetor na submalha.</span><span class="sxs-lookup"><span data-stu-id="d2c55-114">Value by which to multiply each vector in the submesh.</span></span>

</dd> <dt>

<span data-ttu-id="d2c55-115">*pDataOut* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="d2c55-115">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2c55-116">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="d2c55-116">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="d2c55-117">Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) para receber amostras redimensionadas na submalha.</span><span class="sxs-lookup"><span data-stu-id="d2c55-117">Pointer to a [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object to receive rescaled samples in the submesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2c55-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d2c55-118">Return value</span></span>

<span data-ttu-id="d2c55-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d2c55-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d2c55-120">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d2c55-120">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d2c55-121">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="d2c55-121">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2c55-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2c55-122">Requirements</span></span>



| <span data-ttu-id="d2c55-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2c55-123">Requirement</span></span> | <span data-ttu-id="d2c55-124">Valor</span><span class="sxs-lookup"><span data-stu-id="d2c55-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2c55-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d2c55-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d2c55-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2c55-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d2c55-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d2c55-127">Library</span></span><br/> | <dl> <span data-ttu-id="d2c55-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2c55-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d2c55-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2c55-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2c55-130">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="d2c55-130">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
