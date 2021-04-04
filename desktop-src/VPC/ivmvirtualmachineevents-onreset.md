---
title: Método OnReset do IVMVirtualMachineEvents (VPCCOMInterfaces. h)
description: Recebe a notificação de que uma máquina virtual foi redefinida.
ms.assetid: 10a66aea-9a8f-4663-8eb6-cc35f361e43f
keywords:
- Método OnReset Virtual PC
- Método OnReset Virtual PC, interface IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface virtual PC, método OnReset
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnReset
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6345d0e925777fbecf42247b3e3064b9f993c7c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917948"
---
# <a name="ivmvirtualmachineeventsonreset-method"></a><span data-ttu-id="1e708-106">Método IVMVirtualMachineEvents:: OnReset</span><span class="sxs-lookup"><span data-stu-id="1e708-106">IVMVirtualMachineEvents::OnReset method</span></span>

<span data-ttu-id="1e708-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1e708-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1e708-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1e708-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1e708-109">Recebe a notificação de que uma máquina virtual foi redefinida.</span><span class="sxs-lookup"><span data-stu-id="1e708-109">Receives notification that a virtual machine has been reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e708-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1e708-110">Syntax</span></span>


```C++
HRESULT OnReset();
```



## <a name="parameters"></a><span data-ttu-id="1e708-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1e708-111">Parameters</span></span>

<span data-ttu-id="1e708-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="1e708-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1e708-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1e708-113">Return value</span></span>

<span data-ttu-id="1e708-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1e708-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1e708-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1e708-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e708-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="1e708-116">Remarks</span></span>

<span data-ttu-id="1e708-117">Esse método é chamado quando a máquina virtual é redefinida.</span><span class="sxs-lookup"><span data-stu-id="1e708-117">This method is called when the virtual machine has been reset.</span></span> <span data-ttu-id="1e708-118">O programa cliente deve implementar esse método de interface para receber a notificação do \_ evento de redefinição de vmVirtualMachineEvent originado de [**IVMVirtualMachine**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="1e708-118">The client program must implement this interface method to receive notification of the vmVirtualMachineEvent\_Reset event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1e708-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e708-119">Requirements</span></span>



| <span data-ttu-id="1e708-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e708-120">Requirement</span></span> | <span data-ttu-id="1e708-121">Valor</span><span class="sxs-lookup"><span data-stu-id="1e708-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e708-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e708-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1e708-123">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="1e708-123">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1e708-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e708-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1e708-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1e708-125">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1e708-126">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="1e708-126">End of client support</span></span><br/>    | <span data-ttu-id="1e708-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e708-127">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1e708-128">Produto</span><span class="sxs-lookup"><span data-stu-id="1e708-128">Product</span></span><br/>                  | <span data-ttu-id="1e708-129">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1e708-129">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1e708-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1e708-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e708-131"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e708-131"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1e708-132">IID</span><span class="sxs-lookup"><span data-stu-id="1e708-132">IID</span></span><br/>                      | <span data-ttu-id="1e708-133">DIID \_ IVMVirtualMachineEvents é definido como 9d84f560-bb67-4961-BD12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="1e708-133">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="1e708-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e708-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e708-135">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="1e708-135">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

