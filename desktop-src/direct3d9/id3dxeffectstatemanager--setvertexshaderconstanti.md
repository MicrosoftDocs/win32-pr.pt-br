---
description: 'Método ID3DXEffectStateManager:: SetVertexShaderConstantI – uma função de retorno de chamada que deve ser implementada por um usuário para definir uma matriz de constantes de inteiro de sombreador de vértice.'
ms.assetid: 0035c97a-1b17-4665-9032-7b3b9a9d2cff
title: 'Método ID3DXEffectStateManager:: SetVertexShaderConstantI (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShaderConstantI
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c129e3e01fe6fbae6ba7ede1b9ea8c4bee5338a4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090394"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstanti-method"></a><span data-ttu-id="86b30-103">Método ID3DXEffectStateManager:: SetVertexShaderConstantI</span><span class="sxs-lookup"><span data-stu-id="86b30-103">ID3DXEffectStateManager::SetVertexShaderConstantI method</span></span>

<span data-ttu-id="86b30-104">Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma matriz de constantes de inteiro de sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="86b30-104">A callback function that must be implemented by a user to set an array of vertex shader integer constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="86b30-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="86b30-105">Syntax</span></span>


```C++
HRESULT SetVertexShaderConstantI(
  [out]       UINT StartRegister,
  [out] const INT  *pConstantData,
  [out]       UINT RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="86b30-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="86b30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86b30-107">*StartRegister* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="86b30-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86b30-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="86b30-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="86b30-109">O índice de base zero da primeira constante registrada.</span><span class="sxs-lookup"><span data-stu-id="86b30-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="86b30-110">*pConstantData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="86b30-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86b30-111">Tipo: **const [**int**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="86b30-111">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="86b30-112">Uma matriz de constantes de inteiro.</span><span class="sxs-lookup"><span data-stu-id="86b30-112">An array of integer constants.</span></span>

</dd> <dt>

<span data-ttu-id="86b30-113">*RegisterCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="86b30-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86b30-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="86b30-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="86b30-115">O número de registros em pConstantData.</span><span class="sxs-lookup"><span data-stu-id="86b30-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86b30-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="86b30-116">Return value</span></span>

<span data-ttu-id="86b30-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="86b30-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="86b30-118">O método implementado pelo usuário deve retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="86b30-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="86b30-119">Se o retorno de chamada falhar ao definir o estado do dispositivo, ocorrerá uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="86b30-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="86b30-120">O efeito falhará durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="86b30-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="86b30-121">A chamada de estado de efeito dinâmico (como [**IDirect3DDevice9:: SetVertexShaderConstantI**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti)) falhará.</span><span class="sxs-lookup"><span data-stu-id="86b30-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetVertexShaderConstantI**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="86b30-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86b30-122">Requirements</span></span>



| <span data-ttu-id="86b30-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="86b30-123">Requirement</span></span> | <span data-ttu-id="86b30-124">Valor</span><span class="sxs-lookup"><span data-stu-id="86b30-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="86b30-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="86b30-125">Header</span></span><br/>  | <dl> <span data-ttu-id="86b30-126"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="86b30-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="86b30-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="86b30-127">Library</span></span><br/> | <dl> <span data-ttu-id="86b30-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86b30-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="86b30-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="86b30-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86b30-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="86b30-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
