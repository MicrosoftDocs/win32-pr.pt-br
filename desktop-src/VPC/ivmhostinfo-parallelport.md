---
title: Propriedade IVMHostInfo ParallelPort (VPCCOMInterfaces. h)
description: Recupera a porta paralela do host que pode ser anexada ao convidado.
ms.assetid: 4c9486b8-ab66-4874-b467-a7a0ab7934f1
keywords:
- Propriedade ParallelPort Virtual PC
- Propriedade ParallelPort Virtual PC, interface IVMHostInfo
- IVMHostInfo interface virtual PC, Propriedade ParallelPort
topic_type:
- apiref
api_name:
- IVMHostInfo.ParallelPort
- IVMHostInfo.get_ParallelPort
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac0a2050ff505f5ed7a54cf3857ea28661d4d3d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499231"
---
# <a name="ivmhostinfoparallelport-property"></a><span data-ttu-id="40136-106">IVMHostInfo: Propriedade arallelPort de:P</span><span class="sxs-lookup"><span data-stu-id="40136-106">IVMHostInfo::ParallelPort property</span></span>

<span data-ttu-id="40136-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="40136-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="40136-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="40136-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="40136-109">Recupera a porta paralela do host que pode ser anexada ao convidado.</span><span class="sxs-lookup"><span data-stu-id="40136-109">Retrieves the host parallel port that can be attached to the guest.</span></span>

<span data-ttu-id="40136-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="40136-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="40136-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="40136-111">Syntax</span></span>


```C++
HRESULT get_ParallelPort(
  [out, retval] BSTR *vmParallelPort
);
```



## <a name="property-value"></a><span data-ttu-id="40136-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="40136-112">Property value</span></span>

<span data-ttu-id="40136-113">O nome da porta paralela.</span><span class="sxs-lookup"><span data-stu-id="40136-113">The name of the parallel port.</span></span>

## <a name="error-codes"></a><span data-ttu-id="40136-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="40136-114">Error codes</span></span>



| <span data-ttu-id="40136-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="40136-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="40136-116">Significado</span><span class="sxs-lookup"><span data-stu-id="40136-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="40136-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="40136-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="40136-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="40136-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="40136-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="40136-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="40136-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="40136-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="40136-121"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="40136-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="40136-122">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="40136-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="40136-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40136-123">Requirements</span></span>



| <span data-ttu-id="40136-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="40136-124">Requirement</span></span> | <span data-ttu-id="40136-125">Valor</span><span class="sxs-lookup"><span data-stu-id="40136-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="40136-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40136-126">Minimum supported client</span></span><br/> | <span data-ttu-id="40136-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="40136-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="40136-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40136-128">Minimum supported server</span></span><br/> | <span data-ttu-id="40136-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="40136-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="40136-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="40136-130">End of client support</span></span><br/>    | <span data-ttu-id="40136-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="40136-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="40136-132">Produto</span><span class="sxs-lookup"><span data-stu-id="40136-132">Product</span></span><br/>                  | <span data-ttu-id="40136-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="40136-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="40136-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="40136-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="40136-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="40136-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="40136-136">IID</span><span class="sxs-lookup"><span data-stu-id="40136-136">IID</span></span><br/>                      | <span data-ttu-id="40136-137">IID \_ IVMHostInfo é definido como 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="40136-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="40136-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="40136-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40136-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="40136-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

