---
title: Método de inicialização IVMVirtualMachine (VPCCOMInterfaces. h)
description: Inicia a máquina virtual no estado não inicializado ou salvo.
ms.assetid: 82f9b6f1-99b1-4402-93f5-b4aa3520a505
keywords:
- Método de inicialização do PC virtual
- Método de inicialização, PC virtual, interface IVMVirtualMachine
- Virtual PC de interface IVMVirtualMachine, método de inicialização
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Startup
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a45e0952fc1a17fc6ba2ea639f2ee87f7b9ef2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918936"
---
# <a name="ivmvirtualmachinestartup-method"></a><span data-ttu-id="77e3f-106">Método IVMVirtualMachine:: Startup</span><span class="sxs-lookup"><span data-stu-id="77e3f-106">IVMVirtualMachine::Startup method</span></span>

<span data-ttu-id="77e3f-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="77e3f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="77e3f-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="77e3f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="77e3f-109">Inicia a máquina virtual no estado não inicializado ou salvo.</span><span class="sxs-lookup"><span data-stu-id="77e3f-109">Starts the virtual machine from either the uninitialized or saved state.</span></span>

## <a name="syntax"></a><span data-ttu-id="77e3f-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="77e3f-110">Syntax</span></span>


```C++
HRESULT Startup(
  [out, retval] IVMTask **startupTask
);
```



## <a name="parameters"></a><span data-ttu-id="77e3f-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77e3f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77e3f-112">*startupTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="77e3f-112">*startupTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="77e3f-113">Um objeto [**IVMTask**](ivmtask.md) que é usado para acompanhar o progresso de conclusão da sequência de inicialização da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="77e3f-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the virtual machine's startup sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77e3f-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="77e3f-114">Return value</span></span>

<span data-ttu-id="77e3f-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="77e3f-115">This method can return one of these values.</span></span>



| <span data-ttu-id="77e3f-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="77e3f-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="77e3f-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="77e3f-117">Description</span></span>                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="77e3f-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="77e3f-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="77e3f-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="77e3f-119">The operation was successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="77e3f-120"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="77e3f-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="77e3f-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="77e3f-121">The parameter is **NULL**.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="77e3f-122"><dt>**HRESULT \_ DO \_ Win32 (erro de \_ acesso \_ negado)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="77e3f-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="77e3f-123">O chamador deve ter permissões de acesso de execução para iniciar esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="77e3f-123">The caller must have execute access permissions to start this virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="77e3f-124"><dt>**VM \_ E \_ atingiu o tempo \_ limite**</dt> de <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="77e3f-124"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="77e3f-125">A operação não foi concluída oportunamente.</span><span class="sxs-lookup"><span data-stu-id="77e3f-125">The operation did not complete in a timely manner.</span></span><br/>                             |
| <dl> <span data-ttu-id="77e3f-126"><dt>**VM \_ E \_ 0xA0040203 \_ de \_ recurso**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="77e3f-126"><dt>**VM\_E\_OUT\_OF\_RESOURCE**</dt> <dt>0xA0040203</dt></span></span> </dl>                    | <span data-ttu-id="77e3f-127">Não há recursos de host suficientes.</span><span class="sxs-lookup"><span data-stu-id="77e3f-127">There are not enough host resources.</span></span><br/>                                           |
| <dl> <span data-ttu-id="77e3f-128"><dt>**VM \_ E \_ \_ muitas \_ VMs**</dt> <dt>0xA0040204</dt></span><span class="sxs-lookup"><span data-stu-id="77e3f-128"><dt>**VM\_E\_TOO\_MANY\_VMS**</dt> <dt>0xA0040204</dt></span></span> </dl>                       | <span data-ttu-id="77e3f-129">Há muitas máquinas virtuais ativas.</span><span class="sxs-lookup"><span data-stu-id="77e3f-129">There are too many active virtual machines.</span></span><br/>                                    |
| <dl> <span data-ttu-id="77e3f-130"><dt>**VM \_ E \_ VM \_ executando**</dt> <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="77e3f-130"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>                          | <span data-ttu-id="77e3f-131">A máquina virtual já está em execução.</span><span class="sxs-lookup"><span data-stu-id="77e3f-131">The virtual machine is already running.</span></span><br/>                                        |
| <dl> <span data-ttu-id="77e3f-132"><dt>**VM \_ E 0xA00400687 de \_ \_ modificação pai**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="77e3f-132"><dt>**VM\_E\_PARENT\_MODIFIED**</dt> <dt>0xA00400687</dt></span></span> </dl>                    | <span data-ttu-id="77e3f-133">A máquina virtual não pode ser iniciada porque o VHD pai foi modificado.</span><span class="sxs-lookup"><span data-stu-id="77e3f-133">The virtual machine cannot be started as the parent VHD has been modified.</span></span><br/>     |
| <dl> <span data-ttu-id="77e3f-134"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="77e3f-134"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="77e3f-135">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="77e3f-135">An unexpected error has occurred.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="77e3f-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="77e3f-136">Remarks</span></span>

<span data-ttu-id="77e3f-137">Se a máquina virtual for salva, ela será restaurada a partir do estado salvo.</span><span class="sxs-lookup"><span data-stu-id="77e3f-137">If the virtual machine is saved, it will be restored from the saved state.</span></span>

<span data-ttu-id="77e3f-138">Os valores a seguir podem ser retornados por meio da propriedade [**Error**](ivmtask-error.md) do objeto [**IVMTask**](ivmtask.md) retornado.</span><span class="sxs-lookup"><span data-stu-id="77e3f-138">The following values can be returned through the [**Error**](ivmtask-error.md) property of the returned [**IVMTask**](ivmtask.md) object.</span></span>



| <span data-ttu-id="77e3f-139">Código/valor do [**erro**](ivmtask-error.md)</span><span class="sxs-lookup"><span data-stu-id="77e3f-139">[**Error**](ivmtask-error.md) code/Value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="77e3f-140">Descrição</span><span class="sxs-lookup"><span data-stu-id="77e3f-140">Description</span></span>                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="77e3f-141"><span id="VM_E_UNSUPPORTED_HARDWARE__0xA0040950_"></span><span id="vm_e_unsupported_hardware__0xa0040950_"></span><span id="VM_E_UNSUPPORTED_HARDWARE__0XA0040950_"></span>`VM_E_UNSUPPORTED_HARDWARE` (0xA0040950)</span><span class="sxs-lookup"><span data-stu-id="77e3f-141"><span id="VM_E_UNSUPPORTED_HARDWARE__0xA0040950_"></span><span id="vm_e_unsupported_hardware__0xa0040950_"></span><span id="VM_E_UNSUPPORTED_HARDWARE__0XA0040950_"></span>`VM_E_UNSUPPORTED_HARDWARE` (0xA0040950)</span></span><br/>                                                 | <span data-ttu-id="77e3f-142">O hardware não oferece suporte à virtualização.</span><span class="sxs-lookup"><span data-stu-id="77e3f-142">The hardware does not support virtualization.</span></span><br/>              |
| <span data-ttu-id="77e3f-143"><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0xA0040951_"></span><span id="vm_e_hardware_virtualization_disabled__0xa0040951_"></span><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0XA0040951_"></span>`VM_E_HARDWARE_VIRTUALIZATION_DISABLED` (0xA0040951)</span><span class="sxs-lookup"><span data-stu-id="77e3f-143"><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0xA0040951_"></span><span id="vm_e_hardware_virtualization_disabled__0xa0040951_"></span><span id="VM_E_HARDWARE_VIRTUALIZATION_DISABLED__0XA0040951_"></span>`VM_E_HARDWARE_VIRTUALIZATION_DISABLED` (0xA0040951)</span></span><br/> | <span data-ttu-id="77e3f-144">A virtualização de hardware está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="77e3f-144">Hardware virtualization is disabled.</span></span><br/>                       |
| <span data-ttu-id="77e3f-145"><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0xA0040952_"></span><span id="vm_e_vmvirtualpc_older_version__0xa0040952_"></span><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0XA0040952_"></span>`VM_E_VMVIRTUALPC_OLDER_VERSION` (0xA0040952)</span><span class="sxs-lookup"><span data-stu-id="77e3f-145"><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0xA0040952_"></span><span id="vm_e_vmvirtualpc_older_version__0xa0040952_"></span><span id="VM_E_VMVIRTUALPC_OLDER_VERSION__0XA0040952_"></span>`VM_E_VMVIRTUALPC_OLDER_VERSION` (0xA0040952)</span></span><br/>                             | <span data-ttu-id="77e3f-146">O Virtual PC 2007 e o Windows Virtual PC estão instalados.</span><span class="sxs-lookup"><span data-stu-id="77e3f-146">Both Virtual PC 2007 and Windows Virtual PC are installed.</span></span><br/> |
| <span data-ttu-id="77e3f-147"><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0xA0040953_"></span><span id="vm_e_other_virtualization_software__0xa0040953_"></span><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0XA0040953_"></span>`VM_E_OTHER_VIRTUALIZATION_SOFTWARE` (0xA0040953)</span><span class="sxs-lookup"><span data-stu-id="77e3f-147"><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0xA0040953_"></span><span id="vm_e_other_virtualization_software__0xa0040953_"></span><span id="VM_E_OTHER_VIRTUALIZATION_SOFTWARE__0XA0040953_"></span>`VM_E_OTHER_VIRTUALIZATION_SOFTWARE` (0xA0040953)</span></span><br/>             | <span data-ttu-id="77e3f-148">Outros softwares de virtualização estão instalados.</span><span class="sxs-lookup"><span data-stu-id="77e3f-148">Other virtualization software is installed.</span></span><br/>                |
| <span data-ttu-id="77e3f-149"><span id="VM_E_OUT_OF_RESOURCE__0xa00400203_"></span><span id="vm_e_out_of_resource__0xa00400203_"></span><span id="VM_E_OUT_OF_RESOURCE__0XA00400203_"></span>`VM_E_OUT_OF_RESOURCE` (0xa00400203)</span><span class="sxs-lookup"><span data-stu-id="77e3f-149"><span id="VM_E_OUT_OF_RESOURCE__0xa00400203_"></span><span id="vm_e_out_of_resource__0xa00400203_"></span><span id="VM_E_OUT_OF_RESOURCE__0XA00400203_"></span>`VM_E_OUT_OF_RESOURCE` (0xa00400203)</span></span><br/>                                                                 | <span data-ttu-id="77e3f-150">Não há recursos de host suficientes.</span><span class="sxs-lookup"><span data-stu-id="77e3f-150">There are not enough host resources.</span></span><br/>                       |



 

## <a name="requirements"></a><span data-ttu-id="77e3f-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77e3f-151">Requirements</span></span>



| <span data-ttu-id="77e3f-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="77e3f-152">Requirement</span></span> | <span data-ttu-id="77e3f-153">Valor</span><span class="sxs-lookup"><span data-stu-id="77e3f-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="77e3f-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77e3f-154">Minimum supported client</span></span><br/> | <span data-ttu-id="77e3f-155">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="77e3f-155">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="77e3f-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77e3f-156">Minimum supported server</span></span><br/> | <span data-ttu-id="77e3f-157">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="77e3f-157">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="77e3f-158">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="77e3f-158">End of client support</span></span><br/>    | <span data-ttu-id="77e3f-159">Windows 7</span><span class="sxs-lookup"><span data-stu-id="77e3f-159">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="77e3f-160">Produto</span><span class="sxs-lookup"><span data-stu-id="77e3f-160">Product</span></span><br/>                  | <span data-ttu-id="77e3f-161">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="77e3f-161">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="77e3f-162">parâmetro</span><span class="sxs-lookup"><span data-stu-id="77e3f-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="77e3f-163"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="77e3f-163"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="77e3f-164">IID</span><span class="sxs-lookup"><span data-stu-id="77e3f-164">IID</span></span><br/>                      | <span data-ttu-id="77e3f-165">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="77e3f-165">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="77e3f-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="77e3f-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77e3f-167">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="77e3f-167">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

