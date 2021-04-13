---
title: Propriedade UndoAction IVMVirtualMachine (VPCCOMInterfaces. h)
description: Ação padrão a ser executada em todas as unidades de desfazer quando a VM for desligada.
ms.assetid: fcdd5217-4909-435a-b11d-63578ab46e37
keywords:
- Propriedade UndoAction Virtual PC
- Propriedade UndoAction Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, Propriedade UndoAction
topic_type:
- apiref
api_name:
- IVMVirtualMachine.UndoAction
- IVMVirtualMachine.get_UndoAction
- IVMVirtualMachine.put_UndoAction
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 039a9e65863e41ba2c7edc1befd2598aa16bb362
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455681"
---
# <a name="ivmvirtualmachineundoaction-property"></a><span data-ttu-id="81620-106">Propriedade IVMVirtualMachine:: UndoAction</span><span class="sxs-lookup"><span data-stu-id="81620-106">IVMVirtualMachine::UndoAction property</span></span>

<span data-ttu-id="81620-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="81620-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="81620-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="81620-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="81620-109">Recupera e define a ação padrão a ser executada em todas as unidades de desfazer quando a VM (máquina virtual) for desligada usando [**o método de**](ivmvirtualmachine-turnoff.md) desativação ou desligar usando o método [**Shutdown**](ivmguestos-shutdown.md) ou desativado de dentro do sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="81620-109">Retrieves and sets the default action to be performed on all undo drives when the virtual machine (VM) is turned off using the [**TurnOff**](ivmvirtualmachine-turnoff.md) method or shut down using the [**Shutdown**](ivmguestos-shutdown.md) method or turned off from within the guest operating system.</span></span>

<span data-ttu-id="81620-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="81620-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="81620-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="81620-111">Syntax</span></span>


```C++
HRESULT put_UndoAction(
  [in]          VMUndoAction undoAction
);

HRESULT get_UndoAction(
  [out, retval] VMUndoAction *undoAction
);
```



## <a name="property-value"></a><span data-ttu-id="81620-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="81620-112">Property value</span></span>

<span data-ttu-id="81620-113">Especifica a ação padrão a ser executada em todas as unidades de desfazer quando a VM for desligada de dentro do sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="81620-113">Specifies the default action to be performed on all undo drives when the VM is shut down from within the guest operating system.</span></span> <span data-ttu-id="81620-114">Para obter uma lista de valores, consulte [**VMUndoAction**](vmundoaction.md).</span><span class="sxs-lookup"><span data-stu-id="81620-114">For a list of values, see [**VMUndoAction**](vmundoaction.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="81620-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="81620-115">Error codes</span></span>



| <span data-ttu-id="81620-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="81620-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="81620-117">Significado</span><span class="sxs-lookup"><span data-stu-id="81620-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="81620-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="81620-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="81620-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="81620-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="81620-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="81620-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="81620-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="81620-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="81620-122"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="81620-122"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="81620-123">O parâmetro não é válido.</span><span class="sxs-lookup"><span data-stu-id="81620-123">The parameter is not valid.</span></span><br/>       |
| <dl> <span data-ttu-id="81620-124"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="81620-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="81620-125">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="81620-125">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="81620-126"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="81620-126"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="81620-127">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="81620-127">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="81620-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81620-128">Requirements</span></span>



| <span data-ttu-id="81620-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="81620-129">Requirement</span></span> | <span data-ttu-id="81620-130">Valor</span><span class="sxs-lookup"><span data-stu-id="81620-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="81620-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81620-131">Minimum supported client</span></span><br/> | <span data-ttu-id="81620-132">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="81620-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="81620-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81620-133">Minimum supported server</span></span><br/> | <span data-ttu-id="81620-134">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="81620-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="81620-135">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="81620-135">End of client support</span></span><br/>    | <span data-ttu-id="81620-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="81620-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="81620-137">Produto</span><span class="sxs-lookup"><span data-stu-id="81620-137">Product</span></span><br/>                  | <span data-ttu-id="81620-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="81620-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="81620-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="81620-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="81620-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="81620-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="81620-141">IID</span><span class="sxs-lookup"><span data-stu-id="81620-141">IID</span></span><br/>                      | <span data-ttu-id="81620-142">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="81620-142">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="81620-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="81620-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81620-144">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="81620-144">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

