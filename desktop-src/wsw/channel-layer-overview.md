---
title: Visão geral da camada de canal
description: A camada de canal fornece uma abstração do canal de transporte, bem como as mensagens enviadas no canal.
ms.assetid: d7dddcc6-8eb0-4ee6-8cf5-7701a2be7a19
keywords:
- Serviços Web de visão geral da camada de canal para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e52c4844bee472d4d22df7681fece16330f30cf
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104566215"
---
# <a name="channel-layer-overview"></a>Visão geral da camada de canal

A camada de canal fornece uma abstração do canal de transporte, bem como as mensagens enviadas no canal. Ele também inclui funções para a serialização de tipos de dados C de e para estruturas SOAP. A camada de canal permite o controle total de comunicações por meio de [mensagens](message.md) que consistem em dados enviados ou recebidos e que contêm corpos e cabeçalhos, e [canais](channel.md) que abstraem protocolos de troca de mensagens e fornecem propriedades para personalizar as configurações.

## <a name="message"></a>Mensagem

Uma [mensagem](message.md) é um objeto que encapsula dados de rede, especificamente, dados transmitidos ou recebidos em uma rede. A estrutura da mensagem é definida pelo SOAP, com um conjunto discreto de cabeçalhos e um corpo da mensagem. Os cabeçalhos são colocados em um buffer de memória e o corpo da mensagem é lido ou gravado usando uma API de fluxo.

![Diagrama mostrando o cabeçalho e o corpo de uma mensagem.](images/messageenvelope.png)

Embora o modelo de dados de uma mensagem seja sempre o modelo de dados XML, o formato de conexão real é flexível. Antes que uma mensagem seja transmitida, ela é codificada usando uma codificação específica (como texto, binário ou MTOM). Consulte [**\_ codificação WS**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) para obter mais informações sobre codificações.

![Diagrama mostrando vários formatos de codificação de mensagem.](images/messageandencodings.png)

## <a name="channel"></a>Canal

Um [canal](channel.md) é um objeto usado para enviar e receber mensagens em uma rede entre dois ou mais pontos de extremidade.

Os canais têm dados associados que descrevem como [tratar](endpoint-address.md) a mensagem quando ela é enviada. O envio de uma mensagem em um canal é como colocá-lo em uma rampa — o canal inclui as informações em que a mensagem deve ir e como obtê-la.

![Diagrama mostrando canais para mensagens.](images/channelsaschute.png)

Os canais são categorizados em [**tipos de canal**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type). Um tipo de canal especifica quais mensagens de direção podem fluir. O tipo de canal também identifica se o canal é de sessão ou de sessão. Uma sessão é definida como uma maneira abstrata de correlacionar mensagens entre duas ou mais partes. Um exemplo de um canal de sessão é um canal TCP, que usa a conexão TCP como a implementação da sessão concreta. Um exemplo de um canal sem sessão é UDP, que não tem um mecanismo de sessão subjacente. Embora HTTP tenha conexões TCP subjacentes, esse fato não é exposto diretamente por essa API e, portanto, HTTP também é considerado um canal sem sessão.

![Diagrama mostrando tipos de canal de sessão e de sessão.](images/channeltypes.png)

Embora os tipos de canal descrevam a direção e as informações de sessão para um canal, eles não especificam como o canal é implementado. Qual protocolo o canal deve usar? Quão difícil o canal deve tentar entregar a mensagem? Que tipo de segurança é usado? Ele é singlecast ou multicast? Essas configurações são chamadas de "Associação" do canal. A associação consiste no seguinte:

-   Uma [**\_ \_ associação do WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), que identifica o protocolo de transferência a ser usado (TCP, UDP, http, NAMEDPIPE).
-   Uma [**\_ \_ Descrição de segurança do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), que especifica como proteger o canal.
-   Um conjunto [**de \_ \_ Propriedades s do WS Channel**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property), que especificam configurações opcionais adicionais. Consulte [**\_ ID de \_ propriedade \_ do WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) para obter a lista de propriedades.

![Diagrama mostrando uma lista de propriedades de canal.](images/channelsandbindings.png)

## <a name="listener"></a>Ouvinte

Para começar a se comunicar, o cliente cria um objeto de canal. Mas como o serviço obtém seu objeto de canal? Ele faz isso criando um [ouvinte](listener.md). A criação de um ouvinte requer as mesmas informações de ligação necessárias para criar um canal. Depois que um ouvinte tiver sido criado, o aplicativo poderá aceitar canais do ouvinte. Como o aplicativo pode ficar atrás na aceitação de canais, os ouvintes normalmente mantêm uma fila de canais que estão prontos para aceitar (até certa cota).

![Diagrama mostrando canais na fila de ouvintes.](images/channelaccept.png)

## <a name="initiating-communication-client"></a>Iniciando comunicação (cliente)

Para iniciar a comunicação no cliente, use a sequência a seguir.

``` syntax
WsCreateChannel
for each address being sent to
{
    WsOpenChannel           // open channel to address
    // send and/or receive messages
    WsCloseChannel          // close channel
    WsResetChannel?         // reset if opening again
}
WsFreeChannel
```

## <a name="accepting-communication-server"></a>Aceitando comunicação (servidor)

Para aceitar as comunicações de entrada no servidor, use a sequência a seguir.

``` syntax
WsCreateListener
WsOpenListener
for each channel being accepted (can be done in parallel)
{
    WsCreateChannelForListener
    for each accept
    {
        WsAcceptChannel     // accept the channel
        // send and/or receive messages
        WsCloseChannel      // close the channel
        WsResetChannel?     // reset if accepting again
    }
    WsFreeChannel
}
WsCloseListener
WsFreeListener
```

## <a name="sending-messages-client-or-server"></a>Enviando mensagens (cliente ou servidor)

Para enviar mensagens, use a sequência a seguir.

``` syntax
WsCreateMessageForChannel
for each message being sent
{
    WsSendMessage       // send message
    WsResetMessage?     // reset if sending another message
}
WsFreeMessage
```

A função [**WsSendMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendmessage) não permite streaming e pressupõe que o corpo contém apenas um elemento. Para evitar essas restrições, use a seguinte sequência em vez de **WsSendMessage**.

``` syntax
WsInitializeMessage     // initialize message to WS_BLANK_MESSAGE
WsSetHeader             // serialize action header into header buffer
WsAddressMessage?       // optionally address message
for each application defined header
{
    WsAddCustomHeader   // serialize application-defined headers into header buffer
}
WsWriteMessageStart     // write out the headers of the message
for each element of the body
{
    WsWriteBody         // serialize the element of the body
    WsFlushBody?        // optionally flush the body
}
WsWriteMessageEnd       // write the end of the message
```

A função [**WsWriteBody**](/windows/desktop/api/WebServices/nf-webservices-wswritebody) usa a serialização para gravar os elementos do corpo. Para gravar os dados diretamente no gravador de XML, use a seguinte sequência em vez de **WsWriteBody**.

``` syntax
WS_MESSAGE_PROPERTY_BODY_WRITER     // get the writer used to write the body
WsWriteStartElement
// use the writer functions to write the body
WsWriteEndElement
// optionally flush the body
WsFlushBody?        
```

A função [**WsAddCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsaddcustomheader) usa a serialização para definir os cabeçalhos para o buffer de cabeçalho da mensagem. Para usar o gravador de XML para gravar um cabeçalho, use a seguinte sequência em vez de **WsAddCustomHeader**.

``` syntax
WS_MESSAGE_PROPERTY_HEADER_BUFFER   // get the header buffer 
WsCreateWriter                      // create an xml writer
WsSetOutputToBuffer                 // specify output of writer should go to buffer
WsMoveWriter*                       // move to inside envelope header element
WsWriteStartElement                 // write application header start element
// use the writer functions to write the header 
WsWriteEndElement                   // write appilcation header end element
```

## <a name="receiving-messages-client-or-server"></a>Recebendo mensagens (cliente ou servidor)

Para receber mensagens, use a sequência a seguir.

``` syntax
WsCreateMessageForChannel
for each message being received
{
    WsReceiveMessage            // receive a message
    WsGetHeader*                // optionally access standard headers such as To or Action
    WsResetMessage              // reset if reading another message
}
WsFreeMessage
```

A função [**WsReceiveMessage**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage) não permite streaming e pressupõe que o corpo contenha apenas um elemento e que o tipo da mensagem (ação e esquema do corpo) seja conhecido com antecedência. Para evitar essas restrições, use a seguinte sequência em vez de **WsReceiveMessage**.

``` syntax
WsReadMessageStart              // read all headers into header buffer
for each standard header
{
    WsGetHeader                 // deserialize standard header such as To or Action
}
for each application defined header
{
    WsGetCustomHeader           // deserialize application defined header
}
for each element of the body
{
    WsFillBody?                 // optionally fill the body
    WsReadBody                  // deserialize element of body
}
WsReadMessageEnd                // read end of message
```

A função [**WsReadBody**](/windows/desktop/api/WebServices/nf-webservices-wsreadbody) usa a serialização para ler os elementos do corpo. Para ler os dados diretamente do [leitor de XML](xml-reader.md), use a seguinte sequência em vez de **WsReadBody**.

``` syntax
WS_MESSAGE_PROPERTY_BODY_READER     // get the reader used to read the body
WsFillBody?                         // optionally fill the body
WsReadToStartElement                // read up to the body element
WsReadStartElement                  // consume the start of the body element
// use the read functions to read the contents of the body element
WsReadEndElement                    // consume the end of the body element
```

As funções [**WsGetCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetcustomheader) usam a serialização para obter os cabeçalhos do buffer de cabeçalho da mensagem. Para usar o [leitor de XML](xml-reader.md) para ler um cabeçalho, use a seguinte sequência em vez de **WsGetCustomHeader**.

``` syntax
WS_MESSAGE_PROPERTY_HEADER_BUFFER   // get the header buffer 
WsCreateReader                      // create an xml reader
WsSetInputToBuffer                  // specify input of reader should be buffer
WsMoveReader*                       // move to inside header element
while looking for header to read
{
    WsReadToStartElement            // see if the header matches the application header
    if header matched
    {
        WsGetHeaderAttributes?      // get the standard header attributes
        WsReadStartElement          // consume the start of the header element
        // use the read functions to read the contents of the header element
        WsReadEndElement            // consume the end of the header element
    }
    else
    {
        WsSkipNode                  // skip the header element
    }
}                
```

## <a name="request-reply-client"></a>Solicitação de resposta (cliente)

A execução de uma solicitação-resposta no cliente pode ser feita com a sequência a seguir.

``` syntax
WsCreateMessageForChannel               // create request message 
WsCreateMessageForChannel               // create reply message 
for each request reply
{
    WsRequestReply                      // send request, receive reply
    WsResetMessage?                     // reset request message (if repeating)
    WsResetMessage?                     // reset reply message (if repeating)
}
WsFreeMessage                           // free request message
WsFreeMessage                           // free reply message
```

A função [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply) pressupõe um único elemento para o corpo da solicitação e as mensagens de resposta, e que o tipo da mensagem (ação e esquema do corpo) é conhecido com antecedência. Para evitar essas limitações, a solicitação e a mensagem de resposta podem ser enviadas manualmente, conforme mostrado na sequência a seguir. Essa sequência corresponde à sequência anterior para enviar e receber uma mensagem, exceto quando indicado.

``` syntax
WsInitializeMessage     // initialize message to WS_BLANK_MESSAGE
WsSetHeader             // serialize action header into header buffer
WsAddressMessage?       // optionally address message

// the following block is specific to sending a request
{
    generate a unique MessageID for request
    WsSetHeader         // set the message ID            
}

for each application defined header
{
    WsAddCustomHeader   // serialize application-defined headers into header buffer
}
WsWriteMessageStart     // write out the headers of the message
for each element of the body
{
    WsWriteBody         // serialize the element of the body
    WsFlushBody?        // optionally flush the body
}
WsWriteMessageEnd       // write the end of the message

WsReadMessageStart      // read all headers into header buffer

// the following is specific to receiving a reply
{
    WsGetHeader         // deserialize RelatesTo ID of reply
    verify request MessageID is equal to RelatesTo ID
}

for each standard header
{
    WsGetHeader         // deserialize standard header such as To or Action
}
for each application defined header
{
    WsGetCustomHeader   // deserialize application defined header
}
for each element of the body
{
    WsFillBody?         // optionally fill the body
    WsReadBody          // deserialize element of body
}
WsReadMessageEnd        // read end of message                
```

## <a name="request-reply-server"></a>Solicitação de resposta (servidor)

Para receber uma mensagem de solicitação no servidor, use a mesma sequência descrita na seção anterior sobre como receber mensagens.

Para enviar uma mensagem de resposta ou de falha, use a sequência a seguir.

``` syntax
WsCreateMessageForChannel
for each reply being sent
{
    WsSendReplyMessage | WsSendFaultMessageForError  // send reply or fault message
    WsResetMessage?     // reset if sending another message
}
WsFreeMessage
```

A função [**WsSendReplyMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage) pressupõe um único elemento no corpo e não permite streaming. Para evitar essas limitações, use a sequência a seguir. Isso é o mesmo que a sequência anterior para enviar uma mensagem, mas usa [**a \_ \_ mensagem de resposta WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_initialization) em vez de **WS \_ \_ Message em branco** ao inicializar.

``` syntax
// the following block is specific to sending a reply
{
    WsInitializeMessage // initialize message to WS_REPLY_MESSAGE
}
WsSetHeader             // serialize action header into header buffer                                
WsAddressMessage?       // optionally address message
for each application defined header
{
    WsAddCustomHeader   // serialize application-defined headers into header buffer
}
WsWriteMessageStart     // write out the headers of the message
for each element of the body
{
    WsWriteBody         // serialize the element of the body
    WsFlushBody?        // optionally flush the body
}
WsWriteMessageEnd       // write the end of the message
```

## <a name="message-exchange-patterns"></a>Padrões de troca de mensagens

O [**\_ \_ tipo de canal do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) determina o padrão de troca de mensagens possível para um determinado canal. O tipo com suporte, varia de acordo com a associação, da seguinte maneira:

-   [**WS \_ A \_ \_ Associação de canal http**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) dá suporte à [**\_ \_ \_ solicitação de tipo WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) no cliente e o tipo de **\_ canal WS \_ \_ responde** no servidor.
-   [**WS \_ A \_ \_ Associação de canal TCP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) dá suporte à [**\_ \_ \_ \_ sessão duplex do tipo WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) na **\_ \_ \_ \_ sessão duplex do tipo** de cliente e do WS Channel no servidor.
-   [**WS \_ A \_ \_ Associação de canal UDP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) dá suporte ao tipo de canal [**\_ \_ \_ duplex do WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) na entrada do tipo do cliente e do **WS \_ \_ \_ Channel** no servidor.
-   [**WS \_ A \_ \_ Associação de canal NAMEDPIPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) dá suporte ao tipo de canal [**\_ \_ \_ duplex do WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) na entrada do tipo do cliente e do **WS \_ \_ \_ Channel** no servidor.

## <a name="message-loops"></a>Loops de mensagens

Para cada padrão de troca de mensagens, há um "loop" específico que pode ser usado para enviar ou receber mensagens. O loop descreve a ordem legal das operações necessárias para enviar/receber várias mensagens. Os loops são descritos abaixo como produções gramaticais. O termo "End" é um recebimento onde o **WS- \_ \_ end** é retornado (consulte [valores de retorno dos serviços Web do Windows](windows-web-services-return-values.md)), indicando que não há mais mensagens disponíveis no canal. A produção paralela especifica que, para Parallel (x & y), a operação x pode ser feita simultaneamente com y.

Os seguintes loops são usados no cliente:

``` syntax
client-loop := client-request-loop | client-duplex-session-loop | client-duplex-loop
client-request-loop := open (send (receive | end))* close // WS_CHANNEL_TYPE_REQUEST
client-duplex-session-loop := open parallel(send* & receive*) parallel(send? & end*) close // WS_CHANNEL_TYPE_DUPLEX_SESSION
client-duplex-loop := open parallel(send & receive)* close // WS_CHANNEL_TYPE_DUPLEX
```

Os seguintes loops são usados no servidor:

``` syntax
server-loop: server-reply-loop | server-duplex-session-loop | server-duplex-loop
server-reply-loop := accept receive end* send? end* close // WS_CHANNEL_TYPE_REPLY
server-duplex-session-loop := accept parallel(send* & receive*) parallel(send* & end*) close // WS_CHANNEL_TYPE_DUPLEX_SESSION
server-input-loop := accept receive end* close // WS_CHANNEL_TYPE_INPUT
```

O uso [**da \_ \_ Associação de \_ \_ segurança de \_ mensagem de contexto de segurança do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) no servidor requer um recebimento bem-sucedido antes que o envio seja permitido mesmo com um canal do tipo [**WS \_ Channel \_ tipo \_ \_ sessão duplex**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type). Após o primeiro recebimento. o loop regular se aplica.

Observe que os canais do [**tipo \_ \_ \_ solicitação de tipo WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) e **\_ \_ \_ resposta de tipo de canal WS** podem ser usados para enviar e receber mensagens unidirecionais (bem como o padrão de solicitação-resposta padrão). Isso é feito fechando o canal de resposta sem enviar uma resposta. Nesse caso, não haverá nenhuma resposta recebida no canal de solicitação. O valor de retorno **WS- \_ \_ end** usando [**a \_ \_ Associação de \_ \_ segurança de \_ mensagem de contexto de segurança WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) no servidor requer um recebimento bem-sucedido antes que o envio seja permitido mesmo com um canal do tipo **WS \_ Channel \_ Type \_ duplex \_ Session**. Depois que o primeiro recebimento do loop regular é aplicado.

será retornado, indicando que nenhuma mensagem está disponível.

Os loops de cliente ou de servidor podem ser feitos em paralelo entre si usando várias instâncias de canal.

``` syntax
parallel-client: parallel(client-loop(channel1) & client-loop(channel2) & ...)
parallel-server: parallel(server-loop(channel1) & server-loop(channel2) & ...)
```

## <a name="message-filtering"></a>Filtragem de Mensagem

Um canal de servidor pode filtrar mensagens recebidas que não são destinadas ao aplicativo, como mensagens que estabelecem um [contexto de segurança](security-context.md). Nesse caso, o **WS- \_ \_ end** será retornado de [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart) e nenhuma mensagem de aplicativo estará disponível nesse canal. No entanto, isso não sinaliza que o cliente se destina a terminar a comunicação com o servidor. Mais mensagens podem estar disponíveis em outro canal. Consulte [**WsShutdownSessionChannel**](/windows/desktop/api/WebServices/nf-webservices-wsshutdownsessionchannel).

## <a name="cancellation"></a>Cancelamento

A função [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel) é usada para cancelar a e/s pendente para um canal. Essa API não aguardará a operação (ões) de e/s ser concluída. Consulte o diagrama de estado do [**\_ \_ estado do WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state) e a documentação do **WsAbortChannel** para obter mais informações.

A API [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener) é usada para cancelar a e/s pendente para um ouvinte. Essa API não aguardará a operação (ões) de e/s ser concluída. Anular um ouvinte fará com que as aceitações pendentes também sejam anuladas. Consulte o diagrama estado do estado do [**\_ ouvinte \_ do WS Listener**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) e **WsAbortListener** para obter mais informações.

## <a name="tcp"></a>TCP

A [**\_ Associação de \_ canal \_ TCP do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) oferece suporte a SOAP sobre TCP. A especificação de SOAP sobre TCP baseia-se no mecanismo de enquadramento do .NET.

Não há suporte para o compartilhamento de porta nesta versão. Cada ouvinte aberto deve usar um número de porta diferente.

## <a name="udp"></a>UDP

A [**\_ Associação de \_ canal \_ do WS UDP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) dá suporte a SOAP sobre UDP.

Há uma série de limitações com a associação de UDP:

-   Não há suporte para segurança.
-   As mensagens podem ser perdidas ou duplicadas.
-   Há suporte para apenas uma codificação: [**WS \_ Encoding \_ XML \_ UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding).
-   As mensagens são fundamentalmente limitadas a 64K e, muitas vezes, têm uma chance maior de serem perdidas se o tamanho exceder o MTU da rede.

## <a name="http"></a>HTTP

A [**\_ Associação de \_ canal \_ http do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) oferece suporte a SOAP sobre http.

Para controlar os cabeçalhos específicos de HTTP no cliente e no servidor, consulte [**\_ \_ \_ mapeamento de mensagem http do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping).

Para enviar e receber mensagens não SOAP no servidor, use [**WS \_ Encoding \_ RAW**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) para a [**codificação de \_ \_ propriedade \_ do WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).

## <a name="namedpipes"></a>NAMEDPIPES

A [**\_ Associação de \_ canal \_ WS NAMEDPIPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) dá suporte a SOAP em pipes nomeados, permitindo a comunicação com o serviço Windows Communication Foundation (WCF) usando NetNamedPipeBinding.

## <a name="correlating-requestreply-messages"></a>Correlacionando mensagens de solicitação/resposta

As mensagens de solicitação/resposta são correlacionadas de uma das duas maneiras:

-   A correlação é feita usando o canal como o mecanismo de correlação. Por exemplo, ao usar [**o \_ \_ \_ transporte de versão de endereçamento WS**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) e a [**\_ \_ \_ Associação de canal http WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) , a resposta para a mensagem de solicitação é correlacionada à solicitação pelo fato de que é o corpo da entidade da resposta http.
-   A correlação é feita usando os cabeçalhos MessageID e RelatesTo. Esse mecanismo é usado com o [**WS \_ Addressing \_ versão \_ 1 \_ 0**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) e **WS \_ Addressing \_ version \_ 0 \_ 9** (mesmo ao usar a [**\_ \_ \_ Associação de canal http do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)). Nesse caso, a mensagem de solicitação inclui o cabeçalho MessageID. A mensagem de resposta inclui um cabeçalho RelatesTo que tem o valor do cabeçalho MessageID da solicitação. O cabeçalho RelatesTo permite que o cliente correlacione uma resposta com uma solicitação enviada.

As seguintes APIs de camada de canal usam automaticamente os mecanismos de correlação apropriados com base na [**\_ \_ versão de endereçamento do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) do canal.

-   [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply)
-   [**WsSendReplyMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage)
-   [**WsSendFaultMessageForError**](/windows/desktop/api/WebServices/nf-webservices-wssendfaultmessageforerror)

Se essas APIs não forem usadas, os cabeçalhos poderão ser adicionados e acessados manualmente usando [**WsSetHeader**](/windows/desktop/api/WebServices/nf-webservices-wssetheader) ou [**WsGetHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetheader).

## <a name="custom-channels-and-listeners"></a>Canais e ouvintes personalizados

Se o conjunto predefinido de associações de canal não atender às necessidades do aplicativo, uma implementação de canal e ouvinte personalizado poderá ser definida especificando-se a [**\_ \_ \_ Associação de canal personalizado do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) ao criar o canal ou o ouvinte. A implementação real do canal/ouvinte é especificada como um conjunto de retornos de chamada por meio da [**Propriedade do WS \_ Channel \_ \_ \_ \_ retornos**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) de chamada de canal personalizado ou propriedades de [**retorno de \_ \_ \_ \_ \_ chamada de ouvinte personalizado da propriedade WS Listener**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) . Depois que um canal ou ouvinte personalizado é criado, o resultado é um objeto [WS \_ Channel](ws-channel.md) ou [WS \_ Listener](ws-listener.md) que pode ser usado com as APIs existentes.

Um canal e um ouvinte personalizado também podem ser usados com proxy de serviço e [host de serviço](service-host.md) especificando o valor de **\_ \_ \_ Associação de canal personalizado WS** na enumeração de [**\_ \_ associação do WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) e as propriedades de retorno de chamada de [**\_ \_ \_ \_ canal \_ personalizado de propriedade**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) do WS Channel e Propriedade do WS-up do [**\_ \_ \_ \_ ouvinte \_ personalizado**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) para a criação do proxy de serviço ou host de serviço.

## <a name="security"></a>Segurança

O canal permite limitar a quantidade de memória usada para vários aspectos das operações por meio de propriedades como:

-   [**WS \_ Propriedade do canal \_ \_ máximo \_ \_ \_ tamanho da mensagem em buffer**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ \_ \_ tamanho máximo da \_ \_ mensagem \_ em fluxo da Propriedade do canal**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ Propriedade de canal \_ \_ máximo \_ \_ \_ tamanho inicial em fluxo**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ Propriedade de canal \_ \_ máximo de cabeçalhos de \_ \_ solicitação HTTP \_ \_ \_ tamanho do buffer**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ \_ \_ tamanho máximo do \_ \_ dicionário \_ de sessão da propriedade de canal**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).

Essas propriedades têm valores padrão que são conservador e seguras para a maioria dos cenários. Os valores padrão e quaisquer modificações a eles devem ser cuidadosamente avaliados em relação a possíveis vetores de ataque que podem causar negação de serviço por um usuário remoto.

O canal permite definir valores de tempo limite para vários aspectos de operações por meio de propriedades como:

-   [**WS \_ \_ \_ \_ tempo limite de conexão da Propriedade do canal**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ \_ \_ \_ tempo limite de envio da Propriedade do canal**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ \_ \_ \_ \_ tempo limite de resposta de recebimento de Propriedade do canal**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ \_ \_ \_ tempo limite de recebimento da Propriedade do canal**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ \_ \_ \_ tempo limite de resolução da Propriedade do canal**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ \_ \_ \_ tempo limite de fechamento da Propriedade do canal**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).

Essas propriedades têm valores padrão que são conservador e seguras para a maioria dos cenários. Aumentar os valores de tempo limite aumenta a quantidade de tempo que uma parte remota pode manter um recurso local ativo, como memória, soquetes e threads fazendo e/s síncrona. Um aplicativo deve avaliar os valores padrão e ter cuidado ao aumentar um tempo limite, pois ele pode abrir vetores de ataque potenciais que podem causar negação de serviço de um computador remoto.

Algumas das outras opções de configuração e considerações de design de aplicativo que devem ser avaliadas cuidadosamente ao usar a API de canal do WWSAPI:

-   Ao usar a camada de canal/ouvinte, cabe ao aplicativo criar e aceitar canais no lado do servidor. Da mesma forma, cabe ao aplicativo criar e abrir canais no lado do cliente. Um aplicativo deve colocar um limite superior nessas operações porque cada canal consome memória e outros recursos limitados, como soquetes. Um aplicativo deve ser especialmente cuidadoso ao criar um canal em resposta a qualquer ação disparada por uma parte remota.
-   Cabe ao aplicativo gravar a lógica para criar canais e aceitá-los. Cada canal consome recursos limitados, como memória e soquetes. Um aplicativo deve ter um limite superior no número de canais que está disposto a aceitar, ou uma parte remota pode fazer muitas conexões, levando a OOM e, portanto, a negação de serviço. Ele também deve receber mensagens ativamente dessas conexões usando um tempo limite pequeno. Se nenhuma mensagem for recebida, a operação atingirá o tempo limite e a conexão deverá ser liberada.
-   Cabe a um aplicativo enviar uma resposta ou falha interpretando os cabeçalhos de resposta de SOAP ou FaultTo. A prática segura é respeitar apenas um cabeçalho ReplyTo ou FaultTo, que é "anônimo", o que significa que a conexão existente (TCP, HTTP) ou UDP (IP de origem) deve ser usada para enviar a resposta SOAP. Os aplicativos devem ter muito cuidado ao criar recursos (como um canal) para responder a um endereço diferente, a menos que a mensagem tenha sido assinada por uma entidade que possa falar pelo endereço ao qual a resposta está sendo enviada.
-   A validação feita na camada de canal não é substituída pela integridade dos dados obtida por meio de segurança. Um aplicativo deve contar com os recursos de segurança do WWSAPI para garantir que ele esteja se comunicando com uma entidade confiável e também deve contar com a segurança para garantir a integridade dos dados.

Da mesma forma, há opções de configuração de mensagem e considerações de design de aplicativo que devem ser avaliadas cuidadosamente ao usar a API de mensagem WWSAPI:

-   O tamanho do heap usado para armazenar os cabeçalhos de uma mensagem pode ser configurado usando a propriedade [**de \_ \_ Propriedades do \_ heap \_ da propriedade de mensagem WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) . Aumentar esse valor permite que mais memória seja consumida pelos cabeçalhos da mensagem, o que pode levar a OOM.
-   O usuário do objeto Message deve perceber que as APIs de acesso ao cabeçalho são O (n) em relação ao número de cabeçalhos na mensagem, pois eles verificam se há duplicatas. Os designs que exigem muitos cabeçalhos em uma mensagem podem levar ao uso excessivo da CPU.
-   O número máximo de cabeçalhos em uma mensagem pode ser configurado usando a propriedade [**WS \_ Message \_ propriedade \_ Max \_ Processed \_ Headers**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) . Há também um limite implícito com base no tamanho do heap da mensagem. O aumento de ambos os valores permite que mais cabeçalhos estejam presentes, o que aumenta o tempo necessário para encontrar um cabeçalho (ao usar as APIs de acesso ao cabeçalho).

 

 




