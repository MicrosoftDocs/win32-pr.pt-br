---
description: Após uma restauração, os gravadores verificam o status da operação para que possam fazer uso dos dados restaurados e lidar com erros.
ms.assetid: f9def67a-c4ea-4014-929f-51fbd10d770a
title: Visão geral da limpeza e término da restauração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 391e029cdb109589b42240b5482f6aba2ff43555
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010852"
---
# <a name="overview-of-restore-clean-up-and-termination"></a>Visão geral da limpeza e término da restauração

Após uma restauração, os gravadores verificam o status da operação para que possam fazer uso dos dados restaurados e lidar com erros. O solicitante deve aguardar a conclusão desta atividade. Para obter mais informações, consulte [visão geral do processamento de uma restauração no VSS](overview-of-processing-a-restore-under-vss.md).

A tabela a seguir mostra a sequência de ações e eventos que são necessários depois que uma operação de restauração ocorre.



| Ação do solicitante                                                                                                                                                                                                                                                                                                                                                              | Evento                                                           | Ação do gravador                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| O solicitante indica o fim da restauração (consulte [**IVssBackupComponents::P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)).                                                                                                                                                                                                                                           | [*Restauração*](vssgloss-p.md) | O gravador realiza a limpeza após a restauração e lida com falhas de restauração e arquivos que foram restaurados em locais não padrão (consulte [**CVssWriter:: OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore), [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)). |
| O solicitante aguarda os gravadores para manipular o evento de [**restauração**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) com [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync). Ele também deve verificar o status do gravador (consulte [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus), [**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus)). | Nenhum                                                            | Nenhum                                                                                                                                                                                                                                               |
| O solicitante libera a interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) .                                                                                                                                                                                                                                                                                    | Nenhum                                                            | Nenhum                                                                                                                                                                                                                                               |



 

## <a name="requester-actions-during-cleanup-and-termination"></a>Ações do solicitante durante a limpeza e o encerramento

Neste ponto, um solicitante indica o final de suas atividades de restauração de arquivo gerando um evento de [*restauração*](vssgloss-p.md) chamando [**IVssBackupComponents::P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore).

As ações do solicitante são limitadas à espera nos gravadores, que talvez precisem executar alguma limpeza final e manipular erros de restauração e liberar a interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) depois que todos os gravadores tiverem retornado de manipular o evento de [*restauração*](vssgloss-p.md) .

## <a name="writer-actions-during-cleanup-and-termination"></a>Ações do gravador durante a limpeza e o encerramento

O evento [*Createrestore*](vssgloss-p.md) é tratado pelo método virtual [**CVssWriter:: OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore). A implementação padrão simplesmente retorna **true** sem realizar nenhuma ação. Se um gravador precisar exercer mais controle sobre a situação após a restauração, ele poderá substituir esse método.

Além de qualquer limpeza normal (como a remoção de arquivos temporários) que um gravador pode executar em [**CVssWriter:: OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore), ele pode lidar com o êxito ou a falha das operações de restauração.

Como ele lida com erros de restauração, arquivos restaurados em um local alternativo e a necessidade de restaurações futuras está completamente no critério do escritor. As ações típicas podem incluir a comparação de arquivos em locais alternativos ou novos com arquivos em uso no momento, mesclando dados de vários arquivos ou iniciando novas sessões conectadas aos novos arquivos de dados. O VSS fornece os seguintes mecanismos para dar suporte a isso em uma base componente por componente:

-   O êxito ou a falha na restauração de qualquer componente pode ser encontrado com [**IVssComponent:: GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus).
-   O uso de mapeamentos de local alternativo na restauração de arquivos será indicado por [**IVssComponent:: GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping).
-   Determinar se uma restauração é incremental e exigir restaurações adicionais é feita chamando [**IVssComponent:: GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores). Os gravadores que precisam de uma restauração completa de seus dados não devem ser reiniciados até que esse método retorne FALSE.
-   Os gravadores podem determinar se o solicitante precisava restaurar arquivos para um local não especificado anteriormente usando [**IVssComponent:: GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount) e [**IVssComponent:: GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)

(Para obter mais informações sobre como restaurar arquivos para locais não padrão, consulte [locais de backup e restauração não padrão](non-default-backup-and-restore-locations.md).)

Assim como ocorre com qualquer método [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) , as informações retornadas por uma determinada instância se aplicam a esses componentes [*explicitamente incluídos*](vssgloss-e.md) para backup e qualquer um de seus [*inclusos implicitamente*](vssgloss-i.md) para subcomponentes de backup, incluindo os subcomponentes explicitamente incluídos para restauração pelo solicitante usando [**IVssBackupComponents:: AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) (consulte [trabalhando com a seleção para restauração e subcomponentes](working-with-selectability-for-restore-and-subcomponents.md) para obter detalhes).

Como os gravadores precisarão acessar o documento de componentes de backup, é importante que o solicitante não libere a interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) até que os gravadores tenham terminado o processamento.

 

 



