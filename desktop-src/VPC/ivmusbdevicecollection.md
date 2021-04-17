---
title: Interface IVMUSBDeviceCollection (VPCCOMInterfaces. h)
description: Define a coleção de dispositivos USB conectados ao sistema host. Para obter um objeto IVMUSBDeviceCollection, use a propriedade IVMVirtualPC USBDeviceCollection.
ms.assetid: a5cca485-29d3-47fa-9cda-fedcdc379155
keywords:
- Virtual PC de interface IVMUSBDeviceCollection
- Virtual PC de interface IVMUSBDeviceCollection, descrito
topic_type:
- apiref
api_name:
- IVMUSBDeviceCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e773f006a1d98253a20ad37d5a70db43f487980
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105770582"
---
# <a name="ivmusbdevicecollection-interface"></a><span data-ttu-id="243d0-106">Interface IVMUSBDeviceCollection</span><span class="sxs-lookup"><span data-stu-id="243d0-106">IVMUSBDeviceCollection interface</span></span>

<span data-ttu-id="243d0-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="243d0-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="243d0-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="243d0-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="243d0-109">Define a coleção de dispositivos USB conectados ao sistema host.</span><span class="sxs-lookup"><span data-stu-id="243d0-109">Defines the collection of USB devices attached to the host system.</span></span> <span data-ttu-id="243d0-110">Para obter um objeto **IVMUSBDeviceCollection** , use a propriedade [**IVMVirtualPC:: USBDeviceCollection**](ivmvirtualpc-usbdevicecollection.md) .</span><span class="sxs-lookup"><span data-stu-id="243d0-110">To obtain an **IVMUSBDeviceCollection** object, use the [**IVMVirtualPC::USBDeviceCollection**](ivmvirtualpc-usbdevicecollection.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="243d0-111">Membros</span><span class="sxs-lookup"><span data-stu-id="243d0-111">Members</span></span>

<span data-ttu-id="243d0-112">A interface **IVMUSBDeviceCollection** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="243d0-112">The **IVMUSBDeviceCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="243d0-113">**IVMUSBDeviceCollection** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="243d0-113">**IVMUSBDeviceCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="243d0-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="243d0-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="243d0-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="243d0-115">Properties</span></span>

<span data-ttu-id="243d0-116">A interface **IVMUSBDeviceCollection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="243d0-116">The **IVMUSBDeviceCollection** interface has these properties.</span></span>



| <span data-ttu-id="243d0-117">Propriedade</span><span class="sxs-lookup"><span data-stu-id="243d0-117">Property</span></span>                                                        | <span data-ttu-id="243d0-118">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="243d0-118">Access type</span></span>          | <span data-ttu-id="243d0-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="243d0-119">Description</span></span>                                                                         |
|:----------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="243d0-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="243d0-120">**\_NewEnum**</span></span>](ivmusbdevicecollection--newenum.md)<br/> | <span data-ttu-id="243d0-121">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="243d0-121">Read-only</span></span><br/> | <span data-ttu-id="243d0-122">Um enumerador para a coleção.</span><span class="sxs-lookup"><span data-stu-id="243d0-122">An enumerator for the collection.</span></span><br/>                                        |
| [<span data-ttu-id="243d0-123">**Contar**</span><span class="sxs-lookup"><span data-stu-id="243d0-123">**Count**</span></span>](ivmusbdevicecollection-count.md)<br/>        | <span data-ttu-id="243d0-124">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="243d0-124">Read-only</span></span><br/> | <span data-ttu-id="243d0-125">O número de dispositivos USB nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="243d0-125">The number of USB devices in this collection.</span></span><br/>                            |
| [<span data-ttu-id="243d0-126">**Item**</span><span class="sxs-lookup"><span data-stu-id="243d0-126">**Item**</span></span>](ivmusbdevicecollection-item.md)<br/>          | <span data-ttu-id="243d0-127">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="243d0-127">Read-only</span></span><br/> | <span data-ttu-id="243d0-128">O objeto de dispositivo USB que corresponde ao índice especificado (baseado em 1).</span><span class="sxs-lookup"><span data-stu-id="243d0-128">The USB device object that corresponds to the specified index (1-based).</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="243d0-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="243d0-129">Requirements</span></span>



| <span data-ttu-id="243d0-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="243d0-130">Requirement</span></span> | <span data-ttu-id="243d0-131">Valor</span><span class="sxs-lookup"><span data-stu-id="243d0-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="243d0-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="243d0-132">Minimum supported client</span></span><br/> | <span data-ttu-id="243d0-133">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="243d0-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="243d0-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="243d0-134">Minimum supported server</span></span><br/> | <span data-ttu-id="243d0-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="243d0-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="243d0-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="243d0-136">End of client support</span></span><br/>    | <span data-ttu-id="243d0-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="243d0-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="243d0-138">Produto</span><span class="sxs-lookup"><span data-stu-id="243d0-138">Product</span></span><br/>                  | <span data-ttu-id="243d0-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="243d0-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="243d0-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="243d0-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="243d0-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="243d0-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="243d0-142">IID</span><span class="sxs-lookup"><span data-stu-id="243d0-142">IID</span></span><br/>                      | <span data-ttu-id="243d0-143">IID \_ IVMUSBDeviceCollection é definido como 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span><span class="sxs-lookup"><span data-stu-id="243d0-143">IID\_IVMUSBDeviceCollection is defined as 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="243d0-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="243d0-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="243d0-145">**IVMUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="243d0-145">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> <dt>

[<span data-ttu-id="243d0-146">**IVMVirtualPC::USBDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="243d0-146">**IVMVirtualPC::USBDeviceCollection**</span></span>](ivmvirtualpc-usbdevicecollection.md)
</dt> </dl>

 

