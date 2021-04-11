---
title: Usando a alternância de fluxo de eventos ao vivo
description: Usando a alternância de fluxo de eventos ao vivo
ms.assetid: fa8af007-2db6-438f-9551-8e748bb79ef4
keywords:
- Playlists do metarquivo do Windows Media, alternância de fluxo de eventos ao vivo
- listas de reprodução, alternância de fluxo de eventos ao vivo
- listas de reprodução de metarquivo, alternância de fluxo de eventos ao vivo
- Playlists do metarquivo do Windows Media, alternância de fluxo de eventos
- listas de reprodução, alternância de fluxo de eventos
- listas de reprodução de metarquivo, alternância de fluxo de eventos
- Playlists do metarquivo do Windows Media, inserção do AD
- listas de reprodução, inserção de anúncio
- listas de reprodução de metarquivo, inserção de anúncio
- Windows Media Player, alternância de fluxo de eventos ao vivo
- Windows Media Player, alternância de fluxo de eventos
- Windows Media Player, inserção de anúncio
- alternância de fluxo de eventos ao vivo
- alternância de fluxo de eventos
- inserção de anúncio
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fd5c586e0f1ef2b36913dee822e461daeffbfcbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159519"
---
# <a name="using-live-event-stream-switching"></a>Usando a alternância de fluxo de eventos ao vivo

A mídia de streaming também pode ser controlada pela interação dos comandos de script inseridos em um fluxo de mídia com elementos do metarquivo do Windows Media em uma lista de reprodução de metarquivo.

Um evento é um tipo específico de comando de script inserido em um fluxo de mídia ou arquivo de mídia. Quando o controle do Windows Media Player recebe o comando de script, ele processa o evento conforme definido pelo elemento **Event** na lista de reprodução do metarquivo. O Windows Media Player alterna do fluxo atual que está renderizando e renderiza o conteúdo referenciado no elemento de **evento** de playlist de metarquivo. O elemento **Event** geralmente é usado na produção ao vivo.

Um elemento de **evento** é semelhante a um elemento de **entrada** , mas cada um manipula a reprodução de fluxos e arquivos de mídia de forma diferente. O elemento **entry** é usado para criar listas de reprodução. Um fluxo ou arquivo de mídia referenciado em um elemento de **entrada** começa a ser reproduzido quando o fluxo ou o arquivo de mídia referenciado na **entrada** anterior é concluído. Um fluxo referenciado em um **evento** é executado somente quando um comando de script específico é recebido. Por exemplo, quando o Windows Media Player recebe um comando de script com a cadeia de caracteres de tipo "EVENT" e a cadeia de caracteres de comando "Adlink", ele pesquisa os seguintes elementos na lista de reprodução.


```XML
<EVENT NAME="Adlink" WHENDONE="RESUME"> 
    <ENTRY HREF=mms://www.proseware.com/adlink.wma />
</EVENT>

```



Em seguida, o Windows Media Player alterna da transmissão ao vivo para reproduzir o fluxo ou o arquivo de mídia contido no **evento**, neste caso, Adlink. WMA. O código `WHENDONE="RESUME"` instrui o Windows Media Player a retomar a reprodução do fluxo anterior quando o Adlink. WMA for concluído.

> [!Note]  
> A falha ao manipular todos os eventos inseridos em um fluxo de mídia ou arquivo de mídia pode gerar resultados inesperados.

 

Se você quiser usar a alternância de fluxo de eventos ao vivo, deverá incluir um elemento de **evento** em sua lista de reprodução para manipular cada comando de script de evento inserido nos fluxos de mídia ou nos arquivos de mídia em sua lista de reprodução. Antes de criar sua lista de reprodução, você deve saber os detalhes sobre quais comandos de script são inseridos no seu conteúdo de mídia digital. Se houver um comando de script de evento que você deseja que o Windows Media Player ignore, inclua um elemento de **evento** em sua lista de reprodução para manipular o evento, mas faça referência a uma URL fictícia no manipulador de eventos.

## <a name="ad-insertion"></a>Inserção de anúncio

Essa técnica pode ser usada para inserção de anúncios. Por exemplo, durante uma transmissão ao vivo pela Internet de um jogo de bola, um comando pode ser enviado no início de cada interrupção comercial que instrui cada cliente (Windows Media Player) a reproduzir comerciais listados em sua lista de reprodução. Quando os clientes terminarem de reproduzir os negócios, a lista de reprodução instruirá cada cliente a recortar para a transmissão ao vivo. O conteúdo de mídia do **evento** será renderizado somente quando a mídia de streaming que está sendo acessada difundir o script incorporado com o nome do **evento** correspondente.

As possibilidades inerentes à alternância de **eventos** são mais bem apreciadas ao contrastarem como os anúncios atingem os visualizadores por meio de transmissão padrão por satélite com o modo como os anúncios podem acessar os visualizadores usando tecnologias de mídia do Windows. Historicamente, os anúncios de difusão podem ser apenas aproximadamente direcionados para os visualizadores, usando dados de classificação como os critérios primários. Os anúncios enviados usando tecnologias de mídia do Windows podem ser direcionados diretamente ao usuário de destino, pois os **eventos** e as listas de reprodução podem ser criados dinamicamente com base na entrada do usuário. Para obter mais informações, consulte [Personalizando a entrega de mídia](personalizing-media-delivery.md).

Você também pode usar listas de reprodução de metarquivo para exibir gráficos, áudio e texto personalizados para publicidade. Você pode usar o elemento **banner** como um elemento filho de um **evento** para exibir um gráfico de mensagem de anúncio. O elemento **banner** fornece o caminho e o arquivo que contém os elementos gráficos para sua faixa publicitária. Você também pode fornecer um link para um site ou arquivo usando o elemento filho **moreinfo** . A URL no elemento **moreinfo** pode fornecer um link para ainda mais anúncios na Web. O exemplo a seguir demonstra como usar esses elementos.

Código de exemplo


```XML
<BANNER HREF="SomePath\2.gif">
    <ABSTRACT>Read This Ad and Buy.</ABSTRACT>
    <MOREINFO HREF="https://www.proseware.com" />
</BANNER>

```



O exemplo a seguir insere o AD anúncio. WMA no fluxo unicast de difusão BallGame quando um cliente recebe um **evento** de comando de script com o atributo **Name** definido como "tempo limite". **CLIENTSKIP** é definido como não para impedir que o anúncio em fluxo seja ignorado. Neste exemplo, o anúncio transmitido deve ser reproduzido antes de retornar ao fluxo original. Quando o anúncio é concluído, o cliente retoma a reprodução do fluxo original.

Código de exemplo


```XML
<ASX VERSION="3.0">
    <ENTRY>
        <REF HREF="mms://proseware.com/BallGame" />
    </ENTRY>
    <EVENT NAME="Time-Out" WHENDONE="RESUME">
        <ENTRY>
            <REF HREF = "mms://proseware.com/Advert.wma" 
                CLIENTSKIP = "NO" />
       </ENTRY>
    </EVENT>
</ASX>

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Playlists de metarquivo**](metafile-playlists.md)
</dt> <dt>

[**Usando listas de reprodução de metarquivo**](using-metafile-playlists.md)
</dt> <dt>

[**Referência de elementos de metarquivo do Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guia de metarquivo do Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




