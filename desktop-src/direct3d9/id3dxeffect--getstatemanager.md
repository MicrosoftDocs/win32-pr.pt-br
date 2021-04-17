---
description: Obtenha o Gerenciador de estado do efeito.
ms.assetid: 4a09eb2a-2393-40b0-81b9-3c27998c2b77
title: 'Método ID3DXEffect:: getstatemanager (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.GetStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 293b642dfecfa4cc14426addf2567d43dffa7233
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105782470"
---
# <a name="id3dxeffectgetstatemanager-method"></a><span data-ttu-id="882db-103">Método ID3DXEffect:: getstatemanager</span><span class="sxs-lookup"><span data-stu-id="882db-103">ID3DXEffect::GetStateManager method</span></span>

<span data-ttu-id="882db-104">Obtenha o Gerenciador de estado do efeito.</span><span class="sxs-lookup"><span data-stu-id="882db-104">Get the effect state manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="882db-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="882db-105">Syntax</span></span>


```C++
HRESULT GetStateManager(
  [out] LPD3DXEFFECTSTATEMANAGER *ppManager
);
```



## <a name="parameters"></a><span data-ttu-id="882db-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="882db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="882db-107">*ppManager* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="882db-107">*ppManager* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="882db-108">Tipo: **[ **LPD3DXEFFECTSTATEMANAGER**](id3dxeffectstatemanager.md)\***</span><span class="sxs-lookup"><span data-stu-id="882db-108">Type: **[**LPD3DXEFFECTSTATEMANAGER**](id3dxeffectstatemanager.md)\***</span></span>

<span data-ttu-id="882db-109">Retorna um ponteiro para o Gerenciador de estado.</span><span class="sxs-lookup"><span data-stu-id="882db-109">Returns a pointer to the state manager.</span></span> <span data-ttu-id="882db-110">Consulte [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md).</span><span class="sxs-lookup"><span data-stu-id="882db-110">See [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="882db-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="882db-111">Return value</span></span>

<span data-ttu-id="882db-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="882db-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="882db-113">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="882db-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="882db-114">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="882db-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="882db-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="882db-115">Remarks</span></span>

<span data-ttu-id="882db-116">O [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md) é uma interface implementada pelo usuário que fornece retornos de chamada em um aplicativo para definir o estado do dispositivo de um efeito.</span><span class="sxs-lookup"><span data-stu-id="882db-116">The [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md) is a user-implemented interface that furnishes callbacks into an application for setting device state from an effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="882db-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="882db-117">Requirements</span></span>



| <span data-ttu-id="882db-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="882db-118">Requirement</span></span> | <span data-ttu-id="882db-119">Valor</span><span class="sxs-lookup"><span data-stu-id="882db-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="882db-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="882db-120">Header</span></span><br/>  | <dl> <span data-ttu-id="882db-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="882db-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="882db-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="882db-122">Library</span></span><br/> | <dl> <span data-ttu-id="882db-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="882db-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="882db-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="882db-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="882db-125">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="882db-125">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="882db-126">**ID3DXEffect:: setstatemanager**</span><span class="sxs-lookup"><span data-stu-id="882db-126">**ID3DXEffect::SetStateManager**</span></span>](id3dxeffect--setstatemanager.md)
</dt> </dl>

 

 




