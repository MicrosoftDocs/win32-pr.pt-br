---
title: Método IVMVirtualMachineEvents OnStateChange (VPCCOMInterfaces. h)
description: Recebe a notificação de que o estado de uma máquina virtual foi alterado. | Método IVMVirtualMachineEvents OnStateChange (VPCCOMInterfaces. h)
ms.assetid: 1737bb5e-078d-4ebe-9558-de083aae1baa
keywords:
- OnStateChange do método virtual PC
- Método OnStateChange Virtual PC, interface IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface virtual PC, método OnStateChange
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnStateChange
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7da112d8f6211882953056afef0219b9efdf9843
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298413"
---
# <a name="ivmvirtualmachineeventsonstatechange-method"></a><span data-ttu-id="63743-107">Método IVMVirtualMachineEvents:: OnStateChange</span><span class="sxs-lookup"><span data-stu-id="63743-107">IVMVirtualMachineEvents::OnStateChange method</span></span>

<span data-ttu-id="63743-108">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="63743-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="63743-109">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="63743-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="63743-110">Recebe a notificação de que o estado de uma máquina virtual foi alterado.</span><span class="sxs-lookup"><span data-stu-id="63743-110">Receives notification that a virtual machine's state has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="63743-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63743-111">Syntax</span></span>


```C++
HRESULT OnStateChange(
  [in] VMVMState virtualMachineState
);
```



## <a name="parameters"></a><span data-ttu-id="63743-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="63743-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63743-113">*virtualMachineState* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="63743-113">*virtualMachineState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63743-114">O novo estado da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="63743-114">The new state of the virtual machine.</span></span> <span data-ttu-id="63743-115">Para obter uma lista de valores, consulte [**VMVMState**](vmvmstate.md).</span><span class="sxs-lookup"><span data-stu-id="63743-115">For a list of values, see [**VMVMState**](vmvmstate.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63743-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="63743-116">Return value</span></span>

<span data-ttu-id="63743-117">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="63743-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="63743-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="63743-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="63743-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="63743-119">Remarks</span></span>

<span data-ttu-id="63743-120">Esse método é chamado quando o estado dessa máquina virtual é alterado.</span><span class="sxs-lookup"><span data-stu-id="63743-120">This method is called when the state for this virtual machine changes.</span></span> <span data-ttu-id="63743-121">O programa cliente deve implementar esse método de interface para receber a notificação do \_ evento vmVirtualMachineEvent StateChanged originado de [**IVMVirtualMachine**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="63743-121">The client program must implement this interface method to receive notification of the vmVirtualMachineEvent\_StateChanged event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="63743-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63743-122">Requirements</span></span>



| <span data-ttu-id="63743-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="63743-123">Requirement</span></span> | <span data-ttu-id="63743-124">Valor</span><span class="sxs-lookup"><span data-stu-id="63743-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="63743-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63743-125">Minimum supported client</span></span><br/> | <span data-ttu-id="63743-126">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="63743-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="63743-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63743-127">Minimum supported server</span></span><br/> | <span data-ttu-id="63743-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="63743-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="63743-129">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="63743-129">End of client support</span></span><br/>    | <span data-ttu-id="63743-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="63743-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="63743-131">Produto</span><span class="sxs-lookup"><span data-stu-id="63743-131">Product</span></span><br/>                  | <span data-ttu-id="63743-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="63743-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="63743-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="63743-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="63743-134"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="63743-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="63743-135">IID</span><span class="sxs-lookup"><span data-stu-id="63743-135">IID</span></span><br/>                      | <span data-ttu-id="63743-136">DIID \_ IVMVirtualMachineEvents é definido como 9d84f560-bb67-4961-BD12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="63743-136">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="63743-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="63743-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63743-138">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="63743-138">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

