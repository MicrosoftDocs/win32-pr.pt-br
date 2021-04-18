---
description: Em um protocolo de aplicativo cliente/servidor, um servidor é associado a uma porta de comunicação, como um soquete ou uma interface RPC.
ms.assetid: 176d4ca5-83dd-42ef-b116-227d4badc0dd
title: Estabelecendo uma conexão segura com autenticação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a43483893c8dcf56e6db6b3c7d7aa1451bf9540
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751726"
---
# <a name="establishing-a-secure-connection-with-authentication"></a>Estabelecendo uma conexão segura com autenticação

Em um [*protocolo de aplicativo*](/windows/desktop/SecGloss/a-gly)cliente/servidor, um servidor é associado a uma porta de comunicação, como um soquete ou uma interface RPC. Em seguida, o servidor aguarda um cliente se conectar e solicitar o serviço. A função de segurança na instalação da conexão é duas vezes no caso de autenticação mútua:

-   Autenticação de cliente pelo servidor.
-   Autenticação de servidor pelo cliente.

Os componentes de cliente e servidor de um aplicativo de transporte usam um [*pacote de segurança*](/windows/desktop/SecGloss/s-gly) para estabelecer uma conexão segura para transmissão de mensagens. A primeira etapa ao estabelecer uma conexão segura é criar um [*contexto de segurança*](/windows/desktop/SecGloss/s-gly); ou seja, uma estrutura de dados opaca que contém os dados de segurança relevantes para uma conexão, como uma [*chave de sessão*](/windows/desktop/SecGloss/s-gly) e a duração da sessão.

Um contexto de segurança é, essencialmente, uma mensagem do pacote de segurança associado ao cliente para o pacote de segurança associado ao servidor. Consequentemente, a criação de um contexto de segurança geralmente exige que o cliente e o servidor façam chamadas para seus respectivos pacotes de segurança. Para obter mais informações sobre funções de contexto, consulte [Gerenciamento de contexto](authentication-functions.md).

O protocolo usado para estabelecer uma conexão segura e autenticada envolve a troca de um ou mais "tokens de segurança" entre o cliente e o servidor. Esses tokens são enviados como mensagens opacas pelos dois lados, juntamente com quaisquer outras informações específicas de [*protocolo de aplicativo*](/windows/desktop/SecGloss/a-gly). Como uma mensagem opaca, o token é recebido de uma função de pacote de segurança pelo cliente, que não pode interpretar ou alterá-la e encaminhada como uma mensagem para o servidor. O token também é opaco para o servidor, que não pode interpretar nem alterar o token. O servidor encaminha o token opaco para seu pacote de segurança para interpretação. Em seguida, o pacote informa ao servidor a autenticação do cliente ou falha na autenticação.

O cliente recebe o token do servidor em uma mensagem, recupera o token da mensagem recebida e usa esse token em uma chamada para seu pacote de segurança. O cliente então chama o pacote de segurança novamente indicando se uma conexão segura foi estabelecida ou se outras trocas são necessárias antes que uma conexão segura esteja pronta. Teoricamente, não há nenhum limite para o número de trocas de tokens de segurança necessários. Na prática, apenas um número limitado de trocas é necessário. A autenticação NTLM é baseada no esquema de desafio/resposta e usa três segmentos para autenticar um cliente no servidor. O protocolo [*Kerberos*](/windows/desktop/SecGloss/k-gly) versão 5,0 pode exigir trocas de mensagens adicionais.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Inicialização do contexto do cliente](client-context-initialization.md)
</dt> <dt>

[Inicialização do contexto do servidor](server-context-initialization.md)
</dt> </dl>

 

 
