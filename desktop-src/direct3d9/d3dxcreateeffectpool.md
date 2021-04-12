---
description: Crie um pool de efeitos. Um pool é usado para compartilhar parâmetros entre efeitos.
ms.assetid: 5b202f85-b32b-4041-8873-0de535c2f59f
title: Função D3DXCreateEffectPool (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectPool
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 14753500ac15fb0ed30d46b1121431af78e1fe93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173156"
---
# <a name="d3dxcreateeffectpool-function"></a><span data-ttu-id="297a0-104">Função D3DXCreateEffectPool</span><span class="sxs-lookup"><span data-stu-id="297a0-104">D3DXCreateEffectPool function</span></span>

<span data-ttu-id="297a0-105">Crie um pool de efeitos.</span><span class="sxs-lookup"><span data-stu-id="297a0-105">Create an effect pool.</span></span> <span data-ttu-id="297a0-106">Um pool é usado para compartilhar parâmetros entre efeitos.</span><span class="sxs-lookup"><span data-stu-id="297a0-106">A pool is used to share parameters between effects.</span></span>

## <a name="syntax"></a><span data-ttu-id="297a0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="297a0-107">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectPool(
  _Out_ LPD3DXEFFECTPOOL *ppPool
);
```



## <a name="parameters"></a><span data-ttu-id="297a0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="297a0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="297a0-109">*ppPool* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="297a0-109">*ppPool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="297a0-110">Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***</span><span class="sxs-lookup"><span data-stu-id="297a0-110">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***</span></span>

<span data-ttu-id="297a0-111">Retorna um ponteiro para o pool criado.</span><span class="sxs-lookup"><span data-stu-id="297a0-111">Returns a pointer to the created pool.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="297a0-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="297a0-112">Return value</span></span>

<span data-ttu-id="297a0-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="297a0-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="297a0-114">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="297a0-114">If the method succeeds, the return value is S\_OK.</span></span>

<span data-ttu-id="297a0-115">Se os argumentos forem inválidos, o método retornará D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="297a0-115">If the arguments are invalid, the method will return D3DERR\_INVALIDCALL.</span></span>

<span data-ttu-id="297a0-116">Se o método falhar, o valor de retorno será E \_ falhará.</span><span class="sxs-lookup"><span data-stu-id="297a0-116">If the method fails, the return value will be E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="297a0-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="297a0-117">Remarks</span></span>

<span data-ttu-id="297a0-118">Para efeitos em um pool, os parâmetros compartilhados com o mesmo nome compartilham valores.</span><span class="sxs-lookup"><span data-stu-id="297a0-118">For effects within a pool, shared parameters with the same name share values.</span></span>

## <a name="requirements"></a><span data-ttu-id="297a0-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="297a0-119">Requirements</span></span>



| <span data-ttu-id="297a0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="297a0-120">Requirement</span></span> | <span data-ttu-id="297a0-121">Valor</span><span class="sxs-lookup"><span data-stu-id="297a0-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="297a0-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="297a0-122">Header</span></span><br/>  | <dl> <span data-ttu-id="297a0-123"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="297a0-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="297a0-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="297a0-124">Library</span></span><br/> | <dl> <span data-ttu-id="297a0-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="297a0-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="297a0-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="297a0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="297a0-127">Funções de efeito</span><span class="sxs-lookup"><span data-stu-id="297a0-127">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> </dl>

 

 




