---
description: Os pacotes de autenticação estão contidos em bibliotecas de vínculo dinâmico.
ms.assetid: b0d7bca1-b4bb-4b3f-822e-04a6a500cd9a
title: Pacotes de autenticação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d556489d520ebf45224e3e9b8a5526cc4debcf1c7e7ab95028ecd9e35a6de217
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141359"
---
# <a name="authentication-packages"></a>Pacotes de autenticação

[*Os pacotes de*](/windows/desktop/SecGloss/a-gly) autenticação estão contidos em bibliotecas de vínculo dinâmico. A [*LSA (Autoridade de*](/windows/desktop/SecGloss/l-gly) Segurança Local) carrega pacotes de autenticação usando informações de configuração armazenadas no Registro. Carregar vários pacotes de autenticação permite que o LSA seja suportado por vários processos de logon e vários [*protocolos de segurança.*](/windows/desktop/SecGloss/s-gly)

Os processos de logon usam pacotes de autenticação para analisar dados de logon. Novos processos de logon são adicionados a um sistema adicionando [*um AO PARA*](/windows/desktop/SecGloss/g-gly) coletar os dados de logon necessários e, se necessário, adicionando um novo pacote de autenticação para analisar os dados.

Os protocolos de segurança são implementados por pacotes de autenticação. Um pacote de autenticação analisa os dados de logon seguindo as regras e os procedimentos definidos em um protocolo de segurança.

Os pacotes de autenticação são responsáveis pelas seguintes tarefas:

-   Analisar dados de logon para determinar se uma entidade [*de segurança*](/windows/desktop/SecGloss/s-gly) tem permissão para fazer logon em um sistema.
-   Estabelecer uma nova [*sessão de logon*](/windows/desktop/SecGloss/l-gly) e criar um identificador de [*logon exclusivo*](/windows/desktop/SecGloss/l-gly) para a entidade de segurança autenticada com êxito.
-   Passando informações de segurança para o LSA para o token de segurança da entidade de segurança.

Quando um usuário tenta um logon interativo, o LSA chama um pacote de autenticação para determinar se deve permitir que o usuário faça logon. MSV1 0, por exemplo, é um pacote de autenticação \_ instalado com o sistema operacional Microsoft Windows. O pacote MSV1 \_ 0 aceita um nome de usuário e uma [*senha com hashed.*](/windows/desktop/SecGloss/h-gly) Ele procura o nome de usuário e a combinação de senha com hashed no banco de dados sam (Gerenciador de Contas de Segurança). Se os dados de logon corresponde às credenciais [*armazenadas*](/windows/desktop/SecGloss/c-gly), o pacote de autenticação permite que o logon seja bem-sucedido.

Depois de autenticar com êxito as credenciais de uma entidade de segurança, um pacote de autenticação é responsável por criar uma nova sessão de logon LSA para [*a*](/windows/desktop/SecGloss/s-gly) entidade de segurança e alocar o [*identificador*](/windows/desktop/SecGloss/l-gly) de logon que identifica exclusivamente a sessão de logon. O pacote de autenticação pode associar informações de credencial à sessão de logon para solicitações de autenticação subsequentes. Por exemplo, o pacote de autenticação MSV1 0 (fornecido pela Microsoft) associa o nome da conta de usuário e um hash da senha do usuário a cada sessão \_ de logon.

O pacote de autenticação também fornece um conjunto de SIDs [*(identificadores*](/windows/desktop/SecGloss/s-gly) de segurança) e outras informações apropriadas para inclusão no token de segurança criado pela LSA. Esse token representará o contexto de segurança da [*entidade de segurança*](/windows/desktop/SecGloss/c-gly) para acesso Windows operações.

Depois que uma sessão de logon é criada e associada a uma entidade de segurança, as solicitações de autenticação subsequentes feitas em nome da entidade de segurança são tratadas de forma diferente do logon inicial. O pacote de autenticação não cria uma nova sessão de logon nem retorna informações para a criação de um token. No entanto, o pacote de autenticação pode associar credenciais [*complementares obtidas*](/windows/desktop/SecGloss/s-gly) durante uma autenticação subsequente à sessão de logon existente da entidade de segurança. As credenciais complementares são obtidas quando o acesso a um recurso solicitado requer informações além das credenciais estabelecidas pelo logon inicial. Por exemplo, quando um usuário conectado solicita um logon de rede da Novell, um pacote de autenticação específico da Novell pode ser chamado e as credenciais específicas da Novell podem ser autenticadas e associadas à sessão de logon. Essas credenciais podem ser referenciadas por um redirecionador da Novell (por meio do pacote de autenticação Novell) quando o usuário acessa a rede Novell.

Os tópicos a seguir discutem os vários tipos de [*pacotes de autenticação*](/windows/desktop/SecGloss/a-gly):

-   [Windows Pacotes de autenticação](windows-authentication-packages.md)
-   [Provedor de suporte de segurança/pacotes de autenticação](security-support-provider-authentication-packages.md)
-   [Pacotes de autenticação fornecidos pela Microsoft](authentication-packages-provided-by-microsoft.md)
-   [Pacotes de subauthenticação](subauthentication-packages.md)

 

 
