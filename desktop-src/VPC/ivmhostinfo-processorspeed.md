---
title: Propriedade IVMHostInfo ProcessorSpeed (VPCCOMInterfaces. h)
description: Velocidade do processador do host, em megahertz (MHz) ou gigahertz (GHz).
ms.assetid: 2d5e3f2e-8e81-4527-bd7f-52bf5b1f56ef
keywords:
- Propriedade ProcessorSpeed Virtual PC
- Propriedade ProcessorSpeed Virtual PC, interface IVMHostInfo
- IVMHostInfo interface virtual PC, Propriedade ProcessorSpeed
topic_type:
- apiref
api_name:
- IVMHostInfo.ProcessorSpeed
- IVMHostInfo.get_ProcessorSpeed
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28fc890392db5f61a7819fa1d4b4a11d2b3de312
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008813"
---
# <a name="ivmhostinfoprocessorspeed-property"></a><span data-ttu-id="1ae5f-106">IVMHostInfo: Propriedade rocessorSpeed de:P</span><span class="sxs-lookup"><span data-stu-id="1ae5f-106">IVMHostInfo::ProcessorSpeed property</span></span>

<span data-ttu-id="1ae5f-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1ae5f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1ae5f-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1ae5f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1ae5f-109">Recupera a velocidade do processador do host, em megahertz (MHz) ou gigahertz (GHz).</span><span class="sxs-lookup"><span data-stu-id="1ae5f-109">Retrieves the speed of the host processor, in megahertz (MHz) or gigahertz (GHz).</span></span>

<span data-ttu-id="1ae5f-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="1ae5f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ae5f-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ae5f-111">Syntax</span></span>


```C++
HRESULT get_ProcessorSpeed(
  [out, retval] long *processorSpeed
);
```



## <a name="property-value"></a><span data-ttu-id="1ae5f-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="1ae5f-112">Property value</span></span>

<span data-ttu-id="1ae5f-113">A velocidade do processador, em megahertz ou gigahertz.</span><span class="sxs-lookup"><span data-stu-id="1ae5f-113">The processor speed, in megahertz or gigahertz.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1ae5f-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="1ae5f-114">Error codes</span></span>



| <span data-ttu-id="1ae5f-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="1ae5f-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="1ae5f-116">Significado</span><span class="sxs-lookup"><span data-stu-id="1ae5f-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="1ae5f-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1ae5f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="1ae5f-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="1ae5f-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="1ae5f-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="1ae5f-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="1ae5f-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="1ae5f-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="1ae5f-121"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="1ae5f-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="1ae5f-122">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="1ae5f-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="1ae5f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ae5f-123">Requirements</span></span>



| <span data-ttu-id="1ae5f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ae5f-124">Requirement</span></span> | <span data-ttu-id="1ae5f-125">Valor</span><span class="sxs-lookup"><span data-stu-id="1ae5f-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ae5f-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ae5f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1ae5f-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="1ae5f-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1ae5f-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ae5f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1ae5f-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1ae5f-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1ae5f-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="1ae5f-130">End of client support</span></span><br/>    | <span data-ttu-id="1ae5f-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1ae5f-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1ae5f-132">Produto</span><span class="sxs-lookup"><span data-stu-id="1ae5f-132">Product</span></span><br/>                  | <span data-ttu-id="1ae5f-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1ae5f-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1ae5f-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1ae5f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ae5f-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ae5f-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1ae5f-136">IID</span><span class="sxs-lookup"><span data-stu-id="1ae5f-136">IID</span></span><br/>                      | <span data-ttu-id="1ae5f-137">IID \_ IVMHostInfo é definido como 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="1ae5f-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="1ae5f-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ae5f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ae5f-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="1ae5f-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

