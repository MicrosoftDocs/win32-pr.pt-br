---
description: Você pode especificar um descritor de segurança para um pipe nomeado ao chamar a função CreateNamedPipe. O descritor de segurança controla o acesso às extremidades do cliente e do servidor do pipe nomeado.
ms.assetid: f9ea97c9-9a97-4083-82d8-29ffb8be5a77
title: Segurança de pipe nomeado e direitos de acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 556987cf35845de249bf0e19f3a0b481aab18e891c3b6211f26eb51571704d7b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451206"
---
# <a name="named-pipe-security-and-access-rights"></a>Segurança de pipe nomeado e direitos de acesso

Windows segurança permite controlar o acesso a pipes nomeados. Para obter mais informações sobre segurança, consulte [Modelo de controle de acesso.](/windows/desktop/SecAuthZ/access-control-model)

Você pode especificar um [descritor de segurança para](/windows/desktop/SecAuthZ/security-descriptors) um pipe nomeado ao chamar a [**função CreateNamedPipe.**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) O descritor de segurança controla o acesso às extremidades do cliente e do servidor do pipe nomeado. Se você especificar **NULL,** o pipe nomeado obtém um descritor de segurança padrão. As ACLs no descritor de segurança padrão para um pipe nomeado concedem controle total à conta LocalSystem, aos administradores e ao proprietário do criador. Eles também concedem acesso de leitura aos membros do grupo Todos e à conta anônima.

Para recuperar o descritor de segurança de um pipe nomeado, chame a [**função GetSecurityInfo.**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) Para alterar o descritor de segurança de um pipe nomeado, chame a [**função SetSecurityInfo.**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)

Quando um thread chama [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) para abrir um identificador para a extremidade do servidor de um pipe nomeado existente, o sistema executa uma verificação de acesso antes de retornar o identificador. A verificação de acesso compara o token de [](/windows/desktop/SecAuthZ/access-rights-and-access-masks) acesso do thread e os direitos de acesso solicitados em relação à DACL no descritor de segurança do pipe nomeado. Além dos direitos de acesso solicitados, a DACL deve permitir que o thread de chamada \_ FILE CREATE PIPE INSTANCE acesse o pipe \_ \_ nomeado.

Da mesma forma, quando um cliente chama a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) ou [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) para se conectar ao final do cliente de um pipe nomeado, o sistema executa uma verificação de acesso antes de conceder acesso ao cliente.

O identificador retornado pela [**função CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) sempre tem acesso SYNCHRONIZE. Ele também tem LEITURA \_ GENÉRICA, GRAVAÇÃO GENÉRICA ou \_ ambos, dependendo do modo aberto do pipe. A seguir estão os direitos de acesso para cada modo aberto.



| Modo aberto                           | Direitos de acesso                                              |
|-------------------------------------|------------------------------------------------------------|
| PIPE \_ ACCESS \_ DUPLEX (0x00000003)   | LEITURA \_ \_ GENÉRICA DE ARQUIVO, \_ GRAVAÇÃO \_ GENÉRICA DE ARQUIVO e SINCRONIZAÇÃO |
| PIPE \_ ACCESS \_ INBOUND (0x00000001)  | FILE \_ GENERIC \_ READ and SYNCHRONIZE                        |
| PIPE \_ ACCESS \_ OUTBOUND (0x00000002) | FILE \_ GENERIC \_ WRITE and SYNCHRONIZE                       |



 

O acesso FILE GENERIC READ para um pipe nomeado combina os direitos para ler dados do pipe, ler atributos de pipe, ler atributos estendidos e ler \_ \_ a DACL do pipe.

O acesso FILE GENERIC WRITE para um pipe nomeado combina os direitos para gravar dados no pipe, anexar dados a ele, gravar atributos de pipe, gravar atributos estendidos e ler a DACL do \_ \_ pipe. Como FILE APPEND DATA e FILE CREATE PIPE INSTANCE têm a mesma definição, o FILE GENERIC WRITE permite a permissão \_ \_ para criar o \_ \_ \_ \_ \_ pipe. Para evitar esse problema, use os direitos individuais em vez de usar FILE \_ GENERIC \_ WRITE.

Você pode solicitar o direito de acesso ACCESS SYSTEM SECURITY a um objeto de pipe nomeado se quiser ler ou gravar a \_ \_ SACL do objeto. Para obter mais informações, consulte [ACLs (Listas de Controle](/windows/desktop/SecAuthZ/access-control-lists) de Acesso) e [Direito de Acesso SACL.](/windows/desktop/SecAuthZ/sacl-access-right)

Para impedir que usuários remotos ou usuários em uma sessão de serviços de terminal diferentes acessem um pipe nomeado, use o SID de logon na DACL para o pipe. O SID de logon também é usado em logons executar como; é o SID usado para proteger o namespace de objeto por sessão. Para obter mais informações, consulte [Getting the Logon SID in C++.](/previous-versions//aa446670(v=vs.85))

 

 
