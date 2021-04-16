---
title: Função D3D12GetFormatPlaneCount (D3dx12. h)
description: Obtém o número de planos para o formato DXGI especificado para o adaptador virtual especificado (um ID3D12Device).
ms.assetid: CD21F6F9-A9AA-4CE8-A430-57C70326CB4B
keywords:
- Função D3D12GetFormatPlaneCount
topic_type:
- apiref
api_name:
- D3D12GetFormatPlaneCount
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bfc2e88c162068de2b97c9df5071398e2fab068
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105782430"
---
# <a name="d3d12getformatplanecount-function"></a><span data-ttu-id="3003d-104">Função D3D12GetFormatPlaneCount</span><span class="sxs-lookup"><span data-stu-id="3003d-104">D3D12GetFormatPlaneCount function</span></span>

<span data-ttu-id="3003d-105">Obtém o número de planos para o formato DXGI especificado para o adaptador virtual especificado (um **ID3D12Device**).</span><span class="sxs-lookup"><span data-stu-id="3003d-105">Gets the number of planes for the specified DXGI format for the specified virtual adapter (an **ID3D12Device**).</span></span>

## <a name="syntax"></a><span data-ttu-id="3003d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3003d-106">Syntax</span></span>


```C++
UINT8 inline D3D12GetFormatPlaneCount(
  _In_ ID3D12Device *pDevice,
       DXGI_FORMAT  Format
);
```



## <a name="parameters"></a><span data-ttu-id="3003d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3003d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3003d-108">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3003d-108">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3003d-109">Tipo: **[ **ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)\***</span><span class="sxs-lookup"><span data-stu-id="3003d-109">Type: **[**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)\***</span></span>

<span data-ttu-id="3003d-110">O adaptador virtual (um [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)) para o qual obter a contagem de planos.</span><span class="sxs-lookup"><span data-stu-id="3003d-110">The virtual adapter (an [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)) for which to get the plane count.</span></span>

</dd> <dt>

<span data-ttu-id="3003d-111">*Formato*</span><span class="sxs-lookup"><span data-stu-id="3003d-111">*Format*</span></span> 
</dt> <dd>

<span data-ttu-id="3003d-112">Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="3003d-112">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="3003d-113">O [**\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) para o qual obter a contagem de planos.</span><span class="sxs-lookup"><span data-stu-id="3003d-113">The [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) for which to get the plane count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3003d-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3003d-114">Return value</span></span>

<span data-ttu-id="3003d-115">Tipo: **UINT8**</span><span class="sxs-lookup"><span data-stu-id="3003d-115">Type: **UINT8**</span></span>

<span data-ttu-id="3003d-116">A contagem de planos para o formato especificado no adaptador virtual especificado.</span><span class="sxs-lookup"><span data-stu-id="3003d-116">The plane count for the specified format on the specified virtual adapter.</span></span>

## <a name="requirements"></a><span data-ttu-id="3003d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3003d-117">Requirements</span></span>



| <span data-ttu-id="3003d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3003d-118">Requirement</span></span> | <span data-ttu-id="3003d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="3003d-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3003d-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3003d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="3003d-121"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="3003d-121"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="3003d-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3003d-122">Library</span></span><br/> | <dl> <span data-ttu-id="3003d-123"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3003d-123"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="3003d-124">DLL</span><span class="sxs-lookup"><span data-stu-id="3003d-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="3003d-125"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3003d-125"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3003d-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="3003d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3003d-127">**\_Informações de \_ formato de dados de recurso D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3003d-127">**D3D12\_FEATURE\_DATA\_FORMAT\_INFO**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info)
</dt> <dt>

[<span data-ttu-id="3003d-128">**CheckFeatureSupport**</span><span class="sxs-lookup"><span data-stu-id="3003d-128">**CheckFeatureSupport**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
</dt> <dt>

[<span data-ttu-id="3003d-129">Funções auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="3003d-129">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

