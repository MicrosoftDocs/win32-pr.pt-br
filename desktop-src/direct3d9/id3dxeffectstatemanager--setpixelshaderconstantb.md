---
description: Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma matriz de constantes booleanas do sombreador de vértice.
ms.assetid: ad4d9beb-fd34-4574-9787-61bd3bfaaaaa
title: 'Método ID3DXEffectStateManager:: SetPixelShaderConstantB (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetPixelShaderConstantB
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e3c3c988bdbfa84a3e815fe94d89c24f3fa3a264
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105768315"
---
# <a name="id3dxeffectstatemanagersetpixelshaderconstantb-method"></a><span data-ttu-id="85af8-103">Método ID3DXEffectStateManager:: SetPixelShaderConstantB</span><span class="sxs-lookup"><span data-stu-id="85af8-103">ID3DXEffectStateManager::SetPixelShaderConstantB method</span></span>

<span data-ttu-id="85af8-104">Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma matriz de constantes booleanas do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="85af8-104">A callback function that must be implemented by a user to set an array of vertex shader Boolean constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="85af8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="85af8-105">Syntax</span></span>


```C++
HRESULT SetPixelShaderConstantB(
  [out]       UINT StartRegister,
  [out] const BOOL *pConstantData,
  [out]       UINT RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="85af8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="85af8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85af8-107">*StartRegister* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="85af8-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85af8-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="85af8-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="85af8-109">O índice de base zero da primeira constante registrada.</span><span class="sxs-lookup"><span data-stu-id="85af8-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="85af8-110">*pConstantData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="85af8-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85af8-111">Tipo: **const [**bool**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="85af8-111">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="85af8-112">Uma matriz de constantes boolianas.</span><span class="sxs-lookup"><span data-stu-id="85af8-112">An array of Boolean constants.</span></span>

</dd> <dt>

<span data-ttu-id="85af8-113">*RegisterCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="85af8-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85af8-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="85af8-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="85af8-115">O número de registros em pConstantData.</span><span class="sxs-lookup"><span data-stu-id="85af8-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85af8-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="85af8-116">Return value</span></span>

<span data-ttu-id="85af8-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="85af8-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="85af8-118">O método implementado pelo usuário deve retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="85af8-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="85af8-119">Se o retorno de chamada falhar ao definir o estado do dispositivo, ocorrerá uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="85af8-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="85af8-120">O efeito falhará durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="85af8-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="85af8-121">A chamada de estado de efeito dinâmico (como [**IDirect3DDevice9:: SetPixelShaderConstantB**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)) falhará.</span><span class="sxs-lookup"><span data-stu-id="85af8-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetPixelShaderConstantB**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="85af8-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85af8-122">Requirements</span></span>



| <span data-ttu-id="85af8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="85af8-123">Requirement</span></span> | <span data-ttu-id="85af8-124">Valor</span><span class="sxs-lookup"><span data-stu-id="85af8-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="85af8-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="85af8-125">Header</span></span><br/>  | <dl> <span data-ttu-id="85af8-126"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="85af8-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="85af8-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="85af8-127">Library</span></span><br/> | <dl> <span data-ttu-id="85af8-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85af8-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="85af8-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="85af8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85af8-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="85af8-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
