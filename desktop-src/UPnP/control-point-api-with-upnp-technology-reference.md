---
title: Referência de API de ponto de controle
description: As interfaces a seguir fazem parte da API do ponto de controle com tecnologia UPnP. A API do ponto de controle dá suporte ao Microsoft Visual Basic Scripting Edition (VBScript), ao Microsoft Visual Basic e ao C++.
ms.assetid: 6f73bf8c-0423-430f-a654-58d076712aae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691a0d764f612d957ac11b3b052859f081bc7285
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292017"
---
# <a name="control-point-api-reference"></a>Referência de API de ponto de controle

As interfaces a seguir fazem parte da API do ponto de controle com tecnologia UPnP. A API do ponto de controle dá suporte ao Microsoft Visual Basic Scripting Edition (VBScript), ao Microsoft Visual Basic e ao C++.



| Interface                                                                                      | Descrição                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUPnPAddressFamilyControl**](/windows/desktop/api/Upnp/nn-upnp-iupnpaddressfamilycontrol)                                 | Permite que um aplicativo acesse o sinalizador de família de endereços do objeto do localizador de dispositivos.                                                                                                                                          |
| [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument)                                   | Permite que um aplicativo carregue uma descrição do dispositivo. Esta interface é segura para scripts.                                                                                                                                     |
| [**IUPnPDescriptionDocumentCallback**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocumentcallback)                   | Permite que um aplicativo receba os resultados de uma operação de carregamento assíncrona.                                                                                                                                               |
| [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice)                                                             | Permite que um aplicativo recupere informações sobre um dispositivo específico.                                                                                                                                                        |
| [**IUPnPDeviceDocumentAccess**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccess)                                 | Permite que um aplicativo obtenha a URL de um documento de descrição do dispositivo.                                                                                                                                                     |
| [**IUPnPDeviceDocumentAccessEx**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccessex)                             | Fornece um método para obter todo o documento de descrição do dispositivo XML para um dispositivo específico.                                                                                                                                  |
| [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder)                                                 | Permite que um aplicativo encontre um dispositivo.                                                                                                                                                                                       |
| [**IUPnPDeviceFinderAddCallbackWithInterface**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinderaddcallbackwithinterface) | Permite que um aplicativo receba resultados de pesquisa assíncrona da estrutura UPnP junto com o GUID do adaptador de rede por meio do qual o anúncio do dispositivo veio.                                                  |
| [**IUPnPDeviceFinderCallback**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefindercallback)                                 | Permite que um aplicativo receba resultados de pesquisa assíncrona da estrutura UPnP.                                                                                                                                         |
| [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices)                                                           | Enumera uma coleção de dispositivos.                                                                                                                                                                                            |
| [**IUPnPHttpHeaderControl**](/windows/desktop/api/Upnp/nn-upnp-iupnphttpheadercontrol)                                       | Permite que um aplicativo defina cabeçalhos HTTP "agente do usuário" de instâncias de classe que implementam as interfaces [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) ou [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) . |
| [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice)                                                           | Permite que um aplicativo recupere informações de estado e invoque ações para um serviço.                                                                                                                                         |
| [**IUPnPServiceAsync**](/windows/desktop/api/Upnp/nn-upnp-iupnpserviceasync)                                                 | Variáveis de estado de consulta assíncrona e invocar ações em uma instância de um serviço.                                                                                                                                           |
| [**IUPnPServiceCallback**](/windows/desktop/api/Upnp/nn-upnp-iupnpservicecallback)                                           | Permite que um aplicativo receba notificação da estrutura UPnP quando ocorrerem eventos.                                                                                                                                      |
| [**IUPnPServices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices)                                                         | Enumera uma coleção de serviços.                                                                                                                                                                                           |



 

 

 




