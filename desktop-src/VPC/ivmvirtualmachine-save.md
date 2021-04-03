---
title: Método IVMVirtualMachine Save (VPCCOMInterfaces. h)
description: Salva o estado da VM (máquina virtual).
ms.assetid: e9f6e773-4e2d-4d7b-9624-e7864d5b248b
keywords:
- Salvar método virtual PC
- Método Save Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, método Save
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Save
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27b4dbe18b89f107657d67fb7e7b90e024b01383
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644995"
---
# <a name="ivmvirtualmachinesave-method"></a><span data-ttu-id="05e77-106">Método IVMVirtualMachine:: Save</span><span class="sxs-lookup"><span data-stu-id="05e77-106">IVMVirtualMachine::Save method</span></span>

<span data-ttu-id="05e77-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="05e77-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="05e77-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="05e77-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="05e77-109">Salva o estado da VM (máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="05e77-109">Saves the virtual machine (VM) state.</span></span>

## <a name="syntax"></a><span data-ttu-id="05e77-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="05e77-110">Syntax</span></span>


```C++
HRESULT Save(
  [out, retval] IVMTask **saveTask
);
```



## <a name="parameters"></a><span data-ttu-id="05e77-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="05e77-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05e77-112">*saveTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="05e77-112">*saveTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="05e77-113">Um objeto [**IVMTask**](ivmtask.md) que é usado para acompanhar o progresso de conclusão da sequência de salvamento de estado da VM.</span><span class="sxs-lookup"><span data-stu-id="05e77-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the VM's state saving sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05e77-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="05e77-114">Return value</span></span>

<span data-ttu-id="05e77-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="05e77-115">This method can return one of these values.</span></span>



| <span data-ttu-id="05e77-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="05e77-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="05e77-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="05e77-117">Description</span></span>                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="05e77-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="05e77-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="05e77-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="05e77-119">The operation was successful.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="05e77-120"><dt>**E \_ FALHA**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="05e77-120"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>                                     | <span data-ttu-id="05e77-121">Não foi possível salvar a VM porque os discos de desfazer foram marcados para exclusão.</span><span class="sxs-lookup"><span data-stu-id="05e77-121">The VM could not be saved because the undo disks were marked for deletion.</span></span><br/>    |
| <dl> <span data-ttu-id="05e77-122"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="05e77-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="05e77-123">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="05e77-123">The parameter is **NULL**.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="05e77-124"><dt>**HRESULT \_ DO \_ Win32 (erro de \_ acesso \_ negado)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="05e77-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="05e77-125">O chamador deve ter permissões de acesso de execução para salvar o estado dessa VM.</span><span class="sxs-lookup"><span data-stu-id="05e77-125">The caller must have execute access permissions to save the state of this VM.</span></span><br/> |
| <dl> <span data-ttu-id="05e77-126"><dt>**VM \_ E a \_ VM \_ não \_ está executando**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="05e77-126"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="05e77-127">A VM não está em execução.</span><span class="sxs-lookup"><span data-stu-id="05e77-127">The VM is not running.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="05e77-128"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="05e77-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="05e77-129">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="05e77-129">An unexpected error has occurred.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="05e77-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="05e77-130">Remarks</span></span>

<span data-ttu-id="05e77-131">A VM é desativada quando a tarefa de **salvamento** atinge a conclusão.</span><span class="sxs-lookup"><span data-stu-id="05e77-131">The VM is turned off when the **Save** task reaches completion.</span></span> <span data-ttu-id="05e77-132">A propriedade [**IVMVirtualMachine:: State**](ivmvirtualmachine-state.md) conterá **o \_ salvamento de vmVMState** enquanto o salvamento estiver em andamento, seguido pelo **vmVMState \_ salvo** quando o salvamento for concluído e a VM for desativada.</span><span class="sxs-lookup"><span data-stu-id="05e77-132">The [**IVMVirtualMachine::State**](ivmvirtualmachine-state.md) property will contain **vmVMState\_Saving** while the save is in progress, followed by **vmVMState\_Saved** when the save has completed and the VM is turned off.</span></span>

## <a name="requirements"></a><span data-ttu-id="05e77-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05e77-133">Requirements</span></span>



| <span data-ttu-id="05e77-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="05e77-134">Requirement</span></span> | <span data-ttu-id="05e77-135">Valor</span><span class="sxs-lookup"><span data-stu-id="05e77-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="05e77-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05e77-136">Minimum supported client</span></span><br/> | <span data-ttu-id="05e77-137">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="05e77-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="05e77-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05e77-138">Minimum supported server</span></span><br/> | <span data-ttu-id="05e77-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="05e77-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="05e77-140">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="05e77-140">End of client support</span></span><br/>    | <span data-ttu-id="05e77-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="05e77-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="05e77-142">Produto</span><span class="sxs-lookup"><span data-stu-id="05e77-142">Product</span></span><br/>                  | <span data-ttu-id="05e77-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="05e77-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="05e77-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="05e77-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="05e77-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="05e77-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="05e77-146">IID</span><span class="sxs-lookup"><span data-stu-id="05e77-146">IID</span></span><br/>                      | <span data-ttu-id="05e77-147">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="05e77-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="05e77-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="05e77-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05e77-149">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="05e77-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

