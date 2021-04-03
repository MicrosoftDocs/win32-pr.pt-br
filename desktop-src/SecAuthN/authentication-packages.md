---
description: Os pacotes de autenticação estão contidos em bibliotecas de vínculo dinâmico.
ms.assetid: b0d7bca1-b4bb-4b3f-822e-04a6a500cd9a
title: Pacotes de autenticação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff02017b653521d80741bcdf3c205ab924c4bceb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828840"
---
# <a name="authentication-packages"></a>Pacotes de autenticação

Os [*pacotes de autenticação*](/windows/desktop/SecGloss/a-gly) estão contidos em bibliotecas de vínculo dinâmico. A [*autoridade de segurança local*](/windows/desktop/SecGloss/l-gly) (LSA) carrega pacotes de autenticação usando as informações de configuração armazenadas no registro. O carregamento de vários pacotes de autenticação permite que a LSA ofereça suporte a vários processos de logon e a vários [*protocolos de segurança*](/windows/desktop/SecGloss/s-gly).

Os processos de logon usam pacotes de autenticação para analisar dados de logon. Novos processos de logon são adicionados a um sistema adicionando uma [*Gina*](/windows/desktop/SecGloss/g-gly) para coletar os dados de logon necessários e, se necessário, adicionando um novo pacote de autenticação para analisar os dados.

Os protocolos de segurança são implementados por pacotes de autenticação. Um pacote de autenticação analisa os dados de logon seguindo as regras e os procedimentos estabelecidos em um protocolo de segurança.

Os pacotes de autenticação são responsáveis pelas seguintes tarefas:

-   Analisar dados de logon para determinar se uma [*entidade de segurança*](/windows/desktop/SecGloss/s-gly) tem permissão para fazer logon em um sistema.
-   Estabelecendo uma nova [*sessão de logon*](/windows/desktop/SecGloss/l-gly) e criando um identificador de [*logon*](/windows/desktop/SecGloss/l-gly) exclusivo para a entidade de segurança autenticada com êxito.
-   Passando informações de segurança para o LSA para o token de segurança da entidade.

Quando um usuário tenta um logon interativo, o LSA chama um pacote de autenticação para determinar se deve permitir que o usuário faça logon. MSV1 \_ 0, por exemplo, é um pacote de autenticação instalado com o sistema operacional Microsoft Windows. O \_ pacote MSV1 0 aceita um nome de usuário e uma senha de [*hash*](/windows/desktop/SecGloss/h-gly) . Ele pesquisa a combinação de nome de usuário e senha com hash no banco de dados SAM (Gerenciador de contas de segurança). Se os dados de logon corresponderem às [*credenciais*](/windows/desktop/SecGloss/c-gly)armazenadas, o pacote de autenticação permitirá que o logon tenha sucesso.

Depois de autenticar com êxito as credenciais de uma [*entidade de segurança*](/windows/desktop/SecGloss/s-gly) , um pacote de autenticação é responsável por criar uma nova sessão de logon LSA para a entidade e alocar o [*identificador de logon*](/windows/desktop/SecGloss/l-gly) que identifica exclusivamente a sessão de logon. O pacote de autenticação pode associar informações de credenciais com a sessão de logon para solicitações de autenticação subsequentes. Por exemplo, o \_ pacote de autenticação MSV1 0 (fornecido pela Microsoft) associa o nome da conta de usuário e um hash da senha do usuário a cada sessão de logon.

O pacote de autenticação também fornece um conjunto de SIDs ( [*identificadores de segurança*](/windows/desktop/SecGloss/s-gly) ) e outras informações apropriadas para inclusão no token de segurança criado pela LSA. Esse token representará o [*contexto*](/windows/desktop/SecGloss/c-gly) de segurança da entidade para acesso às operações do Windows.

Depois que uma sessão de logon é criada e associada a uma entidade de segurança, as solicitações de autenticação subsequentes feitas em nome da entidade de segurança são tratadas de forma diferente do logon inicial. O pacote de autenticação não cria uma nova sessão de logon nem retorna informações para a criação de um token. No entanto, o pacote de autenticação pode associar [*as credenciais complementares*](/windows/desktop/SecGloss/s-gly) obtidas durante uma autenticação subsequente com a sessão de logon existente da entidade de segurança. As credenciais complementares são obtidas quando o acesso a um recurso solicitado requer informações além das credenciais estabelecidas pelo logon inicial. Por exemplo, quando um usuário conectado solicita um logon de rede Novell, um pacote de autenticação específico do Novell pode ser chamado e as credenciais específicas do Novell podem ser autenticadas e associadas à sessão de logon. Essas credenciais podem ser referenciadas por um redirecionador Novell (por meio do pacote de autenticação Novell) quando o usuário acessa a rede Novell.

Os tópicos a seguir abordam os vários tipos de [*pacotes de autenticação*](/windows/desktop/SecGloss/a-gly):

-   [Pacotes de autenticação do Windows](windows-authentication-packages.md)
-   [Provedor de suporte de segurança/pacotes de autenticação](security-support-provider-authentication-packages.md)
-   [Pacotes de autenticação fornecidos pela Microsoft](authentication-packages-provided-by-microsoft.md)
-   [Pacotes de subautenticação](subauthentication-packages.md)

 

 
