---
title: 'Método ID3D12DeviceDownlevel:: QueryVideoMemoryInfo'
description: 'Copia o conteúdo de um recurso do Direct3D 12 Texture2D para uma janela. | Método ID3D12DeviceDownlevel:: QueryVideoMemoryInfo'
keywords:
- Método QueryVideoMemoryInfo
- Método QueryVideoMemoryInfo, interface ID3D12DeviceDownlevel
- Interface ID3D12DeviceDownlevel, método QueryVideoMemoryInfo
topic_type:
- apiref
api_name:
- ID3D12DeviceDownlevel.QueryVideoMemoryInfo
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 32b93fcbbe44aaae0916e6d8f3f403eb960e26eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105769659"
---
# <a name="id3d12devicedownlevelqueryvideomemoryinfo-method"></a><span data-ttu-id="3f495-107">Método ID3D12DeviceDownlevel:: QueryVideoMemoryInfo</span><span class="sxs-lookup"><span data-stu-id="3f495-107">ID3D12DeviceDownlevel::QueryVideoMemoryInfo method</span></span>

<span data-ttu-id="3f495-108">Fornece estatísticas de memória no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3f495-108">Provides memory statistics on Windows 7.</span></span> <span data-ttu-id="3f495-109">Esse método é equivalente a [IDXGIAdapter3:: QueryVideoMemoryInfo](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo), que não está disponível no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3f495-109">This method is equivalent to [IDXGIAdapter3::QueryVideoMemoryInfo](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo), which is not available on Windows 7.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f495-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f495-110">Syntax</span></span>

```cpp
HRESULT QueryVideoMemoryInfo( 
    UINT NodeIndex,
    DXGI_MEMORY_SEGMENT_GROUP MemorySegmentGroup,
    DXGI_QUERY_VIDEO_MEMORY_INFO *pVideoMemoryInfo
);
```

## <a name="parameters"></a><span data-ttu-id="3f495-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f495-111">Parameters</span></span>

`NodeIndex`

<span data-ttu-id="3f495-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="3f495-112">Type: **UINT**</span></span>

<span data-ttu-id="3f495-113">Especifica o adaptador físico do dispositivo para o qual as informações de memória de vídeo são consultadas.</span><span class="sxs-lookup"><span data-stu-id="3f495-113">Specifies the device's physical adapter for which the video memory information is queried.</span></span> <span data-ttu-id="3f495-114">Para uma operação de GPU única, defina como zero.</span><span class="sxs-lookup"><span data-stu-id="3f495-114">For single-GPU operation, set this to zero.</span></span> <span data-ttu-id="3f495-115">Se houver vários nós de GPU, defina-o como o índice do nó (o adaptador físico do dispositivo) para o qual as informações de memória de vídeo são consultadas.</span><span class="sxs-lookup"><span data-stu-id="3f495-115">If there are multiple GPU nodes, set this to the index of the node (the device's physical adapter) for which the video memory information is queried.</span></span> <span data-ttu-id="3f495-116">Consulte [sistemas com vários adaptadores](multi-engine.md).</span><span class="sxs-lookup"><span data-stu-id="3f495-116">See [Multi-adapter systems](multi-engine.md).</span></span>

`MemorySegmentGroup`

<span data-ttu-id="3f495-117">Tipo: **[DXGI_MEMORY_SEGMENT_GROUP](/windows/win32/api/dxgi1_4/ne-dxgi1_4-dxgi_memory_segment_group)**</span><span class="sxs-lookup"><span data-stu-id="3f495-117">Type: **[DXGI_MEMORY_SEGMENT_GROUP](/windows/win32/api/dxgi1_4/ne-dxgi1_4-dxgi_memory_segment_group)**</span></span>

<span data-ttu-id="3f495-118">Especifica um **DXGI_MEMORY_SEGMENT_GROUP** que identifica o grupo como local ou não local.</span><span class="sxs-lookup"><span data-stu-id="3f495-118">Specifies a **DXGI_MEMORY_SEGMENT_GROUP** that identifies the group as local or non-local.</span></span>

`pVideoMemoryInfo`

<span data-ttu-id="3f495-119">Tipo: **[DXGI_QUERY_VIDEO_MEMORY_INFO](/windows/win32/api/dxgi1_4/ns-dxgi1_4-dxgi_query_video_memory_info)\***</span><span class="sxs-lookup"><span data-stu-id="3f495-119">Type: **[DXGI_QUERY_VIDEO_MEMORY_INFO](/windows/win32/api/dxgi1_4/ns-dxgi1_4-dxgi_query_video_memory_info)\***</span></span>

<span data-ttu-id="3f495-120">Preenche uma estrutura de **DXGI_QUERY_VIDEO_MEMORY_INFO** com os valores atuais.</span><span class="sxs-lookup"><span data-stu-id="3f495-120">Fills in a **DXGI_QUERY_VIDEO_MEMORY_INFO** structure with the current values.</span></span>

## <a name="return-value"></a><span data-ttu-id="3f495-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3f495-121">Return value</span></span>

<span data-ttu-id="3f495-122">Retorna **S_OK** em caso de êxito ou um HRESULT com falha.</span><span class="sxs-lookup"><span data-stu-id="3f495-122">Returns **S_OK** on success, or else a failing HRESULT.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f495-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f495-123">Requirements</span></span>

| <span data-ttu-id="3f495-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f495-124">Requirement</span></span> | <span data-ttu-id="3f495-125">Valor</span><span class="sxs-lookup"><span data-stu-id="3f495-125">Value</span></span> |
|--------|------------------|
| <span data-ttu-id="3f495-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3f495-126">Header</span></span> | <span data-ttu-id="3f495-127">d3d12downlevel. h e dxgi1_4. h</span><span class="sxs-lookup"><span data-stu-id="3f495-127">d3d12downlevel.h and dxgi1_4.h</span></span> |
| <span data-ttu-id="3f495-128">DLL</span><span class="sxs-lookup"><span data-stu-id="3f495-128">DLL</span></span>    | <span data-ttu-id="3f495-129">D3D12.dll (somente Windows 7)</span><span class="sxs-lookup"><span data-stu-id="3f495-129">D3D12.dll (Windows 7 only)</span></span> |

## <a name="see-also"></a><span data-ttu-id="3f495-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f495-130">See also</span></span>
* [<span data-ttu-id="3f495-131">ID3D12DeviceDownlevel</span><span class="sxs-lookup"><span data-stu-id="3f495-131">ID3D12DeviceDownlevel</span></span>](id3d12devicedownlevel.md)
* [<span data-ttu-id="3f495-132">O Direct3D 12 em interfaces do Windows 7</span><span class="sxs-lookup"><span data-stu-id="3f495-132">Direct3D 12 On Windows 7 interfaces</span></span>](direct3d-12on7-interfaces.md)
* [<span data-ttu-id="3f495-133">Referência do Direct3D 12 no Windows 7 (d3d12downlevel. h)</span><span class="sxs-lookup"><span data-stu-id="3f495-133">Direct3D 12 on Windows 7 reference (d3d12downlevel.h)</span></span>](direct3d-12on7-reference.md)
* [<span data-ttu-id="3f495-134">O Direct3D 12 no Windows 7</span><span class="sxs-lookup"><span data-stu-id="3f495-134">Direct3D 12 On Windows 7</span></span>](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
