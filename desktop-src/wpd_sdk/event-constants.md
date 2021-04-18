---
description: Os dispositivos portáteis do Windows definem os seguintes valores de evento.
ms.assetid: d73788a1-d0fe-4a69-b472-edf438a28f90
title: Constantes de evento (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EVENT_DEVICE_CAPABILITIES_UPDATED
- WPD_EVENT_DEVICE_REMOVED
- WPD_EVENT_DEVICE_RESET
- WPD_EVENT_OBJECT_ADDED
- WPD_EVENT_OBJECT_REMOVED
- WPD_EVENT_OBJECT_TRANSFER_REQUESTED
- WPD_EVENT_OBJECT_UPDATED
- WPD_EVENT_SERVICE_METHOD_COMPLETE
- WPD_EVENT_STORAGE_FORMAT
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e60c44cda2585655a86ca1cdb4653ad002a0225d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781409"
---
# <a name="event-constants-portabledeviceh"></a><span data-ttu-id="fec3c-103">Constantes de evento (PortableDevice. h)</span><span class="sxs-lookup"><span data-stu-id="fec3c-103">Event Constants (PortableDevice.h)</span></span>

<span data-ttu-id="fec3c-104">Os dispositivos portáteis do Windows definem os seguintes valores de evento.</span><span class="sxs-lookup"><span data-stu-id="fec3c-104">Windows Portable Devices defines the following event values.</span></span>



| <span data-ttu-id="fec3c-105">Constante</span><span class="sxs-lookup"><span data-stu-id="fec3c-105">Constant</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="fec3c-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="fec3c-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WPD_EVENT_DEVICE_CAPABILITIES_UPDATED"></span><span id="wpd_event_device_capabilities_updated"></span><dl> <span data-ttu-id="fec3c-107"><dt>**\_recursos do dispositivo de eventos WPD \_ \_ \_ atualizados**</dt></span><span class="sxs-lookup"><span data-stu-id="fec3c-107"><dt>**WPD\_EVENT\_DEVICE\_CAPABILITIES\_UPDATED**</dt></span></span> </dl> | <span data-ttu-id="fec3c-108">Esse evento indica que os recursos do dispositivo foram alterados.</span><span class="sxs-lookup"><span data-stu-id="fec3c-108">This event indicates that the device capabilities have changed.</span></span> <span data-ttu-id="fec3c-109">Os clientes devem repetir o dispositivo se tiverem tomada alguma decisão com base nos recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fec3c-109">Clients should requery the device if they have made any decisions based on device capabilities.</span></span><br/>                                                                                                                                                                                              |
| <span id="WPD_EVENT_DEVICE_REMOVED"></span><span id="wpd_event_device_removed"></span><dl> <span data-ttu-id="fec3c-110"><dt>**\_dispositivo de eventos WPD \_ \_ removido**</dt></span><span class="sxs-lookup"><span data-stu-id="fec3c-110"><dt>**WPD\_EVENT\_DEVICE\_REMOVED**</dt></span></span> </dl>                                         | <span data-ttu-id="fec3c-111">Esse evento é enviado quando um driver de um dispositivo está sendo descarregado.</span><span class="sxs-lookup"><span data-stu-id="fec3c-111">This event is sent when a driver for a device is being unloaded.</span></span> <span data-ttu-id="fec3c-112">Normalmente, isso é resultado do dispositivo que está sendo desconectado.</span><span class="sxs-lookup"><span data-stu-id="fec3c-112">Typically this is a result of the device being unplugged.</span></span><br/> <span data-ttu-id="fec3c-113">Os clientes devem liberar a interface **IPortableDevice** e todas as interfaces [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) especificadas na **\_ \_ \_ \_ \_ ID do dispositivo PnP do parâmetro de evento WPD**.</span><span class="sxs-lookup"><span data-stu-id="fec3c-113">Clients should release the **IPortableDevice** interface and any [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) interfaces specified in **WPD\_EVENT\_PARAMETER\_PNP\_DEVICE\_ID**.</span></span><br/>                          |
| <span id="WPD_EVENT_DEVICE_RESET"></span><span id="wpd_event_device_reset"></span><dl> <span data-ttu-id="fec3c-114"><dt>**redefinição de \_ dispositivo de evento WPD \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fec3c-114"><dt>**WPD\_EVENT\_DEVICE\_RESET**</dt></span></span> </dl>                                               | <span data-ttu-id="fec3c-115">Esse evento indica que o dispositivo está prestes a ser redefinido e que todos os clientes conectados devem fechar suas conexões com o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fec3c-115">This event indicates that the device is about to be reset, and all connected clients should close their connections to the device.</span></span><br/>                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_ADDED"></span><span id="wpd_event_object_added"></span><dl> <span data-ttu-id="fec3c-116"><dt>**\_objeto de evento WPD \_ \_ adicionado**</dt></span><span class="sxs-lookup"><span data-stu-id="fec3c-116"><dt>**WPD\_EVENT\_OBJECT\_ADDED**</dt></span></span> </dl>                                               | <span data-ttu-id="fec3c-117">Esse evento indica que um novo objeto está disponível no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fec3c-117">This event indicates that a new object is available on the device.</span></span><br/>                                                                                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_REMOVED"></span><span id="wpd_event_object_removed"></span><dl> <span data-ttu-id="fec3c-118"><dt>**\_objeto de evento WPD \_ \_ removido**</dt></span><span class="sxs-lookup"><span data-stu-id="fec3c-118"><dt>**WPD\_EVENT\_OBJECT\_REMOVED**</dt></span></span> </dl>                                         | <span data-ttu-id="fec3c-119">Esse evento é enviado depois que um objeto existente anteriormente é removido do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fec3c-119">This event is sent after a previously existing object has been removed from the device.</span></span><br/> <span data-ttu-id="fec3c-120">O objeto pode ser um objeto de conteúdo, por exemplo, um arquivo de imagem foi excluído; ou pode ser um objeto funcional, por exemplo, um novo dispositivo de armazenamento foi desconectado do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fec3c-120">The object might be a content object, for example, an image file was deleted; or it might be a functional object, for example, a new storage device was unplugged from the device.</span></span><br/>                                                                        |
| <span id="WPD_EVENT_OBJECT_TRANSFER_REQUESTED"></span><span id="wpd_event_object_transfer_requested"></span><dl> <span data-ttu-id="fec3c-121"><dt>**\_transferência de objeto de evento WPD \_ \_ \_ solicitada**</dt></span><span class="sxs-lookup"><span data-stu-id="fec3c-121"><dt>**WPD\_EVENT\_OBJECT\_TRANSFER\_REQUESTED**</dt></span></span> </dl>       | <span data-ttu-id="fec3c-122">Esse evento é enviado para solicitar que um aplicativo Transfira um objeto específico do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fec3c-122">This event is sent to request an application to transfer a particular object from the device.</span></span><br/> <span data-ttu-id="fec3c-123">O objeto é geralmente um objeto de conteúdo, por exemplo, um arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="fec3c-123">The object is usually a content object, for example, an image file.</span></span><br/>                                                                                                                                                                                 |
| <span id="WPD_EVENT_OBJECT_UPDATED"></span><span id="wpd_event_object_updated"></span><dl> <span data-ttu-id="fec3c-124"><dt>**\_objeto de evento WPD \_ \_ atualizado**</dt></span><span class="sxs-lookup"><span data-stu-id="fec3c-124"><dt>**WPD\_EVENT\_OBJECT\_UPDATED**</dt></span></span> </dl>                                         | <span data-ttu-id="fec3c-125">Esse evento é enviado após a atualização de um objeto e qualquer cliente conectado deve atualizar sua exibição desse objeto.</span><span class="sxs-lookup"><span data-stu-id="fec3c-125">This event is sent after an object has been updated, and any connected client should refresh its view of that object.</span></span><br/>                                                                                                                                                                                                                                        |
| <span id="WPD_EVENT_SERVICE_METHOD_COMPLETE"></span><span id="wpd_event_service_method_complete"></span><dl> <span data-ttu-id="fec3c-126"><dt>**\_método de serviço de evento WPD \_ \_ \_ concluído**</dt></span><span class="sxs-lookup"><span data-stu-id="fec3c-126"><dt>**WPD\_EVENT\_SERVICE\_METHOD\_COMPLETE**</dt></span></span> </dl>             | <span data-ttu-id="fec3c-127">Esse evento é enviado quando um driver conclui a invocação de um método de serviço.</span><span class="sxs-lookup"><span data-stu-id="fec3c-127">This event is sent when a driver has completed invoking a service method.</span></span> <span data-ttu-id="fec3c-128">Esse evento deve ser enviado mesmo quando o método falhar.</span><span class="sxs-lookup"><span data-stu-id="fec3c-128">This event must be sent even when the method fails.</span></span> <span data-ttu-id="fec3c-129">Esse é um evento de DDI de WPD interno e não estará disponível para nenhum aplicativo por meio de [**IPortableDevice:: Advise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-advise) ou [**IPortableDeviceService:: Advise**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-advise).</span><span class="sxs-lookup"><span data-stu-id="fec3c-129">This is an internal WPD DDI event, and will not be available to any applications through [**IPortableDevice::Advise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-advise) or [**IPortableDeviceService::Advise**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-advise).</span></span><br/> |
| <span id="WPD_EVENT_STORAGE_FORMAT"></span><span id="wpd_event_storage_format"></span><dl> <span data-ttu-id="fec3c-130"><dt>**\_formato de \_ armazenamento de eventos WPD \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fec3c-130"><dt>**WPD\_EVENT\_STORAGE\_FORMAT**</dt></span></span> </dl>                                         | <span data-ttu-id="fec3c-131">Esse evento indica o progresso de uma operação de formatação em um objeto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="fec3c-131">This event indicates the progress of a format operation on a storage object.</span></span><br/>                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a><span data-ttu-id="fec3c-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fec3c-132">Requirements</span></span>



| <span data-ttu-id="fec3c-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="fec3c-133">Requirement</span></span> | <span data-ttu-id="fec3c-134">Valor</span><span class="sxs-lookup"><span data-stu-id="fec3c-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="fec3c-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fec3c-135">Header</span></span><br/> | <dl> <span data-ttu-id="fec3c-136"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="fec3c-136"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fec3c-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="fec3c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fec3c-138">Constantes</span><span class="sxs-lookup"><span data-stu-id="fec3c-138">Constants</span></span>](constants.md)
</dt> </dl>

 

 




