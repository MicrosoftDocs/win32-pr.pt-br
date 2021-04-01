---
description: Para obter mais informações sobre o diagrama a seguir, consulte a legenda do diagrama de relação de entidade.
ms.assetid: ec4f585d-cbd5-4c25-aaf4-1c1333fd4587
title: Grupo de tabelas principais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a5cc87e80c60505025825353272699db574bd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922625"
---
# <a name="core-tables-group"></a>Grupo de tabelas principais

Para obter mais informações sobre o diagrama a seguir, consulte a [legenda do diagrama de relação de entidade](entity-relationship-diagram-legend.md).

![grupo de tabelas principais](images/core.png)

O grupo principal consiste em tabelas que descrevem os recursos fundamentais e os componentes do aplicativo e o pacote do instalador. Os desenvolvedores de instalar pacotes devem, portanto, considerar como preencher essas tabelas primeiro, pois a organização de grande parte do banco de dados ficará aparente com o conteúdo desse grupo.

-   A [tabela de recursos](feature-table.md) lista todos os recursos que pertencem ao aplicativo.
-   A [tabela de condição](condition-table.md) contém as expressões condicionais que determinam se um determinado recurso será instalado ou não.
-   A [tabela FeatureComponents](featurecomponents-table.md) descreve quais componentes pertencem a cada recurso.
-   A [tabela de componentes](component-table.md) lista todos os componentes que pertencem à instalação.
-   A [tabela de diretórios](directory-table.md) lista os diretórios que são necessários durante a instalação. Como cada componente deve ser associado a um e apenas um diretório, a tabela de componentes está diretamente relacionada a essa tabela e tem uma chave externa para a tabela de diretórios.
-   A [tabela PublishComponent](publishcomponent-table.md) lista os recursos e componentes que são publicados para uso por outros aplicativos. [Componentes e recursos](components-and-features.md) são os dois tipos de anúncio de recursos.
-   A [tabela MsiAssembly](msiassembly-table.md) Especifica configurações de Windows Installer para assemblies de Common Language Runtime de .NET Framework e assemblies do Win32.
-   A [tabela MsiAssemblyName](msiassemblyname-table.md) especifica o esquema para os elementos de um nome de cache de assembly forte para um assembly Common Language Runtime ou Win32.
-   A [tabela ComPlus](complus-table.md) contém as informações necessárias para instalar aplicativos com+.
-   A [tabela IsolatedComponent](isolatedcomponent-table.md) associa o componente especificado na \_ coluna aplicativo de componente (normalmente um. exe) com o componente especificado na \_ coluna compartilhada componente (normalmente, uma DLL compartilhada).
-   A [tabela de atualização](upgrade-table.md) contém as informações necessárias durante as [atualizações principais](major-upgrades.md).

 

 



