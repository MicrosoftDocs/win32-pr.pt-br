---
title: Propriedade IVMVirtualMachine adaptadores (VPCCOMInterfaces. h)
description: Recupera uma coleção enumerável de NICs anexadas à máquina virtual.
ms.assetid: 3877edf7-92b8-43c9-8229-a198a07079a4
keywords:
- Propriedade adaptadores Virtual PC
- Propriedade adaptadores Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, Propriedade adaptadores
topic_type:
- apiref
api_name:
- IVMVirtualMachine.NetworkAdapters
- IVMVirtualMachine.get_NetworkAdapters
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9ce6e1fa22eca40c037eebb48803fe182810c38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369685"
---
# <a name="ivmvirtualmachinenetworkadapters-property"></a><span data-ttu-id="da17f-106">Propriedade IVMVirtualMachine:: adaptadores</span><span class="sxs-lookup"><span data-stu-id="da17f-106">IVMVirtualMachine::NetworkAdapters property</span></span>

<span data-ttu-id="da17f-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="da17f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="da17f-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="da17f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="da17f-109">Recupera uma coleção enumerável de NICs anexadas à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="da17f-109">Retrieves an enumerable collection of NICs attached to the virtual machine.</span></span>

<span data-ttu-id="da17f-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="da17f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="da17f-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="da17f-111">Syntax</span></span>


```C++
HRESULT get_NetworkAdapters(
  [out, retval] IVMNetworkAdapterCollection **networkAdapterCollection
);
```



## <a name="property-value"></a><span data-ttu-id="da17f-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="da17f-112">Property value</span></span>

<span data-ttu-id="da17f-113">Um objeto [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md) .</span><span class="sxs-lookup"><span data-stu-id="da17f-113">An [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="da17f-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="da17f-114">Error codes</span></span>



| <span data-ttu-id="da17f-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="da17f-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="da17f-116">Significado</span><span class="sxs-lookup"><span data-stu-id="da17f-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="da17f-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="da17f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="da17f-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="da17f-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="da17f-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="da17f-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="da17f-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="da17f-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="da17f-121"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="da17f-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="da17f-122">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="da17f-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="da17f-123"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="da17f-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="da17f-124">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="da17f-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="da17f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da17f-125">Requirements</span></span>



| <span data-ttu-id="da17f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="da17f-126">Requirement</span></span> | <span data-ttu-id="da17f-127">Valor</span><span class="sxs-lookup"><span data-stu-id="da17f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="da17f-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da17f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="da17f-129">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="da17f-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="da17f-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da17f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="da17f-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="da17f-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="da17f-132">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="da17f-132">End of client support</span></span><br/>    | <span data-ttu-id="da17f-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="da17f-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="da17f-134">Produto</span><span class="sxs-lookup"><span data-stu-id="da17f-134">Product</span></span><br/>                  | <span data-ttu-id="da17f-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="da17f-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="da17f-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="da17f-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="da17f-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="da17f-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="da17f-138">IID</span><span class="sxs-lookup"><span data-stu-id="da17f-138">IID</span></span><br/>                      | <span data-ttu-id="da17f-139">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="da17f-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="da17f-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="da17f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da17f-141">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="da17f-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

