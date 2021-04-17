---
description: 'Em resposta a um evento de identificação, cada gravador presente no sistema constrói seu próprio documento de metadados do gravador usando o IVssCreateWriterMetadata. Um evento de identificação normalmente é gerado por um solicitante chamando IVssBackupComponents:: GatherWriterMetadata.'
ms.assetid: bae9bbe7-ca55-47cb-b253-8092007cb181
title: Ciclo de vida do documento de metadados do gravador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45be5748625d21f99abe3e77e0d6474a62210904
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760915"
---
# <a name="writer-metadata-document-life-cycle"></a>Ciclo de vida do documento de metadados do gravador

Em resposta a um [*evento de identificação*](vssgloss-i.md), cada gravador presente no sistema constrói seu próprio documento de metadados do gravador usando o [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata). Um *evento de identificação* normalmente é gerado por um solicitante chamando [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).

Ao criar um documento de metadados do gravador, seja por meio da interface [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) ou por meio da inicialização do gravador ([**CVssWriter:: Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize)), um gravador deve especificar explicitamente o seguinte:

-   [*Método Restore*](vssgloss-r.md)
-   Nome do gravador
-   [*ID da classe do gravador*](vssgloss-w.md)
-   Uso de dados ( [**consulte \_ \_ tipo de uso do VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type))
-   Tipo de fonte de dados (consulte [**\_ \_ tipo de origem VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type))

Além disso, ele também pode especificar o seguinte:

-   Componentes (que podem ou não conter conjuntos de arquivos)
-   Adicionar mapeamentos alternativos
-   Excluir listas de arquivos

Uma visão geral da criação do documento de metadados do gravador é encontrada em [ações do gravador durante a inicialização do backup](overview-of-backup-initialization.md).

Os solicitantes normalmente fazem uso de um dos dois métodos para obter acesso aos metadados do gravador:

-   Durante a maioria das operações de backup, um solicitante usa [**IVssBackupComponents:: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) para obter uma instância da interface [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) para permitir o acesso aos metadados de um gravador em execução no momento.
-   Para operações de restauração ou backups usando cópias de sombra importadas (consulte [importação de volumes copiados de sombra transportável](importing-transportable-shadow-copied-volumes.md) para obter mais informações sobre como importar cópias de sombra), um solicitante recupera um documento XML que contém os metadados e usa [**CreateVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssexaminewritermetadata) para obter uma interface [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) , que é usada para ler os metadados de restauração.

Os documentos de metadados do gravador permitem que o solicitante execute um backup para saber mais sobre os gravadores em execução no momento durante a fase de descoberta de um backup.

Para que os gravadores escolhidos participem de um backup, um solicitante importa muito, mas não todas, as informações no documento de metadados do gravador em seu próprio documento de componentes de backup durante a fase de descoberta de um backup.

No entanto, somente documentos de metadados do gravador e não o documento de componentes de backup contêm as especificações de arquivo e caminho.

Para obter mais informações sobre como a fase de descoberta de uma operação de backup é realizada, consulte [visão geral da fase de descoberta de backup](overview-of-the-backup-discovery-phase.md).

Além disso, somente os componentes [*explicitamente incluídos*](vssgloss-e.md) têm suas informações armazenadas no documento de componentes de backup durante uma operação de backup. As informações sobre componentes [*incluídos implicitamente*](vssgloss-i.md) não estão incluídas no documento de componentes de backup durante uma operação de backup e devem ser interpoladas usando informações sobre os componentes explicitamente incluídos e os documentos de metadados do gravador disponíveis.

Os componentes incluídos implicitamente ainda podem ser [*selecionáveis para restauração*](vssgloss-s.md) e talvez precisem ser incluídos explicitamente no documento componentes de backup no momento da restauração. Nesse caso, assim como a adição de um componente durante uma operação de backup exigia acesso ao documento de metadados do gravador writer's do componente (então recuperado do gravador), um solicitante exigirá acesso a uma cópia dos documentos de metadados do gravador do gravador armazenados no momento do backup.

Portanto, a única maneira de obter todas as informações sobre todos os arquivos e componentes envolvidos em um backup ou restauração é ter cada documento de metadados do gravador para cada gravador que participa de um backup armazenado junto com o documento de componentes de backup. (Para obter mais informações, consulte [visão geral da restauração de arquivo real](overview-of-actual-file-restoration.md).)

 

 



