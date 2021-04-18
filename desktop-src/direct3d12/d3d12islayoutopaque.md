---
title: Função D3D12IsLayoutOpaque (D3dx12. h)
description: Indica se o layout é opaco.
ms.assetid: 43B46A18-A725-4999-BD97-108032793A95
keywords:
- Função D3D12IsLayoutOpaque
topic_type:
- apiref
api_name:
- D3D12IsLayoutOpaque
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 971c44688e57dd1081d33a4a077a8dcadcb89abf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105807335"
---
# <a name="d3d12islayoutopaque-function"></a><span data-ttu-id="9e3d3-104">Função D3D12IsLayoutOpaque</span><span class="sxs-lookup"><span data-stu-id="9e3d3-104">D3D12IsLayoutOpaque function</span></span>

<span data-ttu-id="9e3d3-105">Indica se o layout é opaco.</span><span class="sxs-lookup"><span data-stu-id="9e3d3-105">Indicates whether the layout is opaque.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e3d3-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e3d3-106">Syntax</span></span>


```C++
bool inline D3D12IsLayoutOpaque(
   D3D12_TEXTURE_LAYOUT Layout
);
```



## <a name="parameters"></a><span data-ttu-id="9e3d3-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9e3d3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e3d3-108">*Layout*</span><span class="sxs-lookup"><span data-stu-id="9e3d3-108">*Layout*</span></span> 
</dt> <dd>

<span data-ttu-id="9e3d3-109">Tipo: **[ **\_ \_ layout de textura D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)**</span><span class="sxs-lookup"><span data-stu-id="9e3d3-109">Type: **[**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)**</span></span>

<span data-ttu-id="9e3d3-110">O layout a ser verificado, como [**um \_ \_ layout de textura D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout).</span><span class="sxs-lookup"><span data-stu-id="9e3d3-110">The layout to check, as a [**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e3d3-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9e3d3-111">Return value</span></span>

<span data-ttu-id="9e3d3-112">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="9e3d3-112">Type: **bool**</span></span>

<span data-ttu-id="9e3d3-113">Um **bool** que indica se o layout é opaco.</span><span class="sxs-lookup"><span data-stu-id="9e3d3-113">A **bool** that indicates whether the layout is opaque.</span></span> <span data-ttu-id="9e3d3-114">Um layout será opaco se for um \_ layout de textura D3D12 \_ \_ desconhecido ou D3D12 do \_ layout de textura \_ \_ 64 KB \_ indefinido \_ SWIZZLE.</span><span class="sxs-lookup"><span data-stu-id="9e3d3-114">A layout is opaque if it is D3D12\_TEXTURE\_LAYOUT\_UNKNOWN or D3D12\_TEXTURE\_LAYOUT\_64KB\_UNDEFINED\_SWIZZLE.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e3d3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e3d3-115">Requirements</span></span>



| <span data-ttu-id="9e3d3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e3d3-116">Requirement</span></span> | <span data-ttu-id="9e3d3-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9e3d3-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9e3d3-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9e3d3-118">Header</span></span><br/>  | <dl> <span data-ttu-id="9e3d3-119"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e3d3-119"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="9e3d3-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9e3d3-120">Library</span></span><br/> | <dl> <span data-ttu-id="9e3d3-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e3d3-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="9e3d3-122">DLL</span><span class="sxs-lookup"><span data-stu-id="9e3d3-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="9e3d3-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e3d3-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e3d3-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e3d3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e3d3-125">Funções auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="9e3d3-125">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





