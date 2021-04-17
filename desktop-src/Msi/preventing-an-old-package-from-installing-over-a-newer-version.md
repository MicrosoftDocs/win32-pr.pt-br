---
description: Windows Installer pacotes de atualização podem ser criados para que as principais atualizações não sejam instaladas se um usuário já tiver uma versão mais recente instalada.
ms.assetid: f46e82bd-70b3-46a2-8246-a1eadfdc589d
title: Impedir que um pacote antigo seja instalado em uma versão mais recente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320ab062c4ffbc740d85c59ece3d3baaa63f4209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748975"
---
# <a name="preventing-an-old-package-from-installing-over-a-newer-version"></a>Impedindo que um pacote antigo seja instalado em uma versão mais recente

Windows Installer pacotes de atualização podem ser criados para que as principais atualizações não sejam instaladas se um usuário já tiver uma versão mais recente instalada. O procedimento neste tópico só pode impedir downgrades que podem ser causados pela execução de um pacote de atualização principal. Esse procedimento depende da [ação FindRelatedProducts](findrelatedproducts-action.md), que é executada apenas durante uma instalação inicial e não é executada no modo de manutenção (reinstalação). Como as atualizações secundárias são executadas usando a reinstalação, esse procedimento não pode ser usado para determinar se um pacote de atualização secundário está tentando fazer downgrade de um aplicativo. Para obter mais informações, consulte [preparando um aplicativo para futuras atualizações importantes](preparing-an-application-for-future-major-upgrades.md).

**Para impedir que um pacote antigo seja instalado em uma versão mais recente**

1.  Insira a propriedade [**UpgradeCode**](upgradecode.md) para o grupo de produtos relacionados que podem estar qualificados para receber essa atualização na coluna UpgradeCode da tabela de [atualização](upgrade-table.md).
2.  Insira o sinalizador de bit **msidbUpgradeAttributesOnlyDetect** na coluna atributos da [tabela de atualização](upgrade-table.md).
3.  Insira a versão da atualização fornecida por esse pacote na coluna VersionMin da [tabela de atualização](upgrade-table.md). Deixe a coluna VersionMax em branco.
4.  Insira o nome da propriedade que deve ser definida pela [ação FindRelatedProducts](findrelatedproducts-action.md) na coluna actionproperty da [tabela de atualização](upgrade-table.md).
5.  Adicione a propriedade [**SecureCustomProperties**](securecustomproperties.md) e a propriedade chamada na coluna actionproperty da tabela de [atualização](upgrade-table.md) à tabela de [Propriedades](property-table.md).
6.  Adicione um [tipo de ação personalizada 19](custom-action-type-19.md) após a ação FindRelatedProducts na [tabela InstallExecuteSequence](installexecutesequence-table.md). Inclua um registro na [tabela CustomAction](customaction-table.md) para esta ação e insira o texto a ser exibido na coluna de destino. A ação personalizada Type 19 é criada no instalador, portanto, não há nenhum código a ser escrito.
7.  Insira o nome da Actionproperty na coluna Condition do registro na [tabela InstallExecuteSequence](installexecutesequence-table.md) que contém o [tipo de ação personalizada 19](custom-action-type-19.md). Isso faz com que a ação personalizada seja executada somente quando a [tabela de atualização](upgrade-table.md) detectar que uma versão mais recente já está instalada.

    Por exemplo, um pacote Windows Installer que atualiza um grupo de produtos relacionados à versão 3,0 pode incluir os seguintes registros em suas tabelas de [Propriedade](property-table.md) , [CustomAction](customaction-table.md), [InstallExecuteSequence](installexecutesequence-table.md)e de [atualização](upgrade-table.md). Todos os produtos relacionados no grupo têm o mesmo UpgradeCode, mas o instalador não instala esse pacote de atualização se uma versão posterior à 3,0 já estiver instalada no computador. Nesse caso, o instalador apresenta uma mensagem de erro e a instalação falha. O pacote de atualização da versão 3,0 é instalado nas versões 1,0 e 2,0.

    [Atualizar tabela](upgrade-table.md)

    

    | UpgradeCode                            | VersionMin | VersionMax | Idioma | Atributos                                | Remover | Açãoproperty  |
    |----------------------------------------|------------|------------|----------|-------------------------------------------|--------|-----------------|
    | {E7BE6D45-49FF-4701-A17E-BDCC98CE180D} | 3.0        |            |          | msidbUpgradeAttributesOnlyDetect          |        | NEWPRODUCTFOUND |
    | {E7BE6D45-49FF-4701-A17E-BDCC98CE180D} | 1.0        | 3.0        |          | msidbUpgradeAttributesVersionMinInclusive |        | UPGRADEFOUND    |

    

     

    [Tabela CustomAction](customaction-table.md)

    

    | Ação | Tipo | Fonte | Destino                                 |
    |--------|------|--------|----------------------------------------|
    | CA1    | 19   |        | Uma atualização mais alta já está instalada. |

    

     

    [Tabela InstallExecuteSequence](installexecutesequence-table.md)

    

    | Ação              | Condição       | Sequência |
    |---------------------|-----------------|----------|
    | FindRelatedProducts |                 | 200      |
    | CA1                 | NEWPRODUCTFOUND | 201      |

    

     

    [Tabela de propriedades](property-table.md)

    

    | Propriedade                                                 | Valor                        |
    |----------------------------------------------------------|------------------------------|
    | [**SecureCustomProperties**](securecustomproperties.md) | NEWPRODUCTFOUND; UPGRADEFOUND |

    

     

 

 



