---
description: A categoria de SENSOR de \_ \_ outra categoria contém sensores que dão suporte à classe personalizada no driver de classe HID.
ms.assetid: 866F7BF4-15CC-4F69-9510-B5858D47C4D0
title: SENSOR_CATEGORY_OTHER (sensores. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e26ece66ae74e873c48cd973cc447beec2dd8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010426"
---
# <a name="sensor_category_other"></a><span data-ttu-id="4ee50-103">Categoria de SENSOR \_ \_ outra</span><span class="sxs-lookup"><span data-stu-id="4ee50-103">SENSOR\_CATEGORY\_OTHER</span></span>

<span data-ttu-id="4ee50-104">A categoria de SENSOR de \_ \_ outra categoria contém sensores que dão suporte à classe personalizada no driver de classe HID.</span><span class="sxs-lookup"><span data-stu-id="4ee50-104">The SENSOR\_CATEGORY\_OTHER category contains sensors that support the Custom class in the HID Class driver.</span></span>

<dl> <dt>

<span data-ttu-id="4ee50-105"><span id="SENSOR_TYPE_CUSTOM"></span><span id="sensor_type_custom"></span>**tipo de SENSOR \_ \_ personalizado**</span><span class="sxs-lookup"><span data-stu-id="4ee50-105"><span id="SENSOR_TYPE_CUSTOM"></span><span id="sensor_type_custom"></span>**SENSOR\_TYPE\_CUSTOM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ee50-106">{E83AF229-8640-4D18-A213-E22675EBB2C3}</span><span class="sxs-lookup"><span data-stu-id="4ee50-106">{E83AF229-8640-4D18-A213-E22675EBB2C3}</span></span>
</dt> <dt>



<span data-ttu-id="4ee50-107">Sensor personalizado que dá suporte à classe personalizada no driver de classe HID.</span><span class="sxs-lookup"><span data-stu-id="4ee50-107">Custom sensor that supports the Custom class in the HID Class driver.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="4ee50-108">**Campos de dados definidos pela plataforma**</span><span class="sxs-lookup"><span data-stu-id="4ee50-108">**Platform-Defined Data Fields**</span></span>

<span data-ttu-id="4ee50-109">As chaves de propriedade definidas pela plataforma para essa categoria se baseiam no \_ GUID personalizado de tipo de dados do sensor \_ \_ \_ :</span><span class="sxs-lookup"><span data-stu-id="4ee50-109">Platform-defined property keys for this category are based on SENSOR\_DATA\_TYPE\_CUSTOM\_GUID:</span></span>

<span data-ttu-id="4ee50-110">{B14C764F-07CF-41E8-9D82-EBE3D0776A6F}</span><span class="sxs-lookup"><span data-stu-id="4ee50-110">{B14C764F-07CF-41E8-9D82-EBE3D0776A6F}</span></span>

<span data-ttu-id="4ee50-111">Essa categoria inclui os seguintes campos de dados definidos pela plataforma.</span><span class="sxs-lookup"><span data-stu-id="4ee50-111">This category includes the following platform-defined data fields.</span></span>



| <span data-ttu-id="4ee50-112">Nome do campo de dados e PID</span><span class="sxs-lookup"><span data-stu-id="4ee50-112">Data field name and PID</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="4ee50-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="4ee50-113">Description</span></span>                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_CUSTOM_USAGE"></span><span id="sensor_data_type_custom_usage"></span><dl> <span data-ttu-id="4ee50-114"><dt>**Sensor \_ \_ \_ \_ Uso personalizado de tipo de dados**</dt> <dt> (PID = 5)</dt></span><span class="sxs-lookup"><span data-stu-id="4ee50-114"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_USAGE**</dt> <dt> (PID = 5) </dt></span></span> </dl>                          | <span data-ttu-id="4ee50-115">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="4ee50-115">**VT\_UI4**</span></span><br/> <span data-ttu-id="4ee50-116">Um uso de HID que pode ser usado para distinguir vários sensores personalizados.</span><span class="sxs-lookup"><span data-stu-id="4ee50-116">A HID usage which can be used to distinguish multiple, custom sensors.</span></span><br/> |
| <span id="SENSOR_DATA_TYPE_CUSTOM_BOOLEAN_ARRAY"></span><span id="sensor_data_type_custom_boolean_array"></span><dl> <span data-ttu-id="4ee50-117"><dt>**Sensor \_ \_ \_ \_ \_ Matriz booleana personalizada de tipo de dados**</dt> <dt> (PID = 6)</dt></span><span class="sxs-lookup"><span data-stu-id="4ee50-117"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_BOOLEAN\_ARRAY**</dt> <dt> (PID = 6) </dt></span></span> </dl> | <span data-ttu-id="4ee50-118">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="4ee50-118">**VT\_UI4**</span></span><br/> <span data-ttu-id="4ee50-119">Uma matriz de valores Boolianos para um determinado sensor personalizado.</span><span class="sxs-lookup"><span data-stu-id="4ee50-119">An array of Boolean values for a given custom sensor.</span></span><br/>                  |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE1"></span><span id="sensor_data_type_custom_value1"></span><dl> <span data-ttu-id="4ee50-120"><dt>**Sensor \_ \_ \_ \_ Value1 personalizado de tipo de dados**</dt> <dt> (PID = 7)</dt></span><span class="sxs-lookup"><span data-stu-id="4ee50-120"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE1**</dt> <dt> (PID = 7) </dt></span></span> </dl>                       | <span data-ttu-id="4ee50-121">**VT \_ UI4 \| \| VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="4ee50-121">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="4ee50-122">Um dos seis valores disponíveis para um determinado sensor personalizado.</span><span class="sxs-lookup"><span data-stu-id="4ee50-122">One of six available values for a given custom sensor.</span></span><br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE2"></span><span id="sensor_data_type_custom_value2"></span><dl> <span data-ttu-id="4ee50-123"><dt>**Sensor \_ \_ \_ \_ VALUE2 personalizado de tipo de dados**</dt> <dt> (PID = 8)</dt></span><span class="sxs-lookup"><span data-stu-id="4ee50-123"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE2**</dt> <dt> (PID = 8) </dt></span></span> </dl>                       | <span data-ttu-id="4ee50-124">**VT \_ UI4 \| \| VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="4ee50-124">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="4ee50-125">Um dos seis valores disponíveis para um determinado sensor personalizado.</span><span class="sxs-lookup"><span data-stu-id="4ee50-125">One of six available values for a given custom sensor.</span></span><br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE3"></span><span id="sensor_data_type_custom_value3"></span><dl> <span data-ttu-id="4ee50-126"><dt>**Sensor \_ Tipo de dados \_ \_ Custom \_ VALUE3**</dt> <dt> (PID = 9)</dt></span><span class="sxs-lookup"><span data-stu-id="4ee50-126"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE3**</dt> <dt> (PID = 9) </dt></span></span> </dl>                       | <span data-ttu-id="4ee50-127">**VT \_ UI4 \| \| VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="4ee50-127">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="4ee50-128">Um dos seis valores disponíveis para um determinado sensor personalizado.</span><span class="sxs-lookup"><span data-stu-id="4ee50-128">One of six available values for a given custom sensor.</span></span><br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE4"></span><span id="sensor_data_type_custom_value4"></span><dl> <span data-ttu-id="4ee50-129"><dt>**Sensor \_ Tipo de dados \_ \_ Custom \_ VALUE4**</dt> <dt> (PID = 10)</dt></span><span class="sxs-lookup"><span data-stu-id="4ee50-129"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE4**</dt> <dt> (PID = 10) </dt></span></span> </dl>                      | <span data-ttu-id="4ee50-130">**VT \_ UI4 \| \| VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="4ee50-130">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="4ee50-131">Um dos seis valores disponíveis para um determinado sensor personalizado.</span><span class="sxs-lookup"><span data-stu-id="4ee50-131">One of six available values for a given custom sensor.</span></span><br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE5"></span><span id="sensor_data_type_custom_value5"></span><dl> <span data-ttu-id="4ee50-132"><dt>**Sensor \_ Tipo de dados \_ \_ Custom \_ VALUE5**</dt> <dt> (PID = 11)</dt></span><span class="sxs-lookup"><span data-stu-id="4ee50-132"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE5**</dt> <dt> (PID = 11) </dt></span></span> </dl>                      | <span data-ttu-id="4ee50-133">**VT \_ UI4 \| \| VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="4ee50-133">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="4ee50-134">Um dos seis valores disponíveis para um determinado sensor personalizado.</span><span class="sxs-lookup"><span data-stu-id="4ee50-134">One of six available values for a given custom sensor.</span></span><br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE6"></span><span id="sensor_data_type_custom_value6"></span><dl> <span data-ttu-id="4ee50-135"><dt>**Sensor \_ Tipo de dados \_ \_ Custom \_ VALUE6**</dt> <dt> (PID = 12)</dt></span><span class="sxs-lookup"><span data-stu-id="4ee50-135"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE6**</dt> <dt> (PID = 12) </dt></span></span> </dl>                      | <span data-ttu-id="4ee50-136">**VT \_ UI4 \| \| VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="4ee50-136">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="4ee50-137">Um dos seis valores disponíveis para um determinado sensor personalizado.</span><span class="sxs-lookup"><span data-stu-id="4ee50-137">One of six available values for a given custom sensor.</span></span><br/>       |



## <a name="remarks"></a><span data-ttu-id="4ee50-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ee50-138">Remarks</span></span>

<span data-ttu-id="4ee50-139">Um sensor que dá suporte à classe genérica no driver de classe HID será mapeado para uma das outras categorias definidas (biométrica, elétrica, ambiental e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="4ee50-139">A sensor that supports the Generic class in the HID class driver will map to one of the other defined categories (biometric, electrical, environmental, and so on).</span></span>

## <a name="requirements"></a><span data-ttu-id="4ee50-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ee50-140">Requirements</span></span>



| <span data-ttu-id="4ee50-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ee50-141">Requirement</span></span> | <span data-ttu-id="4ee50-142">Valor</span><span class="sxs-lookup"><span data-stu-id="4ee50-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4ee50-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ee50-143">Minimum supported client</span></span><br/> | <span data-ttu-id="4ee50-144">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4ee50-144">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4ee50-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ee50-145">Minimum supported server</span></span><br/> | <span data-ttu-id="4ee50-146">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4ee50-146">None supported</span></span><br/>                                                            |
| <span data-ttu-id="4ee50-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4ee50-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ee50-148"><dt>Sensores. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ee50-148"><dt>Sensors.h</dt></span></span> </dl> |



 

 




