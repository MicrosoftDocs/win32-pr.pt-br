---
title: Enumeração VMShutdownAction (VPCCOMInterfaces. h)
description: Especifica como desligar uma máquina virtual quando o host é desligado ou o processo de vpc.exe é encerrado.
ms.assetid: 271a685a-cac9-4a15-b363-bf8873fd5324
keywords:
- VMShutdownAction de enumeração Virtual PC
topic_type:
- apiref
api_name:
- VMShutdownAction
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b939954042a446f7ad9f128580e804d73e9d29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105781120"
---
# <a name="vmshutdownaction-enumeration"></a><span data-ttu-id="98986-104">Enumeração VMShutdownAction</span><span class="sxs-lookup"><span data-stu-id="98986-104">VMShutdownAction enumeration</span></span>

<span data-ttu-id="98986-105">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="98986-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="98986-106">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="98986-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="98986-107">Especifica como desligar uma máquina virtual (VM) quando o host é desligado ou o processo de vpc.exe é encerrado.</span><span class="sxs-lookup"><span data-stu-id="98986-107">Specifies how to shut down a virtual machine (VM) when the host shuts down or the vpc.exe process exits.</span></span>

## <a name="syntax"></a><span data-ttu-id="98986-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="98986-108">Syntax</span></span>


```C++
typedef enum  { 
  vmShutdownAction_Save      = 0,
  vmShutdownAction_TurnOff   = 1,
  vmShutdownAction_Shutdown  = 2
} VMShutdownAction;
```



## <a name="constants"></a><span data-ttu-id="98986-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="98986-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="98986-110"><span id="vmShutdownAction_Save"></span><span id="vmshutdownaction_save"></span><span id="VMSHUTDOWNACTION_SAVE"></span>**vmShutdownAction \_ salvar**</span><span class="sxs-lookup"><span data-stu-id="98986-110"><span id="vmShutdownAction_Save"></span><span id="vmshutdownaction_save"></span><span id="VMSHUTDOWNACTION_SAVE"></span>**vmShutdownAction\_Save**</span></span>
</dt> <dd>

<span data-ttu-id="98986-111">Salve o estado da VM.</span><span class="sxs-lookup"><span data-stu-id="98986-111">Save the VM state.</span></span>

</dd> <dt>

<span data-ttu-id="98986-112"><span id="vmShutdownAction_TurnOff"></span><span id="vmshutdownaction_turnoff"></span><span id="VMSHUTDOWNACTION_TURNOFF"></span>**desativação \_ de vmShutdownAction**</span><span class="sxs-lookup"><span data-stu-id="98986-112"><span id="vmShutdownAction_TurnOff"></span><span id="vmshutdownaction_turnoff"></span><span id="VMSHUTDOWNACTION_TURNOFF"></span>**vmShutdownAction\_TurnOff**</span></span>
</dt> <dd>

<span data-ttu-id="98986-113">Desative a VM sem desfazer as unidades.</span><span class="sxs-lookup"><span data-stu-id="98986-113">Turn off the VM without undoing the drives.</span></span>

</dd> <dt>

<span data-ttu-id="98986-114"><span id="vmShutdownAction_Shutdown"></span><span id="vmshutdownaction_shutdown"></span><span id="VMSHUTDOWNACTION_SHUTDOWN"></span>**\_desligamento vmShutdownAction**</span><span class="sxs-lookup"><span data-stu-id="98986-114"><span id="vmShutdownAction_Shutdown"></span><span id="vmshutdownaction_shutdown"></span><span id="VMSHUTDOWNACTION_SHUTDOWN"></span>**vmShutdownAction\_Shutdown**</span></span>
</dt> <dd>

<span data-ttu-id="98986-115">Desligue o sistema operacional convidado na VM sem desfazer as unidades se os componentes de integração estiverem disponíveis e, caso contrário, salvará a VM.</span><span class="sxs-lookup"><span data-stu-id="98986-115">Shut down the guest operating system on the VM without undoing the drives if the integration components are available and will save the VM otherwise.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="98986-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98986-116">Requirements</span></span>



| <span data-ttu-id="98986-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="98986-117">Requirement</span></span> | <span data-ttu-id="98986-118">Valor</span><span class="sxs-lookup"><span data-stu-id="98986-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="98986-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98986-119">Minimum supported client</span></span><br/> | <span data-ttu-id="98986-120">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="98986-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="98986-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98986-121">Minimum supported server</span></span><br/> | <span data-ttu-id="98986-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="98986-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="98986-123">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="98986-123">End of client support</span></span><br/>    | <span data-ttu-id="98986-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="98986-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="98986-125">Produto</span><span class="sxs-lookup"><span data-stu-id="98986-125">Product</span></span><br/>                  | <span data-ttu-id="98986-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="98986-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="98986-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="98986-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="98986-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="98986-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98986-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="98986-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98986-130">Enumerações do Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="98986-130">Windows Virtual PC Enumerations</span></span>](virtual-pc-enumerations.md)
</dt> <dt>

[<span data-ttu-id="98986-131">**IVMVirtualMachine::ShutdownActionOnQuit**</span><span class="sxs-lookup"><span data-stu-id="98986-131">**IVMVirtualMachine::ShutdownActionOnQuit**</span></span>](ivmvirtualmachine-shutdownactiononquit.md)
</dt> </dl>

 

