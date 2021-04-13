---
title: Interface IBasicDevice
description: Encapsula os métodos e eventos necessários para modelar um dispositivo DLNA.
ms.assetid: E4F99A11-4ED5-44CB-BE16-CBB558412ED4
keywords:
- API de streaming de mídia da interface IBasicDevice
- API de streaming de mídia da interface IBasicDevice, descrita
topic_type:
- apiref
api_name:
- IBasicDevice
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1567605fb160fc69ac933bb94a0b0282e35616d5
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2020
ms.locfileid: "104366904"
---
# <a name="ibasicdevice-interface"></a><span data-ttu-id="7aa11-105">Interface IBasicDevice</span><span class="sxs-lookup"><span data-stu-id="7aa11-105">IBasicDevice interface</span></span>

<span data-ttu-id="7aa11-106">Encapsula os métodos e eventos necessários para modelar um dispositivo DLNA.</span><span class="sxs-lookup"><span data-stu-id="7aa11-106">Encapsulates the methods and events needed to model a DLNA Device.</span></span>

## <a name="members"></a><span data-ttu-id="7aa11-107">Membros</span><span class="sxs-lookup"><span data-stu-id="7aa11-107">Members</span></span>

<span data-ttu-id="7aa11-108">A interface **IBasicDevice** herda de [**IInspectable**](/windows/desktop/api/inspectable/nn-inspectable-iinspectable).</span><span class="sxs-lookup"><span data-stu-id="7aa11-108">The **IBasicDevice** interface inherits from [**IInspectable**](/windows/desktop/api/inspectable/nn-inspectable-iinspectable).</span></span> <span data-ttu-id="7aa11-109">**IBasicDevice** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7aa11-109">**IBasicDevice** also has these types of members:</span></span>

-   [<span data-ttu-id="7aa11-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="7aa11-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7aa11-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="7aa11-111">Methods</span></span>

<span data-ttu-id="7aa11-112">A interface **IBasicDevice** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="7aa11-112">The **IBasicDevice** interface has these methods.</span></span>



| <span data-ttu-id="7aa11-113">Método</span><span class="sxs-lookup"><span data-stu-id="7aa11-113">Method</span></span>                                                                                 | <span data-ttu-id="7aa11-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="7aa11-114">Description</span></span>                                                                                                                    |
|:---------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7aa11-115">**Adicionar \_ ConnectionStatusChanged**</span><span class="sxs-lookup"><span data-stu-id="7aa11-115">**add\_ConnectionStatusChanged**</span></span>](ibasicdevice-add-connectionstatuschanged.md)       | <span data-ttu-id="7aa11-116">Registra um manipulador de eventos para o evento [**ConnectionStatusChanged**](connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="7aa11-116">Registers an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span><br/>                |
| [<span data-ttu-id="7aa11-117">**CanWakeDevices**</span><span class="sxs-lookup"><span data-stu-id="7aa11-117">**CanWakeDevices**</span></span>](ibasicdevice-canwakedevices.md)                                  | <span data-ttu-id="7aa11-118">Recupera um valor que indica se o dispositivo pode ser ativado.</span><span class="sxs-lookup"><span data-stu-id="7aa11-118">Retrieves a value that indicates if the device can wake.</span></span><br/>                                                            |
| <span data-ttu-id="7aa11-119">[**ConnectionStatus**](/previous-versions/windows/desktop/legacy/hh828873(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7aa11-119">[**ConnectionStatus**](/previous-versions/windows/desktop/legacy/hh828873(v=vs.85))</span></span>                              | <span data-ttu-id="7aa11-120">Retorna um valor de enumeração que indica se o dispositivo está atualmente online, off-line ou em suspensão, mas Despertável.</span><span class="sxs-lookup"><span data-stu-id="7aa11-120">Returns an enumeration value indicating whether the device is currently on-line, off-line or sleeping but wakeable.</span></span><br/> |
| [<span data-ttu-id="7aa11-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7aa11-121">**Description**</span></span>](ibasicdevice-description.md)                                        | <span data-ttu-id="7aa11-122">Recupera uma descrição do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7aa11-122">Retrieves a description of the device.</span></span><br/>                                                                              |
| [<span data-ttu-id="7aa11-123">**DiscoveredOnCurrentNetwork**</span><span class="sxs-lookup"><span data-stu-id="7aa11-123">**DiscoveredOnCurrentNetwork**</span></span>](ibasicdevice-discoveredoncurrentnetwork.md)          | <span data-ttu-id="7aa11-124">Recupera um valor que indica se o dispositivo está na rede atual.</span><span class="sxs-lookup"><span data-stu-id="7aa11-124">Retrieves a value that indicates if the device is on the current network.</span></span><br/>                                           |
| [<span data-ttu-id="7aa11-125">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="7aa11-125">**FriendlyName**</span></span>](ibasicdevice-friendlyname.md)                                      | <span data-ttu-id="7aa11-126">Recupera o nome amigável do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7aa11-126">Retrieves the device s friendly name.</span></span><br/>                                                                               |
| [<span data-ttu-id="7aa11-127">**Ícones**</span><span class="sxs-lookup"><span data-stu-id="7aa11-127">**Icons**</span></span>](ibasicdevice-icons.md)                                                    | <span data-ttu-id="7aa11-128">Retorna um vetor de interfaces [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) .</span><span class="sxs-lookup"><span data-stu-id="7aa11-128">Returns a vector of [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) interfaces.</span></span><br/>                                                  |
| [<span data-ttu-id="7aa11-129">**IpAddresses**</span><span class="sxs-lookup"><span data-stu-id="7aa11-129">**IpAddresses**</span></span>](ibasicdevice-ipaddresses.md)                                        | <span data-ttu-id="7aa11-130">Retorna um vetor de endereços IP.</span><span class="sxs-lookup"><span data-stu-id="7aa11-130">Returns a vector of IP addresses.</span></span><br/>                                                                                   |
| [<span data-ttu-id="7aa11-131">**ManufacturerName**</span><span class="sxs-lookup"><span data-stu-id="7aa11-131">**ManufacturerName**</span></span>](ibasicdevice-manufacturername.md)                              | <span data-ttu-id="7aa11-132">Recupera o nome do fabricante do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7aa11-132">Retrieves the device s manufacturer name.</span></span><br/>                                                                           |
| [<span data-ttu-id="7aa11-133">**ManufacturerUrl**</span><span class="sxs-lookup"><span data-stu-id="7aa11-133">**ManufacturerUrl**</span></span>](ibasicdevice-manufacturerurl.md)                                | <span data-ttu-id="7aa11-134">Recupera a URL do fabricante do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7aa11-134">Retrieves the device s manufacturer URL.</span></span><br/>                                                                            |
| [<span data-ttu-id="7aa11-135">**ModelName**</span><span class="sxs-lookup"><span data-stu-id="7aa11-135">**ModelName**</span></span>](ibasicdevice-modelname.md)                                            | <span data-ttu-id="7aa11-136">Recupera o nome do modelo do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7aa11-136">Retrieves the device s model name.</span></span><br/>                                                                                  |
| [<span data-ttu-id="7aa11-137">**ModelNumber**</span><span class="sxs-lookup"><span data-stu-id="7aa11-137">**ModelNumber**</span></span>](ibasicdevice-modelnumber.md)                                        | <span data-ttu-id="7aa11-138">Recupera o número do modelo do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7aa11-138">Retrieves the device s model number.</span></span><br/>                                                                                |
| [<span data-ttu-id="7aa11-139">**ModelUrl**</span><span class="sxs-lookup"><span data-stu-id="7aa11-139">**ModelUrl**</span></span>](ibasicdevice-modelurl.md)                                              | <span data-ttu-id="7aa11-140">Recupera a URL do modelo do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7aa11-140">Retrieves the device s model URL.</span></span><br/>                                                                                   |
| [<span data-ttu-id="7aa11-141">**PhysicalAddresses**</span><span class="sxs-lookup"><span data-stu-id="7aa11-141">**PhysicalAddresses**</span></span>](ibasicdevice-physicaladdresses.md)                            | <span data-ttu-id="7aa11-142">Retorna um vetor de endereços físicos.</span><span class="sxs-lookup"><span data-stu-id="7aa11-142">Returns a vector of physical addresses.</span></span><br/>                                                                             |
| [<span data-ttu-id="7aa11-143">**PresentationUrl**</span><span class="sxs-lookup"><span data-stu-id="7aa11-143">**PresentationUrl**</span></span>](ibasicdevice-presentationurl.md)                                | <span data-ttu-id="7aa11-144">Recupera a URL de apresentação do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7aa11-144">Retrieves the device s presentation URL.</span></span><br/>                                                                            |
| [<span data-ttu-id="7aa11-145">**RemoteStreamingUrls**</span><span class="sxs-lookup"><span data-stu-id="7aa11-145">**RemoteStreamingUrls**</span></span>](ibasicdevice-remotestreamingurls.md)                        | <span data-ttu-id="7aa11-146">Retorna um vetor de URLs de streaming remota.</span><span class="sxs-lookup"><span data-stu-id="7aa11-146">Returns a vector of remote streaming URLs.</span></span><br/>                                                                          |
| [<span data-ttu-id="7aa11-147">**Remover \_ ConnectionStatusChanged**</span><span class="sxs-lookup"><span data-stu-id="7aa11-147">**remove\_ConnectionStatusChanged**</span></span>](ibasicdevice-remove-connectionstatuschanged.md) | <span data-ttu-id="7aa11-148">Cancela o registro de um manipulador de eventos para o evento [**ConnectionStatusChanged**](connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="7aa11-148">Unregisters an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span><br/>              |
| [<span data-ttu-id="7aa11-149">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="7aa11-149">**SerialNumber**</span></span>](ibasicdevice-serialnumber.md)                                      | <span data-ttu-id="7aa11-150">Recupera o número de série do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7aa11-150">Retrieves the device s serial number.</span></span><br/>                                                                               |
| [<span data-ttu-id="7aa11-151">**Escreva**</span><span class="sxs-lookup"><span data-stu-id="7aa11-151">**Type**</span></span>](ibasicdevice-type.md)                                                      | <span data-ttu-id="7aa11-152">Recupera um valor de enumeração que indica o tipo de dispositivo do dispositivo DLNA.</span><span class="sxs-lookup"><span data-stu-id="7aa11-152">Retrieves an enumeration value indicating the device type of the DLNA device.</span></span><br/>                                       |
| [<span data-ttu-id="7aa11-153">**UniqueDeviceName**</span><span class="sxs-lookup"><span data-stu-id="7aa11-153">**UniqueDeviceName**</span></span>](ibasicdevice-uniquedevicename.md)                              | <span data-ttu-id="7aa11-154">Recupera o nome do dispositivo exclusivo do dispositivo (UDN).</span><span class="sxs-lookup"><span data-stu-id="7aa11-154">Retrieves the device s unique device name (UDN).</span></span><br/>                                                                    |



 

## <a name="see-also"></a><span data-ttu-id="7aa11-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="7aa11-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7aa11-156">**IInspectable**</span><span class="sxs-lookup"><span data-stu-id="7aa11-156">**IInspectable**</span></span>](/windows/desktop/api/inspectable/nn-inspectable-iinspectable)
</dt> </dl>

 

