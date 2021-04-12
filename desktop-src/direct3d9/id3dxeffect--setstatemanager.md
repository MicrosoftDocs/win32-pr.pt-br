---
description: Defina o Gerenciador de estado do efeito.
ms.assetid: 87409687-03f1-4593-ae58-3a8ba08e592b
title: 'Método ID3DXEffect:: setstatemanager (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.SetStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: bb32e3f668884a6f51bd5c5058a4f27e141f0aa3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370928"
---
# <a name="id3dxeffectsetstatemanager-method"></a><span data-ttu-id="27151-103">Método ID3DXEffect:: setstatemanager</span><span class="sxs-lookup"><span data-stu-id="27151-103">ID3DXEffect::SetStateManager method</span></span>

<span data-ttu-id="27151-104">Defina o Gerenciador de estado do efeito.</span><span class="sxs-lookup"><span data-stu-id="27151-104">Set the effect state manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="27151-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="27151-105">Syntax</span></span>


```C++
HRESULT SetStateManager(
  [in] LPD3DXEFFECTSTATEMANAGER pManager
);
```



## <a name="parameters"></a><span data-ttu-id="27151-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="27151-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27151-107">*pManager* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="27151-107">*pManager* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27151-108">Tipo: **[ **LPD3DXEFFECTSTATEMANAGER**](id3dxeffectstatemanager.md)**</span><span class="sxs-lookup"><span data-stu-id="27151-108">Type: **[**LPD3DXEFFECTSTATEMANAGER**](id3dxeffectstatemanager.md)**</span></span>

<span data-ttu-id="27151-109">Um ponteiro para o Gerenciador de estado.</span><span class="sxs-lookup"><span data-stu-id="27151-109">A pointer to the state manager.</span></span> <span data-ttu-id="27151-110">Consulte [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md).</span><span class="sxs-lookup"><span data-stu-id="27151-110">See [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27151-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="27151-111">Return value</span></span>

<span data-ttu-id="27151-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="27151-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="27151-113">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="27151-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="27151-114">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="27151-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="27151-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="27151-115">Remarks</span></span>

<span data-ttu-id="27151-116">O [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md) é uma interface implementada pelo usuário que fornece retornos de chamada em um aplicativo para definir o estado do dispositivo de um efeito.</span><span class="sxs-lookup"><span data-stu-id="27151-116">The [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md) is a user-implemented interface that furnishes callbacks into an application for setting device state from an effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="27151-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27151-117">Requirements</span></span>



| <span data-ttu-id="27151-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="27151-118">Requirement</span></span> | <span data-ttu-id="27151-119">Valor</span><span class="sxs-lookup"><span data-stu-id="27151-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="27151-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="27151-120">Header</span></span><br/>  | <dl> <span data-ttu-id="27151-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="27151-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="27151-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="27151-122">Library</span></span><br/> | <dl> <span data-ttu-id="27151-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="27151-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="27151-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="27151-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27151-125">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="27151-125">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="27151-126">**ID3DXEffect:: getstatemanager**</span><span class="sxs-lookup"><span data-stu-id="27151-126">**ID3DXEffect::GetStateManager**</span></span>](id3dxeffect--getstatemanager.md)
</dt> </dl>

 

 




