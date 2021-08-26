---
description: O objeto de relatório de dados do sensor contém dados do sensor.
ms.assetid: 8a812860-338b-4ada-8f5f-ea693e038941
title: O objeto de relatório de dados do sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ca1a8e5f61b23753437bd8b1cf4c2a176515b7042b21e84c4d2f431debc8fe6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992596"
---
# <a name="the-sensor-data-report-object"></a>O objeto de relatório de dados do sensor

O objeto de relatório de dados do sensor contém dados do sensor.

Para que um sensor seja útil, ele deve fornecer dados significativos. A quantidade e a frequência de geração de dados variam de sensor para sensor. Por exemplo, um sensor que detecta se uma porta  está aberta geraria uma pequena quantidade de dados boolianas, enquanto um sensor de movimento pode gerar continuamente vários itens de dados. Para padronizar a maneira como seu programa recebe dados, a API do Sensor usa o objeto de relatório de dados do sensor.

Você pode acessar as informações em um relatório de dados do sensor por meio da interface [**ISensorDataReport.**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) Essa interface permite recuperar o carimbo de data/hora do relatório de dados para que você possa determinar se as informações no relatório são úteis. Você pode recuperar os dados em si de duas maneiras: como um valor de campo de dados individual ou como um conjunto de valores. Para recuperar dados como um valor individual, chame o [**método GetSensorValue.**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalue) Para recuperar vários valores, chame o [**método GetSensorValues.**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalues)

Especifique o tipo de dados ou campos de dados que deseja recuperar do relatório usando uma **constante PROPERTYKEY.** As chaves de propriedade para campos de dados de tipos de sensor comuns são definidas em Sensors.h.

 

 
