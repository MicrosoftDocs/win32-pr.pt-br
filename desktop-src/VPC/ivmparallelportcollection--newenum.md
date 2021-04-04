---
title: Propriedade _NewEnum IVMParallelPortCollection (VPCCOMInterfaces. h)
description: Recupera um enumerador para a coleção. | Propriedade _NewEnum IVMParallelPortCollection (VPCCOMInterfaces. h)
ms.assetid: 2e26fba7-bcc0-4bb3-bf89-3c62cbd2b37e
keywords:
- _NewEnum a propriedade Virtual PC
- Propriedade _NewEnum Virtual PC, interface IVMParallelPortCollection
- IVMParallelPortCollection interface virtual PC, Propriedade _NewEnum
topic_type:
- apiref
api_name:
- IVMParallelPortCollection._NewEnum
- IVMParallelPortCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de7b0a7330e38abaa604c84c2b703bd5d908619a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930276"
---
# <a name="ivmparallelportcollection_newenum-property"></a><span data-ttu-id="bb069-107">Propriedade IVMParallelPortCollection:: \_ NewEnum</span><span class="sxs-lookup"><span data-stu-id="bb069-107">IVMParallelPortCollection::\_NewEnum property</span></span>

<span data-ttu-id="bb069-108">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bb069-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bb069-109">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="bb069-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bb069-110">Recupera um enumerador para a coleção.</span><span class="sxs-lookup"><span data-stu-id="bb069-110">Retrieves an enumerator for the collection.</span></span>

<span data-ttu-id="bb069-111">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="bb069-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb069-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bb069-112">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a><span data-ttu-id="bb069-113">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="bb069-113">Property value</span></span>

<span data-ttu-id="bb069-114">O enumerador [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .</span><span class="sxs-lookup"><span data-stu-id="bb069-114">The [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumerator.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bb069-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="bb069-115">Error codes</span></span>



| <span data-ttu-id="bb069-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="bb069-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="bb069-117">Significado</span><span class="sxs-lookup"><span data-stu-id="bb069-117">Meaning</span></span>                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="bb069-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bb069-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="bb069-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="bb069-119">The operation was successful.</span></span><br/> |
| <dl> <span data-ttu-id="bb069-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="bb069-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="bb069-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="bb069-121">The parameter is **NULL**.</span></span><br/>    |
| <dl> <span data-ttu-id="bb069-122"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="bb069-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="bb069-123">Erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="bb069-123">An unexpected error occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="bb069-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb069-124">Requirements</span></span>



| <span data-ttu-id="bb069-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb069-125">Requirement</span></span> | <span data-ttu-id="bb069-126">Valor</span><span class="sxs-lookup"><span data-stu-id="bb069-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb069-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb069-127">Minimum supported client</span></span><br/> | <span data-ttu-id="bb069-128">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="bb069-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bb069-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb069-129">Minimum supported server</span></span><br/> | <span data-ttu-id="bb069-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="bb069-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bb069-131">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="bb069-131">End of client support</span></span><br/>    | <span data-ttu-id="bb069-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bb069-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bb069-133">Produto</span><span class="sxs-lookup"><span data-stu-id="bb069-133">Product</span></span><br/>                  | <span data-ttu-id="bb069-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bb069-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bb069-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bb069-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb069-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb069-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="bb069-137">IID</span><span class="sxs-lookup"><span data-stu-id="bb069-137">IID</span></span><br/>                      | <span data-ttu-id="bb069-138">IID \_ IVMParallelPortCollection é definido como 27c3e036-198f-430c-8735-6e652f7203fd</span><span class="sxs-lookup"><span data-stu-id="bb069-138">IID\_IVMParallelPortCollection is defined as 27c3e036-198f-430c-8735-6e652f7203fd</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="bb069-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb069-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb069-140">**IVMParallelPortCollection**</span><span class="sxs-lookup"><span data-stu-id="bb069-140">**IVMParallelPortCollection**</span></span>](ivmparallelportcollection.md)
</dt> </dl>

 

