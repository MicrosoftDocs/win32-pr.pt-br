---
description: Acessando Propriedades de objeto de serviço
ms.assetid: 66d9802b-ad28-47a4-8151-9df7aff07d61
title: Acessando Propriedades de objeto de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 028ffc178f29f21aa60295b137b48c0fa2357a28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781205"
---
# <a name="accessing-service-object-properties"></a>Acessando Propriedades de objeto de serviço

Um aplicativo pode ler e gravar propriedades para um único objeto em um serviço, para vários objetos identificados por identificadores de objeto ou para vários objetos do mesmo tipo. O tópico [Recuperando propriedades do objeto](retrieving-content-object-properties.md) descreve a leitura de propriedades de um único objeto em um serviço. O tópico [gravando Propriedades de objeto](writing-content-object-properties.md) descreve a gravação de propriedades para um único objeto em um serviço.

Consulte a seção [tarefas avançadas](advanced-tasks.md) para obter uma descrição da recuperação de propriedade para vários objetos.

## <a name="when-to-use-service-property-definitions"></a>Quando usar definições de propriedade de serviço

As chamadas à API WPD usadas para recuperar e definir propriedades de objeto para um serviço são as mesmas que as chamadas para recuperar propriedades de objeto para um dispositivo (compare "Recuperando propriedades para um único objeto" para obter um exemplo). A principal diferença é que um conjunto diferente de PROPERTYKEYs é usado para consultar as propriedades do objeto. Para o WpdServiceApiSample, o serviço de dispositivo PROPERTYKEYs é usado (como **PKEY \_ GenericObj \_ Name**); para o WpdApiSample, o PropertyKeys de WPD é usado (como o **\_ \_ nome do objeto WPD**).

O serviço de dispositivo PROPERTYKEYs é definido em BridgeDeviceServices. h (incluído por cada arquivo de cabeçalho de serviço) e representa o conjunto comum de PROPERTYKEYS empregado por aplicativos de serviços de dispositivo e a implementação de firmware no dispositivo. Isso permite um conjunto consistente de definições em toda a pilha de dispositivos com a tradução mínima, agrupa o PROPERTYKEYs com base no serviço e permite que novos serviços sejam definidos com mais facilidade sem a necessidade de atualizar o esquema WPD.

O conjunto de PROPERTYKEYs usado dependerá das necessidades do seu aplicativo:

-   Se seu aplicativo estiver se comunicando com o dispositivo chamando [**IPortableDevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open), use o PROPERTYKEYs definido em PortableDevice. h. Um exemplo desse tipo de aplicativo é o WpdApiSample.
-   Se seu aplicativo estiver se comunicando com os serviços de dispositivo chamando [**IPortableDeviceService:: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open), use o PROPERTYKEYS definido em BridgeDeviceServices. h. Um exemplo desse tipo de aplicativo é o WpdServicesApiSample.
-   Se você estiver escrevendo um aplicativo complexo que precisa dar suporte a um híbrido de serviços de dispositivo e ao dispositivo (isso significa que seu aplicativo chama **IPortableDevice:: Open** e **IPortableDeviceService:: Open**), você precisará usar o PROPERTYKEYs WPD ao usar IPortableDevice e suas interfaces derivadas e o serviço de dispositivo PROPERTYKEYs ao usar [IPortableDeviceService](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) e suas interfaces derivadas.

A maioria dos aplicativos WPD deve enquadrar-se na primeira ou segunda categoria.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[Recuperando propriedades do objeto](retrieving-content-object-properties.md)
</dt> <dt>

[Gravando Propriedades do objeto](writing-content-object-properties.md)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



