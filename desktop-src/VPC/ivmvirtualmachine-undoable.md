---
title: Propriedade IVMVirtualMachineble (VPCCOMInterfaces. h)
description: Determina se as unidades de desfazer estão habilitadas para discos rígidos conectados à VM.
ms.assetid: 4f591360-1229-46ae-9925-3a3d02ab3202
keywords:
- PC virtual de propriedade de desfazer
- Propriedade undoable Virtual PC, interface IVMVirtualMachine
- Virtual PC da interface IVMVirtualMachine, Propriedade undoable
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Undoable
- IVMVirtualMachine.get_Undoable
- IVMVirtualMachine.put_Undoable
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2cbc77f4d68fbdbfcc8d3998e3c207b8f4245c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499400"
---
# <a name="ivmvirtualmachineundoable-property"></a><span data-ttu-id="17897-106">Propriedade IVMVirtualMachine:: undoable</span><span class="sxs-lookup"><span data-stu-id="17897-106">IVMVirtualMachine::Undoable property</span></span>

<span data-ttu-id="17897-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="17897-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="17897-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="17897-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="17897-109">Determina se as unidades de desfazer estão habilitadas para discos rígidos conectados à VM (máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="17897-109">Determines whether undo drives are enabled for hard disks connected to the virtual machine (VM).</span></span>

<span data-ttu-id="17897-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="17897-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="17897-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="17897-111">Syntax</span></span>


```C++
HRESULT put_Undoable(
  [in]          VARIANT_BOOL enableUndo
);

HRESULT get_Undoable(
  [out, retval] VARIANT_BOOL *isUndoable
);
```



## <a name="property-value"></a><span data-ttu-id="17897-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="17897-112">Property value</span></span>

<span data-ttu-id="17897-113">Especifica a **variante \_ true** se as unidades de desfazer estiverem habilitadas para discos rígidos conectados à VM e **Variant \_ false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="17897-113">Specifies **VARIANT\_TRUE** if undo drives are enabled for hard disks connected to the VM and **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="17897-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="17897-114">Error codes</span></span>



| <span data-ttu-id="17897-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="17897-115">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="17897-116">Significado</span><span class="sxs-lookup"><span data-stu-id="17897-116">Meaning</span></span>                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="17897-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="17897-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="17897-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="17897-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="17897-119"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="17897-119"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="17897-120">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="17897-120">An unexpected error has occurred.</span></span><br/> |
| <dl> <span data-ttu-id="17897-121"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="17897-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="17897-122">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="17897-122">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="17897-123"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="17897-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="17897-124">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="17897-124">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="17897-125"><dt>VM \_ E \_ pref \_ VM \_ ativa</dt> <dt>0xA0040302</dt></span><span class="sxs-lookup"><span data-stu-id="17897-125"><dt>VM\_E\_PREF\_VM\_ACTIVE</dt> <dt>0xA0040302</dt></span></span> </dl> | <span data-ttu-id="17897-126">A VM está em execução ou salva.</span><span class="sxs-lookup"><span data-stu-id="17897-126">The VM is running or saved.</span></span><br/>       |



## <a name="remarks"></a><span data-ttu-id="17897-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="17897-127">Remarks</span></span>

<span data-ttu-id="17897-128">Se as unidades de desfazer estiverem desabilitadas, qualquer arquivo de unidade de desfazer existente será excluído.</span><span class="sxs-lookup"><span data-stu-id="17897-128">If undo drives are disabled, any existing undo drive files will be deleted.</span></span>

<span data-ttu-id="17897-129">Você não poderá definir essa propriedade se a VM estiver em execução ou salva.</span><span class="sxs-lookup"><span data-stu-id="17897-129">You cannot set this property if the VM is running or saved.</span></span>

## <a name="requirements"></a><span data-ttu-id="17897-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17897-130">Requirements</span></span>



| <span data-ttu-id="17897-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="17897-131">Requirement</span></span> | <span data-ttu-id="17897-132">Valor</span><span class="sxs-lookup"><span data-stu-id="17897-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="17897-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17897-133">Minimum supported client</span></span><br/> | <span data-ttu-id="17897-134">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="17897-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="17897-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="17897-135">Minimum supported server</span></span><br/> | <span data-ttu-id="17897-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="17897-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="17897-137">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="17897-137">End of client support</span></span><br/>    | <span data-ttu-id="17897-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="17897-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="17897-139">Produto</span><span class="sxs-lookup"><span data-stu-id="17897-139">Product</span></span><br/>                  | <span data-ttu-id="17897-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="17897-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="17897-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="17897-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="17897-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="17897-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="17897-143">IID</span><span class="sxs-lookup"><span data-stu-id="17897-143">IID</span></span><br/>                      | <span data-ttu-id="17897-144">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="17897-144">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="17897-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="17897-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17897-146">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="17897-146">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

