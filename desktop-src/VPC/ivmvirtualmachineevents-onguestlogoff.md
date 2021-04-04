---
title: Método IVMVirtualMachineEvents OnGuestLogoff (VPCCOMInterfaces. h)
description: Recebe a notificação de que um usuário fez logoff do sistema operacional convidado.
ms.assetid: 3771ba28-eea9-4c8b-9224-231b00d2f2f5
keywords:
- OnGuestLogoff do método virtual PC
- Método OnGuestLogoff Virtual PC, interface IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface virtual PC, método OnGuestLogoff
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnGuestLogoff
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ce5100c3901b3de32a769b6bae0e16fcffe26a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917949"
---
# <a name="ivmvirtualmachineeventsonguestlogoff-method"></a><span data-ttu-id="d3ed6-106">Método IVMVirtualMachineEvents:: OnGuestLogoff</span><span class="sxs-lookup"><span data-stu-id="d3ed6-106">IVMVirtualMachineEvents::OnGuestLogoff method</span></span>

<span data-ttu-id="d3ed6-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d3ed6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d3ed6-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d3ed6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d3ed6-109">Recebe a notificação de que um usuário fez logoff do sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="d3ed6-109">Receives notification that a user has logged off from the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3ed6-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d3ed6-110">Syntax</span></span>


```C++
HRESULT OnGuestLogoff(
  [in] VMLogoffType logoffType
);
```



## <a name="parameters"></a><span data-ttu-id="d3ed6-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d3ed6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3ed6-112">*logofftype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d3ed6-112">*logoffType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3ed6-113">Valor da enumeração [**VMLogoffType**](vmlogofftype.md) que descreve o tipo de logoff.</span><span class="sxs-lookup"><span data-stu-id="d3ed6-113">Value from the [**VMLogoffType**](vmlogofftype.md) enumeration that describes the type of logoff.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3ed6-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d3ed6-114">Return value</span></span>

<span data-ttu-id="d3ed6-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d3ed6-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d3ed6-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d3ed6-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3ed6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3ed6-117">Requirements</span></span>



| <span data-ttu-id="d3ed6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3ed6-118">Requirement</span></span> | <span data-ttu-id="d3ed6-119">Valor</span><span class="sxs-lookup"><span data-stu-id="d3ed6-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3ed6-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3ed6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d3ed6-121">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d3ed6-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d3ed6-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3ed6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d3ed6-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d3ed6-123">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d3ed6-124">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="d3ed6-124">End of client support</span></span><br/>    | <span data-ttu-id="d3ed6-125">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d3ed6-125">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d3ed6-126">Produto</span><span class="sxs-lookup"><span data-stu-id="d3ed6-126">Product</span></span><br/>                  | <span data-ttu-id="d3ed6-127">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d3ed6-127">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d3ed6-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d3ed6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3ed6-129"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3ed6-129"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d3ed6-130">IID</span><span class="sxs-lookup"><span data-stu-id="d3ed6-130">IID</span></span><br/>                      | <span data-ttu-id="d3ed6-131">DIID \_ IVMVirtualMachineEvents é definido como 9d84f560-bb67-4961-BD12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="d3ed6-131">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="d3ed6-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="d3ed6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3ed6-133">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="d3ed6-133">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> <dt>

[<span data-ttu-id="d3ed6-134">**VMLogoffType**</span><span class="sxs-lookup"><span data-stu-id="d3ed6-134">**VMLogoffType**</span></span>](vmlogofftype.md)
</dt> </dl>

 

