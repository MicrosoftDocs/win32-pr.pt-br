---
description: Ao desenvolver um aplicativo que usa o Microsoft Windows HTTP Services (WinHTTP), é importante entender os conceitos e a terminologia a seguir relacionados à rede em geral e o protocolo HTTP em particular.
ms.assetid: 6ea0c16f-1233-4580-97bb-14e224646857
title: Terminologia de rede (WinHTTP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8173b921957a95ebde7f00034c31b2f016b78ab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105797611"
---
# <a name="network-terminology-winhttp"></a>Terminologia de rede (WinHTTP)

Ao desenvolver um aplicativo que usa o Microsoft Windows HTTP Services (WinHTTP), é importante entender os conceitos e a terminologia a seguir relacionados à rede em geral e o protocolo HTTP em particular.

-   [Transações HTTP](#http-transactions)
-   [Servidores proxy](#proxy-servers)
-   [Modos síncronos e assíncronos](#synchronous-and-asynchronous-modes)
-   [Autenticação](#authentication)

## <a name="http-transactions"></a>Transações HTTP

Quando você trabalha com transações HTTP, está trocando informações com outro computador em outro lugar em uma rede. As informações trocadas podem ser um arquivo que contém texto ou multimídia, ou podem ser os resultados de uma consulta de banco de dados. Uma informação trocada em uma rede é chamada de *recurso*. Normalmente, o computador que envia um recurso é o servidor e o computador que recebe esse recurso é um cliente do. No entanto, também é possível que um cliente poste dados em um servidor. Às vezes, uma transação HTTP envolve um servidor de camada intermediária. Um servidor de camada intermediária reúne vários recursos de outros servidores, compila as informações em um recurso e envia esse recurso para o cliente.

O processo de obtenção de um recurso usando o protocolo HTTP requer que uma série de mensagens seja trocada entre o cliente e o servidor. O cliente inicia a transação enviando uma mensagem que solicita um recurso. Essa mensagem é chamada de solicitação HTTP ou, às vezes, apenas uma solicitação. Uma solicitação HTTP consiste nos seguintes componentes.

-   Método, Uniform Resource Identifier (URI), número de versão do protocolo
-   Cabeçalhos
-   Corpo da entidade

Quando um servidor recebe uma solicitação, ele responde enviando uma mensagem de volta ao cliente. A mensagem enviada pelo servidor é chamada de resposta HTTP. Uma resposta HTTP consiste nos seguintes componentes.

-   Número de versão do protocolo, código de status, texto de status
-   Cabeçalhos
-   Corpo da entidade

A resposta indica que a solicitação não pode ser processada ou fornece informações solicitadas. Dependendo do tipo de solicitação, podem ser informações sobre um recurso, como seu tamanho e tipo, ou podem ser alguns ou todos os recursos em si. A parte de uma resposta que inclui alguns ou todos os recursos solicitados é chamada de "dados de resposta" ou "corpo da entidade", e a resposta não é concluída até que todos os dados de resposta sejam recebidos.

Para obter informações detalhadas sobre transações HTTP e o protocolo HTTP, consulte [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt), protocolo de transferência de hipertexto – HTTP/1.1.

## <a name="proxy-servers"></a>Servidores proxy

Embora uma solicitação enviada por um cliente seja eventualmente recebida pelo servidor de destino, às vezes a transação passa pela primeira vez por um servidor proxy. Um proxy intercepta a solicitação e pode até mesmo modificar a solicitação, antes de enviá-la para o servidor. Quando o servidor responde, a resposta também passa pelo proxy antes de ele ser encaminhado para o cliente. O proxy pode modificar os cabeçalhos nesta resposta.

Interceptando e convertendo as transações de rede, um proxy pode:

-   Proteja o cliente Monitorando transações potencialmente perigosas.
-   Habilite o cliente para se comunicar usando protocolos que podem não ser implementados pelo software cliente.
-   Agir como um gateway entre uma rede privada e uma rede pública.

A API do WinHTTP inclui uma ferramenta de configuração de proxy que permite fornecer ao WinHTTP informações sobre quaisquer servidores proxy que interceptam suas transações HTTP. Para obter informações sobre como usar a ferramenta de configuração de proxy, consulte [ProxyCfg.exe, uma ferramenta de configuração de proxy](proxycfg-exe--a-proxy-configuration-tool.md).

## <a name="synchronous-and-asynchronous-modes"></a>Modos síncronos e assíncronos

Há dois modelos de programação para obter recursos em uma rede usando o WinHTTP — os modelos síncronos e assíncronos. Em um modelo síncrono, uma chamada para uma função ou método não é concluída até que a operação solicitada seja concluída ou até que ocorra um erro. Por exemplo, quando o aplicativo solicita um recurso usando o WinHTTP de forma síncrona, ele não continua com a próxima etapa até que os dados solicitados tenham sido recebidos.

Um modelo assíncrono, por outro lado, permite que um aplicativo execute outras tarefas enquanto aguarda o recurso ser recuperado. Se outra função ou método WinHTTP for chamado e uma operação anterior não tiver sido concluída, a função retornará um erro. Ao usar o WinHTTP de forma assíncrona, os eventos de Component Object Model (COM) e o retorno de chamada estão disponíveis para notificar um aplicativo sobre o progresso em uma operação HTTP.

## <a name="authentication"></a>Autenticação

A autenticação é o processo pelo qual um proxy HTTP ou servidor HTTP valida as informações de logon de um usuário antes de permitir o acesso aos recursos. Vários esquemas de autenticação são usados na Internet. Normalmente, o nome e a senha de um usuário são comparados com uma lista autorizada e, se o sistema detectar uma correspondência, o acesso será concedido à extensão especificada na lista de permissões para o usuário.

As funções WinHTTP dão suporte à autenticação de servidor e proxy para sessões HTTP. O WinHTTP dá suporte aos seguintes esquemas de autenticação: básico, Digest (consulte [RFC 2617](https://www.ietf.org/rfc/rfc2617.txt)), [autenticação NTLM](../com/ntlmssp.md), Negotiate/ [Kerberos](../com/kerberos-v5-protocol.md)e Microsoft Passport 1,4. Para obter informações detalhadas sobre a autenticação, bem como um exemplo de como usar a autenticação em um aplicativo Microsoft Visual C++, consulte [autenticação no WinHTTP](authentication-in-winhttp.md).

Para obter informações sobre considerações de segurança sobre autenticação básica e do Passport, consulte [considerações de segurança do WinHTTP](winhttp-security-considerations.md).

 

 
