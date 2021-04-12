---
title: Propriedade Count de IVMUSBDeviceCollection (VPCCOMInterfaces. h)
description: Recupera o número de dispositivos USB nesta coleção.
ms.assetid: 8d17397b-4f4a-475d-99fe-4df0d74fe5a5
keywords:
- Propriedade de contagem Virtual PC
- Propriedade Count Virtual PC, interface IVMUSBDeviceCollection
- Virtual PC de interface IVMUSBDeviceCollection, Propriedade Count
topic_type:
- apiref
api_name:
- IVMUSBDeviceCollection.Count
- IVMUSBDeviceCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5a0c2146df70f0432a19d65daad44ba6f1ec372
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455257"
---
# <a name="ivmusbdevicecollectioncount-property"></a><span data-ttu-id="8924b-106">Propriedade IVMUSBDeviceCollection:: Count</span><span class="sxs-lookup"><span data-stu-id="8924b-106">IVMUSBDeviceCollection::Count property</span></span>

<span data-ttu-id="8924b-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8924b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8924b-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8924b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8924b-109">Recupera o número de dispositivos USB nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="8924b-109">Retrieves the number of USB devices in this collection.</span></span>

<span data-ttu-id="8924b-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="8924b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8924b-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8924b-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="8924b-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="8924b-112">Property value</span></span>

<span data-ttu-id="8924b-113">O número de dispositivos USB.</span><span class="sxs-lookup"><span data-stu-id="8924b-113">The number of USB devices.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8924b-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="8924b-114">Error codes</span></span>



| <span data-ttu-id="8924b-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="8924b-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="8924b-116">Significado</span><span class="sxs-lookup"><span data-stu-id="8924b-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="8924b-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8924b-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="8924b-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8924b-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="8924b-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="8924b-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="8924b-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="8924b-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="8924b-121"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="8924b-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="8924b-122">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="8924b-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="8924b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8924b-123">Requirements</span></span>



| <span data-ttu-id="8924b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8924b-124">Requirement</span></span> | <span data-ttu-id="8924b-125">Valor</span><span class="sxs-lookup"><span data-stu-id="8924b-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8924b-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8924b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8924b-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8924b-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8924b-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8924b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8924b-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8924b-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8924b-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="8924b-130">End of client support</span></span><br/>    | <span data-ttu-id="8924b-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8924b-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8924b-132">Produto</span><span class="sxs-lookup"><span data-stu-id="8924b-132">Product</span></span><br/>                  | <span data-ttu-id="8924b-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8924b-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8924b-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8924b-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="8924b-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8924b-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8924b-136">IID</span><span class="sxs-lookup"><span data-stu-id="8924b-136">IID</span></span><br/>                      | <span data-ttu-id="8924b-137">IID \_ IVMUSBDeviceCollection é definido como 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span><span class="sxs-lookup"><span data-stu-id="8924b-137">IID\_IVMUSBDeviceCollection is defined as 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="8924b-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="8924b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8924b-139">**IVMUSBDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="8924b-139">**IVMUSBDeviceCollection**</span></span>](ivmusbdevicecollection.md)
</dt> </dl>

 

