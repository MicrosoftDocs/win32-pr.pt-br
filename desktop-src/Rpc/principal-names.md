---
title: Nomes de entidade
description: Para que um cliente crie uma sessão mutuamente autenticada com um programa de servidor, ele deve fornecer o nome principal esperado do servidor.
ms.assetid: 4d9977f8-0efb-4559-977e-3eba4e277bc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 554ffecff6eb019b4712e6b2d9f5c6319db492e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453698"
---
# <a name="principal-names"></a>Nomes de entidade

Para que um cliente crie uma sessão mutuamente autenticada com um programa de servidor, ele deve fornecer o nome principal esperado do servidor. Alguns protocolos, como o Kerberos, exigem um nome principal de servidor correto para qualquer sessão autenticada. Um principal é uma entidade que o sistema de segurança reconhece. Isso inclui usuários humanos, bem como serviços do sistema. Todos os nomes de entidade usam um formato semelhante para um determinado SSP (provedor de suporte de segurança). Um SSP é um módulo de software que executa a validação de segurança. Para obter mais informações, consulte [visão geral da arquitetura SSPI](sspi-architectural-overview.md). Para manter a uniformidade, um provedor de segurança geralmente fornece nomes semelhantes aos serviços do sistema como usuários. Em alguns provedores de segurança, os serviços do sistema podem não ter um nome principal.

O servidor registra seu nome principal para o provedor de segurança usando a função [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) . Somente um nome principal de servidor pode ser usado para cada provedor de segurança. Se mais de um nome for registrado, um nome será escolhido e usado aleatoriamente. O SSP determina o formato do nome principal. Por exemplo, o Kerberos/negociar SSPs para um serviço do sistema é semelhante ao seguinte: nome do computador \_ $ @childdomain.parentdomain1.parentdomain2.COM .

O procedimento recomendado para gerar nomes de entidade de segurança é usar APIs documentadas (como a função **DsMakeSpn** ), em vez de compondo juntos o nome da entidade de segurança de cadeias de caracteres. O uso de APIs documentadas aumenta a portabilidade entre diferentes ambientes de implantação e elimina a possibilidade de erros.

Especificar um nome de entidade incorreto pode impedir que o cliente e o servidor estabeleçam uma sessão autenticada. O SSP do SCHANNEL usa os nomes principais em uma das duas formas:

-   O primeiro formulário do nome principal do SCHANNEL é o formulário [*msstd*](m-glos.md) . Os nomes no formulário msstd geralmente seguem o padrão msstd:servername@serverdomain.com . Isso é conhecido como uma propriedade de nome de email. Se o certificado contiver uma propriedade de nome de email e contiver o sinal de arroba (@), o nome da entidade será msstd: nome de email. Caso contrário, ele deve conter a propriedade nome comum. As barras invertidas internas são duplicadas, assim como nas associações de cadeia de caracteres.
-   O segundo formulário de nome principal de SCHANNEL é o formulário [*fullsic*](f-glos.md) . Esta é uma série de nomes em conformidade com RFC1779 limitados por colchetes angulares e separados por barras invertidas. Normalmente, segue o padrão fullsic: \\ < \\ Authority \\ subauthority \\ . \\ ... Pessoa> ou fullsic: \\ < \\ autoridade de certificação \\ .. \\ .. \\> ServerProgram.

Se o nome não corresponder ao certificado, o \_ acesso \_ negado ao erro será retornado. Se o formato de nome for inválido, o SSP do SCHANNEL retornará o parâmetro de erro de código \_ inválido \_ .

Para consultar o nome principal do servidor, os aplicativos podem chamar [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname). Isso aloca uma cadeia de caracteres terminada em nulo para conter o nome da entidade de segurança. Antes de ser encerrado, seu aplicativo deve invocar [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) para liberar a memória ocupada por essa cadeia de caracteres.

Consultar o nome do servidor dessa maneira não é seguro e deve ser evitado. Para a autenticação de servidor, o programa cliente deve saber a qual servidor ele está se conectando e deve criar o nome principal do servidor do zero.

 

 




