---
title: Propriedade IVMVirtualPC HostInfo (VPCCOMInterfaces. h)
description: Recupera informações sobre o computador físico.
ms.assetid: 9efefea1-e608-48db-a91a-e3808b420fc2
keywords:
- Propriedade HostInfo Virtual PC
- Propriedade HostInfo Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, Propriedade HostInfo
topic_type:
- apiref
api_name:
- IVMVirtualPC.HostInfo
- IVMVirtualPC.get_HostInfo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 351da69a19fd691b037a607a57136576e3b64011
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086061"
---
# <a name="ivmvirtualpchostinfo-property"></a><span data-ttu-id="45cf1-106">Propriedade IVMVirtualPC:: HostInfo</span><span class="sxs-lookup"><span data-stu-id="45cf1-106">IVMVirtualPC::HostInfo property</span></span>

<span data-ttu-id="45cf1-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="45cf1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="45cf1-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="45cf1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="45cf1-109">Recupera informações sobre o computador físico.</span><span class="sxs-lookup"><span data-stu-id="45cf1-109">Retrieves information about the physical computer.</span></span>

<span data-ttu-id="45cf1-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="45cf1-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="45cf1-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45cf1-111">Syntax</span></span>


```C++
HRESULT get_HostInfo(
  [out, retval] IVMHostInfo **hostInfo
);
```



## <a name="property-value"></a><span data-ttu-id="45cf1-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="45cf1-112">Property value</span></span>

<span data-ttu-id="45cf1-113">O objeto [**IVMHostInfo**](ivmhostinfo.md) que contém informações sobre o computador host.</span><span class="sxs-lookup"><span data-stu-id="45cf1-113">The [**IVMHostInfo**](ivmhostinfo.md) object containing information about the host machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="45cf1-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="45cf1-114">Error codes</span></span>



| <span data-ttu-id="45cf1-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="45cf1-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="45cf1-116">Significado</span><span class="sxs-lookup"><span data-stu-id="45cf1-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="45cf1-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="45cf1-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="45cf1-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="45cf1-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="45cf1-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="45cf1-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="45cf1-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="45cf1-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="45cf1-121"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="45cf1-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="45cf1-122">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="45cf1-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="45cf1-123"><dt>VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="45cf1-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="45cf1-124">O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).</span><span class="sxs-lookup"><span data-stu-id="45cf1-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="45cf1-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45cf1-125">Requirements</span></span>



| <span data-ttu-id="45cf1-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="45cf1-126">Requirement</span></span> | <span data-ttu-id="45cf1-127">Valor</span><span class="sxs-lookup"><span data-stu-id="45cf1-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="45cf1-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45cf1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="45cf1-129">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="45cf1-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="45cf1-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45cf1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="45cf1-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="45cf1-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="45cf1-132">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="45cf1-132">End of client support</span></span><br/>    | <span data-ttu-id="45cf1-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="45cf1-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="45cf1-134">Produto</span><span class="sxs-lookup"><span data-stu-id="45cf1-134">Product</span></span><br/>                  | <span data-ttu-id="45cf1-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="45cf1-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="45cf1-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="45cf1-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="45cf1-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="45cf1-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="45cf1-138">IID</span><span class="sxs-lookup"><span data-stu-id="45cf1-138">IID</span></span><br/>                      | <span data-ttu-id="45cf1-139">IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="45cf1-139">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="45cf1-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="45cf1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45cf1-141">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="45cf1-141">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

