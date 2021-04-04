---
title: Método onconfigurationchanged IVMVirtualMachineEvents (VPCCOMInterfaces. h)
description: Recebe uma notificação de que um valor na configuração para esta máquina virtual foi alterado.
ms.assetid: 1955f23e-b318-41aa-b82e-81283be81608
keywords:
- Método onconfigurationchanged Virtual PC
- Método onconfigurationchanged Virtual PC, interface IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface virtual PC, método onconfigurationchanged
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnConfigurationChanged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10459562da2d87b8c883217e003cd822ef923fad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917950"
---
# <a name="ivmvirtualmachineeventsonconfigurationchanged-method"></a><span data-ttu-id="bc12c-106">Método IVMVirtualMachineEvents:: onconfigurationchanged</span><span class="sxs-lookup"><span data-stu-id="bc12c-106">IVMVirtualMachineEvents::OnConfigurationChanged method</span></span>

<span data-ttu-id="bc12c-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bc12c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bc12c-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="bc12c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bc12c-109">Recebe uma notificação de que um valor na configuração para esta máquina virtual foi alterado.</span><span class="sxs-lookup"><span data-stu-id="bc12c-109">Receives notification that a value in the configuration for this virtual machine has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc12c-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bc12c-110">Syntax</span></span>


```C++
HRESULT OnConfigurationChanged(
  [in] BSTR    configKey,
  [in] VARIANT configData
);
```



## <a name="parameters"></a><span data-ttu-id="bc12c-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc12c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc12c-112">*configKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bc12c-112">*configKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc12c-113">O valor dentro da configuração que foi alterada.</span><span class="sxs-lookup"><span data-stu-id="bc12c-113">The value inside the configuration that has changed.</span></span>

</dd> <dt>

<span data-ttu-id="bc12c-114">*configData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bc12c-114">*configData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc12c-115">O novo valor para a configuração.</span><span class="sxs-lookup"><span data-stu-id="bc12c-115">The new value for the configuration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc12c-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bc12c-116">Return value</span></span>

<span data-ttu-id="bc12c-117">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bc12c-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bc12c-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bc12c-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc12c-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="bc12c-119">Remarks</span></span>

<span data-ttu-id="bc12c-120">Esse método é chamado quando a configuração é alterada para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="bc12c-120">This method is called when the configuration changes for this virtual machine.</span></span> <span data-ttu-id="bc12c-121">O programa cliente deve implementar esse método de interface para receber a notificação do \_ evento vmVirtualMachineEvent configurationchanged originado de [**IVMVirtualMachine**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="bc12c-121">The client program must implement this interface method to receive notification of the vmVirtualMachineEvent\_ConfigurationChanged event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc12c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc12c-122">Requirements</span></span>



| <span data-ttu-id="bc12c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc12c-123">Requirement</span></span> | <span data-ttu-id="bc12c-124">Valor</span><span class="sxs-lookup"><span data-stu-id="bc12c-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc12c-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc12c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="bc12c-126">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="bc12c-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bc12c-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc12c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="bc12c-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="bc12c-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bc12c-129">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="bc12c-129">End of client support</span></span><br/>    | <span data-ttu-id="bc12c-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bc12c-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bc12c-131">Produto</span><span class="sxs-lookup"><span data-stu-id="bc12c-131">Product</span></span><br/>                  | <span data-ttu-id="bc12c-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bc12c-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bc12c-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bc12c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc12c-134"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc12c-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="bc12c-135">IID</span><span class="sxs-lookup"><span data-stu-id="bc12c-135">IID</span></span><br/>                      | <span data-ttu-id="bc12c-136">DIID \_ IVMVirtualMachineEvents é definido como 9d84f560-bb67-4961-BD12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="bc12c-136">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="bc12c-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc12c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc12c-138">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="bc12c-138">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

