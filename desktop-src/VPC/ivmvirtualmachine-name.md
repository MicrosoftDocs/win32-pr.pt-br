---
title: Propriedade nome do IVMVirtualMachine (VPCCOMInterfaces. h)
description: Nome da configuração da máquina virtual.
ms.assetid: 90acedbf-4159-48a3-a9e9-6f1ee00dab8b
keywords:
- Propriedade do nome Virtual PC
- Propriedade de nome Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, Propriedade Name
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Name
- IVMVirtualMachine.get_Name
- IVMVirtualMachine.put_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c163173a778d8103922fd8c8948ab5156f512ed0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085696"
---
# <a name="ivmvirtualmachinename-property"></a><span data-ttu-id="e8a45-106">Propriedade IVMVirtualMachine:: Name</span><span class="sxs-lookup"><span data-stu-id="e8a45-106">IVMVirtualMachine::Name property</span></span>

<span data-ttu-id="e8a45-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e8a45-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e8a45-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e8a45-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e8a45-109">Recupera e define o nome da configuração da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e8a45-109">Retrieves and sets the name of the virtual machine configuration.</span></span>

<span data-ttu-id="e8a45-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="e8a45-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8a45-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e8a45-111">Syntax</span></span>


```C++
HRESULT put_Name(
  [in]          BSTR virtualMachineName
);

HRESULT get_Name(
  [out, retval] BSTR *virtualMachineName
);
```



## <a name="property-value"></a><span data-ttu-id="e8a45-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e8a45-112">Property value</span></span>

<span data-ttu-id="e8a45-113">Especifica o nome da configuração da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e8a45-113">Specifies the name of the virtual machine configuration.</span></span> <span data-ttu-id="e8a45-114">O comprimento do nome não pode ter mais de 80 caracteres e o comprimento total do caminho totalmente qualificado que inclui o arquivo de configuração de nome da máquina virtual não pode ser maior que o máximo de caracteres de **\_ caminho** (260).</span><span class="sxs-lookup"><span data-stu-id="e8a45-114">The length of the name cannot be more than 80 characters and the total length of the fully qualified path that includes the virtual machine name configuration file cannot be more than **MAX\_PATH** (260) characters.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e8a45-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="e8a45-115">Error codes</span></span>



| <span data-ttu-id="e8a45-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="e8a45-116">Name/value</span></span>                                                                                                                                                                    | <span data-ttu-id="e8a45-117">Significado</span><span class="sxs-lookup"><span data-stu-id="e8a45-117">Meaning</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e8a45-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e8a45-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                       | <span data-ttu-id="e8a45-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e8a45-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="e8a45-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="e8a45-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                         | <span data-ttu-id="e8a45-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e8a45-121">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="e8a45-122"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="e8a45-122"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                      | <span data-ttu-id="e8a45-123">O parâmetro não é válido ou é uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="e8a45-123">The parameter is not valid or is an empty string.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e8a45-124"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e8a45-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>                 | <span data-ttu-id="e8a45-125">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="e8a45-125">The configuration is unknown.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="e8a45-126"><dt>VM \_ E \_ pref \_ VM \_ ativa</dt> <dt>0xA0040302</dt></span><span class="sxs-lookup"><span data-stu-id="e8a45-126"><dt>VM\_E\_PREF\_VM\_ACTIVE</dt> <dt>0xA0040302</dt></span></span> </dl>            | <span data-ttu-id="e8a45-127">A máquina virtual está em execução ou salva.</span><span class="sxs-lookup"><span data-stu-id="e8a45-127">The virtual machine is running or saved.</span></span><br/>                                             |
| <dl> <span data-ttu-id="e8a45-128"><dt>VM \_ E \_ config \_ sem \_ nome</dt> <dt>0xA0040400</dt></span><span class="sxs-lookup"><span data-stu-id="e8a45-128"><dt>VM\_E\_CONFIG\_NO\_NAME</dt> <dt>0xA0040400</dt></span></span> </dl>            | <span data-ttu-id="e8a45-129">O parâmetro *virtualMachineName* está vazio.</span><span class="sxs-lookup"><span data-stu-id="e8a45-129">The *virtualMachineName* parameter is empty.</span></span><br/>                                         |
| <dl> <span data-ttu-id="e8a45-130"><dt>VM \_ O \_ nome da configuração E é \_ \_ muito \_ longo</dt> <dt>0xA00400401</dt></span><span class="sxs-lookup"><span data-stu-id="e8a45-130"><dt>VM\_E\_CONFIG\_NAME\_TOO\_LONG</dt> <dt>0xA00400401</dt></span></span> </dl>    | <span data-ttu-id="e8a45-131">O parâmetro contém muitos caracteres.</span><span class="sxs-lookup"><span data-stu-id="e8a45-131">The parameter contains too many characters.</span></span><br/>                                          |
| <dl> <span data-ttu-id="e8a45-132"><dt>VM \_ Nome de config & 0xA0040402 de \_ \_ \_ \_ caracteres inválido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e8a45-132"><dt>VM\_E\_CONFIG\_NAME\_INVALID\_CHAR</dt> <dt>0xA0040402</dt></span></span> </dl> | <span data-ttu-id="e8a45-133">O parâmetro contém um dos seguintes caracteres inválidos " \* ?: <>/ \| \\ " ".</span><span class="sxs-lookup"><span data-stu-id="e8a45-133">The parameter contains one of the following invalid characters "\*?:<>/\|\\"".</span></span><br/> |
| <dl> <span data-ttu-id="e8a45-134"><dt>VM \_ E \_ config \_ \_ nome duplicado</dt> <dt>0xA0040403</dt></span><span class="sxs-lookup"><span data-stu-id="e8a45-134"><dt>VM\_E\_CONFIG\_DUPLICATE\_NAME</dt> <dt>0xA0040403</dt></span></span> </dl>     | <span data-ttu-id="e8a45-135">O nome especificado já existe como o nome de outra máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e8a45-135">The specified name already exists as the name of another virtual machine.</span></span><br/>            |
| <dl> <span data-ttu-id="e8a45-136"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="e8a45-136"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                 | <span data-ttu-id="e8a45-137">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="e8a45-137">An unexpected error has occurred.</span></span><br/>                                                    |



## <a name="remarks"></a><span data-ttu-id="e8a45-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8a45-138">Remarks</span></span>

<span data-ttu-id="e8a45-139">Os nomes de máquina virtual não diferenciam maiúsculas de minúsculas, por exemplo, "MyVM" e "MyVM" referem-se à mesma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e8a45-139">Virtual machine names are case-insensitive, e.g. "MyVM" and "myvm" refer to the same virtual machine.</span></span> <span data-ttu-id="e8a45-140">Essa é a propriedade padrão para [**IVMVirtualMachine**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="e8a45-140">This is the default property for [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

<span data-ttu-id="e8a45-141">Se VPC.exe estiver em execução e a VM for salva, a definição da propriedade **Name** não terá sucesso.</span><span class="sxs-lookup"><span data-stu-id="e8a45-141">If VPC.exe is running and the VM is saved then setting the **Name** property will not succeed.</span></span> <span data-ttu-id="e8a45-142">Se VPC.exe não estiver em execução e a VM for salva, a configuração da propriedade **nome** terá sucesso quando VPC.exe for iniciado.</span><span class="sxs-lookup"><span data-stu-id="e8a45-142">If VPC.exe is not running and the VM is saved then setting the **Name** property will succeed when VPC.exe is next started.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8a45-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8a45-143">Requirements</span></span>



| <span data-ttu-id="e8a45-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8a45-144">Requirement</span></span> | <span data-ttu-id="e8a45-145">Valor</span><span class="sxs-lookup"><span data-stu-id="e8a45-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8a45-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8a45-146">Minimum supported client</span></span><br/> | <span data-ttu-id="e8a45-147">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e8a45-147">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e8a45-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8a45-148">Minimum supported server</span></span><br/> | <span data-ttu-id="e8a45-149">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e8a45-149">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e8a45-150">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="e8a45-150">End of client support</span></span><br/>    | <span data-ttu-id="e8a45-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e8a45-151">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e8a45-152">Produto</span><span class="sxs-lookup"><span data-stu-id="e8a45-152">Product</span></span><br/>                  | <span data-ttu-id="e8a45-153">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e8a45-153">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e8a45-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e8a45-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8a45-155"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8a45-155"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e8a45-156">IID</span><span class="sxs-lookup"><span data-stu-id="e8a45-156">IID</span></span><br/>                      | <span data-ttu-id="e8a45-157">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="e8a45-157">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="e8a45-158">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e8a45-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8a45-159">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="e8a45-159">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

