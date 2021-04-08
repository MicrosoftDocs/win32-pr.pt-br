---
title: Propriedade IVMNetworkAdapter VirtualMachine (VPCCOMInterfaces. h)
description: Recupera a máquina virtual associada a esta interface de rede.
ms.assetid: a3519041-0081-44e7-aa76-760d59ca8587
keywords:
- Propriedade VirtualMachine Virtual PC
- Propriedade VirtualMachine Virtual PC, interface IVMNetworkAdapter
- IVMNetworkAdapter interface virtual PC, Propriedade VirtualMachine
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.VirtualMachine
- IVMNetworkAdapter.get_VirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea50e43bdcffcd16f668ef596a0f9db9d9bccfe2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008807"
---
# <a name="ivmnetworkadaptervirtualmachine-property"></a><span data-ttu-id="e475e-106">Propriedade IVMNetworkAdapter:: VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e475e-106">IVMNetworkAdapter::VirtualMachine property</span></span>

<span data-ttu-id="e475e-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e475e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e475e-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e475e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e475e-109">Recupera a máquina virtual associada a esta interface de rede.</span><span class="sxs-lookup"><span data-stu-id="e475e-109">Retrieves the virtual machine associated with this network interface.</span></span>

<span data-ttu-id="e475e-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="e475e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e475e-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e475e-111">Syntax</span></span>


```C++
HRESULT get_VirtualMachine(
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="property-value"></a><span data-ttu-id="e475e-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e475e-112">Property value</span></span>

<span data-ttu-id="e475e-113">Uma interface [**IVMVirtualMachine**](ivmvirtualmachine.md) que representa a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e475e-113">An [**IVMVirtualMachine**](ivmvirtualmachine.md) interface that represents the virtual machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e475e-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="e475e-114">Error codes</span></span>



| <span data-ttu-id="e475e-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="e475e-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="e475e-116">Significado</span><span class="sxs-lookup"><span data-stu-id="e475e-116">Meaning</span></span>                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="e475e-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e475e-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="e475e-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e475e-118">The operation was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="e475e-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="e475e-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="e475e-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e475e-120">The parameter is **NULL**.</span></span><br/>           |
| <dl> <span data-ttu-id="e475e-121"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e475e-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="e475e-122">Não é possível encontrar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e475e-122">The virtual machine cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="e475e-123"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="e475e-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="e475e-124">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="e475e-124">An unexpected error has occurred.</span></span><br/>    |



## <a name="requirements"></a><span data-ttu-id="e475e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e475e-125">Requirements</span></span>



| <span data-ttu-id="e475e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e475e-126">Requirement</span></span> | <span data-ttu-id="e475e-127">Valor</span><span class="sxs-lookup"><span data-stu-id="e475e-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e475e-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e475e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e475e-129">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e475e-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e475e-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e475e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e475e-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e475e-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e475e-132">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="e475e-132">End of client support</span></span><br/>    | <span data-ttu-id="e475e-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e475e-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e475e-134">Produto</span><span class="sxs-lookup"><span data-stu-id="e475e-134">Product</span></span><br/>                  | <span data-ttu-id="e475e-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e475e-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e475e-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e475e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="e475e-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e475e-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e475e-138">IID</span><span class="sxs-lookup"><span data-stu-id="e475e-138">IID</span></span><br/>                      | <span data-ttu-id="e475e-139">IID \_ IVMNetworkAdapter é definido como e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="e475e-139">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="e475e-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="e475e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e475e-141">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="e475e-141">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

