---
title: Enumeração VMVirtualPCEvent (VPCCOMInterfaces. h)
description: Especifica os eventos do Windows Virtual PC.
ms.assetid: 3b239cd0-d922-42de-8bcc-51f625c0d8b0
keywords:
- VMVirtualPCEvent de enumeração Virtual PC
topic_type:
- apiref
api_name:
- VMVirtualPCEvent
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4de7ecb639d0b62165dec691d522bed8116670c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009756"
---
# <a name="vmvirtualpcevent-enumeration"></a><span data-ttu-id="e430d-104">Enumeração VMVirtualPCEvent</span><span class="sxs-lookup"><span data-stu-id="e430d-104">VMVirtualPCEvent enumeration</span></span>

<span data-ttu-id="e430d-105">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e430d-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e430d-106">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e430d-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e430d-107">Especifica os eventos do Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="e430d-107">Specifies the Windows Virtual PC events.</span></span>

## <a name="syntax"></a><span data-ttu-id="e430d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e430d-108">Syntax</span></span>


```C++
typedef enum  { 
  vmVirtualPCEvent_VMStateChange  = 2,
  vmVirtualPCEvent_EventLogged    = 3
} VMVirtualPCEvent;
```



## <a name="constants"></a><span data-ttu-id="e430d-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="e430d-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e430d-110"><span id="vmVirtualPCEvent_VMStateChange"></span><span id="vmvirtualpcevent_vmstatechange"></span><span id="VMVIRTUALPCEVENT_VMSTATECHANGE"></span>**vmVirtualPCEvent \_ VMStateChange**</span><span class="sxs-lookup"><span data-stu-id="e430d-110"><span id="vmVirtualPCEvent_VMStateChange"></span><span id="vmvirtualpcevent_vmstatechange"></span><span id="VMVIRTUALPCEVENT_VMSTATECHANGE"></span>**vmVirtualPCEvent\_VMStateChange**</span></span>
</dt> <dd>

<span data-ttu-id="e430d-111">O estado de uma máquina virtual foi alterado.</span><span class="sxs-lookup"><span data-stu-id="e430d-111">A virtual machine's state has changed.</span></span>

</dd> <dt>

<span data-ttu-id="e430d-112"><span id="vmVirtualPCEvent_EventLogged"></span><span id="vmvirtualpcevent_eventlogged"></span><span id="VMVIRTUALPCEVENT_EVENTLOGGED"></span>**vmVirtualPCEvent \_ EventLogged**</span><span class="sxs-lookup"><span data-stu-id="e430d-112"><span id="vmVirtualPCEvent_EventLogged"></span><span id="vmvirtualpcevent_eventlogged"></span><span id="VMVIRTUALPCEVENT_EVENTLOGGED"></span>**vmVirtualPCEvent\_EventLogged**</span></span>
</dt> <dd>

<span data-ttu-id="e430d-113">O Virtual PC registrou um evento.</span><span class="sxs-lookup"><span data-stu-id="e430d-113">Virtual PC has logged an event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e430d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e430d-114">Requirements</span></span>



| <span data-ttu-id="e430d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e430d-115">Requirement</span></span> | <span data-ttu-id="e430d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e430d-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e430d-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e430d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e430d-118">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e430d-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e430d-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e430d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e430d-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e430d-120">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e430d-121">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="e430d-121">End of client support</span></span><br/>    | <span data-ttu-id="e430d-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e430d-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e430d-123">Produto</span><span class="sxs-lookup"><span data-stu-id="e430d-123">Product</span></span><br/>                  | <span data-ttu-id="e430d-124">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e430d-124">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e430d-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e430d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e430d-126"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e430d-126"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e430d-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="e430d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e430d-128">**IVMVirtualPCEvents**</span><span class="sxs-lookup"><span data-stu-id="e430d-128">**IVMVirtualPCEvents**</span></span>](ivmvirtualpcevents.md)
</dt> </dl>

 

