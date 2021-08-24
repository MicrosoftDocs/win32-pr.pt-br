---
title: Usando a alternância de fluxo de eventos ao vivo
description: Usando a alternância de fluxo de eventos ao vivo
ms.assetid: fa8af007-2db6-438f-9551-8e748bb79ef4
keywords:
- Windows Playlists de metarquivo de mídia, alternância de fluxo de eventos ao vivo
- listas de reprodução, alternância de fluxo de eventos ao vivo
- listas de reprodução de metarquivo, alternância de fluxo de eventos ao vivo
- Windows Playlists de metarquivo de mídia, alternância de fluxo de eventos
- listas de reprodução, alternância de fluxo de eventos
- listas de reprodução de metarquivo, alternância de fluxo de eventos
- Windows Playlists de metarquivo de mídia, inserção de anúncio
- listas de reprodução, inserção de anúncio
- listas de reprodução de metarquivo, inserção de anúncio
- Windows Media Player, alternância de fluxo de eventos ao vivo
- Windows Media Player, alternância de fluxo de eventos
- Windows Media Player, inserção do ad
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
ms.openlocfilehash: d8524fe1a83a6b3276c274726fa27fa7fcccb97b88f0384a54e5433d09380501
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134359"
---
# <a name="using-live-event-stream-switching"></a>Usando a alternância de fluxo de eventos ao vivo

a mídia de Streaming também pode ser controlada pela interação dos comandos de script inseridos em um fluxo de mídia com Windows elementos de metarquivo de mídia em uma lista de reprodução de metarquivo.

Um evento é um tipo específico de comando de script inserido em um fluxo de mídia ou arquivo de mídia. quando o controle de Windows Media Player recebe o comando de script, ele processa o evento conforme definido pelo elemento **event** na lista de reprodução do metarquivo. Windows Media Player alternar do fluxo atual que está renderizando e renderiza o conteúdo referenciado no elemento de **evento** de playlist de metarquivo. O elemento **Event** geralmente é usado na produção ao vivo.

Um elemento de **evento** é semelhante a um elemento de **entrada** , mas cada um manipula a reprodução de fluxos e arquivos de mídia de forma diferente. O elemento **entry** é usado para criar listas de reprodução. Um fluxo ou arquivo de mídia referenciado em um elemento de **entrada** começa a ser reproduzido quando o fluxo ou o arquivo de mídia referenciado na **entrada** anterior é concluído. Um fluxo referenciado em um **evento** é executado somente quando um comando de script específico é recebido. por exemplo, quando Windows Media Player recebe um comando de script com a cadeia de caracteres de tipo "EVENT" e a cadeia de caracteres de comando "Adlink", ele pesquisa os seguintes elementos na lista de reprodução.


```XML
<EVENT NAME="Adlink" WHENDONE="RESUME"> 
    <ENTRY HREF=mms://www.proseware.com/adlink.wma />
</EVENT>

```



Windows Media Player, em seguida, muda da transmissão ao vivo para reproduzir o fluxo ou arquivo de mídia contido no **evento**, neste caso, Adlink. wma. o código `WHENDONE="RESUME"` instrui Windows Media Player a retomar a reprodução do fluxo anterior quando o Adlink. wma for concluído.

> [!Note]  
> A falha ao manipular todos os eventos inseridos em um fluxo de mídia ou arquivo de mídia pode gerar resultados inesperados.

 

Se você quiser usar a alternância de fluxo de eventos ao vivo, deverá incluir um elemento de **evento** em sua lista de reprodução para manipular cada comando de script de evento inserido nos fluxos de mídia ou nos arquivos de mídia em sua lista de reprodução. Antes de criar sua lista de reprodução, você deve saber os detalhes sobre quais comandos de script são inseridos no seu conteúdo de mídia digital. se houver um comando de script de evento que você deseja que Windows Media Player ignore, inclua um elemento de **evento** em sua lista de reprodução para manipular o evento, mas faça referência a uma URL fictícia no manipulador de eventos.

## <a name="ad-insertion"></a>Inserção de anúncio

Essa técnica pode ser usada para inserção de anúncios. por exemplo, durante uma transmissão ao vivo pela Internet de um jogo de bola, um comando pode ser enviado no início de cada interrupção comercial que instrui cada cliente (Windows Media Player) a reproduzir os negócios listados em sua lista de reprodução. Quando os clientes terminarem de reproduzir os negócios, a lista de reprodução instruirá cada cliente a recortar para a transmissão ao vivo. O conteúdo de mídia do **evento** será renderizado somente quando a mídia de streaming que está sendo acessada difundir o script incorporado com o nome do **evento** correspondente.

as possibilidades inerentes à alternância de **eventos** são mais bem apreciadas ao contrastarem como os anúncios atingem os visualizadores por meio de transmissão padrão por satélite com o modo como os anúncios podem acessar os visualizadores usando as tecnologias de mídia Windows. Historicamente, os anúncios de difusão podem ser apenas aproximadamente direcionados para os visualizadores, usando dados de classificação como os critérios primários. os anúncios enviados usando Windows tecnologias de mídia podem ser direcionados diretamente ao usuário de destino, pois os **eventos** e as listas de reprodução podem ser criados dinamicamente com base na entrada do usuário. Para obter mais informações, consulte [Personalizando a entrega de mídia](personalizing-media-delivery.md).

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

[**Windows Referência de elementos de metarquivo de mídia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guia de metarquivo de mídia**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




