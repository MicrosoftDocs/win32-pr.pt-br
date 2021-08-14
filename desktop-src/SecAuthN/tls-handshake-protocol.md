---
description: O protocolo de handshake TLS é responsável pela autenticação e pela troca de chaves necessárias para estabelecer ou retomar sessões seguras.
ms.assetid: 65fb4db3-e505-457a-9159-dba0b506ea0b
title: Protocolo de handshake TLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fe32e11127bf46088aa04e58dd6444620cea327c08d2609e01749efcb1e00df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915814"
---
# <a name="tls-handshake-protocol"></a>Protocolo de handshake TLS

O [*protocolo de handshake*](../secgloss/t-gly.md) TLS é responsável pela autenticação e pela troca de chaves necessárias para estabelecer ou retomar sessões seguras. Ao estabelecer uma sessão [*segura,*](../secgloss/s-gly.md)o Protocolo handshake gerencia o seguinte:

-   Negociação do conjunto de criptografias
-   Autenticação do servidor e, opcionalmente, do cliente
-   Troca de informações de chave de sessão.

## <a name="cipher-suite-negotiation"></a>Negociação do Cipher Suite

O cliente e o servidor fazem contato e escolhem o conjunto de criptografias que será usado em toda a troca de mensagens.

## <a name="authentication"></a>Autenticação

No TLS, um servidor prova sua identidade para o cliente. O cliente também pode precisar provar sua identidade para o servidor. A PKI, o uso de [*pares de chaves públicas/privadas,*](../secgloss/p-gly.md)é a base dessa autenticação. O método exato usado para autenticação é determinado pelo pacote de criptografia negociado.

## <a name="key-exchange"></a>Chave Exchange

O cliente e o servidor trocam números aleatórios e um número especial chamado Segredo pré-mestre. Esses números são combinados com dados adicionais que permitem que o cliente e o servidor criem seu segredo compartilhado, chamado de Segredo Mestre. O Segredo Mestre é usado pelo cliente e pelo servidor para gerar o segredo mac de gravação, [](../secgloss/s-gly.md) que é a chave de sessão usada para [*hash*](../secgloss/h-gly.md)e a chave de gravação, que é a chave de sessão usada para criptografia.

## <a name="establishing-a-secure-session-by-using-tls"></a>Estabelecendo uma sessão segura usando TLS

O Protocolo de Handshake TLS envolve as seguintes etapas:

1.  O cliente envia uma mensagem "Olá do cliente" para o servidor, juntamente com o valor aleatório do cliente e os pacote de criptografia com suporte.
2.  O servidor responde enviando uma mensagem "Olá do servidor" para o cliente, juntamente com o valor aleatório do servidor.
3.  O servidor envia seu certificado para o cliente para autenticação e pode solicitar um certificado do cliente. O servidor envia a mensagem "Server hello done".
4.  Se o servidor solicitou um certificado do cliente, o cliente o envia.
5.  O cliente cria um segredo pré-mestre aleatório [](../secgloss/p-gly.md) e o criptografa com a chave pública do certificado do servidor, enviando o Segredo Pré-Mestre criptografado para o servidor.
6.  O servidor recebe o segredo pré-mestre. Cada servidor e cliente geram o Segredo Mestre e as chaves [*de sessão*](../secgloss/s-gly.md) com base no Segredo pré-mestre.
7.  O cliente envia a notificação "Alterar especificação de criptografia" [](../secgloss/s-gly.md) para o servidor para indicar que o cliente começará a usar as novas chaves de sessão para [*hash*](../secgloss/h-gly.md) e mensagens criptografadas. O cliente também envia a mensagem "Cliente concluído".
8.  O servidor recebe "Alterar especificação de criptografia" e alterna seu estado de segurança da camada de registro para criptografia [*simétrica*](../secgloss/s-gly.md) usando as [*chaves de sessão*](../secgloss/s-gly.md). O servidor envia a mensagem "Servidor concluído" para o cliente.
9.  O cliente e o servidor agora podem trocar dados de aplicativo pelo canal protegido que eles estabeleceram. Todas as mensagens enviadas do cliente para o servidor e do servidor para o cliente são criptografadas usando a chave de sessão.

## <a name="resuming-a-secure-session-by-using-tls"></a>Retomar uma sessão segura usando TLS

1.  O cliente envia uma mensagem "Olá do cliente" usando a ID da Sessão da sessão a ser retomada.
2.  O servidor verifica seu cache de sessão quanto a uma ID de sessão correspondente. Se uma corresponder for encontrada e o servidor for capaz de retomar a sessão, ele enviará uma mensagem "Server hello" com a ID da Sessão.
    > [!Note]  
    > Se uma ID de sessão não for encontrada, o servidor gerará uma nova ID de sessão e o cliente e o servidor TLS executarão um handshake completo.

     

3.  O cliente e o servidor devem trocar mensagens "Alterar especificação de criptografia" e enviar mensagens "Cliente concluído" e "Servidor concluído".
4.  O cliente e o servidor agora podem retomar a troca de dados do aplicativo pelo canal seguro.

 

 
