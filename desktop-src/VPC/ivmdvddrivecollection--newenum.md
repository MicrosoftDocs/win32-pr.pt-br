---
title: Propriedade _NewEnum IVMDVDDriveCollection (VPCCOMInterfaces. h)
description: Recupera um enumerador para a coleção de CD/DVD.
ms.assetid: e911628b-2a92-41e5-9271-556a297d747d
keywords:
- _NewEnum a propriedade Virtual PC
- Propriedade _NewEnum Virtual PC, interface IVMDVDDriveCollection
- IVMDVDDriveCollection interface virtual PC, Propriedade _NewEnum
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection._NewEnum
- IVMDVDDriveCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dfd0de3aaf6b25808d1afa591b0c2099599e6bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918401"
---
# <a name="ivmdvddrivecollection_newenum-property"></a><span data-ttu-id="fb072-106">Propriedade IVMDVDDriveCollection:: \_ NewEnum</span><span class="sxs-lookup"><span data-stu-id="fb072-106">IVMDVDDriveCollection::\_NewEnum property</span></span>

<span data-ttu-id="fb072-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fb072-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fb072-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="fb072-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fb072-109">Recupera um enumerador para a coleção de CD/DVD.</span><span class="sxs-lookup"><span data-stu-id="fb072-109">Retrieves an enumerator for the CD/DVD collection.</span></span>

<span data-ttu-id="fb072-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="fb072-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb072-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb072-111">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a><span data-ttu-id="fb072-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="fb072-112">Property value</span></span>

<span data-ttu-id="fb072-113">O enumerador [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .</span><span class="sxs-lookup"><span data-stu-id="fb072-113">The [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumerator.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fb072-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="fb072-114">Error codes</span></span>



| <span data-ttu-id="fb072-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="fb072-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="fb072-116">Significado</span><span class="sxs-lookup"><span data-stu-id="fb072-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="fb072-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fb072-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="fb072-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="fb072-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="fb072-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="fb072-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="fb072-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="fb072-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="fb072-121"><dt>E \_ FALHA</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="fb072-121"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>            | <span data-ttu-id="fb072-122">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="fb072-122">An unexpected error has occurred.</span></span><br/> |
| <dl> <span data-ttu-id="fb072-123"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="fb072-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="fb072-124">Erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="fb072-124">An unexpected error occurred.</span></span><br/>     |



## <a name="requirements"></a><span data-ttu-id="fb072-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb072-125">Requirements</span></span>



| <span data-ttu-id="fb072-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb072-126">Requirement</span></span> | <span data-ttu-id="fb072-127">Valor</span><span class="sxs-lookup"><span data-stu-id="fb072-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb072-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb072-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fb072-129">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="fb072-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fb072-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb072-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fb072-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="fb072-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fb072-132">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="fb072-132">End of client support</span></span><br/>    | <span data-ttu-id="fb072-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fb072-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fb072-134">Produto</span><span class="sxs-lookup"><span data-stu-id="fb072-134">Product</span></span><br/>                  | <span data-ttu-id="fb072-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fb072-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fb072-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fb072-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb072-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb072-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="fb072-138">IID</span><span class="sxs-lookup"><span data-stu-id="fb072-138">IID</span></span><br/>                      | <span data-ttu-id="fb072-139">IID \_ IVMDVDDriveCollection é definido como bc86e297-e55f-4742-9614-ad11d3131f68</span><span class="sxs-lookup"><span data-stu-id="fb072-139">IID\_IVMDVDDriveCollection is defined as bc86e297-e55f-4742-9614-ad11d3131f68</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="fb072-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb072-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb072-141">**IVMDVDDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="fb072-141">**IVMDVDDriveCollection**</span></span>](ivmdvddrivecollection.md)
</dt> </dl>

 

