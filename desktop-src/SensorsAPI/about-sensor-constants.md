---
description: Sobre constantes de sensor
ms.assetid: ba85ccd8-5251-4e47-84da-80899fe84c39
title: Sobre constantes de sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45cab8b5def4cdfa185a55dd993896fb5157563424b7753497413e5d7706465e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890251"
---
# <a name="about-sensor-constants"></a>Sobre constantes de sensor

A plataforma Windows Sensor e Localização usa constantes de várias maneiras. A plataforma define constantes diferentes que você pode usar no código do driver do sensor. Os fabricantes de sensor podem definir constantes personalizadas. Você pode encontrar as definições de constantes definidas pela plataforma no arquivo Sensors.h. Para obter informações detalhadas sobre constantes de sensor definidas pela plataforma, consulte [Constantes](constants.md).

### <a name="sensor-and-data-organization"></a>Sensor e organização de dados

A plataforma organiza sensores e dados das seguintes maneiras.

-   As categorias representam classes amplas de dispositivos de sensor. As categorias permitem agrupar sensores que provavelmente fornecem tipos semelhantes de informações ou que estão relacionados de alguma forma. Cada categoria é representada por uma constante **GUID.** Por exemplo, sensores que relatam coordenadas de latitude e longitude pertencem à categoria do sensor de localização. Isso é representando pela constante SENSOR \_ CATEGORY \_ LOCATION.
-   Os tipos de sensor representam tipos específicos de sensores. Cada tipo de sensor se encaixa em uma categoria específica. Dois sensores de tipos diferentes podem pertencer à mesma categoria ou categorias diferentes. Cada tipo de sensor é representado por uma **constante GUID.** Por exemplo, um sensor do sistema de posicionamento global seria identificado pela constante GPS SENSOR \_ TYPE \_ \_ LOCATION. No entanto, um sensor que fornece o local atual usando um endereço IP seria identificado pela constante SENSOR \_ TYPE \_ LOCATION \_ LOOKUP. No entanto, ambos os sensores pertencem à categoria de sensor de localização.
-   Os tipos de dados representam tipos específicos de informações que o sensor pode fornecer. Os tipos de dados do sensor podem conter o valor de medida real, como altitude; informações sobre as unidades usadas para expressar os dados, como medidores; e pontos de referência para os dados, como nível do mar. Cada tipo de dados é representado por uma **constante PROPERTYKEY.** Por exemplo, o tipo de dados que representa a altitude acima do nível do mar, em metros, seria identificado pela constante SENSOR \_ DATA \_ TYPE ALTITUDE \_ \_ SEALEVEL \_ METERS.
-   Ao relatar dados, diz-se que um valor está contido em um campo de dados e uma coleção de campos de dados relacionados comem um relatório de dados. Os relatórios de dados são empacotados juntos usando a interface [IPortableDeviceValues.](/previous-versions//ms740012(v=vs.85)) Cada relatório de dados deve conter pelo menos um campo de dados válido e um carimbo de data/hora que identifica quando o relatório de dados foi criado. Os carimbos de data/hora são representados pela constante \_ \_ TIMESTAMP DO TIPO DE DADOS DO \_ SENSOR.

### <a name="other-constants"></a>Outras constantes

Seu programa também deve usar outras constantes. Essas constantes incluem o seguinte:

-   Propriedades do sensor, como SENSOR \_ PROPERTY \_ DESCRIPTION. Normalmente, essas constantes são usadas para descrever um sensor. Algumas propriedades do sensor devem ser fornecidas pelo sensor, algumas propriedades podem ser definidas por aplicativos cliente e algumas sempre devem retornar o mesmo valor do sensor. A [**seção de referência Propriedades**](sensor-properties.md) do Sensor fornece essas informações para cada propriedade.
-   Constantes de evento, como SENSOR \_ EVENT \_ STATE \_ CHANGED. As constantes de evento incluem **GUID** s, que representam tipos de eventos, e **PROPERTYKEY** s, que representam tipos de parâmetro de evento. Você usará essas constantes para chamadas de método, como [**ISensor::SetEventInterest**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventinterest) e [**ISensor::GetEventInterest**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-geteventinterest).

### <a name="custom-constants"></a>Constantes personalizadas

Os fabricantes de sensor podem definir constantes personalizadas. Por exemplo, um sensor pode pertencer a uma categoria não definida pela plataforma. Antes de usar um sensor que define constantes personalizadas, o fabricante do sensor deve publicar os valores, por exemplo, publicando um arquivo de header. Para obter mais informações, consulte a documentação fornecida com o sensor.

 

 
