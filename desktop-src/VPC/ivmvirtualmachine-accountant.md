---
title: Propriedade de contador de IVMVirtualMachine (VPCCOMInterfaces. h)
description: Recupera um contador para esta máquina virtual.
ms.assetid: 5e512b83-8630-46ee-b521-c8a8193727f5
keywords:
- Propriedade do contador Virtual PC
- Propriedade de contador Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, Propriedade do contador
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Accountant
- IVMVirtualMachine.get_Accountant
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af1212de041b1d4c5bda59b9b12ab1d715be67cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086344"
---
# <a name="ivmvirtualmachineaccountant-property"></a><span data-ttu-id="a5ef8-106">Propriedade IVMVirtualMachine:: contador</span><span class="sxs-lookup"><span data-stu-id="a5ef8-106">IVMVirtualMachine::Accountant property</span></span>

<span data-ttu-id="a5ef8-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a5ef8-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a5ef8-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a5ef8-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a5ef8-109">Recupera um contador para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a5ef8-109">Retrieves an accountant for this virtual machine.</span></span>

<span data-ttu-id="a5ef8-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="a5ef8-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5ef8-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a5ef8-111">Syntax</span></span>


```C++
HRESULT get_Accountant(
  [out, retval] IVMAccountant **accountant
);
```



## <a name="property-value"></a><span data-ttu-id="a5ef8-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a5ef8-112">Property value</span></span>

<span data-ttu-id="a5ef8-113">O objeto [**IVMAccountant**](ivmaccountant.md) .</span><span class="sxs-lookup"><span data-stu-id="a5ef8-113">The [**IVMAccountant**](ivmaccountant.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a5ef8-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="a5ef8-114">Error codes</span></span>



| <span data-ttu-id="a5ef8-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="a5ef8-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="a5ef8-116">Significado</span><span class="sxs-lookup"><span data-stu-id="a5ef8-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a5ef8-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a5ef8-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="a5ef8-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="a5ef8-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="a5ef8-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="a5ef8-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="a5ef8-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a5ef8-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="a5ef8-121"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a5ef8-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="a5ef8-122">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="a5ef8-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="a5ef8-123"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="a5ef8-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="a5ef8-124">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="a5ef8-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a5ef8-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5ef8-125">Requirements</span></span>



| <span data-ttu-id="a5ef8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5ef8-126">Requirement</span></span> | <span data-ttu-id="a5ef8-127">Valor</span><span class="sxs-lookup"><span data-stu-id="a5ef8-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5ef8-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5ef8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a5ef8-129">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a5ef8-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a5ef8-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5ef8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a5ef8-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a5ef8-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a5ef8-132">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="a5ef8-132">End of client support</span></span><br/>    | <span data-ttu-id="a5ef8-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a5ef8-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a5ef8-134">Produto</span><span class="sxs-lookup"><span data-stu-id="a5ef8-134">Product</span></span><br/>                  | <span data-ttu-id="a5ef8-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a5ef8-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a5ef8-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a5ef8-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5ef8-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5ef8-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a5ef8-138">IID</span><span class="sxs-lookup"><span data-stu-id="a5ef8-138">IID</span></span><br/>                      | <span data-ttu-id="a5ef8-139">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="a5ef8-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="a5ef8-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5ef8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5ef8-141">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="a5ef8-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

