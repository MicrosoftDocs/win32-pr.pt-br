---
title: Sobre a autenticação mútua usando o Kerberos
description: Na autenticação mútua, o cliente e o serviço devem verificar suas respectivas identidades entre si antes de executar funções de aplicativo.
ms.assetid: 5ce923d6-bede-4acb-b297-e93f2f506ea9
ms.tgt_platform: multiple
keywords:
- Sobre a autenticação mútua usando o AD do Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9685dad0bd20f233b8dcb0ecf12af338f318646f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004823"
---
# <a name="about-mutual-authentication-using-kerberos"></a>Sobre a autenticação mútua usando o Kerberos

Na autenticação mútua, o cliente e o serviço devem verificar suas respectivas identidades entre si antes de executar funções de aplicativo. Nenhuma das partes pode executar operações com a outra até que a identidade tenha sido verificada; ou seja, o serviço deve ser capaz de verificar o cliente sem consultar o cliente e o cliente deve ser capaz de verificar o serviço sem consultar o serviço.

O valor de um serviço que pode autenticar um cliente é bem conhecido. Por exemplo, um serviço de arquivo representa um cliente para determinar quais arquivos o cliente pode acessar.

O valor de um cliente que pode autenticar um serviço é menos compreendido. A autenticação de um serviço permite que o cliente confie nos dados que obtém do serviço e que seja seguro no envio de dados confidenciais para o serviço. A capacidade de um cliente de autenticar um serviço é particularmente importante em aplicativos cliente/serviço que dão suporte à delegação do contexto de segurança do cliente; ou seja, o cliente autoriza o serviço a atuar como seu representante no acesso a serviços adicionais ou recursos de rede.

Um serviço autentica um cliente da seguinte maneira: o cliente estabelece um contexto de segurança local executando em um contexto estabelecido anteriormente, por exemplo, na sessão de um usuário conectado ou apresentando explicitamente as credenciais para o provedor de segurança subjacente. O serviço não pode aceitar conexões de nenhum cliente não autenticado.

O mecanismo Kerberos pelo qual um cliente autentica um serviço funciona da seguinte maneira: quando um serviço é instalado, um instalador de serviço, executando com privilégios de administrador, registra um ou mais SPNs exclusivos para cada instância de serviço. Os nomes são registrados no controlador de Domínio do Active Directory (DC) no objeto de conta de usuário ou computador que a instância de serviço usará para fazer logon. Quando um cliente solicita uma conexão a um serviço, ele compõe um SPN para uma instância de serviço, usando dados conhecidos ou dados fornecidos pelo usuário. Em seguida, o cliente usa o pacote de negociação SSPI para apresentar o SPN ao centro de distribuição de chaves (KDC) para a conta de domínio do cliente. O KDC pesquisa a floresta em busca de uma conta de usuário ou computador na qual o SPN está registrado. Se o SPN estiver registrado em mais de uma conta, a autenticação falhará. Caso contrário, o KDC criptografa uma mensagem usando a senha da conta na qual o SPN foi registrado. O KDC passa essa mensagem criptografada para o cliente, que, por sua vez, a passa para a instância do serviço. O serviço usa o pacote de negociação SSPI para descriptografar a mensagem, que passa de volta para o cliente e para o KDC do cliente. O KDC autenticará o serviço se a mensagem descriptografada corresponder à sua mensagem original.

-   Para obter mais informações sobre como compor e registrar SPNs, consulte. [Nomes da entidade de serviço](service-principal-names.md)
-   Para obter mais informações e um exemplo de código que compõe um SPN para um serviço do Windows Sockets que se publica com um ponto de conexão de serviço, consulte [compondo os SPNs de um serviço com um SCP](composing-the-spns-for-a-service-with-an-scp.md).
-   Para obter mais informações e um exemplo de código que compõe um SPN para um serviço RPC, consulte [compoting SPNs para um serviço RpcNs](composing-spns-for-an-rpcns-service.md).

 

 




