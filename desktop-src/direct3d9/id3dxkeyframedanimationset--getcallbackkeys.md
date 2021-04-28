---
description: 'Método ID3DXKeyframedAnimationSet:: GetCallbackKeys – preenche uma matriz com dados de chave de retorno de chamada usados para a animação do quadro chave.'
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
ms.openlocfilehash: 5f3bdb7049de3b5d6aad10b5ff5100d01d05e3ee
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093714"
---
# <a name="id3dxkeyframedanimationsetgetcallbackkeys-method"></a><span data-ttu-id="27d10-103">Método ID3DXKeyframedAnimationSet:: GetCallbackKeys</span><span class="sxs-lookup"><span data-stu-id="27d10-103">ID3DXKeyframedAnimationSet::GetCallbackKeys method</span></span>

<span data-ttu-id="27d10-104">Preenche uma matriz com dados de chave de retorno de chamada usados para animação de quadro chave.</span><span class="sxs-lookup"><span data-stu-id="27d10-104">Fills an array with callback key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="27d10-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="27d10-105">Syntax</span></span>


```C++
HRESULT GetCallbackKeys(
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a><span data-ttu-id="27d10-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="27d10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27d10-107">*pCallbackKeys* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="27d10-107">*pCallbackKeys* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="27d10-108">Tipo: **[ **\_ retorno de chamada LPD3DXKEY**](d3dxkey-callback.md)**</span><span class="sxs-lookup"><span data-stu-id="27d10-108">Type: **[**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)**</span></span>

<span data-ttu-id="27d10-109">Ponteiro para uma matriz alocada pelo usuário de estruturas de [**\_ retorno de chamada D3DXKEY**](d3dxkey-callback.md) que o método deve preencher com dados de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="27d10-109">Pointer to a user-allocated array of [**D3DXKEY\_CALLBACK**](d3dxkey-callback.md) structures that the method is to fill with callback data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27d10-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="27d10-110">Return value</span></span>

<span data-ttu-id="27d10-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="27d10-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="27d10-112">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="27d10-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="27d10-113">Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="27d10-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="27d10-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27d10-114">Requirements</span></span>



| <span data-ttu-id="27d10-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="27d10-115">Requirement</span></span> | <span data-ttu-id="27d10-116">Valor</span><span class="sxs-lookup"><span data-stu-id="27d10-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="27d10-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="27d10-117">Header</span></span><br/>  | <dl> <span data-ttu-id="27d10-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="27d10-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="27d10-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="27d10-119">Library</span></span><br/> | <dl> <span data-ttu-id="27d10-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="27d10-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="27d10-121">Consulte também</span><span class="sxs-lookup"><span data-stu-id="27d10-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27d10-122">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="27d10-122">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="27d10-123">**ID3DXKeyframedAnimationSet::GetNumCallbackKeys**</span><span class="sxs-lookup"><span data-stu-id="27d10-123">**ID3DXKeyframedAnimationSet::GetNumCallbackKeys**</span></span>](id3dxkeyframedanimationset--getnumcallbackkeys.md)
</dt> </dl>

 

 




