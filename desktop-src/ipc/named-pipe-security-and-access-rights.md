---
description: Você pode especificar um descritor de segurança para um pipe nomeado ao chamar a função CreateNamedPipe. O descritor de segurança controla o acesso às extremidades do cliente e do servidor do pipe nomeado.
ms.assetid: f9ea97c9-9a97-4083-82d8-29ffb8be5a77
title: Segurança de pipe nomeado e direitos de acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11cada606d8197ac2f64943aa742bbfd614fa4ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750516"
---
# <a name="named-pipe-security-and-access-rights"></a>Segurança de pipe nomeado e direitos de acesso

A segurança do Windows permite que você controle o acesso a pipes nomeados. Para obter mais informações sobre segurança, consulte [modelo de controle de acesso](/windows/desktop/SecAuthZ/access-control-model).

Você pode especificar um [descritor de segurança](/windows/desktop/SecAuthZ/security-descriptors) para um pipe nomeado ao chamar a função [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) . O descritor de segurança controla o acesso às extremidades do cliente e do servidor do pipe nomeado. Se você especificar **NULL**, o pipe nomeado obterá um descritor de segurança padrão. As ACLs no descritor de segurança padrão para um pipe nomeado concedem controle total à conta LocalSystem, aos administradores e ao proprietário criador. Eles também concedem acesso de leitura aos membros do grupo todos e à conta anônima.

Para recuperar o descritor de segurança de um pipe nomeado, chame a função [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) . Para alterar o descritor de segurança de um pipe nomeado, chame a função [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .

Quando um thread chama [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) para abrir um identificador para a extremidade do servidor de um pipe nomeado existente, o sistema executa uma verificação de acesso antes de retornar o identificador. A verificação de acesso compara o token de acesso do thread e os [direitos de acesso](/windows/desktop/SecAuthZ/access-rights-and-access-masks) solicitados com relação à DACL no descritor de segurança do pipe nomeado. Além dos direitos de acesso solicitados, a DACL deve permitir que o arquivo de thread de chamada \_ crie \_ \_ acesso à instância de pipe para o pipe nomeado.

Da mesma forma, quando um cliente chama a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) ou [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) para se conectar à extremidade do cliente de um pipe nomeado, o sistema executa uma verificação de acesso antes de conceder acesso ao cliente.

O identificador retornado pela função [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) sempre tem o acesso de sincronização. Ele também tem \_ leitura genérica, \_ gravação genérica ou ambas, dependendo do modo aberto do pipe. A seguir estão os direitos de acesso para cada modo aberto.



| Modo de abertura                           | Direitos de acesso                                              |
|-------------------------------------|------------------------------------------------------------|
| \_ \_ Duplex de acesso de pipe (0x00000003)   | ARQUIVO \_ \_ de leitura genérica, \_ gravação genérica de arquivo \_ e sincronização |
| \_ \_ Entrada de acesso de pipe (0x00000001)  | \_ \_ Leitura e sincronização genérica de arquivo                        |
| \_ \_ Saída de acesso de pipe (0x00000002) | \_ \_ Gravação e sincronização genérica de arquivo                       |



 

\_ \_ O acesso de leitura genérico de arquivo para um pipe nomeado combina os direitos de leitura de dados do pipe, leitura de atributos de pipe, leitura de atributos estendidos e leitura da DACL do pipe.

\_ \_ O acesso de gravação genérico de arquivo para um pipe nomeado combina os direitos de gravar dados no pipe, acrescentar dados a ele, gravar atributos de pipe, gravar atributos estendidos e ler a DACL do pipe. Como \_ \_ \_ a instância do pipe de criação de arquivos e dados de anexação \_ \_ de arquivo tem a mesma definição, a \_ gravação genérica de arquivo habilita a \_ permissão para criar o pipe. Para evitar esse problema, use os direitos individuais em vez de usar a \_ gravação genérica de arquivo \_ .

Você pode solicitar o direito de acesso de segurança do sistema de acesso \_ \_ a um objeto de pipe nomeado se desejar ler ou gravar a SACL do objeto. Para obter mais informações, consulte [listas de controle de acesso (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) e [direito de acesso SACL](/windows/desktop/SecAuthZ/sacl-access-right).

Para impedir que usuários ou usuários remotos em uma sessão de serviços de terminal diferente acessem um pipe nomeado, use o SID de logon na DACL do pipe. O SID de logon também é usado em logons executar como; é o SID usado para proteger o namespace de objeto por sessão. Para obter mais informações, consulte [obtendo o Sid de logon em C++](/previous-versions//aa446670(v=vs.85)).

 

 
