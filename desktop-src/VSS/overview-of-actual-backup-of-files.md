---
description: O VSS permite que um solicitante acesse a cópia de sombra de volumes contendo dados para backup e copie dados para mídia de backup.
ms.assetid: 187f26f2-f191-4703-9bde-3357f1ceef0c
title: Visão geral do backup real de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2413111467014b666d219a7a1e92efad26302e5c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475692"
---
# <a name="overview-of-actual-backup-of-files"></a>Visão geral do backup real de arquivos

O VSS permite que um solicitante acesse a cópia de sombra de volumes contendo dados para backup e copie dados para mídia de backup. Os gravadores geralmente prosseguem com a operação normal durante esse processo. Para obter mais informações, consulte [visão geral do processamento de um backup em VSS](overview-of-processing-a-backup-under-vss.md).

A tabela a seguir mostra a sequência de ações e eventos necessários para o backup dos arquivos.




| Ação do solicitante | Evento | Ação do gravador | 
|------------------|-------|---------------|
| Acessar arquivos no volume copiado por sombra (consulte <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties"><strong>IVssBackupComponents:: Getinstantâneoproperties</strong></a>, <a href="/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop"><strong>VSS_SNAPSHOT_PROP</strong></a>) | Nenhum | Nenhum | 
| Gere a lista de arquivos para fazer backup e copie os dados de arquivo para mídia de backup. | Nenhum | Nenhum | 
| Indique o êxito ou a falha do backup com <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded"><strong>IVssBackupComponents:: SetBackupSucceeded</strong></a>. | Nenhum | Nenhum | 
| O solicitante indica que o backup foi concluído chamando <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete"><strong>IVssBackupComponents:: BackupComplete</strong></a>. | <a href="vssgloss-b.md"><em>BackupComplete</em></a> | Execute qualquer limpeza após o backup (consulte <a href="/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete"><strong>CVssWriter:: OnBackupComplete</strong></a>, <a href="/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents"><strong>IVssWriterComponents</strong></a>, <a href="/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent"><strong>IVssComponent</strong></a>). | 
| O solicitante espera que todos os gravadores reconheçam o recebimento do evento <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete"><strong>IVssBackupComponents:: BackupComplete</strong></a> usando <a href="/windows/desktop/api/Vss/nn-vss-ivssasync"><strong>IVssAsync</strong></a>. Ele também deve verificar o status do gravador (consulte <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus"><strong>IVssBackupComponents:: GatherWriterStatus</strong></a>, <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus"><strong>IVssBackupComponents:: GetWriterStatus</strong></a>). O solicitante deve chamar <strong>GatherWriterStatus</strong> no momento para fazer com que a sessão do gravador seja definida como um estado concluído.<blockquote>[!Note]<br />isso só é necessário no Windows Server 2008 com Service Pack 2 (SP2) e versões anteriores.</blockquote><br /> | Nenhum | Nenhum | 
| Salve o documento componentes de backup e cada documento de metadados do gravador em documentos XML, que podem ser gravados na mídia de backup (consulte <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml"><strong>IVssBackupComponents:: SaveAsXML</strong></a> e <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml"><strong>IVssExamineWriterMetadata:: SaveAsXML</strong></a>). | Nenhum | Nenhum | 




 

## <a name="writer-actions-during-backup-of-files"></a>Ações do gravador durante o backup de arquivos

Após a conclusão da cópia de sombra, todas as operações de e/s no sistema que estão sendo submetidas a backup devem ser capazes de retomar sem interromper a integridade do backup. Essa é uma das principais motivações para ter a funcionalidade de cópia de sombra.

Portanto, como na fase de descoberta (consulte [visão geral da fase de descoberta de backup](overview-of-the-backup-discovery-phase.md)), há poucas demandas colocadas nos gravadores enquanto os arquivos estão sendo realmente submetidos a backup.

Depois que um backup for concluído e um solicitante tiver gerado um evento [*BackupComplete*](vssgloss-b.md) , o VSS chamará o método [**CVssWriter:: OnBackupComplete**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete) de cada gravador, um método virtual que, por padrão, simplesmente retorna **true**. No entanto, os gravadores podem substituir a implementação padrão e tomar essas ações como remover arquivos temporários restantes ou usar a interface [**IVssWriterComponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) com a qual ele é chamado para verificar o estado do backup de cada um de seus componentes [*explicitamente incluídos*](vssgloss-e.md) (e qualquer [*conjunto de componentes*](vssgloss-c.md) que possam definir) recuperando o objeto [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondente. O gravador pode, então, determinar e agir, o êxito ou a falha do backup chamando [**IVssComponent: GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded). O valor retornado por **IVssComponent: GetBackupSucceeded** será **true** somente se todos os arquivos explicitamente incluídos no componente e todos os seus [*Subcomponentes*](vssgloss-s.md) tiverem sido [*incluídos*](vssgloss-i.md) em backup com êxito.

Quando a chamada para [**CVssWriter:: OnBackupComplete**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete) for concluída, o solicitante deverá chamar [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) e [**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) (para cada gravador) uma última vez. A memória de estado da sessão do gravador é um recurso limitado e os gravadores devem eventualmente reutilizar Estados de sessão. Esta etapa marca o estado da sessão de backup do gravador como concluída e notifica o VSS de que esse slot de sessão de backup pode ser reutilizado por uma operação de backup subsequente.

## <a name="requester-actions-during-backup-of-files"></a>Ações do solicitante durante o backup de arquivos

Conforme observado em [visão geral da fase de descoberta de backup](overview-of-the-backup-discovery-phase.md), você não deve gerar a lista real de arquivos cujo backup será feito até que a cópia de sombra seja concluída.

O [*objeto de dispositivo*](vssgloss-d.md) correspondente à cópia de sombra de um determinado volume é usado para obter acesso aos arquivos no volume de sombra copiado após a conclusão da cópia de sombra. O objeto de dispositivo é obtido do [**objeto \_ \_ prop do instantâneo do VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) retornado por [**IVssBackupComponents:: getinstantâneoproperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties). Cada cópia de sombra de um conjunto de cópias de sombra terá seu próprio objeto de dispositivo.

O objeto de dispositivo e os caminhos obtidos nas especificações do documento de metadados do gravador de componentes são então usados para selecionar arquivos para backup. Consulte [acesso do solicitante para sombra de dados copiados](requestor-access-to-shadow-copied-data.md) para obter mais informações.

Quais arquivos serão incluídos na lista de backup depende da natureza do backup específico, na seleção de componentes [*para backup*](vssgloss-s.md)e na estrutura de caminho lógico do gravador (consulte [trabalhando com a seleção de backup](working-with-selectability-for-backup.md)).

Além dos arquivos especificados nos componentes, um determinado gravador também pode ter arquivos explicitamente excluídos. A exclusão de arquivo sempre deve ser respeitada, independentemente dos componentes selecionados.

Além disso, conforme observado em [visão geral da fase de descoberta de backup](overview-of-the-backup-discovery-phase.md), uma pasta montada ou um ponto de nova análise pode aparecer em uma cópia de sombra e pode ser feito backup. No entanto, uma pasta montada ou um ponto de nova análise não pode ser atravessado no volume copiado por sombra (consulte [trabalhando com pastas montadas e pontos de nova análise](working-with-reparse-and-mount-points.md)).

O cuidado também deve ser feito durante uma operação de backup, se o [*caminho alternativo*](vssgloss-a.md) retornado por [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) não estiver em branco. Um caminho alternativo difere de um [*mapeamento de local alternativo*](vssgloss-a.md) , pois ele é usado somente durante os backups, enquanto um mapeamento de local alternativo é usado somente durante as restaurações.

Nesse caso, os dados não serão submetidos a backup de seu local normal (indicado por [**IVssWMFiledesc:: GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)), mas do local retornado por [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation). Na restauração, o arquivo deve ser retornado para seu local normal. Consulte [locais de backup e restauração não padrão](non-default-backup-and-restore-locations.md) para obter mais informações.

O VSS não coloca nenhuma restrição no mecanismo real de backup de dados em um meio de armazenamento ou na escolha desse meio. No entanto, é recomendável que os arquivos de cada componente de cada [*instância do gravador*](vssgloss-w.md) sejam processados como uma unidade. Consulte [gerando um conjunto de backup](generating-a-backup-set.md) para uma discussão das práticas recomendadas na geração da lista de arquivos de backup.

O êxito ou a falha de fazer backup de qualquer um dos arquivos gerenciados por um determinado componente e (se ele [*definir um conjunto de componentes*](vssgloss-c.md)) seus [*Subcomponentes*](vssgloss-s.md) para uma determinada instância do gravador devem ser preservados no documento componentes de backup chamando [**IVssBackupComponents:: SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded). Se algum arquivo gerenciado por um componente ou conjunto de componentes falhar no backup, o componente inteiro será considerado como falha. As informações exatas sobre o backup do arquivo que falhou devem ser sempre registradas.

Os desenvolvedores podem achar útil armazenar um registro na mídia de backup de quais arquivos são armazenados em backup, os componentes e o conjunto de componentes dos quais eram membros, sua especificação e quais são seus caminhos originais. Também pode ser útil armazenar informações, como a definição de componente de cada gravador. Fazer isso pode tornar a operação de recuperação mais simples. No entanto, esses detalhes são deixados para o desenvolvedor solicitante.

Como os gravadores podem modificar o documento de componentes de backup ao manipular o evento de [**instantâneo**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) gerado pela chamada do solicitante para [**IVssBackupComponents::D Osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), o documento de componentes de backup não deve ser salvo até que a chamada assíncrona seja concluída.

Embora possa ocorrer antes, esse também é um momento conveniente para salvar o documento de metadados do gravador.

É muito importante que o documento dos componentes de backup e os documentos de metadados do gravador sejam preservados usando [**IVssBackupComponents:: SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml) e [**IVssExamineWriterMetadata:: SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml). Se não forem, não será possível usar o VSS durante a restauração do arquivo.

Além de armazenar os metadados originais, alguns aplicativos de backup podem achar útil salvar uma cópia de sua própria lista de arquivos (em seu próprio formato otimizado) — e seu gravador, componente, procedimento de restauração e informações de localização associados — à mídia de backup para recuperação posterior. Essa lista pode ser usada para evitar algumas das análises e comparações dos documentos de metadados do gravador e dos documentos do componente de backup durante a restauração.

Os volumes cujo backup está sendo feito podem ter dados que não são gerenciados por gravadores VSS. Esses dados podem e devem ser submetidos a backup do volume copiado de sombra, onde estarão em um [*estado consistente com falhas*](vssgloss-c.md). Consulte [backups sem a participação do gravador](backups-without-writer-participation.md) para obter mais informações.

 

 




