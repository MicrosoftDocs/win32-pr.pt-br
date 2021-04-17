---
title: Interface IWMPNetwork (VB e C) (WMP. h)
description: Fornece propriedades e métodos para acessar estatísticas relacionadas à qualidade de uma conexão de rede e para especificar e recuperar as configurações de proxy de rede. A interface IWMPNetwork expõe as propriedades a seguir.
ms.assetid: d385510f-11cf-4a2a-96be-b416cddc3d80
keywords:
- IWMPNetwork (VB e C) interface do Windows Media Player
- IWMPNetwork (VB e C) interface do Windows Media Player, descrito
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
ms.openlocfilehash: 301fe5c89d2eb5df3dd4c22927e75a5607e7abd0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780220"
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
| [**getproxyname**](wmplibiwmpnetwork-iwmpnetwork-getproxyname--vb-and-c.md)                     | Retorna o nome do servidor proxy que está sendo usado.<br/>                                                            |
| [**getProxyPort**](wmplibiwmpnetwork-iwmpnetwork-getproxyport--vb-and-c.md)                     | Retorna a porta do proxy que está sendo usada.<br/>                                                                          |
| [**getProxySettings**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)             | Retorna informações sobre as configurações de proxy para um protocolo.<br/>                                                |
| [**setProxyBypassForLocal**](wmplibiwmpnetwork-iwmpnetwork-setproxybypassforlocal--vb-and-c.md) | Especifica se o servidor proxy será ignorado se o servidor de origem estiver em uma rede local.<br/>                  |
| [**setProxyExceptionList**](wmplibiwmpnetwork-iwmpnetwork-setproxyexceptionlist--vb-and-c.md)   | Especifica a lista de exceções de proxy.<br/>                                                                         |
| [**setproxyname**](wmplibiwmpnetwork-iwmpnetwork-setproxyname--vb-and-c.md)                     | Especifica o nome do servidor proxy a ser usado.<br/>                                                              |
| [**setProxyPort**](wmplibiwmpnetwork-iwmpnetwork-setproxyport--vb-and-c.md)                     | Especifica a porta proxy a ser usada.<br/>                                                                            |
| [**setProxySettings**](wmplibiwmpnetwork-iwmpnetwork-setproxysettings--vb-and-c.md)             | Especifica as configurações de proxy para um protocolo.<br/>                                                                |



 

### <a name="properties"></a>Propriedades

A interface **IWMPNetwork (VB e C#)** tem essas propriedades.



| Propriedade                                                                                          | Tipo de acesso           | Descrição                                                                                  |
|:--------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------|
| [**Larga**](wmplibiwmpnetwork-iwmpnetwork-bandwidth--vb-and-c.md)<br/>                 | Somente leitura<br/>  | Obtém a largura de banda atual do item de mídia.<br/>                                     |
| [**720p**](wmplibiwmpnetwork-iwmpnetwork-bitrate--vb-and-c.md)<br/>                     | Somente leitura<br/>  | Obtém a taxa de bits atual sendo recebida.<br/>                                         |
| [**bufferingCount**](wmplibiwmpnetwork-iwmpnetwork-bufferingcount--vb-and-c.md)<br/>       | Somente leitura<br/>  | Obtém o número de vezes que o buffer ocorreu durante a reprodução.<br/>                      |
| [**bufferingProgress**](wmplibiwmpnetwork-iwmpnetwork-bufferingprogress--vb-and-c.md)<br/> | Somente leitura<br/>  | Obtém a porcentagem de buffer concluído.<br/>                                       |
| [**bufferingTime**](wmplibiwmpnetwork-iwmpnetwork-bufferingtime--vb-and-c.md)<br/>         | Leitura/gravação<br/> | Obtém ou define a quantidade de tempo de buffer em milissegundos antes que a reprodução seja iniciada.<br/> |
| [**downloadProgress**](wmplibiwmpnetwork-iwmpnetwork-downloadprogress--vb-and-c.md)<br/>   | Somente leitura<br/>  | Obtém a porcentagem de download concluído.<br/>                                     |
| [**encodedFrameRate**](wmplibiwmpnetwork-iwmpnetwork-encodedframerate--vb-and-c.md)<br/>   | Somente leitura<br/>  | Obtém a taxa de quadros de vídeo especificada pelo autor do conteúdo.<br/>                        |
| [**Quadros**](wmplibiwmpnetwork-iwmpnetwork-framerate--vb-and-c.md)<br/>                 | Somente leitura<br/>  | Obtém a taxa de quadros de vídeo atual.<br/>                                                |
| [**framesSkipped**](wmplibiwmpnetwork-iwmpnetwork-framesskipped--vb-and-c.md)<br/>         | Somente leitura<br/>  | Obtém o número total de quadros ignorados durante a reprodução.<br/>                          |
| [**lostPackets**](wmplibiwmpnetwork-iwmpnetwork-lostpackets--vb-and-c.md)<br/>             | Somente leitura<br/>  | Obtém o número de pacotes perdidos.<br/>                                                  |
| [**maxBandwidth**](wmplibiwmpnetwork-iwmpnetwork-maxbandwidth--vb-and-c.md)<br/>           | Leitura/gravação<br/> | Obtém ou define a largura de banda máxima permitida.<br/>                                       |
| [**maxBitRate**](wmplibiwmpnetwork-iwmpnetwork-maxbitrate--vb-and-c.md)<br/>               | Somente leitura<br/>  | Obtém a taxa máxima de bits de vídeo possível.<br/>                                         |
| [**receivedPackets**](wmplibiwmpnetwork-iwmpnetwork-receivedpackets--vb-and-c.md)<br/>     | Somente leitura<br/>  | Obtém o número de pacotes recebidos.<br/>                                              |
| [**receptionQuality**](wmplibiwmpnetwork-iwmpnetwork-receptionquality--vb-and-c.md)<br/>   | Somente leitura<br/>  | Obtém a porcentagem de pacotes que não são perdidos nos últimos 30 segundos.<br/>                   |
| [**recoveredPackets**](wmplibiwmpnetwork-iwmpnetwork-recoveredpackets--vb-and-c.md)<br/>   | Somente leitura<br/>  | Obtém o número de pacotes recuperados.<br/>                                             |
| [**sourceProtocol**](wmplibiwmpnetwork-iwmpnetwork-sourceprotocol--vb-and-c.md)<br/>       | Somente leitura<br/>  | Obtém o protocolo de origem usado para receber dados.<br/>                                    |



 

Obtenha uma interface **IWMPNetwork** usando a propriedade a seguir.



| Objeto                                                                   | Propriedade                                                           |
|--------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Objeto AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**rede**](axwmplib-axwindowsmediaplayer-network--vb-and-c.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces para Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





