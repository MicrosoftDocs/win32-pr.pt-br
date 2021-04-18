---
title: Interface ID3D12DeviceDownlevel
description: Fornece uma consulta de estatísticas de memória específica do Windows-7.
keywords:
- Interface ID3D12DeviceDownlevel
topic_type:
- apiref
api_name:
- ID3D12DeviceDownlevel
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 401cbd0045211ef51e3ef6b06042262964ae2ec5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105764320"
---
# <a name="id3d12devicedownlevel-interface"></a><span data-ttu-id="d2e39-104">Interface ID3D12DeviceDownlevel</span><span class="sxs-lookup"><span data-stu-id="d2e39-104">ID3D12DeviceDownlevel interface</span></span>

<span data-ttu-id="d2e39-105">Essa interface pode ser acessada por meio de **QueryInterface** de um [dispositivo Direct3D 12](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) ao usar o [Direct3D 12 no Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/).</span><span class="sxs-lookup"><span data-stu-id="d2e39-105">This interface can be accessed via **QueryInterface** off of a [Direct3D 12 device](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) when using [Direct3D 12 on Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/).</span></span> <span data-ttu-id="d2e39-106">Ele fornece uma consulta de estatísticas de memória específica do Windows-7.</span><span class="sxs-lookup"><span data-stu-id="d2e39-106">It provides a Windows-7-specific memory statistics query.</span></span>

### <a name="methods"></a><span data-ttu-id="d2e39-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="d2e39-107">Methods</span></span>

<span data-ttu-id="d2e39-108">A interface **ID3D12DeviceDownlevel** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="d2e39-108">The **ID3D12DeviceDownlevel** interface has these methods.</span></span>

| <span data-ttu-id="d2e39-109">Método</span><span class="sxs-lookup"><span data-stu-id="d2e39-109">Method</span></span> | <span data-ttu-id="d2e39-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="d2e39-110">Description</span></span> |
|:-------|:------------|
| [<span data-ttu-id="d2e39-111">**QueryVideoMemoryInfo**</span><span class="sxs-lookup"><span data-stu-id="d2e39-111">**QueryVideoMemoryInfo**</span></span>](id3d12devicedownlevel-queryvideomemoryinfo.md) | <span data-ttu-id="d2e39-112">Fornece estatísticas de memória no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d2e39-112">Provides memory statistics on Windows 7.</span></span> |

## <a name="requirements"></a><span data-ttu-id="d2e39-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2e39-113">Requirements</span></span>

| <span data-ttu-id="d2e39-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2e39-114">Requirement</span></span> | <span data-ttu-id="d2e39-115">Valor</span><span class="sxs-lookup"><span data-stu-id="d2e39-115">Value</span></span> |
|--------|------------------|
| <span data-ttu-id="d2e39-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d2e39-116">Header</span></span> | <span data-ttu-id="d2e39-117">d3d12downlevel. h</span><span class="sxs-lookup"><span data-stu-id="d2e39-117">d3d12downlevel.h</span></span> |
| <span data-ttu-id="d2e39-118">DLL</span><span class="sxs-lookup"><span data-stu-id="d2e39-118">DLL</span></span>    | <span data-ttu-id="d2e39-119">D3D12.dll (somente Windows 7)</span><span class="sxs-lookup"><span data-stu-id="d2e39-119">D3D12.dll (Windows 7 only)</span></span> |

## <a name="see-also"></a><span data-ttu-id="d2e39-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2e39-120">See also</span></span>
* [<span data-ttu-id="d2e39-121">O Direct3D 12 em interfaces do Windows 7</span><span class="sxs-lookup"><span data-stu-id="d2e39-121">Direct3D 12 On Windows 7 interfaces</span></span>](direct3d-12on7-interfaces.md)
* [<span data-ttu-id="d2e39-122">Referência do Direct3D 12 no Windows 7 (d3d12downlevel. h)</span><span class="sxs-lookup"><span data-stu-id="d2e39-122">Direct3D 12 on Windows 7 reference (d3d12downlevel.h)</span></span>](direct3d-12on7-reference.md)
* [<span data-ttu-id="d2e39-123">O Direct3D 12 no Windows 7</span><span class="sxs-lookup"><span data-stu-id="d2e39-123">Direct3D 12 On Windows 7</span></span>](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
