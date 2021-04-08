---
description: A categoria de scanner de categoria de SENSOR \_ \_ contém sensores que fornecem informações obtidas pela verificação.
ms.assetid: 98a772c9-2a21-489f-ad8d-3b772b7ff892
title: SENSOR_CATEGORY_SCANNER (sensores. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b38fdb3358ff3ce2ae96ce901972cc6842a0d1b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920801"
---
# <a name="sensor_category_scanner"></a><span data-ttu-id="ef52d-103">\_scanner de categoria de sensor \_</span><span class="sxs-lookup"><span data-stu-id="ef52d-103">SENSOR\_CATEGORY\_SCANNER</span></span>

<span data-ttu-id="ef52d-104">A categoria de scanner de categoria de SENSOR \_ \_ contém sensores que fornecem informações obtidas pela verificação.</span><span class="sxs-lookup"><span data-stu-id="ef52d-104">The SENSOR\_CATEGORY\_SCANNER category contains sensors that provide information that is obtained by scanning.</span></span>

<span data-ttu-id="ef52d-105">**Tipos de sensor definidos pela plataforma**</span><span class="sxs-lookup"><span data-stu-id="ef52d-105">**Platform-Defined Sensor Types**</span></span>

<span data-ttu-id="ef52d-106">Essa categoria inclui os seguintes tipos de sensor definidos pela plataforma.</span><span class="sxs-lookup"><span data-stu-id="ef52d-106">This category includes the following platform-defined sensor types.</span></span>



| <span data-ttu-id="ef52d-107">Tipo de sensor</span><span class="sxs-lookup"><span data-stu-id="ef52d-107">Sensor type</span></span>                                                                                                                                                                                                                                                                                           | <span data-ttu-id="ef52d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ef52d-108">Description</span></span>                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| <span id="SENSOR_TYPE_BARCODE_SCANNER"></span><span id="sensor_type_barcode_scanner"></span><dl> <span data-ttu-id="ef52d-109"><dt>**Sensor \_ TIPO de \_ \_ scanner de código de barras**</dt> <dt>{990B3D8F-85BB-45FF-914D-998C04F372DF}</dt></span><span class="sxs-lookup"><span data-stu-id="ef52d-109"><dt>**SENSOR\_TYPE\_BARCODE\_SCANNER**</dt> <dt>{990B3D8F-85BB-45FF-914D-998C04F372DF}</dt></span></span> </dl> | <span data-ttu-id="ef52d-110">Sensores que usam a verificação óptica para ler códigos de barras.</span><span class="sxs-lookup"><span data-stu-id="ef52d-110">Sensors that use optical scanning to read bar codes.</span></span><br/> |
| <span id="SENSOR_TYPE_RFID_SCANNER"></span><span id="sensor_type_rfid_scanner"></span><dl> <span data-ttu-id="ef52d-111"><dt>**Sensor \_ TIPO \_ de \_ scanner RFID**</dt> <dt>{44328EF5-02DD-4E8D-AD5D-9249832B2ECA}</dt></span><span class="sxs-lookup"><span data-stu-id="ef52d-111"><dt>**SENSOR\_TYPE\_RFID\_SCANNER**</dt> <dt>{44328EF5-02DD-4E8D-AD5D-9249832B2ECA}</dt></span></span> </dl>          | <span data-ttu-id="ef52d-112">Sensores de verificação de ID de frequência de rádio.</span><span class="sxs-lookup"><span data-stu-id="ef52d-112">Radio-frequency ID scanning sensors.</span></span><br/>                 |



<span data-ttu-id="ef52d-113">**Campos de dados definidos pela plataforma**</span><span class="sxs-lookup"><span data-stu-id="ef52d-113">**Platform-Defined Data Fields**</span></span>

<span data-ttu-id="ef52d-114">As chaves de propriedade definidas pela plataforma para esta categoria são baseadas no tipo de dados do SENSOR \_ \_ GUID do \_ scanner \_ :</span><span class="sxs-lookup"><span data-stu-id="ef52d-114">Platform-defined property keys for this category are based on SENSOR\_DATA\_TYPE\_SCANNER\_GUID:</span></span>

<span data-ttu-id="ef52d-115">{D7A59A3C-3421-44AB-8D3A-9DE8AB6C4CAE}</span><span class="sxs-lookup"><span data-stu-id="ef52d-115">{D7A59A3C-3421-44AB-8D3A-9DE8AB6C4CAE}</span></span>

<span data-ttu-id="ef52d-116">Essa categoria inclui os seguintes campos de dados definidos pela plataforma.</span><span class="sxs-lookup"><span data-stu-id="ef52d-116">This category includes the following platform-defined data fields.</span></span>



| <span data-ttu-id="ef52d-117">Nome do campo de dados e PID</span><span class="sxs-lookup"><span data-stu-id="ef52d-117">Data field name and PID</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="ef52d-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="ef52d-118">Description</span></span>                                                            |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_RFID_TAG_40_BIT"></span><span id="sensor_data_type_rfid_tag_40_bit"></span><dl> <span data-ttu-id="ef52d-119"><dt>**Sensor \_ Tipo de dados \_ \_ marca RFID de \_ \_ 40 \_ bits**</dt> <dt>(PID = 2)</dt></span><span class="sxs-lookup"><span data-stu-id="ef52d-119"><dt>**SENSOR\_DATA\_TYPE\_RFID\_TAG\_40\_BIT**</dt> <dt>(PID = 2) </dt></span></span> </dl> | <span data-ttu-id="ef52d-120">**\_UI8 VT**</span><span class="sxs-lookup"><span data-stu-id="ef52d-120">**VT\_UI8**</span></span><br/> <span data-ttu-id="ef52d-121">valor da marca de ID de frequência de rádio de 40 bits.</span><span class="sxs-lookup"><span data-stu-id="ef52d-121">40-bit radio frequency ID tag value.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ef52d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef52d-122">Requirements</span></span>



| <span data-ttu-id="ef52d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef52d-123">Requirement</span></span> | <span data-ttu-id="ef52d-124">Valor</span><span class="sxs-lookup"><span data-stu-id="ef52d-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ef52d-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef52d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ef52d-126">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ef52d-126">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ef52d-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef52d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ef52d-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ef52d-128">None supported</span></span><br/>                                                            |
| <span data-ttu-id="ef52d-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ef52d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef52d-130"><dt>Sensores. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef52d-130"><dt>Sensors.h</dt></span></span> </dl> |



 

 




