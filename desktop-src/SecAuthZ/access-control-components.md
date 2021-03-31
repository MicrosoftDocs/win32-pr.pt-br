---
description: Explica as partes do modelo de controle de acesso.
ms.assetid: cca78195-90f5-45ee-9d16-c445d87e9f5e
title: Partes do modelo de controle de acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3aa6d3547d486c33f4b31cdb5d5de24c7d27cec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828018"
---
# <a name="parts-of-the-access-control-model"></a>Partes do modelo de controle de acesso

Há duas partes básicas do modelo de controle de acesso:

-   [Tokens de acesso](access-tokens.md), que contêm informações sobre um usuário conectado
-   [Descritores de segurança](security-descriptors.md), que contêm as informações de segurança que protegem um [objeto protegível](securable-objects.md)

Quando um usuário faz logon, o sistema [*autentica*](/windows/desktop/SecGloss/a-gly) o nome da conta e a senha do usuário. Se o logon for bem-sucedido, o sistema criará um token de acesso. Cada [*processo*](/windows/desktop/SecGloss/p-gly) executado em nome desse usuário terá uma cópia desse token de acesso. O token de acesso contém [identificadores de segurança](security-identifiers.md) que identificam a conta do usuário e as contas de grupo às quais o usuário pertence. O token também contém uma lista dos [privilégios](privileges.md) mantidos pelo usuário ou pelos grupos do usuário. O sistema usa esse token para identificar o usuário associado quando um processo tenta acessar um objeto protegível ou executar uma tarefa de administração do sistema que exige privilégios.

Quando um objeto protegível é criado, o sistema atribui a ele um [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) que contém informações de segurança especificadas por seu criador ou informações de segurança padrão se nenhuma for especificada. Os aplicativos podem usar funções para recuperar e definir as informações de segurança de um objeto existente.

Um descritor de segurança identifica o proprietário do objeto e também pode conter as seguintes [listas de controle de acesso](access-control-lists.md):

-   Uma DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) que identifica os usuários e grupos com permissão ou acesso negado ao objeto
-   Uma SACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/s-gly) ) do sistema que controla como o sistema [audita](audit-generation.md) tentativas de acessar o objeto

Uma ACL contém uma lista de ACEs ( [entradas de controle de acesso](access-control-entries.md) ). Cada ACE especifica um conjunto de [direitos de acesso](access-rights-and-access-masks.md) e contém um SID que identifica um grupo de [confiança](trustees.md) para o qual os direitos são permitidos, negados ou auditados. Um confiável pode ser uma conta de usuário, uma conta de grupo ou uma [*sessão de logon*](/windows/desktop/SecGloss/l-gly).

Use funções para manipular o conteúdo de descritores de segurança, SIDs e ACLs em vez de acessá-los diretamente. Isso ajuda a garantir que essas estruturas permaneçam sintaticamente precisas e impede que futuros aprimoramentos no sistema de segurança quebrem o código existente.

Os tópicos a seguir fornecem informações sobre partes do modelo de controle de acesso:

-   [Tokens de acesso](access-tokens.md)
-   [Descritores de segurança](security-descriptors.md)
-   [Listas de controle de acesso](access-control-lists.md)
-   [Entradas de controle de acesso](access-control-entries.md)
-   [Direitos de acesso e máscaras de acesso](access-rights-and-access-masks.md)
-   [Como a AccessCheck funciona](how-dacls-control-access-to-an-object.md)
-   [Política de autorização centralizada](centralized-authorization-policy.md)
-   [Identificadores de segurança](security-identifiers.md)

 

 
