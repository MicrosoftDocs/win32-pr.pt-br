---
description: O controle de acesso refere-se aos recursos de segurança que controlam quem pode acessar recursos no sistema operacional. Os aplicativos chamam funções de controle de acesso para definir quem pode acessar recursos específicos ou controlar o acesso aos recursos fornecidos pelo aplicativo.
ms.assetid: d9ce4ec5-5c09-4b33-93a1-39638a925986
title: Controle de acesso (autorização)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31c0198f0ce0de77750e0587d9b54c1e20cee756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010898"
---
# <a name="access-control-authorization"></a>Controle de acesso (autorização)

O controle de acesso refere-se aos recursos de segurança que controlam quem pode acessar recursos no sistema operacional. Os aplicativos chamam funções de controle de acesso para definir quem pode acessar recursos específicos ou controlar o acesso aos recursos fornecidos pelo aplicativo.

Esta visão geral descreve o modelo de segurança para controlar o acesso a objetos do Windows, como arquivos, e para controlar o acesso a funções administrativas, como definir a hora do sistema ou as ações do usuário de auditoria. O tópico [modelo de controle de acesso](access-control-model.md) fornece uma descrição de alto nível das partes do controle de acesso e como elas interagem entre si.

Os tópicos a seguir descrevem o controle de acesso:

-   [Segurança em nível C2](c2-level-security.md)
-   [Modelo de controle de acesso](access-control-model.md)
-   [Linguagem de definição do descritor de segurança](security-descriptor-definition-language.md)
-   [Direitos](privileges.md)
-   [Geração de auditoria](audit-generation.md)
-   [Objetos protegíveis](securable-objects.md)
-   [Controle de acesso de baixo nível](low-level-access-control.md)

A seguir estão as tarefas comuns de controle de acesso:

-   [Como as DACLs controlam o acesso a um objeto](how-dacls-control-access-to-an-object.md)
-   [Controlando a criação de objetos filho em C++](controlling-child-object-creation-in-c--.md)
-   [ACEs para controlar o acesso às propriedades de um objeto](aces-to-control-access-to-an-object-s-properties.md)
-   [Solicitando direitos de acesso a um objeto](requesting-access-rights-to-an-object.md)

Os tópicos a seguir fornecem código de exemplo para tarefas de controle de acesso:

-   [Modificando as ACLs de um objeto em C++](modifying-the-acls-of-an-object-in-c--.md)
-   [Criando um descritor de segurança para um novo objeto em C++](creating-a-security-descriptor-for-a-new-object-in-c--.md)
-   [Controlando a criação de objetos filho em C++](controlling-child-object-creation-in-c--.md)
-   [Habilitando e desabilitando privilégios em C++](enabling-and-disabling-privileges-in-c--.md)
-   [Pesquisando um SID em um token de acesso em C++](searching-for-a-sid-in-an-access-token-in-c--.md)
-   [Localizando o proprietário de um objeto de arquivo em C++](finding-the-owner-of-a-file-object-in-c--.md)
-   [Tirando a propriedade do objeto em C++](taking-object-ownership-in-c--.md)
-   [Criando uma DACL](/windows/desktop/SecBP/creating-a-dacl)

 

 
