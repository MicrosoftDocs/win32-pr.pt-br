---
description: 'Método ID3DXEffectStateManager:: SetPixelShaderConstantI – uma função de retorno de chamada que deve ser implementada por um usuário para definir uma matriz de constantes de inteiro de sombreador de vértice.'
ms.assetid: 55f5747d-b7f8-4d13-ac2c-df2dcb160091
title: 'Método ID3DXEffectStateManager:: SetPixelShaderConstantI (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetPixelShaderConstantI
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 53eab5993ee737efe866c73a550e6b216edaac3b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090474"
---
# <a name="id3dxeffectstatemanagersetpixelshaderconstanti-method"></a><span data-ttu-id="434c5-103">Método ID3DXEffectStateManager:: SetPixelShaderConstantI</span><span class="sxs-lookup"><span data-stu-id="434c5-103">ID3DXEffectStateManager::SetPixelShaderConstantI method</span></span>

<span data-ttu-id="434c5-104">Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma matriz de constantes de inteiro de sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="434c5-104">A callback function that must be implemented by a user to set an array of vertex shader integer constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="434c5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="434c5-105">Syntax</span></span>


```C++
HRESULT SetPixelShaderConstantI(
  [out]       UINT StartRegister,
  [out] const INT  *pConstantData,
  [out]       UINT RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="434c5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="434c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="434c5-107">*StartRegister* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="434c5-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="434c5-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="434c5-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="434c5-109">O índice de base zero da primeira constante registrada.</span><span class="sxs-lookup"><span data-stu-id="434c5-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="434c5-110">*pConstantData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="434c5-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="434c5-111">Tipo: **const [**int**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="434c5-111">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="434c5-112">Uma matriz de constantes de inteiro.</span><span class="sxs-lookup"><span data-stu-id="434c5-112">An array of integer constants.</span></span>

</dd> <dt>

<span data-ttu-id="434c5-113">*RegisterCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="434c5-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="434c5-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="434c5-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="434c5-115">O número de registros em pConstantData.</span><span class="sxs-lookup"><span data-stu-id="434c5-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="434c5-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="434c5-116">Return value</span></span>

<span data-ttu-id="434c5-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="434c5-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="434c5-118">O método implementado pelo usuário deve retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="434c5-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="434c5-119">Se o retorno de chamada falhar ao definir o estado do dispositivo, ocorrerá uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="434c5-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="434c5-120">O efeito falhará durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="434c5-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="434c5-121">A chamada de estado de efeito dinâmico (como [**IDirect3DDevice9:: SetPixelShaderConstantI**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)) falhará.</span><span class="sxs-lookup"><span data-stu-id="434c5-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetPixelShaderConstantI**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="434c5-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="434c5-122">Requirements</span></span>



| <span data-ttu-id="434c5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="434c5-123">Requirement</span></span> | <span data-ttu-id="434c5-124">Valor</span><span class="sxs-lookup"><span data-stu-id="434c5-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="434c5-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="434c5-125">Header</span></span><br/>  | <dl> <span data-ttu-id="434c5-126"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="434c5-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="434c5-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="434c5-127">Library</span></span><br/> | <dl> <span data-ttu-id="434c5-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="434c5-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="434c5-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="434c5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="434c5-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="434c5-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
