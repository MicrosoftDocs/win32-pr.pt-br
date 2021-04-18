---
title: 'ID3D12CommandQueueDownlevel: método reenviado:P'
description: 'Copia o conteúdo de um recurso do Direct3D 12 Texture2D para uma janela. | ID3D12CommandQueueDownlevel: método reenviado:P'
keywords:
- Método presente
- Método presente, interface ID3D12CommandQueueDownlevel
- Interface ID3D12CommandQueueDownlevel, método presente
topic_type:
- apiref
api_name:
- ID3D12CommandQueueDownlevel.Present
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: a6c74685911e52a671eaeb02645754a45b8d647e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105802159"
---
# <a name="id3d12commandqueuedownlevelpresent-method"></a><span data-ttu-id="1897d-107">ID3D12CommandQueueDownlevel: método reenviado:P</span><span class="sxs-lookup"><span data-stu-id="1897d-107">ID3D12CommandQueueDownlevel::Present method</span></span>

<span data-ttu-id="1897d-108">Copia o conteúdo de um recurso do Direct3D 12 Texture2D para uma janela.</span><span class="sxs-lookup"><span data-stu-id="1897d-108">Copies contents from a Direct3D 12 Texture2D resource into a window.</span></span>

## <a name="syntax"></a><span data-ttu-id="1897d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1897d-109">Syntax</span></span>

```cpp
HRESULT Present
    ID3D12GraphicsCommandList *pOpenCommandList,
    ID3D12Resource *pSourceTex2D,
    HWND hWindow,
    D3D12_DOWNLEVEL_PRESENT_FLAGS Flags
);
```

## <a name="parameters"></a><span data-ttu-id="1897d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1897d-110">Parameters</span></span>

`pOpenCommandList`

<span data-ttu-id="1897d-111">Tipo: **[ID3D12GraphicsCommandList](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span><span class="sxs-lookup"><span data-stu-id="1897d-111">Type: **[ID3D12GraphicsCommandList](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span></span>

<span data-ttu-id="1897d-112">Uma lista de comandos aberta, que o Direct3D 12 enfileira um comando presente em e, em seguida, fecha e envia para você.</span><span class="sxs-lookup"><span data-stu-id="1897d-112">An open command list, which Direct3D 12 enqueues a Present command onto, and then closes and submits for you.</span></span>

`pSourceTex2D`

<span data-ttu-id="1897d-113">Tipo: **[ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="1897d-113">Type: **[ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="1897d-114">Um recurso que contém o conteúdo desejado a ser exibido, com Dimension [**D3D12 \_ Resource \_ Dimension \_ TEXTURE2D**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension)e um formato que seja um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="1897d-114">A resource containing your desired contents to display, with dimension [**D3D12\_RESOURCE\_DIMENSION\_TEXTURE2D**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension), and a format that is one of the following.</span></span>

* <span data-ttu-id="1897d-115">DXGI_FORMAT_R16G16B16A16_FLOAT</span><span class="sxs-lookup"><span data-stu-id="1897d-115">DXGI_FORMAT_R16G16B16A16_FLOAT</span></span>
* <span data-ttu-id="1897d-116">DXGI_FORMAT_R10G10B10A2_UNORM</span><span class="sxs-lookup"><span data-stu-id="1897d-116">DXGI_FORMAT_R10G10B10A2_UNORM</span></span>
* <span data-ttu-id="1897d-117">DXGI_FORMAT_R8G8B8A8_UNORM</span><span class="sxs-lookup"><span data-stu-id="1897d-117">DXGI_FORMAT_R8G8B8A8_UNORM</span></span>
* <span data-ttu-id="1897d-118">DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</span><span class="sxs-lookup"><span data-stu-id="1897d-118">DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</span></span>
* <span data-ttu-id="1897d-119">DXGI_FORMAT_B8G8R8X8_UNORM</span><span class="sxs-lookup"><span data-stu-id="1897d-119">DXGI_FORMAT_B8G8R8X8_UNORM</span></span>
* <span data-ttu-id="1897d-120">DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM</span><span class="sxs-lookup"><span data-stu-id="1897d-120">DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM</span></span>
* <span data-ttu-id="1897d-121">DXGI_FORMAT_B8G8R8A8_UNORM</span><span class="sxs-lookup"><span data-stu-id="1897d-121">DXGI_FORMAT_B8G8R8A8_UNORM</span></span>
* <span data-ttu-id="1897d-122">DXGI_FORMAT_B8G8R8A8_UNORM_SRGB</span><span class="sxs-lookup"><span data-stu-id="1897d-122">DXGI_FORMAT_B8G8R8A8_UNORM_SRGB</span></span>

`hWindow`

<span data-ttu-id="1897d-123">Tipo: **[HWND](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1897d-123">Type: **[HWND](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1897d-124">O identificador para a janela em que o conteúdo deve ser exibido.</span><span class="sxs-lookup"><span data-stu-id="1897d-124">The handle to the window where the contents should be displayed.</span></span>

`Flags`

<span data-ttu-id="1897d-125">Tipo: **[ \_ \_ \_ sinalizadores presentes de D3D12 de nível inferior](d3d12_downlevel_present_flags.md)**</span><span class="sxs-lookup"><span data-stu-id="1897d-125">Type: **[D3D12\_DOWNLEVEL\_PRESENT\_FLAGS](d3d12_downlevel_present_flags.md)**</span></span>

<span data-ttu-id="1897d-126">Sinalizadores para modificar a operação **atual** .</span><span class="sxs-lookup"><span data-stu-id="1897d-126">Flags to modify the **Present** operation.</span></span>

## <a name="return-value"></a><span data-ttu-id="1897d-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1897d-127">Return value</span></span>

<span data-ttu-id="1897d-128">Retorna **S_OK** em caso de êxito ou um HRESULT com falha.</span><span class="sxs-lookup"><span data-stu-id="1897d-128">Returns **S_OK** on success, or else a failing HRESULT.</span></span>

## <a name="requirements"></a><span data-ttu-id="1897d-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1897d-129">Requirements</span></span>

| <span data-ttu-id="1897d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1897d-130">Requirement</span></span> | <span data-ttu-id="1897d-131">Valor</span><span class="sxs-lookup"><span data-stu-id="1897d-131">Value</span></span> |
|--------|------------------|
| <span data-ttu-id="1897d-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1897d-132">Header</span></span> | <span data-ttu-id="1897d-133">d3d12downlevel. h</span><span class="sxs-lookup"><span data-stu-id="1897d-133">d3d12downlevel.h</span></span> |
| <span data-ttu-id="1897d-134">DLL</span><span class="sxs-lookup"><span data-stu-id="1897d-134">DLL</span></span>    | <span data-ttu-id="1897d-135">D3D12.dll (somente Windows 7)</span><span class="sxs-lookup"><span data-stu-id="1897d-135">D3D12.dll (Windows 7 only)</span></span> |

## <a name="see-also"></a><span data-ttu-id="1897d-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="1897d-136">See also</span></span>
* [<span data-ttu-id="1897d-137">ID3D12CommandQueueDownlevel</span><span class="sxs-lookup"><span data-stu-id="1897d-137">ID3D12CommandQueueDownlevel</span></span>](id3d12commandqueuedownlevel.md)
* [<span data-ttu-id="1897d-138">O Direct3D 12 em interfaces do Windows 7</span><span class="sxs-lookup"><span data-stu-id="1897d-138">Direct3D 12 On Windows 7 interfaces</span></span>](direct3d-12on7-interfaces.md)
* [<span data-ttu-id="1897d-139">Referência do Direct3D 12 no Windows 7 (d3d12downlevel. h)</span><span class="sxs-lookup"><span data-stu-id="1897d-139">Direct3D 12 on Windows 7 reference (d3d12downlevel.h)</span></span>](direct3d-12on7-reference.md)
* [<span data-ttu-id="1897d-140">O Direct3D 12 no Windows 7</span><span class="sxs-lookup"><span data-stu-id="1897d-140">Direct3D 12 On Windows 7</span></span>](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
