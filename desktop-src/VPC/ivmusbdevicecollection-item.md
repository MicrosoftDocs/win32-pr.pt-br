---
title: Propriedade de item IVMUSBDeviceCollection (VPCCOMInterfaces. h)
description: Recupera o objeto de dispositivo USB que corresponde ao índice especificado.
ms.assetid: 664a038e-7c86-43a9-a376-c913d431dc93
keywords:
- Propriedade do item Virtual PC
- Propriedade de item Virtual PC, interface IVMUSBDeviceCollection
- IVMUSBDeviceCollection interface virtual PC, Propriedade Item
topic_type:
- apiref
api_name:
- IVMUSBDeviceCollection.Item
- IVMUSBDeviceCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b50b96de6b19dab15852f58d78480b46da1e9ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455256"
---
# <a name="ivmusbdevicecollectionitem-property"></a><span data-ttu-id="cbdc4-106">Propriedade IVMUSBDeviceCollection:: item</span><span class="sxs-lookup"><span data-stu-id="cbdc4-106">IVMUSBDeviceCollection::Item property</span></span>

<span data-ttu-id="cbdc4-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cbdc4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="cbdc4-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="cbdc4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="cbdc4-109">Recupera o objeto de dispositivo USB que corresponde ao índice especificado.</span><span class="sxs-lookup"><span data-stu-id="cbdc4-109">Retrieves the USB device object that corresponds to the specified index.</span></span>

<span data-ttu-id="cbdc4-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="cbdc4-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbdc4-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cbdc4-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long         index,
  [out, retval] IVMUSBDevice **usbDevice
);
```



## <a name="property-value"></a><span data-ttu-id="cbdc4-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="cbdc4-112">Property value</span></span>

<span data-ttu-id="cbdc4-113">O objeto [**IVMUSBDevice**](ivmusbdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="cbdc4-113">The [**IVMUSBDevice**](ivmusbdevice.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cbdc4-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="cbdc4-114">Error codes</span></span>



| <span data-ttu-id="cbdc4-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="cbdc4-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="cbdc4-116">Significado</span><span class="sxs-lookup"><span data-stu-id="cbdc4-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cbdc4-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cbdc4-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="cbdc4-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="cbdc4-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="cbdc4-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="cbdc4-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="cbdc4-120">O parâmetro *usbDevice* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="cbdc4-120">The *usbDevice* parameter is **NULL**.</span></span> <br/>                                             |
| <dl> <span data-ttu-id="cbdc4-121"><dt>DISP \_ E \_ BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="cbdc4-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="cbdc4-122">O índice do item solicitado não corresponde a um item nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="cbdc4-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="cbdc4-123"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="cbdc4-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="cbdc4-124">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="cbdc4-124">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="cbdc4-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbdc4-125">Requirements</span></span>



| <span data-ttu-id="cbdc4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbdc4-126">Requirement</span></span> | <span data-ttu-id="cbdc4-127">Valor</span><span class="sxs-lookup"><span data-stu-id="cbdc4-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbdc4-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cbdc4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cbdc4-129">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="cbdc4-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cbdc4-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cbdc4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cbdc4-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="cbdc4-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="cbdc4-132">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="cbdc4-132">End of client support</span></span><br/>    | <span data-ttu-id="cbdc4-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cbdc4-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="cbdc4-134">Produto</span><span class="sxs-lookup"><span data-stu-id="cbdc4-134">Product</span></span><br/>                  | <span data-ttu-id="cbdc4-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="cbdc4-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="cbdc4-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cbdc4-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbdc4-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbdc4-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="cbdc4-138">IID</span><span class="sxs-lookup"><span data-stu-id="cbdc4-138">IID</span></span><br/>                      | <span data-ttu-id="cbdc4-139">IID \_ IVMUSBDeviceCollection é definido como 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span><span class="sxs-lookup"><span data-stu-id="cbdc4-139">IID\_IVMUSBDeviceCollection is defined as 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="cbdc4-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="cbdc4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbdc4-141">**IVMUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="cbdc4-141">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> <dt>

[<span data-ttu-id="cbdc4-142">**IVMUSBDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="cbdc4-142">**IVMUSBDeviceCollection**</span></span>](ivmusbdevicecollection.md)
</dt> </dl>

 

