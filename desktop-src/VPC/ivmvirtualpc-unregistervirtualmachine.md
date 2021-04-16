---
title: Método IVMVirtualPC UnregisterVirtualMachine (VPCCOMInterfaces. h)
description: Cancela o registro de uma configuração de VM sem excluir o arquivo de configuração.
ms.assetid: 82ca6ef3-e9e5-471e-b2dc-0ff689a618d9
keywords:
- UnregisterVirtualMachine do método virtual PC
- Método UnregisterVirtualMachine Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, método UnregisterVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.UnregisterVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d74380a822253918791b78bc34ac1c796f595ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455905"
---
# <a name="ivmvirtualpcunregistervirtualmachine-method"></a><span data-ttu-id="e4b72-106">Método IVMVirtualPC:: UnregisterVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e4b72-106">IVMVirtualPC::UnregisterVirtualMachine method</span></span>

<span data-ttu-id="e4b72-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e4b72-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e4b72-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e4b72-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e4b72-109">Cancela o registro de uma configuração de VM (máquina virtual) sem excluir o arquivo de configuração.</span><span class="sxs-lookup"><span data-stu-id="e4b72-109">Unregisters a virtual machine (VM) configuration without deleting the configuration file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4b72-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4b72-110">Syntax</span></span>


```C++
HRESULT UnregisterVirtualMachine(
  [in] IVMVirtualMachine *virtualMachine
);
```



## <a name="parameters"></a><span data-ttu-id="e4b72-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4b72-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4b72-112">*VirtualMachine* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e4b72-112">*virtualMachine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4b72-113">Um ponteiro para um objeto [**IVMVirtualMachine**](ivmvirtualmachine.md) que representa a configuração de VM a ser cancelada.</span><span class="sxs-lookup"><span data-stu-id="e4b72-113">A pointer to an [**IVMVirtualMachine**](ivmvirtualmachine.md) object that represents the VM configuration to be unregistered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4b72-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e4b72-114">Return value</span></span>

<span data-ttu-id="e4b72-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="e4b72-115">This method can return one of these values.</span></span>



| <span data-ttu-id="e4b72-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e4b72-116">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="e4b72-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="e4b72-117">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e4b72-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e4b72-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="e4b72-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e4b72-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="e4b72-120"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="e4b72-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="e4b72-121">O parâmetro *VirtualMachine* era **nulo**.</span><span class="sxs-lookup"><span data-stu-id="e4b72-121">The *virtualMachine* parameter was **NULL**.</span></span><br/>                                         |
| <dl> <span data-ttu-id="e4b72-122"><dt>**VM \_ E \_ VM \_ executando**</dt> <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="e4b72-122"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>                        | <span data-ttu-id="e4b72-123">A VM está em execução.</span><span class="sxs-lookup"><span data-stu-id="e4b72-123">The VM is running.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="e4b72-124"><dt>**VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e4b72-124"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="e4b72-125">O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).</span><span class="sxs-lookup"><span data-stu-id="e4b72-125">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |
| <dl> <span data-ttu-id="e4b72-126"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="e4b72-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="e4b72-127">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="e4b72-127">An unexpected error has occurred.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="e4b72-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4b72-128">Remarks</span></span>

<span data-ttu-id="e4b72-129">Somente VMs interrompidas podem ter o registro cancelado.</span><span class="sxs-lookup"><span data-stu-id="e4b72-129">Only stopped VMs can be unregistered.</span></span> <span data-ttu-id="e4b72-130">O estado salvo existente ou os dados da unidade de desfazer para essa configuração serão mantidos quando uma VM tiver o registro cancelado.</span><span class="sxs-lookup"><span data-stu-id="e4b72-130">Existing saved state or undo drive data for this configuration will be retained when a VM is unregistered.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4b72-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4b72-131">Requirements</span></span>



| <span data-ttu-id="e4b72-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4b72-132">Requirement</span></span> | <span data-ttu-id="e4b72-133">Valor</span><span class="sxs-lookup"><span data-stu-id="e4b72-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4b72-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4b72-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e4b72-135">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e4b72-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e4b72-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4b72-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e4b72-137">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e4b72-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e4b72-138">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="e4b72-138">End of client support</span></span><br/>    | <span data-ttu-id="e4b72-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e4b72-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e4b72-140">Produto</span><span class="sxs-lookup"><span data-stu-id="e4b72-140">Product</span></span><br/>                  | <span data-ttu-id="e4b72-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e4b72-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e4b72-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e4b72-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4b72-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4b72-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e4b72-144">IID</span><span class="sxs-lookup"><span data-stu-id="e4b72-144">IID</span></span><br/>                      | <span data-ttu-id="e4b72-145">IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="e4b72-145">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="e4b72-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4b72-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4b72-147">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="e4b72-147">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

