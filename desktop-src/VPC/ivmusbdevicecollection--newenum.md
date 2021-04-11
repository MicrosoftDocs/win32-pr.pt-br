---
title: Propriedade _NewEnum IVMUSBDeviceCollection (VPCCOMInterfaces. h)
description: Recupera um enumerador para a coleção. | Propriedade _NewEnum IVMUSBDeviceCollection (VPCCOMInterfaces. h)
ms.assetid: f14f64a0-e65a-44d6-b053-54bbcb9ea804
keywords:
- _NewEnum a propriedade Virtual PC
- Propriedade _NewEnum Virtual PC, interface IVMUSBDeviceCollection
- IVMUSBDeviceCollection interface virtual PC, Propriedade _NewEnum
topic_type:
- apiref
api_name:
- IVMUSBDeviceCollection._NewEnum
- IVMUSBDeviceCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2e1e2a4d80691be26161ae4835ccb85c0e722d8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930516"
---
# <a name="ivmusbdevicecollection_newenum-property"></a><span data-ttu-id="2de9c-107">Propriedade IVMUSBDeviceCollection:: \_ NewEnum</span><span class="sxs-lookup"><span data-stu-id="2de9c-107">IVMUSBDeviceCollection::\_NewEnum property</span></span>

<span data-ttu-id="2de9c-108">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2de9c-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2de9c-109">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2de9c-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2de9c-110">Recupera um enumerador para a coleção.</span><span class="sxs-lookup"><span data-stu-id="2de9c-110">Retrieves an enumerator for the collection.</span></span>

<span data-ttu-id="2de9c-111">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="2de9c-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2de9c-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2de9c-112">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a><span data-ttu-id="2de9c-113">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="2de9c-113">Property value</span></span>

<span data-ttu-id="2de9c-114">O enumerador [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .</span><span class="sxs-lookup"><span data-stu-id="2de9c-114">The [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumerator.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2de9c-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="2de9c-115">Error codes</span></span>



| <span data-ttu-id="2de9c-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="2de9c-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="2de9c-117">Significado</span><span class="sxs-lookup"><span data-stu-id="2de9c-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="2de9c-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2de9c-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="2de9c-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2de9c-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="2de9c-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="2de9c-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="2de9c-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="2de9c-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="2de9c-122"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="2de9c-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="2de9c-123">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="2de9c-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="2de9c-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2de9c-124">Requirements</span></span>



| <span data-ttu-id="2de9c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2de9c-125">Requirement</span></span> | <span data-ttu-id="2de9c-126">Valor</span><span class="sxs-lookup"><span data-stu-id="2de9c-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2de9c-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2de9c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2de9c-128">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2de9c-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2de9c-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2de9c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2de9c-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2de9c-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2de9c-131">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="2de9c-131">End of client support</span></span><br/>    | <span data-ttu-id="2de9c-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2de9c-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2de9c-133">Produto</span><span class="sxs-lookup"><span data-stu-id="2de9c-133">Product</span></span><br/>                  | <span data-ttu-id="2de9c-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2de9c-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2de9c-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2de9c-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="2de9c-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2de9c-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2de9c-137">IID</span><span class="sxs-lookup"><span data-stu-id="2de9c-137">IID</span></span><br/>                      | <span data-ttu-id="2de9c-138">IID \_ IVMUSBDeviceCollection é definido como 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span><span class="sxs-lookup"><span data-stu-id="2de9c-138">IID\_IVMUSBDeviceCollection is defined as 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="2de9c-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="2de9c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2de9c-140">**IVMUSBDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="2de9c-140">**IVMUSBDeviceCollection**</span></span>](ivmusbdevicecollection.md)
</dt> </dl>

 

