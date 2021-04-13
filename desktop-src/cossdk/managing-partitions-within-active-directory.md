---
description: Como alternativa ao gerenciamento de partições Active Directory por meio da ferramenta administrativa usuários e computadores Active Directory, você pode gerenciar partições COM+ programaticamente por meio do uso de um conjunto de objetos COM+ na ADSI (interface do sistema do Active Directory).
ms.assetid: 915b4643-cbda-433a-a383-65a6b0fd0874
title: Gerenciando partições no Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6635e49b7d2833a1e6e177c25f9f2fb05ff0dff4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501081"
---
# <a name="managing-partitions-within-active-directory"></a>Gerenciando partições no Active Directory

Como alternativa ao gerenciamento de partições Active Directory por meio da ferramenta administrativa usuários e computadores Active Directory, você pode gerenciar partições COM+ programaticamente por meio do uso de um conjunto de objetos COM+ na ADSI (interface do sistema do Active Directory).

Independentemente da técnica administrativa que você escolher para gerenciar partições COM+, há uma sequência geral de etapas que os administradores devem seguir:

1.  Crie as novas partições COM+ dentro de Active Directory para seu domínio.
2.  Crie conjuntos de partições COM+ dentro de Active Directory e mapeie-os para suas partições COM+ recém-criadas.
3.  Configure suas partições de Active Directory no computador local, usando o objeto COM+ apropriado. Quando você configura uma partição de Active Directory em um computador local, uma pasta de **aplicativos com+** é criada automaticamente nessa pasta de partição.
4.  Instale seus aplicativos COM+ nas partições COM+ apropriadas.

Todas as etapas anteriores podem ser feitas programaticamente, usando um conjunto de interfaces Active Directory chamado ADSI. Os objetos disponíveis para o gerenciamento de partições que estão disponíveis no ADSI são os seguintes:

-   \_nome do USERPARTITIONSETLINK DS \_
-   \_nome do PARTITIONLINK DS \_
-   \_nome do OBJECTID DS \_
-   \_nome do DEFAULTPARTITIONLINK DS \_
-   \_nome do USERlink do DS \_
-   \_nome do particionado DS \_
-   \_nome da partição DS \_

Para obter informações sobre como criar e gerenciar partições COM+ por meio do uso do Active Directory usuários e computadores e ferramentas administrativas de serviços de componentes, consulte a ajuda online disponível em cada ferramenta.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Coletando métricas de partição](collecting-partition-metrics.md)
</dt> <dt>

[Configurando o cache de partição](configuring-the-partition-cache.md)
</dt> <dt>

[Agrupando aplicativos em partições](grouping-applications-into-partitions.md)
</dt> <dt>

[Gerenciando partições locais](managing-local-partitions.md)
</dt> <dt>

[Configurando direitos administrativos para uma partição](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



