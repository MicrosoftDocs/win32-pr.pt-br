---
title: Delegação
description: A delegação é um dos recursos de segurança mais importantes do Active Directory Domain Services.
ms.assetid: ab8740c9-f5a2-40cc-abce-0ef80c3fca7a
ms.tgt_platform: multiple
keywords:
- ANÚNCIO de delegação
- ANÚNCIO de segurança, delegação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e1f48b851aa17abb9f9823e0b4cf32e845786b29d31e45daa4c9965ce60aef8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118019783"
---
# <a name="delegation"></a>Delegação

A *delegação* é um dos recursos de segurança mais importantes do Active Directory Domain Services. A delegação permite que uma autoridade administrativa mais alta Conceda direitos administrativos específicos para contêineres e subárvores a indivíduos e grupos. Os administradores de domínio, com autoridade ampla sobre grandes segmentos de usuários, não são mais necessários.

Uma ACE pode conceder direitos administrativos específicos para os objetos em um contêiner para um usuário ou grupo. São concedidos direitos para operações específicas em classes de objetos específicas usando ACEs na ACL do contêiner. Por exemplo, para habilitar um usuário chamado "usuário 1" para ser um administrador da unidade organizacional "contabilidade corporativa", adicione ACEs à ACL em "contabilidade corporativa" da seguinte maneira:

"usuário 1"; Conceder Criar, modificar, excluir; usuário de classe de objeto "usuário 1"; Conceder Criar, modificar, excluir; grupo de classes de objeto "usuário 1"; Conceder Write; usuário de classe de objeto; Senha do atributo "

Agora, o usuário 1 pode criar novos usuários e grupos em contabilidade corporativa e definir as senhas em usuários existentes, mas o usuário 1 não pode criar nenhuma outra classe de objeto e não pode afetar os usuários em nenhum outro contêiner, a menos que, é claro, o usuário 1 receba esse acesso por ACEs nos outros contêineres.

 

 




