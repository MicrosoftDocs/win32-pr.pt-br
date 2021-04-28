---
description: 'Método ID3DXEffectStateManager:: SetVertexShaderConstantF – uma função de retorno de chamada que deve ser implementada por um usuário para definir uma matriz de constantes de ponto flutuante de sombreador de vértice.'
ms.assetid: 3a13040d-5d5a-4454-bf11-cda9653585c0
title: 'Método ID3DXEffectStateManager:: SetVertexShaderConstantF (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShaderConstantF
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ffbad3c695758a0388baf8161c322c1ff423699b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090384"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstantf-method"></a><span data-ttu-id="f72f6-103">Método ID3DXEffectStateManager:: SetVertexShaderConstantF</span><span class="sxs-lookup"><span data-stu-id="f72f6-103">ID3DXEffectStateManager::SetVertexShaderConstantF method</span></span>

<span data-ttu-id="f72f6-104">Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma matriz de constantes de ponto flutuante do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="f72f6-104">A callback function that must be implemented by a user to set an array of vertex shader floating-point constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="f72f6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f72f6-105">Syntax</span></span>


```C++
HRESULT SetVertexShaderConstantF(
  [out]       UINT  StartRegister,
  [out] const FLOAT *pConstantData,
  [out]       UINT  RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="f72f6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f72f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f72f6-107">*StartRegister* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f72f6-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f72f6-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f72f6-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f72f6-109">O índice de base zero da primeira constante registrada.</span><span class="sxs-lookup"><span data-stu-id="f72f6-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="f72f6-110">*pConstantData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f72f6-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f72f6-111">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="f72f6-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f72f6-112">Uma matriz de constantes de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="f72f6-112">An array of floating-point constants.</span></span>

</dd> <dt>

<span data-ttu-id="f72f6-113">*RegisterCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f72f6-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f72f6-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f72f6-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f72f6-115">O número de registros em pConstantData.</span><span class="sxs-lookup"><span data-stu-id="f72f6-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f72f6-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f72f6-116">Return value</span></span>

<span data-ttu-id="f72f6-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f72f6-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f72f6-118">O método implementado pelo usuário deve retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f72f6-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="f72f6-119">Se o retorno de chamada falhar ao definir o estado do dispositivo, ocorrerá uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="f72f6-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="f72f6-120">O efeito falhará durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="f72f6-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="f72f6-121">A chamada de estado de efeito dinâmico (como [**IDirect3DDevice9:: SetVertexShaderConstantF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)) falhará.</span><span class="sxs-lookup"><span data-stu-id="f72f6-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetVertexShaderConstantF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="f72f6-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f72f6-122">Requirements</span></span>



| <span data-ttu-id="f72f6-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f72f6-123">Requirement</span></span> | <span data-ttu-id="f72f6-124">Valor</span><span class="sxs-lookup"><span data-stu-id="f72f6-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f72f6-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f72f6-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f72f6-126"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f72f6-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="f72f6-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f72f6-127">Library</span></span><br/> | <dl> <span data-ttu-id="f72f6-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f72f6-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f72f6-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f72f6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f72f6-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="f72f6-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
