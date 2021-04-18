---
description: Obtém uma descrição de passagem.
ms.assetid: 44c65a82-bcf4-49f5-9312-8320e133bb2f
title: 'Método ID3DXBaseEffect:: GetPassDesc (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPassDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 15a997470fddf5056b7191fcc3226ad210724041
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105764246"
---
# <a name="id3dxbaseeffectgetpassdesc-method"></a><span data-ttu-id="7ea65-103">Método ID3DXBaseEffect:: GetPassDesc</span><span class="sxs-lookup"><span data-stu-id="7ea65-103">ID3DXBaseEffect::GetPassDesc method</span></span>

<span data-ttu-id="7ea65-104">Obtém uma descrição de passagem.</span><span class="sxs-lookup"><span data-stu-id="7ea65-104">Gets a pass description.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ea65-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ea65-105">Syntax</span></span>


```C++
HRESULT GetPassDesc(
  [in]  D3DXHANDLE    hPass,
  [out] D3DXPASS_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="7ea65-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7ea65-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ea65-107">*hPass* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7ea65-107">*hPass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ea65-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="7ea65-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="7ea65-109">Ponteiro de passagem.</span><span class="sxs-lookup"><span data-stu-id="7ea65-109">Pass handle.</span></span> <span data-ttu-id="7ea65-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="7ea65-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ea65-111">*pDesc* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7ea65-111">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ea65-112">Tipo: **[ **D3DXPASS \_ desc**](d3dxpass-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="7ea65-112">Type: **[**D3DXPASS\_DESC**](d3dxpass-desc.md)\***</span></span>

<span data-ttu-id="7ea65-113">Retorna uma descrição da passagem especificada.</span><span class="sxs-lookup"><span data-stu-id="7ea65-113">Returns a description of the specified pass.</span></span> <span data-ttu-id="7ea65-114">Consulte [**D3DXPASS \_ desc**](d3dxpass-desc.md).</span><span class="sxs-lookup"><span data-stu-id="7ea65-114">See [**D3DXPASS\_DESC**](d3dxpass-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ea65-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7ea65-115">Return value</span></span>

<span data-ttu-id="7ea65-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7ea65-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7ea65-117">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7ea65-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="7ea65-118">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="7ea65-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ea65-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ea65-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7ea65-120">Se um efeito for criado com [D3DXFX \_ não \_ clonável](d3dxfx.md), esse método retornará ponteiros **nulos** (em [**D3DXPASS \_ desc**](d3dxpass-desc.md)) para as funções de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7ea65-120">If an effect is created with [D3DXFX\_NOT\_CLONEABLE](d3dxfx.md), this method will return **NULL** pointers (in [**D3DXPASS\_DESC**](d3dxpass-desc.md)) to the shader functions.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7ea65-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ea65-121">Requirements</span></span>



| <span data-ttu-id="7ea65-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ea65-122">Requirement</span></span> | <span data-ttu-id="7ea65-123">Valor</span><span class="sxs-lookup"><span data-stu-id="7ea65-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ea65-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7ea65-124">Header</span></span><br/>  | <dl> <span data-ttu-id="7ea65-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ea65-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="7ea65-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7ea65-126">Library</span></span><br/> | <dl> <span data-ttu-id="7ea65-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ea65-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7ea65-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ea65-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ea65-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="7ea65-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 




