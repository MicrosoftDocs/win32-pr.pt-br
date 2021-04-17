---
description: Obtém um conjunto de animações, dado seu nome.
ms.assetid: 4c3f3002-45f6-49b2-8a42-18d5824fb36f
title: 'Método ID3DXAnimationController:: GetAnimationSetByName (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetAnimationSetByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d520625e457a50fe962ae74d6e25fc17e2beb729
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105782569"
---
# <a name="id3dxanimationcontrollergetanimationsetbyname-method"></a><span data-ttu-id="6bb16-103">Método ID3DXAnimationController:: GetAnimationSetByName</span><span class="sxs-lookup"><span data-stu-id="6bb16-103">ID3DXAnimationController::GetAnimationSetByName method</span></span>

<span data-ttu-id="6bb16-104">Obtém um conjunto de animações, dado seu nome.</span><span class="sxs-lookup"><span data-stu-id="6bb16-104">Gets an animation set, given its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bb16-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6bb16-105">Syntax</span></span>


```C++
HRESULT GetAnimationSetByName(
  [in]  LPCSTR             pName,
  [out] LPD3DXANIMATIONSET *ppAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="6bb16-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6bb16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bb16-107">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6bb16-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bb16-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6bb16-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6bb16-109">Cadeia de caracteres que contém o nome do conjunto de animações.</span><span class="sxs-lookup"><span data-stu-id="6bb16-109">String containing the name of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="6bb16-110">*ppAnimSet* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6bb16-110">*ppAnimSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6bb16-111">Tipo: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span><span class="sxs-lookup"><span data-stu-id="6bb16-111">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span></span>

<span data-ttu-id="6bb16-112">Ponteiro para o conjunto de animações [**ID3DXAnimationSet**](id3dxanimationset.md) .</span><span class="sxs-lookup"><span data-stu-id="6bb16-112">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bb16-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6bb16-113">Return value</span></span>

<span data-ttu-id="6bb16-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6bb16-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6bb16-115">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6bb16-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="6bb16-116">Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="6bb16-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bb16-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="6bb16-117">Remarks</span></span>

<span data-ttu-id="6bb16-118">O controlador de animação contém uma matriz de conjuntos de animação.</span><span class="sxs-lookup"><span data-stu-id="6bb16-118">The animation controller contains an array of animation sets.</span></span> <span data-ttu-id="6bb16-119">Esse método retorna um conjunto de animações que tem o nome fornecido.</span><span class="sxs-lookup"><span data-stu-id="6bb16-119">This method returns an animation set that has the given name.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bb16-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6bb16-120">Requirements</span></span>



| <span data-ttu-id="6bb16-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bb16-121">Requirement</span></span> | <span data-ttu-id="6bb16-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6bb16-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6bb16-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6bb16-123">Header</span></span><br/>  | <dl> <span data-ttu-id="6bb16-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bb16-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="6bb16-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6bb16-125">Library</span></span><br/> | <dl> <span data-ttu-id="6bb16-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6bb16-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6bb16-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="6bb16-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bb16-128">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="6bb16-128">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
