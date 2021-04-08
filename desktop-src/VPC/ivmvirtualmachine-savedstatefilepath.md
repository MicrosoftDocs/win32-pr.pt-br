---
title: Propriedade IVMVirtualMachine SavedStateFilePath (VPCCOMInterfaces. h)
description: Recupera o caminho completo para o arquivo de estado salvo.
ms.assetid: 01bd5491-4d08-4558-ac33-01b096f057a2
keywords:
- Propriedade SavedStateFilePath Virtual PC
- Propriedade SavedStateFilePath Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, Propriedade SavedStateFilePath
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SavedStateFilePath
- IVMVirtualMachine.get_SavedStateFilePath
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e9baea53e3fce2455a2bdfa361e56b45b9b65d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086109"
---
# <a name="ivmvirtualmachinesavedstatefilepath-property"></a><span data-ttu-id="7e454-106">Propriedade IVMVirtualMachine:: SavedStateFilePath</span><span class="sxs-lookup"><span data-stu-id="7e454-106">IVMVirtualMachine::SavedStateFilePath property</span></span>

<span data-ttu-id="7e454-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7e454-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7e454-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7e454-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7e454-109">Recupera o caminho completo para o arquivo de estado salvo.</span><span class="sxs-lookup"><span data-stu-id="7e454-109">Retrieves the full path to the saved state file.</span></span>

<span data-ttu-id="7e454-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="7e454-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e454-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e454-111">Syntax</span></span>


```C++
HRESULT get_SavedStateFilePath(
  [out, retval] BSTR *savedStateFilePath
);
```



## <a name="property-value"></a><span data-ttu-id="7e454-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7e454-112">Property value</span></span>

<span data-ttu-id="7e454-113">O caminho totalmente qualificado para o arquivo de estado salvo da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7e454-113">The fully qualified path to the virtual machine's saved state file.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7e454-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="7e454-114">Error codes</span></span>



| <span data-ttu-id="7e454-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="7e454-115">Name/value</span></span>                                                                                                                                                              | <span data-ttu-id="7e454-116">Significado</span><span class="sxs-lookup"><span data-stu-id="7e454-116">Meaning</span></span>                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="7e454-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7e454-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="7e454-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7e454-118">The operation was successful.</span></span><br/>                           |
| <dl> <span data-ttu-id="7e454-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="7e454-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                   | <span data-ttu-id="7e454-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="7e454-120">The parameter is **NULL**.</span></span><br/>                              |
| <dl> <span data-ttu-id="7e454-121"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7e454-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>           | <span data-ttu-id="7e454-122">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="7e454-122">The configuration is unknown.</span></span><br/>                           |
| <dl> <span data-ttu-id="7e454-123"><dt>VM \_ E \_ VM \_ não \_ 0xA00400501 \_ estado salvo</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7e454-123"><dt>VM\_E\_VM\_NO\_SAVED\_STATE</dt> <dt>0xA00400501</dt></span></span> </dl> | <span data-ttu-id="7e454-124">A máquina virtual não tem nenhum arquivo de estado salvo associado.</span><span class="sxs-lookup"><span data-stu-id="7e454-124">The virtual machine has no associated saved state file.</span></span><br/> |
| <dl> <span data-ttu-id="7e454-125"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="7e454-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>           | <span data-ttu-id="7e454-126">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="7e454-126">An unexpected error has occurred.</span></span><br/>                       |



## <a name="requirements"></a><span data-ttu-id="7e454-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e454-127">Requirements</span></span>



| <span data-ttu-id="7e454-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e454-128">Requirement</span></span> | <span data-ttu-id="7e454-129">Valor</span><span class="sxs-lookup"><span data-stu-id="7e454-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e454-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7e454-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7e454-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7e454-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7e454-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7e454-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7e454-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7e454-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7e454-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="7e454-134">End of client support</span></span><br/>    | <span data-ttu-id="7e454-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7e454-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7e454-136">Produto</span><span class="sxs-lookup"><span data-stu-id="7e454-136">Product</span></span><br/>                  | <span data-ttu-id="7e454-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7e454-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7e454-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7e454-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e454-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e454-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7e454-140">IID</span><span class="sxs-lookup"><span data-stu-id="7e454-140">IID</span></span><br/>                      | <span data-ttu-id="7e454-141">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="7e454-141">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="7e454-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="7e454-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e454-143">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="7e454-143">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

