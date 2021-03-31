---
title: Método IVMVirtualMachine Startup2 (VPCCOMInterfaces. h)
description: Inicia a máquina virtual no estado não inicializado ou salvo, com opções avançadas.
ms.assetid: c2679ea1-bbd5-42dc-9326-2019ad99554c
keywords:
- Startup2 do método virtual PC
- Método Startup2 Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, método Startup2
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Startup2
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51b40149b0b21abc126261d8b1ddec34b9948371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369657"
---
# <a name="ivmvirtualmachinestartup2-method"></a><span data-ttu-id="b7c76-106">Método IVMVirtualMachine:: Startup2</span><span class="sxs-lookup"><span data-stu-id="b7c76-106">IVMVirtualMachine::Startup2 method</span></span>

<span data-ttu-id="b7c76-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b7c76-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b7c76-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b7c76-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b7c76-109">Inicia a VM (máquina virtual) a partir do estado não inicializado ou salvo, com opções avançadas.</span><span class="sxs-lookup"><span data-stu-id="b7c76-109">Starts the virtual machine (VM) from either the uninitialized or saved state, with advanced options.</span></span>

<span data-ttu-id="b7c76-110">Esse método fornece um mecanismo para iniciar uma VM com um disco diferencial, mesmo que o carimbo de data/hora do disco pai tenha sido alterado.</span><span class="sxs-lookup"><span data-stu-id="b7c76-110">This method provides a mechanism to start a VM with a differencing disk even if the parent disk's timestamp has been changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7c76-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7c76-111">Syntax</span></span>


```C++
HRESULT Startup2(
  [in]          VMStartupOption startupOption,
  [out, retval] IVMTask         **startupTask
);
```



## <a name="parameters"></a><span data-ttu-id="b7c76-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7c76-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7c76-113">*startupOption* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b7c76-113">*startupOption* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7c76-114">A opção de inicialização avançada.</span><span class="sxs-lookup"><span data-stu-id="b7c76-114">The advanced startup option.</span></span> <span data-ttu-id="b7c76-115">Os valores possíveis são da enumeração [**VMStartupOption**](vmstartupoption.md) .</span><span class="sxs-lookup"><span data-stu-id="b7c76-115">The possible values are from the [**VMStartupOption**](vmstartupoption.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="b7c76-116">*startupTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="b7c76-116">*startupTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="b7c76-117">Um objeto [**IVMTask**](ivmtask.md) que é usado para acompanhar o progresso da conclusão da sequência inicial.</span><span class="sxs-lookup"><span data-stu-id="b7c76-117">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the start sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7c76-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b7c76-118">Return value</span></span>

<span data-ttu-id="b7c76-119">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="b7c76-119">This method can return one of these values.</span></span>



| <span data-ttu-id="b7c76-120">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b7c76-120">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="b7c76-121">Description</span><span class="sxs-lookup"><span data-stu-id="b7c76-121">Description</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b7c76-122"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b7c76-122"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="b7c76-123">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b7c76-123">The operation was successful.</span></span><br/>                                     |
| <dl> <span data-ttu-id="b7c76-124"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="b7c76-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                               | <span data-ttu-id="b7c76-125">O parâmetro *startupOption* não é válido.</span><span class="sxs-lookup"><span data-stu-id="b7c76-125">The *startupOption* parameter is not valid.</span></span><br/>                       |
| <dl> <span data-ttu-id="b7c76-126"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="b7c76-126"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="b7c76-127">O parâmetro *startupTask* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b7c76-127">The *startupTask* parameter is **NULL**.</span></span><br/>                          |
| <dl> <span data-ttu-id="b7c76-128"><dt>**HRESULT \_ DO \_ Win32 (erro de \_ acesso \_ negado)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="b7c76-128"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="b7c76-129">O chamador deve ter permissões de acesso de execução para iniciar esta VM.</span><span class="sxs-lookup"><span data-stu-id="b7c76-129">The caller must have execute access permissions to start this VM.</span></span><br/> |
| <dl> <span data-ttu-id="b7c76-130"><dt>**VM \_ E \_ atingiu o tempo \_ limite**</dt> de <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="b7c76-130"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="b7c76-131">A operação não foi concluída oportunamente.</span><span class="sxs-lookup"><span data-stu-id="b7c76-131">The operation did not complete in a timely manner.</span></span><br/>                |
| <dl> <span data-ttu-id="b7c76-132"><dt>**VM \_ E \_ 0xA0040203 \_ de \_ recurso**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b7c76-132"><dt>**VM\_E\_OUT\_OF\_RESOURCE**</dt> <dt>0xA0040203</dt></span></span> </dl>                    | <span data-ttu-id="b7c76-133">Não há recursos de host suficientes.</span><span class="sxs-lookup"><span data-stu-id="b7c76-133">There are not enough host resources.</span></span><br/>                              |
| <dl> <span data-ttu-id="b7c76-134"><dt>**VM \_ E \_ \_ muitas \_ VMs**</dt> <dt>0xA0040204</dt></span><span class="sxs-lookup"><span data-stu-id="b7c76-134"><dt>**VM\_E\_TOO\_MANY\_VMS**</dt> <dt>0xA0040204</dt></span></span> </dl>                       | <span data-ttu-id="b7c76-135">Há muitas VMs ativas.</span><span class="sxs-lookup"><span data-stu-id="b7c76-135">There are too many active VMs.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b7c76-136"><dt>**VM \_ E \_ VM \_ executando**</dt> <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="b7c76-136"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>                          | <span data-ttu-id="b7c76-137">A VM já está em execução.</span><span class="sxs-lookup"><span data-stu-id="b7c76-137">The VM is already running.</span></span><br/>                                        |
| <dl> <span data-ttu-id="b7c76-138"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="b7c76-138"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="b7c76-139">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="b7c76-139">An unexpected error has occurred.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="b7c76-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7c76-140">Remarks</span></span>

<span data-ttu-id="b7c76-141">Os valores a seguir podem ser retornados por meio da propriedade [**Error**](ivmtask-error.md) do objeto [**IVMTask**](ivmtask.md) retornado.</span><span class="sxs-lookup"><span data-stu-id="b7c76-141">The following values can be returned through the [**Error**](ivmtask-error.md) property of the returned [**IVMTask**](ivmtask.md) object.</span></span>



| <span data-ttu-id="b7c76-142">Código/valor do [**erro**](ivmtask-error.md)</span><span class="sxs-lookup"><span data-stu-id="b7c76-142">[**Error**](ivmtask-error.md) code/Value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="b7c76-143">Description</span><span class="sxs-lookup"><span data-stu-id="b7c76-143">Description</span></span>                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="b7c76-144"><span id="VM_E_UNSUPPORTED_HARDWARE__0xA0040950_"></span><span id="vm_e_unsupported_hardware__0xa0040950_"></span><span id="VM_E_UNSUPPORTED_HARDWARE__0XA0040950_"></span>`VM_E_UNSUPPORTED_HARDWARE` (0xA0040950)</span><span class="sxs-lookup"><span data-stu-id="b7c76-144"><span id="VM_E_UNSUPPORTED_HARDWARE__0xA0040950_"></span><span id="vm_e_unsupported_hardware__0xa0040950_"></span><span id="VM_E_UNSUPPORTED_HARDWARE__0XA0040950_"></span>`VM_E_UNSUPPORTED_HARDWARE` (0xA0040950)</span></span><br/>                                                 | <span data-ttu-id="b7c76-145">O hardware não oferece suporte à virtualização.</span><span class="sxs-lookup"><span data-stu-id="b7c76-145">The hardware does not support virtualization.</span></span><br/>              |
| <span data-ttu-id="b7c76-146"><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0xA0040951_"></span><span id="vm_e_hardware_virtualization_disabled__0xa0040951_"></span><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0XA0040951_"></span>`VM_E_HARDWARE_VIRTUALIZATION_DISABLED` (0xA0040951)</span><span class="sxs-lookup"><span data-stu-id="b7c76-146"><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0xA0040951_"></span><span id="vm_e_hardware_virtualization_disabled__0xa0040951_"></span><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0XA0040951_"></span>`VM_E_HARDWARE_VIRTUALIZATION_DISABLED` (0xA0040951)</span></span><br/> | <span data-ttu-id="b7c76-147">A virtualização de hardware está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="b7c76-147">Hardware virtualization is disabled.</span></span><br/>                       |
| <span data-ttu-id="b7c76-148"><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0xA0040952_"></span><span id="vm_e_vmvirtualpc_older_version__0xa0040952_"></span><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0XA0040952_"></span>`VM_E_VMVIRTUALPC_OLDER_VERSION` (0xA0040952)</span><span class="sxs-lookup"><span data-stu-id="b7c76-148"><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0xA0040952_"></span><span id="vm_e_vmvirtualpc_older_version__0xa0040952_"></span><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0XA0040952_"></span>`VM_E_VMVIRTUALPC_OLDER_VERSION` (0xA0040952)</span></span><br/>                             | <span data-ttu-id="b7c76-149">O Virtual PC 2007 e o Windows Virtual PC estão instalados.</span><span class="sxs-lookup"><span data-stu-id="b7c76-149">Both Virtual PC 2007 and Windows Virtual PC are installed.</span></span><br/> |
| <span data-ttu-id="b7c76-150"><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0xA0040953_"></span><span id="vm_e_other_virtualization_software__0xa0040953_"></span><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0XA0040953_"></span>`VM_E_OTHER_VIRTUALIZATION_SOFTWARE` (0xA0040953)</span><span class="sxs-lookup"><span data-stu-id="b7c76-150"><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0xA0040953_"></span><span id="vm_e_other_virtualization_software__0xa0040953_"></span><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0XA0040953_"></span>`VM_E_OTHER_VIRTUALIZATION_SOFTWARE` (0xA0040953)</span></span><br/>             | <span data-ttu-id="b7c76-151">Outros softwares de virtualização estão instalados.</span><span class="sxs-lookup"><span data-stu-id="b7c76-151">Other virtualization software is installed.</span></span><br/>                |
| <span data-ttu-id="b7c76-152"><span id="VM_E_OUT_OF_RESOURCE__0xa00400203_"></span><span id="vm_e_out_of_resource__0xa00400203_"></span><span id="VM_E_OUT_OF_RESOURCE__0XA00400203_"></span>`VM_E_OUT_OF_RESOURCE` (0xa00400203)</span><span class="sxs-lookup"><span data-stu-id="b7c76-152"><span id="VM_E_OUT_OF_RESOURCE__0xa00400203_"></span><span id="vm_e_out_of_resource__0xa00400203_"></span><span id="VM_E_OUT_OF_RESOURCE__0XA00400203_"></span>`VM_E_OUT_OF_RESOURCE` (0xa00400203)</span></span><br/>                                                                 | <span data-ttu-id="b7c76-153">Não há recursos de host suficientes.</span><span class="sxs-lookup"><span data-stu-id="b7c76-153">There are not enough host resources.</span></span><br/>                       |



 

## <a name="requirements"></a><span data-ttu-id="b7c76-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7c76-154">Requirements</span></span>



| <span data-ttu-id="b7c76-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7c76-155">Requirement</span></span> | <span data-ttu-id="b7c76-156">Valor</span><span class="sxs-lookup"><span data-stu-id="b7c76-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7c76-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7c76-157">Minimum supported client</span></span><br/> | <span data-ttu-id="b7c76-158">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b7c76-158">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b7c76-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7c76-159">Minimum supported server</span></span><br/> | <span data-ttu-id="b7c76-160">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b7c76-160">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b7c76-161">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="b7c76-161">End of client support</span></span><br/>    | <span data-ttu-id="b7c76-162">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b7c76-162">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b7c76-163">Produto</span><span class="sxs-lookup"><span data-stu-id="b7c76-163">Product</span></span><br/>                  | <span data-ttu-id="b7c76-164">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b7c76-164">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b7c76-165">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b7c76-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7c76-166"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7c76-166"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b7c76-167">IID</span><span class="sxs-lookup"><span data-stu-id="b7c76-167">IID</span></span><br/>                      | <span data-ttu-id="b7c76-168">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="b7c76-168">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="b7c76-169">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b7c76-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7c76-170">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="b7c76-170">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

