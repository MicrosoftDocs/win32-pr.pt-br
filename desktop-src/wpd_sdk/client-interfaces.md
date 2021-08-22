---
description: Interfaces do cliente
ms.assetid: fbe53f17-940a-485e-82b2-c11ae39b3300
title: Interfaces do cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b44db8fdd42b20fb2ff7a3224bccf5214147069baa9187facdb1c832c375a59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590386"
---
# <a name="client-interfaces"></a>Interfaces do cliente

Os aplicativos usam os métodos compatíveis com as interfaces a seguir para executar operações em dispositivos portáteis. Essas operações incluem abrir uma conexão com um dispositivo, recuperar dados de um dispositivo, escrever dados em um dispositivo e assim por diante.



| Interface                                                                              | Descrição                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)                   | Enumera os objetos em um dispositivo portátil.                                                                                                                                                                                        |
| [**IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)                                             | Fornece acesso de baixo nível a um dispositivo portátil.                                                                                                                                                                                     |
| [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                     | Recupera uma variedade de funcionalidades do dispositivo, incluindo formatos, comandos e objetos funcionais com suporte.                                                                                                                          |
| [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                               | Fornece métodos para criar, enumerar e excluir conteúdo em um dispositivo.                                                                                                                                                              |
| [**IPortableDeviceDataStream**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream)                         | Expõe métodos adicionais em um **IStream** usado para transferências de dados.                                                                                                                                                               |
| [**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)                   | Implementado pelo aplicativo para receber retornos de chamada assíncronos.                                                                                                                                                                   |
| [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)                               | Enumera os dispositivos conectados ao computador e fornece uma maneira simples de solicitar informações de instalação para o dispositivo (incluindo fabricante, nome amigável e descrição).                                       |
| [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                         | Ler e gravar propriedades para um objeto no dispositivo.                                                                                                                                                                              |
| [**IPortableDevicePropertiesBulk**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)                 | Lê e grava várias propriedades em vários objetos em um dispositivo, de forma assíncrona.                                                                                                                                               |
| [**IPortableDevicePropertiesBulkCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulkcallback) | Implementado pelo aplicativo para acompanhar o progresso de uma operação assíncrona iniciada usando a interface **IPortableDevicePropertiesBulk.**                                                                          |
| [**IPortableDeviceResources**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources)                           | Fornece acesso aos dados de um objeto.                                                                                                                                                                                                |
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                               | Windows 7. Fornece acesso de baixo nível a um serviço de dispositivo portátil.                                                                                                                                                             |
| [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)              | Windows 7. Recupera uma variedade de recursos de serviço, incluindo formatos, comandos, métodos e perfis de renderização com suporte.                                                                                                |
| [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)                 | Windows 7. Invoca métodos de forma síncrona e assíncrona em um serviço.                                                                                                                                                      |
| [**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback)   | Windows 7. Implementado pelo aplicativo para acompanhar a conclusão de uma operação de método de serviço assíncrona iniciada chamando [ **IPortableDeviceServiceMethods::InvokeAsync**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync) |
| [**IPortableDeviceServiceManager**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager)                 | Windows 7. Enumera os serviços com suporte de um dispositivo e recupera o dispositivo associado a um serviço.                                                                                                             |



 

O diagrama a seguir mostra como um aplicativo obtém a maioria das interfaces de que precisa. Nem todos os métodos de todas as interfaces ou interfaces implementadas pelo aplicativo são mostrados.

![diagrama mostrando a criação e a recuperação da maioria das interfaces de cliente necessárias](images/wpd-sdk-interface-diagram.gif)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação**](programming-reference.md)
</dt> </dl>

 

 



