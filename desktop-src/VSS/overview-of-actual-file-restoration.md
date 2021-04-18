---
description: Depois de executar as ações descritas em visão geral da inicialização da restauração e da visão geral da preparação para a restauração, o solicitante tem informações suficientes para começar a restaurar arquivos.
ms.assetid: 15df39fa-1eb1-4e96-9e26-14470f391de4
title: Visão geral da restauração de arquivo real
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6527a10d0880b1e599377abb797449816019ab89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759775"
---
# <a name="overview-of-actual-file-restoration"></a>Visão geral da restauração de arquivo real

Depois de executar as ações descritas em [visão geral da inicialização da restauração](overview-of-restore-initialization.md) e [da visão geral da preparação para a restauração](overview-of-preparing-for-restore.md), o solicitante tem informações suficientes para começar a restaurar arquivos. A restauração de arquivos não envolve interações de gravador ou a geração de eventos. Para obter mais informações, consulte [visão geral do processamento de uma restauração no VSS](overview-of-processing-a-restore-under-vss.md).

A tabela a seguir mostra a sequência de ações e eventos necessários para restaurar arquivos.



| Ação do solicitante                                                                                                                                                                                                                                                                                                          | Evento | Ação do gravador |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|---------------|
| Gere uma listagem de conjunto de restauração para arquivos na mídia de backup.                                                                                                                                                                                                                                                                 | Nenhum  | Nenhum          |
| Manipule [*destinos direcionados*](vssgloss-d.md) ou restauração de [*arquivo parcial*](vssgloss-p.md) (Confira [**IVssComponent:: GetDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget), [**IVssComponent:: getparcialfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)). | Nenhum  | Nenhum          |
| Se necessário, ignore todos os locais de restauração especificados e restaure para um novo local especificado em uma chamada anterior para [**IVssBackupComponents:: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget).                                                                                                                       | Nenhum  | Nenhum          |
| Se a restauração for incremental e outras restaurações forem necessárias, indique (consulte [**IVssBackupComponents:: SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) e [backups incrementais e diferenciais](incremental-and-differential-backups.md)).                                                     | Nenhum  | Nenhum          |
| Para saber se um gravador modificou o conteúdo do documento de componentes de backup, chame [**IVssBackupComponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents). Por exemplo, o gravador pode ter alterado o destino de restauração.                                                                 | Nenhum  | Nenhum          |



 

## <a name="requester-actions-during-restoring-files"></a>Ações do solicitante durante a restauração de arquivos

Para a maioria dos arquivos na mídia de backup, o solicitante precisa determinar seus locais originais e quaisquer novos locais ou mapeamentos de locais alternativos que se aplicam a eles. (Consulte [gerando um conjunto de restauração](generating-a-restore-set.md) para uma discussão sobre práticas recomendadas para determinar quais arquivos restaurar e onde restaurá-los.)

Além disso, alguns arquivos podem ter [*destinos direcionados*](vssgloss-d.md) ou dar suporte à restauração [*parcial de arquivos*](vssgloss-p.md) . O número de tais arquivos pode ser encontrado chamando [**IVssComponent:: GetDirectedTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtargetcount) e [**IVssComponent:: GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount)e informações sobre instruções de restauração detalhadas podem ser encontradas chamando [**IVssComponent:: AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget) e [**IVssComponent:: getparcialfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile). (Arquivos parciais e direcionados podem fazer parte dos componentes adicionados implicitamente ou explicitamente ao backup original, consulte [trabalhando com a seleção de restauração e subcomponentes](working-with-selectability-for-restore-and-subcomponents.md) para obter mais informações.)

O êxito ou a falha de uma restauração é indicado em uma base de componente por componente usando [**IVssBackupComponents:: SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus). A necessidade de operações de restauração adicionais (no caso de restaurações incrementais ou diferenciais) também é indicada em uma base de componente por componente usando [**IVssBackupComponents:: SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores).

Em geral, o VSS não especifica um mecanismo para recuperar dados de uma mídia de armazenamento, uma opção de meio de armazenamento ou como determinar quais arquivos devem ser restaurados onde.

No entanto, para determinados gravadores, a restauração de arquivos pode envolver o uso de uma interface personalizada documentada e um procedimento. Os gravadores de sistema do Windows, que atualmente exigem esse suporte, são documentados em [casos de uso do VSS especiais](special-vss-usage-cases.md).

Em geral, é recomendável que os arquivos de cada componente de cada [*instância do gravador*](vssgloss-w.md) sejam processados como uma unidade. Isso exige o seguinte:

-   Associar cada arquivo a ser restaurado com o componente que o gerenciau. Isso requer o uso de documentos de metadados do gravador.
-   Obtendo informações corretas de destino de restauração. Isso requer informações do documento de componentes de backup.

 

 



