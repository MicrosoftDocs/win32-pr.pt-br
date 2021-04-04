---
description: A categoria SENSOR \_ categoria \_ todas representa o conjunto de todas as categorias de sensor definidas pela plataforma.
ms.assetid: e2d9fe6d-450a-446b-968b-0924116af6fe
title: SENSOR_CATEGORY_ALL (sensores. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a2e5641e51dde130cc51d9b2fc35fcc1e158ea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646979"
---
# <a name="sensor_category_all"></a><span data-ttu-id="499f1-103">Categoria do SENSOR \_ \_ tudo</span><span class="sxs-lookup"><span data-stu-id="499f1-103">SENSOR\_CATEGORY\_ALL</span></span>

<span data-ttu-id="499f1-104">A categoria SENSOR \_ categoria \_ todas representa o conjunto de todas as categorias de sensor definidas pela plataforma.</span><span class="sxs-lookup"><span data-stu-id="499f1-104">The SENSOR\_CATEGORY\_ALL category represents the set of all platform-defined sensor categories.</span></span>

<span data-ttu-id="499f1-105">**Chaves de propriedade definidas pela plataforma**</span><span class="sxs-lookup"><span data-stu-id="499f1-105">**Platform-Defined Property Keys**</span></span>

<span data-ttu-id="499f1-106">As chaves de propriedade definidas pela plataforma para essa categoria baseiam-se no \_ GUID comum de tipo de dados do sensor \_ \_ \_ :</span><span class="sxs-lookup"><span data-stu-id="499f1-106">Platform-defined property keys for this category are based on SENSOR\_DATA\_TYPE\_COMMON\_GUID:</span></span>

<span data-ttu-id="499f1-107">{DB5E0CF2-CF1F-4C18-B46C-D86011D62150}</span><span class="sxs-lookup"><span data-stu-id="499f1-107">{DB5E0CF2-CF1F-4C18-B46C-D86011D62150}</span></span>

<span data-ttu-id="499f1-108">A tabela a seguir descreve os campos de dados definidos pela plataforma.</span><span class="sxs-lookup"><span data-stu-id="499f1-108">The following table describes platform-defined data fields.</span></span>



| <span data-ttu-id="499f1-109">Nome do campo de dados e PID</span><span class="sxs-lookup"><span data-stu-id="499f1-109">Data field name and PID</span></span>                                                                                                                                                                                                                                                 | <span data-ttu-id="499f1-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="499f1-110">Description</span></span>                                                                                                                                                                        |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_TIMESTAMP"></span><span id="sensor_data_type_timestamp"></span><dl> <span data-ttu-id="499f1-111"><dt>**Sensor \_ Carimbo de DATA \_ \_ /hora do tipo de dados**</dt> <dt>(PID = 2)</dt></span><span class="sxs-lookup"><span data-stu-id="499f1-111"><dt>**SENSOR\_DATA\_TYPE\_TIMESTAMP**</dt> <dt>(PID = 2 ) </dt></span></span> </dl> | <span data-ttu-id="499f1-112">**FILETIME do VT \_**</span><span class="sxs-lookup"><span data-stu-id="499f1-112">**VT\_FILETIME**</span></span><br/> <span data-ttu-id="499f1-113">Necessário para todos os relatórios de dados.</span><span class="sxs-lookup"><span data-stu-id="499f1-113">Required for all data reports.</span></span> <span data-ttu-id="499f1-114">Marca cada relatório de dados com a hora em que o relatório de dados foi criado no formato UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="499f1-114">Marks each data report with the time the data report was created in Coordinated Universal Time (UTC) format.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="499f1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="499f1-115">Requirements</span></span>



| <span data-ttu-id="499f1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="499f1-116">Requirement</span></span> | <span data-ttu-id="499f1-117">Valor</span><span class="sxs-lookup"><span data-stu-id="499f1-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="499f1-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="499f1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="499f1-119">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="499f1-119">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="499f1-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="499f1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="499f1-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="499f1-121">None supported</span></span><br/>                                                            |
| <span data-ttu-id="499f1-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="499f1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="499f1-123"><dt>Sensores. h</dt></span><span class="sxs-lookup"><span data-stu-id="499f1-123"><dt>Sensors.h</dt></span></span> </dl> |



 

 




