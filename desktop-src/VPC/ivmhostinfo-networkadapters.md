---
title: Propriedade IVMHostInfo adaptadores (VPCCOMInterfaces. h)
description: Recupera uma coleção enumerável de NICs no computador host.
ms.assetid: 17393d7a-c883-4d67-826b-83b886c0d7a6
keywords:
- Propriedade adaptadores Virtual PC
- Propriedade adaptadores Virtual PC, interface IVMHostInfo
- IVMHostInfo interface virtual PC, Propriedade adaptadores
topic_type:
- apiref
api_name:
- IVMHostInfo.NetworkAdapters
- IVMHostInfo.get_NetworkAdapters
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eeff5c6d459fb8f6999f896c3c13fcd980bf70ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917954"
---
# <a name="ivmhostinfonetworkadapters-property"></a><span data-ttu-id="3e7ad-106">Propriedade IVMHostInfo:: adaptadores</span><span class="sxs-lookup"><span data-stu-id="3e7ad-106">IVMHostInfo::NetworkAdapters property</span></span>

<span data-ttu-id="3e7ad-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3e7ad-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3e7ad-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3e7ad-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3e7ad-109">Recupera uma coleção enumerável de NICs no computador host.</span><span class="sxs-lookup"><span data-stu-id="3e7ad-109">Retrieves an enumerable collection of NICs in the host machine.</span></span>

<span data-ttu-id="3e7ad-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="3e7ad-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e7ad-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e7ad-111">Syntax</span></span>


```C++
HRESULT get_NetworkAdapters(
  [out, retval] VARIANT *hostNICs
);
```



## <a name="property-value"></a><span data-ttu-id="3e7ad-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3e7ad-112">Property value</span></span>

<span data-ttu-id="3e7ad-113">Uma coleção de placas de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="3e7ad-113">A collection of network interface cards.</span></span> <span data-ttu-id="3e7ad-114">Esta é uma matriz de valores **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="3e7ad-114">This is an array of **BSTR** values.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3e7ad-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="3e7ad-115">Error codes</span></span>



| <span data-ttu-id="3e7ad-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="3e7ad-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="3e7ad-117">Significado</span><span class="sxs-lookup"><span data-stu-id="3e7ad-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="3e7ad-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3e7ad-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="3e7ad-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="3e7ad-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="3e7ad-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="3e7ad-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="3e7ad-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="3e7ad-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="3e7ad-122"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="3e7ad-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="3e7ad-123">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="3e7ad-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="3e7ad-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e7ad-124">Requirements</span></span>



| <span data-ttu-id="3e7ad-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e7ad-125">Requirement</span></span> | <span data-ttu-id="3e7ad-126">Valor</span><span class="sxs-lookup"><span data-stu-id="3e7ad-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e7ad-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e7ad-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3e7ad-128">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3e7ad-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3e7ad-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e7ad-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3e7ad-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3e7ad-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3e7ad-131">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="3e7ad-131">End of client support</span></span><br/>    | <span data-ttu-id="3e7ad-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3e7ad-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3e7ad-133">Produto</span><span class="sxs-lookup"><span data-stu-id="3e7ad-133">Product</span></span><br/>                  | <span data-ttu-id="3e7ad-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3e7ad-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3e7ad-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3e7ad-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e7ad-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e7ad-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3e7ad-137">IID</span><span class="sxs-lookup"><span data-stu-id="3e7ad-137">IID</span></span><br/>                      | <span data-ttu-id="3e7ad-138">IID \_ IVMHostInfo é definido como 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="3e7ad-138">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="3e7ad-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e7ad-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e7ad-140">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="3e7ad-140">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

