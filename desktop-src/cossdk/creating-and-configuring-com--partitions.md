---
description: Os administradores podem usar o COM+ para criar e configurar programaticamente partições COM+.
ms.assetid: 15f0cd9a-cd40-49df-85b8-15c4e626f8ee
title: Criando e configurando partições COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf654c25c75cc2e12f55b7ee826184fdeb04a214
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500927"
---
# <a name="creating-and-configuring-com-partitions"></a>Criando e configurando partições COM+

Os administradores podem usar o COM+ para criar e configurar programaticamente partições COM+. Na verdade, todas as tarefas de criação e configuração que um administrador pode fazer nos serviços de componentes ou nas ferramentas administrativas de usuários e computadores Active Directory podem ser feitas usando coleções, objetos e interfaces COM+ ou por meio da interface do sistema de Active Directory (ADSI).

**Windows XP:** A capacidade de criar, configurar ou delegar partições COM+ não está disponível. A partição global é a única partição COM+ disponível.

* * Windows 2000: * * o serviço de partições COM+ não está disponível no Windows 2000.

> [!Note]  
> O serviço de partições COM+ não está habilitado por padrão. Para usar o serviço de partições COM+, você deve habilitá-lo por meio da ferramenta de administração de serviços de componentes ou alterando a propriedade PartitionsEnabled na coleção [**LocalComputer**](localcomputer.md) para true.

 

Para realizar tarefas relacionadas à partição, o COM+ fornece os seguintes elementos de programação:

-   Métodos e propriedades da interface [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) na classe [**COMAdminCatalog**](comadmincatalog.md) :
    -   Propriedade [**CurrentPartition**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-put_currentpartition) .
    -   Propriedade [**CurrentPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionid) .
    -   Propriedade [**CurrentPartitionName**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_currentpartitionname) .
    -   Método [**FlushPartitionCache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) .
    -   Método [**Getparticionaid**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionid) .
    -   Método [**Getparticionaname**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-getpartitionname) .
    -   Propriedade [**GlobalPartitionID**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-get_globalpartitionid) .
-   Um conjunto de objetos COM+ para criar e gerenciar partições no Active Directory.
-   Uma chave do registro do COM+, **PartitionCache**, para alterar o tamanho do cache da partição.
-   Um conjunto de [coleções de administração com+](com--administration-collections.md)relacionadas a partições:
    -   Coleção de [**partições**](partitions.md) .
    -   Coleção [**PartitionUsers**](partitionusers.md) .
    -   Coleção [**RolesForPartition**](rolesforpartition.md) .
    -   Coleção [**UsersInPartitionRole**](usersinpartitionrole.md) .
-   Propriedades de outras [coleções de administração do com+](com--administration-collections.md):
    -   Propriedade PartitionID na coleção [**ApplicationInstances**](applicationinstances.md) .
    -   Propriedade AppPartitionID na coleção de [**aplicativos**](applications.md) .
    -   Propriedades PartitionDescription, PartitionID e PartitionName na coleção [**FilesForImport**](filesforimport.md) .
    -   Propriedades DSPartitionLookupEnabled, LocalPartitionLookupEnabled e PartitionsEnabled na coleção [**LocalComputer**](localcomputer.md) .
    -   Propriedades EventClassPartitionID e SubscriberPartitionID na coleção [**SubscriptionsForComponent**](subscriptionsforcomponent.md) .
    -   Propriedades EventClassPartitionID e SubscriberPartitionID na coleção [**TransientSubscriptions**](transientsubscriptions.md) .

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

[Gerenciando partições no Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Configurando direitos administrativos para uma partição](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



