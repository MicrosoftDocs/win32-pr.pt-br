---
description: Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma matriz de constantes de inteiro de sombreador de vértice.
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
ms.openlocfilehash: be95d678ee6b0c44dc49e180df4d3332a84d5fe7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105814564"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstanti-method"></a><span data-ttu-id="c6775-103">Método ID3DXEffectStateManager:: SetVertexShaderConstantI</span><span class="sxs-lookup"><span data-stu-id="c6775-103">ID3DXEffectStateManager::SetVertexShaderConstantI method</span></span>

<span data-ttu-id="c6775-104">Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma matriz de constantes de inteiro de sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="c6775-104">A callback function that must be implemented by a user to set an array of vertex shader integer constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6775-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c6775-105">Syntax</span></span>


```C++
HRESULT SetVertexShaderConstantI(
  [out]       UINT StartRegister,
  [out] const INT  *pConstantData,
  [out]       UINT RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="c6775-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c6775-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6775-107">*StartRegister* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c6775-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6775-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c6775-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c6775-109">O índice de base zero da primeira constante registrada.</span><span class="sxs-lookup"><span data-stu-id="c6775-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="c6775-110">*pConstantData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c6775-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6775-111">Tipo: **const [**int**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="c6775-111">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c6775-112">Uma matriz de constantes de inteiro.</span><span class="sxs-lookup"><span data-stu-id="c6775-112">An array of integer constants.</span></span>

</dd> <dt>

<span data-ttu-id="c6775-113">*RegisterCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c6775-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6775-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c6775-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c6775-115">O número de registros em pConstantData.</span><span class="sxs-lookup"><span data-stu-id="c6775-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6775-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c6775-116">Return value</span></span>

<span data-ttu-id="c6775-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c6775-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c6775-118">O método implementado pelo usuário deve retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c6775-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="c6775-119">Se o retorno de chamada falhar ao definir o estado do dispositivo, ocorrerá uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="c6775-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="c6775-120">O efeito falhará durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="c6775-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="c6775-121">A chamada de estado de efeito dinâmico (como [**IDirect3DDevice9:: SetVertexShaderConstantI**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti)) falhará.</span><span class="sxs-lookup"><span data-stu-id="c6775-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetVertexShaderConstantI**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6775-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6775-122">Requirements</span></span>



| <span data-ttu-id="c6775-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6775-123">Requirement</span></span> | <span data-ttu-id="c6775-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c6775-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6775-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c6775-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c6775-126"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6775-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="c6775-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c6775-127">Library</span></span><br/> | <dl> <span data-ttu-id="c6775-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c6775-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c6775-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6775-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6775-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="c6775-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
