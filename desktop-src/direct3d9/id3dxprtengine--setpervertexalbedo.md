---
description: Define um valor de albedo para cada vértice de malha, substituindo valores de albedo anteriores.
ms.assetid: 5220dfe3-8d41-480c-a850-b9aad3d2bb2f
title: 'Método ID3DXPRTEngine:: SetPerVertexAlbedo (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerVertexAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da7a33a79cc50963e87d0eff15baf22ee8d79ce3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105752752"
---
# <a name="id3dxprtenginesetpervertexalbedo-method"></a><span data-ttu-id="ac0dc-103">Método ID3DXPRTEngine:: SetPerVertexAlbedo</span><span class="sxs-lookup"><span data-stu-id="ac0dc-103">ID3DXPRTEngine::SetPerVertexAlbedo method</span></span>

<span data-ttu-id="ac0dc-104">Define um valor de albedo para cada vértice de malha, substituindo valores de albedo anteriores.</span><span class="sxs-lookup"><span data-stu-id="ac0dc-104">Sets an albedo value for each mesh vertex, overwriting previous albedo values.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac0dc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ac0dc-105">Syntax</span></span>


```C++
HRESULT SetPerVertexAlbedo(
  [in] const VOID *pDataIn,
  [in]       UINT NumChannels,
  [in]       UINT Stride
);
```



## <a name="parameters"></a><span data-ttu-id="ac0dc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac0dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac0dc-107">*pDataIn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ac0dc-107">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac0dc-108">Tipo: **const void \***</span><span class="sxs-lookup"><span data-stu-id="ac0dc-108">Type: **const VOID\***</span></span>

<span data-ttu-id="ac0dc-109">Ponteiro para FLUTUAr dados albedo do primeiro exemplo.</span><span class="sxs-lookup"><span data-stu-id="ac0dc-109">Pointer to FLOAT albedo data of the first sample.</span></span>

</dd> <dt>

<span data-ttu-id="ac0dc-110">*NumChannels* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ac0dc-110">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac0dc-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac0dc-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ac0dc-112">Número de canais de cores a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="ac0dc-112">Number of color channels to set.</span></span> <span data-ttu-id="ac0dc-113">Defina como 1 para especificar os materiais em cinza (R = G = B) ou 3 para habilitar os efeitos de sangramento de cor.</span><span class="sxs-lookup"><span data-stu-id="ac0dc-113">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span>

</dd> <dt>

<span data-ttu-id="ac0dc-114">*Stride* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ac0dc-114">*Stride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac0dc-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac0dc-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ac0dc-116">Stride em bytes necessário para chegar ao valor de albedo do próximo exemplo.</span><span class="sxs-lookup"><span data-stu-id="ac0dc-116">Stride in bytes needed to get to next sample's albedo value.</span></span> <span data-ttu-id="ac0dc-117">Consulte [largura vs. pitch (Direct3D 9)](width-vs--pitch.md).</span><span class="sxs-lookup"><span data-stu-id="ac0dc-117">See [Width vs. Pitch (Direct3D 9)](width-vs--pitch.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac0dc-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ac0dc-118">Return value</span></span>

<span data-ttu-id="ac0dc-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ac0dc-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ac0dc-120">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ac0dc-120">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ac0dc-121">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ac0dc-121">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac0dc-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac0dc-122">Requirements</span></span>



| <span data-ttu-id="ac0dc-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac0dc-123">Requirement</span></span> | <span data-ttu-id="ac0dc-124">Valor</span><span class="sxs-lookup"><span data-stu-id="ac0dc-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac0dc-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ac0dc-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ac0dc-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac0dc-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ac0dc-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ac0dc-127">Library</span></span><br/> | <dl> <span data-ttu-id="ac0dc-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac0dc-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ac0dc-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac0dc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac0dc-130">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="ac0dc-130">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
