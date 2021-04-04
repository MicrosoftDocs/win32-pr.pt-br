---
description: Uma função de retorno de chamada que deve ser implementada por um usuário para definir o número de segmentos de subdivisão para N-patches.
ms.assetid: f94910ee-3385-44d3-b4f1-a0e88c7afa39
title: 'Método ID3DXEffectStateManager:: SetNPatchMode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetNPatchMode
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 9b8725a0482b6945b04013df43d34a502f25b7b9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930744"
---
# <a name="id3dxeffectstatemanagersetnpatchmode-method"></a><span data-ttu-id="c754b-103">Método ID3DXEffectStateManager:: SetNPatchMode</span><span class="sxs-lookup"><span data-stu-id="c754b-103">ID3DXEffectStateManager::SetNPatchMode method</span></span>

<span data-ttu-id="c754b-104">Uma função de retorno de chamada que deve ser implementada por um usuário para definir o número de segmentos de subdivisão para N-patches.</span><span class="sxs-lookup"><span data-stu-id="c754b-104">A callback function that must be implemented by a user to set the number of subdivision segments for N-patches.</span></span>

## <a name="syntax"></a><span data-ttu-id="c754b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c754b-105">Syntax</span></span>


```C++
HRESULT SetNPatchMode(
  [in] FLOAT nSegments
);
```



## <a name="parameters"></a><span data-ttu-id="c754b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c754b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c754b-107">*nSegments* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c754b-107">*nSegments* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c754b-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c754b-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c754b-109">Quebre a superfície nesse número de subdivisãos.</span><span class="sxs-lookup"><span data-stu-id="c754b-109">Break the surface into this number of subdivisions.</span></span> <span data-ttu-id="c754b-110">Isso é o mesmo que o número usado por [**IDirect3DDevice9:: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span><span class="sxs-lookup"><span data-stu-id="c754b-110">This is the same as the number used by [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c754b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c754b-111">Return value</span></span>

<span data-ttu-id="c754b-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c754b-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c754b-113">O método implementado pelo usuário deve retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c754b-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="c754b-114">Se o retorno de chamada falhar ao definir o estado do dispositivo, ocorrerá uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="c754b-114">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="c754b-115">O efeito falhará durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="c754b-115">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="c754b-116">A chamada de estado de efeito dinâmico (como [**IDirect3DDevice9:: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)) falhará.</span><span class="sxs-lookup"><span data-stu-id="c754b-116">The dynamic effect state call (such as [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="c754b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c754b-117">Requirements</span></span>



| <span data-ttu-id="c754b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c754b-118">Requirement</span></span> | <span data-ttu-id="c754b-119">Valor</span><span class="sxs-lookup"><span data-stu-id="c754b-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c754b-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c754b-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c754b-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c754b-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="c754b-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c754b-122">Library</span></span><br/> | <dl> <span data-ttu-id="c754b-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c754b-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c754b-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="c754b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c754b-125">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="c754b-125">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
