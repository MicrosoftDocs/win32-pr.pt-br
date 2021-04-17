---
title: Propriedade IVMHostInfo OperatingSystem (VPCCOMInterfaces. h)
description: Recupera o sistema operacional em execução no computador.
ms.assetid: 1164bb7d-cdce-4649-86d6-22e3ea7bad98
keywords:
- PC virtual da Propriedade OperatingSystem
- Propriedade OperatingSystem Virtual PC, interface IVMHostInfo
- Interface IVMHostInfo Virtual PC, Propriedade OperatingSystem
topic_type:
- apiref
api_name:
- IVMHostInfo.OperatingSystem
- IVMHostInfo.get_OperatingSystem
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55af1d0cfdc2abaa01fe78c08509c2448b4d8cc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105813254"
---
# <a name="ivmhostinfooperatingsystem-property"></a><span data-ttu-id="4297f-106">Propriedade IVMHostInfo:: OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="4297f-106">IVMHostInfo::OperatingSystem property</span></span>

<span data-ttu-id="4297f-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4297f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4297f-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4297f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4297f-109">Recupera o sistema operacional em execução no computador.</span><span class="sxs-lookup"><span data-stu-id="4297f-109">Retrieves the operating system running on the machine.</span></span>

<span data-ttu-id="4297f-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="4297f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4297f-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4297f-111">Syntax</span></span>


```C++
HRESULT get_OperatingSystem(
  [out, retval] BSTR *operatingSystem
);
```



## <a name="property-value"></a><span data-ttu-id="4297f-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4297f-112">Property value</span></span>

<span data-ttu-id="4297f-113">O nome do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="4297f-113">The name of the operating system.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4297f-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="4297f-114">Error codes</span></span>



| <span data-ttu-id="4297f-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="4297f-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="4297f-116">Significado</span><span class="sxs-lookup"><span data-stu-id="4297f-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="4297f-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4297f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="4297f-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4297f-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="4297f-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="4297f-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="4297f-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4297f-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="4297f-121"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="4297f-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="4297f-122">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="4297f-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="4297f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4297f-123">Requirements</span></span>



| <span data-ttu-id="4297f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4297f-124">Requirement</span></span> | <span data-ttu-id="4297f-125">Valor</span><span class="sxs-lookup"><span data-stu-id="4297f-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4297f-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4297f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4297f-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4297f-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4297f-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4297f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4297f-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4297f-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4297f-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="4297f-130">End of client support</span></span><br/>    | <span data-ttu-id="4297f-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4297f-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4297f-132">Produto</span><span class="sxs-lookup"><span data-stu-id="4297f-132">Product</span></span><br/>                  | <span data-ttu-id="4297f-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4297f-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4297f-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4297f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="4297f-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4297f-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4297f-136">IID</span><span class="sxs-lookup"><span data-stu-id="4297f-136">IID</span></span><br/>                      | <span data-ttu-id="4297f-137">IID \_ IVMHostInfo é definido como 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="4297f-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="4297f-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="4297f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4297f-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="4297f-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

