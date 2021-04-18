---
description: Definir informações de tradução para um quadro-chave específico no conjunto de animações.
ms.assetid: 4a926c0f-6d57-48d4-bb3b-60766fc78e40
title: 'Método ID3DXKeyframedAnimationSet:: SetTranslationKey (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.SetTranslationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5bdfb8fb02a2b06dc797317d35cc14e75bd6f221
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105815534"
---
# <a name="id3dxkeyframedanimationsetsettranslationkey-method"></a><span data-ttu-id="2bcc5-103">Método ID3DXKeyframedAnimationSet:: SetTranslationKey</span><span class="sxs-lookup"><span data-stu-id="2bcc5-103">ID3DXKeyframedAnimationSet::SetTranslationKey method</span></span>

<span data-ttu-id="2bcc5-104">Definir informações de tradução para um quadro-chave específico no conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="2bcc5-104">Set translation information for a specific key frame in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bcc5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2bcc5-105">Syntax</span></span>


```C++
HRESULT SetTranslationKey(
  [in] UINT              Animation,
  [in] UINT              Key,
  [in] LPD3DXKEY_VECTOR3 pTranslationKey
);
```



## <a name="parameters"></a><span data-ttu-id="2bcc5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2bcc5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bcc5-107">*Animação* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2bcc5-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bcc5-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2bcc5-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2bcc5-109">Índice de animação.</span><span class="sxs-lookup"><span data-stu-id="2bcc5-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="2bcc5-110">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2bcc5-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bcc5-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2bcc5-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2bcc5-112">Quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="2bcc5-112">Key Frame.</span></span>

</dd> <dt>

<span data-ttu-id="2bcc5-113">*pTranslationKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2bcc5-113">*pTranslationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bcc5-114">Tipo: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**</span><span class="sxs-lookup"><span data-stu-id="2bcc5-114">Type: **[**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)**</span></span>

<span data-ttu-id="2bcc5-115">Ponteiro para os dados de tradução.</span><span class="sxs-lookup"><span data-stu-id="2bcc5-115">Pointer to the translation data.</span></span> <span data-ttu-id="2bcc5-116">Consulte [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md).</span><span class="sxs-lookup"><span data-stu-id="2bcc5-116">See [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bcc5-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2bcc5-117">Return value</span></span>

<span data-ttu-id="2bcc5-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2bcc5-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2bcc5-119">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2bcc5-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2bcc5-120">Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="2bcc5-120">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bcc5-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2bcc5-121">Requirements</span></span>



| <span data-ttu-id="2bcc5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bcc5-122">Requirement</span></span> | <span data-ttu-id="2bcc5-123">Valor</span><span class="sxs-lookup"><span data-stu-id="2bcc5-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2bcc5-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2bcc5-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2bcc5-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bcc5-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="2bcc5-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2bcc5-126">Library</span></span><br/> | <dl> <span data-ttu-id="2bcc5-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2bcc5-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2bcc5-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="2bcc5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bcc5-129">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="2bcc5-129">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
