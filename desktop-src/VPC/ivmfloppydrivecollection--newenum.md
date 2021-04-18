---
title: Propriedade _NewEnum IVMFloppyDriveCollection (VPCCOMInterfaces. h)
description: Recupera um enumerador para a coleção. | Propriedade _NewEnum IVMFloppyDriveCollection (VPCCOMInterfaces. h)
ms.assetid: 06de9560-cba9-4c64-907e-83e77781cafc
keywords:
- _NewEnum a propriedade Virtual PC
- Propriedade _NewEnum Virtual PC, interface IVMFloppyDriveCollection
- IVMFloppyDriveCollection interface virtual PC, Propriedade _NewEnum
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection._NewEnum
- IVMFloppyDriveCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7db9960ca627b66442e583c6e6bc8fdc89d8d878
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105788870"
---
# <a name="ivmfloppydrivecollection_newenum-property"></a><span data-ttu-id="948bd-107">Propriedade IVMFloppyDriveCollection:: \_ NewEnum</span><span class="sxs-lookup"><span data-stu-id="948bd-107">IVMFloppyDriveCollection::\_NewEnum property</span></span>

<span data-ttu-id="948bd-108">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="948bd-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="948bd-109">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="948bd-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="948bd-110">Recupera um enumerador para a coleção.</span><span class="sxs-lookup"><span data-stu-id="948bd-110">Retrieves an enumerator for the collection.</span></span>

<span data-ttu-id="948bd-111">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="948bd-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="948bd-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="948bd-112">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a><span data-ttu-id="948bd-113">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="948bd-113">Property value</span></span>

<span data-ttu-id="948bd-114">O enumerador [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .</span><span class="sxs-lookup"><span data-stu-id="948bd-114">The [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumerator.</span></span>

## <a name="error-codes"></a><span data-ttu-id="948bd-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="948bd-115">Error codes</span></span>



| <span data-ttu-id="948bd-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="948bd-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="948bd-117">Significado</span><span class="sxs-lookup"><span data-stu-id="948bd-117">Meaning</span></span>                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="948bd-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="948bd-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="948bd-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="948bd-119">The operation was successful.</span></span><br/> |
| <dl> <span data-ttu-id="948bd-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="948bd-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="948bd-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="948bd-121">The parameter is **NULL**.</span></span><br/>    |
| <dl> <span data-ttu-id="948bd-122"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="948bd-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="948bd-123">Erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="948bd-123">An unexpected error occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="948bd-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="948bd-124">Requirements</span></span>



| <span data-ttu-id="948bd-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="948bd-125">Requirement</span></span> | <span data-ttu-id="948bd-126">Valor</span><span class="sxs-lookup"><span data-stu-id="948bd-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="948bd-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="948bd-127">Minimum supported client</span></span><br/> | <span data-ttu-id="948bd-128">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="948bd-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="948bd-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="948bd-129">Minimum supported server</span></span><br/> | <span data-ttu-id="948bd-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="948bd-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="948bd-131">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="948bd-131">End of client support</span></span><br/>    | <span data-ttu-id="948bd-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="948bd-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="948bd-133">Produto</span><span class="sxs-lookup"><span data-stu-id="948bd-133">Product</span></span><br/>                  | <span data-ttu-id="948bd-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="948bd-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="948bd-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="948bd-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="948bd-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="948bd-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="948bd-137">IID</span><span class="sxs-lookup"><span data-stu-id="948bd-137">IID</span></span><br/>                      | <span data-ttu-id="948bd-138">IID \_ IVMFloppyDriveCollection é definido como 8ba70a25-f698-4ee5-85CE-3cc93a925516</span><span class="sxs-lookup"><span data-stu-id="948bd-138">IID\_IVMFloppyDriveCollection is defined as 8ba70a25-f698-4ee5-85ce-3cc93a925516</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="948bd-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="948bd-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="948bd-140">**IVMFloppyDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="948bd-140">**IVMFloppyDriveCollection**</span></span>](ivmfloppydrivecollection.md)
</dt> </dl>

 

