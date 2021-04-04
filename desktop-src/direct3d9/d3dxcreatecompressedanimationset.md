---
description: Cria uma interface de conjunto de animações com quadros-chave ID3DXCompressedAnimationSet que armazena dados de quadro de chave em um formato compactado.
ms.assetid: c3f97d35-5654-4d85-a337-d77819ce3874
title: Função D3DXCreateCompressedAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCompressedAnimationSet
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8aab23466cecf43a50a4136eb0b3d93a271dcb0e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930622"
---
# <a name="d3dxcreatecompressedanimationset-function"></a><span data-ttu-id="d34ef-103">Função D3DXCreateCompressedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="d34ef-103">D3DXCreateCompressedAnimationSet function</span></span>

<span data-ttu-id="d34ef-104">Cria uma interface de conjunto de animações com quadros-chave [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) que armazena dados de quadro de chave em um formato compactado.</span><span class="sxs-lookup"><span data-stu-id="d34ef-104">Creates a [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) key framed animation set interface that stores key frame data in a compressed format.</span></span>

## <a name="syntax"></a><span data-ttu-id="d34ef-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d34ef-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCompressedAnimationSet(
  _In_        LPCSTR                       pName,
  _In_        DOUBLE                       TicksPerSecond,
  _In_        D3DXPLAYBACK_TYPE            Playback,
  _In_        LPD3DXBUFFER                 pCompressedData,
  _In_        UINT                         NumCallbackKeys,
  _In_  const LPD3DXKEY_CALLBACK           *pCallKeys,
  _Out_       LPD3DXCOMPRESSEDANIMATIONSET *ppAnimationSet
);
```



## <a name="parameters"></a><span data-ttu-id="d34ef-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d34ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d34ef-107">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d34ef-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d34ef-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d34ef-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d34ef-109">Ponteiro para o nome do conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="d34ef-109">Pointer to the name of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="d34ef-110">*TicksPerSecond* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d34ef-110">*TicksPerSecond* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d34ef-111">Tipo: **[ **duplo**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d34ef-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d34ef-112">Número de tiques de quadro chave decorridos por segundo.</span><span class="sxs-lookup"><span data-stu-id="d34ef-112">Number of key frame ticks that elapse per second.</span></span>

</dd> <dt>

<span data-ttu-id="d34ef-113">*Reprodução* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d34ef-113">*Playback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d34ef-114">Tipo: **[ **\_ tipo de D3DXPLAYBACK**](./d3dxplayback-type.md)**</span><span class="sxs-lookup"><span data-stu-id="d34ef-114">Type: **[**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md)**</span></span>

<span data-ttu-id="d34ef-115">Tipo do loop de reprodução do conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="d34ef-115">Type of the animation set playback loop.</span></span> <span data-ttu-id="d34ef-116">Consulte [**\_ tipo de D3DXPLAYBACK**](./d3dxplayback-type.md).</span><span class="sxs-lookup"><span data-stu-id="d34ef-116">See [**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="d34ef-117">*pCompressedData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d34ef-117">*pCompressedData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d34ef-118">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="d34ef-118">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)**</span></span>

<span data-ttu-id="d34ef-119">Ponteiro para o buffer [**ID3DXBuffer**](id3dxbuffer.md) que armazena a animação definida como dados compactados.</span><span class="sxs-lookup"><span data-stu-id="d34ef-119">Pointer to the [**ID3DXBuffer**](id3dxbuffer.md) buffer that stores the animation set as compressed data.</span></span>

</dd> <dt>

<span data-ttu-id="d34ef-120">*NumCallbackKeys* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d34ef-120">*NumCallbackKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d34ef-121">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d34ef-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d34ef-122">Número de chaves de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="d34ef-122">Number of callback keys.</span></span>

</dd> <dt>

<span data-ttu-id="d34ef-123">*pCallKeys* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d34ef-123">*pCallKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d34ef-124">Tipo: **[**retorno de \_ chamada**](d3dxkey-callback.md) \* const LPD3DXKEY**</span><span class="sxs-lookup"><span data-stu-id="d34ef-124">Type: **const [**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)\***</span></span>

<span data-ttu-id="d34ef-125">Ponteiro para uma estrutura de [**\_ retorno de chamada D3DXKEY**](d3dxkey-callback.md) que armazena dados de retorno de chamada do usuário.</span><span class="sxs-lookup"><span data-stu-id="d34ef-125">Pointer to a [**D3DXKEY\_CALLBACK**](d3dxkey-callback.md) structure that stores user callback data.</span></span>

</dd> <dt>

<span data-ttu-id="d34ef-126">*ppAnimationSet* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d34ef-126">*ppAnimationSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d34ef-127">Tipo: **[ **LPD3DXCOMPRESSEDANIMATIONSET**](id3dxcompressedanimationset.md)\***</span><span class="sxs-lookup"><span data-stu-id="d34ef-127">Type: **[**LPD3DXCOMPRESSEDANIMATIONSET**](id3dxcompressedanimationset.md)\***</span></span>

<span data-ttu-id="d34ef-128">Endereço de um ponteiro para a interface [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) que armazena dados de quadros de animação de chave definida em um formato compactado.</span><span class="sxs-lookup"><span data-stu-id="d34ef-128">Address of a pointer to the [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) interface that stores key framed animation set data in a compressed format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d34ef-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d34ef-129">Return value</span></span>

<span data-ttu-id="d34ef-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d34ef-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d34ef-131">Se a função for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d34ef-131">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d34ef-132">Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="d34ef-132">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="d34ef-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d34ef-133">Requirements</span></span>



| <span data-ttu-id="d34ef-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="d34ef-134">Requirement</span></span> | <span data-ttu-id="d34ef-135">Valor</span><span class="sxs-lookup"><span data-stu-id="d34ef-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d34ef-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d34ef-136">Header</span></span><br/>  | <dl> <span data-ttu-id="d34ef-137"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="d34ef-137"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="d34ef-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d34ef-138">Library</span></span><br/> | <dl> <span data-ttu-id="d34ef-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d34ef-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d34ef-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="d34ef-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d34ef-141">Funções de animação</span><span class="sxs-lookup"><span data-stu-id="d34ef-141">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
