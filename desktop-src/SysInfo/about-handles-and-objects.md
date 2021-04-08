---
description: O sistema usa objetos e identificadores para regular o acesso aos recursos do sistema por dois motivos principais.
ms.assetid: 122acb9e-2a1b-480b-9207-5cc6bbe6b6d4
title: Sobre identificadores e objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c7474c11298166cc8d63032c6e1d8f84e6db249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921834"
---
# <a name="about-handles-and-objects"></a>Sobre identificadores e objetos

O sistema usa objetos e identificadores para regular o acesso aos recursos do sistema por dois motivos principais. Primeiro, o uso de objetos garante que a Microsoft possa atualizar a funcionalidade do sistema, desde que a interface do objeto original seja mantida. Quando as versões subsequentes do sistema são liberadas, você pode usar o objeto atualizado com pouco ou nenhum trabalho adicional.

Em segundo lugar, o uso de objetos permite que você aproveite a segurança do Windows. Cada objeto tem sua própria lista de controle de acesso (ACL) que especifica as ações que um processo pode executar no objeto. O sistema examina a ACL de um objeto cada vez que um aplicativo cria um identificador para o objeto. Para mais informações, consulte [Controle de acesso](/windows/desktop/SecAuthZ/access-control).

-   [Gerenciador de objetos](object-manager.md)
-   [Interface de objeto](object-interface.md)
-   [Namespaces de objeto](/windows/desktop/Sync/object-namespaces)
-   [Limitações de identificador](handle-limitations.md)
-   [Manipular herança](handle-inheritance.md)

 

 
