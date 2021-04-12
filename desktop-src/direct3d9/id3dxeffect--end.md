---
description: Termina uma técnica ativa.
ms.assetid: 7297aa67-5cd4-4557-b5ef-faa6c27eaeb5
title: 'Método ID3DXEffect:: End (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.End
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: baaccd7710845296497dcc7f16d3d71c7ceeb9bd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298652"
---
# <a name="id3dxeffectend-method"></a><span data-ttu-id="f3aad-103">Método ID3DXEffect:: End</span><span class="sxs-lookup"><span data-stu-id="f3aad-103">ID3DXEffect::End method</span></span>

<span data-ttu-id="f3aad-104">Termina uma técnica ativa.</span><span class="sxs-lookup"><span data-stu-id="f3aad-104">Ends an active technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3aad-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f3aad-105">Syntax</span></span>


```C++
HRESULT End();
```



## <a name="parameters"></a><span data-ttu-id="f3aad-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f3aad-106">Parameters</span></span>

<span data-ttu-id="f3aad-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f3aad-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f3aad-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f3aad-108">Return value</span></span>

<span data-ttu-id="f3aad-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f3aad-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f3aad-110">Esse método sempre retorna o valor S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f3aad-110">This method always returns the value S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3aad-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f3aad-111">Remarks</span></span>

<span data-ttu-id="f3aad-112">Toda a renderização em um efeito é feita dentro de um par correspondente de [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) e **ID3DXEffect:: End** calls.</span><span class="sxs-lookup"><span data-stu-id="f3aad-112">All rendering in an effect is done within a matching pair of [**ID3DXEffect::Begin**](id3dxeffect--begin.md) and **ID3DXEffect::End** calls.</span></span> <span data-ttu-id="f3aad-113">Depois que todas as passagens são renderizadas, **ID3DXEffect:: End** deve ser chamado para encerrar a técnica ativa.</span><span class="sxs-lookup"><span data-stu-id="f3aad-113">After all passes are rendered, **ID3DXEffect::End** must be called to end the active technique.</span></span> <span data-ttu-id="f3aad-114">O sistema de efeitos responde usando o bloco de estado criado quando **ID3DXEffect:: Begin** foi chamado, para restaurar automaticamente o estado do pipeline antes de **ID3DXEffect:: Begin**.</span><span class="sxs-lookup"><span data-stu-id="f3aad-114">The effect system responds by using the state block created when **ID3DXEffect::Begin** was called, to automatically restore the pipeline state before **ID3DXEffect::Begin**.</span></span>

<span data-ttu-id="f3aad-115">Por padrão, o sistema de efeitos cuida do salvamento do estado antes de uma técnica e da restauração do estado após uma técnica.</span><span class="sxs-lookup"><span data-stu-id="f3aad-115">By default, the effect system takes care of saving state prior to a technique, and restoring state after a technique.</span></span> <span data-ttu-id="f3aad-116">Se você optar por desabilitar essa funcionalidade de salvar e restaurar, consulte [D3DXFX \_ DONOTSAVESAMPLERSTATE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="f3aad-116">If you choose to disable this save and restore functionality, see [D3DXFX\_DONOTSAVESAMPLERSTATE](d3dxfx.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f3aad-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3aad-117">Requirements</span></span>



| <span data-ttu-id="f3aad-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3aad-118">Requirement</span></span> | <span data-ttu-id="f3aad-119">Valor</span><span class="sxs-lookup"><span data-stu-id="f3aad-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3aad-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f3aad-120">Header</span></span><br/>  | <dl> <span data-ttu-id="f3aad-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3aad-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="f3aad-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f3aad-122">Library</span></span><br/> | <dl> <span data-ttu-id="f3aad-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3aad-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f3aad-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="f3aad-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3aad-125">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="f3aad-125">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




