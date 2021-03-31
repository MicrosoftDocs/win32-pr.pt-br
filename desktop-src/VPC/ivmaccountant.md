---
title: Interface IVMAccountant (VPCCOMInterfaces. h)
description: Fornece acesso a informações relacionadas à contabilidade para uma máquina virtual.
ms.assetid: 047fa4c9-cb2e-4830-bab8-0513247eff9b
keywords:
- Virtual PC de interface IVMAccountant
- Virtual PC de interface IVMAccountant, descrito
topic_type:
- apiref
api_name:
- IVMAccountant
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d207833b92794510789e66e31b10e94d70b319fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645143"
---
# <a name="ivmaccountant-interface"></a><span data-ttu-id="6cb3c-105">Interface IVMAccountant</span><span class="sxs-lookup"><span data-stu-id="6cb3c-105">IVMAccountant interface</span></span>

<span data-ttu-id="6cb3c-106">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6cb3c-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6cb3c-107">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6cb3c-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6cb3c-108">Fornece acesso a informações relacionadas à contabilidade para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6cb3c-108">Provides access to accounting-related information for a virtual machine.</span></span> <span data-ttu-id="6cb3c-109">Para recuperar o **IVMAccountant** de uma máquina virtual, use a propriedade [**IVMVirtualMachine:: contador**](ivmvirtualmachine-accountant.md) .</span><span class="sxs-lookup"><span data-stu-id="6cb3c-109">To retrieve the **IVMAccountant** for a virtual machine, use the [**IVMVirtualMachine::Accountant**](ivmvirtualmachine-accountant.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="6cb3c-110">Membros</span><span class="sxs-lookup"><span data-stu-id="6cb3c-110">Members</span></span>

<span data-ttu-id="6cb3c-111">A interface **IVMAccountant** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="6cb3c-111">The **IVMAccountant** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="6cb3c-112">**IVMAccountant** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6cb3c-112">**IVMAccountant** also has these types of members:</span></span>

-   [<span data-ttu-id="6cb3c-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6cb3c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6cb3c-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6cb3c-114">Properties</span></span>

<span data-ttu-id="6cb3c-115">A interface **IVMAccountant** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6cb3c-115">The **IVMAccountant** interface has these properties.</span></span>



| <span data-ttu-id="6cb3c-116">Propriedade</span><span class="sxs-lookup"><span data-stu-id="6cb3c-116">Property</span></span>                                                                        | <span data-ttu-id="6cb3c-117">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="6cb3c-117">Access type</span></span>          | <span data-ttu-id="6cb3c-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="6cb3c-118">Description</span></span>                                                                                             |
|:--------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6cb3c-119">**CPUUtilization**</span><span class="sxs-lookup"><span data-stu-id="6cb3c-119">**CPUUtilization**</span></span>](ivmaccountant-cpuutilization.md)<br/>               | <span data-ttu-id="6cb3c-120">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6cb3c-120">Read-only</span></span><br/> | <span data-ttu-id="6cb3c-121">A porcentagem de utilização da CPU atual para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6cb3c-121">The percentage of current CPU utilization for this virtual machine.</span></span><br/>                          |
| [<span data-ttu-id="6cb3c-122">**CPUUtilizationHistory**</span><span class="sxs-lookup"><span data-stu-id="6cb3c-122">**CPUUtilizationHistory**</span></span>](ivmaccountant-cpuutilizationhistory.md)<br/> | <span data-ttu-id="6cb3c-123">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6cb3c-123">Read-only</span></span><br/> | <span data-ttu-id="6cb3c-124">A utilização de CPU recente desta máquina virtual (como uma matriz de valores percentuais).</span><span class="sxs-lookup"><span data-stu-id="6cb3c-124">The recent CPU utilization of this virtual machine (as an array of percentage values).</span></span><br/>       |
| [<span data-ttu-id="6cb3c-125">**DiskBytesRead**</span><span class="sxs-lookup"><span data-stu-id="6cb3c-125">**DiskBytesRead**</span></span>](ivmaccountant-diskbytesread.md)<br/>                 | <span data-ttu-id="6cb3c-126">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6cb3c-126">Read-only</span></span><br/> | <span data-ttu-id="6cb3c-127">O número total de bytes lidos por todos os controladores de armazenamento para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6cb3c-127">The total number of bytes read by all storage controllers for this virtual machine.</span></span><br/>          |
| [<span data-ttu-id="6cb3c-128">**DiskBytesWritten**</span><span class="sxs-lookup"><span data-stu-id="6cb3c-128">**DiskBytesWritten**</span></span>](ivmaccountant-diskbyteswritten.md)<br/>           | <span data-ttu-id="6cb3c-129">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6cb3c-129">Read-only</span></span><br/> | <span data-ttu-id="6cb3c-130">O número total de bytes gravados por todos os controladores de armazenamento para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6cb3c-130">The total number of bytes written by all storage controllers for this virtual machine.</span></span><br/>       |
| [<span data-ttu-id="6cb3c-131">**NetworkBytesReceived**</span><span class="sxs-lookup"><span data-stu-id="6cb3c-131">**NetworkBytesReceived**</span></span>](ivmaccountant-networkbytesreceived.md)<br/>   | <span data-ttu-id="6cb3c-132">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6cb3c-132">Read-only</span></span><br/> | <span data-ttu-id="6cb3c-133">O número total de bytes recebidos por todos os adaptadores de rede virtual para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6cb3c-133">The total number of bytes received by all virtual network adapters for this virtual machine.</span></span><br/> |
| [<span data-ttu-id="6cb3c-134">**NetworkBytesSent**</span><span class="sxs-lookup"><span data-stu-id="6cb3c-134">**NetworkBytesSent**</span></span>](ivmaccountant-networkbytessent.md)<br/>           | <span data-ttu-id="6cb3c-135">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6cb3c-135">Read-only</span></span><br/> | <span data-ttu-id="6cb3c-136">O número total de bytes enviados por todos os adaptadores de rede virtual para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6cb3c-136">The total number of bytes sent by all virtual network adapters for this virtual machine.</span></span><br/>     |
| [<span data-ttu-id="6cb3c-137">**Atividade**</span><span class="sxs-lookup"><span data-stu-id="6cb3c-137">**UpTime**</span></span>](ivmaccountant-uptime.md)<br/>                               | <span data-ttu-id="6cb3c-138">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6cb3c-138">Read-only</span></span><br/> | <span data-ttu-id="6cb3c-139">O número de segundos em que a máquina virtual está em execução.</span><span class="sxs-lookup"><span data-stu-id="6cb3c-139">The number of seconds that the virtual machine has been running.</span></span><br/>                             |



 

## <a name="requirements"></a><span data-ttu-id="6cb3c-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6cb3c-140">Requirements</span></span>



| <span data-ttu-id="6cb3c-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cb3c-141">Requirement</span></span> | <span data-ttu-id="6cb3c-142">Valor</span><span class="sxs-lookup"><span data-stu-id="6cb3c-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cb3c-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6cb3c-143">Minimum supported client</span></span><br/> | <span data-ttu-id="6cb3c-144">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6cb3c-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6cb3c-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6cb3c-145">Minimum supported server</span></span><br/> | <span data-ttu-id="6cb3c-146">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6cb3c-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6cb3c-147">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="6cb3c-147">End of client support</span></span><br/>    | <span data-ttu-id="6cb3c-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6cb3c-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6cb3c-149">Produto</span><span class="sxs-lookup"><span data-stu-id="6cb3c-149">Product</span></span><br/>                  | <span data-ttu-id="6cb3c-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6cb3c-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6cb3c-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6cb3c-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cb3c-152"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cb3c-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6cb3c-153">IID</span><span class="sxs-lookup"><span data-stu-id="6cb3c-153">IID</span></span><br/>                      | <span data-ttu-id="6cb3c-154">IID \_ IVMAccountant é definido como 6376c067-7f57-4D63-b754-06e2e4f51d73</span><span class="sxs-lookup"><span data-stu-id="6cb3c-154">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



 

