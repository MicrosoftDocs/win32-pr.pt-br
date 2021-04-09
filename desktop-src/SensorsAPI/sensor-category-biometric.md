---
description: A \_ categoria biométrica da categoria do sensor \_ contém sensores que fornecem informações sobre seres de vida.
ms.assetid: dfc7ad46-c13b-46d1-8854-0d93ecaac55a
title: SENSOR_CATEGORY_BIOMETRIC (sensores. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71660c7bc94037c21502c91e017a8eba369766a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090169"
---
# <a name="sensor_category_biometric"></a><span data-ttu-id="fc8af-103">\_biometria da categoria de sensor \_</span><span class="sxs-lookup"><span data-stu-id="fc8af-103">SENSOR\_CATEGORY\_BIOMETRIC</span></span>

<span data-ttu-id="fc8af-104">A \_ categoria biométrica da categoria do sensor \_ contém sensores que fornecem informações sobre seres de vida.</span><span class="sxs-lookup"><span data-stu-id="fc8af-104">The SENSOR\_CATEGORY\_BIOMETRIC category contains sensors that provide information about living beings.</span></span>

<span data-ttu-id="fc8af-105">**Tipos de sensor definidos pela plataforma**</span><span class="sxs-lookup"><span data-stu-id="fc8af-105">**Platform-Defined Sensor Types**</span></span>

<span data-ttu-id="fc8af-106">Essa categoria inclui os seguintes tipos de sensor definidos pela plataforma.</span><span class="sxs-lookup"><span data-stu-id="fc8af-106">This category includes the following platform-defined sensor types.</span></span>



| <span data-ttu-id="fc8af-107">Tipo de sensor</span><span class="sxs-lookup"><span data-stu-id="fc8af-107">Sensor type</span></span>                                                                                                                                                                                                                                                                                           | <span data-ttu-id="fc8af-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc8af-108">Description</span></span>                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------|
| <span id="SENSOR_TYPE_HUMAN_PRESENCE"></span><span id="sensor_type_human_presence"></span><dl> <span data-ttu-id="fc8af-109"><dt>**Sensor \_ TIPO \_ de \_ presença humana**</dt> <dt>{C138C12B-AD52-451C-9375-87F518FF10C6}</dt></span><span class="sxs-lookup"><span data-stu-id="fc8af-109"><dt>**SENSOR\_TYPE\_HUMAN\_PRESENCE**</dt> <dt>{C138C12B-AD52-451C-9375-87F518FF10C6}</dt></span></span> </dl>    | <span data-ttu-id="fc8af-110">Sensores que detectam a presença humana.</span><span class="sxs-lookup"><span data-stu-id="fc8af-110">Sensors that detect human presence.</span></span><br/>  |
| <span id="SENSOR_TYPE_HUMAN_PROXIMITY"></span><span id="sensor_type_human_proximity"></span><dl> <span data-ttu-id="fc8af-111"><dt>**Sensor \_ Digite \_ a \_ proximidade humana**</dt> <dt>{5220DAE9-3179-4430-9F90-06266D2A34DE}</dt></span><span class="sxs-lookup"><span data-stu-id="fc8af-111"><dt>**SENSOR\_TYPE\_HUMAN\_PROXIMITY**</dt> <dt>{5220DAE9-3179-4430-9F90-06266D2A34DE}</dt></span></span> </dl> | <span data-ttu-id="fc8af-112">Sensores que detectam proximidade humana.</span><span class="sxs-lookup"><span data-stu-id="fc8af-112">Sensors that detect human proximity.</span></span><br/> |
| <span id="SENSOR_TYPE_TOUCH"></span><span id="sensor_type_touch"></span><dl> <span data-ttu-id="fc8af-113"><dt>**Sensor \_ Digite \_ Touch**</dt> <dt>{17DB3018-06C4-4F7D-81AF-9274B7599C27}</dt></span><span class="sxs-lookup"><span data-stu-id="fc8af-113"><dt>**SENSOR\_TYPE\_TOUCH**</dt> <dt>{17DB3018-06C4-4F7D-81AF-9274B7599C27}</dt></span></span> </dl>                                | <span data-ttu-id="fc8af-114">Sensores de toque.</span><span class="sxs-lookup"><span data-stu-id="fc8af-114">Touch sensors.</span></span><br/>                       |



<span data-ttu-id="fc8af-115">**Campos de dados definidos pela plataforma**</span><span class="sxs-lookup"><span data-stu-id="fc8af-115">**Platform-Defined Data Fields**</span></span>

<span data-ttu-id="fc8af-116">As chaves de propriedade definidas pela plataforma para esta categoria são baseadas no tipo de dados do SENSOR \_ \_ \_ GUID biométrico \_ :</span><span class="sxs-lookup"><span data-stu-id="fc8af-116">Platform-defined property keys for this category are based on SENSOR\_DATA\_TYPE\_BIOMETRIC\_GUID:</span></span>

<span data-ttu-id="fc8af-117">{2299288A-6D9E-4B0B-B7EC-3528F89E40AF}</span><span class="sxs-lookup"><span data-stu-id="fc8af-117">{2299288A-6D9E-4B0B-B7EC-3528F89E40AF}</span></span>

<span data-ttu-id="fc8af-118">Essa categoria inclui os seguintes campos de dados definidos pela plataforma.</span><span class="sxs-lookup"><span data-stu-id="fc8af-118">This category includes the following platform-defined data fields.</span></span>



| <span data-ttu-id="fc8af-119">Nome do campo de dados e PID</span><span class="sxs-lookup"><span data-stu-id="fc8af-119">Data field name and PID</span></span>                                                                                                                                                                                                                                                                                         | <span data-ttu-id="fc8af-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc8af-120">Description</span></span>                                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_HUMAN_PRESENCE"></span><span id="sensor_data_type_human_presence"></span><dl> <span data-ttu-id="fc8af-121"><dt>**Sensor \_ \_ \_ \_ Presença humana de tipo de dados**</dt> <dt>(PID = 2)</dt></span><span class="sxs-lookup"><span data-stu-id="fc8af-121"><dt>**SENSOR\_DATA\_TYPE\_HUMAN\_PRESENCE**</dt> <dt>(PID = 2) </dt></span></span> </dl>                          | <span data-ttu-id="fc8af-122">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="fc8af-122">**VT\_BOOL**</span></span><br/> <span data-ttu-id="fc8af-123">**Verdadeiro** quando um humano estiver usando o computador.</span><span class="sxs-lookup"><span data-stu-id="fc8af-123">**TRUE** when a human is using the computer.</span></span><br/>                           |
| <span id="SENSOR_DATA_TYPE_HUMAN_PROXIMITY_METERS"></span><span id="sensor_data_type_human_proximity_meters"></span><dl> <span data-ttu-id="fc8af-124"><dt>**Sensor \_ \_ \_ \_ \_ Medidores de proximidade humana do tipo de dados**</dt> <dt>(PID = 3)</dt></span><span class="sxs-lookup"><span data-stu-id="fc8af-124"><dt>**SENSOR\_DATA\_TYPE\_HUMAN\_PROXIMITY\_METERS**</dt> <dt>(PID = 3) </dt></span></span> </dl> | <span data-ttu-id="fc8af-125">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="fc8af-125">**VT\_R4**</span></span><br/> <span data-ttu-id="fc8af-126">Distância entre um humano e o computador, em metros.</span><span class="sxs-lookup"><span data-stu-id="fc8af-126">Distance between a human and the computer, in meters.</span></span><br/>                    |
| <span id="SENSOR_DATA_TYPE_TOUCH_STATE"></span><span id="sensor_data_type_touch_state"></span><dl> <span data-ttu-id="fc8af-127"><dt>**Sensor \_ \_Estado de \_ toque \_ do tipo de dados**</dt> <dt>(PID = 4)</dt></span><span class="sxs-lookup"><span data-stu-id="fc8af-127"><dt>**SENSOR\_DATA\_TYPE\_TOUCH\_STATE**</dt> <dt>(PID = 4) </dt></span></span> </dl>                                   | <span data-ttu-id="fc8af-128">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="fc8af-128">**VT\_BOOL**</span></span><br/> <span data-ttu-id="fc8af-129">**Verdadeiro** quando o sensor de toque está sendo tocado; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="fc8af-129">**TRUE** when the touch sensor is being touched; otherwise, **FALSE**.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="fc8af-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc8af-130">Requirements</span></span>



| <span data-ttu-id="fc8af-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc8af-131">Requirement</span></span> | <span data-ttu-id="fc8af-132">Valor</span><span class="sxs-lookup"><span data-stu-id="fc8af-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fc8af-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc8af-133">Minimum supported client</span></span><br/> | <span data-ttu-id="fc8af-134">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="fc8af-134">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fc8af-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc8af-135">Minimum supported server</span></span><br/> | <span data-ttu-id="fc8af-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="fc8af-136">None supported</span></span><br/>                                                            |
| <span data-ttu-id="fc8af-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fc8af-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc8af-138"><dt>Sensores. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc8af-138"><dt>Sensors.h</dt></span></span> </dl> |



 

 




