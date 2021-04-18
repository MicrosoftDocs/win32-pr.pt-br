---
description: Define um vetor.
ms.assetid: 7dae88fc-d5d3-4751-859a-fa1bde4d0ce8
title: 'Método ID3DXBaseEffect:: setvector (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetVector
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5d6fccc24410e06dd9bb4e6b0b1f1c36b03dd355
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105772534"
---
# <a name="id3dxbaseeffectsetvector-method"></a><span data-ttu-id="a16bd-103">Método ID3DXBaseEffect:: setvector</span><span class="sxs-lookup"><span data-stu-id="a16bd-103">ID3DXBaseEffect::SetVector method</span></span>

<span data-ttu-id="a16bd-104">Define um vetor.</span><span class="sxs-lookup"><span data-stu-id="a16bd-104">Sets a vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="a16bd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a16bd-105">Syntax</span></span>


```C++
HRESULT SetVector(
  [in]       D3DXHANDLE  hParameter,
  [in] const D3DXVECTOR4 *pVector
);
```



## <a name="parameters"></a><span data-ttu-id="a16bd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a16bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a16bd-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a16bd-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a16bd-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a16bd-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a16bd-109">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="a16bd-109">Unique identifier.</span></span> <span data-ttu-id="a16bd-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="a16bd-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="a16bd-111">*pVector* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a16bd-111">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a16bd-112">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="a16bd-112">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="a16bd-113">Ponteiro para um vetor 4D.</span><span class="sxs-lookup"><span data-stu-id="a16bd-113">Pointer to a 4D vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a16bd-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a16bd-114">Return value</span></span>

<span data-ttu-id="a16bd-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a16bd-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a16bd-116">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a16bd-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a16bd-117">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a16bd-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a16bd-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="a16bd-118">Remarks</span></span>

<span data-ttu-id="a16bd-119">Se o vetor de destino for menor do que o vetor de origem, os componentes adicionais do vetor de origem serão ignorados.</span><span class="sxs-lookup"><span data-stu-id="a16bd-119">If the destination vector is smaller than the source vector, the additional components of the source vector will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="a16bd-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a16bd-120">Requirements</span></span>



| <span data-ttu-id="a16bd-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a16bd-121">Requirement</span></span> | <span data-ttu-id="a16bd-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a16bd-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a16bd-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a16bd-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a16bd-124"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="a16bd-124"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a16bd-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a16bd-125">Library</span></span><br/> | <dl> <span data-ttu-id="a16bd-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a16bd-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a16bd-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="a16bd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a16bd-128">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="a16bd-128">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="a16bd-129">**Getvector**</span><span class="sxs-lookup"><span data-stu-id="a16bd-129">**GetVector**</span></span>](id3dxbaseeffect--getvector.md)
</dt> </dl>

 

 




