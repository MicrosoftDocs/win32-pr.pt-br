---
description: Obtém um vetor.
ms.assetid: 55f5512f-42f2-4588-abd4-1cdea530b9bf
title: 'Método ID3DXBaseEffect:: getvector (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetVector
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ea50cb6bf8c3f5b08d408539eba6c9f7cb09efc1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298475"
---
# <a name="id3dxbaseeffectgetvector-method"></a><span data-ttu-id="f62d6-103">Método ID3DXBaseEffect:: getvector</span><span class="sxs-lookup"><span data-stu-id="f62d6-103">ID3DXBaseEffect::GetVector method</span></span>

<span data-ttu-id="f62d6-104">Obtém um vetor.</span><span class="sxs-lookup"><span data-stu-id="f62d6-104">Gets a vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="f62d6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f62d6-105">Syntax</span></span>


```C++
HRESULT GetVector(
  [in]  D3DXHANDLE  hParameter,
  [out] D3DXVECTOR4 *pVector
);
```



## <a name="parameters"></a><span data-ttu-id="f62d6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f62d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f62d6-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f62d6-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f62d6-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f62d6-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f62d6-109">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="f62d6-109">Unique identifier.</span></span> <span data-ttu-id="f62d6-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="f62d6-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="f62d6-111">*pVector* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f62d6-111">*pVector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f62d6-112">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="f62d6-112">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="f62d6-113">Retorna um vetor 4D.</span><span class="sxs-lookup"><span data-stu-id="f62d6-113">Returns a 4D vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f62d6-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f62d6-114">Return value</span></span>

<span data-ttu-id="f62d6-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f62d6-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f62d6-116">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f62d6-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f62d6-117">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="f62d6-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f62d6-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="f62d6-118">Remarks</span></span>

<span data-ttu-id="f62d6-119">Se o vetor de destino for maior que o vetor de origem, somente os componentes iniciais do vetor de destino serão preenchidos e os componentes restantes serão definidos como zero.</span><span class="sxs-lookup"><span data-stu-id="f62d6-119">If the destination vector is larger than the source vector, only the initial components of the destination vector will be filled, and the remaining components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="f62d6-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f62d6-120">Requirements</span></span>



| <span data-ttu-id="f62d6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f62d6-121">Requirement</span></span> | <span data-ttu-id="f62d6-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f62d6-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f62d6-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f62d6-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f62d6-124"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="f62d6-124"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="f62d6-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f62d6-125">Library</span></span><br/> | <dl> <span data-ttu-id="f62d6-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f62d6-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f62d6-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f62d6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f62d6-128">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="f62d6-128">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="f62d6-129">**Setvector**</span><span class="sxs-lookup"><span data-stu-id="f62d6-129">**SetVector**</span></span>](id3dxbaseeffect--setvector.md)
</dt> </dl>

 

 




