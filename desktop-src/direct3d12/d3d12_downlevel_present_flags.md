---
title: Enumeração de D3D12_DOWNLEVEL_PRESENT_FLAGS
description: Sinalizadores passados para o método ID3D12CommandQueueDownlevel::P reenviado.
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
topic_type:
- APIRef
api_name:
- D3D12_DOWNLEVEL_PRESENT_FLAGS
api_type:
- HeaderDef
ms.openlocfilehash: 1ce1536945748bae09fc7a0981c14c076fc6394e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105790645"
---
# <a name="d3d12_downlevel_present_flags-enumeration"></a><span data-ttu-id="687c0-103">\_Enumeração de \_ \_ sinalizadores presentes de D3D12 de nível inferior</span><span class="sxs-lookup"><span data-stu-id="687c0-103">D3D12\_DOWNLEVEL\_PRESENT\_FLAGS enumeration</span></span>

<span data-ttu-id="687c0-104">Sinalizadores passados para a função [**ID3D12CommandQueueDownlevel::P reenviada**](id3d12commandqueuedownlevel-present.md) para modificar o comportamento.</span><span class="sxs-lookup"><span data-stu-id="687c0-104">Flags passed to the [**ID3D12CommandQueueDownlevel::Present**](id3d12commandqueuedownlevel-present.md) function to modify behavior.</span></span>

## <a name="syntax"></a><span data-ttu-id="687c0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="687c0-105">Syntax</span></span>

```cpp
enum D3D12_DOWNLEVEL_PRESENT_FLAGS
{
    D3D12_DOWNLEVEL_PRESENT_FLAG_NONE = 0,
    D3D12_DOWNLEVEL_PRESENT_FLAG_WAIT_FOR_VBLANK = 1
};
```

## <a name="constants"></a><span data-ttu-id="687c0-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="687c0-106">Constants</span></span>

<span data-ttu-id="687c0-107">**\_Sinalizador de apresentação de nível inferior D3D12 \_ \_ \_ None**</span><span class="sxs-lookup"><span data-stu-id="687c0-107">**D3D12\_DOWNLEVEL\_PRESENT\_FLAG\_NONE**</span></span>

<span data-ttu-id="687c0-108">Nenhuma opção selecionada.</span><span class="sxs-lookup"><span data-stu-id="687c0-108">No options selected.</span></span>

<span data-ttu-id="687c0-109">**D3D12 \_ \_ \_ de sinalizador presente \_ de nível inferior \_ de \_ VBLANK**</span><span class="sxs-lookup"><span data-stu-id="687c0-109">**D3D12\_DOWNLEVEL\_PRESENT\_FLAG\_WAIT\_FOR\_VBLANK**</span></span>

<span data-ttu-id="687c0-110">A operação **atual** não será feita até que um vsync tenha ocorrido desde a última vez que você **apresentar** o Ed.</span><span class="sxs-lookup"><span data-stu-id="687c0-110">The **Present** operation won't be done until a VSync has occurred since the last time you **Present** ed.</span></span>

## <a name="requirements"></a><span data-ttu-id="687c0-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="687c0-111">Requirements</span></span>

| <span data-ttu-id="687c0-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="687c0-112">Requirement</span></span> | <span data-ttu-id="687c0-113">Valor</span><span class="sxs-lookup"><span data-stu-id="687c0-113">Value</span></span> |
|--------|------------------|
| <span data-ttu-id="687c0-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="687c0-114">Header</span></span> | <span data-ttu-id="687c0-115">d3d12downlevel. h</span><span class="sxs-lookup"><span data-stu-id="687c0-115">d3d12downlevel.h</span></span> |
| <span data-ttu-id="687c0-116">DLL</span><span class="sxs-lookup"><span data-stu-id="687c0-116">DLL</span></span>    | <span data-ttu-id="687c0-117">D3D12.dll (somente Windows 7)</span><span class="sxs-lookup"><span data-stu-id="687c0-117">D3D12.dll (Windows 7 only)</span></span> |

## <a name="see-also"></a><span data-ttu-id="687c0-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="687c0-118">See also</span></span>
* [<span data-ttu-id="687c0-119">ID3D12CommandQueueDownlevel</span><span class="sxs-lookup"><span data-stu-id="687c0-119">ID3D12CommandQueueDownlevel</span></span>](id3d12commandqueuedownlevel.md)
* [<span data-ttu-id="687c0-120">Enumerações do Direct3D 12 no Windows 7</span><span class="sxs-lookup"><span data-stu-id="687c0-120">Direct3D 12 On Windows 7 enumerations</span></span>](direct3d-12on7-enumerations.md)
* [<span data-ttu-id="687c0-121">Referência do Direct3D 12 no Windows 7 (d3d12downlevel. h)</span><span class="sxs-lookup"><span data-stu-id="687c0-121">Direct3D 12 on Windows 7 reference (d3d12downlevel.h)</span></span>](direct3d-12on7-reference.md)
* [<span data-ttu-id="687c0-122">O Direct3D 12 no Windows 7</span><span class="sxs-lookup"><span data-stu-id="687c0-122">Direct3D 12 On Windows 7</span></span>](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
