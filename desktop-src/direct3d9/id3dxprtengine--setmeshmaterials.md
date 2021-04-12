---
description: Define as propriedades de material de malha na cena 3D. Use este método para especificar os parâmetros de dispersão de subsuperfície.
ms.assetid: 830d73be-bba6-454d-8476-341d291a5b2e
title: 'Método ID3DXPRTEngine:: SetMeshMaterials (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetMeshMaterials
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c90ae72cab5d7a20c2c65b940d28a9b57902d2d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298786"
---
# <a name="id3dxprtenginesetmeshmaterials-method"></a><span data-ttu-id="5ed32-104">Método ID3DXPRTEngine:: SetMeshMaterials</span><span class="sxs-lookup"><span data-stu-id="5ed32-104">ID3DXPRTEngine::SetMeshMaterials method</span></span>

<span data-ttu-id="5ed32-105">Define as propriedades de material de malha na cena 3D.</span><span class="sxs-lookup"><span data-stu-id="5ed32-105">Sets mesh material properties in the 3D scene.</span></span> <span data-ttu-id="5ed32-106">Use este método para especificar os parâmetros de dispersão de subsuperfície.</span><span class="sxs-lookup"><span data-stu-id="5ed32-106">Use this method to specify subsurface scattering parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ed32-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5ed32-107">Syntax</span></span>


```C++
HRESULT SetMeshMaterials(
  [in] const D3DXSHMATERIAL **ppMaterials,
  [in]       UINT           NumMeshes,
  [in]       UINT           NumChannels,
  [in]       BOOL           bSetAlbedo,
  [in]       FLOAT          fLengthScale
);
```



## <a name="parameters"></a><span data-ttu-id="5ed32-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5ed32-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ed32-109">*ppMaterials* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5ed32-109">*ppMaterials* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ed32-110">Tipo: **const [**D3DXSHMATERIAL**](d3dxshmaterial.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="5ed32-110">Type: **const [**D3DXSHMATERIAL**](d3dxshmaterial.md)\*\***</span></span>

<span data-ttu-id="5ed32-111">Endereço de um ponteiro para as propriedades de material de malha desejadas.</span><span class="sxs-lookup"><span data-stu-id="5ed32-111">Address of a pointer to desired mesh material properties.</span></span> <span data-ttu-id="5ed32-112">Consulte [**D3DXSHMATERIAL**](d3dxshmaterial.md).</span><span class="sxs-lookup"><span data-stu-id="5ed32-112">See [**D3DXSHMATERIAL**](d3dxshmaterial.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ed32-113">*NumMeshes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5ed32-113">*NumMeshes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ed32-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ed32-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ed32-115">Índice da malha na qual definir as propriedades do material.</span><span class="sxs-lookup"><span data-stu-id="5ed32-115">Index of the mesh on which to set material properties.</span></span>

</dd> <dt>

<span data-ttu-id="5ed32-116">*NumChannels* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5ed32-116">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ed32-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ed32-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ed32-118">Número de canais de cores a serem definidos na malha.</span><span class="sxs-lookup"><span data-stu-id="5ed32-118">Number of color channels to set in the mesh.</span></span> <span data-ttu-id="5ed32-119">Defina como 1 para especificar os materiais em cinza (R = G = B) ou 3 para habilitar os efeitos de sangramento de cor.</span><span class="sxs-lookup"><span data-stu-id="5ed32-119">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span> <span data-ttu-id="5ed32-120">Se você pretende alterar esse parâmetro, primeiro defina o albedo usando outro método, como [**ID3DXPRTEngine:: SetPerTexelAlbedo**](id3dxprtengine--setpertexelalbedo.md) ou [**ID3DXPRTEngine:: SetPerVertexAlbedo**](id3dxprtengine--setpervertexalbedo.md).</span><span class="sxs-lookup"><span data-stu-id="5ed32-120">If you intend to change this parameter, first set the albedo using another method such as [**ID3DXPRTEngine::SetPerTexelAlbedo**](id3dxprtengine--setpertexelalbedo.md) or [**ID3DXPRTEngine::SetPerVertexAlbedo**](id3dxprtengine--setpervertexalbedo.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ed32-121">*bSetAlbedo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5ed32-121">*bSetAlbedo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ed32-122">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ed32-122">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ed32-123">Se **for true**, define o albedo da malha como ppMaterials, substituindo todos os valores existentes de albedo Texel e Vertex.</span><span class="sxs-lookup"><span data-stu-id="5ed32-123">If **TRUE**, sets the albedo of the mesh to ppMaterials, overwriting all existing texel and vertex albedo values.</span></span> <span data-ttu-id="5ed32-124">Se **for false**, preservará todos os valores existentes de albedo Texel e Vertex definidos por outros métodos; NumChannels deve corresponder ao parâmetro NumChannels usado para criar o buffer em [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) ou [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md).</span><span class="sxs-lookup"><span data-stu-id="5ed32-124">If **FALSE**, preserves all existing texel and vertex albedo values set by other methods; NumChannels must match the NumChannels parameter used to create the buffer in [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) or [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ed32-125">*fLengthScale* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5ed32-125">*fLengthScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ed32-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ed32-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ed32-127">Escala da cena 3D em relação a um cubo de 1 mm.</span><span class="sxs-lookup"><span data-stu-id="5ed32-127">Scale of the 3D scene relative to a 1-mm cube.</span></span> <span data-ttu-id="5ed32-128">Usado para computações de dispersão de subsuperfície.</span><span class="sxs-lookup"><span data-stu-id="5ed32-128">Used for subsurface scattering computations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ed32-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5ed32-129">Return value</span></span>

<span data-ttu-id="5ed32-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5ed32-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5ed32-131">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5ed32-131">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5ed32-132">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="5ed32-132">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ed32-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ed32-133">Requirements</span></span>



| <span data-ttu-id="5ed32-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ed32-134">Requirement</span></span> | <span data-ttu-id="5ed32-135">Valor</span><span class="sxs-lookup"><span data-stu-id="5ed32-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed32-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ed32-136">Header</span></span><br/>  | <dl> <span data-ttu-id="5ed32-137"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ed32-137"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="5ed32-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5ed32-138">Library</span></span><br/> | <dl> <span data-ttu-id="5ed32-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ed32-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5ed32-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="5ed32-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ed32-141">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="5ed32-141">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
