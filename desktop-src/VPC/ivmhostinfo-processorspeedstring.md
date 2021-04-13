---
title: Propriedade IVMHostInfo ProcessorSpeedString (VPCCOMInterfaces. h)
description: Velocidade do processador do host, em megahertz (MHz) ou gigahertz (GHz), como uma cadeia de caracteres.
ms.assetid: 1a4a42bf-b7aa-4eec-8df5-1820aac82de3
keywords:
- Propriedade ProcessorSpeedString Virtual PC
- Propriedade ProcessorSpeedString Virtual PC, interface IVMHostInfo
- IVMHostInfo interface virtual PC, Propriedade ProcessorSpeedString
topic_type:
- apiref
api_name:
- IVMHostInfo.ProcessorSpeedString
- IVMHostInfo.get_ProcessorSpeedString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c91b8cb19baef62275954f0c1d9f6475c5b4817f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455841"
---
# <a name="ivmhostinfoprocessorspeedstring-property"></a><span data-ttu-id="06df8-106">IVMHostInfo: Propriedade rocessorSpeedString de:P</span><span class="sxs-lookup"><span data-stu-id="06df8-106">IVMHostInfo::ProcessorSpeedString property</span></span>

<span data-ttu-id="06df8-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="06df8-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="06df8-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="06df8-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="06df8-109">Recupera a velocidade do processador do host, em megahertz (MHz) ou gigahertz (GHz), como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="06df8-109">Retrieves the speed of the host processor, in megahertz (MHz) or gigahertz (GHz), as a string.</span></span>

<span data-ttu-id="06df8-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="06df8-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="06df8-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="06df8-111">Syntax</span></span>


```C++
HRESULT get_ProcessorSpeedString(
  [out, retval] BSTR *processorSpeedString
);
```



## <a name="property-value"></a><span data-ttu-id="06df8-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="06df8-112">Property value</span></span>

<span data-ttu-id="06df8-113">A velocidade do processador, em megahertz ou gigahertz.</span><span class="sxs-lookup"><span data-stu-id="06df8-113">The processor speed, in megahertz or gigahertz.</span></span>

## <a name="error-codes"></a><span data-ttu-id="06df8-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="06df8-114">Error codes</span></span>



| <span data-ttu-id="06df8-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="06df8-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="06df8-116">Significado</span><span class="sxs-lookup"><span data-stu-id="06df8-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="06df8-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="06df8-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="06df8-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="06df8-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="06df8-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="06df8-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="06df8-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="06df8-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="06df8-121"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="06df8-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="06df8-122">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="06df8-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="06df8-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06df8-123">Requirements</span></span>



| <span data-ttu-id="06df8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="06df8-124">Requirement</span></span> | <span data-ttu-id="06df8-125">Valor</span><span class="sxs-lookup"><span data-stu-id="06df8-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="06df8-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06df8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="06df8-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="06df8-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="06df8-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06df8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="06df8-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="06df8-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="06df8-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="06df8-130">End of client support</span></span><br/>    | <span data-ttu-id="06df8-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="06df8-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="06df8-132">Produto</span><span class="sxs-lookup"><span data-stu-id="06df8-132">Product</span></span><br/>                  | <span data-ttu-id="06df8-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="06df8-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="06df8-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="06df8-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="06df8-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="06df8-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="06df8-136">IID</span><span class="sxs-lookup"><span data-stu-id="06df8-136">IID</span></span><br/>                      | <span data-ttu-id="06df8-137">IID \_ IVMHostInfo é definido como 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="06df8-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="06df8-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="06df8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06df8-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="06df8-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

