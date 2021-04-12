---
title: Propriedade IVMVirtualMachine Notes (VPCCOMInterfaces. h)
description: Observações para a máquina virtual.
ms.assetid: 4be6842b-31b2-4619-a6ab-b728be1e2174
keywords:
- Propriedade do Notes Virtual PC
- Propriedade Notes Virtual PC, interface IVMVirtualMachine
- Interface do IVMVirtualMachine Virtual PC, propriedade Notes
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Notes
- IVMVirtualMachine.get_Notes
- IVMVirtualMachine.put_Notes
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca8fba8659a8f9546866129f21299e44006eb496
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455801"
---
# <a name="ivmvirtualmachinenotes-property"></a><span data-ttu-id="ee95e-106">Propriedade IVMVirtualMachine:: Notes</span><span class="sxs-lookup"><span data-stu-id="ee95e-106">IVMVirtualMachine::Notes property</span></span>

<span data-ttu-id="ee95e-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ee95e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ee95e-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ee95e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ee95e-109">Recupera e define as notas para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ee95e-109">Retrieves and sets the notes for the virtual machine.</span></span>

<span data-ttu-id="ee95e-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="ee95e-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee95e-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee95e-111">Syntax</span></span>


```C++
HRESULT put_Notes(
  [in]          BSTR virtualMachineNotes
);

HRESULT get_Notes(
  [out, retval] BSTR *virtualMachineNotes
);
```



## <a name="property-value"></a><span data-ttu-id="ee95e-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ee95e-112">Property value</span></span>

<span data-ttu-id="ee95e-113">Especifica as notas para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ee95e-113">Specifies the notes for the virtual machine.</span></span> <span data-ttu-id="ee95e-114">O comprimento máximo da cadeia de caracteres é de 65.536 caracteres.</span><span class="sxs-lookup"><span data-stu-id="ee95e-114">The maximum length of the string is 65,536 characters.</span></span>

<span data-ttu-id="ee95e-115">Para remover todas as observações, passe uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="ee95e-115">To remove any notes, pass an empty string.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ee95e-116">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="ee95e-116">Error codes</span></span>



| <span data-ttu-id="ee95e-117">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="ee95e-117">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="ee95e-118">Significado</span><span class="sxs-lookup"><span data-stu-id="ee95e-118">Meaning</span></span>                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ee95e-119"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ee95e-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="ee95e-120">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ee95e-120">The operation was successful.</span></span><br/>                                       |
| <dl> <span data-ttu-id="ee95e-121"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="ee95e-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="ee95e-122">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="ee95e-122">The parameter is **NULL**.</span></span><br/>                                          |
| <dl> <span data-ttu-id="ee95e-123"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="ee95e-123"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="ee95e-124">O parâmetro não é válido ou contém mais de 65.536 caracteres.</span><span class="sxs-lookup"><span data-stu-id="ee95e-124">The parameter is not valid or contains more than 65,536 characters.</span></span><br/> |
| <dl> <span data-ttu-id="ee95e-125"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ee95e-125"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="ee95e-126">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="ee95e-126">The configuration is unknown.</span></span><br/>                                       |
| <dl> <span data-ttu-id="ee95e-127"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="ee95e-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="ee95e-128">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="ee95e-128">An unexpected error has occurred.</span></span><br/>                                   |



## <a name="requirements"></a><span data-ttu-id="ee95e-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee95e-129">Requirements</span></span>



| <span data-ttu-id="ee95e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee95e-130">Requirement</span></span> | <span data-ttu-id="ee95e-131">Valor</span><span class="sxs-lookup"><span data-stu-id="ee95e-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee95e-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee95e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ee95e-133">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ee95e-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ee95e-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee95e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ee95e-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ee95e-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ee95e-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="ee95e-136">End of client support</span></span><br/>    | <span data-ttu-id="ee95e-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ee95e-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ee95e-138">Produto</span><span class="sxs-lookup"><span data-stu-id="ee95e-138">Product</span></span><br/>                  | <span data-ttu-id="ee95e-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ee95e-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ee95e-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ee95e-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee95e-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee95e-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ee95e-142">IID</span><span class="sxs-lookup"><span data-stu-id="ee95e-142">IID</span></span><br/>                      | <span data-ttu-id="ee95e-143">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="ee95e-143">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="ee95e-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee95e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee95e-145">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="ee95e-145">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

