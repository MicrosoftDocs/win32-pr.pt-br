---
title: Método IVMVirtualMachineEvents OnTripleFault (VPCCOMInterfaces. h)
description: Recebe uma notificação de que uma máquina virtual tem falha tripla.
ms.assetid: a17b1a05-3058-48ba-a196-7e9563f3e1c0
keywords:
- OnTripleFault do método virtual PC
- Método OnTripleFault Virtual PC, interface IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface virtual PC, método OnTripleFault
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnTripleFault
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48d635b9009ecadecb7aed4a921a9c609ef69505
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499636"
---
# <a name="ivmvirtualmachineeventsontriplefault-method"></a><span data-ttu-id="71e59-106">Método IVMVirtualMachineEvents:: OnTripleFault</span><span class="sxs-lookup"><span data-stu-id="71e59-106">IVMVirtualMachineEvents::OnTripleFault method</span></span>

<span data-ttu-id="71e59-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="71e59-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="71e59-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="71e59-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="71e59-109">Recebe uma notificação de que uma máquina virtual tem falha tripla.</span><span class="sxs-lookup"><span data-stu-id="71e59-109">Receives notification that a virtual machine has triple-faulted.</span></span>

## <a name="syntax"></a><span data-ttu-id="71e59-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="71e59-110">Syntax</span></span>


```C++
HRESULT OnTripleFault();
```



## <a name="parameters"></a><span data-ttu-id="71e59-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71e59-111">Parameters</span></span>

<span data-ttu-id="71e59-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="71e59-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="71e59-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="71e59-113">Return value</span></span>

<span data-ttu-id="71e59-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="71e59-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="71e59-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="71e59-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="71e59-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="71e59-116">Remarks</span></span>

<span data-ttu-id="71e59-117">Esse método é chamado quando uma máquina virtual tem uma falha tripla.</span><span class="sxs-lookup"><span data-stu-id="71e59-117">This method is called when a virtual machine has triple-faulted.</span></span> <span data-ttu-id="71e59-118">O programa cliente deve implementar esse método de interface para receber a notificação do \_ evento vmVirtualMachineEvent TripleFault originado do [**IVMVirtualMachine**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="71e59-118">The client program must implement this interface method to receive notification of the vmVirtualMachineEvent\_TripleFault event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="71e59-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71e59-119">Requirements</span></span>



| <span data-ttu-id="71e59-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="71e59-120">Requirement</span></span> | <span data-ttu-id="71e59-121">Valor</span><span class="sxs-lookup"><span data-stu-id="71e59-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="71e59-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71e59-122">Minimum supported client</span></span><br/> | <span data-ttu-id="71e59-123">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="71e59-123">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="71e59-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71e59-124">Minimum supported server</span></span><br/> | <span data-ttu-id="71e59-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="71e59-125">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="71e59-126">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="71e59-126">End of client support</span></span><br/>    | <span data-ttu-id="71e59-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="71e59-127">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="71e59-128">Produto</span><span class="sxs-lookup"><span data-stu-id="71e59-128">Product</span></span><br/>                  | <span data-ttu-id="71e59-129">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="71e59-129">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="71e59-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="71e59-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="71e59-131"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="71e59-131"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="71e59-132">IID</span><span class="sxs-lookup"><span data-stu-id="71e59-132">IID</span></span><br/>                      | <span data-ttu-id="71e59-133">DIID \_ IVMVirtualMachineEvents é definido como 9d84f560-bb67-4961-BD12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="71e59-133">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="71e59-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="71e59-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71e59-135">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="71e59-135">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

