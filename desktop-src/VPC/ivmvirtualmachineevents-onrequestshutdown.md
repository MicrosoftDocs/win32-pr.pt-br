---
title: Método IVMVirtualMachineEvents OnRequestShutdown (VPCCOMInterfaces. h)
description: Recebe a notificação de que uma solicitação de desligamento foi feita.
ms.assetid: e04131fd-5ca7-4392-9725-ba62b905324a
keywords:
- OnRequestShutdown do método virtual PC
- Método OnRequestShutdown Virtual PC, interface IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface virtual PC, método OnRequestShutdown
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnRequestShutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94dce60a7dfdb5ed5dce714e8b8eafcbd9558b95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455375"
---
# <a name="ivmvirtualmachineeventsonrequestshutdown-method"></a><span data-ttu-id="02e5d-106">Método IVMVirtualMachineEvents:: OnRequestShutdown</span><span class="sxs-lookup"><span data-stu-id="02e5d-106">IVMVirtualMachineEvents::OnRequestShutdown method</span></span>

<span data-ttu-id="02e5d-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="02e5d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="02e5d-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="02e5d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="02e5d-109">Recebe a notificação de que uma solicitação de desligamento foi feita.</span><span class="sxs-lookup"><span data-stu-id="02e5d-109">Receives notification that a shutdown request has been made.</span></span>

## <a name="syntax"></a><span data-ttu-id="02e5d-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="02e5d-110">Syntax</span></span>


```C++
HRESULT OnRequestShutdown();
```



## <a name="parameters"></a><span data-ttu-id="02e5d-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="02e5d-111">Parameters</span></span>

<span data-ttu-id="02e5d-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="02e5d-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="02e5d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="02e5d-113">Return value</span></span>

<span data-ttu-id="02e5d-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="02e5d-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="02e5d-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="02e5d-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="02e5d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="02e5d-116">Remarks</span></span>

<span data-ttu-id="02e5d-117">Esse método é chamado sempre que a sessão da máquina virtual está prestes a ser desligada.</span><span class="sxs-lookup"><span data-stu-id="02e5d-117">This method is called whenever the virtual machine session is about to shut down.</span></span> <span data-ttu-id="02e5d-118">O programa cliente deve implementar esse método de interface para receber a notificação do evento **vmVirtualMachineEvent \_ RequestShutdown** originado do [**IVMVirtualMachine**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="02e5d-118">The client program must implement this interface method to receive notification of the **vmVirtualMachineEvent\_RequestShutdown** event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

<span data-ttu-id="02e5d-119">Essa notificação de evento é enviada somente quando a sessão de máquinas virtuais está prestes a ser desligada.</span><span class="sxs-lookup"><span data-stu-id="02e5d-119">This event notification is sent only when the virtual machines session is about to shut down.</span></span> <span data-ttu-id="02e5d-120">As rotinas de desligamento do sistema operacional, como [**IVMGuestOS:: Shutdown**](ivmguestos-shutdown.md), não acionam esse evento diretamente, a menos que eles também tentem realizar uma desligamento do software do hardware virtual.</span><span class="sxs-lookup"><span data-stu-id="02e5d-120">Operating system shutdown routines, such as [**IVMGuestOS::Shutdown**](ivmguestos-shutdown.md), do not fire this event directly unless they also attempt to perform a software power off of the virtual hardware.</span></span>

## <a name="requirements"></a><span data-ttu-id="02e5d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02e5d-121">Requirements</span></span>



| <span data-ttu-id="02e5d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="02e5d-122">Requirement</span></span> | <span data-ttu-id="02e5d-123">Valor</span><span class="sxs-lookup"><span data-stu-id="02e5d-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="02e5d-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02e5d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="02e5d-125">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="02e5d-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="02e5d-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02e5d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="02e5d-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="02e5d-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="02e5d-128">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="02e5d-128">End of client support</span></span><br/>    | <span data-ttu-id="02e5d-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="02e5d-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="02e5d-130">Produto</span><span class="sxs-lookup"><span data-stu-id="02e5d-130">Product</span></span><br/>                  | <span data-ttu-id="02e5d-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="02e5d-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="02e5d-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="02e5d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="02e5d-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="02e5d-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="02e5d-134">IID</span><span class="sxs-lookup"><span data-stu-id="02e5d-134">IID</span></span><br/>                      | <span data-ttu-id="02e5d-135">DIID \_ IVMVirtualMachineEvents é definido como 9d84f560-bb67-4961-BD12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="02e5d-135">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="02e5d-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="02e5d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02e5d-137">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="02e5d-137">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

