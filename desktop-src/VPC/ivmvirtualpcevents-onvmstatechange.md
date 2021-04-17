---
title: Método IVMVirtualPCEvents OnVMStateChange (VPCCOMInterfaces. h)
description: Recebe a notificação de que o estado de uma máquina virtual foi alterado. | Método IVMVirtualPCEvents OnVMStateChange (VPCCOMInterfaces. h)
ms.assetid: a79afe14-9b7d-4528-ad38-e9b5ad068561
keywords:
- OnVMStateChange do método virtual PC
- Método OnVMStateChange Virtual PC, interface IVMVirtualPCEvents
- IVMVirtualPCEvents interface virtual PC, método OnVMStateChange
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents.OnVMStateChange
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d0a8bd9a362c558c307fb4719c95a9ba8cbf4a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105811417"
---
# <a name="ivmvirtualpceventsonvmstatechange-method"></a><span data-ttu-id="e4717-107">Método IVMVirtualPCEvents:: OnVMStateChange</span><span class="sxs-lookup"><span data-stu-id="e4717-107">IVMVirtualPCEvents::OnVMStateChange method</span></span>

<span data-ttu-id="e4717-108">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e4717-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e4717-109">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e4717-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e4717-110">Recebe a notificação de que o estado de uma máquina virtual foi alterado.</span><span class="sxs-lookup"><span data-stu-id="e4717-110">Receives notification that a virtual machine's state has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4717-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4717-111">Syntax</span></span>


```C++
HRESULT OnVMStateChange(
  [in] BSTR      virtualMachineConfig,
  [in] VMVMState virtualMachineState
);
```



## <a name="parameters"></a><span data-ttu-id="e4717-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4717-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4717-113">*virtualMachineConfig* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e4717-113">*virtualMachineConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4717-114">O nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e4717-114">The name of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="e4717-115">*virtualMachineState* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e4717-115">*virtualMachineState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4717-116">O novo estado da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e4717-116">The new state of the virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4717-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e4717-117">Return value</span></span>

<span data-ttu-id="e4717-118">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e4717-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e4717-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e4717-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4717-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4717-120">Remarks</span></span>

<span data-ttu-id="e4717-121">O programa cliente deve implementar esse método de interface para receber a notificação do evento **vmVirtualPCEvent \_ VMStateChanged** originado do [**IVMVirtualPC**](ivmvirtualpc.md).</span><span class="sxs-lookup"><span data-stu-id="e4717-121">The client program must implement this interface method to receive notification of the **vmVirtualPCEvent\_VMStateChanged** event originating from [**IVMVirtualPC**](ivmvirtualpc.md).</span></span> <span data-ttu-id="e4717-122">Para monitorar uma máquina virtual específica, use o método [**IVMVirtualMachineEvents:: OnStateChange**](ivmvirtualmachineevents-onstatechange.md) .</span><span class="sxs-lookup"><span data-stu-id="e4717-122">To monitor a specific virtual machine, use the [**IVMVirtualMachineEvents::OnStateChange**](ivmvirtualmachineevents-onstatechange.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4717-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4717-123">Requirements</span></span>



| <span data-ttu-id="e4717-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4717-124">Requirement</span></span> | <span data-ttu-id="e4717-125">Valor</span><span class="sxs-lookup"><span data-stu-id="e4717-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4717-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4717-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e4717-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e4717-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e4717-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4717-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e4717-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e4717-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e4717-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="e4717-130">End of client support</span></span><br/>    | <span data-ttu-id="e4717-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e4717-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e4717-132">Produto</span><span class="sxs-lookup"><span data-stu-id="e4717-132">Product</span></span><br/>                  | <span data-ttu-id="e4717-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e4717-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e4717-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e4717-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4717-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4717-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e4717-136">IID</span><span class="sxs-lookup"><span data-stu-id="e4717-136">IID</span></span><br/>                      | <span data-ttu-id="e4717-137">DIID \_ IVMVirtualPCEvents é definido como efed1ef1-3c09-41F7-a9c2-7e29fa286c9d</span><span class="sxs-lookup"><span data-stu-id="e4717-137">DIID\_IVMVirtualPCEvents is defined as efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="e4717-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4717-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4717-139">**IVMVirtualPCEvents**</span><span class="sxs-lookup"><span data-stu-id="e4717-139">**IVMVirtualPCEvents**</span></span>](ivmvirtualpcevents.md)
</dt> </dl>

 

