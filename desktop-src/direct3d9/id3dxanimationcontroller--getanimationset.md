---
description: Obtém um conjunto de animações.
ms.assetid: 61785f60-82c1-4ddc-b4cd-2e7f665cfe8c
title: 'Método ID3DXAnimationController:: getanimationset (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c21f073b74d1ab7dac09ddd8bfb3d6be543e122a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104091979"
---
# <a name="id3dxanimationcontrollergetanimationset-method"></a><span data-ttu-id="f8c51-103">Método ID3DXAnimationController:: getanimationset</span><span class="sxs-lookup"><span data-stu-id="f8c51-103">ID3DXAnimationController::GetAnimationSet method</span></span>

<span data-ttu-id="f8c51-104">Obtém um conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="f8c51-104">Gets an animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8c51-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f8c51-105">Syntax</span></span>


```C++
HRESULT GetAnimationSet(
  [in]  UINT               Index,
  [out] LPD3DXANIMATIONSET *ppAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="f8c51-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f8c51-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8c51-107">*Índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="f8c51-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8c51-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8c51-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f8c51-109">Índice do conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="f8c51-109">Index of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="f8c51-110">*ppAnimSet* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f8c51-110">*ppAnimSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8c51-111">Tipo: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span><span class="sxs-lookup"><span data-stu-id="f8c51-111">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span></span>

<span data-ttu-id="f8c51-112">Ponteiro para o conjunto de animações [**ID3DXAnimationSet**](id3dxanimationset.md) .</span><span class="sxs-lookup"><span data-stu-id="f8c51-112">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8c51-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f8c51-113">Return value</span></span>

<span data-ttu-id="f8c51-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f8c51-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f8c51-115">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f8c51-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f8c51-116">Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="f8c51-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8c51-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8c51-117">Remarks</span></span>

<span data-ttu-id="f8c51-118">O controlador de animação contém uma matriz de conjuntos de animação.</span><span class="sxs-lookup"><span data-stu-id="f8c51-118">The animation controller contains an array of animation sets.</span></span> <span data-ttu-id="f8c51-119">Esse método retorna um deles no índice fornecido.</span><span class="sxs-lookup"><span data-stu-id="f8c51-119">This method returns one of them at the given index.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8c51-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8c51-120">Requirements</span></span>



| <span data-ttu-id="f8c51-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8c51-121">Requirement</span></span> | <span data-ttu-id="f8c51-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f8c51-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8c51-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f8c51-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f8c51-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8c51-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="f8c51-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f8c51-125">Library</span></span><br/> | <dl> <span data-ttu-id="f8c51-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8c51-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f8c51-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8c51-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8c51-128">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="f8c51-128">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
