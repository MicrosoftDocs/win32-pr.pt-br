---
description: Em resposta a um evento Identify, cada autor presente no sistema constrói seu próprio Documento de Metadados do Writer usando IVssCreateWriterMetadata. Um evento Identify normalmente é gerado por um solicitante que chama IVssBackupComponents::GatherWriterMetadata.
ms.assetid: bae9bbe7-ca55-47cb-b253-8092007cb181
title: Ciclo de vida do documento de metadados de autor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2796d1a7b995f13829ac81485f74fa342bebe5e0e312b7b014d761a9962aa74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118121568"
---
# <a name="writer-metadata-document-life-cycle"></a>Ciclo de vida do documento de metadados de autor

Em resposta [*a*](vssgloss-i.md)um evento Identificar , cada autor presente no sistema constrói seu próprio Documento de Metadados do Autor usando [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata). Um *evento Identify* normalmente é gerado por um solicitante que chama [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).

Ao criar um Documento de Metadados do Writer, seja por meio da interface [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) ou por meio da inicialização do autor ([**CVssWriter::Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize)), um autor deve especificar explicitamente o seguinte:

-   [*Método de restauração*](vssgloss-r.md)
-   Nome do autor
-   [*ID da classe writer*](vssgloss-w.md)
-   Uso de dados (consulte [**TIPO DE USO DO VSS \_ \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type))
-   Tipo de origem de data (consulte [**TIPO DE \_ ORIGEM \_ DO VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type))

Além disso, ele também pode especificar o seguinte:

-   Componentes (que podem ou não conter conjuntos de arquivos)
-   Adicionar mapeamentos alternativos
-   Excluir listas de arquivos

Uma visão geral da criação do Documento de Metadados do Writer é encontrada em [Ações do Writer durante a Inicialização de Backup](overview-of-backup-initialization.md).

Os solicitantes normalmente usam um dos dois métodos para obter acesso aos metadados do autor:

-   Durante a maioria das operações de backup, um solicitante usa [**IVssBackupComponents::GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) para obter uma instância da interface [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) para permitir o acesso aos metadados de um autor em execução no momento.
-   Para operações de restauração ou backups usando cópias de sombra importadas (consulte Importando [volumes](importing-transportable-shadow-copied-volumes.md) copiados de sombra transportáveis para obter mais informações sobre como importar cópias de sombra), um solicitante recupera um documento XML que contém os metadados e usa [**CreateVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssexaminewritermetadata) para obter uma interface [**IVssExamineWriterMetadata,**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) que ele usa para ler os metadados de restauração.

Os Documentos de Metadados do Writer permitem que o solicitante que executa um backup saiba mais sobre os autores em execução no momento durante a fase de descoberta de um backup.

Para os autores escolhidos para participar de um backup, um solicitante importa grande parte, mas não todas, das informações no Documento de Metadados do Autor para seu próprio Documento de Componentes de Backup durante a fase de descoberta de um backup.

No entanto, somente os Documentos de Metadados do Writer e não o Documento de Componentes de Backup contêm as especificações de arquivo e caminho.

Para obter mais informações sobre como a fase de descoberta de uma operação de backup é realizada, consulte [Visão geral da fase de descoberta de backup](overview-of-the-backup-discovery-phase.md).

Além disso, somente [*componentes explicitamente incluídos*](vssgloss-e.md) têm suas informações armazenadas no Documento de Componentes de Backup durante uma operação de backup. As [*informações*](vssgloss-i.md) sobre componentes incluídos implicitamente não são incluídas no Documento de Componentes de Backup durante uma operação de backup e devem ser interpoladas usando informações sobre os componentes explicitamente incluídos e os Documentos de Metadados do Writer disponíveis.

Os componentes incluídos [](vssgloss-s.md) implicitamente ainda podem ser selecionáveis para restauração e talvez precisem ser explicitamente incluídos no Documento de Componentes de Backup no momento da restauração. Nesse caso, assim como a adição de um componente durante uma operação de backup exigia acesso ao Documento de Metadados do Autor do autor do componente (recuperado do autor), um solicitante exigirá acesso a uma cópia dos Documentos de Metadados do Autor do autor armazenados no momento do backup.

Portanto, a única maneira de obter todas as informações sobre todos os arquivos e componentes envolvidos em um backup ou restauração é ter cada Documento de Metadados do Writer para cada autor que participa de um backup armazenado junto com o Documento de Componentes de Backup. (Para obter mais informações, consulte [Visão geral da restauração de arquivo real](overview-of-actual-file-restoration.md).)

 

 



