---
description: Em um modelo de aplicativo cliente/servidor, os clientes são programas que atuam em nome de usuários que precisam de algo feito.
ms.assetid: c3e38cd3-3749-4384-80ff-0551acfe1eec
title: Conceitos básicos de autenticação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d28aa1da3555561740dfd119603a42268ebf86056842788f7dbb1c473fe60e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141309"
---
# <a name="basic-authentication-concepts"></a>Conceitos básicos de autenticação

Em um modelo de aplicativo cliente/servidor, os clientes são programas que atuam em nome de usuários que precisam de algo feito. Isso pode estar abrindo e usando um arquivo, acessando uma caixa de correio, consultando um banco de dados ou imprimindo um documento. Os servidores são programas que fornece serviços para clientes como armazenamento de arquivos, tratamento de email, processamento de consulta e spooling de impressão. Os clientes iniciam a ação, os servidores respondem. Normalmente, um servidor escuta em uma porta de comunicação aguardando que os clientes se conectem e peçam serviço.

No modelo de protocolo Kerberos, todas as conexões de cliente/servidor começam com a autenticação. Por sua vez, cliente e servidor seguem uma sequência de ações que se destinam a verificar em uma ponta da conexão se a outra ponta é verdadeira. Se a autenticação tiver êxito, a configuração da sessão será concluída e uma sessão cliente/servidor segura será estabelecida.

O protocolo Kerberos usa:

-   [Autenticação de chave](key-authentication.md)
-   [Authenticator mensagens](authenticator-messages.md)
-   [Distribuição de chaves](key-distribution.md)
-   [Tíquetes de sessão](session-tickets.md)
-   [Tíquetes de concessão de tíquete](ticket-granting-tickets.md)

 

 



