---
description: Após um tíquete de concessão de tíquete (TGT) e uma chave de sessão terem sido estabelecidos para o cliente, o cliente pode solicitar uma chave de sessão e um tíquete separados para o serviço.
ms.assetid: b4f63642-9282-4e11-b40c-eec406b2dd2b
title: Troca de serviços de concessão de tíquete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b227ee551d762abd145ca56c6cced110b6a2dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750452"
---
# <a name="ticket-granting-service-exchange"></a>Troca de serviços de concessão de tíquete

Após um tíquete de concessão de tíquete (TGT) e uma [*chave de sessão*](../secgloss/s-gly.md) terem sido estabelecidos para o cliente, o cliente pode solicitar uma chave de sessão e um tíquete separados para o serviço.

**Para solicitar um tíquete para outro serviço**

1.  O cliente Kerberos na estação de trabalho do usuário solicita [*credenciais*](../secgloss/c-gly.md) para o serviço enviando para o [*centro de distribuição de chaves*](../secgloss/k-gly.md) (KDC), uma mensagem do tipo KRB \_ TGS \_ req (Ticket-Granting solicitação de serviço Kerberos). Essa mensagem consiste na identidade do serviço para o qual o cliente está solicitando credenciais, uma mensagem de autenticador criptografada com a nova [*chave de sessão*](../secgloss/s-gly.md)de logon do usuário e o TGT obtido da [troca do serviço de autenticação](authentication-service-exchange.md).
2.  Quando o KDC recebe um KRB \_ TGS \_ req, o KDC DESCRIPTOGRAFA o TGT com sua chave secreta e extrai a chave de sessão de logon do usuário.
3.  O KDC usa a [*chave de sessão*](../secgloss/s-gly.md) de logon para descriptografar a mensagem do autenticador do usuário e a avalia. Se o autenticador passar no teste, o KDC extrairá os dados de autorização do usuário do TGT e ininventará uma chave de sessão para o usuário compartilhar com o servidor solicitado.
4.  O KDC criptografa uma cópia da chave de sessão de serviço com a chave de sessão de logon do usuário.
5.  O KDC insere outra cópia da chave de sessão de serviço em um tíquete, juntamente com os dados de autorização do usuário, e criptografa o tíquete com a [*chave mestra*](../secgloss/m-gly.md)do servidor.
6.  O KDC envia essas credenciais de volta para o cliente respondendo com uma mensagem do tipo KRB \_ TGS \_ Rep (Kerberos Ticket-Granting Service Reply).
7.  Quando o cliente recebe a resposta, ele descriptografa a chave de sessão de serviço com a chave de sessão de logon do usuário e armazena a chave de sessão de serviço em seu cache de tíquete.
8.  O cliente extrai o tíquete para o servidor e o armazena em seu cache de tíquetes.

 

 
