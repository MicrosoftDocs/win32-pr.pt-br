---
title: Método IVMVirtualMachineEvents OnAdditionsAvailable (VPCCOMInterfaces. h)
description: Recebe a notificação de que os componentes de integração estão disponíveis em uma máquina virtual.
ms.assetid: c940104b-4d34-47c2-bf48-9024a7f86c46
keywords:
- OnAdditionsAvailable do método virtual PC
- Método OnAdditionsAvailable Virtual PC, interface IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface virtual PC, método OnAdditionsAvailable
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnAdditionsAvailable
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 193b44f533079bc957cbb8b297409641814b6e21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455798"
---
# <a name="ivmvirtualmachineeventsonadditionsavailable-method"></a><span data-ttu-id="5aa23-106">Método IVMVirtualMachineEvents:: OnAdditionsAvailable</span><span class="sxs-lookup"><span data-stu-id="5aa23-106">IVMVirtualMachineEvents::OnAdditionsAvailable method</span></span>

<span data-ttu-id="5aa23-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5aa23-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5aa23-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="5aa23-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5aa23-109">Recebe a notificação de que os componentes de integração estão disponíveis em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5aa23-109">Receives notification that integration components are available in a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="5aa23-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5aa23-110">Syntax</span></span>


```C++
HRESULT OnAdditionsAvailable();
```



## <a name="parameters"></a><span data-ttu-id="5aa23-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5aa23-111">Parameters</span></span>

<span data-ttu-id="5aa23-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5aa23-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5aa23-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5aa23-113">Return value</span></span>

<span data-ttu-id="5aa23-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5aa23-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5aa23-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5aa23-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5aa23-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5aa23-116">Requirements</span></span>



| <span data-ttu-id="5aa23-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5aa23-117">Requirement</span></span> | <span data-ttu-id="5aa23-118">Valor</span><span class="sxs-lookup"><span data-stu-id="5aa23-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5aa23-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5aa23-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5aa23-120">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5aa23-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5aa23-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5aa23-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5aa23-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5aa23-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5aa23-123">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="5aa23-123">End of client support</span></span><br/>    | <span data-ttu-id="5aa23-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5aa23-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5aa23-125">Produto</span><span class="sxs-lookup"><span data-stu-id="5aa23-125">Product</span></span><br/>                  | <span data-ttu-id="5aa23-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5aa23-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5aa23-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5aa23-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5aa23-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="5aa23-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="5aa23-129">IID</span><span class="sxs-lookup"><span data-stu-id="5aa23-129">IID</span></span><br/>                      | <span data-ttu-id="5aa23-130">DIID \_ IVMVirtualMachineEvents é definido como 9d84f560-bb67-4961-BD12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="5aa23-130">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="5aa23-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="5aa23-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aa23-132">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="5aa23-132">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

