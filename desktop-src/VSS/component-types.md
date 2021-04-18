---
description: Os componentes indicam a espécie de dados que eles representam por meio de um tipo.
ms.assetid: 19d785d5-09a7-48b9-a0a2-eca3049d67fe
title: Tipos de componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1f89355b4b26090b7d43f9753c086b4ccc79df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781335"
---
# <a name="component-types"></a>Tipos de componentes

Os componentes indicam a espécie de dados que eles representam por meio de um tipo.

Atualmente, os tipos de componentes (consulte [**\_ \_ tipo de componente do VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_type)) são limitados ao seguinte:

-   Componentes de banco de dados
-   Grupos de arquivos

Para obter informações de implementação sobre como definir tipos de componentes, consulte [definição de componentes por gravadores](definition-of-components-by-writers.md).

Os gravadores têm uma digitação de dados que indica seu uso (consulte [**\_ \_ tipo de origem VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type)), que pode ser o seguinte:

-   Um banco de dados transacional (como um SQL Server)
-   Um banco de dados não transacional (como um cliente de planilha)
-   Grupo de arquivos (outro)

Especificar um tipo de componente como banco de dados permite a identificação mais fácil de seu conteúdo, permite a manipulação separada de arquivos de log e de dados (consulte [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) e [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) para obter detalhes) e impõe maior rigor na seleção de arquivo, não permitindo a seleção de arquivo recursivo ou o uso de um [*caminho alternativo*](vssgloss-a.md) (consulte [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) e [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)).

Com um componente de grupo de arquivos, por outro lado, ao preço de não saber quais dados ele contém, você tem maior liberdade sobre como os arquivos são inseridos, pois você pode usar especificação recursiva e caminhos alternativos.

Tipos de componentes adicionais podem ser adicionados no futuro.

 

 



