---
title: Nomes de entidade de entidade
description: Para que um cliente crie uma sessão mutuamente autenticada com um programa de servidor, ele deve fornecer o nome principal esperado do servidor.
ms.assetid: 4d9977f8-0efb-4559-977e-3eba4e277bc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c0ba17916fb9f9c91ac959ea961c19d0f0a03e31d4caa11784dc123b54c5a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927215"
---
# <a name="principal-names"></a>Nomes de entidade de entidade

Para que um cliente crie uma sessão mutuamente autenticada com um programa de servidor, ele deve fornecer o nome principal esperado do servidor. Alguns protocolos, como Kerberos, exigem um nome de entidade de servidor correto para qualquer sessão autenticada. Uma entidade é uma entidade que o sistema de segurança reconhece. Isso inclui usuários humanos, bem como serviços do sistema. Todos os nomes de entidades de segurança têm um formato semelhante para um determinado SSP (provedor de suporte de segurança). Um SSP é um módulo de software que executa a validação de segurança. Para obter mais informações, consulte Visão [geral da arquitetura do SSPI.](sspi-architectural-overview.md) Para manter a uniformidade, um provedor de segurança geralmente fornece aos serviços do sistema nomes semelhantes aos usuários. Em alguns provedores de segurança, os serviços do sistema podem não ter um nome principal.

O servidor registra seu nome principal para o provedor de segurança usando a [**função RpcServerRegisterAuthInfo.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) Somente um nome de entidade de segurança do servidor pode ser usado para cada provedor de segurança. Se mais de um nome for registrado, um nome será escolhido e usado aleatoriamente. O SSP determina o formato do nome da entidade de segurança. Por exemplo, os SSPs Kerberos/Negotiate para um serviço do sistema são aproximadamente parecidos com o seguinte: nome \_ do computador$ @childdomain.parentdomain1.parentdomain2.COM .

O procedimento recomendado para gerar nomes de entidade de segurança é usar APIs documentadas (como a função **DsMakeSpn),** em vez de reunir o nome principal de cadeias de caracteres. O uso de APIs documentadas aumenta a portabilidade entre diferentes ambientes de implantação e elimina a possibilidade de erros.

Especificar um nome principal incorreto pode impedir que o cliente e o servidor estabelecidom uma sessão autenticada. O SSP SCHANNEL assume nomes de entidade de segurança em uma das duas formas:

-   O primeiro formulário de nome principal SCHANNEL é o [*formulário msstd.*](m-glos.md) Os nomes no formato msstd geralmente seguem o padrão msstd:servername@serverdomain.com . Isso é conhecido como uma propriedade de nome de email. Se o certificado contiver uma propriedade de nome de email e contiver o sinal de at (@), o nome principal será msstd:email name. Caso contrário, ele deverá conter a propriedade common name. As reslanças internas são dobradas, assim como em vinculações de cadeia de caracteres.
-   O segundo formulário de nome principal SCHANNEL é [*o formulário completo.*](f-glos.md) Esta é uma série de nomes em conformidade com RFC1779 limitados por colchetes angulares e separados por malhas inde fundo. Normalmente, ele segue o padrão fullsic: \\ < \\ Authority \\ SubAuthority \\ ..... \\ Person> ou fullsic: \\ < \\ Authority \\ SubAuthority \\ ....... \\ ServerProgram>.

Se o nome não corresponder ao certificado, ERROR \_ ACCESS \_ DENIED será retornado. Se o formato de nome for inválido, o SSP SCHANNEL retornará o código ERROR \_ INVALID \_ PARAMETER.

Para consultar o nome principal do servidor, os aplicativos podem chamar [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname). Isso aloca uma cadeia de caracteres terminada em nulo para manter o nome principal. Antes de ser encerrado, seu aplicativo deve invocar [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) para liberar a memória que essa cadeia de caracteres ocupa.

Consultar o nome do servidor dessa maneira não é seguro e deve ser evitado. Para autenticação de servidor, o programa cliente deve saber a qual servidor ele está se conectando e deve criar o nome principal do servidor do zero.

 

 




