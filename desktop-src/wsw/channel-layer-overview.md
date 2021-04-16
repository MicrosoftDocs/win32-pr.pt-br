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
# <a name="channel-layer-overview"></a><span data-ttu-id="55b40-106">Visão geral da camada de canal</span><span class="sxs-lookup"><span data-stu-id="55b40-106">Channel Layer Overview</span></span>

<span data-ttu-id="55b40-107">A camada de canal fornece uma abstração do canal de transporte, bem como as mensagens enviadas no canal.</span><span class="sxs-lookup"><span data-stu-id="55b40-107">The Channel Layer provides an abstraction of the transport channel as well as messages sent out on the channel.</span></span> <span data-ttu-id="55b40-108">Ele também inclui funções para a serialização de tipos de dados C de e para estruturas SOAP.</span><span class="sxs-lookup"><span data-stu-id="55b40-108">It also includes functions for the serialization of C data types to and from SOAP structures.</span></span> <span data-ttu-id="55b40-109">A camada de canal permite o controle total de comunicações por meio de [mensagens](message.md) que consistem em dados enviados ou recebidos e que contêm corpos e cabeçalhos, e [canais](channel.md) que abstraem protocolos de troca de mensagens e fornecem propriedades para personalizar as configurações.</span><span class="sxs-lookup"><span data-stu-id="55b40-109">The Channel Layer enables full control of communications by means of [messages](message.md) consisting of data sent or received and containing bodies and headers, and [channels](channel.md) that abstract message exchange protocols and provide properties for customizing settings.</span></span>

## <a name="message"></a><span data-ttu-id="55b40-110">Mensagem</span><span class="sxs-lookup"><span data-stu-id="55b40-110">Message</span></span>

<span data-ttu-id="55b40-111">Uma [mensagem](message.md) é um objeto que encapsula dados de rede, especificamente, dados transmitidos ou recebidos em uma rede.</span><span class="sxs-lookup"><span data-stu-id="55b40-111">A [message](message.md) is an object that encapsulates network data — specifically, data that is transmitted or received over a network.</span></span> <span data-ttu-id="55b40-112">A estrutura da mensagem é definida pelo SOAP, com um conjunto discreto de cabeçalhos e um corpo da mensagem.</span><span class="sxs-lookup"><span data-stu-id="55b40-112">The message structure is defined by SOAP, with a discrete set of headers and a message body.</span></span> <span data-ttu-id="55b40-113">Os cabeçalhos são colocados em um buffer de memória e o corpo da mensagem é lido ou gravado usando uma API de fluxo.</span><span class="sxs-lookup"><span data-stu-id="55b40-113">The headers are placed in a memory buffer, and the message body is read or written using a stream API.</span></span>

![Diagrama mostrando o cabeçalho e o corpo de uma mensagem.](images/messageenvelope.png)

<span data-ttu-id="55b40-115">Embora o modelo de dados de uma mensagem seja sempre o modelo de dados XML, o formato de conexão real é flexível.</span><span class="sxs-lookup"><span data-stu-id="55b40-115">Although the data model of a message is always the XML data model, the actual wire format is flexible.</span></span> <span data-ttu-id="55b40-116">Antes que uma mensagem seja transmitida, ela é codificada usando uma codificação específica (como texto, binário ou MTOM).</span><span class="sxs-lookup"><span data-stu-id="55b40-116">Before a message is transmitted, it is encoded using a particular encoding (such as Text, Binary, or MTOM).</span></span> <span data-ttu-id="55b40-117">Consulte [**\_ codificação WS**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) para obter mais informações sobre codificações.</span><span class="sxs-lookup"><span data-stu-id="55b40-117">See [**WS\_ENCODING**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) for more information on encodings.</span></span>

![Diagrama mostrando vários formatos de codificação de mensagem.](images/messageandencodings.png)

## <a name="channel"></a><span data-ttu-id="55b40-119">Canal</span><span class="sxs-lookup"><span data-stu-id="55b40-119">Channel</span></span>

<span data-ttu-id="55b40-120">Um [canal](channel.md) é um objeto usado para enviar e receber mensagens em uma rede entre dois ou mais pontos de extremidade.</span><span class="sxs-lookup"><span data-stu-id="55b40-120">A [channel](channel.md) is an object used to send and receive messages on a network between two or more endpoints.</span></span>

<span data-ttu-id="55b40-121">Os canais têm dados associados que descrevem como [tratar](endpoint-address.md) a mensagem quando ela é enviada.</span><span class="sxs-lookup"><span data-stu-id="55b40-121">Channels have associated data that describes how to [address](endpoint-address.md) the message when it is sent.</span></span> <span data-ttu-id="55b40-122">O envio de uma mensagem em um canal é como colocá-lo em uma rampa — o canal inclui as informações em que a mensagem deve ir e como obtê-la.</span><span class="sxs-lookup"><span data-stu-id="55b40-122">Sending a message on a channel is like placing it in a chute — the channel includes the information where the message should go and how to get it there.</span></span>

![Diagrama mostrando canais para mensagens.](images/channelsaschute.png)

<span data-ttu-id="55b40-124">Os canais são categorizados em [**tipos de canal**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type).</span><span class="sxs-lookup"><span data-stu-id="55b40-124">Channels are categorized into [**channel types**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type).</span></span> <span data-ttu-id="55b40-125">Um tipo de canal especifica quais mensagens de direção podem fluir.</span><span class="sxs-lookup"><span data-stu-id="55b40-125">A channel type specifies which direction messages can flow.</span></span> <span data-ttu-id="55b40-126">O tipo de canal também identifica se o canal é de sessão ou de sessão.</span><span class="sxs-lookup"><span data-stu-id="55b40-126">The channel type also identifies whether the channel is sessionful, or sessionless.</span></span> <span data-ttu-id="55b40-127">Uma sessão é definida como uma maneira abstrata de correlacionar mensagens entre duas ou mais partes.</span><span class="sxs-lookup"><span data-stu-id="55b40-127">A session is defined as an abstract way of correlating messages between two or more parties.</span></span> <span data-ttu-id="55b40-128">Um exemplo de um canal de sessão é um canal TCP, que usa a conexão TCP como a implementação da sessão concreta.</span><span class="sxs-lookup"><span data-stu-id="55b40-128">An example of a sessionful channel is a TCP channel, which uses the TCP connection as the concrete session implementation.</span></span> <span data-ttu-id="55b40-129">Um exemplo de um canal sem sessão é UDP, que não tem um mecanismo de sessão subjacente.</span><span class="sxs-lookup"><span data-stu-id="55b40-129">An example of a sessionless channel is UDP, which does not have an underlying session mechanism.</span></span> <span data-ttu-id="55b40-130">Embora HTTP tenha conexões TCP subjacentes, esse fato não é exposto diretamente por essa API e, portanto, HTTP também é considerado um canal sem sessão.</span><span class="sxs-lookup"><span data-stu-id="55b40-130">Although HTTP does have underlying TCP connections, this fact is not directly exposed through this API and therefore HTTP is also considered a sessionless channel.</span></span>

![Diagrama mostrando tipos de canal de sessão e de sessão.](images/channeltypes.png)

<span data-ttu-id="55b40-132">Embora os tipos de canal descrevam a direção e as informações de sessão para um canal, eles não especificam como o canal é implementado.</span><span class="sxs-lookup"><span data-stu-id="55b40-132">Although channel types describe the direction and session information for a channel, they do not specify how the channel is implemented.</span></span> <span data-ttu-id="55b40-133">Qual protocolo o canal deve usar?</span><span class="sxs-lookup"><span data-stu-id="55b40-133">What protocol should the channel use?</span></span> <span data-ttu-id="55b40-134">Quão difícil o canal deve tentar entregar a mensagem?</span><span class="sxs-lookup"><span data-stu-id="55b40-134">How hard should the channel try to deliver the message?</span></span> <span data-ttu-id="55b40-135">Que tipo de segurança é usado?</span><span class="sxs-lookup"><span data-stu-id="55b40-135">What kind of security is used?</span></span> <span data-ttu-id="55b40-136">Ele é singlecast ou multicast?</span><span class="sxs-lookup"><span data-stu-id="55b40-136">Is it singlecast or multicast?</span></span> <span data-ttu-id="55b40-137">Essas configurações são chamadas de "Associação" do canal.</span><span class="sxs-lookup"><span data-stu-id="55b40-137">These settings are referred to as the "binding" of the channel.</span></span> <span data-ttu-id="55b40-138">A associação consiste no seguinte:</span><span class="sxs-lookup"><span data-stu-id="55b40-138">The binding consists of the following:</span></span>

-   <span data-ttu-id="55b40-139">Uma [**\_ \_ associação do WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), que identifica o protocolo de transferência a ser usado (TCP, UDP, http, NAMEDPIPE).</span><span class="sxs-lookup"><span data-stu-id="55b40-139">A [**WS\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), which identifies the transfer protocol to use (TCP, UDP, HTTP, NAMEDPIPE).</span></span>
-   <span data-ttu-id="55b40-140">Uma [**\_ \_ Descrição de segurança do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), que especifica como proteger o canal.</span><span class="sxs-lookup"><span data-stu-id="55b40-140">A [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), which specifies how to secure the channel.</span></span>
-   <span data-ttu-id="55b40-141">Um conjunto [**de \_ \_ Propriedades s do WS Channel**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property), que especificam configurações opcionais adicionais.</span><span class="sxs-lookup"><span data-stu-id="55b40-141">A set [**WS\_CHANNEL\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)s, which specify additional optional settings.</span></span> <span data-ttu-id="55b40-142">Consulte [**\_ ID de \_ propriedade \_ do WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) para obter a lista de propriedades.</span><span class="sxs-lookup"><span data-stu-id="55b40-142">See [**WS\_CHANNEL\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) for the list of properties.</span></span>

![Diagrama mostrando uma lista de propriedades de canal.](images/channelsandbindings.png)

## <a name="listener"></a><span data-ttu-id="55b40-144">Ouvinte</span><span class="sxs-lookup"><span data-stu-id="55b40-144">Listener</span></span>

<span data-ttu-id="55b40-145">Para começar a se comunicar, o cliente cria um objeto de canal.</span><span class="sxs-lookup"><span data-stu-id="55b40-145">To start communicating, the client creates a Channel object.</span></span> <span data-ttu-id="55b40-146">Mas como o serviço obtém seu objeto de canal?</span><span class="sxs-lookup"><span data-stu-id="55b40-146">But how does the service get its Channel object?</span></span> <span data-ttu-id="55b40-147">Ele faz isso criando um [ouvinte](listener.md).</span><span class="sxs-lookup"><span data-stu-id="55b40-147">It does so by creating a [Listener](listener.md).</span></span> <span data-ttu-id="55b40-148">A criação de um ouvinte requer as mesmas informações de ligação necessárias para criar um canal.</span><span class="sxs-lookup"><span data-stu-id="55b40-148">Creating a listener requires the same binding information that is necessary to create a channel.</span></span> <span data-ttu-id="55b40-149">Depois que um ouvinte tiver sido criado, o aplicativo poderá aceitar canais do ouvinte.</span><span class="sxs-lookup"><span data-stu-id="55b40-149">Once a Listener has been created, the application can Accept Channels from the Listener.</span></span> <span data-ttu-id="55b40-150">Como o aplicativo pode ficar atrás na aceitação de canais, os ouvintes normalmente mantêm uma fila de canais que estão prontos para aceitar (até certa cota).</span><span class="sxs-lookup"><span data-stu-id="55b40-150">Since the application may fall behind in accepting channels, listeners typically keep a queue of channels that are ready to accept (up to some quota).</span></span>

![Diagrama mostrando canais na fila de ouvintes.](images/channelaccept.png)

## <a name="initiating-communication-client"></a><span data-ttu-id="55b40-152">Iniciando comunicação (cliente)</span><span class="sxs-lookup"><span data-stu-id="55b40-152">Initiating Communication (client)</span></span>

<span data-ttu-id="55b40-153">Para iniciar a comunicação no cliente, use a sequência a seguir.</span><span class="sxs-lookup"><span data-stu-id="55b40-153">To initiate communication on the client, use the following sequence.</span></span>

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

## <a name="accepting-communication-server"></a><span data-ttu-id="55b40-154">Aceitando comunicação (servidor)</span><span class="sxs-lookup"><span data-stu-id="55b40-154">Accepting Communication (server)</span></span>

<span data-ttu-id="55b40-155">Para aceitar as comunicações de entrada no servidor, use a sequência a seguir.</span><span class="sxs-lookup"><span data-stu-id="55b40-155">To accept incoming communications on the server, use the following sequence.</span></span>

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

## <a name="sending-messages-client-or-server"></a><span data-ttu-id="55b40-156">Enviando mensagens (cliente ou servidor)</span><span class="sxs-lookup"><span data-stu-id="55b40-156">Sending Messages (client or server)</span></span>

<span data-ttu-id="55b40-157">Para enviar mensagens, use a sequência a seguir.</span><span class="sxs-lookup"><span data-stu-id="55b40-157">To send messages, use the following sequence.</span></span>

``` syntax
WsCreateMessageForChannel
for each message being sent
{
    WsSendMessage       // send message
    WsResetMessage?     // reset if sending another message
}
WsFreeMessage
```

<span data-ttu-id="55b40-158">A função [**WsSendMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendmessage) não permite streaming e pressupõe que o corpo contém apenas um elemento.</span><span class="sxs-lookup"><span data-stu-id="55b40-158">The [**WsSendMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendmessage) function does not allow for streaming, and assumes that the body contains only one element.</span></span> <span data-ttu-id="55b40-159">Para evitar essas restrições, use a seguinte sequência em vez de **WsSendMessage**.</span><span class="sxs-lookup"><span data-stu-id="55b40-159">To avoid these constraints, use the following sequence instead of **WsSendMessage**.</span></span>

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

<span data-ttu-id="55b40-160">A função [**WsWriteBody**](/windows/desktop/api/WebServices/nf-webservices-wswritebody) usa a serialização para gravar os elementos do corpo.</span><span class="sxs-lookup"><span data-stu-id="55b40-160">The [**WsWriteBody**](/windows/desktop/api/WebServices/nf-webservices-wswritebody) function uses serialization to write the body elements.</span></span> <span data-ttu-id="55b40-161">Para gravar os dados diretamente no gravador de XML, use a seguinte sequência em vez de **WsWriteBody**.</span><span class="sxs-lookup"><span data-stu-id="55b40-161">To write the data directly to the XML Writer, use the following sequence instead of **WsWriteBody**.</span></span>

``` syntax
WS_MESSAGE_PROPERTY_BODY_WRITER     // get the writer used to write the body
WsWriteStartElement
// use the writer functions to write the body
WsWriteEndElement
// optionally flush the body
WsFlushBody?        
```

<span data-ttu-id="55b40-162">A função [**WsAddCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsaddcustomheader) usa a serialização para definir os cabeçalhos para o buffer de cabeçalho da mensagem.</span><span class="sxs-lookup"><span data-stu-id="55b40-162">The [**WsAddCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsaddcustomheader) function uses serialization to set the headers to the header buffer of the message.</span></span> <span data-ttu-id="55b40-163">Para usar o gravador de XML para gravar um cabeçalho, use a seguinte sequência em vez de **WsAddCustomHeader**.</span><span class="sxs-lookup"><span data-stu-id="55b40-163">To use the XML Writer to write a header, use the following sequence instead of **WsAddCustomHeader**.</span></span>

``` syntax
WS_MESSAGE_PROPERTY_HEADER_BUFFER   // get the header buffer 
WsCreateWriter                      // create an xml writer
WsSetOutputToBuffer                 // specify output of writer should go to buffer
WsMoveWriter*                       // move to inside envelope header element
WsWriteStartElement                 // write application header start element
// use the writer functions to write the header 
WsWriteEndElement                   // write appilcation header end element
```

## <a name="receiving-messages-client-or-server"></a><span data-ttu-id="55b40-164">Recebendo mensagens (cliente ou servidor)</span><span class="sxs-lookup"><span data-stu-id="55b40-164">Receiving Messages (client or server)</span></span>

<span data-ttu-id="55b40-165">Para receber mensagens, use a sequência a seguir.</span><span class="sxs-lookup"><span data-stu-id="55b40-165">To receive messages, use the following sequence.</span></span>

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

<span data-ttu-id="55b40-166">A função [**WsReceiveMessage**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage) não permite streaming e pressupõe que o corpo contenha apenas um elemento e que o tipo da mensagem (ação e esquema do corpo) seja conhecido com antecedência.</span><span class="sxs-lookup"><span data-stu-id="55b40-166">The [**WsReceiveMessage**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage) function does not allow for streaming, and assumes that the body contains only one element, and that the type of the message (action and schema of the body) is known up front.</span></span> <span data-ttu-id="55b40-167">Para evitar essas restrições, use a seguinte sequência em vez de **WsReceiveMessage**.</span><span class="sxs-lookup"><span data-stu-id="55b40-167">To avoid these constraints, use the following sequence instead of **WsReceiveMessage**.</span></span>

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

<span data-ttu-id="55b40-168">A função [**WsReadBody**](/windows/desktop/api/WebServices/nf-webservices-wsreadbody) usa a serialização para ler os elementos do corpo.</span><span class="sxs-lookup"><span data-stu-id="55b40-168">The [**WsReadBody**](/windows/desktop/api/WebServices/nf-webservices-wsreadbody) function uses serialization to read the body elements.</span></span> <span data-ttu-id="55b40-169">Para ler os dados diretamente do [leitor de XML](xml-reader.md), use a seguinte sequência em vez de **WsReadBody**.</span><span class="sxs-lookup"><span data-stu-id="55b40-169">To read the data directly from the [XML Reader](xml-reader.md), use the following sequence instead of **WsReadBody**.</span></span>

``` syntax
WS_MESSAGE_PROPERTY_BODY_READER     // get the reader used to read the body
WsFillBody?                         // optionally fill the body
WsReadToStartElement                // read up to the body element
WsReadStartElement                  // consume the start of the body element
// use the read functions to read the contents of the body element
WsReadEndElement                    // consume the end of the body element
```

<span data-ttu-id="55b40-170">As funções [**WsGetCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetcustomheader) usam a serialização para obter os cabeçalhos do buffer de cabeçalho da mensagem.</span><span class="sxs-lookup"><span data-stu-id="55b40-170">The [**WsGetCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetcustomheader) functions use serialization to get the headers from the header buffer of the message.</span></span> <span data-ttu-id="55b40-171">Para usar o [leitor de XML](xml-reader.md) para ler um cabeçalho, use a seguinte sequência em vez de **WsGetCustomHeader**.</span><span class="sxs-lookup"><span data-stu-id="55b40-171">To use the [XML Reader](xml-reader.md) to read a header, use the following sequence instead of **WsGetCustomHeader**.</span></span>

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

## <a name="request-reply-client"></a><span data-ttu-id="55b40-172">Solicitação de resposta (cliente)</span><span class="sxs-lookup"><span data-stu-id="55b40-172">Request Reply (client)</span></span>

<span data-ttu-id="55b40-173">A execução de uma solicitação-resposta no cliente pode ser feita com a sequência a seguir.</span><span class="sxs-lookup"><span data-stu-id="55b40-173">Performing a request-reply on the client can be done with the following sequence.</span></span>

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

<span data-ttu-id="55b40-174">A função [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply) pressupõe um único elemento para o corpo da solicitação e as mensagens de resposta, e que o tipo da mensagem (ação e esquema do corpo) é conhecido com antecedência.</span><span class="sxs-lookup"><span data-stu-id="55b40-174">The [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply) function assumes a single element for the body of the request and reply messages, and that the type of the message (action and schema of the body) are known up front.</span></span> <span data-ttu-id="55b40-175">Para evitar essas limitações, a solicitação e a mensagem de resposta podem ser enviadas manualmente, conforme mostrado na sequência a seguir.</span><span class="sxs-lookup"><span data-stu-id="55b40-175">To avoid these limitations, the request and reply message can be sent manually, as shown in the following sequence.</span></span> <span data-ttu-id="55b40-176">Essa sequência corresponde à sequência anterior para enviar e receber uma mensagem, exceto quando indicado.</span><span class="sxs-lookup"><span data-stu-id="55b40-176">This sequence matches the earlier sequence for sending and receiving a message, except where noted.</span></span>

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

## <a name="request-reply-server"></a><span data-ttu-id="55b40-177">Solicitação de resposta (servidor)</span><span class="sxs-lookup"><span data-stu-id="55b40-177">Request Reply (server)</span></span>

<span data-ttu-id="55b40-178">Para receber uma mensagem de solicitação no servidor, use a mesma sequência descrita na seção anterior sobre como receber mensagens.</span><span class="sxs-lookup"><span data-stu-id="55b40-178">To receive a request message on the server, use the same sequence as outlined in the previous section on receiving messages.</span></span>

<span data-ttu-id="55b40-179">Para enviar uma mensagem de resposta ou de falha, use a sequência a seguir.</span><span class="sxs-lookup"><span data-stu-id="55b40-179">To send a reply or fault message, use the following sequence.</span></span>

``` syntax
WsCreateMessageForChannel
for each reply being sent
{
    WsSendReplyMessage | WsSendFaultMessageForError  // send reply or fault message
    WsResetMessage?     // reset if sending another message
}
WsFreeMessage
```

<span data-ttu-id="55b40-180">A função [**WsSendReplyMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage) pressupõe um único elemento no corpo e não permite streaming.</span><span class="sxs-lookup"><span data-stu-id="55b40-180">The [**WsSendReplyMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage) function assumes a single element in the body and does not allow for streaming.</span></span> <span data-ttu-id="55b40-181">Para evitar essas limitações, use a sequência a seguir.</span><span class="sxs-lookup"><span data-stu-id="55b40-181">To avoid these limitations, use the following sequence.</span></span> <span data-ttu-id="55b40-182">Isso é o mesmo que a sequência anterior para enviar uma mensagem, mas usa [**a \_ \_ mensagem de resposta WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_initialization) em vez de **WS \_ \_ Message em branco** ao inicializar.</span><span class="sxs-lookup"><span data-stu-id="55b40-182">This is the same as the earlier sequence for sending a message, but uses [**WS\_REPLY\_MESSAGE**](/windows/desktop/api/WebServices/ne-webservices-ws_message_initialization) instead of **WS\_BLANK\_MESSAGE** when initializing.</span></span>

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

## <a name="message-exchange-patterns"></a><span data-ttu-id="55b40-183">Padrões de troca de mensagens</span><span class="sxs-lookup"><span data-stu-id="55b40-183">Message Exchange Patterns</span></span>

<span data-ttu-id="55b40-184">O [**\_ \_ tipo de canal do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) determina o padrão de troca de mensagens possível para um determinado canal.</span><span class="sxs-lookup"><span data-stu-id="55b40-184">The [**WS\_CHANNEL\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) dictates the message exchange pattern possible for a given channel.</span></span> <span data-ttu-id="55b40-185">O tipo com suporte, varia de acordo com a associação, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="55b40-185">The type supported, varies according to the binding, as follows:</span></span>

-   <span data-ttu-id="55b40-186">[**WS \_ A \_ \_ Associação de canal http**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) dá suporte à [**\_ \_ \_ solicitação de tipo WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) no cliente e o tipo de **\_ canal WS \_ \_ responde** no servidor.</span><span class="sxs-lookup"><span data-stu-id="55b40-186">[**WS\_HTTP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports [**WS\_CHANNEL\_TYPE\_REQUEST**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) on the client and **WS\_CHANNEL\_TYPE\_REPLY** on the server.</span></span>
-   <span data-ttu-id="55b40-187">[**WS \_ A \_ \_ Associação de canal TCP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) dá suporte à [**\_ \_ \_ \_ sessão duplex do tipo WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) na **\_ \_ \_ \_ sessão duplex do tipo** de cliente e do WS Channel no servidor.</span><span class="sxs-lookup"><span data-stu-id="55b40-187">[**WS\_TCP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports [**WS\_CHANNEL\_TYPE\_DUPLEX\_SESSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) on the client and **WS\_CHANNEL\_TYPE\_DUPLEX\_SESSION** on the server.</span></span>
-   <span data-ttu-id="55b40-188">[**WS \_ A \_ \_ Associação de canal UDP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) dá suporte ao tipo de canal [**\_ \_ \_ duplex do WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) na entrada do tipo do cliente e do **WS \_ \_ \_ Channel** no servidor.</span><span class="sxs-lookup"><span data-stu-id="55b40-188">[**WS\_UDP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports [**WS\_CHANNEL\_TYPE\_DUPLEX**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) on the client and **WS\_CHANNEL\_TYPE\_INPUT** on the server.</span></span>
-   <span data-ttu-id="55b40-189">[**WS \_ A \_ \_ Associação de canal NAMEDPIPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) dá suporte ao tipo de canal [**\_ \_ \_ duplex do WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) na entrada do tipo do cliente e do **WS \_ \_ \_ Channel** no servidor.</span><span class="sxs-lookup"><span data-stu-id="55b40-189">[**WS\_NAMEDPIPE\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports [**WS\_CHANNEL\_TYPE\_DUPLEX**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) on the client and **WS\_CHANNEL\_TYPE\_INPUT** on the server.</span></span>

## <a name="message-loops"></a><span data-ttu-id="55b40-190">Loops de mensagens</span><span class="sxs-lookup"><span data-stu-id="55b40-190">Message Loops</span></span>

<span data-ttu-id="55b40-191">Para cada padrão de troca de mensagens, há um "loop" específico que pode ser usado para enviar ou receber mensagens.</span><span class="sxs-lookup"><span data-stu-id="55b40-191">For each message exchange pattern, there is a specific "loop" that can be used to send or receive messages.</span></span> <span data-ttu-id="55b40-192">O loop descreve a ordem legal das operações necessárias para enviar/receber várias mensagens.</span><span class="sxs-lookup"><span data-stu-id="55b40-192">The loop describes the legal order of operations necessary to send/receive multiple messages.</span></span> <span data-ttu-id="55b40-193">Os loops são descritos abaixo como produções gramaticais.</span><span class="sxs-lookup"><span data-stu-id="55b40-193">The loops are describes below as grammar productions.</span></span> <span data-ttu-id="55b40-194">O termo "End" é um recebimento onde o **WS- \_ \_ end** é retornado (consulte [valores de retorno dos serviços Web do Windows](windows-web-services-return-values.md)), indicando que não há mais mensagens disponíveis no canal.</span><span class="sxs-lookup"><span data-stu-id="55b40-194">The 'end' term is a receive where **WS\_S\_END** is returned (See [Windows Web Services Return Values](windows-web-services-return-values.md)), indicating no more messages are available on the channel.</span></span> <span data-ttu-id="55b40-195">A produção paralela especifica que, para Parallel (x & y), a operação x pode ser feita simultaneamente com y.</span><span class="sxs-lookup"><span data-stu-id="55b40-195">The parallel production specifies that for parallel(x & y) that operation x may be done concurrently with y.</span></span>

<span data-ttu-id="55b40-196">Os seguintes loops são usados no cliente:</span><span class="sxs-lookup"><span data-stu-id="55b40-196">The following loops are used on the client:</span></span>

``` syntax
client-loop := client-request-loop | client-duplex-session-loop | client-duplex-loop
client-request-loop := open (send (receive | end))* close // WS_CHANNEL_TYPE_REQUEST
client-duplex-session-loop := open parallel(send* & receive*) parallel(send? & end*) close // WS_CHANNEL_TYPE_DUPLEX_SESSION
client-duplex-loop := open parallel(send & receive)* close // WS_CHANNEL_TYPE_DUPLEX
```

<span data-ttu-id="55b40-197">Os seguintes loops são usados no servidor:</span><span class="sxs-lookup"><span data-stu-id="55b40-197">The following loops are used on the server:</span></span>

``` syntax
server-loop: server-reply-loop | server-duplex-session-loop | server-duplex-loop
server-reply-loop := accept receive end* send? end* close // WS_CHANNEL_TYPE_REPLY
server-duplex-session-loop := accept parallel(send* & receive*) parallel(send* & end*) close // WS_CHANNEL_TYPE_DUPLEX_SESSION
server-input-loop := accept receive end* close // WS_CHANNEL_TYPE_INPUT
```

<span data-ttu-id="55b40-198">O uso [**da \_ \_ Associação de \_ \_ segurança de \_ mensagem de contexto de segurança do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) no servidor requer um recebimento bem-sucedido antes que o envio seja permitido mesmo com um canal do tipo [**WS \_ Channel \_ tipo \_ \_ sessão duplex**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type).</span><span class="sxs-lookup"><span data-stu-id="55b40-198">Using the [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) on the server requires a successful receive before sending is allowed even with a channel of type [**WS\_CHANNEL\_TYPE\_DUPLEX\_SESSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type).</span></span> <span data-ttu-id="55b40-199">Após o primeiro recebimento.</span><span class="sxs-lookup"><span data-stu-id="55b40-199">After the first receive.</span></span> <span data-ttu-id="55b40-200">o loop regular se aplica.</span><span class="sxs-lookup"><span data-stu-id="55b40-200">the regular loop applies.</span></span>

<span data-ttu-id="55b40-201">Observe que os canais do [**tipo \_ \_ \_ solicitação de tipo WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) e **\_ \_ \_ resposta de tipo de canal WS** podem ser usados para enviar e receber mensagens unidirecionais (bem como o padrão de solicitação-resposta padrão).</span><span class="sxs-lookup"><span data-stu-id="55b40-201">Note that channels of type [**WS\_CHANNEL\_TYPE\_REQUEST**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) and **WS\_CHANNEL\_TYPE\_REPLY** can be used to send and receive one-way messages (as well as the standard request-reply pattern).</span></span> <span data-ttu-id="55b40-202">Isso é feito fechando o canal de resposta sem enviar uma resposta.</span><span class="sxs-lookup"><span data-stu-id="55b40-202">This is accomplished by closing the reply channel without sending a reply.</span></span> <span data-ttu-id="55b40-203">Nesse caso, não haverá nenhuma resposta recebida no canal de solicitação.</span><span class="sxs-lookup"><span data-stu-id="55b40-203">In this case, there will be no reply received on the request channel.</span></span> <span data-ttu-id="55b40-204">O valor de retorno **WS- \_ \_ end** usando [**a \_ \_ Associação de \_ \_ segurança de \_ mensagem de contexto de segurança WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) no servidor requer um recebimento bem-sucedido antes que o envio seja permitido mesmo com um canal do tipo **WS \_ Channel \_ Type \_ duplex \_ Session**.</span><span class="sxs-lookup"><span data-stu-id="55b40-204">The return value **WS\_S\_END** Using the [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) on the server requires a successful receive before sending is allowed even with a channel of type **WS\_CHANNEL\_TYPE\_DUPLEX\_SESSION**.</span></span> <span data-ttu-id="55b40-205">Depois que o primeiro recebimento do loop regular é aplicado.</span><span class="sxs-lookup"><span data-stu-id="55b40-205">After the first receive the regular loop applies.</span></span>

<span data-ttu-id="55b40-206">será retornado, indicando que nenhuma mensagem está disponível.</span><span class="sxs-lookup"><span data-stu-id="55b40-206">will be returned, indicating no message available.</span></span>

<span data-ttu-id="55b40-207">Os loops de cliente ou de servidor podem ser feitos em paralelo entre si usando várias instâncias de canal.</span><span class="sxs-lookup"><span data-stu-id="55b40-207">Client or server loops may be done in parallel with each other by using multiple channel instances.</span></span>

``` syntax
parallel-client: parallel(client-loop(channel1) & client-loop(channel2) & ...)
parallel-server: parallel(server-loop(channel1) & server-loop(channel2) & ...)
```

## <a name="message-filtering"></a><span data-ttu-id="55b40-208">Filtragem de Mensagem</span><span class="sxs-lookup"><span data-stu-id="55b40-208">Message Filtering</span></span>

<span data-ttu-id="55b40-209">Um canal de servidor pode filtrar mensagens recebidas que não são destinadas ao aplicativo, como mensagens que estabelecem um [contexto de segurança](security-context.md).</span><span class="sxs-lookup"><span data-stu-id="55b40-209">A server channel may filter received messages that are not intended for the application, such as messages that establish a [security context](security-context.md).</span></span> <span data-ttu-id="55b40-210">Nesse caso, o **WS- \_ \_ end** será retornado de [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart) e nenhuma mensagem de aplicativo estará disponível nesse canal.</span><span class="sxs-lookup"><span data-stu-id="55b40-210">In that case **WS\_S\_END** will be returned from [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart) and no application messages will be available on that channel.</span></span> <span data-ttu-id="55b40-211">No entanto, isso não sinaliza que o cliente se destina a terminar a comunicação com o servidor.</span><span class="sxs-lookup"><span data-stu-id="55b40-211">However, this does not signal that the client intended to end communication with the server.</span></span> <span data-ttu-id="55b40-212">Mais mensagens podem estar disponíveis em outro canal.</span><span class="sxs-lookup"><span data-stu-id="55b40-212">More messages may be available on another channel.</span></span> <span data-ttu-id="55b40-213">Consulte [**WsShutdownSessionChannel**](/windows/desktop/api/WebServices/nf-webservices-wsshutdownsessionchannel).</span><span class="sxs-lookup"><span data-stu-id="55b40-213">See [**WsShutdownSessionChannel**](/windows/desktop/api/WebServices/nf-webservices-wsshutdownsessionchannel).</span></span>

## <a name="cancellation"></a><span data-ttu-id="55b40-214">Cancelamento</span><span class="sxs-lookup"><span data-stu-id="55b40-214">Cancellation</span></span>

<span data-ttu-id="55b40-215">A função [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel) é usada para cancelar a e/s pendente para um canal.</span><span class="sxs-lookup"><span data-stu-id="55b40-215">The [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel) function is used to cancel pending IO for a channel.</span></span> <span data-ttu-id="55b40-216">Essa API não aguardará a operação (ões) de e/s ser concluída.</span><span class="sxs-lookup"><span data-stu-id="55b40-216">This API will not wait for the IO operation(s) to complete.</span></span> <span data-ttu-id="55b40-217">Consulte o diagrama de estado do [**\_ \_ estado do WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state) e a documentação do **WsAbortChannel** para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="55b40-217">See the [**WS\_CHANNEL\_STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state) state diagram and documentation for **WsAbortChannel** for more information.</span></span>

<span data-ttu-id="55b40-218">A API [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener) é usada para cancelar a e/s pendente para um ouvinte.</span><span class="sxs-lookup"><span data-stu-id="55b40-218">The [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener) API is used to cancel pending IO for a listener.</span></span> <span data-ttu-id="55b40-219">Essa API não aguardará a operação (ões) de e/s ser concluída.</span><span class="sxs-lookup"><span data-stu-id="55b40-219">This API will not wait for the IO operation(s) to complete.</span></span> <span data-ttu-id="55b40-220">Anular um ouvinte fará com que as aceitações pendentes também sejam anuladas.</span><span class="sxs-lookup"><span data-stu-id="55b40-220">Aborting a listener will cause any pending accepts to be aborted as well.</span></span> <span data-ttu-id="55b40-221">Consulte o diagrama estado do estado do [**\_ ouvinte \_ do WS Listener**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) e **WsAbortListener** para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="55b40-221">See the [**WS\_LISTENER\_STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) state diagram and **WsAbortListener** for more information.</span></span>

## <a name="tcp"></a><span data-ttu-id="55b40-222">TCP</span><span class="sxs-lookup"><span data-stu-id="55b40-222">TCP</span></span>

<span data-ttu-id="55b40-223">A [**\_ Associação de \_ canal \_ TCP do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) oferece suporte a SOAP sobre TCP.</span><span class="sxs-lookup"><span data-stu-id="55b40-223">The [**WS\_TCP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports SOAP over TCP.</span></span> <span data-ttu-id="55b40-224">A especificação de SOAP sobre TCP baseia-se no mecanismo de enquadramento do .NET.</span><span class="sxs-lookup"><span data-stu-id="55b40-224">The SOAP over TCP specification builds upon the .NET Framing mechanism.</span></span>

<span data-ttu-id="55b40-225">Não há suporte para o compartilhamento de porta nesta versão.</span><span class="sxs-lookup"><span data-stu-id="55b40-225">Port sharing is not supported in this version.</span></span> <span data-ttu-id="55b40-226">Cada ouvinte aberto deve usar um número de porta diferente.</span><span class="sxs-lookup"><span data-stu-id="55b40-226">Each listener that is opened must use a different port number.</span></span>

## <a name="udp"></a><span data-ttu-id="55b40-227">UDP</span><span class="sxs-lookup"><span data-stu-id="55b40-227">UDP</span></span>

<span data-ttu-id="55b40-228">A [**\_ Associação de \_ canal \_ do WS UDP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) dá suporte a SOAP sobre UDP.</span><span class="sxs-lookup"><span data-stu-id="55b40-228">The [**WS\_UDP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports SOAP over UDP.</span></span>

<span data-ttu-id="55b40-229">Há uma série de limitações com a associação de UDP:</span><span class="sxs-lookup"><span data-stu-id="55b40-229">There are a number of limitations with the UDP binding:</span></span>

-   <span data-ttu-id="55b40-230">Não há suporte para segurança.</span><span class="sxs-lookup"><span data-stu-id="55b40-230">There is no support for security.</span></span>
-   <span data-ttu-id="55b40-231">As mensagens podem ser perdidas ou duplicadas.</span><span class="sxs-lookup"><span data-stu-id="55b40-231">Messages may be lost or duplicated.</span></span>
-   <span data-ttu-id="55b40-232">Há suporte para apenas uma codificação: [**WS \_ Encoding \_ XML \_ UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding).</span><span class="sxs-lookup"><span data-stu-id="55b40-232">Only one encoding is supported: [**WS\_ENCODING\_XML\_UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding).</span></span>
-   <span data-ttu-id="55b40-233">As mensagens são fundamentalmente limitadas a 64K e, muitas vezes, têm uma chance maior de serem perdidas se o tamanho exceder o MTU da rede.</span><span class="sxs-lookup"><span data-stu-id="55b40-233">Messages are fundamentally limited to 64k, and frequently have a greater chance being lost if the size exceeds the MTU of the network.</span></span>

## <a name="http"></a><span data-ttu-id="55b40-234">HTTP</span><span class="sxs-lookup"><span data-stu-id="55b40-234">HTTP</span></span>

<span data-ttu-id="55b40-235">A [**\_ Associação de \_ canal \_ http do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) oferece suporte a SOAP sobre http.</span><span class="sxs-lookup"><span data-stu-id="55b40-235">The [**WS\_HTTP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports SOAP over HTTP.</span></span>

<span data-ttu-id="55b40-236">Para controlar os cabeçalhos específicos de HTTP no cliente e no servidor, consulte [**\_ \_ \_ mapeamento de mensagem http do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping).</span><span class="sxs-lookup"><span data-stu-id="55b40-236">To control HTTP specific headers on the client and server, see [**WS\_HTTP\_MESSAGE\_MAPPING**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping).</span></span>

<span data-ttu-id="55b40-237">Para enviar e receber mensagens não SOAP no servidor, use [**WS \_ Encoding \_ RAW**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) para a [**codificação de \_ \_ propriedade \_ do WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span><span class="sxs-lookup"><span data-stu-id="55b40-237">To send and receive non-SOAP messages on the server, use [**WS\_ENCODING\_RAW**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) for [**WS\_CHANNEL\_PROPERTY\_ENCODING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span></span>

## <a name="namedpipes"></a><span data-ttu-id="55b40-238">NAMEDPIPES</span><span class="sxs-lookup"><span data-stu-id="55b40-238">NAMEDPIPES</span></span>

<span data-ttu-id="55b40-239">A [**\_ Associação de \_ canal \_ WS NAMEDPIPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) dá suporte a SOAP em pipes nomeados, permitindo a comunicação com o serviço Windows Communication Foundation (WCF) usando NetNamedPipeBinding.</span><span class="sxs-lookup"><span data-stu-id="55b40-239">The [**WS\_NAMEDPIPE\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports SOAP over named pipes, allowing communication with the Windows Communication Foundation (WCF) service using NetNamedPipeBinding.</span></span>

## <a name="correlating-requestreply-messages"></a><span data-ttu-id="55b40-240">Correlacionando mensagens de solicitação/resposta</span><span class="sxs-lookup"><span data-stu-id="55b40-240">Correlating Request/Reply Messages</span></span>

<span data-ttu-id="55b40-241">As mensagens de solicitação/resposta são correlacionadas de uma das duas maneiras:</span><span class="sxs-lookup"><span data-stu-id="55b40-241">Request/Reply messages are correlated in one of two ways:</span></span>

-   <span data-ttu-id="55b40-242">A correlação é feita usando o canal como o mecanismo de correlação.</span><span class="sxs-lookup"><span data-stu-id="55b40-242">Correlation is done using the channel as the correlation mechanism.</span></span> <span data-ttu-id="55b40-243">Por exemplo, ao usar [**o \_ \_ \_ transporte de versão de endereçamento WS**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) e a [**\_ \_ \_ Associação de canal http WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) , a resposta para a mensagem de solicitação é correlacionada à solicitação pelo fato de que é o corpo da entidade da resposta http.</span><span class="sxs-lookup"><span data-stu-id="55b40-243">For example, when using [**WS\_ADDRESSING\_VERSION\_TRANSPORT**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) and [**WS\_HTTP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) the reply for the request message is correlated to the request by the fact that is it is the entity body of the HTTP response.</span></span>
-   <span data-ttu-id="55b40-244">A correlação é feita usando os cabeçalhos MessageID e RelatesTo.</span><span class="sxs-lookup"><span data-stu-id="55b40-244">Correlation is done using the MessageID and RelatesTo headers.</span></span> <span data-ttu-id="55b40-245">Esse mecanismo é usado com o [**WS \_ Addressing \_ versão \_ 1 \_ 0**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) e **WS \_ Addressing \_ version \_ 0 \_ 9** (mesmo ao usar a [**\_ \_ \_ Associação de canal http do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)).</span><span class="sxs-lookup"><span data-stu-id="55b40-245">This mechanism is used with [**WS\_ADDRESSING\_VERSION\_1\_0**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) and **WS\_ADDRESSING\_VERSION\_0\_9** (even when using [**WS\_HTTP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)).</span></span> <span data-ttu-id="55b40-246">Nesse caso, a mensagem de solicitação inclui o cabeçalho MessageID.</span><span class="sxs-lookup"><span data-stu-id="55b40-246">In this case, the request message includes the MessageID header.</span></span> <span data-ttu-id="55b40-247">A mensagem de resposta inclui um cabeçalho RelatesTo que tem o valor do cabeçalho MessageID da solicitação.</span><span class="sxs-lookup"><span data-stu-id="55b40-247">The response message includes a RelatesTo header that has the value of the request's MessageID header.</span></span> <span data-ttu-id="55b40-248">O cabeçalho RelatesTo permite que o cliente correlacione uma resposta com uma solicitação enviada.</span><span class="sxs-lookup"><span data-stu-id="55b40-248">The RelatesTo header allows the client to correlate a response with a request it sent.</span></span>

<span data-ttu-id="55b40-249">As seguintes APIs de camada de canal usam automaticamente os mecanismos de correlação apropriados com base na [**\_ \_ versão de endereçamento do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) do canal.</span><span class="sxs-lookup"><span data-stu-id="55b40-249">The following channel layer APIs automatically use the appropriate correlation mechanisms based on the [**WS\_ADDRESSING\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) of the channel.</span></span>

-   [<span data-ttu-id="55b40-250">**WsRequestReply**</span><span class="sxs-lookup"><span data-stu-id="55b40-250">**WsRequestReply**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply)
-   [<span data-ttu-id="55b40-251">**WsSendReplyMessage**</span><span class="sxs-lookup"><span data-stu-id="55b40-251">**WsSendReplyMessage**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage)
-   [<span data-ttu-id="55b40-252">**WsSendFaultMessageForError**</span><span class="sxs-lookup"><span data-stu-id="55b40-252">**WsSendFaultMessageForError**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssendfaultmessageforerror)

<span data-ttu-id="55b40-253">Se essas APIs não forem usadas, os cabeçalhos poderão ser adicionados e acessados manualmente usando [**WsSetHeader**](/windows/desktop/api/WebServices/nf-webservices-wssetheader) ou [**WsGetHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetheader).</span><span class="sxs-lookup"><span data-stu-id="55b40-253">If these APIs are not used, the headers can be manually added and accessed using [**WsSetHeader**](/windows/desktop/api/WebServices/nf-webservices-wssetheader) or [**WsGetHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetheader).</span></span>

## <a name="custom-channels-and-listeners"></a><span data-ttu-id="55b40-254">Canais e ouvintes personalizados</span><span class="sxs-lookup"><span data-stu-id="55b40-254">Custom Channels and Listeners</span></span>

<span data-ttu-id="55b40-255">Se o conjunto predefinido de associações de canal não atender às necessidades do aplicativo, uma implementação de canal e ouvinte personalizado poderá ser definida especificando-se a [**\_ \_ \_ Associação de canal personalizado do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) ao criar o canal ou o ouvinte.</span><span class="sxs-lookup"><span data-stu-id="55b40-255">If the predefined set of channel bindings do not meet the needs of the application, then a custom channel and listener implementation can be defined by specifying [**WS\_CUSTOM\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) when creating the channel or listener.</span></span> <span data-ttu-id="55b40-256">A implementação real do canal/ouvinte é especificada como um conjunto de retornos de chamada por meio da [**Propriedade do WS \_ Channel \_ \_ \_ \_ retornos**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) de chamada de canal personalizado ou propriedades de [**retorno de \_ \_ \_ \_ \_ chamada de ouvinte personalizado da propriedade WS Listener**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) .</span><span class="sxs-lookup"><span data-stu-id="55b40-256">The actual implementation of the channel/listener is specified as a set of callbacks via [**WS\_CHANNEL\_PROPERTY\_CUSTOM\_CHANNEL\_CALLBACKS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) or [**WS\_LISTENER\_PROPERTY\_CUSTOM\_LISTENER\_CALLBACKS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) properties.</span></span> <span data-ttu-id="55b40-257">Depois que um canal ou ouvinte personalizado é criado, o resultado é um objeto [WS \_ Channel](ws-channel.md) ou [WS \_ Listener](ws-listener.md) que pode ser usado com as APIs existentes.</span><span class="sxs-lookup"><span data-stu-id="55b40-257">Once a custom channel or listener are created, the result is a [WS\_CHANNEL](ws-channel.md) or [WS\_LISTENER](ws-listener.md) object that can be used with existing APIs.</span></span>

<span data-ttu-id="55b40-258">Um canal e um ouvinte personalizado também podem ser usados com proxy de serviço e [host de serviço](service-host.md) especificando o valor de **\_ \_ \_ Associação de canal personalizado WS** na enumeração de [**\_ \_ associação do WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) e as propriedades de retorno de chamada de [**\_ \_ \_ \_ canal \_ personalizado de propriedade**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) do WS Channel e Propriedade do WS-up do [**\_ \_ \_ \_ ouvinte \_ personalizado**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) para a criação do proxy de serviço ou host de serviço.</span><span class="sxs-lookup"><span data-stu-id="55b40-258">A custom channel and listener can also be used with Service Proxy and [Service Host](service-host.md) by specifying the **WS\_CUSTOM\_CHANNEL\_BINDING** value in the [**WS\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) enumeration and the [**WS\_CHANNEL\_PROPERTY\_CUSTOM\_CHANNEL\_CALLBACKS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) and [**WS\_LISTENER\_PROPERTY\_CUSTOM\_LISTENER\_CALLBACKS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) properties when creating the Service Proxy or Service Host.</span></span>

## <a name="security"></a><span data-ttu-id="55b40-259">Segurança</span><span class="sxs-lookup"><span data-stu-id="55b40-259">Security</span></span>

<span data-ttu-id="55b40-260">O canal permite limitar a quantidade de memória usada para vários aspectos das operações por meio de propriedades como:</span><span class="sxs-lookup"><span data-stu-id="55b40-260">The channel allows limiting the amount of memory used for various aspects of operations through properties such as:</span></span>

-   <span data-ttu-id="55b40-261">[**WS \_ Propriedade do canal \_ \_ máximo \_ \_ \_ tamanho da mensagem em buffer**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span><span class="sxs-lookup"><span data-stu-id="55b40-261">[**WS\_CHANNEL\_PROPERTY\_MAX\_BUFFERED\_MESSAGE\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="55b40-262">[**WS \_ \_ \_ tamanho máximo da \_ \_ mensagem \_ em fluxo da Propriedade do canal**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span><span class="sxs-lookup"><span data-stu-id="55b40-262">[**WS\_CHANNEL\_PROPERTY\_MAX\_STREAMED\_MESSAGE\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="55b40-263">[**WS \_ Propriedade de canal \_ \_ máximo \_ \_ \_ tamanho inicial em fluxo**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span><span class="sxs-lookup"><span data-stu-id="55b40-263">[**WS\_CHANNEL\_PROPERTY\_MAX\_STREAMED\_START\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="55b40-264">[**WS \_ Propriedade de canal \_ \_ máximo de cabeçalhos de \_ \_ solicitação HTTP \_ \_ \_ tamanho do buffer**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span><span class="sxs-lookup"><span data-stu-id="55b40-264">[**WS\_CHANNEL\_PROPERTY\_MAX\_HTTP\_REQUEST\_HEADERS\_BUFFER\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="55b40-265">[**WS \_ \_ \_ tamanho máximo do \_ \_ dicionário \_ de sessão da propriedade de canal**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span><span class="sxs-lookup"><span data-stu-id="55b40-265">[**WS\_CHANNEL\_PROPERTY\_MAX\_SESSION\_DICTIONARY\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span></span>

<span data-ttu-id="55b40-266">Essas propriedades têm valores padrão que são conservador e seguras para a maioria dos cenários.</span><span class="sxs-lookup"><span data-stu-id="55b40-266">These properties have default values which are conservative and secure for most scenarios.</span></span> <span data-ttu-id="55b40-267">Os valores padrão e quaisquer modificações a eles devem ser cuidadosamente avaliados em relação a possíveis vetores de ataque que podem causar negação de serviço por um usuário remoto.</span><span class="sxs-lookup"><span data-stu-id="55b40-267">Default values and any modifications to them should be carefully evaluated against potential attack vectors which may cause denial of service by a remote user.</span></span>

<span data-ttu-id="55b40-268">O canal permite definir valores de tempo limite para vários aspectos de operações por meio de propriedades como:</span><span class="sxs-lookup"><span data-stu-id="55b40-268">The channel allows setting timeout values for various aspects of operations through properties such as:</span></span>

-   <span data-ttu-id="55b40-269">[**WS \_ \_ \_ \_ tempo limite de conexão da Propriedade do canal**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span><span class="sxs-lookup"><span data-stu-id="55b40-269">[**WS\_CHANNEL\_PROPERTY\_CONNECT\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="55b40-270">[**WS \_ \_ \_ \_ tempo limite de envio da Propriedade do canal**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span><span class="sxs-lookup"><span data-stu-id="55b40-270">[**WS\_CHANNEL\_PROPERTY\_SEND\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="55b40-271">[**WS \_ \_ \_ \_ \_ tempo limite de resposta de recebimento de Propriedade do canal**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span><span class="sxs-lookup"><span data-stu-id="55b40-271">[**WS\_CHANNEL\_PROPERTY\_RECEIVE\_RESPONSE\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="55b40-272">[**WS \_ \_ \_ \_ tempo limite de recebimento da Propriedade do canal**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span><span class="sxs-lookup"><span data-stu-id="55b40-272">[**WS\_CHANNEL\_PROPERTY\_RECEIVE\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="55b40-273">[**WS \_ \_ \_ \_ tempo limite de resolução da Propriedade do canal**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span><span class="sxs-lookup"><span data-stu-id="55b40-273">[**WS\_CHANNEL\_PROPERTY\_RESOLVE\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="55b40-274">[**WS \_ \_ \_ \_ tempo limite de fechamento da Propriedade do canal**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span><span class="sxs-lookup"><span data-stu-id="55b40-274">[**WS\_CHANNEL\_PROPERTY\_CLOSE\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span></span>

<span data-ttu-id="55b40-275">Essas propriedades têm valores padrão que são conservador e seguras para a maioria dos cenários.</span><span class="sxs-lookup"><span data-stu-id="55b40-275">These properties have default values which are conservative and secure for most scenarios.</span></span> <span data-ttu-id="55b40-276">Aumentar os valores de tempo limite aumenta a quantidade de tempo que uma parte remota pode manter um recurso local ativo, como memória, soquetes e threads fazendo e/s síncrona.</span><span class="sxs-lookup"><span data-stu-id="55b40-276">Increasing timeout values increases the amount of time that a remote party can hold a local resource alive, such as memory, sockets, and threads doing synchronous I/O.</span></span> <span data-ttu-id="55b40-277">Um aplicativo deve avaliar os valores padrão e ter cuidado ao aumentar um tempo limite, pois ele pode abrir vetores de ataque potenciais que podem causar negação de serviço de um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="55b40-277">An application should evaluate the default values and use caution when increasing a timeout as it may open up potential attack vectors which may cause denial of service from a remote computer.</span></span>

<span data-ttu-id="55b40-278">Algumas das outras opções de configuração e considerações de design de aplicativo que devem ser avaliadas cuidadosamente ao usar a API de canal do WWSAPI:</span><span class="sxs-lookup"><span data-stu-id="55b40-278">Some of the other configuration options and application design considerations that should be carefully evaluated when using WWSAPI Channel API:</span></span>

-   <span data-ttu-id="55b40-279">Ao usar a camada de canal/ouvinte, cabe ao aplicativo criar e aceitar canais no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="55b40-279">When using the channel/listener layer, it is up to the application to create and accept channels on the server side.</span></span> <span data-ttu-id="55b40-280">Da mesma forma, cabe ao aplicativo criar e abrir canais no lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="55b40-280">Similarly, it is up to the application to create and open channels on the client side.</span></span> <span data-ttu-id="55b40-281">Um aplicativo deve colocar um limite superior nessas operações porque cada canal consome memória e outros recursos limitados, como soquetes.</span><span class="sxs-lookup"><span data-stu-id="55b40-281">An application should put an upper bound on these operations because each channel consumes memory and other limited resources such as sockets.</span></span> <span data-ttu-id="55b40-282">Um aplicativo deve ser especialmente cuidadoso ao criar um canal em resposta a qualquer ação disparada por uma parte remota.</span><span class="sxs-lookup"><span data-stu-id="55b40-282">An application should be especially careful when create a channel in response to any action triggered by a remote party.</span></span>
-   <span data-ttu-id="55b40-283">Cabe ao aplicativo gravar a lógica para criar canais e aceitá-los.</span><span class="sxs-lookup"><span data-stu-id="55b40-283">It is up to the application to write the logic to create channels and accept them.</span></span> <span data-ttu-id="55b40-284">Cada canal consome recursos limitados, como memória e soquetes.</span><span class="sxs-lookup"><span data-stu-id="55b40-284">Each channel consumes limited resources such as memory and sockets.</span></span> <span data-ttu-id="55b40-285">Um aplicativo deve ter um limite superior no número de canais que está disposto a aceitar, ou uma parte remota pode fazer muitas conexões, levando a OOM e, portanto, a negação de serviço.</span><span class="sxs-lookup"><span data-stu-id="55b40-285">An application should have an upper bound on the number of channels it is willing to accept, or a remote party could make many connections, leading to OOM and hence denial of service.</span></span> <span data-ttu-id="55b40-286">Ele também deve receber mensagens ativamente dessas conexões usando um tempo limite pequeno.</span><span class="sxs-lookup"><span data-stu-id="55b40-286">It should also actively receive messages from those connections using a small timeout.</span></span> <span data-ttu-id="55b40-287">Se nenhuma mensagem for recebida, a operação atingirá o tempo limite e a conexão deverá ser liberada.</span><span class="sxs-lookup"><span data-stu-id="55b40-287">If no messages are received, then the operation will time out and the connection should be released.</span></span>
-   <span data-ttu-id="55b40-288">Cabe a um aplicativo enviar uma resposta ou falha interpretando os cabeçalhos de resposta de SOAP ou FaultTo.</span><span class="sxs-lookup"><span data-stu-id="55b40-288">It is up to an application to send a reply or fault by interpreting the ReplyTo or FaultTo SOAP headers.</span></span> <span data-ttu-id="55b40-289">A prática segura é respeitar apenas um cabeçalho ReplyTo ou FaultTo, que é "anônimo", o que significa que a conexão existente (TCP, HTTP) ou UDP (IP de origem) deve ser usada para enviar a resposta SOAP.</span><span class="sxs-lookup"><span data-stu-id="55b40-289">The secure practice is to only honor a ReplyTo or FaultTo header which is "anonymous", meaning that the existing connection (TCP, HTTP) or source IP (UDP) should be used to send the SOAP reply.</span></span> <span data-ttu-id="55b40-290">Os aplicativos devem ter muito cuidado ao criar recursos (como um canal) para responder a um endereço diferente, a menos que a mensagem tenha sido assinada por uma entidade que possa falar pelo endereço ao qual a resposta está sendo enviada.</span><span class="sxs-lookup"><span data-stu-id="55b40-290">Applications should exercise extreme caution when creating resources (such as a channel) in order to reply to a different address, unless the message was signed by a party that can speak for the address that the reply is being sent to.</span></span>
-   <span data-ttu-id="55b40-291">A validação feita na camada de canal não é substituída pela integridade dos dados obtida por meio de segurança.</span><span class="sxs-lookup"><span data-stu-id="55b40-291">The validation done in the channel layer is no replacement for data integrity achieved through security.</span></span> <span data-ttu-id="55b40-292">Um aplicativo deve contar com os recursos de segurança do WWSAPI para garantir que ele esteja se comunicando com uma entidade confiável e também deve contar com a segurança para garantir a integridade dos dados.</span><span class="sxs-lookup"><span data-stu-id="55b40-292">An application must rely on security features of the WWSAPI to ensure that it is communicating with a trusted entity, and must also rely on security to ensure data integrity.</span></span>

<span data-ttu-id="55b40-293">Da mesma forma, há opções de configuração de mensagem e considerações de design de aplicativo que devem ser avaliadas cuidadosamente ao usar a API de mensagem WWSAPI:</span><span class="sxs-lookup"><span data-stu-id="55b40-293">Similarly, there are message configuration options and application design considerations that should be carefully evaluated when using WWSAPI Message API:</span></span>

-   <span data-ttu-id="55b40-294">O tamanho do heap usado para armazenar os cabeçalhos de uma mensagem pode ser configurado usando a propriedade [**de \_ \_ Propriedades do \_ heap \_ da propriedade de mensagem WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) .</span><span class="sxs-lookup"><span data-stu-id="55b40-294">The size of the heap used to store the headers of a message can be configured using the [**WS\_MESSAGE\_PROPERTY\_HEAP\_PROPERTIES**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) property.</span></span> <span data-ttu-id="55b40-295">Aumentar esse valor permite que mais memória seja consumida pelos cabeçalhos da mensagem, o que pode levar a OOM.</span><span class="sxs-lookup"><span data-stu-id="55b40-295">Increasing this value allows more memory to be consumed by the headers of the message, which can lead to OOM.</span></span>
-   <span data-ttu-id="55b40-296">O usuário do objeto Message deve perceber que as APIs de acesso ao cabeçalho são O (n) em relação ao número de cabeçalhos na mensagem, pois eles verificam se há duplicatas.</span><span class="sxs-lookup"><span data-stu-id="55b40-296">The user of the message object must realize that the header access APIs are O(n) with respect to the number of headers in the message, since they check for duplicates.</span></span> <span data-ttu-id="55b40-297">Os designs que exigem muitos cabeçalhos em uma mensagem podem levar ao uso excessivo da CPU.</span><span class="sxs-lookup"><span data-stu-id="55b40-297">Designs which require many headers in a message may lead to excessive CPU usage.</span></span>
-   <span data-ttu-id="55b40-298">O número máximo de cabeçalhos em uma mensagem pode ser configurado usando a propriedade [**WS \_ Message \_ propriedade \_ Max \_ Processed \_ Headers**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) .</span><span class="sxs-lookup"><span data-stu-id="55b40-298">The maximum number of headers in a message can be configured using the [**WS\_MESSAGE\_PROPERTY\_MAX\_PROCESSED\_HEADERS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) property.</span></span> <span data-ttu-id="55b40-299">Há também um limite implícito com base no tamanho do heap da mensagem.</span><span class="sxs-lookup"><span data-stu-id="55b40-299">There is also an implicit limit based on the size of the heap of the message.</span></span> <span data-ttu-id="55b40-300">O aumento de ambos os valores permite que mais cabeçalhos estejam presentes, o que aumenta o tempo necessário para encontrar um cabeçalho (ao usar as APIs de acesso ao cabeçalho).</span><span class="sxs-lookup"><span data-stu-id="55b40-300">Increasing both of these values allows more headers to be present, which compounds the time necessary to find a header (when using the header access APIs).</span></span>

 

 




