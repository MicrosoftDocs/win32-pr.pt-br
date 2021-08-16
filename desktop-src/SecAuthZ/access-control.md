---
description: Controle de acesso refere-se a recursos de segurança que controlam quem pode acessar recursos no sistema operacional. Os aplicativos chamam funções de controle de acesso para definir quem pode acessar recursos específicos ou controlar o acesso aos recursos fornecidos pelo aplicativo.
ms.assetid: d9ce4ec5-5c09-4b33-93a1-39638a925986
title: Controle de acesso (autorização)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b34be93577446066fcaf7e01e634c60632c68c430198a375eadc2efbcec3e701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785636"
---
# <a name="access-control-authorization"></a>Controle de acesso (autorização)

Controle de acesso refere-se a recursos de segurança que controlam quem pode acessar recursos no sistema operacional. Os aplicativos chamam funções de controle de acesso para definir quem pode acessar recursos específicos ou controlar o acesso aos recursos fornecidos pelo aplicativo.

Esta visão geral descreve o modelo de segurança para controlar o acesso a objetos Windows, como arquivos, e para controlar o acesso a funções administrativas, como definir a hora do sistema ou auditar as ações do usuário. O [tópico Modelo de Controle de](access-control-model.md) Acesso fornece uma descrição de alto nível das partes do controle de acesso e como elas interagem entre si.

Os tópicos a seguir descrevem o controle de acesso:

-   [Segurança no nível C2](c2-level-security.md)
-   [Modelo de controle de acesso](access-control-model.md)
-   [Linguagem de definição do descritor de segurança](security-descriptor-definition-language.md)
-   [Privilégios](privileges.md)
-   [Geração de auditoria](audit-generation.md)
-   [Objetos que podem sercuráveis](securable-objects.md)
-   [Controle de acesso de baixo nível](low-level-access-control.md)

A seguir estão as tarefas comuns de controle de acesso:

-   [Como as DACLs controlam o acesso a um objeto](how-dacls-control-access-to-an-object.md)
-   [Controlando a criação de objeto filho em C++](controlling-child-object-creation-in-c--.md)
-   [ACEs para controlar o acesso às propriedades de um objeto](aces-to-control-access-to-an-object-s-properties.md)
-   [Solicitando direitos de acesso a um objeto](requesting-access-rights-to-an-object.md)

Os tópicos a seguir fornecem código de exemplo para tarefas de controle de acesso:

-   [Modificando as ACLs de um objeto em C++](modifying-the-acls-of-an-object-in-c--.md)
-   [Criando um descritor de segurança para um novo objeto em C++](creating-a-security-descriptor-for-a-new-object-in-c--.md)
-   [Controlando a criação de objeto filho em C++](controlling-child-object-creation-in-c--.md)
-   [Habilitando e desabilitando privilégios em C++](enabling-and-disabling-privileges-in-c--.md)
-   [Procurando um SID em um token de acesso em C++](searching-for-a-sid-in-an-access-token-in-c--.md)
-   [Localizar o proprietário de um objeto de arquivo em C++](finding-the-owner-of-a-file-object-in-c--.md)
-   [Assumindo a propriedade do objeto em C++](taking-object-ownership-in-c--.md)
-   [Criando uma DACL](/windows/desktop/SecBP/creating-a-dacl)

 

 
