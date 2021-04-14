---
title: Propriedade IVMHostInfo NetworkAddresses (VPCCOMInterfaces. h)
description: Recupera uma coleção enumerável de endereços TCP/IP no computador host.
ms.assetid: 94716b82-8f35-4702-873d-64507d879dc3
keywords:
- Propriedade NetworkAddresses Virtual PC
- Propriedade NetworkAddresses Virtual PC, interface IVMHostInfo
- IVMHostInfo interface virtual PC, Propriedade NetworkAddresses
topic_type:
- apiref
api_name:
- IVMHostInfo.NetworkAddresses
- IVMHostInfo.get_NetworkAddresses
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 824bedf8433c1025e1f4afc1e624c27606b8d0d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369196"
---
# <a name="ivmhostinfonetworkaddresses-property"></a><span data-ttu-id="06493-106">Propriedade IVMHostInfo:: NetworkAddresses</span><span class="sxs-lookup"><span data-stu-id="06493-106">IVMHostInfo::NetworkAddresses property</span></span>

<span data-ttu-id="06493-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="06493-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="06493-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="06493-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="06493-109">Recupera uma coleção enumerável de endereços TCP/IP no computador host.</span><span class="sxs-lookup"><span data-stu-id="06493-109">Retrieves an enumerable collection of TCP/IP addresses in the host machine.</span></span>

<span data-ttu-id="06493-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="06493-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="06493-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="06493-111">Syntax</span></span>


```C++
HRESULT get_NetworkAddresses(
  [out, retval] VARIANT *hostAddresses
);
```



## <a name="property-value"></a><span data-ttu-id="06493-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="06493-112">Property value</span></span>

<span data-ttu-id="06493-113">Uma matriz de endereços TCP/IP, em notação decimal pontilhada.</span><span class="sxs-lookup"><span data-stu-id="06493-113">An array of TCP/IP addresses, in dotted-decimal notation.</span></span>

## <a name="error-codes"></a><span data-ttu-id="06493-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="06493-114">Error codes</span></span>



| <span data-ttu-id="06493-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="06493-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="06493-116">Significado</span><span class="sxs-lookup"><span data-stu-id="06493-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="06493-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="06493-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="06493-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="06493-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="06493-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="06493-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="06493-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="06493-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="06493-121"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="06493-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="06493-122">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="06493-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="06493-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06493-123">Requirements</span></span>



| <span data-ttu-id="06493-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="06493-124">Requirement</span></span> | <span data-ttu-id="06493-125">Valor</span><span class="sxs-lookup"><span data-stu-id="06493-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="06493-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06493-126">Minimum supported client</span></span><br/> | <span data-ttu-id="06493-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="06493-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="06493-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06493-128">Minimum supported server</span></span><br/> | <span data-ttu-id="06493-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="06493-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="06493-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="06493-130">End of client support</span></span><br/>    | <span data-ttu-id="06493-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="06493-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="06493-132">Produto</span><span class="sxs-lookup"><span data-stu-id="06493-132">Product</span></span><br/>                  | <span data-ttu-id="06493-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="06493-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="06493-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="06493-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="06493-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="06493-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="06493-136">IID</span><span class="sxs-lookup"><span data-stu-id="06493-136">IID</span></span><br/>                      | <span data-ttu-id="06493-137">IID \_ IVMHostInfo é definido como 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="06493-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="06493-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="06493-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06493-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="06493-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

