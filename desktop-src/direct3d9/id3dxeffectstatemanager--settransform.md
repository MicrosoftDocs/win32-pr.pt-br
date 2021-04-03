---
description: Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma transformação.
ms.assetid: 5d886554-ddb6-4b8a-a7fd-453e94b9516f
title: 'Método ID3DXEffectStateManager:: SetTransform (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetTransform
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b19a060cfeb09d5d1a92e5e7a1a1f25b58e64f4d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930656"
---
# <a name="id3dxeffectstatemanagersettransform-method"></a><span data-ttu-id="0a5c6-103">Método ID3DXEffectStateManager:: SetTransform</span><span class="sxs-lookup"><span data-stu-id="0a5c6-103">ID3DXEffectStateManager::SetTransform method</span></span>

<span data-ttu-id="0a5c6-104">Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma transformação.</span><span class="sxs-lookup"><span data-stu-id="0a5c6-104">A callback function that must be implemented by a user to set a transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a5c6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a5c6-105">Syntax</span></span>


```C++
HRESULT SetTransform(
  [in]       D3DTRANSFORMSTATETYPE State,
  [in] const D3DMATRIX             *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="0a5c6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a5c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a5c6-107">*Estado* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0a5c6-107">*State* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a5c6-108">Tipo: **[ **D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md)**</span><span class="sxs-lookup"><span data-stu-id="0a5c6-108">Type: **[**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md)**</span></span>

<span data-ttu-id="0a5c6-109">O tipo de transformação ao qual aplicar a matriz.</span><span class="sxs-lookup"><span data-stu-id="0a5c6-109">The type of transform to apply the matrix to.</span></span> <span data-ttu-id="0a5c6-110">Consulte [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md).</span><span class="sxs-lookup"><span data-stu-id="0a5c6-110">See [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a5c6-111">*pMatrix* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0a5c6-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a5c6-112">Tipo: **const [**D3DMATRIX**](d3dmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="0a5c6-112">Type: **const [**D3DMATRIX**](d3dmatrix.md)\***</span></span>

<span data-ttu-id="0a5c6-113">Uma matriz de transformação.</span><span class="sxs-lookup"><span data-stu-id="0a5c6-113">A transformation matrix.</span></span> <span data-ttu-id="0a5c6-114">Consulte [**D3DMATRIX**](d3dmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="0a5c6-114">See [**D3DMATRIX**](d3dmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a5c6-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0a5c6-115">Return value</span></span>

<span data-ttu-id="0a5c6-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0a5c6-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0a5c6-117">O método implementado pelo usuário deve retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0a5c6-117">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="0a5c6-118">Se o retorno de chamada falhar ao definir o estado do dispositivo, ocorrerá uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="0a5c6-118">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="0a5c6-119">O efeito falhará durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="0a5c6-119">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="0a5c6-120">A chamada de estado de efeito dinâmico (como [**IDirect3DDevice9:: SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)) falhará.</span><span class="sxs-lookup"><span data-stu-id="0a5c6-120">The dynamic effect state call (such as [**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a5c6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a5c6-121">Requirements</span></span>



| <span data-ttu-id="0a5c6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a5c6-122">Requirement</span></span> | <span data-ttu-id="0a5c6-123">Valor</span><span class="sxs-lookup"><span data-stu-id="0a5c6-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a5c6-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0a5c6-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0a5c6-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a5c6-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="0a5c6-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0a5c6-126">Library</span></span><br/> | <dl> <span data-ttu-id="0a5c6-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a5c6-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0a5c6-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a5c6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a5c6-129">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="0a5c6-129">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
