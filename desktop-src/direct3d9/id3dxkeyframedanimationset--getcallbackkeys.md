---
description: Preenche uma matriz com dados de chave de retorno de chamada usados para animação de quadro chave.
ms.assetid: 2a2aa04a-a889-415b-8aa2-cc5f2bed1f9a
title: 'Método ID3DXKeyframedAnimationSet:: GetCallbackKeys (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetCallbackKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d3f8dbc771fcdde6d1c07a1bf810b322b0a70a30
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172945"
---
# <a name="id3dxkeyframedanimationsetgetcallbackkeys-method"></a><span data-ttu-id="a357b-103">Método ID3DXKeyframedAnimationSet:: GetCallbackKeys</span><span class="sxs-lookup"><span data-stu-id="a357b-103">ID3DXKeyframedAnimationSet::GetCallbackKeys method</span></span>

<span data-ttu-id="a357b-104">Preenche uma matriz com dados de chave de retorno de chamada usados para animação de quadro chave.</span><span class="sxs-lookup"><span data-stu-id="a357b-104">Fills an array with callback key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a357b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a357b-105">Syntax</span></span>


```C++
HRESULT GetCallbackKeys(
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a><span data-ttu-id="a357b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a357b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a357b-107">*pCallbackKeys* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a357b-107">*pCallbackKeys* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a357b-108">Tipo: **[ **\_ retorno de chamada LPD3DXKEY**](d3dxkey-callback.md)**</span><span class="sxs-lookup"><span data-stu-id="a357b-108">Type: **[**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)**</span></span>

<span data-ttu-id="a357b-109">Ponteiro para uma matriz alocada pelo usuário de estruturas de [**\_ retorno de chamada D3DXKEY**](d3dxkey-callback.md) que o método deve preencher com dados de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="a357b-109">Pointer to a user-allocated array of [**D3DXKEY\_CALLBACK**](d3dxkey-callback.md) structures that the method is to fill with callback data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a357b-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a357b-110">Return value</span></span>

<span data-ttu-id="a357b-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a357b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a357b-112">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a357b-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a357b-113">Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a357b-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="a357b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a357b-114">Requirements</span></span>



| <span data-ttu-id="a357b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a357b-115">Requirement</span></span> | <span data-ttu-id="a357b-116">Valor</span><span class="sxs-lookup"><span data-stu-id="a357b-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a357b-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a357b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a357b-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="a357b-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="a357b-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a357b-119">Library</span></span><br/> | <dl> <span data-ttu-id="a357b-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a357b-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a357b-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="a357b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a357b-122">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="a357b-122">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="a357b-123">**ID3DXKeyframedAnimationSet::GetNumCallbackKeys**</span><span class="sxs-lookup"><span data-stu-id="a357b-123">**ID3DXKeyframedAnimationSet::GetNumCallbackKeys**</span></span>](id3dxkeyframedanimationset--getnumcallbackkeys.md)
</dt> </dl>

 

 




