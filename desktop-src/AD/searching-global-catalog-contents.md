---
title: Pesquisando o catálogo global
description: Active Directory Domain Services também tem um GC (catálogo global), que contém uma réplica parcial de todos os objetos no diretório.
ms.assetid: 83970563-1a56-4671-b264-56e29939e369
ms.tgt_platform: multiple
keywords:
- pesquisando o catálogo global Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a057330309c12df6d18a209fc3d2adaf42b03005
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634921"
---
# <a name="searching-the-global-catalog"></a>Pesquisando o catálogo global

Active Directory Domain Services também tem um GC (catálogo global), que contém uma réplica parcial de todos os objetos no diretório. Ele também contém réplicas parciais dos contêineres de esquema e configuração. Um ou mais controladores de domínio em um domínio podem armazenar uma cópia do catálogo global. Para obter mais informações sobre como associar a um catálogo global, consulte [associação ao catálogo global](binding-to-the-global-catalog.md).

O catálogo global mantém uma réplica de cada objeto em Active Directory Domain Services, mas com apenas um pequeno número de seus atributos. Os atributos no catálogo global são aqueles usados com mais frequência em operações de pesquisa, como nomes e sobrenome de um usuário, nomes de logon e assim por diante. Os atributos do catálogo global também incluem aqueles necessários para localizar uma réplica completa do objeto. O catálogo global permite que os usuários localizem objetos de interesse rapidamente sem saber qual domínio os contém e sem exigir um namespace estendido contíguo na empresa; ou seja, você pode pesquisar toda a floresta.

Portanto, se você associar a um objeto no catálogo global, pesquisará esse objeto e toda a hierarquia abaixo dele — sem precisar ir para nenhum outro servidor. No entanto, a pesquisa só pode usar um filtro de consulta que contém propriedades no catálogo global e pode recuperar somente propriedades no catálogo global.

Pesquisar o catálogo global tem os seguintes benefícios:

-   O catálogo global permite Pesquisar toda a floresta ou qualquer parte da floresta, bem como os contêineres de esquema e configuração.
-   O catálogo global permite que você execute uma pesquisa completa em um único servidor. Nenhuma referência ou caça de referência é necessária.

Pesquisar o catálogo global tem as seguintes desvantagens:

-   O catálogo global contém um pequeno subconjunto das propriedades em cada objeto. Se o filtro de consulta incluir propriedades que não estão no catálogo global, a consulta avaliará as expressões que contêm essas propriedades como false. Se você especificar propriedades de catálogo não globais na lista de propriedades a serem retornadas, essas propriedades não serão recuperadas.
-   Para pesquisar o catálogo global, um controlador de domínio que contém um catálogo global deve estar disponível. Se um não estiver disponível, você não poderá executar uma pesquisa de catálogo global.
-   O catálogo global é somente leitura. Isso significa que você não pode associar a um objeto no catálogo global para criar, modificar ou excluir objetos.

 

 




