---
title: Registrando dados de fluxo de log
description: Registrando dados de fluxo de log
ms.assetid: c902a755-afdd-4dea-bc3e-036555fdff10
keywords:
- Windows Playlists de metadados de mídia, registro em log de dados de fluxo
- playlists, registro em log de dados de fluxo
- listas de reprodução de metadados, registro em log de dados de fluxo
- Windows Playlists de metadados de mídia, log de dados de fluxo
- playlists, log de dados de fluxo
- listas de reprodução de metadados, log de dados de fluxo
- registro em log de dados de fluxo
- registro em log de dados de fluxo
- Windows Media Player, registrando dados de fluxo
- Windows Media Player, registro em log de dados de fluxo
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c0a2ae6fe4b647e8a5c19fc6f30562973b3280f37cd3af3a1b9d9093771959de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118860"
---
# <a name="logging-stream-data"></a>Registrando dados de fluxo de log

As informações registradas podem ser adquiridas e usadas para determinar o comportamento do visualizador, por exemplo, com que frequência um fluxo é exibido ou se um usuário específico exibiu um fluxo e por quanto tempo em qual qualidade.

As informações de registro em log são enviadas automaticamente ao servidor do qual a playlist foi originada. Você também pode enviar informações de log para servidores adicionais, incluindo servidores Web que você usa exclusivamente para registro em log. Para fazer isso, use o **elemento LOGURL,** especificando uma URL válida para o **atributo HREF.** Você pode incluir **elementos LOGURL** como filhos do **elemento ASX** e como filhos de elementos **ENTRY** individuais. Quando a playlist é aberta pela primeira vez, as informações de log são enviadas para o servidor de origem e para cada URL especificada em filhos **LOGURL** do **elemento ASX.** Em seguida, conforme cada entrada é atingida, as informações de registro em log específicas dessa entrada são enviadas para cada URL especificada em **filhos LOGURL** do **elemento ENTRY.**

O SDK Windows Media Format dá suporte ao elemento **LOGURL** por meio da interface **IWMSReaderNetworkConfig** e dos seguintes métodos:


```XML
HRESULT AddLoggingUrl(LPCWSTR pwszUrl);
HRESULT GetLoggingUrl(DWORD dwIndex, LPCWSTR pwszUrl, DWORD *pcchUrl);
HRESULT GetLoggingUrlCount(DWORD *pdwUrlCount);
HRESULT ResetLoggingUrlList();

```



Além das informações registradas automaticamente, uma playlist de metadados pode registrar informações personalizadas por meio do uso do **elemento PARAM.** Para usar o elemento **PARAM** dessa forma, de definir o atributo **NAME** como "log:" seguido por um nome de campo de log e um namespace XML opcional separado do nome do campo por outros dois-pontos (":"). Tudo após o segundo dois-pontos é tratado como um namespace, portanto, o nome do campo não deve conter dois-pontos.

O campo de log especificado no **atributo NAME** é definido como o valor do **atributo VALUE.** Se o log ainda não tiver um campo com o nome especificado, ele será adicionado.

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

[**Playlists de metadados**](metafile-playlists.md)
</dt> <dt>

[**Windows Referência de elementos de metadados de mídia**](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 




