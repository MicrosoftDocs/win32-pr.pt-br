---
title: Proteção de objeto e atributo
description: Uma ACL (lista de controle de acesso) protege todos os objetos no Active Directory Domain Services.
ms.assetid: 64ac1f88-57d6-4821-bd17-f7ef1004922c
ms.tgt_platform: multiple
keywords:
- Proteção de objeto e atributo
- proteção de AD, objeto e atributo de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7798ca1498c3a8ffe58bf43117dfd8ae249d234115f551c636628ad5b811e04a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025610"
---
# <a name="object-and-attribute-protection"></a>Proteção de objeto e atributo

Uma ACL (lista de controle de acesso) protege todos os objetos no Active Directory Domain Services. As ACLs determinam quem pode exibir o objeto, quais atributos eles podem ler e quais ações cada usuário pode executar no objeto. A existência de um objeto ou de um atributo nunca é revelada a um usuário não autorizado.

Uma ACL é uma lista de ACEs (entradas de controle de acesso) armazenadas com o objeto que ele protege. em Windows NT e Windows 2000, uma ACL é armazenada como um valor binário, chamado de descritor de segurança. Cada ACE contém um SID (identificador de segurança), que identifica a entidade (usuário ou grupo) a quem a ACE se aplica e os dados sobre o tipo de acesso que a ACE concede ou nega.

As ACLs para objetos de diretório contêm ACEs que se aplicam ao objeto como um todo e as ACEs que se aplicam aos atributos individuais do objeto. Isso permite que um administrador controle não apenas quais usuários podem ver um objeto, mas também quais propriedades esses usuários podem exibir. Por exemplo, todos os usuários podem receber acesso de leitura aos atributos email e número de telefone para todos os outros usuários, mas as propriedades de segurança de usuários podem ser negadas a todos, exceto a membros de um grupo de administradores de segurança especial. Os usuários individuais podem receber acesso de gravação a atributos pessoais, como o telefone e os endereços de email em seus próprios objetos de usuário.

 

 




