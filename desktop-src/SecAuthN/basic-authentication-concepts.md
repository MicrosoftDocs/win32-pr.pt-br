---
description: Em um modelo de aplicativo cliente/servidor, os clientes são programas que atuam em nome dos usuários que precisam de algo feito.
ms.assetid: c3e38cd3-3749-4384-80ff-0551acfe1eec
title: Conceitos básicos de autenticação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723cf42913906435c8dbc3c41950da8db8ece0ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091011"
---
# <a name="basic-authentication-concepts"></a>Conceitos básicos de autenticação

Em um modelo de aplicativo cliente/servidor, os clientes são programas que atuam em nome dos usuários que precisam de algo feito. Isso pode estar abrindo e usando um arquivo, acessando uma caixa de correio, consultando um banco de dados ou imprimindo um documento. Os servidores são programas que fornecem serviços para clientes como armazenamento de arquivos, manipulação de email, processamento de consultas e spool de impressão. Os clientes iniciam a ação, os servidores respondem. Normalmente, um servidor escuta em uma porta de comunicações aguardando que os clientes se conectem e solicitem serviço.

No modelo de protocolo Kerberos, todas as conexões de cliente/servidor começam com a autenticação. Por sua vez, cliente e servidor seguem uma sequência de ações que se destinam a verificar em uma ponta da conexão se a outra ponta é verdadeira. Se a autenticação tiver êxito, a configuração da sessão será concluída e uma sessão cliente/servidor segura será estabelecida.

O protocolo Kerberos usa:

-   [Autenticação de chave](key-authentication.md)
-   [Mensagens do autenticador](authenticator-messages.md)
-   [Distribuição de chaves](key-distribution.md)
-   [Tíquetes de sessão](session-tickets.md)
-   [Tíquetes de concessão de tíquetes](ticket-granting-tickets.md)

 

 



