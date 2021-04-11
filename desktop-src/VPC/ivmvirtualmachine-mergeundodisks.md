---
title: Método IVMVirtualMachine MergeUndoDisks (VPCCOMInterfaces. h)
description: Mescla os discos de desfazer virtuais.
ms.assetid: 6445b097-220e-48c4-9a7b-1139ca7b3338
keywords:
- MergeUndoDisks do método virtual PC
- Método MergeUndoDisks Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, método MergeUndoDisks
topic_type:
- apiref
api_name:
- IVMVirtualMachine.MergeUndoDisks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48863bf998ebc02bac93aa9e74d8cdbe07265477
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295861"
---
# <a name="ivmvirtualmachinemergeundodisks-method"></a><span data-ttu-id="20f7e-106">Método IVMVirtualMachine:: MergeUndoDisks</span><span class="sxs-lookup"><span data-stu-id="20f7e-106">IVMVirtualMachine::MergeUndoDisks method</span></span>

<span data-ttu-id="20f7e-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="20f7e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="20f7e-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="20f7e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="20f7e-109">Mescla os discos de desfazer virtuais.</span><span class="sxs-lookup"><span data-stu-id="20f7e-109">Merges the virtual undo disks.</span></span>

## <a name="syntax"></a><span data-ttu-id="20f7e-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20f7e-110">Syntax</span></span>


```C++
HRESULT MergeUndoDisks(
  [out, retval] IVMTask **undoMergeTask
);
```



## <a name="parameters"></a><span data-ttu-id="20f7e-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20f7e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20f7e-112">*undoMergeTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="20f7e-112">*undoMergeTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="20f7e-113">Um objeto [**IVMTask**](ivmtask.md) que é usado para acompanhar a criação da imagem.</span><span class="sxs-lookup"><span data-stu-id="20f7e-113">An [**IVMTask**](ivmtask.md) object that is used to track the creation of the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20f7e-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="20f7e-114">Return value</span></span>

<span data-ttu-id="20f7e-115">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="20f7e-115">This method can return one of these values.</span></span>



| <span data-ttu-id="20f7e-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="20f7e-116">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="20f7e-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="20f7e-117">Description</span></span>                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="20f7e-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="20f7e-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="20f7e-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="20f7e-119">The operation was successful.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="20f7e-120"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="20f7e-120"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="20f7e-121">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="20f7e-121">An unexpected error has occurred.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="20f7e-122"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="20f7e-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="20f7e-123">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="20f7e-123">The parameter is **NULL**.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="20f7e-124"><dt>**HRESULT \_ Do \_ Win32 (caminho de erro \_ \_ não \_ encontrado)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="20f7e-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="20f7e-125">O sistema não pode localizar o caminho especificado pelo parâmetro *convertedDiskImagePath* ou um dos discos pai não é válido.</span><span class="sxs-lookup"><span data-stu-id="20f7e-125">The system cannot find the path specified by the *convertedDiskImagePath* parameter or one of the parent disks is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="20f7e-126"><dt>**E \_ ACCESSDENIED**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="20f7e-126"><dt>**E\_ACCESSDENIED**</dt> <dt>0x80070005</dt></span></span> </dl>                               | <span data-ttu-id="20f7e-127">O usuário atual não tem acesso suficiente ao arquivo pai.</span><span class="sxs-lookup"><span data-stu-id="20f7e-127">The current user has insufficient access to the parent file.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="20f7e-128"><dt>**E \_ MANIPULAR**</dt> <dt>0x80070006</dt></span><span class="sxs-lookup"><span data-stu-id="20f7e-128"><dt>**E\_HANDLE**</dt> <dt>0x80070006</dt></span></span> </dl>                                     | <span data-ttu-id="20f7e-129">Um dos discos pai está em uso.</span><span class="sxs-lookup"><span data-stu-id="20f7e-129">One of the parent disks is in use.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="20f7e-130"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="20f7e-130"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                            | <span data-ttu-id="20f7e-131">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="20f7e-131">The configuration is unknown.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="20f7e-132"><dt>**VM \_ E \_ VM \_ executando**</dt> <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="20f7e-132"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>                            | <span data-ttu-id="20f7e-133">A máquina virtual está em execução.</span><span class="sxs-lookup"><span data-stu-id="20f7e-133">The virtual machine is running.</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="20f7e-134"><dt>**VM \_ E \_ File \_ \_ somente leitura**</dt> <dt>0xA004067A</dt></span><span class="sxs-lookup"><span data-stu-id="20f7e-134"><dt>**VM\_E\_FILE\_READ\_ONLY**</dt> <dt>0xA004067A</dt></span></span> </dl>                       | <span data-ttu-id="20f7e-135">O pai de discos de desfazer virtuais está marcado como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="20f7e-135">The parent of virtual undo disks is marked as read only.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="20f7e-136"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="20f7e-136"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="20f7e-137">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="20f7e-137">An unexpected error has occurred.</span></span><br/>                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="20f7e-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="20f7e-138">Remarks</span></span>

<span data-ttu-id="20f7e-139">**MergeUndoDisks** não pode ser chamado enquanto a máquina virtual ainda estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="20f7e-139">**MergeUndoDisks** cannot be called while the virtual machine is still running.</span></span> <span data-ttu-id="20f7e-140">Use [**IVMVirtualMachine:: Save**](ivmvirtualmachine-save.md) para salvar o estado da máquina virtual antes de chamar **MergeUndoDisks** ou [**IVMVirtualMachine::**](ivmvirtualmachine-turnoff.md) inativação para desligar a máquina virtual sem salvar seu estado atual antecipadamente.</span><span class="sxs-lookup"><span data-stu-id="20f7e-140">Use [**IVMVirtualMachine::Save**](ivmvirtualmachine-save.md) to save the state of the virtual machine before calling **MergeUndoDisks**, or [**IVMVirtualMachine::TurnOff**](ivmvirtualmachine-turnoff.md) to turn off the virtual machine without saving its current state beforehand.</span></span>

## <a name="requirements"></a><span data-ttu-id="20f7e-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20f7e-141">Requirements</span></span>



| <span data-ttu-id="20f7e-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="20f7e-142">Requirement</span></span> | <span data-ttu-id="20f7e-143">Valor</span><span class="sxs-lookup"><span data-stu-id="20f7e-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="20f7e-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20f7e-144">Minimum supported client</span></span><br/> | <span data-ttu-id="20f7e-145">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="20f7e-145">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="20f7e-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20f7e-146">Minimum supported server</span></span><br/> | <span data-ttu-id="20f7e-147">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="20f7e-147">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="20f7e-148">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="20f7e-148">End of client support</span></span><br/>    | <span data-ttu-id="20f7e-149">Windows 7</span><span class="sxs-lookup"><span data-stu-id="20f7e-149">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="20f7e-150">Produto</span><span class="sxs-lookup"><span data-stu-id="20f7e-150">Product</span></span><br/>                  | <span data-ttu-id="20f7e-151">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="20f7e-151">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="20f7e-152">parâmetro</span><span class="sxs-lookup"><span data-stu-id="20f7e-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="20f7e-153"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="20f7e-153"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="20f7e-154">IID</span><span class="sxs-lookup"><span data-stu-id="20f7e-154">IID</span></span><br/>                      | <span data-ttu-id="20f7e-155">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="20f7e-155">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="20f7e-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="20f7e-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20f7e-157">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="20f7e-157">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

