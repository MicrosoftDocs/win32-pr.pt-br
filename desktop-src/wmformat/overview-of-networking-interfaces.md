---
title: Visão geral das interfaces de rede
description: Visão geral das interfaces de rede
ms.assetid: 7aa7ff1b-9c81-4fee-afa9-2a9eed457360
keywords:
- Windows SDK do formato de mídia, interfaces de rede
- Windows SDK do formato de mídia, interfaces
- ASF (Advanced Systems Format), interfaces de rede
- ASF (formato de sistemas avançados), interfaces de rede
- Formato de sistema avançado (ASF), lista de interface para recursos de rede
- ASF (formato de sistemas avançados), lista de interface para recursos de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b87da220f5ac61b7b722e79939a1fd617af46ab6608d4d92e8905f466bb98e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118700258"
---
# <a name="overview-of-networking-interfaces"></a>Visão geral das interfaces de rede

Os recursos de rede desse SDK têm suporte por meio de métodos das interfaces a seguir.



| Interface                                                  | Descrição                                                                                                                                           |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMClientConnections**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections)       | Obtém informações sobre os clientes conectados a um coletor de rede.                                                                                       |
| [**IWMClientConnections2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2)     | Fornece um método para obter informações sobre um cliente anexado a um coletor de rede do gravador. Essa interface estende a interface **IWMClientConnections** . |
| [**IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)     | Fornece um método de retorno de chamada para adquirir credenciais de usuário ao acessar um site remoto.                                                                  |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)           | Fornece métodos avançados no objeto leitor.                                                                                                       |
| [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3)           | Estende a interface **IWMReaderAdvanced2** .                                                                                                         |
| [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)           | Estende a interface **IWMReaderAdvanced3** .                                                                                                         |
| [**IWMReaderNetworkConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig)   | Define as configurações de rede no objeto leitor.                                                                                                 |
| [**IWMReaderNetworkConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2) | Define as configurações de rede adicionais no objeto leitor. Essa interface estende a interface **IWMReaderNetworkConfig** .                         |
| [**IWMWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink)       | Configura o objeto de coletor de rede, que é usado para gravar mídia digital em uma rede.                                                                |
| [**IWMWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)             | Configura o objeto Push Sink, que é usado para distribuir mídia digital para pontos de publicação.                                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando a funcionalidade de rede**](implementing-network-functionality.md)
</dt> </dl>

 

 




