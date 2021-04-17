---
title: Propriedade de memória IVMVirtualMachine (VPCCOMInterfaces. h)
description: Quantidade de memória física na máquina virtual, em megabytes.
ms.assetid: 1a1d4cc7-a537-49f0-981f-0b72eca9013e
keywords:
- Propriedade de memória virtual PC
- Propriedade de memória virtual PC, interface IVMVirtualMachine
- Virtual PC interface IVMVirtualMachine, Propriedade Memory
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Memory
- IVMVirtualMachine.get_Memory
- IVMVirtualMachine.put_Memory
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b73251b58639e0311e33120cd4bb0e778a017b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105747501"
---
# <a name="ivmvirtualmachinememory-property"></a><span data-ttu-id="3e920-106">Propriedade IVMVirtualMachine:: Memory</span><span class="sxs-lookup"><span data-stu-id="3e920-106">IVMVirtualMachine::Memory property</span></span>

<span data-ttu-id="3e920-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3e920-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3e920-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3e920-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3e920-109">Recupera e define a quantidade de memória física na máquina virtual, em megabytes.</span><span class="sxs-lookup"><span data-stu-id="3e920-109">Retrieves and sets the amount of physical memory in the virtual machine, in megabytes.</span></span>

<span data-ttu-id="3e920-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3e920-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e920-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e920-111">Syntax</span></span>


```C++
HRESULT put_Memory(
  [in]          long megabytesOfMemory
);

HRESULT get_Memory(
  [out, retval] long *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="3e920-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3e920-112">Property value</span></span>

<span data-ttu-id="3e920-113">Especifica a quantidade de memória física, em megabytes.</span><span class="sxs-lookup"><span data-stu-id="3e920-113">Specifies the amount of physical memory, in megabytes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3e920-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="3e920-114">Error codes</span></span>



| <span data-ttu-id="3e920-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="3e920-115">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="3e920-116">Significado</span><span class="sxs-lookup"><span data-stu-id="3e920-116">Meaning</span></span>                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="3e920-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3e920-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="3e920-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="3e920-118">The operation was successful.</span></span><br/>                  |
| <dl> <span data-ttu-id="3e920-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="3e920-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="3e920-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="3e920-120">The parameter is **NULL**.</span></span><br/>                     |
| <dl> <span data-ttu-id="3e920-121"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="3e920-121"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="3e920-122">O parâmetro não é válido ou está fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="3e920-122">The parameter is not valid or is out of range.</span></span><br/> |
| <dl> <span data-ttu-id="3e920-123"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3e920-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="3e920-124">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="3e920-124">The configuration is unknown.</span></span><br/>                  |
| <dl> <span data-ttu-id="3e920-125"><dt>VM \_ E \_ pref \_ não \_ encontrado</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="3e920-125"><dt>VM\_E\_PREF\_NOT\_FOUND</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="3e920-126">A preferência não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="3e920-126">The preference was not found.</span></span><br/>                  |
| <dl> <span data-ttu-id="3e920-127"><dt>VM \_ E \_ pref \_ VM \_ ativa</dt> <dt>0xA0040302</dt></span><span class="sxs-lookup"><span data-stu-id="3e920-127"><dt>VM\_E\_PREF\_VM\_ACTIVE</dt> <dt>0xA0040302</dt></span></span> </dl> | <span data-ttu-id="3e920-128">A máquina virtual está em execução ou salva.</span><span class="sxs-lookup"><span data-stu-id="3e920-128">The virtual machine is running or saved.</span></span><br/>       |
| <dl> <span data-ttu-id="3e920-129"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="3e920-129"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="3e920-130">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="3e920-130">An unexpected error has occurred.</span></span><br/>              |



## <a name="remarks"></a><span data-ttu-id="3e920-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e920-131">Remarks</span></span>

<span data-ttu-id="3e920-132">A quantidade de memória física em uma máquina virtual deve ser de pelo menos 4 MB.</span><span class="sxs-lookup"><span data-stu-id="3e920-132">The amount of physical memory in a virtual machine must be at least 4 MB.</span></span> <span data-ttu-id="3e920-133">O limite superior na memória depende da configuração do host, mas pode ter no máximo 3.712 MB.</span><span class="sxs-lookup"><span data-stu-id="3e920-133">The upper limit on memory depends on the host configuration, but can be at most 3,712 MB.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e920-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e920-134">Requirements</span></span>



| <span data-ttu-id="3e920-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e920-135">Requirement</span></span> | <span data-ttu-id="3e920-136">Valor</span><span class="sxs-lookup"><span data-stu-id="3e920-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e920-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e920-137">Minimum supported client</span></span><br/> | <span data-ttu-id="3e920-138">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3e920-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3e920-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e920-139">Minimum supported server</span></span><br/> | <span data-ttu-id="3e920-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3e920-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3e920-141">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="3e920-141">End of client support</span></span><br/>    | <span data-ttu-id="3e920-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3e920-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3e920-143">Produto</span><span class="sxs-lookup"><span data-stu-id="3e920-143">Product</span></span><br/>                  | <span data-ttu-id="3e920-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3e920-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3e920-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3e920-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e920-146"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e920-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3e920-147">IID</span><span class="sxs-lookup"><span data-stu-id="3e920-147">IID</span></span><br/>                      | <span data-ttu-id="3e920-148">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="3e920-148">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="3e920-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e920-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e920-150">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="3e920-150">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

