---
description: O sistema usa objetos e alças para regular o acesso aos recursos do sistema por dois motivos principais.
ms.assetid: 122acb9e-2a1b-480b-9207-5cc6bbe6b6d4
title: Sobre alças e objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eee99e0568a0535462e89bfd5de71e12cfaf4a588a605f190dba41ce0ef2535
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117959044"
---
# <a name="about-handles-and-objects"></a>Sobre alças e objetos

O sistema usa objetos e alças para regular o acesso aos recursos do sistema por dois motivos principais. Primeiro, o uso de objetos garante que a Microsoft possa atualizar a funcionalidade do sistema, desde que a interface do objeto original seja mantida. Quando as versões subsequentes do sistema são lançadas, você pode usar o objeto atualizado com pouco ou nenhum trabalho adicional.

Em segundo lugar, o uso de objetos permite que você aproveite a Windows segurança. Cada objeto tem sua própria ACL (lista de controle de acesso) que especifica as ações que um processo pode executar no objeto . O sistema examina a ACL de um objeto sempre que um aplicativo cria um identificador para o objeto . Para mais informações, consulte [Controle de acesso](/windows/desktop/SecAuthZ/access-control).

-   [Gerenciador de Objetos](object-manager.md)
-   [Interface de objeto](object-interface.md)
-   [Namespaces de objeto](/windows/desktop/Sync/object-namespaces)
-   [Limitações do handle](handle-limitations.md)
-   [Manipular herança](handle-inheritance.md)

 

 
