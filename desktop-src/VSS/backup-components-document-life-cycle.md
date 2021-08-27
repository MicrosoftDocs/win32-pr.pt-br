---
description: Os solicitantes têm responsabilidade principal pelo ciclo de vida de um documento de componentes de backup.
ms.assetid: 287b7b9a-ac04-4a74-83c1-2cdd4a571ac1
title: Ciclo de vida do documento de componentes de backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4804625f979e0d5621d96a2230c1419354d0dbeb4c368312dbd3943e0ac0c4bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124526"
---
# <a name="backup-components-document-life-cycle"></a>Ciclo de vida do documento de componentes de backup

Os solicitantes têm responsabilidade principal pelo ciclo de vida de um documento de componentes de backup.

Esse controle é exercido por uma instância do objeto de interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) retornado por [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents).

Um solicitante deve inicializar um documento de componentes de backup antes de um backup ou restauração chamando [**IVssBackupComponents:: InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) ou [**IVssBackupComponents:: InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore). O solicitante pode inicializar o documento como vazio, ou pode carregar uma cópia armazenada anteriormente do documento.

Para operações de backup, um documento de componentes de backup normalmente é inicializado como vazio. Seus dados serão preenchidos com a cooperação dos gravadores do sistema no decorrer do processamento do backup.

Para operações de restauração, um documento de componentes de backup normalmente é inicializado a partir de um documento armazenado gerado durante o backup inicial. Isso permite que a restauração (em conjunto com o exame de documentos de metadados do gravador armazenados) determine quais dados foram inicialmente copiados em backup e como eles devem ser restaurados.

O backup de [*cópias de sombra transportáveis*](vssgloss-t.md) é uma exceção a essa regra. Nesse caso, uma cópia de sombra poderia ter sido movida de um sistema (onde foi criada junto com o documento de componentes de backup inicial) para outro por meio da reatribuição de uma unidade lógica do dispositivo de armazenamento compartilhado. Para fazer backup dessas circunstâncias, um solicitante carrega o estado de backup armazenado e prossegue de onde o sistema inicial parou. (Para obter mais informações, consulte [importando volumes copiados de sombra transportável](importing-transportable-shadow-copied-volumes.md).)

No decorrer do processamento de um backup, o solicitante decide quais componentes são realmente copiados com base em quais componentes são marcados como [*selecionáveis para backup*](vssgloss-s.md), os [*caminhos lógicos*](vssgloss-l.md)do componente e sua própria lógica interna.

Alguns dos componentes serão [*incluídos explicitamente*](vssgloss-e.md) na operação de backup; as informações sobre o componente serão adicionadas ao documento componentes de backup. Outras serão [*incluídas implicitamente*](vssgloss-i.md) no backup; as informações sobre os componentes adicionados não serão adicionadas ao documento de componentes de backup.

Todos os não selecionáveis do gravador para componentes de backup sem um ancestral selecionável em seu caminho lógico e aqueles selecionáveis para componentes de backup que o solicitante escolhe, serão adicionados explicitamente.

Não selecionável e selecionável para componentes de backup podem ser adicionados implicitamente se tiverem um ancestral selecionável em seu caminho lógico, que é explicitamente incluído no backup. Esses componentes ([*Subcomponentes*](vssgloss-s.md)) são membros de [*conjuntos de componentes*](vssgloss-s.md) definidos pelo ancestral selecionável.

Ao lidar com operações de restauração, o solicitante usa a [*seleção para restauração*](vssgloss-s.md) em vez de seleção para backup em conjunto com informações de caminho lógico e sua própria lógica interna para decidir quais arquivos restaurar.

Se um componente que foi implicitamente adicionado ao backup agora for explicitamente adicionado à restauração, o solicitante atualizará o documento de componentes de backup com as informações desse componente.

As informações sobre os componentes armazenados estão disponíveis para solicitantes e gravadores por meio de instâncias da interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) .

É por meio de interfaces [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) que os gravadores podem consultar e (até o fim dos eventos de [**reinstantâneo**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) e de [**restauração**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore) ) modificam as informações no documento de componentes de backup.

Quando o manipulador de eventos [**CVssWriter:: OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup), [**CVssWriter:: OnPreRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore), [**CVssWriter:: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot), [**CVssWriter:: OnBackupComplete**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete)ou [**CVssWriter:: OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore) é chamado, um gravador recebe uma instância de uma interface [**IVssWriterComponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) .

Observe que, após a geração do evento [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) , o documento de componentes de backup é tornado somente leitura e, portanto, [**CVssWriter:: OnBackupComplete**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete) não pode usar a interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) para modificá-lo.

Na interface [**IVSSWriterComponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) , o gravador pode recuperar instâncias da interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) que permitirão que ela acesse todos os seus componentes explicitamente adicionados ao documento de componentes de backup e altere seu estado. Para obter mais informações, consulte [visão geral do processamento de um backup em VSS](overview-of-processing-a-backup-under-vss.md) e [visão geral do processamento de uma restauração no VSS](overview-of-processing-a-restore-under-vss.md).

Os documentos de componentes de backup são removidos da memória quando a interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) é liberada e devem ser armazenados usando [**IVssBackupComponents:: SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml)ou todas as suas informações serão perdidas.

Além disso, quando um documento [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) é liberado corretamente, um evento [**BackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown) é gerado e as [*cópias de sombra de lançamento automático*](vssgloss-a.md) são excluídas.

 

 



