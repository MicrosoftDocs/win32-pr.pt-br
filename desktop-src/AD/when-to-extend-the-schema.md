---
title: Quando estender o esquema
description: Estenda o esquema somente se nenhuma classe de objeto existente atender aos requisitos do seu aplicativo. Estender o esquema é uma operação complexa; as alterações de esquema são replicadas para cada controlador de domínio na floresta da empresa. Considere isso com cuidado.
ms.assetid: 92231f31-d2af-4c3b-981e-e55cc478899d
ms.tgt_platform: multiple
keywords:
- Quando estender o AD do esquema
- AD do esquema, quando estender
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18c182b346fd1e31bc549325260d9b57d75bbb63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105755906"
---
# <a name="when-to-extend-the-schema"></a>Quando estender o esquema

Estenda o esquema somente se nenhuma classe de objeto existente atender aos requisitos do seu aplicativo. Estender o esquema é uma operação complexa; as alterações de esquema são replicadas para cada controlador de domínio na floresta da empresa. Considere isso com cuidado.

O esquema pode ser estendido de três maneiras:

-   Derive uma nova subclasse de uma classe existente-a subclasse tem todos os atributos da superclasse e todos os atributos que você especificar. Derive de uma classe existente:
    -   Quando a classe existente requer atributos adicionais, mas, caso contrário, é aceitável.
    -   Quando a capacidade de transformar objetos existentes da classe em uma nova classe não é necessária. Não é possível adicionar uma subclasse a um objeto existente.
    -   Para usar o snap-in Gerenciador de diretórios existente para gerenciar os atributos estendidos dos objetos.
-   Adicione atributos a uma classe existente e/ou adicione objetos pai para a classe. Ao adicionar vários atributos, execute essa operação de maneira estruturada definindo uma classe auxiliar e adicionando essa classe auxiliar à classe existente.
-   A modificação de uma classe existente é necessária quando um aplicativo requer a capacidade de estender objetos existentes da classe. Por exemplo, para adicionar dados específicos do aplicativo ao objeto de usuário, estenda o usuário da classe normalmente, pois você deve lidar com usuários existentes e não apenas usuários especiais criados pelo seu aplicativo.
-   Crie uma nova classe com os atributos necessários. Criar uma nova classe; ou seja, uma classe derivada de "Top" quando nenhuma classe existente atende aos requisitos operacionais.

Quando você criar uma subclasse de uma classe existente, todos os itens da interface do usuário associados à classe original não serão herdados pela subclasse. Por exemplo, se você subclasse de um objeto de usuário, as páginas de propriedades e os itens de menu associados ao usuário não serão herdados. Por esse motivo, é preferível estender um objeto existente ou criar uma classe auxiliar em vez de criar uma subclasse.

Se você criar uma classe existente ou modificar uma classe existente, você desejará estender ferramentas como o snap-in Active Directory usuários e computadores para gerenciar os atributos estendidos dos objetos. Para obter mais informações, consulte [estendendo a interface do usuário para objetos de diretório](extending-the-user-interface-for-directory-objects.md).

 

 




