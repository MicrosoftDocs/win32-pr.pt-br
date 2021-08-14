---
description: As coleções de administração do COM+ servem para manter e organizar os dados de configuração armazenados no catálogo COM+.
ms.assetid: eed8ca97-39ad-4188-afc6-8670b5073fad
title: Coleções de administração COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc19ff14959c151dc5736fb4a52c5346d0f5a30b6565551aca2f0edb3cee61b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118308433"
---
# <a name="com-administration-collections"></a>Coleções de administração COM+

As coleções de administração do COM+ servem para manter e organizar os dados de configuração armazenados no catálogo COM+. As coleções correspondem às pastas na árvore de console da ferramenta de administração de serviços de componentes. Você pode acessar essas coleções usando os objetos e as interfaces de administração do COM+.

Você inicia a administração programática usando objetos criados a partir da classe [**COMAdminCatalog**](comadmincatalog.md) , você representa todas as coleções no catálogo usando objetos criados a partir da classe [**COMAdminCatalogCollection**](comadmincatalogcollection.md) e representa itens em coleções usando objetos criados a partir da classe [**COMAdminCatalogObject**](comadmincatalogobject.md) .

Os itens em uma determinada coleção expõem um conjunto consistente de propriedades. Por exemplo, cada item na coleção de [**componentes**](components.md) representa um componente e os itens na coleção de **componentes** expõem as mesmas propriedades usadas para configurar um componente. Essas propriedades podem ser acessadas usando a classe [**COMAdminCatalogObject**](comadmincatalogobject.md) .

> [!Note]  
> As propriedades com acesso WriteOnce são ReadWrite ao usar o método [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) antes de usar [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) e são ReadOnly posteriormente.

 

Para obter uma introdução à administração programática do COM+, consulte [automatizando a administração do com+](automating-com--administration.md).

## <a name="collection-hierarchy"></a>Hierarquia de coleção

A figura a seguir ilustra as relações entre as coleções. As coleções na extrema esquerda (em caixas brancas e cinzas) são coleções de nível superior, que são acessadas chamando o método [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) de um objeto criado a partir da classe [**COMAdminCatalog**](comadmincatalog.md) . As coleções restantes (em caixas amarelas) só podem ser acessadas por meio de sua coleção pai, chamando o método [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) que representa seu pai. As setas apontam de uma coleção pai para suas coleções filho.

![Diagrama que mostra as relações entre as coleções.](images/ab61b0ab-2368-4bd8-9cfc-b7adc5beaca3.png)

As quatro coleções a seguir não são ilustradas na figura: [**errorInfo**](errorinfo.md), [**PropertyInfo**](propertyinfo.md), [**RelatedCollectionInfo**](relatedcollectioninfo.md)e [**root**](root.md). A coleção **errorInfo** é um filho de cada coleção na figura, exceto [**InprocServers**](inprocservers.md) e [**WOWInprocServers**](wowinprocservers.md) (em caixas cinzas). As coleções **PropertyInfo** e **RelatedCollectionInfo** são filhas de cada coleção. A coleção **raiz** é uma coleção de nível superior que é o pai de todas as outras coleções de nível superior. No entanto, não é necessário acessar a coleção **raiz** antes de acessar outras coleções de nível superior.

## <a name="comadmin-library"></a>Biblioteca COMAdmin

As coleções a seguir têm suporte na biblioteca COMAdmin.



| Coleção                                                             | Descrição                                                                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplicationCluster**](applicationcluster.md)                       | Contém uma lista dos servidores no cluster de aplicativos.                                                                                            |
| [**ApplicationInstances**](applicationinstances.md)                   | Contém um objeto para cada instância de um aplicativo COM+ em execução.                                                                                   |
| [**Aplicativos**](applications.md)                                   | Contém um objeto para cada aplicativo COM+ instalado no computador local.                                                                         |
| [**Componentes**](components.md)                                       | Contém um objeto para cada componente no aplicativo ao qual ele está relacionado.                                                                      |
| [**Computerlist**](computerlist.md)                                   | Contém uma lista dos computadores encontrados na pasta **computadores** da ferramenta de administração de serviços de componentes.                                     |
| [**DCOMProtocols**](dcomprotocols.md)                                 | Contém uma lista dos protocolos a serem usados pelo DCOM. Ele contém um objeto para cada protocolo.                                                         |
| [**ErrorInfo**](errorinfo.md)                                         | Recupera informações de erro estendidas referentes a métodos que lidam com vários objetos.                                                               |
| [**EventClassesForIID**](eventclassesforiid.md)                       | Recupera informações sobre classes de evento.                                                                                                        |
| [**FilesForImport**](filesforimport.md)                               | Recupera informações de seu arquivo MSI sobre um aplicativo que pode ser importado.                                                                    |
| [**InprocServers**](inprocservers.md)                                 | Contém uma lista dos servidores em processo registrados no sistema. Ele contém um objeto para cada componente.                                       |
| [**InterfacesForComponent**](interfacesforcomponent.md)               | Contém um objeto para cada interface exposta pelo componente ao qual a coleção está relacionada.                                                    |
| [**LegacyComponents**](legacycomponents.md)                           | Contém um objeto para cada componente não configurado no aplicativo ao qual ele está relacionado.                                                         |
| [**LegacyServers**](legacyservers.md)                                 | Idêntico à coleção [**InprocServers**](inprocservers.md) , exceto que essa coleção também inclui servidores locais.                           |
| [**LocalComputer**](localcomputer.md)                                 | Contém um único objeto que contém informações de configurações de nível de computador para o computador cujo catálogo você está acessando.                             |
| [**MethodsForInterface**](methodsforinterface.md)                     | Contém um objeto para cada método na interface à qual a coleção está relacionada.                                                               |
| [**Partições**](partitions.md)                                       | Usado para especificar os aplicativos contidos em cada partição.                                                                                         |
| [**PartitionUsers**](partitionusers.md)                               | Usado para especificar os usuários contidos em cada partição.                                                                                                |
| [**PropertyInfo**](propertyinfo.md)                                   | Recupera informações sobre as propriedades com suporte de uma coleção especificada.                                                                      |
| [**Editorproperties**](publisherproperties.md)                     | Contém um objeto para cada propriedade do Publicador da coleção [**SubscriptionsForComponent**](subscriptionsforcomponent.md) pai.              |
| [**RelatedCollectionInfo**](relatedcollectioninfo.md)                 | Recupera informações sobre outras coleções relacionadas à coleção da qual ela é chamada.                                                      |
| [**Funções**](roles.md)                                                 | Contém um objeto para cada função atribuída ao aplicativo ao qual ele está relacionado.                                                                  |
| [**RolesForComponent**](rolesforcomponent.md)                         | Contém um objeto para cada função atribuída ao componente ao qual a coleção está relacionada.                                                        |
| [**RolesForInterface**](rolesforinterface.md)                         | Contém um objeto para cada função atribuída à interface à qual a coleção está relacionada.                                                        |
| [**RolesForMethod**](rolesformethod.md)                               | Contém um objeto para cada função atribuída ao método ao qual a coleção está relacionada.                                                           |
| [**RolesForPartition**](rolesforpartition.md)                         | Contém um objeto para cada função atribuída à partição à qual a coleção está relacionada.                                                        |
| [**Básica**](root.md)                                                   | Contém as coleções de nível superior no catálogo.                                                                                                    |
| [**Assinantes**](subscriberproperties.md)                   | Contém um objeto para cada propriedade de assinante para a coleção [**SubscriptionsForComponent**](subscriptionsforcomponent.md) pai.             |
| [**SubscriptionsForComponent**](subscriptionsforcomponent.md)         | Contém um objeto para cada assinatura para a coleção de [**componentes**](components.md) pai.                                                  |
| [**TransientPublisherProperties**](transientpublisherproperties.md)   | Contém um objeto para cada propriedade do Publicador da coleção [**TransientSubscriptions**](transientsubscriptions.md) pai.                    |
| [**TransientSubscriberProperties**](transientsubscriberproperties.md) | Contém um objeto para cada propriedade de assinante para a coleção [**TransientSubscriptions**](transientsubscriptions.md) pai.                   |
| [**TransientSubscriptions**](transientsubscriptions.md)               | Contém um objeto para cada assinatura transitória.                                                                                                   |
| [**UsersInPartitionRole**](usersinpartitionrole.md)                   | Contém um objeto para cada usuário na função de partição à qual a coleção está relacionada.                                                            |
| [**UsersInRole**](usersinrole.md)                                     | Contém um objeto para cada usuário na função ao qual a coleção está relacionada.                                                                      |
| [**WOWInprocServers**](wowinprocservers.md)                           | Contém uma lista dos servidores em processo registrados com o sistema para componentes de 32 bits em computadores de 64 bits.                                       |
| [**WOWLegacyServers**](wowlegacyservers.md)                           | Idêntico à coleção [**LegacyServers**](legacyservers.md) , exceto que essa coleção é desenhada do registro de 32 bits em computadores de 64 bits. |



 

 

 



