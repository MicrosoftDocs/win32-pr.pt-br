---
description: Obtém um inteiro.
ms.assetid: 8074758a-f650-4698-8a75-aa0ffb14cb21
title: 'Método ID3DXBaseEffect:: GetInt (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetInt
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c0fe1fa01260be936b9d7f8be394d0c43a781680
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105811692"
---
# <a name="id3dxbaseeffectgetint-method"></a><span data-ttu-id="c2b1e-103">Método ID3DXBaseEffect:: GetInt</span><span class="sxs-lookup"><span data-stu-id="c2b1e-103">ID3DXBaseEffect::GetInt method</span></span>

<span data-ttu-id="c2b1e-104">Obtém um inteiro.</span><span class="sxs-lookup"><span data-stu-id="c2b1e-104">Gets an integer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2b1e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c2b1e-105">Syntax</span></span>


```C++
HRESULT GetInt(
  [in]  D3DXHANDLE hParameter,
  [out] INT        *pn
);
```



## <a name="parameters"></a><span data-ttu-id="c2b1e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2b1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2b1e-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c2b1e-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2b1e-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c2b1e-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c2b1e-109">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="c2b1e-109">Unique identifier.</span></span> <span data-ttu-id="c2b1e-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="c2b1e-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2b1e-111">*PN* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c2b1e-111">*pn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2b1e-112">Tipo: **[ **int**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c2b1e-112">Type: **[**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c2b1e-113">Retorna um número inteiro.</span><span class="sxs-lookup"><span data-stu-id="c2b1e-113">Returns an integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2b1e-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c2b1e-114">Return value</span></span>

<span data-ttu-id="c2b1e-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c2b1e-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c2b1e-116">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c2b1e-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c2b1e-117">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="c2b1e-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2b1e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2b1e-118">Requirements</span></span>



| <span data-ttu-id="c2b1e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2b1e-119">Requirement</span></span> | <span data-ttu-id="c2b1e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c2b1e-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2b1e-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c2b1e-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c2b1e-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2b1e-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c2b1e-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c2b1e-123">Library</span></span><br/> | <dl> <span data-ttu-id="c2b1e-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2b1e-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c2b1e-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2b1e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2b1e-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="c2b1e-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="c2b1e-127">**SetInt**</span><span class="sxs-lookup"><span data-stu-id="c2b1e-127">**SetInt**</span></span>](id3dxbaseeffect--setint.md)
</dt> </dl>

 

 
