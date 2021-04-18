---
description: Preenche uma matriz com dados de chave de tradução usados para animação de quadro chave.
ms.assetid: ecb791ad-e586-4057-9239-facd37a47637
title: 'Método ID3DXKeyframedAnimationSet:: GetTranslationKeys (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetTranslationKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d6cc56e5538eb45c01ba7c35115e94719119bc4e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771467"
---
# <a name="id3dxkeyframedanimationsetgettranslationkeys-method"></a><span data-ttu-id="24a02-103">Método ID3DXKeyframedAnimationSet:: GetTranslationKeys</span><span class="sxs-lookup"><span data-stu-id="24a02-103">ID3DXKeyframedAnimationSet::GetTranslationKeys method</span></span>

<span data-ttu-id="24a02-104">Preenche uma matriz com dados de chave de tradução usados para animação de quadro chave.</span><span class="sxs-lookup"><span data-stu-id="24a02-104">Fills an array with translational key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="24a02-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="24a02-105">Syntax</span></span>


```C++
HRESULT GetTranslationKeys(
  [in] UINT              Animation,
  [in] LPD3DXKEY_VECTOR3 pTranslationKeys
);
```



## <a name="parameters"></a><span data-ttu-id="24a02-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24a02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24a02-107">*Animação* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="24a02-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24a02-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="24a02-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="24a02-109">Índice de animação.</span><span class="sxs-lookup"><span data-stu-id="24a02-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="24a02-110">*pTranslationKeys* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="24a02-110">*pTranslationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24a02-111">Tipo: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**</span><span class="sxs-lookup"><span data-stu-id="24a02-111">Type: **[**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)**</span></span>

<span data-ttu-id="24a02-112">Ponteiro para uma matriz alocada pelo usuário de vetores [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) que o método deve preencher com dados de tradução de animação.</span><span class="sxs-lookup"><span data-stu-id="24a02-112">Pointer to a user-allocated array of [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md) vectors that the method is to fill with animation translation data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24a02-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="24a02-113">Return value</span></span>

<span data-ttu-id="24a02-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="24a02-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="24a02-115">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="24a02-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="24a02-116">Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="24a02-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="24a02-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24a02-117">Requirements</span></span>



| <span data-ttu-id="24a02-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="24a02-118">Requirement</span></span> | <span data-ttu-id="24a02-119">Valor</span><span class="sxs-lookup"><span data-stu-id="24a02-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="24a02-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="24a02-120">Header</span></span><br/>  | <dl> <span data-ttu-id="24a02-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="24a02-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="24a02-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="24a02-122">Library</span></span><br/> | <dl> <span data-ttu-id="24a02-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="24a02-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="24a02-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="24a02-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24a02-125">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="24a02-125">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="24a02-126">**ID3DXKeyframedAnimationSet::GetNumTranslationKeys**</span><span class="sxs-lookup"><span data-stu-id="24a02-126">**ID3DXKeyframedAnimationSet::GetNumTranslationKeys**</span></span>](id3dxkeyframedanimationset--getnumtranslationkeys.md)
</dt> </dl>

 

 
