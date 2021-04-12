---
description: Este tópico descreve o que você deve fazer para começar a criar programas que usam a API do sensor.
ms.assetid: a8d3228a-5f8b-4850-9e47-5dfb2335e655
title: Requisitos gerais para o desenvolvimento de aplicativos (API de sensor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ec328f659bb51eddf93cc69beb2fe6236113ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297178"
---
# <a name="general-requirements-for-application-development-sensor-api"></a>Requisitos gerais para o desenvolvimento de aplicativos (API de sensor)

Este tópico descreve o que você deve fazer para começar a criar programas que usam a API do sensor.

Para criar um aplicativo de API de sensor, você deve instalar o Windows 7 e o SDK (Software Development Kit) do Windows 7 em seu computador. A tabela a seguir descreve os arquivos específicos que serão necessários.



| Nome do arquivo               | Descrição                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| Sensorsapi. h            | O arquivo de cabeçalho principal para a API do sensor. Esse arquivo de cabeçalho contém as definições de interface.               |
| Sensores. h               | O arquivo de cabeçalho que contém definições de constantes definidas pela plataforma.                                    |
| Initguid. h              | O arquivo de cabeçalho que contém definições para controlar a inicialização do **GUID** .                          |
| FunctionDiscoveryKeys. h | O arquivo de cabeçalho que define as chaves de propriedade de ID do dispositivo que são necessárias quando você se conecta a sensores lógicos. |
| Sensorsapi. lib          | Uma biblioteca estática que contém definições de **GUID** para a API do sensor.                                     |
| PortableDeviceGuids. lib | Uma biblioteca estática que contém definições de **GUID** para objetos de dispositivos portáteis do Windows.                   |



 

Seu programa pode exigir arquivos adicionais.

## <a name="supported-operating-systems"></a>Sistemas operacionais com suporte

Os aplicativos de API do sensor serão executados em todas as edições do Windows 7, exceto para o Windows 7 Starter Edition.

## <a name="windows-portable-devices-interfaces"></a>Interfaces de dispositivos portáteis do Windows

A API do sensor usa determinados objetos de dispositivos portáteis do Windows (WPD) para encapsular valores e chaves de propriedade. A tabela a seguir descreve as interfaces para esses objetos.



| Interface                                                                       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85))        | Essa interface fornece uma maneira conveniente de criar um recipiente de propriedades de pares de nome/valor. Os nomes são representados por a **PROPERTYKEY** s e os valores são representados por **PROPVARIANT** s. <br/> A API usa essa interface para configurar e recuperar valores únicos e conjuntos de valores. Essa interface pode ser recuperada de um método ou, se um novo objeto for necessário, chamando **CoCreateInstance** com CLSID \_ PortableDeviceValues.<br/> |
| [IPortableDeviceKeyCollection](/previous-versions//ms739549(v=vs.85)) | Esta interface contém uma coleção de **PROPERTYKEY** s. Essas chaves representam nomes de propriedade que podem ser armazenados por **IPortableDeviceValues**. A API usa esse objeto de coleção para definir e recuperar os nomes de propriedade única e os conjuntos de nomes de propriedade.<br/> Essa interface pode ser recuperada de um método ou, se um novo objeto for necessário, chamando **CoCreateInstance** com CLSID \_ PortableDeviceKeyCollection. <br/>    |



 

 

