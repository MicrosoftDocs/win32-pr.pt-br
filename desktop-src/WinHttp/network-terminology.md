---
description: Ao desenvolver um aplicativo que usa o WinHTTP (Microsoft Windows HTTP Services), é importante entender os seguintes conceitos e terminologia relacionados à rede em geral e ao protocolo HTTP em particular.
ms.assetid: 6ea0c16f-1233-4580-97bb-14e224646857
title: Terminologia de rede (WinHTTP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bec92d5dd99247fab3ade48760db343983cd7092ea96ac8bd059ed892c9aa42a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643796"
---
# <a name="network-terminology-winhttp"></a>Terminologia de rede (WinHTTP)

Ao desenvolver um aplicativo que usa o WinHTTP (Microsoft Windows HTTP Services), é importante entender os seguintes conceitos e terminologia relacionados à rede em geral e ao protocolo HTTP em particular.

-   [Transações HTTP](#http-transactions)
-   [Servidores proxy](#proxy-servers)
-   [Modos síncronos e assíncronos](#synchronous-and-asynchronous-modes)
-   [Autenticação](#authentication)

## <a name="http-transactions"></a>Transações HTTP

Ao trabalhar com transações HTTP, você está trocando informações com outro computador em outro lugar em uma rede. As informações trocadas podem ser um arquivo que contém texto ou multimídia ou podem ser os resultados de uma consulta de banco de dados. Uma parte das informações trocadas por uma rede é chamada de *recurso*. Normalmente, o computador que envia um recurso é o servidor e o computador que recebe esse recurso é um cliente. No entanto, também é possível que um cliente poste dados em um servidor. Às vezes, uma transação HTTP envolve um servidor de camada intermediária. Um servidor de camada intermediária reúne vários recursos de outros servidores, compila as informações em um recurso e envia esse recurso para o cliente.

O processo de obtenção de um recurso usando o protocolo HTTP requer que uma série de mensagens seja trocada entre o cliente e o servidor. O cliente inicia a transação enviando uma mensagem que solicita um recurso. Essa mensagem é chamada de solicitação HTTP ou, às vezes, apenas uma solicitação. Uma solicitação HTTP consiste nos seguintes componentes.

-   Método, Uniform Resource Identifier (URI), número de versão do protocolo
-   Cabeçalhos
-   Corpo da entidade

Quando um servidor recebe uma solicitação, ele responde enviando uma mensagem de volta ao cliente. A mensagem enviada pelo servidor é chamada de resposta HTTP. Uma resposta HTTP consiste nos seguintes componentes.

-   Número de versão do protocolo, código de status, texto de status
-   Cabeçalhos
-   Corpo da entidade

A resposta indica que a solicitação não pode ser processada ou fornece informações solicitadas. Dependendo do tipo de solicitação, isso pode ser informações sobre um recurso, como seu tamanho e tipo, ou pode ser algum ou todos os recursos em si. A parte de uma resposta que inclui alguns ou todos os recursos solicitados é chamada de "dados de resposta" ou "corpo da entidade", e a resposta não é concluída até que todos os dados de resposta são recebidos.

Para obter informações detalhadas sobre transações HTTP e o protocolo HTTP, consulte [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt), Protocolo de Transferência de Hipertexto — HTTP/1.1.

## <a name="proxy-servers"></a>Servidores proxy

Embora uma solicitação enviada por um cliente seja eventualmente recebida pelo servidor de destino, às vezes, a transação passa primeiro por um servidor proxy. Um proxy intercepta a solicitação e pode até mesmo modificar a solicitação, antes de enviá-la para o servidor. Quando o servidor responde, a resposta também passa pelo proxy antes de ser encaminhada para o cliente. O proxy pode modificar os headers nesta resposta.

Interceptando e traduzindo transações de rede, um proxy pode:

-   Proteja o cliente monitorando transações potencialmente perigosas.
-   Permitir que o cliente se comunique usando protocolos que podem não ser implementados pelo software cliente.
-   Atue como um gateway entre uma rede privada e uma rede pública.

A API WinHTTP inclui uma ferramenta de configuração de proxy que permite que você forneça ao WinHTTP informações sobre os servidores proxy que interceptam suas transações HTTP. Para obter informações sobre como usar a ferramenta de configuração de proxy, [ consulteProxyCfg.exe, uma Ferramenta de Configuração de Proxy](proxycfg-exe--a-proxy-configuration-tool.md).

## <a name="synchronous-and-asynchronous-modes"></a>Modos síncronos e assíncronos

Há dois modelos de programação para obter recursos em uma rede usando WinHTTP — os modelos síncronos e assíncronos. Em um modelo síncrono, uma chamada para uma função ou método não é concluída até que a operação solicitada seja concluída ou até que ocorra um erro. Por exemplo, quando seu aplicativo solicita um recurso usando WinHTTP de forma síncrona, ele não continua com a próxima etapa até que os dados solicitados foram recebidos.

Um modelo assíncrono, por outro lado, permite que um aplicativo execute outras tarefas enquanto aguarda a recuperação do recurso. Se outra função ou método WinHTTP for chamado e uma operação anterior não tiver sido concluída, a função retornará um erro. Ao usar WinHTTP de forma assíncrona, Component Object Model eventos e retorno de chamada (COM) estão disponíveis para notificar um aplicativo de progresso em uma operação HTTP.

## <a name="authentication"></a>Autenticação

A autenticação é o processo pelo qual um proxy HTTP ou servidor HTTP valida as informações de logon de um usuário antes de permitir o acesso aos recursos. Vários esquemas de autenticação são usados na Internet. Normalmente, o nome e a senha de um usuário são comparados com uma lista autorizada e, se o sistema detectar uma combinação, o acesso será concedido até a extensão especificada na lista de permissões para o usuário.

As funções WinHTTP são suportadas pela autenticação de servidor e proxy para sessões HTTP. O WinHTTP dá suporte aos seguintes esquemas de autenticação: Basic, Digest (consulte [RFC 2617),](https://www.ietf.org/rfc/rfc2617.txt) [Autenticação NTLM](../com/ntlmssp.md), Negotiate/Kerberos e Microsoft Passport 1.4. [](../com/kerberos-v5-protocol.md) Para obter informações detalhadas sobre autenticação, bem como um exemplo de como usar a autenticação em um aplicativo Microsoft Visual C++, consulte Autenticação [no WinHTTP](authentication-in-winhttp.md).

Para obter informações sobre considerações de segurança sobre a autenticação Básica e do Passport, consulte Considerações de segurança [do WinHTTP.](winhttp-security-considerations.md)

 

 
