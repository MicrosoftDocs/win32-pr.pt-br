---
description: Uma função de retorno de chamada que deve ser implementada por um usuário para definir o estado do estágio de textura.
ms.assetid: cc86a483-ccf0-400d-b14d-ab55a3cf4b98
title: 'Método ID3DXEffectStateManager:: SetTextureStageState (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetTextureStageState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 937fd3f2b89dc093d9dceb9441f53d6be2cb06b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105754700"
---
# <a name="id3dxeffectstatemanagersettexturestagestate-method"></a><span data-ttu-id="f719c-103">Método ID3DXEffectStateManager:: SetTextureStageState</span><span class="sxs-lookup"><span data-stu-id="f719c-103">ID3DXEffectStateManager::SetTextureStageState method</span></span>

<span data-ttu-id="f719c-104">Uma função de retorno de chamada que deve ser implementada por um usuário para definir o estado do estágio de textura.</span><span class="sxs-lookup"><span data-stu-id="f719c-104">A callback function that must be implemented by a user to set the texture stage state.</span></span>

## <a name="syntax"></a><span data-ttu-id="f719c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f719c-105">Syntax</span></span>


```C++
HRESULT SetTextureStageState(
  [in] DWORD                    Stage,
  [in] D3DTEXTURESTAGESTATETYPE Type,
  [in] DWORD                    Value
);
```



## <a name="parameters"></a><span data-ttu-id="f719c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f719c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f719c-107">*Stage* \[in\]</span><span class="sxs-lookup"><span data-stu-id="f719c-107">*Stage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f719c-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f719c-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f719c-109">O estágio ao qual a textura está atribuída.</span><span class="sxs-lookup"><span data-stu-id="f719c-109">The stage that the texture is assigned to.</span></span> <span data-ttu-id="f719c-110">Este é o valor de índice em [**IDirect3DDevice9:: SetTexture**](/windows/desktop/api) ou [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span><span class="sxs-lookup"><span data-stu-id="f719c-110">This is the index value in [**IDirect3DDevice9::SetTexture**](/windows/desktop/api) or [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span></span>

</dd> <dt>

<span data-ttu-id="f719c-111">*Tipo* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="f719c-111">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f719c-112">Tipo: **[ **D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)**</span><span class="sxs-lookup"><span data-stu-id="f719c-112">Type: **[**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)**</span></span>

<span data-ttu-id="f719c-113">Define o tipo de operação que um estágio de textura executará.</span><span class="sxs-lookup"><span data-stu-id="f719c-113">Defines the type of operation that a texture stage will perform.</span></span> <span data-ttu-id="f719c-114">Consulte [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).</span><span class="sxs-lookup"><span data-stu-id="f719c-114">See [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="f719c-115">*Valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="f719c-115">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f719c-116">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f719c-116">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f719c-117">Pode ser uma operação ([**D3DTEXTUREOP**](./d3dtextureop.md)) ou um valor de argumento ([D3DTA](d3dta.md)), dependendo do que é escolhido para o tipo.</span><span class="sxs-lookup"><span data-stu-id="f719c-117">Can be either an operation ([**D3DTEXTUREOP**](./d3dtextureop.md)) or an argument value ([D3DTA](d3dta.md)), depending on what is chosen for Type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f719c-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f719c-118">Return value</span></span>

<span data-ttu-id="f719c-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f719c-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f719c-120">O método implementado pelo usuário deve retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f719c-120">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="f719c-121">Se o retorno de chamada falhar ao definir o estado do dispositivo, ocorrerá uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="f719c-121">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="f719c-122">O efeito falhará durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="f719c-122">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="f719c-123">A chamada de estado de efeito dinâmico (como [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)) falhará.</span><span class="sxs-lookup"><span data-stu-id="f719c-123">The dynamic effect state call (such as [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="f719c-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f719c-124">Requirements</span></span>



| <span data-ttu-id="f719c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f719c-125">Requirement</span></span> | <span data-ttu-id="f719c-126">Valor</span><span class="sxs-lookup"><span data-stu-id="f719c-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f719c-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f719c-127">Header</span></span><br/>  | <dl> <span data-ttu-id="f719c-128"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f719c-128"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="f719c-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f719c-129">Library</span></span><br/> | <dl> <span data-ttu-id="f719c-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f719c-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f719c-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="f719c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f719c-132">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="f719c-132">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
