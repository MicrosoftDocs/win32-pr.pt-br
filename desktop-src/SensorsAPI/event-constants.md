---
description: O sensor do Windows e a plataforma de localização definem constantes para eventos de driver. O sensor manfuactureres também pode definir suas próprias constantes.
ms.assetid: ca61c912-bce5-4e41-ab48-40615d5b93ba
title: Constantes de evento (sensores. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc9fb3ced92c1fe263538f2ce27c3fc65fdd7676
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753091"
---
# <a name="event-constants-sensorsh"></a><span data-ttu-id="b7fa0-104">Constantes de evento (sensores. h)</span><span class="sxs-lookup"><span data-stu-id="b7fa0-104">Event Constants (Sensors.h)</span></span>

<span data-ttu-id="b7fa0-105">O sensor do Windows e a plataforma de localização definem constantes para eventos de driver.</span><span class="sxs-lookup"><span data-stu-id="b7fa0-105">The Windows Sensor and Location platform defines constants for driver events.</span></span> <span data-ttu-id="b7fa0-106">O sensor manfuactureres também pode definir suas próprias constantes.</span><span class="sxs-lookup"><span data-stu-id="b7fa0-106">Sensor manfuactureres can also define their own constants.</span></span>

<span data-ttu-id="b7fa0-107">**Tipos de evento de sensor**</span><span class="sxs-lookup"><span data-stu-id="b7fa0-107">**Sensor Event Types**</span></span>

<span data-ttu-id="b7fa0-108">A plataforma define os seguintes identificadores de tipo de evento de sensor.</span><span class="sxs-lookup"><span data-stu-id="b7fa0-108">The platform defines the following sensor event type identifiers.</span></span>



| <span data-ttu-id="b7fa0-109">Tipo de evento de sensor</span><span class="sxs-lookup"><span data-stu-id="b7fa0-109">Sensor event type</span></span>                                                                                                                                                                                                                                                                                                    | <span data-ttu-id="b7fa0-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7fa0-110">Description</span></span>                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_EVENT_ACCELEROMETER_SHAKE"></span><span id="sensor_event_accelerometer_shake"></span><dl> <span data-ttu-id="b7fa0-111"><dt>**Sensor \_ \_ \_ Agitar o ACELERÔMETRO de evento**</dt> <dt>{825F5A94-0F48-4396-9CA0-6ECB5C99D915}</dt></span><span class="sxs-lookup"><span data-stu-id="b7fa0-111"><dt>**SENSOR\_EVENT\_ACCELEROMETER\_SHAKE**</dt> <dt>{825F5A94-0F48-4396-9CA0-6ECB5C99D915}</dt></span></span> </dl> | <span data-ttu-id="b7fa0-112">Indica que o dispositivo foi Shaken.</span><span class="sxs-lookup"><span data-stu-id="b7fa0-112">Indicates that the device was shaken.</span></span><br/>                                                                                                                                                                                                                                                                      |
| <span id="SENSOR_EVENT_DATA_UPDATED"></span><span id="sensor_event_data_updated"></span><dl> <span data-ttu-id="b7fa0-113"><dt>**Sensor \_ Dados de evento \_ \_ atualizados**</dt> <dt>{2ED0F2A4-0087-41D3-87DB-6773370B3C88}</dt></span><span class="sxs-lookup"><span data-stu-id="b7fa0-113"><dt>**SENSOR\_EVENT\_DATA\_UPDATED**</dt> <dt>{2ED0F2A4-0087-41D3-87DB-6773370B3C88}</dt></span></span> </dl>                      | <span data-ttu-id="b7fa0-114">Indica que novos dados estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="b7fa0-114">Indicates that new data is available.</span></span><br/>                                                                                                                                                                                                                                                                      |
| <span id="SENSOR_EVENT_PROPERTY_CHANGED"></span><span id="sensor_event_property_changed"></span><dl> <span data-ttu-id="b7fa0-115"><dt>**Sensor \_ Propriedade de evento \_ \_ alterada**</dt> <dt>{2358F099-84C9-4D3D-90DF-C2421E2B2045}</dt></span><span class="sxs-lookup"><span data-stu-id="b7fa0-115"><dt>**SENSOR\_EVENT\_PROPERTY\_CHANGED**</dt> <dt>{2358F099-84C9-4D3D-90DF-C2421E2B2045}</dt></span></span> </dl>          | <span data-ttu-id="b7fa0-116">Indica que um valor de propriedade foi alterado.</span><span class="sxs-lookup"><span data-stu-id="b7fa0-116">Indicates that a property value changed.</span></span> <span data-ttu-id="b7fa0-117">Verifique a interface [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) , passada pelo parâmetro *PEventData* para [**OnEvent**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onevent), para determinar qual propriedade foi alterada e seu novo valor.</span><span class="sxs-lookup"><span data-stu-id="b7fa0-117">Check the [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) interface, passed through the *pEventData* parameter to [**OnEvent**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onevent), to determine which property changed and its new value.</span></span><br/> |
| <span id="SENSOR_EVENT_STATE_CHANGED"></span><span id="sensor_event_state_changed"></span><dl> <span data-ttu-id="b7fa0-118"><dt>**Sensor \_ Estado do evento \_ \_ alterado**</dt> <dt>{BFD96016-6BD7-4560-AD34-F2F6607E8F81}</dt></span><span class="sxs-lookup"><span data-stu-id="b7fa0-118"><dt>**SENSOR\_EVENT\_STATE\_CHANGED**</dt> <dt>{BFD96016-6BD7-4560-AD34-F2F6607E8F81}</dt></span></span> </dl>                   | <span data-ttu-id="b7fa0-119">Indica uma alteração do estado operacional, por exemplo, do estado do SENSOR \_ \_ inicializando para o estado do sensor \_ \_ pronto.</span><span class="sxs-lookup"><span data-stu-id="b7fa0-119">Indicates a change of operational state, for example, from SENSOR\_STATE\_INITIALIZING to SENSOR\_STATE\_READY.</span></span><br/>                                                                                                                                                                                            |



<span data-ttu-id="b7fa0-120">**Evento de sensor PROPERTYKEYs**</span><span class="sxs-lookup"><span data-stu-id="b7fa0-120">**Sensor Event PROPERTYKEYs**</span></span>

<span data-ttu-id="b7fa0-121">As chaves de propriedade definidas pela plataforma para eventos são baseadas no seguinte GUID:</span><span class="sxs-lookup"><span data-stu-id="b7fa0-121">Platform-defined property keys for events are based on the following GUID:</span></span>

<span data-ttu-id="b7fa0-122">{64346E30-8728-4B34-BDF6-4F52442C5C28}</span><span class="sxs-lookup"><span data-stu-id="b7fa0-122">{64346E30-8728-4B34-BDF6-4F52442C5C28}</span></span>

<span data-ttu-id="b7fa0-123">A plataforma de sensor define os seguintes **PROPERTYKEY** s que identificam os parâmetros de evento do sensor.</span><span class="sxs-lookup"><span data-stu-id="b7fa0-123">The sensor platform defines the following **PROPERTYKEY** s that identify sensor event parameters.</span></span>



| <span data-ttu-id="b7fa0-124">O evento de sensor PROPERTYKEY e PID</span><span class="sxs-lookup"><span data-stu-id="b7fa0-124">Sensor event PROPERTYKEY and PID</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="b7fa0-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7fa0-125">Description</span></span>                                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_EVENT_PARAMETER_EVENT_ID"></span><span id="sensor_event_parameter_event_id"></span><dl> <span data-ttu-id="b7fa0-126"><dt>**Sensor \_ \_ID do \_ evento \_ de parâmetro de evento**</dt> <dt>(PID = 2)</dt></span><span class="sxs-lookup"><span data-stu-id="b7fa0-126"><dt>**SENSOR\_EVENT\_PARAMETER\_EVENT\_ID**</dt> <dt>(PID = 2)</dt></span></span> </dl> | <span data-ttu-id="b7fa0-127">Indica que o valor de **GUID** em [IPORTABLEDEVICEVALUES](/previous-versions//ms740012(v=vs.85)) é uma ID de tipo de evento, como dados de evento de sensor \_ \_ \_ atualizados.</span><span class="sxs-lookup"><span data-stu-id="b7fa0-127">Indicates that the **GUID** value in [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) is an event type ID, such as SENSOR\_EVENT\_DATA\_UPDATED.</span></span><br/> |
| <span id="SENSOR_EVENT_PARAMETER_STATE"></span><span id="sensor_event_parameter_state"></span><dl> <span data-ttu-id="b7fa0-128"><dt>**Sensor \_ \_ \_ Estado do parâmetro de evento**</dt> <dt>(PID = 3)</dt></span><span class="sxs-lookup"><span data-stu-id="b7fa0-128"><dt>**SENSOR\_EVENT\_PARAMETER\_STATE**</dt> <dt>(PID = 3)</dt></span></span> </dl>           | <span data-ttu-id="b7fa0-129">Indica que o valor inteiro sem sinal em **IPortableDeviceValues** é um estado de sensor, como \_ pronto para o estado do sensor \_ .</span><span class="sxs-lookup"><span data-stu-id="b7fa0-129">Indicates that the unsigned integer value in **IPortableDeviceValues** is a sensor state, such as SENSOR\_STATE\_READY.</span></span><br/>                                                  |



<span data-ttu-id="b7fa0-130">**Erro de sensor PROPERTYKEYs**</span><span class="sxs-lookup"><span data-stu-id="b7fa0-130">**Sensor Error PROPERTYKEYs**</span></span>

<span data-ttu-id="b7fa0-131">As chaves de propriedade definidas pela plataforma para erros serão baseadas no seguinte GUID:</span><span class="sxs-lookup"><span data-stu-id="b7fa0-131">Platform-defined property keys for errors will be based on the following GUID:</span></span>

<span data-ttu-id="b7fa0-132">{77112BCD-FCE1-4f43-B8B8-A88256ADB4B3}</span><span class="sxs-lookup"><span data-stu-id="b7fa0-132">{77112BCD-FCE1-4f43-B8B8-A88256ADB4B3}</span></span>

<span data-ttu-id="b7fa0-133">A plataforma do sensor reserva esse GUID para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="b7fa0-133">The sensor platform reserves this GUID for future use.</span></span>

<dl></dl>

## <a name="requirements"></a><span data-ttu-id="b7fa0-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7fa0-134">Requirements</span></span>



| <span data-ttu-id="b7fa0-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7fa0-135">Requirement</span></span> | <span data-ttu-id="b7fa0-136">Valor</span><span class="sxs-lookup"><span data-stu-id="b7fa0-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b7fa0-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7fa0-137">Minimum supported client</span></span><br/> | <span data-ttu-id="b7fa0-138">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b7fa0-138">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b7fa0-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7fa0-139">Minimum supported server</span></span><br/> | <span data-ttu-id="b7fa0-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b7fa0-140">None supported</span></span><br/>                                                            |
| <span data-ttu-id="b7fa0-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b7fa0-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7fa0-142"><dt>Sensores. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7fa0-142"><dt>Sensors.h</dt></span></span> </dl> |



 

