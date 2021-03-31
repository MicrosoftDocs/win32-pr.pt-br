---
description: Interfaces de cliente
ms.assetid: fbe53f17-940a-485e-82b2-c11ae39b3300
title: Interfaces de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5d7c85ec5cb9b35e30d68b1d784cdebf230fdaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829092"
---
# <a name="client-interfaces"></a>Interfaces de cliente

Os aplicativos usam os métodos com suporte nas seguintes interfaces para executar operações em dispositivos portáteis. Essas operações incluem a abertura de uma conexão com um dispositivo, a recuperação de dados de um dispositivo, a gravação de dados em um dispositivo e assim por diante.



| Interface                                                                              | Descrição                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)                   | Enumera os objetos em um dispositivo portátil.                                                                                                                                                                                        |
| [**IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)                                             | Fornece acesso de baixo nível a um dispositivo portátil.                                                                                                                                                                                     |
| [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                     | Recupera uma variedade de recursos de dispositivo, incluindo formatos com suporte, comandos e objetos funcionais.                                                                                                                          |
| [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                               | Fornece métodos para criar, enumerar e excluir conteúdo em um dispositivo.                                                                                                                                                              |
| [**IPortableDeviceDataStream**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream)                         | Expõe métodos adicionais em um **IStream** usado para transferências de dados.                                                                                                                                                               |
| [**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)                   | Implementado pelo aplicativo para receber retornos de chamada assíncronos.                                                                                                                                                                   |
| [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)                               | Enumera os dispositivos que estão conectados ao computador e fornece uma maneira simples de solicitar informações de instalação para o dispositivo (incluindo fabricante, nome amigável e descrição).                                       |
| [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                         | Ler e gravar as propriedades de um objeto no dispositivo.                                                                                                                                                                              |
| [**IPortableDevicePropertiesBulk**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)                 | Lê e grava várias propriedades em vários objetos em um dispositivo, de forma assíncrona.                                                                                                                                               |
| [**IPortableDevicePropertiesBulkCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulkcallback) | Implementado pelo aplicativo para acompanhar o progresso de uma operação assíncrona que foi iniciada usando a interface **IPortableDevicePropertiesBulk** .                                                                          |
| [**IPortableDeviceResources**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources)                           | Fornece acesso aos dados de um objeto.                                                                                                                                                                                                |
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                               | Somente Windows 7. Fornece acesso de baixo nível a um serviço de dispositivo portátil.                                                                                                                                                             |
| [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)              | Somente Windows 7. Recupera uma variedade de recursos de serviço, incluindo formatos com suporte, comandos, métodos e perfis de renderização.                                                                                                |
| [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)                 | Somente Windows 7. Invoca métodos de forma síncrona e assíncrona em um serviço.                                                                                                                                                      |
| [**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback)   | Somente Windows 7. Implementado pelo aplicativo para acompanhar a conclusão de uma operação de método de serviço assíncrono iniciada chamando [ **IPortableDeviceServiceMethods:: InvokeAsync**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync) |
| [**IPortableDeviceServiceManager**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager)                 | Somente Windows 7. Enumera os serviços que têm suporte de um dispositivo e recupera o dispositivo associado a um serviço.                                                                                                             |



 

O diagrama a seguir mostra como um aplicativo obtém a maioria das interfaces de que precisa. Nem todos os métodos de todas as interfaces ou interfaces implementadas pelo aplicativo são mostrados.

![diagrama mostrando a criação e a recuperação das interfaces de cliente mais necessárias](images/wpd-sdk-interface-diagram.gif)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação**](programming-reference.md)
</dt> </dl>

 

 



