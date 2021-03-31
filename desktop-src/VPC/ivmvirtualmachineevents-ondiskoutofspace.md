---
title: Método IVMVirtualMachineEvents OnDiskOutOfSpace (VPCCOMInterfaces. h)
description: Recebe uma notificação de que um disco necessário para uma VM está com pouco espaço livre.
ms.assetid: 1c431904-fffd-4513-8670-b9723f53edf1
keywords:
- OnDiskOutOfSpace do método virtual PC
- Método OnDiskOutOfSpace Virtual PC, interface IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface virtual PC, método OnDiskOutOfSpace
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnDiskOutOfSpace
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ac2d5f45068dc8cd7341d0a599b2da4e5c7655a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824139"
---
# <a name="ivmvirtualmachineeventsondiskoutofspace-method"></a><span data-ttu-id="73060-106">Método IVMVirtualMachineEvents:: OnDiskOutOfSpace</span><span class="sxs-lookup"><span data-stu-id="73060-106">IVMVirtualMachineEvents::OnDiskOutOfSpace method</span></span>

<span data-ttu-id="73060-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="73060-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="73060-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="73060-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="73060-109">Recebe a notificação de que um disco necessário para uma VM (máquina virtual) está com pouco espaço livre.</span><span class="sxs-lookup"><span data-stu-id="73060-109">Receives notification that a disk required for a virtual machine (VM) is low on free space.</span></span> <span data-ttu-id="73060-110">Se o espaço livre cair abaixo de 100 MB, esse evento será recebido como um aviso e, se o espaço livre cair abaixo de 20 MB, esse evento será recebido novamente como um erro e a VM será pausada.</span><span class="sxs-lookup"><span data-stu-id="73060-110">If free space drops below 100 MB this event is received as a warning and if free space drops below 20 MB this event is received again as an error and the VM will be paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="73060-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73060-111">Syntax</span></span>


```C++
HRESULT OnDiskOutOfSpace(
  [in] VARIANT_BOOL criticallyLow
);
```



## <a name="parameters"></a><span data-ttu-id="73060-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73060-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73060-113">*criticallyLow* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="73060-113">*criticallyLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73060-114">Defina como **Variant \_ true** se o disco tiver menos de 20 MB livres e para a **variante \_ false** se o espaço livre for superior a 20 MB, mas menor que 100 MB.</span><span class="sxs-lookup"><span data-stu-id="73060-114">Set to **VARIANT\_TRUE** if the disk has less than 20 MB free and to **VARIANT\_FALSE** if the free space is more than 20 MB but less than 100 MB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73060-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="73060-115">Return value</span></span>

<span data-ttu-id="73060-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="73060-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="73060-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="73060-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="73060-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73060-118">Requirements</span></span>



| <span data-ttu-id="73060-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="73060-119">Requirement</span></span> | <span data-ttu-id="73060-120">Valor</span><span class="sxs-lookup"><span data-stu-id="73060-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="73060-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="73060-121">Minimum supported client</span></span><br/> | <span data-ttu-id="73060-122">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="73060-122">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="73060-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="73060-123">Minimum supported server</span></span><br/> | <span data-ttu-id="73060-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="73060-124">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="73060-125">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="73060-125">End of client support</span></span><br/>    | <span data-ttu-id="73060-126">Windows 7</span><span class="sxs-lookup"><span data-stu-id="73060-126">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="73060-127">Produto</span><span class="sxs-lookup"><span data-stu-id="73060-127">Product</span></span><br/>                  | <span data-ttu-id="73060-128">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="73060-128">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="73060-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="73060-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="73060-130"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="73060-130"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="73060-131">IID</span><span class="sxs-lookup"><span data-stu-id="73060-131">IID</span></span><br/>                      | <span data-ttu-id="73060-132">DIID \_ IVMVirtualMachineEvents é definido como 9d84f560-bb67-4961-BD12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="73060-132">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="73060-133">Consulte também</span><span class="sxs-lookup"><span data-stu-id="73060-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73060-134">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="73060-134">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

