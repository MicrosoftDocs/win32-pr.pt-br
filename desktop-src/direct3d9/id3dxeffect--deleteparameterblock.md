---
description: Excluir um bloco de parâmetro.
ms.assetid: 5502dabc-1703-481b-a69d-f6bd8fd01d20
title: 'ID3DXEffect: método eleteParameterBlock de:D (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.DeleteParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 483b09ebf308b8cdfa14d714bc74786e5fcb1f83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105772608"
---
# <a name="id3dxeffectdeleteparameterblock-method"></a><span data-ttu-id="faf7b-103">ID3DXEffect: método eleteParameterBlock de:D</span><span class="sxs-lookup"><span data-stu-id="faf7b-103">ID3DXEffect::DeleteParameterBlock method</span></span>

<span data-ttu-id="faf7b-104">Excluir um bloco de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="faf7b-104">Delete a parameter block.</span></span>

## <a name="syntax"></a><span data-ttu-id="faf7b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="faf7b-105">Syntax</span></span>


```C++
HRESULT DeleteParameterBlock(
  [in] D3DXHANDLE  hParameterBlock
);
```



## <a name="parameters"></a><span data-ttu-id="faf7b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="faf7b-106">Parameters</span></span>

<dl> <dt>

 <span data-ttu-id="faf7b-107">*hParameterBlock* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="faf7b-107">*hParameterBlock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="faf7b-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="faf7b-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="faf7b-109">Um identificador para o bloco de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="faf7b-109">A handle to the parameter block.</span></span> <span data-ttu-id="faf7b-110">Esse é o identificador retornado por [**ID3DXEffect:: EndParameterBlock**](id3dxeffect--endparameterblock.md).</span><span class="sxs-lookup"><span data-stu-id="faf7b-110">This is the handle returned by [**ID3DXEffect::EndParameterBlock**](id3dxeffect--endparameterblock.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="faf7b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="faf7b-111">Return value</span></span>

<span data-ttu-id="faf7b-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="faf7b-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="faf7b-113">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="faf7b-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="faf7b-114">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="faf7b-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="faf7b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="faf7b-115">Remarks</span></span>

<span data-ttu-id="faf7b-116">Os blocos de parâmetro são blocos de Estados de efeito.</span><span class="sxs-lookup"><span data-stu-id="faf7b-116">Parameter blocks are blocks of effect states.</span></span> <span data-ttu-id="faf7b-117">Use um bloco de parâmetro para registrar alterações de estado para que elas possam ser aplicadas posteriormente com uma única chamada à API.</span><span class="sxs-lookup"><span data-stu-id="faf7b-117">Use a parameter block to record state changes so that they can be applied later on with a single API call.</span></span> <span data-ttu-id="faf7b-118">Quando não for mais necessário, exclua o bloco de parâmetro para reduzir o uso de memória.</span><span class="sxs-lookup"><span data-stu-id="faf7b-118">When no longer needed, delete the parameter block to reduce memory usage.</span></span>

## <a name="requirements"></a><span data-ttu-id="faf7b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="faf7b-119">Requirements</span></span>



| <span data-ttu-id="faf7b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="faf7b-120">Requirement</span></span> | <span data-ttu-id="faf7b-121">Valor</span><span class="sxs-lookup"><span data-stu-id="faf7b-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="faf7b-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="faf7b-122">Header</span></span><br/>  | <dl> <span data-ttu-id="faf7b-123"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="faf7b-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="faf7b-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="faf7b-124">Library</span></span><br/> | <dl> <span data-ttu-id="faf7b-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="faf7b-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="faf7b-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="faf7b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faf7b-127">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="faf7b-127">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="faf7b-128">**ID3DXEffect::BeginParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="faf7b-128">**ID3DXEffect::BeginParameterBlock**</span></span>](id3dxeffect--beginparameterblock.md)
</dt> <dt>

[<span data-ttu-id="faf7b-129">**ID3DXEffect::EndParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="faf7b-129">**ID3DXEffect::EndParameterBlock**</span></span>](id3dxeffect--endparameterblock.md)
</dt> </dl>

 

 




