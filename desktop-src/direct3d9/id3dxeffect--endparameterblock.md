---
description: Parar a captura de alterações de estado de parâmetro de efeito.
ms.assetid: b6ca2917-2df0-4f3a-9ee3-23e9d2501ff4
title: 'Método ID3DXEffect:: EndParameterBlock (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.EndParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 3359e3b923d05e003ffbda18791e497d18ba627e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930614"
---
# <a name="id3dxeffectendparameterblock-method"></a><span data-ttu-id="5ee2e-103">Método ID3DXEffect:: EndParameterBlock</span><span class="sxs-lookup"><span data-stu-id="5ee2e-103">ID3DXEffect::EndParameterBlock method</span></span>

<span data-ttu-id="5ee2e-104">Parar a captura de alterações de estado de parâmetro de efeito.</span><span class="sxs-lookup"><span data-stu-id="5ee2e-104">Stop capturing effect parameter state changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ee2e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5ee2e-105">Syntax</span></span>


```C++
D3DXHANDLE EndParameterBlock();
```



## <a name="parameters"></a><span data-ttu-id="5ee2e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5ee2e-106">Parameters</span></span>

<span data-ttu-id="5ee2e-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5ee2e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5ee2e-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5ee2e-108">Return value</span></span>

<span data-ttu-id="5ee2e-109">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5ee2e-109">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5ee2e-110">Retorna um identificador para o bloco de estado do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="5ee2e-110">Returns a handle to the parameter state block.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ee2e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="5ee2e-111">Remarks</span></span>

<span data-ttu-id="5ee2e-112">Todos os parâmetros de efeito que alteram o estado (depois de chamar BeginParameterBlock e antes de chamar EndParameterBlock) serão salvos em um bloco de estado de parâmetro de efeito.</span><span class="sxs-lookup"><span data-stu-id="5ee2e-112">All effect parameters that change state (after calling BeginParameterBlock and before calling EndParameterBlock) will be saved in an effect parameter state block.</span></span> <span data-ttu-id="5ee2e-113">Use ApplyParameterBlock para aplicar esse bloco de alterações de estado ao sistema de efeitos.</span><span class="sxs-lookup"><span data-stu-id="5ee2e-113">Use ApplyParameterBlock to apply this block of state changes to the effect system.</span></span> <span data-ttu-id="5ee2e-114">Quando você terminar com um bloco de estado, use DeleteParameterBlock para liberar a memória.</span><span class="sxs-lookup"><span data-stu-id="5ee2e-114">Once you are finished with a state block use DeleteParameterBlock to free the memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ee2e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ee2e-115">Requirements</span></span>



| <span data-ttu-id="5ee2e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ee2e-116">Requirement</span></span> | <span data-ttu-id="5ee2e-117">Valor</span><span class="sxs-lookup"><span data-stu-id="5ee2e-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ee2e-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ee2e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="5ee2e-119"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ee2e-119"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="5ee2e-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5ee2e-120">Library</span></span><br/> | <dl> <span data-ttu-id="5ee2e-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ee2e-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5ee2e-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="5ee2e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ee2e-123">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="5ee2e-123">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="5ee2e-124">**ID3DXEffect::BeginParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="5ee2e-124">**ID3DXEffect::BeginParameterBlock**</span></span>](id3dxeffect--beginparameterblock.md)
</dt> <dt>

[<span data-ttu-id="5ee2e-125">**ID3DXEffect::ApplyParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="5ee2e-125">**ID3DXEffect::ApplyParameterBlock**</span></span>](id3dxeffect--applyparameterblock.md)
</dt> <dt>

[<span data-ttu-id="5ee2e-126">**ID3DXEffect::D eleteParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="5ee2e-126">**ID3DXEffect::DeleteParameterBlock**</span></span>](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 




