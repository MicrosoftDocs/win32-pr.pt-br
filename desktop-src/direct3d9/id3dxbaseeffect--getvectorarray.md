---
description: Obtém uma matriz de vetores.
ms.assetid: 75fe454c-75f7-4f03-acd2-dd9cbf94fb96
title: 'Método ID3DXBaseEffect:: GetVectorArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetVectorArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: fa57553b993d5746b54e9a03c6b4e52f71937f0d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298474"
---
# <a name="id3dxbaseeffectgetvectorarray-method"></a><span data-ttu-id="16410-103">Método ID3DXBaseEffect:: GetVectorArray</span><span class="sxs-lookup"><span data-stu-id="16410-103">ID3DXBaseEffect::GetVectorArray method</span></span>

<span data-ttu-id="16410-104">Obtém uma matriz de vetores.</span><span class="sxs-lookup"><span data-stu-id="16410-104">Gets an array of vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="16410-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16410-105">Syntax</span></span>


```C++
HRESULT GetVectorArray(
  [in]  D3DXHANDLE  hParameter,
  [out] D3DXVECTOR4 *pVector,
  [in]  UINT        Count
);
```



## <a name="parameters"></a><span data-ttu-id="16410-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16410-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16410-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="16410-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16410-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="16410-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="16410-109">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="16410-109">Unique identifier.</span></span> <span data-ttu-id="16410-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="16410-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="16410-111">*pVector* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="16410-111">*pVector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16410-112">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="16410-112">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="16410-113">Retorna uma matriz de vetores de ponto flutuante 4D.</span><span class="sxs-lookup"><span data-stu-id="16410-113">Returns an array of 4D floating point vectors.</span></span>

</dd> <dt>

<span data-ttu-id="16410-114">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="16410-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16410-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="16410-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="16410-116">Número de vetores na matriz.</span><span class="sxs-lookup"><span data-stu-id="16410-116">Number of vectors in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16410-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="16410-117">Return value</span></span>

<span data-ttu-id="16410-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="16410-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="16410-119">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="16410-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="16410-120">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="16410-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="16410-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="16410-121">Remarks</span></span>

<span data-ttu-id="16410-122">Se os vetores de destino forem maiores que os vetores de origem, somente os componentes iniciais de cada vetor de destino serão preenchidos e os componentes de vetor de destino restantes serão definidos como zero.</span><span class="sxs-lookup"><span data-stu-id="16410-122">If the destination vectors are larger than the source vectors, only the initial components of each destination vector will be filled, and the remaining destination vector components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="16410-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16410-123">Requirements</span></span>



| <span data-ttu-id="16410-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="16410-124">Requirement</span></span> | <span data-ttu-id="16410-125">Valor</span><span class="sxs-lookup"><span data-stu-id="16410-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="16410-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="16410-126">Header</span></span><br/>  | <dl> <span data-ttu-id="16410-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="16410-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="16410-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="16410-128">Library</span></span><br/> | <dl> <span data-ttu-id="16410-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16410-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="16410-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="16410-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16410-131">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="16410-131">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="16410-132">**SetVectorArray**</span><span class="sxs-lookup"><span data-stu-id="16410-132">**SetVectorArray**</span></span>](id3dxbaseeffect--setvectorarray.md)
</dt> </dl>

 

 
