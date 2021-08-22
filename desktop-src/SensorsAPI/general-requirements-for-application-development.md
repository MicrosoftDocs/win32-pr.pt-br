---
description: Este tópico descreve o que você deve fazer para começar a criar programas que usam a API do Sensor.
ms.assetid: a8d3228a-5f8b-4850-9e47-5dfb2335e655
title: Requisitos gerais para desenvolvimento de aplicativos (API do sensor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 148057cd837e8eef26e73ff9cdef07ca01c70cb4a107e5f6e77f9ca43487407d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003774"
---
# <a name="general-requirements-for-application-development-sensor-api"></a>Requisitos gerais para desenvolvimento de aplicativos (API do sensor)

Este tópico descreve o que você deve fazer para começar a criar programas que usam a API do Sensor.

Para criar um aplicativo de API de Sensor, você deve instalar o Windows 7 e o SDK (Software Development Kit) do Windows 7 em seu computador. A tabela a seguir descreve os arquivos específicos de que você precisará.



| Nome do arquivo               | Descrição                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| Sensorsapi.h            | O arquivo de header principal para a API do Sensor. Esse arquivo de header contém as definições de interface.               |
| Sensors.h               | O arquivo de header que contém definições de constantes definidas pela plataforma.                                    |
| Initguid.h              | O arquivo de header que contém definições para controlar a inicialização do **GUID.**                          |
| FunctionDiscoveryKeys.h | O arquivo de header que define as chaves de propriedade da ID do dispositivo que são necessárias quando você se conecta a sensores lógicos. |
| Sensorsapi.lib          | Uma biblioteca estática que contém **definições de GUID** para a API do Sensor.                                     |
| PortableDeviceGuids.lib | Uma biblioteca estática que contém **definições de GUID** para Windows dispositivos portáteis.                   |



 

Seu programa pode exigir arquivos adicionais.

## <a name="supported-operating-systems"></a>Sistemas operacionais com suporte

Os aplicativos de API do sensor serão executados em todas as edições do Windows 7, exceto Windows 7 Starter Edition.

## <a name="windows-portable-devices-interfaces"></a>Windows Interfaces de dispositivos portáteis

A API do Sensor usa determinados Windows WPD (Dispositivos Portáteis) para encapsular valores e chaves de propriedade. A tabela a seguir descreve as interfaces para esses objetos.



| Interface                                                                       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85))        | Essa interface fornece uma maneira conveniente de criar um pacote de propriedades de pares nome/valor. Os nomes são representados **por PROPERTYKEY** s e os valores são representados **por PROPVARIANT** s. <br/> A API usa essa interface para definir e recuperar valores individuais e conjuntos de valores. Essa interface pode ser recuperada de um método ou, se um novo objeto for necessário, chamando **CoCreateInstance** com CLSID \_ PortableDeviceValues.<br/> |
| [IPortableDeviceKeyCollection](/previous-versions//ms739549(v=vs.85)) | Essa interface contém uma coleção de **PROPERTYKEY** s. Essas chaves representam nomes de propriedade que podem ser armazenados por **IPortableDeviceValues.** A API usa esse objeto de coleção para definir e recuperar nomes de propriedade única e conjuntos de nomes de propriedade.<br/> Essa interface pode ser recuperada de um método ou, se um novo objeto for necessário, chamando **CoCreateInstance** com CLSID \_ PortableDeviceKeyCollection. <br/>    |



 

 

