---
description: Obtém uma descrição da função.
ms.assetid: a1a0ccf4-2428-4e60-9af0-07dc2132a367
title: 'Método ID3DXBaseEffect:: GetFunctionDesc (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFunctionDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 718960da7ff73f24f865fdacc09dfe55ff09a466
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105782538"
---
# <a name="id3dxbaseeffectgetfunctiondesc-method"></a><span data-ttu-id="23bed-103">Método ID3DXBaseEffect:: GetFunctionDesc</span><span class="sxs-lookup"><span data-stu-id="23bed-103">ID3DXBaseEffect::GetFunctionDesc method</span></span>

<span data-ttu-id="23bed-104">Obtém uma descrição da função.</span><span class="sxs-lookup"><span data-stu-id="23bed-104">Gets a function description.</span></span>

## <a name="syntax"></a><span data-ttu-id="23bed-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="23bed-105">Syntax</span></span>


```C++
HRESULT GetFunctionDesc(
  [in]  D3DXHANDLE        hFunction,
  [out] D3DXFUNCTION_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="23bed-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="23bed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23bed-107">*hFunction* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="23bed-107">*hFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23bed-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="23bed-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="23bed-109">Identificador de função.</span><span class="sxs-lookup"><span data-stu-id="23bed-109">Function handle.</span></span> <span data-ttu-id="23bed-110">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="23bed-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="23bed-111">*pDesc* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="23bed-111">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23bed-112">Tipo: **[ **D3DXFUNCTION \_ desc**](d3dxfunction-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="23bed-112">Type: **[**D3DXFUNCTION\_DESC**](d3dxfunction-desc.md)\***</span></span>

<span data-ttu-id="23bed-113">Retorna uma descrição da função.</span><span class="sxs-lookup"><span data-stu-id="23bed-113">Returns a description of the function.</span></span> <span data-ttu-id="23bed-114">Consulte [**D3DXFUNCTION \_ desc**](d3dxfunction-desc.md).</span><span class="sxs-lookup"><span data-stu-id="23bed-114">See [**D3DXFUNCTION\_DESC**](d3dxfunction-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23bed-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="23bed-115">Return value</span></span>

<span data-ttu-id="23bed-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="23bed-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="23bed-117">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="23bed-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="23bed-118">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="23bed-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="23bed-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23bed-119">Requirements</span></span>



| <span data-ttu-id="23bed-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="23bed-120">Requirement</span></span> | <span data-ttu-id="23bed-121">Valor</span><span class="sxs-lookup"><span data-stu-id="23bed-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="23bed-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="23bed-122">Header</span></span><br/>  | <dl> <span data-ttu-id="23bed-123"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="23bed-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="23bed-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="23bed-124">Library</span></span><br/> | <dl> <span data-ttu-id="23bed-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23bed-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="23bed-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="23bed-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23bed-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="23bed-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 




