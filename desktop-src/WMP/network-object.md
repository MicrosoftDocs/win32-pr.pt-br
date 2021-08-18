---
title: Objeto de rede
description: O objeto de rede fornece propriedades e métodos usados para acessar estatísticas relacionadas à qualidade de uma conexão de rede e para especificar e recuperar as configurações de proxy de rede.
ms.assetid: 5ae6137e-22f5-4a65-8793-b6f66adb4cba
keywords:
- Windows Media Player de objeto de rede
topic_type:
- apiref
api_name:
- Network Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6bf91c23d6a5c581430b17a370e66027a5f9174d0511a2647fba33834ec6c4b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996106"
---
# <a name="network-object"></a>Objeto de rede

O objeto de **rede** fornece propriedades e métodos usados para acessar estatísticas relacionadas à qualidade de uma conexão de rede e para especificar e recuperar as configurações de proxy de rede.

O objeto de **rede** dá suporte às propriedades a seguir.



| Propriedade                                           | Descrição                                                                                 |
|----------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Larga](network-bandwidth.md)                 | Recupera a largura de banda atual do item de mídia.                                          |
| [720p](network-bitrate.md)                     | Recupera a taxa de bits atual que está sendo recebida.                                              |
| [bufferingCount](network-bufferingcount.md)       | Recupera o número de vezes que o buffer ocorreu durante a reprodução.                           |
| [bufferingProgress](network-bufferingprogress.md) | Recupera a porcentagem de buffer concluído.                                            |
| [bufferingTime](network-bufferingtime.md)         | Especifica ou recupera a quantidade de tempo de buffer em milissegundos antes que a reprodução seja iniciada. |
| [downloadProgress](network-downloadprogress.md)   | Recupera o percentual de download concluído.                                             |
| [encodedFrameRate](network-encodedframerate.md)   | Recupera a taxa de quadros de vídeo especificada pelo autor do conteúdo.                             |
| [Quadros](network-framerate.md)                 | Recupera a taxa de quadros de vídeo atual.                                                     |
| [framesSkipped](network-framesskipped.md)         | Recupera o número total de quadros ignorados durante a reprodução.                               |
| [lostPackets](network-lostpackets.md)             | Recupera o número de pacotes perdidos.                                                       |
| [maxBandwidth](network-maxbandwidth.md)           | Especifica ou recupera a largura de banda máxima permitida.                                       |
| [maxBitRate](network-maxbitrate.md)               | Recupera a taxa máxima de bits de vídeo possível.                                              |
| [receivedPackets](network-receivedpackets.md)     | Recupera o número de pacotes recebidos.                                                   |
| [receptionQuality](network-receptionquality.md)   | Recupera a porcentagem de pacotes recebidos nos últimos 30 segundos.                        |
| [recoveredPackets](network-recoveredpackets.md)   | Recupera o número de pacotes recuperados.                                                  |
| [sourceProtocol](network-sourceprotocol.md)       | Recupera o protocolo de origem usado para receber dados.                                         |



 

O objeto de **rede** dá suporte aos métodos a seguir.



| Método                                                       | Descrição                                                                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [getProxyBypassForLocal](network-getproxybypassforlocal.md) | Recupera um valor que indica se o servidor proxy deve ser ignorado se o servidor de origem estiver em uma rede local. |
| [getProxyExceptionList](network-getproxyexceptionlist.md)   | Recupera a lista de exceções de proxy.                                                                                  |
| [getproxyname](network-getproxyname.md)                     | Recupera o nome de um servidor proxy a ser usado.                                                                         |
| [getProxyPort](network-getproxyport.md)                     | Recupera a porta proxy a ser usada.                                                                                     |
| [getProxySettings](network-getproxysettings.md)             | Recupera a configuração de proxy para um determinado protocolo.                                                                    |
| [setProxyBypassForLocal](network-setproxybypassforlocal.md) | Especifica um valor que indica se o servidor proxy deve ser ignorado se o servidor de origem estiver em uma rede local. |
| [setProxyExceptionList](network-setproxyexceptionlist.md)   | Especifica a lista de exceções de proxy.                                                                                  |
| [setproxyname](network-setproxyname.md)                     | Especifica o nome de um servidor proxy a ser usado.                                                                         |
| [setProxyPort](network-setproxyport.md)                     | Especifica a porta proxy a ser usada.                                                                                     |
| [setProxySettings](network-setproxysettings.md)             | Especifica a configuração de proxy para um determinado protocolo.                                                                    |



 

O objeto de **rede** é acessado por meio da propriedade a seguir.



| Objeto                      | Propriedade                      |
|-----------------------------|-------------------------------|
| [Jogador](player-object.md) | [network](player-network.md) |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de modelo de objeto para scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




