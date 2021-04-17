---
description: O protocolo de handshake de TLS é responsável pela autenticação e troca de chaves necessárias para estabelecer ou retomar as sessões seguras.
ms.assetid: 65fb4db3-e505-457a-9159-dba0b506ea0b
title: Protocolo de handshake TLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c7cfa9e9db54a6035abe147ce00bbde59bcc86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748410"
---
# <a name="tls-handshake-protocol"></a>Protocolo de handshake TLS

O [*protocolo de handshake de TLS*](../secgloss/t-gly.md) é responsável pela autenticação e troca de chaves necessárias para estabelecer ou retomar as sessões seguras. Ao estabelecer uma [*sessão*](../secgloss/s-gly.md)segura, o protocolo de handshake gerencia o seguinte:

-   Negociação do conjunto de codificação
-   Autenticação do servidor e, opcionalmente, o cliente
-   Troca de informações de chave de sessão.

## <a name="cipher-suite-negotiation"></a>Negociação do conjunto de codificação

O cliente e o servidor fazem contato e escolhem o pacote de codificação que será usado em toda a troca de mensagens.

## <a name="authentication"></a>Autenticação

No TLS, um servidor comprova sua identidade para o cliente. O cliente também pode precisar provar sua identidade para o servidor. A PKI, o uso de [*pares de chaves pública/privada*](../secgloss/p-gly.md), é a base dessa autenticação. O método exato usado para autenticação é determinado pelo conjunto de codificação negociado.

## <a name="key-exchange"></a>Troca de chaves

O cliente e o servidor trocam números aleatórios e um número especial chamado de segredo pré-mestre. Esses números são combinados com dados adicionais, permitindo que o cliente e o servidor criem seu segredo compartilhado, chamado de segredo mestre. O segredo mestre é usado pelo cliente e pelo servidor para gerar o segredo de gravação de MAC, que é a chave de sessão usada para [*hash*](../secgloss/h-gly.md)e a chave de gravação, que é a [*chave de sessão*](../secgloss/s-gly.md) usada para criptografia.

## <a name="establishing-a-secure-session-by-using-tls"></a>Estabelecendo uma sessão segura usando TLS

O protocolo de handshake TLS envolve as seguintes etapas:

1.  O cliente envia uma mensagem de "saudação do cliente" para o servidor, juntamente com o valor aleatório do cliente e os conjuntos de criptografia com suporte.
2.  O servidor responde enviando uma mensagem de "servidor Hello" para o cliente, juntamente com o valor aleatório do servidor.
3.  O servidor envia seu certificado ao cliente para autenticação e pode solicitar um certificado do cliente. O servidor envia a mensagem "Olá do servidor".
4.  Se o servidor tiver solicitado um certificado do cliente, o cliente o enviará.
5.  O cliente cria um segredo de pre-mestre aleatório e o criptografa com a [*chave pública*](../secgloss/p-gly.md) do certificado do servidor, enviando o segredo de pré-mestre criptografado para o servidor.
6.  O servidor recebe o segredo pré-mestre. O servidor e o cliente geram o segredo mestre e [*as chaves de sessão*](../secgloss/s-gly.md) com base no segredo de pré-mestre.
7.  O cliente envia a notificação "alterar especificação de codificação" para o servidor para indicar que o cliente começará a usar as novas [*chaves de sessão*](../secgloss/s-gly.md) para [*hash*](../secgloss/h-gly.md) e criptografia de mensagens. O cliente também envia a mensagem "cliente concluído".
8.  O servidor recebe "alterar especificação de codificação" e alterna seu estado de segurança da camada de registro para [*criptografia simétrica*](../secgloss/s-gly.md) usando as [*chaves de sessão*](../secgloss/s-gly.md). O servidor envia a mensagem "servidor concluído" ao cliente.
9.  O cliente e o servidor agora podem trocar dados de aplicativo pelo canal protegido que eles estabeleceram. Todas as mensagens enviadas do cliente para o servidor e do servidor para o cliente são criptografadas usando a chave de sessão.

## <a name="resuming-a-secure-session-by-using-tls"></a>Retomando uma sessão segura usando TLS

1.  O cliente envia uma mensagem "Olá ao cliente" usando a ID de sessão da sessão a ser retomada.
2.  O servidor verifica o cache da sessão em busca de uma ID de sessão correspondente. Se uma correspondência for encontrada e o servidor for capaz de retomar a sessão, ele enviará uma mensagem de "servidor Hello" com a ID de sessão.
    > [!Note]  
    > Se uma correspondência de ID de sessão não for encontrada, o servidor gerará uma nova ID de sessão e o cliente TLS e o servidor executarão um handshake completo.

     

3.  O cliente e o servidor devem trocar mensagens "alterar especificação de codificação" e enviar mensagens "cliente concluído" e "servidor concluído".
4.  O cliente e o servidor agora podem retomar a troca de dados do aplicativo pelo canal seguro.

 

 
