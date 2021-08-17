---
description: No processamento de um backup no VSS, os solicitantes e os gravadores trabalharam juntos para produzir uma imagem de sistema estável da qual fazer backup dos dados, o que exigia a coordenação e a criação de uma cópia de sombra do sistema atual.
ms.assetid: 1cefb6ac-f2bb-464b-a62f-05be91ae56f7
title: Visão geral do processamento de uma restauração no VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b01094a02b823f372271f14c04801820407573b9351bfe7e2fc2ad9dc74077
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117937954"
---
# <a name="overview-of-processing-a-restore-under-vss"></a>Visão geral do processamento de uma restauração no VSS

No processamento de um backup no VSS, os solicitantes e os gravadores trabalharam juntos para produzir uma imagem de sistema estável da qual fazer backup dos dados, o que exigia a coordenação e a criação de uma cópia de sombra do sistema atual.

Ao contrário de um backup do VSS, onde a finalidade da coordenação do solicitante e dos gravadores é produzir uma imagem do sistema estável da qual os dados serão copiados, o objetivo de uma restauração baseada em VSS é retornar arquivos para o disco de maneira mais útil para os aplicativos (gravadores) em execução no sistema. Isso não requer uma imagem de sistema estável, portanto, nenhuma cópia de sombra é necessária.

Em vez disso, a atenção está concentrada em evitar a interrupção da atividade do gravador, impedindo a criação de conjuntos de dados inconsistentes em disco e permitindo que os gravadores o escopo necessário avaliem e mesclem os dados quando necessário.

Como uma operação de backup, uma restauração do VSS requer acesso ao documento de componentes de backup e aos documentos de metadados do gravador. Em geral, esses documentos não são obtidos pela consulta de aplicativos em execução, mas são recuperados de versões armazenadas como documentos XML na mídia de backup.

Como é o caso durante operações de backup, os documentos de metadados do gravador permanecem objetos somente leitura e (uma vez recuperados) o documento de componentes de backup ainda pode ser modificado. As modificações do documento de componentes de backup permitem que gravadores e solicitante se comuniquem sobre o seguinte:

-   Substituindo [*métodos de restauração*](vssgloss-r.md) por [*destinos de restauração*](vssgloss-r.md)
-   Usando [ *mapeamentos de local alternativos*](vssgloss-a.md)
-   Restaurando arquivos para novos locais no disco
-   Usando regras de seleção diferentes daquelas usadas durante o backup

Para entender com mais detalhes as tarefas básicas envolvidas na execução de uma restauração, é útil dividir esta visão geral nos seguintes tópicos:

-   [Visão geral da inicialização da restauração](overview-of-restore-initialization.md)
-   [Visão geral da preparação para restauração](overview-of-preparing-for-restore.md)
-   [Visão geral da restauração de arquivo real](overview-of-actual-file-restoration.md)
-   [Visão geral da limpeza e término da restauração](overview-of-restore-clean-up-and-termination.md)

 

 



