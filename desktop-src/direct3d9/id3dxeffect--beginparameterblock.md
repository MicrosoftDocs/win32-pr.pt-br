---
description: Iniciar a captura de alterações de estado em um bloco de parâmetro.
ms.assetid: cdf6f572-1a21-4c1d-a113-13b48bacd060
title: 'Método ID3DXEffect:: BeginParameterBlock (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.BeginParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 60a43304c8e0e3d64ac6469c1c075c57b5411e3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012106"
---
# <a name="id3dxeffectbeginparameterblock-method"></a><span data-ttu-id="e1b15-103">Método ID3DXEffect:: BeginParameterBlock</span><span class="sxs-lookup"><span data-stu-id="e1b15-103">ID3DXEffect::BeginParameterBlock method</span></span>

<span data-ttu-id="e1b15-104">Iniciar a captura de alterações de estado em um bloco de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e1b15-104">Start capturing state changes in a parameter block.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1b15-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e1b15-105">Syntax</span></span>


```C++
HRESULT BeginParameterBlock();
```



## <a name="parameters"></a><span data-ttu-id="e1b15-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e1b15-106">Parameters</span></span>

<span data-ttu-id="e1b15-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e1b15-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e1b15-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e1b15-108">Return value</span></span>

<span data-ttu-id="e1b15-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e1b15-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e1b15-110">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e1b15-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e1b15-111">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="e1b15-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1b15-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1b15-112">Remarks</span></span>

<span data-ttu-id="e1b15-113">Capturar as alterações de estado do parâmetro de efeito até que EndParameterBlock seja chamado.</span><span class="sxs-lookup"><span data-stu-id="e1b15-113">Capture effect parameter state changes until EndParameterBlock is called.</span></span> <span data-ttu-id="e1b15-114">Os parâmetros de efeito incluem qualquer alteração de estado fora de uma passagem.</span><span class="sxs-lookup"><span data-stu-id="e1b15-114">Effect parameters include any state changes outside of a pass.</span></span> <span data-ttu-id="e1b15-115">Exclua os blocos de parâmetro se eles não forem mais necessários chamando DeleteParameterBlock.</span><span class="sxs-lookup"><span data-stu-id="e1b15-115">Delete parameter blocks if they are no longer needed by calling DeleteParameterBlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1b15-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1b15-116">Requirements</span></span>



| <span data-ttu-id="e1b15-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1b15-117">Requirement</span></span> | <span data-ttu-id="e1b15-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e1b15-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1b15-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e1b15-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e1b15-120"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1b15-120"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="e1b15-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e1b15-121">Library</span></span><br/> | <dl> <span data-ttu-id="e1b15-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e1b15-122"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e1b15-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1b15-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1b15-124">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="e1b15-124">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="e1b15-125">**ID3DXEffect::EndParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="e1b15-125">**ID3DXEffect::EndParameterBlock**</span></span>](id3dxeffect--endparameterblock.md)
</dt> <dt>

[<span data-ttu-id="e1b15-126">**ID3DXEffect::ApplyParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="e1b15-126">**ID3DXEffect::ApplyParameterBlock**</span></span>](id3dxeffect--applyparameterblock.md)
</dt> <dt>

[<span data-ttu-id="e1b15-127">**ID3DXEffect::D eleteParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="e1b15-127">**ID3DXEffect::DeleteParameterBlock**</span></span>](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 




