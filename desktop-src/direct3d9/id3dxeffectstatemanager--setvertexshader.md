---
description: Uma função de retorno de chamada que deve ser implementada por um usuário para definir um sombreador de vértice.
ms.assetid: 8f3d3be3-c073-441d-a318-6d2cd5e7aca5
title: 'Método ID3DXEffectStateManager:: SetVertexShader (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 9fd25158f2aa6ab0a22d6226e8e709c3b498b0e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837959"
---
# <a name="id3dxeffectstatemanagersetvertexshader-method"></a><span data-ttu-id="5fe66-103">Método ID3DXEffectStateManager:: SetVertexShader</span><span class="sxs-lookup"><span data-stu-id="5fe66-103">ID3DXEffectStateManager::SetVertexShader method</span></span>

<span data-ttu-id="5fe66-104">Uma função de retorno de chamada que deve ser implementada por um usuário para definir um sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="5fe66-104">A callback function that must be implemented by a user to set a vertex shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fe66-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5fe66-105">Syntax</span></span>


```C++
HRESULT SetVertexShader(
  [in] LPDIRECT3DVERTEXSHADER9 pShader
);
```



## <a name="parameters"></a><span data-ttu-id="5fe66-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5fe66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fe66-107">*pShader* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5fe66-107">*pShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fe66-108">Tipo: **[ **LPDIRECT3DVERTEXSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9)**</span><span class="sxs-lookup"><span data-stu-id="5fe66-108">Type: **[**LPDIRECT3DVERTEXSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9)**</span></span>

<span data-ttu-id="5fe66-109">Um ponteiro para um objeto de sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="5fe66-109">A pointer to a vertex shader object.</span></span> <span data-ttu-id="5fe66-110">Consulte [**IDirect3DVertexShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9).</span><span class="sxs-lookup"><span data-stu-id="5fe66-110">See [**IDirect3DVertexShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fe66-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5fe66-111">Return value</span></span>

<span data-ttu-id="5fe66-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5fe66-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5fe66-113">O método implementado pelo usuário deve retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5fe66-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="5fe66-114">Se o retorno de chamada falhar ao definir o estado do dispositivo, ocorrerá uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="5fe66-114">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="5fe66-115">O efeito falhará durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="5fe66-115">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="5fe66-116">A chamada de estado de efeito dinâmico (como [**IDirect3DDevice9:: SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader)) falhará.</span><span class="sxs-lookup"><span data-stu-id="5fe66-116">The dynamic effect state call (such as [**IDirect3DDevice9::SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fe66-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5fe66-117">Requirements</span></span>



| <span data-ttu-id="5fe66-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fe66-118">Requirement</span></span> | <span data-ttu-id="5fe66-119">Valor</span><span class="sxs-lookup"><span data-stu-id="5fe66-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fe66-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5fe66-120">Header</span></span><br/>  | <dl> <span data-ttu-id="5fe66-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fe66-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="5fe66-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5fe66-122">Library</span></span><br/> | <dl> <span data-ttu-id="5fe66-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5fe66-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5fe66-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="5fe66-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fe66-125">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="5fe66-125">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
