---
description: Como alternativa ao gerenciamento de partições do Active Directory por meio da ferramenta administrativa Usuários e Computadores do Active Directory, você pode gerenciar partições COM+ programaticamente por meio do uso de um conjunto de objetos COM+ na ADSI (Interface do Sistema do Active Directory).
ms.assetid: 915b4643-cbda-433a-a383-65a6b0fd0874
title: Gerenciando partições no Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87c0aebc9ca52dee005a0343e504756e3e117c3e012098e529fb6d52033428f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070576"
---
# <a name="managing-partitions-within-active-directory"></a>Gerenciando partições no Active Directory

Como alternativa ao gerenciamento de partições do Active Directory por meio da ferramenta administrativa Usuários e Computadores do Active Directory, você pode gerenciar partições COM+ programaticamente por meio do uso de um conjunto de objetos COM+ na ADSI (Interface do Sistema do Active Directory).

Independentemente da técnica administrativa escolhida para gerenciar partições COM+, há uma sequência geral de etapas que os administradores devem seguir:

1.  Crie as novas partições COM+ no Active Directory para seu domínio.
2.  Crie conjuntos de partições COM+ no Active Directory e mapeie-os para suas partições COM+ recém-criadas.
3.  Configure suas partições do Active Directory em seu computador local usando o objeto COM+ apropriado. Quando você configura uma partição do Active Directory em um computador local, uma **pasta Aplicativos COM+** é criada automaticamente nessa pasta de partição.
4.  Instale seus aplicativos COM+ nas partições COM+ apropriadas.

Todas as etapas anteriores podem ser feitas programaticamente, usando um conjunto de interfaces do Active Directory chamada ADSI. Os objetos disponíveis para gerenciar partições que estão disponíveis no ADSI são os exemplos a seguir:

-   DS \_ USERPARTITIONSETLINK \_ NAME
-   DS \_ PARTITIONLINK \_ NAME
-   DS \_ OBJECTID \_ NAME
-   DS \_ DEFAULTPARTITIONLINK \_ NAME
-   NOME DO \_ USERLINK DO DS \_
-   NOME DO \_ PARTITIONSET \_ DS
-   NOME DA \_ PARTIÇÃO \_ DS

Para obter informações sobre como criar e gerenciar partições COM+ por meio do uso das ferramentas administrativas Usuários e Computadores do Active Directory e Serviços de Componentes, consulte a ajuda online disponível de dentro de cada ferramenta.

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

[Definindo direitos administrativos para uma partição](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



