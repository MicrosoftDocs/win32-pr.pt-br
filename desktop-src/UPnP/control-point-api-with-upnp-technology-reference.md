---
title: Referência da API do Ponto de Controle
description: As interfaces a seguir fazem parte da API do Ponto de Controle com a tecnologia UPnP. A API do Ponto de Controle dá suporte Visual Basic VBScript (Microsoft Visual Basic Scripting Edition), Microsoft Visual Basic e C++.
ms.assetid: 6f73bf8c-0423-430f-a654-58d076712aae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24b3dab16874ebeb7b43ef1e8cf28def13d3ef1d7169a5aae4836b39da66636b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058114"
---
# <a name="control-point-api-reference"></a>Referência da API do Ponto de Controle

As interfaces a seguir fazem parte da API do Ponto de Controle com a tecnologia UPnP. A API do Ponto de Controle dá suporte Visual Basic VBScript (Microsoft Visual Basic Scripting Edition), Microsoft Visual Basic e C++.



| Interface                                                                                      | Descrição                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUPnPAddressFamilyControl**](/windows/desktop/api/Upnp/nn-upnp-iupnpaddressfamilycontrol)                                 | Permite que um aplicativo acesse o sinalizador da família de endereços do objeto Device Finder.                                                                                                                                          |
| [**Iupnpdescriptiondocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument)                                   | Permite que um aplicativo carregue uma descrição do dispositivo. Essa interface é segura para scripts.                                                                                                                                     |
| [**IUPnPDescriptionDocumentCallback**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocumentcallback)                   | Permite que um aplicativo receba os resultados de uma operação de carregamento assíncrona.                                                                                                                                               |
| [**Iupnpdevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice)                                                             | Permite que um aplicativo recupere informações sobre um dispositivo específico.                                                                                                                                                        |
| [**IUPnPDeviceDocumentAccess**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccess)                                 | Permite que um aplicativo obtenha a URL de um documento de descrição do dispositivo.                                                                                                                                                     |
| [**IUPnPDeviceDocumentAccessEx**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccessex)                             | Fornece um método para obter todo o documento de descrição do dispositivo XML para um dispositivo específico.                                                                                                                                  |
| [**Iupnpdevicefinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder)                                                 | Permite que um aplicativo encontre um dispositivo.                                                                                                                                                                                       |
| [**IUPnPDeviceCallbackWithInterface**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinderaddcallbackwithinterface) | Permite que um aplicativo receba resultados da pesquisa assíncrona da estrutura UPnP juntamente com o GUID do adaptador de rede por meio do qual o anúncio do dispositivo veio.                                                  |
| [**IUPnPDeviceCallback**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefindercallback)                                 | Permite que um aplicativo receba resultados da pesquisa assíncrona da estrutura UPnP.                                                                                                                                         |
| [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices)                                                           | Enumera uma coleção de dispositivos.                                                                                                                                                                                            |
| [**IUPnPHttpHeaderControl**](/windows/desktop/api/Upnp/nn-upnp-iupnphttpheadercontrol)                                       | Habilita um aplicativo a definir cabeçalhos HTTP "Agente do Usuário" de instâncias de classe que implementam as interfaces [**IUPnPDeviceScript ou**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) [**IUPnPDescriptionDocument.**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) |
| [**Iupnpservice**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice)                                                           | Permite que um aplicativo recupere informações de estado e invoque ações para um serviço.                                                                                                                                         |
| [**IUPnPServiceAsync**](/windows/desktop/api/Upnp/nn-upnp-iupnpserviceasync)                                                 | Consulte variáveis de estado de forma assíncrona e invoque ações em uma instância de um serviço.                                                                                                                                           |
| [**IUPnPServiceCallback**](/windows/desktop/api/Upnp/nn-upnp-iupnpservicecallback)                                           | Permite que um aplicativo receba notificação da estrutura UPnP quando ocorrem eventos.                                                                                                                                      |
| [**IUPnPServices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices)                                                         | Enumera uma coleção de serviços.                                                                                                                                                                                           |



 

 

 




