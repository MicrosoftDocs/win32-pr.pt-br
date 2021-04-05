---
title: Propriedade IVMVirtualPC MaximumNetworkAdaptersPerVM (VPCCOMInterfaces. h)
description: Número máximo de interfaces de rede por máquina virtual.
ms.assetid: 92da4958-5a67-422e-a6bd-68cabf1835ab
keywords:
- Propriedade MaximumNetworkAdaptersPerVM Virtual PC
- Propriedade MaximumNetworkAdaptersPerVM Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, Propriedade MaximumNetworkAdaptersPerVM
topic_type:
- apiref
api_name:
- IVMVirtualPC.MaximumNetworkAdaptersPerVM
- IVMVirtualPC.get_MaximumNetworkAdaptersPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0797775038440c566fa7a3397b05632af839a341
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085120"
---
# <a name="ivmvirtualpcmaximumnetworkadapterspervm-property"></a><span data-ttu-id="d478e-106">Propriedade IVMVirtualPC:: MaximumNetworkAdaptersPerVM</span><span class="sxs-lookup"><span data-stu-id="d478e-106">IVMVirtualPC::MaximumNetworkAdaptersPerVM property</span></span>

<span data-ttu-id="d478e-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d478e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d478e-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d478e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d478e-109">Recupera o número máximo de interfaces de rede por máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d478e-109">Retrieves the maximum number of networks interfaces per virtual machine.</span></span>

<span data-ttu-id="d478e-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="d478e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d478e-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d478e-111">Syntax</span></span>


```C++
HRESULT get_MaximumNetworkAdaptersPerVM(
  [out, retval] long *maxNetworkAdapters
);
```



## <a name="property-value"></a><span data-ttu-id="d478e-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d478e-112">Property value</span></span>

<span data-ttu-id="d478e-113">O número máximo de interfaces de rede por máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d478e-113">The maximum number of network interfaces per virtual machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d478e-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="d478e-114">Error codes</span></span>



| <span data-ttu-id="d478e-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="d478e-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="d478e-116">Significado</span><span class="sxs-lookup"><span data-stu-id="d478e-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d478e-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d478e-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="d478e-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d478e-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="d478e-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="d478e-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="d478e-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d478e-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="d478e-121"><dt>VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d478e-121"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="d478e-122">O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).</span><span class="sxs-lookup"><span data-stu-id="d478e-122">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d478e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d478e-123">Requirements</span></span>



| <span data-ttu-id="d478e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d478e-124">Requirement</span></span> | <span data-ttu-id="d478e-125">Valor</span><span class="sxs-lookup"><span data-stu-id="d478e-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d478e-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d478e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d478e-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d478e-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d478e-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d478e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d478e-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d478e-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d478e-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="d478e-130">End of client support</span></span><br/>    | <span data-ttu-id="d478e-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d478e-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d478e-132">Produto</span><span class="sxs-lookup"><span data-stu-id="d478e-132">Product</span></span><br/>                  | <span data-ttu-id="d478e-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d478e-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d478e-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d478e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d478e-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d478e-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d478e-136">IID</span><span class="sxs-lookup"><span data-stu-id="d478e-136">IID</span></span><br/>                      | <span data-ttu-id="d478e-137">IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="d478e-137">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="d478e-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="d478e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d478e-139">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="d478e-139">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

