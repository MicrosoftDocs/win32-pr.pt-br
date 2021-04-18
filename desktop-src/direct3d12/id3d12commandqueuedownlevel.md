---
title: Interface ID3D12CommandQueueDownlevel
description: Fornece um mecanismo presente do Windows-7 específico.
keywords:
- Interface ID3D12CommandQueueDownlevel
topic_type:
- apiref
api_name:
- ID3D12CommandQueueDownlevel
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 6f2aee6fd1b0f58469162c640d92aeb187bd9641
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105769660"
---
# <a name="id3d12commandqueuedownlevel-interface"></a><span data-ttu-id="00b3f-104">Interface ID3D12CommandQueueDownlevel</span><span class="sxs-lookup"><span data-stu-id="00b3f-104">ID3D12CommandQueueDownlevel interface</span></span>

<span data-ttu-id="00b3f-105">Essa interface pode ser acessada por meio de **QueryInterface** de uma [fila de comando do Direct3D 12](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) ao usar o [Direct3D 12 no Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/).</span><span class="sxs-lookup"><span data-stu-id="00b3f-105">This interface can be accessed via **QueryInterface** off of a [Direct3D 12 command queue](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) when using [Direct3D 12 on Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/).</span></span> <span data-ttu-id="00b3f-106">Ele fornece um mecanismo presente do Windows-7 específico.</span><span class="sxs-lookup"><span data-stu-id="00b3f-106">It provides a Windows-7-specific present mechanism.</span></span>

### <a name="methods"></a><span data-ttu-id="00b3f-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="00b3f-107">Methods</span></span>

<span data-ttu-id="00b3f-108">A interface **ID3D12CommandQueueDownlevel** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="00b3f-108">The **ID3D12CommandQueueDownlevel** interface has these methods.</span></span>

| <span data-ttu-id="00b3f-109">Método</span><span class="sxs-lookup"><span data-stu-id="00b3f-109">Method</span></span> | <span data-ttu-id="00b3f-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="00b3f-110">Description</span></span> |
|:-------|:------------|
| [<span data-ttu-id="00b3f-111">**Existi**</span><span class="sxs-lookup"><span data-stu-id="00b3f-111">**Present**</span></span>](id3d12commandqueuedownlevel-present.md) | <span data-ttu-id="00b3f-112">Copia o conteúdo de um recurso D3D12 Texture2D para uma janela.</span><span class="sxs-lookup"><span data-stu-id="00b3f-112">Copies contents from a D3D12 Texture2D resource into a window.</span></span> |

## <a name="requirements"></a><span data-ttu-id="00b3f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00b3f-113">Requirements</span></span>

| <span data-ttu-id="00b3f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="00b3f-114">Requirement</span></span> | <span data-ttu-id="00b3f-115">Valor</span><span class="sxs-lookup"><span data-stu-id="00b3f-115">Value</span></span> |
|--------|------------------|
| <span data-ttu-id="00b3f-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="00b3f-116">Header</span></span> | <span data-ttu-id="00b3f-117">d3d12downlevel. h</span><span class="sxs-lookup"><span data-stu-id="00b3f-117">d3d12downlevel.h</span></span> |
| <span data-ttu-id="00b3f-118">DLL</span><span class="sxs-lookup"><span data-stu-id="00b3f-118">DLL</span></span>    | <span data-ttu-id="00b3f-119">D3D12.dll (somente Windows 7)</span><span class="sxs-lookup"><span data-stu-id="00b3f-119">D3D12.dll (Windows 7 only)</span></span> |

## <a name="see-also"></a><span data-ttu-id="00b3f-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="00b3f-120">See also</span></span>
* [<span data-ttu-id="00b3f-121">O Direct3D 12 em interfaces do Windows 7</span><span class="sxs-lookup"><span data-stu-id="00b3f-121">Direct3D 12 On Windows 7 interfaces</span></span>](direct3d-12on7-interfaces.md)
* [<span data-ttu-id="00b3f-122">Referência do Direct3D 12 no Windows 7 (d3d12downlevel. h)</span><span class="sxs-lookup"><span data-stu-id="00b3f-122">Direct3D 12 on Windows 7 reference (d3d12downlevel.h)</span></span>](direct3d-12on7-reference.md)
* [<span data-ttu-id="00b3f-123">O Direct3D 12 no Windows 7</span><span class="sxs-lookup"><span data-stu-id="00b3f-123">Direct3D 12 On Windows 7</span></span>](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
