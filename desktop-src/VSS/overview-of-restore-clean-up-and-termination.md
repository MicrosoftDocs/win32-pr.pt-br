---
description: Após uma restauração, os autores verificam o status da operação para que possam usar os dados restaurados e lidar com erros.
ms.assetid: f9def67a-c4ea-4014-929f-51fbd10d770a
title: Visão geral da limpeza e término da restauração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e8ad0b7d40f3c0e5322810f96bb120f28effe4ec3f0d4e278af924962713b2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122028"
---
# <a name="overview-of-restore-clean-up-and-termination"></a>Visão geral da limpeza e término da restauração

Após uma restauração, os autores verificam o status da operação para que possam usar os dados restaurados e lidar com erros. O solicitante deve aguardar a conclusão dessa atividade. Para obter mais informações, consulte [Visão geral do processamento de uma restauração no VSS.](overview-of-processing-a-restore-under-vss.md)

A tabela a seguir mostra a sequência de ações e eventos que são necessários após a realização de uma operação de restauração.



| Ação do solicitante                                                                                                                                                                                                                                                                                                                                                              | Evento                                                           | Ação do autor                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| O solicitante indica o final da restauração (consulte [**IVssBackupComponents::P ostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)).                                                                                                                                                                                                                                           | [*PostRestore*](vssgloss-p.md) | O autor realiza a limpeza pós-restauração e lida com falhas de restauração e arquivos que foram restaurados para locais não padrão (consulte [**CVssWriter::OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore), [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)). |
| O solicitante aguarda que os autores manipularem o [**evento PostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) com [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync). Ele também deve verificar o status do autor (consulte [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus), [**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus)). | Nenhum                                                            | Nenhum                                                                                                                                                                                                                                               |
| O solicitante libera a interface [**IVssBackupComponents.**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)                                                                                                                                                                                                                                                                                    | Nenhum                                                            | Nenhum                                                                                                                                                                                                                                               |



 

## <a name="requester-actions-during-cleanup-and-termination"></a>Ações do solicitante durante a limpeza e o encerramento

Neste ponto, um solicitante indica o final de suas atividades de restauração de arquivo gerando um evento [*PostRestore*](vssgloss-p.md) chamando [**IVssBackupComponents::P ostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore).

As ações do solicitante são limitadas à espera dos autores, que talvez precisem executar alguma limpeza final e tratar erros de restauração e liberar a interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) depois que todos os autores retornarem do tratamento do evento [*PostRestore.*](vssgloss-p.md)

## <a name="writer-actions-during-cleanup-and-termination"></a>Ações de writer durante a limpeza e o encerramento

O [*evento PostRestore*](vssgloss-p.md) é tratado pelo método virtual [**CVssWriter::OnPostRestore.**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore) A implementação padrão simplesmente retorna **true** sem realizar nenhuma ação. Se um autor precisar ter mais controle sobre a situação pós-restauração, ele poderá substituir esse método.

Além de qualquer limpeza normal (como a remoção de arquivos temporários) que um autor possa executar em [**CVssWriter::OnPostRestore,**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore)ele pode lidar com o êxito ou a falha das operações de restauração.

Como ele lida com erros de restauração, arquivos restaurados em um local alternativo e a necessidade de restaurações futuras são completamente a critério do autor. As ações típicas podem incluir a comparação de arquivos em locais alternativos ou novos com arquivos atualmente em uso, mesclar dados de vários arquivos ou iniciar novas sessões conectadas aos novos arquivos de dados. O VSS fornece os seguintes mecanismos para dar suporte a isso em uma base componente por componente:

-   Êxito ou falha na restauração de qualquer componente pode ser encontrado com [**IVssComponent::GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus).
-   O uso de mapeamentos de localização alternativos na restauração de arquivos será indicado por [**IVssComponent::GetAlternateLocationMapping.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping)
-   Determinar se uma restauração é incremental e exigirá restaurações adicionais é feita chamando [**IVssComponent::GetAdditionalRestores.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) Os autores que precisam de uma restauração completa de seus dados não devem reiniciar até que esse método retorne false.
-   Os autores podem determinar se o solicitante precisava restaurar arquivos para um local anteriormente não especificado usando [**IVssComponent::GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount) e [**IVssComponent::GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)

(Para obter mais informações sobre como restaurar arquivos em locais não padrão, consulte Locais de backup e [restauração não padrão](non-default-backup-and-restore-locations.md).)

Assim como com qualquer método [**IVssComponent,**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) as informações retornadas por determinada instância se [](vssgloss-i.md) aplica a esses componentes explicitamente incluídos para backup e qualquer um de seus subcomponentes de backup implicitamente incluídos, incluindo esses subcomponentes explicitamente incluídos para restauração pelo solicitante usando [**IVssBackupComponents::AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) (consulte Trabalhando com selecionável para restauração e [subcomponentes](working-with-selectability-for-restore-and-subcomponents.md) para obter detalhes). [](vssgloss-e.md)

Como os autores exigirão acesso ao Documento de Componentes de Backup, é importante que o solicitante não libere a interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) até que os autores tenham concluído o processamento.

 

 



