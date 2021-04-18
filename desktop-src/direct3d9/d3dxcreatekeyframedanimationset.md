---
description: Cria uma interface de conjunto de animação de chave ID3DXKeyframedAnimationSet com quadros.
ms.assetid: 7b4fffdc-696c-400c-a0cc-fc755fd25b75
title: Função D3DXCreateKeyframedAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateKeyframedAnimationSet
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3f3eb45e999d25c776014c3df5824e0468d03ffd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105813567"
---
# <a name="d3dxcreatekeyframedanimationset-function"></a><span data-ttu-id="deda9-103">Função D3DXCreateKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="deda9-103">D3DXCreateKeyframedAnimationSet function</span></span>

<span data-ttu-id="deda9-104">Cria uma interface de conjunto de animação de chave [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) com quadros.</span><span class="sxs-lookup"><span data-stu-id="deda9-104">Creates a [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) key framed animation set interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="deda9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="deda9-105">Syntax</span></span>


```C++
HRESULT D3DXCreateKeyframedAnimationSet(
  _In_        LPCSTR                      pName,
  _In_        DOUBLE                      TicksPerSecond,
  _In_        D3DXPLAYBACK_TYPE           Playback,
  _In_        UINT                        NumAnimations,
  _In_        UINT                        NumCallbackKeys,
  _In_  const LPD3DXKEY_CALLBACK          *pCallKeys,
  _Out_       LPD3DXKEYFRAMEDANIMATIONSET *ppAnimationSet
);
```



## <a name="parameters"></a><span data-ttu-id="deda9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="deda9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="deda9-107">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="deda9-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deda9-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="deda9-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="deda9-109">Ponteiro para o nome do conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="deda9-109">Pointer to the name of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="deda9-110">*TicksPerSecond* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="deda9-110">*TicksPerSecond* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deda9-111">Tipo: **[ **duplo**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="deda9-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="deda9-112">Número de tiques de quadro chave decorridos por segundo.</span><span class="sxs-lookup"><span data-stu-id="deda9-112">Number of key frame ticks that elapse per second.</span></span>

</dd> <dt>

<span data-ttu-id="deda9-113">*Reprodução* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="deda9-113">*Playback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deda9-114">Tipo: **[ **\_ tipo de D3DXPLAYBACK**](./d3dxplayback-type.md)**</span><span class="sxs-lookup"><span data-stu-id="deda9-114">Type: **[**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md)**</span></span>

<span data-ttu-id="deda9-115">Tipo do loop de reprodução do conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="deda9-115">Type of the animation set playback loop.</span></span> <span data-ttu-id="deda9-116">Consulte [**\_ tipo de D3DXPLAYBACK**](./d3dxplayback-type.md).</span><span class="sxs-lookup"><span data-stu-id="deda9-116">See [**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="deda9-117">*NumAnimations* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="deda9-117">*NumAnimations* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deda9-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="deda9-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="deda9-119">Número de conjuntos de animação de escala, girar e traduzir (SRT).</span><span class="sxs-lookup"><span data-stu-id="deda9-119">Number of scale, rotate, and translate (SRT) animation sets.</span></span>

</dd> <dt>

<span data-ttu-id="deda9-120">*NumCallbackKeys* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="deda9-120">*NumCallbackKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deda9-121">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="deda9-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="deda9-122">Número de chaves de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="deda9-122">Number of callback keys.</span></span>

</dd> <dt>

<span data-ttu-id="deda9-123">*pCallKeys* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="deda9-123">*pCallKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deda9-124">Tipo: **[**retorno de \_ chamada**](d3dxkey-callback.md) \* const LPD3DXKEY**</span><span class="sxs-lookup"><span data-stu-id="deda9-124">Type: **const [**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)\***</span></span>

<span data-ttu-id="deda9-125">Ponteiro para uma estrutura de [**\_ retorno de chamada D3DXKEY**](d3dxkey-callback.md) que armazena dados de retorno de chamada do usuário.</span><span class="sxs-lookup"><span data-stu-id="deda9-125">Pointer to a [**D3DXKEY\_CALLBACK**](d3dxkey-callback.md) structure that stores user callback data.</span></span>

</dd> <dt>

<span data-ttu-id="deda9-126">*ppAnimationSet* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="deda9-126">*ppAnimationSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="deda9-127">Tipo: **[ **LPD3DXKEYFRAMEDANIMATIONSET**](id3dxkeyframedanimationset.md)\***</span><span class="sxs-lookup"><span data-stu-id="deda9-127">Type: **[**LPD3DXKEYFRAMEDANIMATIONSET**](id3dxkeyframedanimationset.md)\***</span></span>

<span data-ttu-id="deda9-128">Endereço de um ponteiro para a interface do conjunto de animações com quadros chave [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) .</span><span class="sxs-lookup"><span data-stu-id="deda9-128">Address of a pointer to the [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) key framed animation set interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="deda9-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="deda9-129">Return value</span></span>

<span data-ttu-id="deda9-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="deda9-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="deda9-131">Se a função for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="deda9-131">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="deda9-132">Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="deda9-132">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="deda9-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="deda9-133">Requirements</span></span>



| <span data-ttu-id="deda9-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="deda9-134">Requirement</span></span> | <span data-ttu-id="deda9-135">Valor</span><span class="sxs-lookup"><span data-stu-id="deda9-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="deda9-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="deda9-136">Header</span></span><br/>  | <dl> <span data-ttu-id="deda9-137"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="deda9-137"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="deda9-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="deda9-138">Library</span></span><br/> | <dl> <span data-ttu-id="deda9-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="deda9-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="deda9-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="deda9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deda9-141">Funções de animação</span><span class="sxs-lookup"><span data-stu-id="deda9-141">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
