---
description: A \_ categoria leve categoria de sensor \_ contém sensores que fornecem informações sobre características de luz.
ms.assetid: 0327bda5-f1d7-476d-9f0f-f4d60a6a106f
title: SENSOR_CATEGORY_LIGHT (sensores. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca14bba297a8f445312873fc810e7d0b5ba13a4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826961"
---
# <a name="sensor_category_light"></a><span data-ttu-id="48238-103">\_luz da categoria do sensor \_</span><span class="sxs-lookup"><span data-stu-id="48238-103">SENSOR\_CATEGORY\_LIGHT</span></span>

<span data-ttu-id="48238-104">A \_ categoria leve categoria de sensor \_ contém sensores que fornecem informações sobre características de luz.</span><span class="sxs-lookup"><span data-stu-id="48238-104">The SENSOR\_CATEGORY\_LIGHT category contains sensors that provide information about characteristics of light.</span></span>

<span data-ttu-id="48238-105">**Tipos de sensor definidos pela plataforma**</span><span class="sxs-lookup"><span data-stu-id="48238-105">**Platform-Defined Sensor Types**</span></span>

<span data-ttu-id="48238-106">Essa categoria inclui os seguintes tipos de sensor definidos pela plataforma.</span><span class="sxs-lookup"><span data-stu-id="48238-106">This category includes the following platform-defined sensor types.</span></span>



| <span data-ttu-id="48238-107">Tipo de sensor</span><span class="sxs-lookup"><span data-stu-id="48238-107">Sensor type</span></span>                                                                                                                                                                                                                                                                                     | <span data-ttu-id="48238-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="48238-108">Description</span></span>                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------|
| <span id="SENSOR_TYPE_AMBIENT_LIGHT"></span><span id="sensor_type_ambient_light"></span><dl> <span data-ttu-id="48238-109"><dt>**Sensor \_ TIPO \_ de \_ luz ambiente**</dt> <dt>{97F115C8-599A-4153-8894-D2D12899918A}</dt></span><span class="sxs-lookup"><span data-stu-id="48238-109"><dt>**SENSOR\_TYPE\_AMBIENT\_LIGHT**</dt> <dt>{97F115C8-599A-4153-8894-D2D12899918A}</dt></span></span> </dl> | <span data-ttu-id="48238-110">Sensores de luz ambiente.</span><span class="sxs-lookup"><span data-stu-id="48238-110">Ambient light sensors.</span></span><br/> |



<span data-ttu-id="48238-111">**Campos de dados definidos pela plataforma**</span><span class="sxs-lookup"><span data-stu-id="48238-111">**Platform-Defined Data Fields**</span></span>

<span data-ttu-id="48238-112">As chaves de propriedade definidas pela plataforma para esta categoria são baseadas no tipo de dados do SENSOR \_ \_ GUID de \_ luz \_ :</span><span class="sxs-lookup"><span data-stu-id="48238-112">Platform-defined property keys for this category are based on SENSOR\_DATA\_TYPE\_LIGHT\_GUID:</span></span>

<span data-ttu-id="48238-113">{E4C77CE2-DCB7-46E9-8439-4FEC548833A6}</span><span class="sxs-lookup"><span data-stu-id="48238-113">{E4C77CE2-DCB7-46E9-8439-4FEC548833A6}</span></span>

<span data-ttu-id="48238-114">Essa categoria inclui os seguintes campos de dados definidos pela plataforma.</span><span class="sxs-lookup"><span data-stu-id="48238-114">This category includes the following platform-defined data fields.</span></span>



| <span data-ttu-id="48238-115">Nome do campo de dados e PID</span><span class="sxs-lookup"><span data-stu-id="48238-115">Data field name and PID</span></span>                                                                                                                                                                                                                                                                                                | <span data-ttu-id="48238-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="48238-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_LIGHT_CHROMACITY__"></span><span id="sensor_data_type_light_chromacity__"></span><dl> <span data-ttu-id="48238-117"><dt> **Tipo de dados do sensor \_ \_ \_ \_ CHROMACITY claro**</dt> <dt>(PID = 4)</dt></span><span class="sxs-lookup"><span data-stu-id="48238-117"><dt>**SENSOR\_DATA\_TYPE\_LIGHT\_CHROMACITY** </dt> <dt> (PID = 4) </dt></span></span> </dl>                     | <span data-ttu-id="48238-118">**\_UI1 de vetor \| VT \_ VT**</span><span class="sxs-lookup"><span data-stu-id="48238-118">**VT\_VECTOR\|VT\_UI1**</span></span><br/> <span data-ttu-id="48238-119">A desvio como uma matriz contada de valores float.</span><span class="sxs-lookup"><span data-stu-id="48238-119">Chromaticity as a counted array of float values.</span></span><br/> <span data-ttu-id="48238-120">Os dados para tipos de vetor são sempre serializados como **VT \_ UI1** (uma matriz de caracteres não assinados de 1 byte).</span><span class="sxs-lookup"><span data-stu-id="48238-120">Data for vector types is always serialized as **VT\_UI1** (an array of unsigned, 1-byte characters).</span></span> <span data-ttu-id="48238-121">Esse campo de dados realmente contém cada valor como um valor real de 4 bytes do IEEE (**VT \_ R4**).</span><span class="sxs-lookup"><span data-stu-id="48238-121">This data field actually contains each value as an IEEE 4-byte real value (**VT\_R4**).</span></span><br/> <span data-ttu-id="48238-122">Para obter informações sobre como trabalhar com matrizes, consulte [Recuperando tipos de vetor](retrieving-vector-types.md).</span><span class="sxs-lookup"><span data-stu-id="48238-122">For information about working with arrays, see [Retrieving Vector Types](retrieving-vector-types.md).</span></span><br/> |
| <span id="SENSOR_DATA_TYPE_LIGHT_LEVEL_LUX"></span><span id="sensor_data_type_light_level_lux"></span><dl> <span data-ttu-id="48238-123"><dt>**Sensor \_ Tipo de dados \_ \_ \_ \_ Lux de nível claro**</dt> <dt> (PID = 2)</dt></span><span class="sxs-lookup"><span data-stu-id="48238-123"><dt>**SENSOR\_DATA\_TYPE\_LIGHT\_LEVEL\_LUX**</dt> <dt> (PID = 2) </dt></span></span> </dl>                            | <span data-ttu-id="48238-124">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="48238-124">**VT\_R4**</span></span><br/> <span data-ttu-id="48238-125">Nível de Illuminance, em Lux.</span><span class="sxs-lookup"><span data-stu-id="48238-125">Illuminance level, in lux.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SENSOR_DATA_TYPE_LIGHT_TEMPERATURE_KELVIN"></span><span id="sensor_data_type_light_temperature_kelvin"></span><dl> <span data-ttu-id="48238-126"><dt>**Sensor \_ Tipo de dados \_ \_ \_ temperatura clara \_ Kelvin**</dt> <dt> (PID = 3)</dt></span><span class="sxs-lookup"><span data-stu-id="48238-126"><dt>**SENSOR\_DATA\_TYPE\_LIGHT\_TEMPERATURE\_KELVIN**</dt> <dt> (PID = 3) </dt></span></span> </dl> | <span data-ttu-id="48238-127">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="48238-127">**VT\_R4**</span></span><br/> <span data-ttu-id="48238-128">Temperatura de cor, em graus Kelvin.</span><span class="sxs-lookup"><span data-stu-id="48238-128">Color temperature, in degrees Kelvin.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                   |



## <a name="requirements"></a><span data-ttu-id="48238-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48238-129">Requirements</span></span>



| <span data-ttu-id="48238-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="48238-130">Requirement</span></span> | <span data-ttu-id="48238-131">Valor</span><span class="sxs-lookup"><span data-stu-id="48238-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="48238-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48238-132">Minimum supported client</span></span><br/> | <span data-ttu-id="48238-133">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="48238-133">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="48238-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48238-134">Minimum supported server</span></span><br/> | <span data-ttu-id="48238-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="48238-135">None supported</span></span><br/>                                                            |
| <span data-ttu-id="48238-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="48238-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="48238-137"><dt>Sensores. h</dt></span><span class="sxs-lookup"><span data-stu-id="48238-137"><dt>Sensors.h</dt></span></span> </dl> |



 

 




