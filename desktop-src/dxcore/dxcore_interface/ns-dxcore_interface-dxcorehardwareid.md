---
title: DXCoreHardwareID
description: Representa as partes de ID de hardware de PnP para um adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6882d9aa16bf72fb33f9a254a6434becb37f9cb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084609"
---
# <a name="dxcorehardwareid-structure"></a><span data-ttu-id="465d0-103">Estrutura DXCoreHardwareID</span><span class="sxs-lookup"><span data-stu-id="465d0-103">DXCoreHardwareID structure</span></span>

<span data-ttu-id="465d0-104">Representa as partes de ID de hardware de PnP para um adaptador.</span><span class="sxs-lookup"><span data-stu-id="465d0-104">Represents the PnP hardware ID parts for an adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="465d0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="465d0-105">Syntax</span></span>

```cpp
struct DXCoreHardwareID
{
  uint32_t vendorID;
  uint32_t deviceID;
  uint32_t subSysID;
  uint32_t revision;
};
```

## <a name="members"></a><span data-ttu-id="465d0-106">Membros</span><span class="sxs-lookup"><span data-stu-id="465d0-106">Members</span></span>

### <a name="vendorid"></a><span data-ttu-id="465d0-107">vendorId</span><span class="sxs-lookup"><span data-stu-id="465d0-107">vendorId</span></span>

<span data-ttu-id="465d0-108">Tipo: **uint32_t \***</span><span class="sxs-lookup"><span data-stu-id="465d0-108">Type: **uint32_t\***</span></span>

<span data-ttu-id="465d0-109">A ID de PCI do fornecedor de hardware do adaptador.</span><span class="sxs-lookup"><span data-stu-id="465d0-109">The PCI ID of the adapter's hardware vendor.</span></span>

### <a name="deviceid"></a><span data-ttu-id="465d0-110">deviceId</span><span class="sxs-lookup"><span data-stu-id="465d0-110">deviceId</span></span>

<span data-ttu-id="465d0-111">Tipo: **uint32_t \***</span><span class="sxs-lookup"><span data-stu-id="465d0-111">Type: **uint32_t\***</span></span>

<span data-ttu-id="465d0-112">A ID de PCI do dispositivo de hardware do adaptador.</span><span class="sxs-lookup"><span data-stu-id="465d0-112">The PCI ID of the adapter's hardware device.</span></span>

### <a name="subsysid"></a><span data-ttu-id="465d0-113">subSysId</span><span class="sxs-lookup"><span data-stu-id="465d0-113">subSysId</span></span>

<span data-ttu-id="465d0-114">Tipo: **uint32_t \***</span><span class="sxs-lookup"><span data-stu-id="465d0-114">Type: **uint32_t\***</span></span>

<span data-ttu-id="465d0-115">A ID de PCI do subsistema de hardware do adaptador.</span><span class="sxs-lookup"><span data-stu-id="465d0-115">The PCI ID of the adapter's hardware subsystem.</span></span>

### <a name="revision"></a><span data-ttu-id="465d0-116">revisão</span><span class="sxs-lookup"><span data-stu-id="465d0-116">revision</span></span>

<span data-ttu-id="465d0-117">Tipo: **uint32_t \***</span><span class="sxs-lookup"><span data-stu-id="465d0-117">Type: **uint32_t\***</span></span>

<span data-ttu-id="465d0-118">A ID de PCI do número de revisão do adaptador.</span><span class="sxs-lookup"><span data-stu-id="465d0-118">The PCI ID of the adapter's revision number.</span></span>

## <a name="see-also"></a><span data-ttu-id="465d0-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="465d0-119">See also</span></span>

<span data-ttu-id="465d0-120">[Referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="465d0-120">[DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>