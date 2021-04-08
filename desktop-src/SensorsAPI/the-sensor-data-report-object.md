---
description: O objeto de relatório de dados do sensor contém dados do sensor.
ms.assetid: 8a812860-338b-4ada-8f5f-ea693e038941
title: O objeto de relatório de dados do sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d43753aa28be5cd20c85b7e65bf4c7516d4c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922100"
---
# <a name="the-sensor-data-report-object"></a><span data-ttu-id="54969-103">O objeto de relatório de dados do sensor</span><span class="sxs-lookup"><span data-stu-id="54969-103">The Sensor Data Report Object</span></span>

<span data-ttu-id="54969-104">O objeto de relatório de dados do sensor contém dados do sensor.</span><span class="sxs-lookup"><span data-stu-id="54969-104">The sensor data report object contains sensor data.</span></span>

<span data-ttu-id="54969-105">Para que um sensor seja útil, ele deve fornecer dados significativos.</span><span class="sxs-lookup"><span data-stu-id="54969-105">For a sensor to be useful, it must provide meaningful data.</span></span> <span data-ttu-id="54969-106">A quantidade e a frequência da geração de dados variam de sensor para sensor.</span><span class="sxs-lookup"><span data-stu-id="54969-106">The amount and frequency of data generation varies from sensor to sensor.</span></span> <span data-ttu-id="54969-107">Por exemplo, um sensor que detecta se uma porta está aberta geraria uma pequena quantidade de dados **boolianos** , enquanto um sensor de movimento pode gerar continuamente vários itens de dados.</span><span class="sxs-lookup"><span data-stu-id="54969-107">For example, a sensor that detects whether a door is open would generate a small amount of **Boolean** data, while a motion sensor might continuously generate multiple data items.</span></span> <span data-ttu-id="54969-108">Para padronizar a maneira como seu programa recebe dados, a API do sensor usa o objeto de relatório de dados do sensor.</span><span class="sxs-lookup"><span data-stu-id="54969-108">To standardize the way your program receives data, the Sensor API uses the sensor data report object.</span></span>

<span data-ttu-id="54969-109">Você pode acessar as informações em um relatório de dados de sensor por meio da interface [**ISensorDataReport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) .</span><span class="sxs-lookup"><span data-stu-id="54969-109">You can access the information in a sensor data report through the [**ISensorDataReport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) interface.</span></span> <span data-ttu-id="54969-110">Essa interface permite recuperar o carimbo de data/hora do relatório de dados para que você possa determinar se as informações no relatório são úteis.</span><span class="sxs-lookup"><span data-stu-id="54969-110">This interface lets you retrieve the data report's time stamp so that you can determine whether the information in the report is useful.</span></span> <span data-ttu-id="54969-111">Você pode recuperar os dados em si de duas maneiras: como um valor de campo de dados individual ou como um conjunto de valores.</span><span class="sxs-lookup"><span data-stu-id="54969-111">You can retrieve the data itself in two ways: as an individual data field value or as a set of values.</span></span> <span data-ttu-id="54969-112">Para recuperar dados como um valor individual, chame o método [**Getsensorvalue**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalue) .</span><span class="sxs-lookup"><span data-stu-id="54969-112">To retrieve data as an individual value, call the [**GetSensorValue**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalue) method.</span></span> <span data-ttu-id="54969-113">Para recuperar vários valores, chame o método [**GetSensorValues**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalues) .</span><span class="sxs-lookup"><span data-stu-id="54969-113">To retrieve multiple values, call the [**GetSensorValues**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalues) method.</span></span>

<span data-ttu-id="54969-114">Você especifica o tipo de dados ou os campos de dados que deseja recuperar do relatório usando uma constante **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="54969-114">You specify the type of data, or data fields, that you want to retrieve from the report by using a **PROPERTYKEY** constant.</span></span> <span data-ttu-id="54969-115">As chaves de propriedade para campos de dados de tipos de sensor comuns são definidas em sensores. h.</span><span class="sxs-lookup"><span data-stu-id="54969-115">Property keys for data fields of common sensor types are defined in Sensors.h.</span></span>

 

 
