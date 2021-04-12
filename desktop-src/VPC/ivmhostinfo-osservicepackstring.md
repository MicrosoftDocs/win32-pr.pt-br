---
title: Propriedade IVMHostInfo OSServicePackString (VPCCOMInterfaces. h)
description: Recupera as informações de service pack do sistema operacional em execução no computador host.
ms.assetid: e5fe51f8-9bcf-49bd-bec6-2538b3e8edfa
keywords:
- Propriedade OSServicePackString Virtual PC
- Propriedade OSServicePackString Virtual PC, interface IVMHostInfo
- IVMHostInfo interface virtual PC, Propriedade OSServicePackString
topic_type:
- apiref
api_name:
- IVMHostInfo.OSServicePackString
- IVMHostInfo.get_OSServicePackString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a046499b72333b4acf8daffbd66dbab44107e0b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294749"
---
# <a name="ivmhostinfoosservicepackstring-property"></a><span data-ttu-id="3eb55-106">Propriedade IVMHostInfo:: OSServicePackString</span><span class="sxs-lookup"><span data-stu-id="3eb55-106">IVMHostInfo::OSServicePackString property</span></span>

<span data-ttu-id="3eb55-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3eb55-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3eb55-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3eb55-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3eb55-109">Recupera as informações de service pack do sistema operacional em execução no computador host.</span><span class="sxs-lookup"><span data-stu-id="3eb55-109">Retrieves the service pack information of the operating system running on the host machine.</span></span>

<span data-ttu-id="3eb55-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="3eb55-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3eb55-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3eb55-111">Syntax</span></span>


```C++
HRESULT get_OSServicePackString(
  [out, retval] BSTR *OSServicePack
);
```



## <a name="property-value"></a><span data-ttu-id="3eb55-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3eb55-112">Property value</span></span>

<span data-ttu-id="3eb55-113">A versão service pack.</span><span class="sxs-lookup"><span data-stu-id="3eb55-113">The service pack version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3eb55-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="3eb55-114">Error codes</span></span>



| <span data-ttu-id="3eb55-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="3eb55-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="3eb55-116">Significado</span><span class="sxs-lookup"><span data-stu-id="3eb55-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="3eb55-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3eb55-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="3eb55-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="3eb55-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="3eb55-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="3eb55-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="3eb55-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="3eb55-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="3eb55-121"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="3eb55-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="3eb55-122">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="3eb55-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="3eb55-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3eb55-123">Requirements</span></span>



| <span data-ttu-id="3eb55-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3eb55-124">Requirement</span></span> | <span data-ttu-id="3eb55-125">Valor</span><span class="sxs-lookup"><span data-stu-id="3eb55-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3eb55-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3eb55-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3eb55-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3eb55-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3eb55-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3eb55-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3eb55-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3eb55-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3eb55-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="3eb55-130">End of client support</span></span><br/>    | <span data-ttu-id="3eb55-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3eb55-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3eb55-132">Produto</span><span class="sxs-lookup"><span data-stu-id="3eb55-132">Product</span></span><br/>                  | <span data-ttu-id="3eb55-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3eb55-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3eb55-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3eb55-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="3eb55-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3eb55-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3eb55-136">IID</span><span class="sxs-lookup"><span data-stu-id="3eb55-136">IID</span></span><br/>                      | <span data-ttu-id="3eb55-137">IID \_ IVMHostInfo é definido como 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="3eb55-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="3eb55-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="3eb55-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3eb55-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="3eb55-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

