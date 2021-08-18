---
description: Explica as partes do modelo de controle de acesso.
ms.assetid: cca78195-90f5-45ee-9d16-c445d87e9f5e
title: Partes do modelo de controle de acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bffdbf6542a9e29360437c50f47495d83467334e09c7aa55e8a136a8fc7556d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785666"
---
# <a name="parts-of-the-access-control-model"></a>Partes do modelo de controle de acesso

Há duas partes básicas do modelo de controle de acesso:

-   [Tokens de acesso](access-tokens.md), que contêm informações sobre um usuário conectado
-   [Descritores de segurança](security-descriptors.md), que contêm as informações de segurança que protegem um [objeto protegível](securable-objects.md)

Quando um usuário faz o login, o [*sistema autentica o*](/windows/desktop/SecGloss/a-gly) nome e a senha da conta do usuário. Se o logon for bem-sucedido, o sistema criará um token de acesso. Cada [*processo*](/windows/desktop/SecGloss/p-gly) executado em nome desse usuário terá uma cópia desse token de acesso. O token de acesso contém [identificadores de segurança](security-identifiers.md) que identificam a conta do usuário e todas as contas de grupo às quais o usuário pertence. O token também contém uma lista dos [privilégios mantidos](privileges.md) pelo usuário ou pelos grupos do usuário. O sistema usa esse token para identificar o usuário associado quando um processo tenta acessar um objeto de segurança ou executar uma tarefa de administração do sistema que requer privilégios.

Quando um objeto seguro é criado, o sistema atribui a ele um descritor de segurança que contém informações [*de*](/windows/desktop/SecGloss/s-gly) segurança especificadas por seu criador ou informações de segurança padrão se nenhuma for especificada. Os aplicativos podem usar funções para recuperar e definir as informações de segurança para um objeto existente.

Um descritor de segurança identifica o proprietário do objeto e também pode conter as seguintes listas [de controle de acesso:](access-control-lists.md)

-   Uma [*DACL (lista de*](/windows/desktop/SecGloss/d-gly) controle de acesso discricionário) que identifica os usuários e grupos que permitiram ou negaram acesso ao objeto
-   Uma [*SACL (lista de*](/windows/desktop/SecGloss/s-gly) controle de acesso do sistema) que controla como o [sistema audita](audit-generation.md) tentativas de acessar o objeto

Uma ACL contém uma lista de ACEs (entradas de controle [de](access-control-entries.md) acesso). Cada ACE especifica um [](access-rights-and-access-masks.md) conjunto de direitos de acesso [](trustees.md) e contém um SID que identifica um usuário confiável para o qual os direitos são permitidos, negados ou auditados. Um usuário confiável pode ser uma conta de usuário, uma conta de grupo ou uma [*sessão de logon.*](/windows/desktop/SecGloss/l-gly)

Use funções para manipular o conteúdo de descritores de segurança, SIDs e ACLs em vez de acessá-los diretamente. Isso ajuda a garantir que essas estruturas permaneçam sintaticamente precisas e impeça que aprimoramentos futuros para o sistema de segurança quebrando o código existente.

Os tópicos a seguir fornecem informações sobre partes do modelo de controle de acesso:

-   [Tokens de acesso](access-tokens.md)
-   [Descritores de segurança](security-descriptors.md)
-   [Listas de controle de acesso](access-control-lists.md)
-   [Entradas de controle de acesso](access-control-entries.md)
-   [Direitos de acesso e máscaras de acesso](access-rights-and-access-masks.md)
-   [Como o AccessCheck funciona](how-dacls-control-access-to-an-object.md)
-   [Política de autorização centralizada](centralized-authorization-policy.md)
-   [Identificadores de segurança](security-identifiers.md)

 

 
