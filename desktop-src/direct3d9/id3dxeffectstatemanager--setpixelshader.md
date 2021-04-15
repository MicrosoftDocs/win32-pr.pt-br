---
description: Uma função de retorno de chamada que deve ser implementada por um usuário para definir um sombreador de pixel.
ms.assetid: 4124eff2-1d88-429c-b7ed-8d87155b5ddc
title: 'Método ID3DXEffectStateManager:: SetPixelShader (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetPixelShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 71a16bc267df95ed7efc1e0f74871b131e34ebe1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506503"
---
# <a name="id3dxeffectstatemanagersetpixelshader-method"></a><span data-ttu-id="b6526-103">Método ID3DXEffectStateManager:: SetPixelShader</span><span class="sxs-lookup"><span data-stu-id="b6526-103">ID3DXEffectStateManager::SetPixelShader method</span></span>

<span data-ttu-id="b6526-104">Uma função de retorno de chamada que deve ser implementada por um usuário para definir um sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="b6526-104">A callback function that must be implemented by a user to set a pixel shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6526-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b6526-105">Syntax</span></span>


```C++
HRESULT SetPixelShader(
  [in] LPDIRECT3DPIXELSHADER9 pShader
);
```



## <a name="parameters"></a><span data-ttu-id="b6526-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6526-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6526-107">*pShader* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b6526-107">*pShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6526-108">Tipo: **[ **LPDIRECT3DPIXELSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9)**</span><span class="sxs-lookup"><span data-stu-id="b6526-108">Type: **[**LPDIRECT3DPIXELSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9)**</span></span>

<span data-ttu-id="b6526-109">Um ponteiro para um objeto de sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="b6526-109">A pointer to a pixel shader object.</span></span> <span data-ttu-id="b6526-110">Consulte [**IDirect3DPixelShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9).</span><span class="sxs-lookup"><span data-stu-id="b6526-110">See [**IDirect3DPixelShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6526-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b6526-111">Return value</span></span>

<span data-ttu-id="b6526-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b6526-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b6526-113">O método implementado pelo usuário deve retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b6526-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="b6526-114">Se o retorno de chamada falhar ao definir o estado do dispositivo, ocorrerá uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="b6526-114">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="b6526-115">O efeito falhará durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="b6526-115">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="b6526-116">A chamada de estado de efeito dinâmico (como [**IDirect3DDevice9:: SetPixelShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader)) falhará.</span><span class="sxs-lookup"><span data-stu-id="b6526-116">The dynamic effect state call (such as [**IDirect3DDevice9::SetPixelShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6526-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6526-117">Requirements</span></span>



| <span data-ttu-id="b6526-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6526-118">Requirement</span></span> | <span data-ttu-id="b6526-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b6526-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6526-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b6526-120">Header</span></span><br/>  | <dl> <span data-ttu-id="b6526-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6526-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="b6526-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b6526-122">Library</span></span><br/> | <dl> <span data-ttu-id="b6526-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6526-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b6526-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6526-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6526-125">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="b6526-125">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
