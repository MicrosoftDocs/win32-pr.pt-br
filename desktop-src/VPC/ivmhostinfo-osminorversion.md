---
title: Propriedade IVMHostInfo OSMinorVersion (VPCCOMInterfaces. h)
description: Recupera a versão secundária do sistema operacional em execução no computador host.
ms.assetid: 12f3ac59-ab7d-40f6-a0e6-fb870d2dff16
keywords:
- Propriedade OSMinorVersion Virtual PC
- Propriedade OSMinorVersion Virtual PC, interface IVMHostInfo
- IVMHostInfo interface virtual PC, Propriedade OSMinorVersion
topic_type:
- apiref
api_name:
- IVMHostInfo.OSMinorVersion
- IVMHostInfo.get_OSMinorVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3063a752886ebd196f1462ce67572fe62d032f4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085130"
---
# <a name="ivmhostinfoosminorversion-property"></a><span data-ttu-id="f5fec-106">Propriedade IVMHostInfo:: OSMinorVersion</span><span class="sxs-lookup"><span data-stu-id="f5fec-106">IVMHostInfo::OSMinorVersion property</span></span>

<span data-ttu-id="f5fec-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f5fec-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f5fec-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f5fec-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f5fec-109">Recupera a versão secundária do sistema operacional em execução no computador host.</span><span class="sxs-lookup"><span data-stu-id="f5fec-109">Retrieves the minor version of the operating system running on the host machine.</span></span>

<span data-ttu-id="f5fec-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="f5fec-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5fec-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5fec-111">Syntax</span></span>


```C++
HRESULT get_OSMinorVersion(
  [out, retval] long *osMinorVersion
);
```



## <a name="property-value"></a><span data-ttu-id="f5fec-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f5fec-112">Property value</span></span>

<span data-ttu-id="f5fec-113">A versão secundária.</span><span class="sxs-lookup"><span data-stu-id="f5fec-113">The minor version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f5fec-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="f5fec-114">Error codes</span></span>



| <span data-ttu-id="f5fec-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="f5fec-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="f5fec-116">Significado</span><span class="sxs-lookup"><span data-stu-id="f5fec-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="f5fec-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f5fec-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="f5fec-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f5fec-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="f5fec-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="f5fec-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="f5fec-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="f5fec-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="f5fec-121"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="f5fec-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="f5fec-122">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="f5fec-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f5fec-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5fec-123">Requirements</span></span>



| <span data-ttu-id="f5fec-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5fec-124">Requirement</span></span> | <span data-ttu-id="f5fec-125">Valor</span><span class="sxs-lookup"><span data-stu-id="f5fec-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5fec-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5fec-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f5fec-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f5fec-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f5fec-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5fec-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f5fec-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f5fec-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f5fec-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="f5fec-130">End of client support</span></span><br/>    | <span data-ttu-id="f5fec-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f5fec-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f5fec-132">Produto</span><span class="sxs-lookup"><span data-stu-id="f5fec-132">Product</span></span><br/>                  | <span data-ttu-id="f5fec-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f5fec-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f5fec-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f5fec-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5fec-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5fec-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f5fec-136">IID</span><span class="sxs-lookup"><span data-stu-id="f5fec-136">IID</span></span><br/>                      | <span data-ttu-id="f5fec-137">IID \_ IVMHostInfo é definido como 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="f5fec-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="f5fec-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5fec-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5fec-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="f5fec-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

