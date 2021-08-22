---
title: Interface IWMPNetwork (VB e C ) (Wmp.h)
description: Fornece propriedades e métodos para acessar estatísticas relacionadas à qualidade de uma conexão de rede e para especificar e recuperar as configurações de proxy de rede. A interface IWMPNetwork expõe as propriedades a seguir.
ms.assetid: d385510f-11cf-4a2a-96be-b416cddc3d80
keywords:
- Interface IWMPNetwork (VB e C) Windows Media Player
- Interface IWMPNetwork (VB e C ) Windows Media Player , descrita
topic_type:
- apiref
api_name:
- IWMPNetwork (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93110b25bd7d194c4f1d7c213228512fd8bc6000df15b726e3f32a6e6e79a62a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119572446"
---
# <a name="iwmpnetwork-vb-and-c-interface"></a>Interface IWMPNetwork (VB e C#)

Fornece propriedades e métodos para acessar estatísticas relacionadas à qualidade de uma conexão de rede e para especificar e recuperar as configurações de proxy de rede.

A interface **IWMPNetwork** expõe as propriedades a seguir.

## <a name="members"></a>Membros

A interface **IWMPNetwork (VB e C#)** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IWMPNetwork (VB e C#)** tem esses métodos.



| Método                                                                                           | Descrição                                                                                                            |
|:-------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [**getProxyBypassForLocal**](iwmpnetwork-getproxybypassforlocal--vb-and-c.md)                   | Retorna um valor que indica se o servidor proxy será ignorado se o servidor de origem estiver em uma rede local.<br/> |
| [**getProxyExceptionList**](wmplibiwmpnetwork-iwmpnetwork-getproxyexceptionlist--vb-and-c.md)   | Retorna a lista de exceções de proxy.<br/>                                                                           |
| [**getProxyName**](wmplibiwmpnetwork-iwmpnetwork-getproxyname--vb-and-c.md)                     | Retorna o nome do servidor proxy que está sendo usado.<br/>                                                            |
| [**getProxyPort**](wmplibiwmpnetwork-iwmpnetwork-getproxyport--vb-and-c.md)                     | Retorna a porta proxy que está sendo usada.<br/>                                                                          |
| [**getProxySettings**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)             | Retorna informações sobre as configurações de proxy para um protocolo.<br/>                                                |
| [**setProxyBypassForLocal**](wmplibiwmpnetwork-iwmpnetwork-setproxybypassforlocal--vb-and-c.md) | Especifica se o servidor proxy será ignorado se o servidor de origem estiver em uma rede local.<br/>                  |
| [**setProxyExceptionList**](wmplibiwmpnetwork-iwmpnetwork-setproxyexceptionlist--vb-and-c.md)   | Especifica a lista de exceções de proxy.<br/>                                                                         |
| [**setProxyName**](wmplibiwmpnetwork-iwmpnetwork-setproxyname--vb-and-c.md)                     | Especifica o nome do servidor proxy a ser usado.<br/>                                                              |
| [**setProxyPort**](wmplibiwmpnetwork-iwmpnetwork-setproxyport--vb-and-c.md)                     | Especifica a porta proxy a ser usada.<br/>                                                                            |
| [**setProxySettings**](wmplibiwmpnetwork-iwmpnetwork-setproxysettings--vb-and-c.md)             | Especifica as configurações de proxy para um protocolo.<br/>                                                                |



 

### <a name="properties"></a>Propriedades

A interface **IWMPNetwork (VB e C#)** tem essas propriedades.



| Propriedade                                                                                          | Tipo de acesso           | Descrição                                                                                  |
|:--------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------|
| [**Banda**](wmplibiwmpnetwork-iwmpnetwork-bandwidth--vb-and-c.md)<br/>                 | Somente leitura<br/>  | Obtém a largura de banda atual do item de mídia.<br/>                                     |
| [**Bitrate**](wmplibiwmpnetwork-iwmpnetwork-bitrate--vb-and-c.md)<br/>                     | Somente leitura<br/>  | Obtém a taxa de bits atual que está sendo recebida.<br/>                                         |
| [**bufferingCount**](wmplibiwmpnetwork-iwmpnetwork-bufferingcount--vb-and-c.md)<br/>       | Somente leitura<br/>  | Obtém o número de vezes que o buffer ocorreu durante a reprodução.<br/>                      |
| [**bufferingProgress**](wmplibiwmpnetwork-iwmpnetwork-bufferingprogress--vb-and-c.md)<br/> | Somente leitura<br/>  | Obtém o percentual de buffer concluído.<br/>                                       |
| [**bufferingTime**](wmplibiwmpnetwork-iwmpnetwork-bufferingtime--vb-and-c.md)<br/>         | Leitura/gravação<br/> | Obtém ou define a quantidade de tempo de buffer em milissegundos antes do início da reprodução.<br/> |
| [**downloadProgress**](wmplibiwmpnetwork-iwmpnetwork-downloadprogress--vb-and-c.md)<br/>   | Somente leitura<br/>  | Obtém o percentual de download concluído.<br/>                                     |
| [**encodedFrameRate**](wmplibiwmpnetwork-iwmpnetwork-encodedframerate--vb-and-c.md)<br/>   | Somente leitura<br/>  | Obtém a taxa de quadros de vídeo especificada pelo autor do conteúdo.<br/>                        |
| [**Framerate**](wmplibiwmpnetwork-iwmpnetwork-framerate--vb-and-c.md)<br/>                 | Somente leitura<br/>  | Obtém a taxa de quadros de vídeo atual.<br/>                                                |
| [**framesSkipped**](wmplibiwmpnetwork-iwmpnetwork-framesskipped--vb-and-c.md)<br/>         | Somente leitura<br/>  | Obtém o número total de quadros ignorados durante a reprodução.<br/>                          |
| [**lostPackets**](wmplibiwmpnetwork-iwmpnetwork-lostpackets--vb-and-c.md)<br/>             | Somente leitura<br/>  | Obtém o número de pacotes perdidos.<br/>                                                  |
| [**maxBandwidth**](wmplibiwmpnetwork-iwmpnetwork-maxbandwidth--vb-and-c.md)<br/>           | Leitura/gravação<br/> | Obtém ou define a largura de banda máxima permitida.<br/>                                       |
| [**maxBitRate**](wmplibiwmpnetwork-iwmpnetwork-maxbitrate--vb-and-c.md)<br/>               | Somente leitura<br/>  | Obtém a taxa máxima de bits de vídeo possível.<br/>                                         |
| [**receivedPackets**](wmplibiwmpnetwork-iwmpnetwork-receivedpackets--vb-and-c.md)<br/>     | Somente leitura<br/>  | Obtém o número de pacotes recebidos.<br/>                                              |
| [**igualdade de recepção**](wmplibiwmpnetwork-iwmpnetwork-receptionquality--vb-and-c.md)<br/>   | Somente leitura<br/>  | Obtém o percentual de pacotes não perdidos nos últimos 30 segundos.<br/>                   |
| [**recoveredPackets**](wmplibiwmpnetwork-iwmpnetwork-recoveredpackets--vb-and-c.md)<br/>   | Somente leitura<br/>  | Obtém o número de pacotes recuperados.<br/>                                             |
| [**sourceProtocol**](wmplibiwmpnetwork-iwmpnetwork-sourceprotocol--vb-and-c.md)<br/>       | Somente leitura<br/>  | Obtém o protocolo de origem usado para receber dados.<br/>                                    |



 

Obter uma interface **IWMPNetwork** usando a propriedade a seguir.



| Objeto                                                                   | Propriedade                                                           |
|--------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Objeto AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**Rede**](axwmplib-axwindowsmediaplayer-network--vb-and-c.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces para Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





