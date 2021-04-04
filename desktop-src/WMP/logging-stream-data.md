---
title: Log de dados de fluxo
description: Log de dados de fluxo
ms.assetid: c902a755-afdd-4dea-bc3e-036555fdff10
keywords:
- Listas de reprodução do metarquivo do Windows Media, log de dados de fluxo
- listas de reprodução, log de dados de fluxo
- listas de reprodução de metarquivo, log de dados de fluxo
- Playlists do metarquivo do Windows Media, log de dados de fluxo
- listas de reprodução, log de dados de fluxo
- playlists de metarquivo, log de dados de fluxo
- log de dados de fluxo
- log de dados de fluxo
- Windows Media Player, log de dados de fluxo
- Windows Media Player, log de dados de fluxo
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f234851cabf071ed2308fb5c96df2b53b60b9d45
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084129"
---
# <a name="logging-stream-data"></a>Log de dados de fluxo

As informações registradas podem ser adquiridas e usadas para determinar o comportamento do visualizador, por exemplo, com que frequência um fluxo é exibido ou se um usuário específico exibiu um fluxo e por quanto tempo a qualidade.

As informações de log são enviadas automaticamente para o servidor do qual a lista de reprodução foi originada. Você também pode enviar informações de log para servidores adicionais, incluindo servidores Web que você usa exclusivamente para registro em log. Para fazer isso, use o elemento **LogURL** , ESPECIFICANDO uma URL válida para o atributo **href** . Você pode incluir elementos **LogURL** como filhos do elemento **ASX** e como filhos de elementos de **entrada** individuais. Quando a playlist é aberta pela primeira vez, as informações de log são enviadas para o servidor de origem e para cada URL especificada em **LogURL** filhos do elemento **ASX** . Em seguida, à medida que cada entrada é atingida, as informações de log específicas para essa entrada são enviadas para cada URL especificada em **LogURL** filhos do elemento de **entrada** .

O SDK do Windows Media Format dá suporte ao elemento **LogURL** por meio da interface **IWMSReaderNetworkConfig** e dos seguintes métodos:


```XML
HRESULT AddLoggingUrl(LPCWSTR pwszUrl);
HRESULT GetLoggingUrl(DWORD dwIndex, LPCWSTR pwszUrl, DWORD *pcchUrl);
HRESULT GetLoggingUrlCount(DWORD *pdwUrlCount);
HRESULT ResetLoggingUrlList();

```



Além das informações que são registradas automaticamente, uma lista de reprodução de metarquivo pode registrar informações personalizadas por meio do uso do elemento **param** . Para usar o elemento **param** dessa forma, defina o atributo **Name** como "log:" seguido de um nome de campo de log e um namespace XML opcional separado do nome do campo por dois pontos (":"). Tudo depois que o segundo dois pontos é tratado como um namespace, portanto, o nome do campo não deve conter dois-pontos.

O campo de log especificado no atributo **Name** é definido como o valor do atributo **Value** . Se o log ainda não contiver um campo com o nome especificado, ele será adicionado.

**Código de exemplo**


```XML

    <ASX version="3.0">
      <LOGURL href="https://www.proseware.com/log.asp?SomeArg=SomeVal" />
      <ENTRY>
        <REF href="mms://ucast.proseware.com/Media1.wma" />
        <LOGURL href="https://www.proseware.com/cgi-bin/logging.pl?SomeArg=SomeVal" />
        <LOGURL href="https://www.proseware.com/WMLogging.dll?SomeArg=SomeVal" />
        <PARAM name="log:cs-media-role" value="Advertisement"/>
        <PARAM name="log:cs-media-name:namespace" value="Music"/>
        <REF href=rtsp://ucast.proseware.com/Media1.wma"/>
      </ENTRY>
      <ENTRY>
        <REF href="mms://ucast.proseware.com/Media2.wma"/>
      </ENTRY>
    </ASX>
    

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Playlists de metarquivo**](metafile-playlists.md)
</dt> <dt>

[**Referência de elementos de metarquivo do Windows Media**](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 




