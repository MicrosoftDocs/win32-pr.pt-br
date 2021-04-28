---
description: 'Método ID3DXAnimationSet:: getcallback – Obtém informações sobre um retorno de chamada específico no conjunto de animações.'
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
ms.openlocfilehash: 563c1007cc471ab10a9609e776da69b7c5ed493b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097534"
---
# <a name="id3dxanimationsetgetcallback-method"></a><span data-ttu-id="5a4e8-103">Método ID3DXAnimationSet:: getcallback</span><span class="sxs-lookup"><span data-stu-id="5a4e8-103">ID3DXAnimationSet::GetCallback method</span></span>

<span data-ttu-id="5a4e8-104">Obtém informações sobre um retorno de chamada específico no conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="5a4e8-104">Gets information about a specific callback in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a4e8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5a4e8-105">Syntax</span></span>


```C++
HRESULT GetCallback(
  [in]  DOUBLE Position,
  [in]  DWORD  Flags,
  [out] DOUBLE *pCallbackPosition,
  [out] LPVOID *ppCallbackData
);
```



## <a name="parameters"></a><span data-ttu-id="5a4e8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5a4e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a4e8-107">*Posição* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5a4e8-107">*Position* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a4e8-108">Tipo: **[ **duplo**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a4e8-108">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5a4e8-109">Posição a partir da qual encontrar retornos de chamada.</span><span class="sxs-lookup"><span data-stu-id="5a4e8-109">Position from which to find callbacks.</span></span>

</dd> <dt>

<span data-ttu-id="5a4e8-110">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="5a4e8-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a4e8-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a4e8-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5a4e8-112">Sinalizadores de pesquisa de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="5a4e8-112">Callback search flags.</span></span> <span data-ttu-id="5a4e8-113">Esse parâmetro pode ser definido como uma combinação de um ou mais sinalizadores de [**\_ \_ sinalizadores de pesquisa do D3DXCALLBACK**](./d3dxcallback-search-flags.md).</span><span class="sxs-lookup"><span data-stu-id="5a4e8-113">This parameter can be set to a combination of one or more flags from [**D3DXCALLBACK\_SEARCH\_FLAGS**](./d3dxcallback-search-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a4e8-114">*pCallbackPosition* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5a4e8-114">*pCallbackPosition* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a4e8-115">Tipo: **[ **duplo**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a4e8-115">Type: **[**DOUBLE**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5a4e8-116">Ponteiro para a posição do retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="5a4e8-116">Pointer to the position of the callback.</span></span>

</dd> <dt>

<span data-ttu-id="5a4e8-117">*ppCallbackData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5a4e8-117">*ppCallbackData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a4e8-118">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a4e8-118">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5a4e8-119">Endereço do ponteiro de dados de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="5a4e8-119">Address of the callback data pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a4e8-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="5a4e8-120">Return value</span></span>

<span data-ttu-id="5a4e8-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5a4e8-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5a4e8-122">Os valores de retorno desse método são implementados por um programador de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="5a4e8-122">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="5a4e8-123">Em geral, se nenhum erro ocorrer, Programe o método para retornar o D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5a4e8-123">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="5a4e8-124">Caso contrário, Programe o método para retornar uma mensagem de erro apropriada de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md).</span><span class="sxs-lookup"><span data-stu-id="5a4e8-124">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a4e8-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a4e8-125">Requirements</span></span>



| <span data-ttu-id="5a4e8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a4e8-126">Requirement</span></span> | <span data-ttu-id="5a4e8-127">Valor</span><span class="sxs-lookup"><span data-stu-id="5a4e8-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a4e8-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5a4e8-128">Header</span></span><br/>  | <dl> <span data-ttu-id="5a4e8-129"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a4e8-129"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="5a4e8-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5a4e8-130">Library</span></span><br/> | <dl> <span data-ttu-id="5a4e8-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a4e8-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5a4e8-132">Consulte também</span><span class="sxs-lookup"><span data-stu-id="5a4e8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a4e8-133">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="5a4e8-133">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
