---
title: Propriedade de arquivo IVMVirtualMachine (VPCCOMInterfaces. h)
description: Recupera o caminho totalmente qualificado do arquivo. VMC para a configuração da máquina virtual.
ms.assetid: fc215068-e908-417c-bd68-214539a0a14e
keywords:
- Propriedade de arquivo Virtual PC
- Propriedade de arquivo Virtual PC, interface IVMVirtualMachine
- Virtual PC interface IVMVirtualMachine, Propriedade File
topic_type:
- apiref
api_name:
- IVMVirtualMachine.File
- IVMVirtualMachine.get_File
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71ac3bc68d167a7057d76adc1ce84a29291b7c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644787"
---
# <a name="ivmvirtualmachinefile-property"></a><span data-ttu-id="dac80-106">Propriedade IVMVirtualMachine:: File</span><span class="sxs-lookup"><span data-stu-id="dac80-106">IVMVirtualMachine::File property</span></span>

<span data-ttu-id="dac80-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="dac80-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="dac80-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="dac80-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="dac80-109">Recupera o caminho totalmente qualificado do arquivo. VMC para a configuração da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dac80-109">Retrieves the fully qualified path of the .vmc file for the virtual machine configuration.</span></span>

<span data-ttu-id="dac80-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="dac80-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="dac80-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dac80-111">Syntax</span></span>


```C++
HRESULT get_File(
  [out, retval] BSTR *virtualMachineXMLFile
);
```



## <a name="property-value"></a><span data-ttu-id="dac80-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="dac80-112">Property value</span></span>

<span data-ttu-id="dac80-113">O nome totalmente qualificado do arquivo " \* . vmc" que descreve essa configuração de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dac80-113">The fully qualified name of the "\*.vmc" file that describes this virtual machine configuration.</span></span>

## <a name="error-codes"></a><span data-ttu-id="dac80-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="dac80-114">Error codes</span></span>



| <span data-ttu-id="dac80-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="dac80-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="dac80-116">Significado</span><span class="sxs-lookup"><span data-stu-id="dac80-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="dac80-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="dac80-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="dac80-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="dac80-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="dac80-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="dac80-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="dac80-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="dac80-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="dac80-121"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="dac80-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="dac80-122">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="dac80-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="dac80-123"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="dac80-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="dac80-124">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="dac80-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="dac80-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dac80-125">Requirements</span></span>



| <span data-ttu-id="dac80-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="dac80-126">Requirement</span></span> | <span data-ttu-id="dac80-127">Valor</span><span class="sxs-lookup"><span data-stu-id="dac80-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="dac80-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dac80-128">Minimum supported client</span></span><br/> | <span data-ttu-id="dac80-129">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="dac80-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dac80-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dac80-130">Minimum supported server</span></span><br/> | <span data-ttu-id="dac80-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="dac80-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="dac80-132">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="dac80-132">End of client support</span></span><br/>    | <span data-ttu-id="dac80-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="dac80-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="dac80-134">Produto</span><span class="sxs-lookup"><span data-stu-id="dac80-134">Product</span></span><br/>                  | <span data-ttu-id="dac80-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="dac80-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="dac80-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dac80-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="dac80-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="dac80-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="dac80-138">IID</span><span class="sxs-lookup"><span data-stu-id="dac80-138">IID</span></span><br/>                      | <span data-ttu-id="dac80-139">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="dac80-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="dac80-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="dac80-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dac80-141">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="dac80-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

