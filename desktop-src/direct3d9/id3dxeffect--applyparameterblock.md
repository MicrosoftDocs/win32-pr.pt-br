---
description: Aplique os valores em um bloco de estado ao estado atual do sistema de efeito.
ms.assetid: f228e2a2-64fa-4354-9f49-42d1d3b12d50
title: 'Método ID3DXEffect:: ApplyParameterBlock (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.ApplyParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 12af672b929822180c4dba681ca333692a9174ec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105785289"
---
# <a name="id3dxeffectapplyparameterblock-method"></a><span data-ttu-id="6d3c6-103">Método ID3DXEffect:: ApplyParameterBlock</span><span class="sxs-lookup"><span data-stu-id="6d3c6-103">ID3DXEffect::ApplyParameterBlock method</span></span>

<span data-ttu-id="6d3c6-104">Aplique os valores em um bloco de estado ao estado atual do sistema de efeito.</span><span class="sxs-lookup"><span data-stu-id="6d3c6-104">Apply the values in a state block to the current effect system state.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d3c6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d3c6-105">Syntax</span></span>


```C++
HRESULT ApplyParameterBlock(
  [in] D3DXHANDLE  hParameterBlock
);
```



## <a name="parameters"></a><span data-ttu-id="6d3c6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d3c6-106">Parameters</span></span>

<dl> <dt>

 <span data-ttu-id="6d3c6-107">*hParameterBlock* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6d3c6-107">*hParameterBlock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d3c6-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="6d3c6-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="6d3c6-109">Um identificador para o bloco de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="6d3c6-109">A handle to the parameter block.</span></span> <span data-ttu-id="6d3c6-110">Esse é o identificador retornado por [**ID3DXEffect:: EndParameterBlock**](id3dxeffect--endparameterblock.md).</span><span class="sxs-lookup"><span data-stu-id="6d3c6-110">This is the handle returned by [**ID3DXEffect::EndParameterBlock**](id3dxeffect--endparameterblock.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d3c6-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6d3c6-111">Return value</span></span>

<span data-ttu-id="6d3c6-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6d3c6-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6d3c6-113">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6d3c6-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6d3c6-114">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="6d3c6-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d3c6-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d3c6-115">Remarks</span></span>

<span data-ttu-id="6d3c6-116">Capturar alterações de estado de parâmetro de efeito em um bloco de parâmetro chamando BeginParameterBlock; Pare a captura de alterações de estado chamando EndParameterBlock.</span><span class="sxs-lookup"><span data-stu-id="6d3c6-116">Capture effect parameter state changes in a parameter block by calling BeginParameterBlock; stop capturing state changes by calling EndParameterBlock.</span></span> <span data-ttu-id="6d3c6-117">Essas alterações de estado incluem qualquer alteração de parâmetro de efeito que ocorra dentro de uma técnica (incluindo aquelas fora de uma passagem).</span><span class="sxs-lookup"><span data-stu-id="6d3c6-117">These state changes include any effect parameter changes that occur inside of a technique (including those outside of a pass).</span></span> <span data-ttu-id="6d3c6-118">Depois de concluir o bloco de parâmetro, chame DeleteParameterBlock para recuperar a memória.</span><span class="sxs-lookup"><span data-stu-id="6d3c6-118">Once you are done with the parameter block, call DeleteParameterBlock to recover memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d3c6-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d3c6-119">Requirements</span></span>



| <span data-ttu-id="6d3c6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d3c6-120">Requirement</span></span> | <span data-ttu-id="6d3c6-121">Valor</span><span class="sxs-lookup"><span data-stu-id="6d3c6-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d3c6-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6d3c6-122">Header</span></span><br/>  | <dl> <span data-ttu-id="6d3c6-123"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d3c6-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="6d3c6-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6d3c6-124">Library</span></span><br/> | <dl> <span data-ttu-id="6d3c6-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d3c6-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6d3c6-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d3c6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d3c6-127">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="6d3c6-127">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="6d3c6-128">**ID3DXEffect::BeginParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="6d3c6-128">**ID3DXEffect::BeginParameterBlock**</span></span>](id3dxeffect--beginparameterblock.md)
</dt> <dt>

[<span data-ttu-id="6d3c6-129">**ID3DXEffect::EndParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="6d3c6-129">**ID3DXEffect::EndParameterBlock**</span></span>](id3dxeffect--endparameterblock.md)
</dt> <dt>

[<span data-ttu-id="6d3c6-130">**ID3DXEffect::D eleteParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="6d3c6-130">**ID3DXEffect::DeleteParameterBlock**</span></span>](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 




