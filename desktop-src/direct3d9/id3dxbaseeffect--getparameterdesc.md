---
description: Obtém uma descrição de parâmetro ou anotação.
ms.assetid: fd54eb08-a7e4-4106-b0ed-49a4da7fcadc
title: 'Método ID3DXBaseEffect:: GetParameterDesc (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8c3a52c06ebed764b3ab1718488c2dbc55ceda41
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105797528"
---
# <a name="id3dxbaseeffectgetparameterdesc-method"></a><span data-ttu-id="32141-103">Método ID3DXBaseEffect:: GetParameterDesc</span><span class="sxs-lookup"><span data-stu-id="32141-103">ID3DXBaseEffect::GetParameterDesc method</span></span>

<span data-ttu-id="32141-104">Obtém uma descrição de parâmetro ou anotação.</span><span class="sxs-lookup"><span data-stu-id="32141-104">Gets a parameter or annotation description.</span></span>

## <a name="syntax"></a><span data-ttu-id="32141-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="32141-105">Syntax</span></span>


```C++
HRESULT GetParameterDesc(
  [in]  D3DXHANDLE         hParameter,
  [out] D3DXPARAMETER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="32141-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="32141-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32141-107">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="32141-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32141-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="32141-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="32141-109">Identificador de parâmetro ou de anotação.</span><span class="sxs-lookup"><span data-stu-id="32141-109">Parameter or annotation handle.</span></span> <span data-ttu-id="32141-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="32141-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="32141-111">*pDesc* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="32141-111">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32141-112">Tipo: **[ **D3DXPARAMETER \_ desc**](d3dxparameter-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="32141-112">Type: **[**D3DXPARAMETER\_DESC**](d3dxparameter-desc.md)\***</span></span>

<span data-ttu-id="32141-113">Retorna uma descrição do parâmetro ou da anotação especificada.</span><span class="sxs-lookup"><span data-stu-id="32141-113">Returns a description of the specified parameter or annotation.</span></span> <span data-ttu-id="32141-114">Consulte [**D3DXPARAMETER \_ desc**](d3dxparameter-desc.md).</span><span class="sxs-lookup"><span data-stu-id="32141-114">See [**D3DXPARAMETER\_DESC**](d3dxparameter-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32141-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="32141-115">Return value</span></span>

<span data-ttu-id="32141-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="32141-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="32141-117">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="32141-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="32141-118">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="32141-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="32141-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32141-119">Requirements</span></span>



| <span data-ttu-id="32141-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="32141-120">Requirement</span></span> | <span data-ttu-id="32141-121">Valor</span><span class="sxs-lookup"><span data-stu-id="32141-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="32141-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="32141-122">Header</span></span><br/>  | <dl> <span data-ttu-id="32141-123"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="32141-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="32141-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="32141-124">Library</span></span><br/> | <dl> <span data-ttu-id="32141-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="32141-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="32141-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="32141-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32141-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="32141-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 




