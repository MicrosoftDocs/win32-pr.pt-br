---
title: Enumeração VMLogoffType (VPCCOMInterfaces. h)
description: Especifica como desligar uma máquina virtual.
ms.assetid: 3a2965e3-2637-4677-b487-98d2b508672c
keywords:
- VMLogoffType de enumeração Virtual PC
topic_type:
- apiref
api_name:
- VMLogoffType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c2311736115390d807058bbfc54c24e7f9e9654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009324"
---
# <a name="vmlogofftype-enumeration"></a><span data-ttu-id="f88a0-104">Enumeração VMLogoffType</span><span class="sxs-lookup"><span data-stu-id="f88a0-104">VMLogoffType enumeration</span></span>

<span data-ttu-id="f88a0-105">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f88a0-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f88a0-106">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f88a0-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f88a0-107">Especifica como desligar uma máquina virtual (VM).</span><span class="sxs-lookup"><span data-stu-id="f88a0-107">Specifies how to shut down a virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="f88a0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f88a0-108">Syntax</span></span>


```C++
typedef enum  { 
  vmLogoff_Normal    = 0,
  vmLogoff_Forced    = 1,
  vmLogoff_External  = 2
} VMLogoffType;
```



## <a name="constants"></a><span data-ttu-id="f88a0-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="f88a0-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f88a0-110"><span id="vmLogoff_Normal"></span><span id="vmlogoff_normal"></span><span id="VMLOGOFF_NORMAL"></span>**vmLogoff \_ normal**</span><span class="sxs-lookup"><span data-stu-id="f88a0-110"><span id="vmLogoff_Normal"></span><span id="vmlogoff_normal"></span><span id="VMLOGOFF_NORMAL"></span>**vmLogoff\_Normal**</span></span>
</dt> <dd>

<span data-ttu-id="f88a0-111">O logoff na VM convidada foi normal.</span><span class="sxs-lookup"><span data-stu-id="f88a0-111">The logoff in the guest VM was normal.</span></span>

</dd> <dt>

<span data-ttu-id="f88a0-112"><span id="vmLogoff_Forced"></span><span id="vmlogoff_forced"></span><span id="VMLOGOFF_FORCED"></span>**vmLogoff \_ forçado**</span><span class="sxs-lookup"><span data-stu-id="f88a0-112"><span id="vmLogoff_Forced"></span><span id="vmlogoff_forced"></span><span id="VMLOGOFF_FORCED"></span>**vmLogoff\_Forced**</span></span>
</dt> <dd>

<span data-ttu-id="f88a0-113">O logoff na VM convidada foi forçado.</span><span class="sxs-lookup"><span data-stu-id="f88a0-113">The logoff in the guest VM was forced.</span></span>

</dd> <dt>

<span data-ttu-id="f88a0-114"><span id="vmLogoff_External"></span><span id="vmlogoff_external"></span><span id="VMLOGOFF_EXTERNAL"></span>**vmLogoff \_ externo**</span><span class="sxs-lookup"><span data-stu-id="f88a0-114"><span id="vmLogoff_External"></span><span id="vmlogoff_external"></span><span id="VMLOGOFF_EXTERNAL"></span>**vmLogoff\_External**</span></span>
</dt> <dd>

<span data-ttu-id="f88a0-115">O logoff na VM convidada foi feito usando o método [**IVMGuestOS:: logoff**](ivmguestos-logoff.md) .</span><span class="sxs-lookup"><span data-stu-id="f88a0-115">The logoff in the guest VM was done using the [**IVMGuestOS::Logoff**](ivmguestos-logoff.md) method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f88a0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f88a0-116">Requirements</span></span>



| <span data-ttu-id="f88a0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f88a0-117">Requirement</span></span> | <span data-ttu-id="f88a0-118">Valor</span><span class="sxs-lookup"><span data-stu-id="f88a0-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f88a0-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f88a0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f88a0-120">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f88a0-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f88a0-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f88a0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f88a0-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f88a0-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f88a0-123">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="f88a0-123">End of client support</span></span><br/>    | <span data-ttu-id="f88a0-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f88a0-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f88a0-125">Produto</span><span class="sxs-lookup"><span data-stu-id="f88a0-125">Product</span></span><br/>                  | <span data-ttu-id="f88a0-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f88a0-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f88a0-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f88a0-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f88a0-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f88a0-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f88a0-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="f88a0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f88a0-130">**IVMVirtualMachine::ShutdownActionOnQuit**</span><span class="sxs-lookup"><span data-stu-id="f88a0-130">**IVMVirtualMachine::ShutdownActionOnQuit**</span></span>](ivmvirtualmachine-shutdownactiononquit.md)
</dt> </dl>

 

