---
description: Obtém uma matriz de valores BOOL.
ms.assetid: 4a5e2f48-fa82-47dc-a388-02a8679585d2
title: 'Método ID3DXBaseEffect:: GetBoolArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetBoolArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f714dfa91baba14524f12b6c3b2cb85211484cf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105748658"
---
# <a name="id3dxbaseeffectgetboolarray-method"></a><span data-ttu-id="97e09-103">Método ID3DXBaseEffect:: GetBoolArray</span><span class="sxs-lookup"><span data-stu-id="97e09-103">ID3DXBaseEffect::GetBoolArray method</span></span>

<span data-ttu-id="97e09-104">Obtém uma matriz de valores BOOL.</span><span class="sxs-lookup"><span data-stu-id="97e09-104">Gets an array of BOOL values.</span></span>

## <a name="syntax"></a><span data-ttu-id="97e09-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="97e09-105">Syntax</span></span>


```C++
HRESULT GetBoolArray(
  [in]  D3DXHANDLE hParameter,
  [out] BOOL       *pB,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="97e09-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="97e09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97e09-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="97e09-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97e09-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="97e09-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="97e09-109">Identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="97e09-109">Unique identifier.</span></span> <span data-ttu-id="97e09-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="97e09-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="97e09-111">*PB* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="97e09-111">*pB* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97e09-112">Tipo: **[ **bool**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="97e09-112">Type: **[**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="97e09-113">Retorna uma matriz de valores Boolianos.</span><span class="sxs-lookup"><span data-stu-id="97e09-113">Returns an array of Boolean values.</span></span>

</dd> <dt>

<span data-ttu-id="97e09-114">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="97e09-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97e09-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="97e09-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="97e09-116">Número de valores Boolianos na matriz.</span><span class="sxs-lookup"><span data-stu-id="97e09-116">Number of Boolean values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97e09-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="97e09-117">Return value</span></span>

<span data-ttu-id="97e09-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="97e09-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="97e09-119">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="97e09-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="97e09-120">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="97e09-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="97e09-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97e09-121">Requirements</span></span>



| <span data-ttu-id="97e09-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="97e09-122">Requirement</span></span> | <span data-ttu-id="97e09-123">Valor</span><span class="sxs-lookup"><span data-stu-id="97e09-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="97e09-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="97e09-124">Header</span></span><br/>  | <dl> <span data-ttu-id="97e09-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="97e09-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="97e09-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="97e09-126">Library</span></span><br/> | <dl> <span data-ttu-id="97e09-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="97e09-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="97e09-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="97e09-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97e09-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="97e09-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="97e09-130">**SetBoolArray**</span><span class="sxs-lookup"><span data-stu-id="97e09-130">**SetBoolArray**</span></span>](id3dxbaseeffect--setboolarray.md)
</dt> </dl>

 

 
