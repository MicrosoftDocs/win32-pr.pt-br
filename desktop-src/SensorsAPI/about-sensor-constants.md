---
description: Sobre as constantes do sensor
ms.assetid: ba85ccd8-5251-4e47-84da-80899fe84c39
title: Sobre as constantes do sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ea862d38af74058d11d3a6fa1eb11a702b3b277
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506134"
---
# <a name="about-sensor-constants"></a>Sobre as constantes do sensor

A plataforma de sensor e localização do Windows usa constantes de várias maneiras. A plataforma define constantes diferentes que você pode usar em seu código de driver de sensor. Os fabricantes de sensor podem definir constantes personalizadas. Você pode encontrar as definições de constantes definidas pela plataforma no arquivo sensors. h. Para obter informações detalhadas sobre constantes de sensor definidas pela plataforma, consulte [constantes](constants.md).

### <a name="sensor-and-data-organization"></a>Sensor e organização de dados

A plataforma organiza sensores e dados das seguintes maneiras.

-   As categorias representam classes amplas de dispositivos de sensor. As categorias permitem que você agrupe os sensores que provavelmente fornecerão tipos de informações semelhantes ou que estão relacionados de alguma maneira. Cada categoria é representada por uma constante de **GUID** . Por exemplo, os sensores que relatam coordenadas de latitude e longitude pertencem à categoria de sensor de localização. Isso é representented pela \_ constante local da categoria do sensor \_ .
-   Os tipos de sensor representam tipos específicos de sensores. Cada tipo de sensor se encaixa em uma determinada categoria. Dois sensores de tipos diferentes podem pertencer à mesma categoria ou categorias diferentes. Cada tipo de sensor é representado por uma constante de **GUID** . Por exemplo, um sensor de sistema de posicionamento global seria identificado pelo tipo de SENSOR \_ \_ local \_ GPS Constant. No entanto, um sensor que fornece o local atual usando um endereço IP seria identificado pela constante de \_ pesquisa de local do tipo de sensor \_ \_ . No entanto, ambos os sensores pertenceriam à categoria de sensor de localização.
-   Os tipos de dados representam tipos específicos de informações que o sensor pode fornecer. Os tipos de dados de sensor podem conter o valor de medição real, como altitude; informações sobre as unidades usadas para expressar os dados, como medidores; e pontos de referência para os dados, como nível de Sea. Cada tipo de dados é representado por uma constante **PROPERTYKEY** . Por exemplo, o tipo de dados que representa a altitude acima do nível do mar, em metros, seria identificado pelo \_ tipo de dados sensor altitude de \_ medidores de nível de texto \_ \_ \_ constante.
-   Ao relatar dados, um valor é dito como está contido em um campo de dados e uma coleção de campos de dados relacionados compõe um relatório de dados. Os relatórios de dados são empacotados em conjunto usando a interface [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) . Cada relatório de dados deve conter pelo menos um campo de dados válido e um carimbo de data/hora que identifica quando o relatório de dados foi criado. Os carimbos de data/hora são representados pela constante do tipo de dados do SENSOR \_ \_ \_ .

### <a name="other-constants"></a>Outras constantes

O programa também deve usar outras constantes. Essas constantes incluem o seguinte:

-   Propriedades do sensor, como descrição da Propriedade do SENSOR \_ \_ . Normalmente, essas constantes são usadas para descrever um sensor. Algumas propriedades de sensor devem ser fornecidas pelo sensor, algumas propriedades podem ser definidas por aplicativos cliente e algumas devem sempre retornar o mesmo valor do sensor. A seção de referência de [**Propriedades do sensor**](sensor-properties.md) fornece essas informações para cada propriedade.
-   Constantes de evento, como estado de evento de SENSOR \_ \_ \_ alterado. As constantes de evento incluem **GUID** s, que representam tipos de eventos e **PROPERTYKEY** s, que representam tipos de parâmetro de evento. Você usará essas constantes para chamadas de método, como [**ISensor:: SetEventInterest**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventinterest) e [**ISensor:: GetEventInterest**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-geteventinterest).

### <a name="custom-constants"></a>Constantes personalizadas

Os fabricantes de sensor podem definir constantes personalizadas. Por exemplo, um sensor pode pertencer a uma categoria não definida pela plataforma. Para que você possa usar um sensor que define constantes personalizadas, o fabricante do sensor deve publicar os valores, por exemplo, publicando um arquivo de cabeçalho. Para obter mais informações, consulte a documentação fornecida com o sensor.

 

 
