---
title: Método IVMVirtualMachineEvents OnHeartbeatStopped (VPCCOMInterfaces. h)
description: Recebe a notificação de que a pulsação de uma máquina virtual foi interrompida.
ms.assetid: 58fc81a8-747c-47f9-98ec-38482694f533
keywords:
- OnHeartbeatStopped do método virtual PC
- Método OnHeartbeatStopped Virtual PC, interface IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface virtual PC, método OnHeartbeatStopped
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnHeartbeatStopped
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ade783d2d182439d5c500dcc114c74c8278ba6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918932"
---
# <a name="ivmvirtualmachineeventsonheartbeatstopped-method"></a><span data-ttu-id="e72e9-106">Método IVMVirtualMachineEvents:: OnHeartbeatStopped</span><span class="sxs-lookup"><span data-stu-id="e72e9-106">IVMVirtualMachineEvents::OnHeartbeatStopped method</span></span>

<span data-ttu-id="e72e9-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e72e9-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e72e9-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e72e9-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e72e9-109">Recebe a notificação de que a pulsação de uma máquina virtual foi interrompida.</span><span class="sxs-lookup"><span data-stu-id="e72e9-109">Receives notification that a virtual machine's heartbeat has stopped.</span></span>

## <a name="syntax"></a><span data-ttu-id="e72e9-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e72e9-110">Syntax</span></span>


```C++
HRESULT OnHeartbeatStopped();
```



## <a name="parameters"></a><span data-ttu-id="e72e9-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e72e9-111">Parameters</span></span>

<span data-ttu-id="e72e9-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e72e9-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e72e9-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e72e9-113">Return value</span></span>

<span data-ttu-id="e72e9-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e72e9-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e72e9-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e72e9-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e72e9-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e72e9-116">Remarks</span></span>

<span data-ttu-id="e72e9-117">Esse método é chamado quando o sistema operacional convidado para esta máquina virtual foi interrompido abruptamente.</span><span class="sxs-lookup"><span data-stu-id="e72e9-117">This method is called when the guest operating system for this virtual machine has stopped abruptly.</span></span> <span data-ttu-id="e72e9-118">O programa cliente deve implementar esse método de interface para receber a notificação do \_ evento vmVirtualMachineEvent HeartbeatStopped originado do [**IVMVirtualMachine**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="e72e9-118">The client program must implement this interface method to receive notification of the vmVirtualMachineEvent\_HeartbeatStopped event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e72e9-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e72e9-119">Requirements</span></span>



| <span data-ttu-id="e72e9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e72e9-120">Requirement</span></span> | <span data-ttu-id="e72e9-121">Valor</span><span class="sxs-lookup"><span data-stu-id="e72e9-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e72e9-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e72e9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e72e9-123">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e72e9-123">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e72e9-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e72e9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e72e9-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e72e9-125">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e72e9-126">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="e72e9-126">End of client support</span></span><br/>    | <span data-ttu-id="e72e9-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e72e9-127">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e72e9-128">Produto</span><span class="sxs-lookup"><span data-stu-id="e72e9-128">Product</span></span><br/>                  | <span data-ttu-id="e72e9-129">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e72e9-129">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e72e9-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e72e9-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e72e9-131"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e72e9-131"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e72e9-132">IID</span><span class="sxs-lookup"><span data-stu-id="e72e9-132">IID</span></span><br/>                      | <span data-ttu-id="e72e9-133">DIID \_ IVMVirtualMachineEvents é definido como 9d84f560-bb67-4961-BD12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="e72e9-133">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="e72e9-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="e72e9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e72e9-135">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="e72e9-135">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

