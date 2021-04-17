---
description: Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de evento.
ms.assetid: 672b75ac-cd47-4212-a505-c220ecdf98e3
title: Propriedades do evento (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 54c7aefeaf1170b7a8b8e3e79a62288f2d14dad2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763238"
---
# <a name="event-properties"></a><span data-ttu-id="04aa5-103">Propriedades do evento</span><span class="sxs-lookup"><span data-stu-id="04aa5-103">Event Properties</span></span>

<span data-ttu-id="04aa5-104">Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de evento.</span><span class="sxs-lookup"><span data-stu-id="04aa5-104">Windows Portable Devices supports the following event properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="04aa5-105">Propriedade</span><span class="sxs-lookup"><span data-stu-id="04aa5-105">Property</span></span></th>
<th><span data-ttu-id="04aa5-106">VarType</span><span class="sxs-lookup"><span data-stu-id="04aa5-106">VarType</span></span></th>
<th><span data-ttu-id="04aa5-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="04aa5-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="04aa5-108"><strong>WPD_EVENT_OPTION_IS_AUTOPLAY_EVENT</strong></span><span class="sxs-lookup"><span data-stu-id="04aa5-108"><strong>WPD_EVENT_OPTION_IS_AUTOPLAY_EVENT</strong></span></span></td>
<td><span data-ttu-id="04aa5-109"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="04aa5-109"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="04aa5-110">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="04aa5-110">Reserved for future use.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04aa5-111"><strong>WPD_EVENT_OPTION_IS_BROADCAST_EVENT</strong></span><span class="sxs-lookup"><span data-stu-id="04aa5-111"><strong>WPD_EVENT_OPTION_IS_BROADCAST_EVENT</strong></span></span></td>
<td><span data-ttu-id="04aa5-112"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="04aa5-112"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="04aa5-113">Um valor booliano que especifica se o evento é difundido para todos os clientes. Os clientes podem receber esse evento registrando seu retorno de chamada com <strong>IPortableDevice:: Advise</strong>.</span><span class="sxs-lookup"><span data-stu-id="04aa5-113">A Boolean value that specifies whether the event is broadcast to all clients.Clients can receive this event by registering their callback with <strong>IPortableDevice::Advise</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04aa5-114"><strong>WPD_EVENT_PARAMETER_CHILD_HIERARCHY_CHANGED</strong></span><span class="sxs-lookup"><span data-stu-id="04aa5-114"><strong>WPD_EVENT_PARAMETER_CHILD_HIERARCHY_CHANGED</strong></span></span></td>
<td><span data-ttu-id="04aa5-115"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="04aa5-115"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="04aa5-116">Um valor booliano que especifica se a hierarquia filho do objeto foi alterada. Esse parâmetro é usado para notificar o chamador de que alguns filhos do objeto especificado foram adicionados ou removidos.</span><span class="sxs-lookup"><span data-stu-id="04aa5-116">A Boolean value that specifies whether the child hierarchy for the object has changed.This parameter is used to notify the caller that some children for the specified object have been added or removed.</span></span> <span data-ttu-id="04aa5-117">Normalmente, a alteração da hierarquia é iniciada no lado do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="04aa5-117">Typically the hierarchy change is initiated on the device side.</span></span> <span data-ttu-id="04aa5-118">Os clientes podem precisar enumerar novamente os filhos dessa pasta para manter suas exibições atualizadas.</span><span class="sxs-lookup"><span data-stu-id="04aa5-118">Clients may have to re-enumerate this folder's children to keep their views up to date.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04aa5-119"><strong>WPD_EVENT_PARAMETER_EVENT_ID</strong></span><span class="sxs-lookup"><span data-stu-id="04aa5-119"><strong>WPD_EVENT_PARAMETER_EVENT_ID</strong></span></span></td>
<td><span data-ttu-id="04aa5-120"><strong>VT_CLSID</strong></span><span class="sxs-lookup"><span data-stu-id="04aa5-120"><strong>VT_CLSID</strong></span></span></td>
<td><span data-ttu-id="04aa5-121">Um valor que identifica um evento.</span><span class="sxs-lookup"><span data-stu-id="04aa5-121">A value that identifies an event.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04aa5-122"><strong>WPD_EVENT_PARAMETER_OBJECT_CREATION_COOKIE</strong></span><span class="sxs-lookup"><span data-stu-id="04aa5-122"><strong>WPD_EVENT_PARAMETER_OBJECT_CREATION_COOKIE</strong></span></span></td>
<td><span data-ttu-id="04aa5-123"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="04aa5-123"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="04aa5-124">O cookie é devolvido a um cliente quando ele solicita uma criação de objeto chamando o método <a href="/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata"><strong>IPortableDeviceContent:: CreateObjectWithPropertiesAndData</strong></a> . Esse parâmetro é adicionado como uma conveniência para ajudar o chamador a ligar um evento de objeto adicionado à solicitação enviada para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="04aa5-124">The cookie handed back to a client when it requests an object creation by calling the <a href="/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata"><strong>IPortableDeviceContent::CreateObjectWithPropertiesAndData</strong></a> method.This parameter is added as a convenience to help the caller tie an object-added event to the request it sent to create the object.</span></span> <span data-ttu-id="04aa5-125">O driver passa esse cookie de volta como o <strong>WPD_PROPERTY_OBJECT_MANAGEMENT_CONTEXT</strong> valor de retorno ao processar o comando <strong>WPD_COMMAND_OBJECT_MANAGEMENT_CREATE_OBJECT_WITH_PROPERTIES_AND_DATA</strong> .</span><span class="sxs-lookup"><span data-stu-id="04aa5-125">The driver hands this cookie back as the <strong>WPD_PROPERTY_OBJECT_MANAGEMENT_CONTEXT</strong> return value when processing the <strong>WPD_COMMAND_OBJECT_MANAGEMENT_CREATE_OBJECT_WITH_PROPERTIES_AND_DATA</strong> command.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04aa5-126"><strong>WPD_EVENT_PARAMETER_OBJECT_PARENT_PERSISTENT_UNIQUE_ID</strong></span><span class="sxs-lookup"><span data-stu-id="04aa5-126"><strong>WPD_EVENT_PARAMETER_OBJECT_PARENT_PERSISTENT_UNIQUE_ID</strong></span></span></td>
<td><span data-ttu-id="04aa5-127"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="04aa5-127"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="04aa5-128">Um valor que identifica exclusivamente o objeto pai.</span><span class="sxs-lookup"><span data-stu-id="04aa5-128">A value that uniquely identifies the parent object.</span></span> <span data-ttu-id="04aa5-129">Essa propriedade é semelhante a <strong>WPD_OBJECT_PARENT_ID</strong>, mas essa ID não é alterada entre sessões.</span><span class="sxs-lookup"><span data-stu-id="04aa5-129">This property is similar to <strong>WPD_OBJECT_PARENT_ID</strong>, but this ID does not change between sessions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04aa5-130"><strong>WPD_EVENT_PARAMETER_OPERATION_PROGRESS</strong></span><span class="sxs-lookup"><span data-stu-id="04aa5-130"><strong>WPD_EVENT_PARAMETER_OPERATION_PROGRESS</strong></span></span></td>
<td><span data-ttu-id="04aa5-131"><strong>VT_UI4</strong></span><span class="sxs-lookup"><span data-stu-id="04aa5-131"><strong>VT_UI4</strong></span></span></td>
<td><span data-ttu-id="04aa5-132">Um valor que especifica o progresso de uma operação em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="04aa5-132">A value that specifies the progress of a currently executing operation.</span></span> <span data-ttu-id="04aa5-133">O valor dessa propriedade pode variar de 0 a 100, com 100 indicando que a operação foi concluída.</span><span class="sxs-lookup"><span data-stu-id="04aa5-133">The value of this property can range from 0 to 100, with 100 indicating that the operation is complete.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04aa5-134"><strong>WPD_EVENT_PARAMETER_OPERATION_STATE</strong></span><span class="sxs-lookup"><span data-stu-id="04aa5-134"><strong>WPD_EVENT_PARAMETER_OPERATION_STATE</strong></span></span></td>
<td><span data-ttu-id="04aa5-135"><strong>VT_UI4</strong></span><span class="sxs-lookup"><span data-stu-id="04aa5-135"><strong>VT_UI4</strong></span></span></td>
<td><span data-ttu-id="04aa5-136">Um valor que indica o estado atual da operação, por exemplo, iniciado, em execução, parado e assim por diante. Os valores possíveis desse parâmetro são da enumeração <strong>WPD_OPERATION_STATES</strong> definida em PortableDevice. h.</span><span class="sxs-lookup"><span data-stu-id="04aa5-136">A value that indicates the current state of the operation, for example, started, running, stopped, and so on.This parameter's possible values are from the <strong>WPD_OPERATION_STATES</strong> enumeration defined in PortableDevice.h.</span></span> <span data-ttu-id="04aa5-137">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="04aa5-137">Possible values are:</span></span><br/> <dl> <span data-ttu-id="04aa5-138"><strong>WPD_OPERATION_STATE_UNSPECIFIED</strong></span><span class="sxs-lookup"><span data-stu-id="04aa5-138"><strong>WPD_OPERATION_STATE_UNSPECIFIED</strong></span></span><br /><span data-ttu-id="04aa5-139">
<strong>WPD_OPERATION_STATE_STARTED</strong></span><span class="sxs-lookup"><span data-stu-id="04aa5-139">
<strong>WPD_OPERATION_STATE_STARTED</strong></span></span><br /><span data-ttu-id="04aa5-140">
<strong>WPD_OPERATION_STATE_RUNNING</strong></span><span class="sxs-lookup"><span data-stu-id="04aa5-140">
<strong>WPD_OPERATION_STATE_RUNNING</strong></span></span><br /><span data-ttu-id="04aa5-141">
<strong>WPD_OPERATION_STATE_PAUSED</strong></span><span class="sxs-lookup"><span data-stu-id="04aa5-141">
<strong>WPD_OPERATION_STATE_PAUSED</strong></span></span><br /><span data-ttu-id="04aa5-142">
<strong>WPD_OPERATION_STATE_CANCELLED</strong></span><span class="sxs-lookup"><span data-stu-id="04aa5-142">
<strong>WPD_OPERATION_STATE_CANCELLED</strong></span></span><br /><span data-ttu-id="04aa5-143">
<strong>WPD_OPERATION_STATE_FINISHED</strong></span><span class="sxs-lookup"><span data-stu-id="04aa5-143">
<strong>WPD_OPERATION_STATE_FINISHED</strong></span></span><br /><span data-ttu-id="04aa5-144">
<strong>WPD_OPERATION_STATE_ABORTED</strong></span><span class="sxs-lookup"><span data-stu-id="04aa5-144">
<strong>WPD_OPERATION_STATE_ABORTED</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04aa5-145"><strong>WPD_EVENT_PARAMETER_PNP_DEVICE_ID</strong></span><span class="sxs-lookup"><span data-stu-id="04aa5-145"><strong>WPD_EVENT_PARAMETER_PNP_DEVICE_ID</strong></span></span></td>
<td><span data-ttu-id="04aa5-146"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="04aa5-146"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="04aa5-147">Um valor que especifica o dispositivo que originou o evento. Esse é o identificador de dispositivo ou serviço fornecido pelo sistema de plug-and-Play (PnP) e é a mesma cadeia de caracteres usada nos métodos <strong>IPortableDevice:: Open</strong>ou <a href="/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open"><strong>IPortableDeviceService:: Open</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="04aa5-147">A value that specifies the device that originated the event.This is the device or service identifier given by the Plug-and-Play (PnP) system, and is the same string used in the <strong>IPortableDevice::Open</strong>or <a href="/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open"><strong>IPortableDeviceService::Open</strong></a> methods.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04aa5-148"><strong>WPD_EVENT_PARAMETER_SERVICE_METHOD_CONTEXT</strong></span><span class="sxs-lookup"><span data-stu-id="04aa5-148"><strong>WPD_EVENT_PARAMETER_SERVICE_METHOD_CONTEXT</strong></span></span></td>
<td><span data-ttu-id="04aa5-149"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="04aa5-149"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="04aa5-150">Uma cadeia de caracteres que é usada por um driver WPD para identificar a operação de um método de serviço de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="04aa5-150">A string that is used by a WPD driver to identify the operation of a device-service method.</span></span> <span data-ttu-id="04aa5-151">Os aplicativos não devem usar esse parâmetro diretamente.</span><span class="sxs-lookup"><span data-stu-id="04aa5-151">Applications should not use this parameter directly.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="04aa5-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04aa5-152">Requirements</span></span>



| <span data-ttu-id="04aa5-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="04aa5-153">Requirement</span></span> | <span data-ttu-id="04aa5-154">Valor</span><span class="sxs-lookup"><span data-stu-id="04aa5-154">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="04aa5-155">parâmetro</span><span class="sxs-lookup"><span data-stu-id="04aa5-155">Header</span></span><br/> | <dl> <span data-ttu-id="04aa5-156"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="04aa5-156"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04aa5-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="04aa5-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04aa5-158">**Propriedades e atributos WPD**</span><span class="sxs-lookup"><span data-stu-id="04aa5-158">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




