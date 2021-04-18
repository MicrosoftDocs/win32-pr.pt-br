---
description: Cada recurso de Windows Installer usa um ou mais componentes do Windows Installer, e os recursos podem compartilhar componentes.
ms.assetid: 7ab4b359-e729-4ca5-8ef3-fa8e988be6da
title: Especificando relações de Feature-Component
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05ff15f4c735ac7d081c16f49f1aafe555a96db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770177"
---
# <a name="specifying-feature-component-relationships"></a>Especificando relações de Feature-Component

Cada [recurso de Windows Installer](windows-installer-features.md) usa um ou mais [componentes do Windows Installer](windows-installer-components.md), e os recursos podem compartilhar componentes. A [tabela FeatureComponents](featurecomponents-table.md) define a relação entre recursos e componentes. Consulte o [grupo de tabelas principais](core-tables-group.md) e os [componentes e recursos](components-and-features.md) no Windows Installer visão geral. Nesta seção, você adiciona informações à tabela FeatureComponents do exemplo do bloco de notas.

Use o editor de banco de dados para abrir MNP2000.msi e insira os dados a seguir na tabela FeatureComponents vazia.

[Tabela FeatureComponents](featurecomponents-table.md)



| Recurso\_ | Componente\_ |
|-----------|-------------|
| Beisebol  | Beisebol    |
| Concerto   | Concerto     |
| Dance     | Dance       |
| Comemorar  | Comemorar    |
| Ajuda      | Ajuda        |
| Janeiro   | Janeiro     |
| NewYears  | NewYears    |
| Bloco de notas   | Bloco de notas     |
| Leiame    | Bloco de notas     |



 

[Continuar](adding-registry-information.md)

 

 



