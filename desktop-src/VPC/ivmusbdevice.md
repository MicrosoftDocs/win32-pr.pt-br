---
title: Interface IVMUSBDevice (VPCCOMInterfaces. h)
description: Define a interface para um dispositivo USB conectado ao host. Você pode anexar o dispositivo USB a uma máquina virtual para usar o dispositivo dentro da máquina virtual.
ms.assetid: f491fe8f-bc43-4dfa-b9c1-c93b4e5a7df6
keywords:
- Virtual PC de interface IVMUSBDevice
- Virtual PC de interface IVMUSBDevice, descrito
topic_type:
- apiref
api_name:
- IVMUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a1547bd812ea6d8f117f5910a254334676cafd1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105794598"
---
# <a name="ivmusbdevice-interface"></a><span data-ttu-id="8e014-106">Interface IVMUSBDevice</span><span class="sxs-lookup"><span data-stu-id="8e014-106">IVMUSBDevice interface</span></span>

<span data-ttu-id="8e014-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8e014-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8e014-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8e014-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8e014-109">Define a interface para um dispositivo USB conectado ao host.</span><span class="sxs-lookup"><span data-stu-id="8e014-109">Defines the interface for a USB device attached to host.</span></span> <span data-ttu-id="8e014-110">Você pode anexar o dispositivo USB a uma máquina virtual para usar o dispositivo dentro da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8e014-110">You can attach USB device to a virtual machine to use the device inside the virtual machine.</span></span>

## <a name="members"></a><span data-ttu-id="8e014-111">Membros</span><span class="sxs-lookup"><span data-stu-id="8e014-111">Members</span></span>

<span data-ttu-id="8e014-112">A interface **IVMUSBDevice** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="8e014-112">The **IVMUSBDevice** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="8e014-113">**IVMUSBDevice** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8e014-113">**IVMUSBDevice** also has these types of members:</span></span>

-   [<span data-ttu-id="8e014-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8e014-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8e014-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8e014-115">Properties</span></span>

<span data-ttu-id="8e014-116">A interface **IVMUSBDevice** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8e014-116">The **IVMUSBDevice** interface has these properties.</span></span>



| <span data-ttu-id="8e014-117">Propriedade</span><span class="sxs-lookup"><span data-stu-id="8e014-117">Property</span></span>                                                                 | <span data-ttu-id="8e014-118">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="8e014-118">Access type</span></span>          | <span data-ttu-id="8e014-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e014-119">Description</span></span>                                                                     |
|:-------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="8e014-120">**AttachedToVM**</span><span class="sxs-lookup"><span data-stu-id="8e014-120">**AttachedToVM**</span></span>](ivmusbdevice-attachedtovm.md)<br/>             | <span data-ttu-id="8e014-121">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e014-121">Read-only</span></span><br/> | <span data-ttu-id="8e014-122">O nome da máquina virtual à qual o dispositivo USB está anexado.</span><span class="sxs-lookup"><span data-stu-id="8e014-122">The name of the virtual machine to which the USB device is attached.</span></span><br/> |
| [<span data-ttu-id="8e014-123">**DeviceClass**</span><span class="sxs-lookup"><span data-stu-id="8e014-123">**DeviceClass**</span></span>](ivmusbdevice-deviceclass.md)<br/>               | <span data-ttu-id="8e014-124">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e014-124">Read-only</span></span><br/> | <span data-ttu-id="8e014-125">A classe de dispositivo do dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="8e014-125">The device class of the USB device.</span></span><br/>                                  |
| [<span data-ttu-id="8e014-126">**DeviceString**</span><span class="sxs-lookup"><span data-stu-id="8e014-126">**DeviceString**</span></span>](ivmusbdevice-devicestring.md)<br/>             | <span data-ttu-id="8e014-127">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e014-127">Read-only</span></span><br/> | <span data-ttu-id="8e014-128">O nome do dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="8e014-128">The name of the USB device.</span></span><br/>                                          |
| [<span data-ttu-id="8e014-129">**HubID**</span><span class="sxs-lookup"><span data-stu-id="8e014-129">**HubID**</span></span>](ivmusbdevice-hubid.md)<br/>                           | <span data-ttu-id="8e014-130">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e014-130">Read-only</span></span><br/> | <span data-ttu-id="8e014-131">O identificador do Hub no qual o dispositivo está conectado.</span><span class="sxs-lookup"><span data-stu-id="8e014-131">The identifier of the hub on which the device is connected.</span></span><br/>          |
| [<span data-ttu-id="8e014-132">**Manufacturerstring**</span><span class="sxs-lookup"><span data-stu-id="8e014-132">**ManufacturerString**</span></span>](ivmusbdevice-manufacturerstring.md)<br/> | <span data-ttu-id="8e014-133">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e014-133">Read-only</span></span><br/> | <span data-ttu-id="8e014-134">O nome do fabricante do dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="8e014-134">The name of the USB device manufacturer.</span></span><br/>                             |
| [<span data-ttu-id="8e014-135">**Porta**</span><span class="sxs-lookup"><span data-stu-id="8e014-135">**Port**</span></span>](ivmusbdevice-port.md)<br/>                             | <span data-ttu-id="8e014-136">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8e014-136">Read-only</span></span><br/> | <span data-ttu-id="8e014-137">O identificador da porta na qual o dispositivo está conectado.</span><span class="sxs-lookup"><span data-stu-id="8e014-137">The identifier of the port on which the device is connected.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="8e014-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e014-138">Requirements</span></span>



| <span data-ttu-id="8e014-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e014-139">Requirement</span></span> | <span data-ttu-id="8e014-140">Valor</span><span class="sxs-lookup"><span data-stu-id="8e014-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e014-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e014-141">Minimum supported client</span></span><br/> | <span data-ttu-id="8e014-142">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8e014-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8e014-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e014-143">Minimum supported server</span></span><br/> | <span data-ttu-id="8e014-144">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8e014-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8e014-145">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="8e014-145">End of client support</span></span><br/>    | <span data-ttu-id="8e014-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8e014-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8e014-147">Produto</span><span class="sxs-lookup"><span data-stu-id="8e014-147">Product</span></span><br/>                  | <span data-ttu-id="8e014-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8e014-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8e014-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8e014-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e014-150"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e014-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8e014-151">IID</span><span class="sxs-lookup"><span data-stu-id="8e014-151">IID</span></span><br/>                      | <span data-ttu-id="8e014-152">IID \_ IVMUSBDevice é definido como 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span><span class="sxs-lookup"><span data-stu-id="8e014-152">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



 

