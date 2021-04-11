---
description: Obtém informações sobre um retorno de chamada específico no conjunto de animações.
ms.assetid: e8388bfc-5438-4216-a98f-dd0dbca12c87
title: 'Método ID3DXAnimationSet:: getcallback (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetCallback
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f4cde6c9d51fd29c0412f33b34ca7bea8260dfea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173187"
---
# <a name="id3dxanimationsetgetcallback-method"></a><span data-ttu-id="7473d-103">Método ID3DXAnimationSet:: getcallback</span><span class="sxs-lookup"><span data-stu-id="7473d-103">ID3DXAnimationSet::GetCallback method</span></span>

<span data-ttu-id="7473d-104">Obtém informações sobre um retorno de chamada específico no conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="7473d-104">Gets information about a specific callback in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="7473d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7473d-105">Syntax</span></span>


```C++
HRESULT GetCallback(
  [in]  DOUBLE Position,
  [in]  DWORD  Flags,
  [out] DOUBLE *pCallbackPosition,
  [out] LPVOID *ppCallbackData
);
```



## <a name="parameters"></a><span data-ttu-id="7473d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7473d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7473d-107">*Posição* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7473d-107">*Position* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7473d-108">Tipo: **[ **duplo**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7473d-108">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7473d-109">Posição a partir da qual encontrar retornos de chamada.</span><span class="sxs-lookup"><span data-stu-id="7473d-109">Position from which to find callbacks.</span></span>

</dd> <dt>

<span data-ttu-id="7473d-110">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="7473d-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7473d-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7473d-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7473d-112">Sinalizadores de pesquisa de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="7473d-112">Callback search flags.</span></span> <span data-ttu-id="7473d-113">Esse parâmetro pode ser definido como uma combinação de um ou mais sinalizadores de [**\_ \_ sinalizadores de pesquisa do D3DXCALLBACK**](./d3dxcallback-search-flags.md).</span><span class="sxs-lookup"><span data-stu-id="7473d-113">This parameter can be set to a combination of one or more flags from [**D3DXCALLBACK\_SEARCH\_FLAGS**](./d3dxcallback-search-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="7473d-114">*pCallbackPosition* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7473d-114">*pCallbackPosition* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7473d-115">Tipo: **[ **duplo**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7473d-115">Type: **[**DOUBLE**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7473d-116">Ponteiro para a posição do retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="7473d-116">Pointer to the position of the callback.</span></span>

</dd> <dt>

<span data-ttu-id="7473d-117">*ppCallbackData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7473d-117">*ppCallbackData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7473d-118">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7473d-118">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7473d-119">Endereço do ponteiro de dados de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="7473d-119">Address of the callback data pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7473d-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7473d-120">Return value</span></span>

<span data-ttu-id="7473d-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7473d-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7473d-122">Os valores de retorno desse método são implementados por um programador de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="7473d-122">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="7473d-123">Em geral, se nenhum erro ocorrer, Programe o método para retornar o D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7473d-123">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="7473d-124">Caso contrário, Programe o método para retornar uma mensagem de erro apropriada de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md).</span><span class="sxs-lookup"><span data-stu-id="7473d-124">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7473d-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7473d-125">Requirements</span></span>



| <span data-ttu-id="7473d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7473d-126">Requirement</span></span> | <span data-ttu-id="7473d-127">Valor</span><span class="sxs-lookup"><span data-stu-id="7473d-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7473d-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7473d-128">Header</span></span><br/>  | <dl> <span data-ttu-id="7473d-129"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="7473d-129"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="7473d-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7473d-130">Library</span></span><br/> | <dl> <span data-ttu-id="7473d-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7473d-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7473d-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="7473d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7473d-133">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="7473d-133">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
