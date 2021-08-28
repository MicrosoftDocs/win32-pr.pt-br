---
title: Quando estender o esquema
description: Estenda o esquema somente se nenhuma classe de objeto existente atender aos requisitos do seu aplicativo. Estender o esquema é uma operação complexa; As alterações de esquema são replicadas para todos os controladores de domínio na floresta corporativa. Considere isso com cuidado.
ms.assetid: 92231f31-d2af-4c3b-981e-e55cc478899d
ms.tgt_platform: multiple
keywords:
- Quando estender o AD de esquema
- schema AD , quando estender
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 042665069b06804dd648798debca6e0cee5628e115f5f512718ea0a51cc765ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024324"
---
# <a name="when-to-extend-the-schema"></a>Quando estender o esquema

Estenda o esquema somente se nenhuma classe de objeto existente atender aos requisitos do seu aplicativo. Estender o esquema é uma operação complexa; As alterações de esquema são replicadas para todos os controladores de domínio na floresta corporativa. Considere isso com cuidado.

O esquema pode ser estendido de três maneiras:

-   Derivar uma nova subclasse de uma classe existente – a subclasse tem todos os atributos da superclasse e todos os atributos que você especificar. Derivar de uma classe existente:
    -   Quando a classe existente requer atributos adicionais, mas caso contrário, é aceitável.
    -   Quando a capacidade de transformar objetos existentes da classe em uma nova classe não é necessária. Não é possível adicionar uma subclasse a um objeto existente.
    -   Para usar o snap-in do Gerenciador de Diretórios existente para gerenciar os atributos estendidos dos objetos.
-   Adicione atributos a uma classe existente e/ou adicione objetos pai para a classe . Ao adicionar vários atributos, execute essa operação de maneira estruturada definindo uma classe auxiliar e adicionando essa classe auxiliar à classe existente.
-   A modificação de uma classe existente é necessária quando um aplicativo exige a capacidade de estender objetos existentes da classe . Por exemplo, para adicionar dados específicos do aplicativo ao objeto Usuário, estenda a classe Usuário normalmente, pois você deve lidar com usuários existentes e não apenas usuários especiais criados pelo seu aplicativo.
-   Crie uma nova classe com os atributos necessários. Criar uma nova classe; ou seja, uma classe derivada de "Top" quando nenhuma classe existente atende aos requisitos operacionais.

Quando você subclasse uma classe existente, todos os itens de interface do usuário associados à classe original não serão herdados pela subclasse. Por exemplo, se você subclassificar um objeto de usuário, as páginas de propriedades e os itens de menu associados ao usuário não serão herdados. Por esse motivo, é preferível estender um objeto existente ou criar uma classe auxiliar em vez de criar uma subclasse.

Quer você subclasse uma classe existente ou modifique uma classe existente, você deseja estender ferramentas como o snap-in Usuários e Computadores do Active Directory para gerenciar os atributos estendidos dos objetos. Para obter mais informações, consulte [Estendendo o Interface do Usuário para objetos de diretório](extending-the-user-interface-for-directory-objects.md).

 

 




