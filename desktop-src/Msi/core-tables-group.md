---
description: Para obter mais informações sobre o diagrama a seguir, consulte a legenda do diagrama de relação de entidade.
ms.assetid: ec4f585d-cbd5-4c25-aaf4-1c1333fd4587
title: Grupo de Tabelas Principais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a8704a13e71f019e3d0686384057d3f209de06530c97bda6f0a63ff352d4db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948531"
---
# <a name="core-tables-group"></a>Grupo de Tabelas Principais

Para obter mais informações sobre o diagrama a seguir, consulte a legenda [do diagrama de relação de entidade](entity-relationship-diagram-legend.md).

![grupo de tabelas principais](images/core.png)

O grupo principal consiste em tabelas que descrevem os recursos e componentes fundamentais do aplicativo e do pacote do instalador. Portanto, os desenvolvedores de pacotes de instalação devem considerar como preencher essas tabelas primeiro porque a organização de grande parte do banco de dados se tornará aparente com base no conteúdo desse grupo.

-   A [tabela Recurso lista](feature-table.md) todos os recursos que pertencem ao aplicativo.
-   A [tabela Condição](condition-table.md) contém as expressões condicionais que determinam se um recurso específico será instalado ou não.
-   A [tabela FeatureComponents descreve](featurecomponents-table.md) quais componentes pertencem a cada recurso.
-   A [tabela Componente](component-table.md) lista todos os componentes que pertencem à instalação.
-   A [tabela Diretório](directory-table.md) lista os diretórios necessários durante a instalação. Como cada componente deve ser associado a um e apenas um diretório, a tabela Component está intimamente relacionada a essa tabela e tem uma chave externa para a tabela Directory.
-   A [tabela PublishComponent lista](publishcomponent-table.md) os recursos e componentes publicados para uso por outros aplicativos. [Componentes e recursos](components-and-features.md) são os dois tipos de anúncio de recurso.
-   A [tabela MsiAssembly](msiassembly-table.md) especifica Windows do Instalador para .NET Framework assemblies do Common Language Runtime e assemblies win32.
-   A [tabela MsiAssemblyName](msiassemblyname-table.md) especifica o esquema para os elementos de um nome de cache de assembly forte para um common language runtime ou assembly Win32.
-   A [tabela Complus contém](complus-table.md) as informações necessárias para instalar aplicativos COM+.
-   A [tabela IsolatedComponent](isolatedcomponent-table.md) associa o componente especificado na coluna Aplicativo de Componente (normalmente um .exe) ao componente especificado na coluna Componente Compartilhado (normalmente uma \_ \_ DLL compartilhada).
-   A [tabela Upgrade](upgrade-table.md) contém as informações necessárias durante as [atualizações principais.](major-upgrades.md)

 

 



