---
description: Saiba mais sobre a função de solicitante em backups incrementais e diferenciais, que exigem cooperação estreita entre solicitantes e autores.
ms.assetid: 00391a49-8c81-4518-88a2-741ad5ee4ac3
title: Função do solicitante no back-up de armazenamentos complexos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84dfa1b0b1837bacc2488b6bd9e3ffdd51b92c0
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262178"
---
# <a name="requester-role-in-backing-up-complex-stores"></a>Função do solicitante no back-up de armazenamentos complexos

Assim como com todas as operações importantes no VSS, [*backups*](vssgloss-d.md) [*incrementais*](vssgloss-i.md) e diferenciais exigem cooperação estreita entre solicitantes e autores.

## <a name="backup-type"></a>Tipo de backup

A infraestrutura fornece suporte especial para cinco tipos de backup. Elas são descritas da seguinte maneira:

-   Full (**VSS \_ BT \_ FULL**). O backup dos arquivos será feito independentemente da data do último backup. O histórico de backup de cada arquivo será atualizado e esse tipo de backup pode ser usado como base de um backup incremental ou diferencial. Se houver arquivos de log, eles poderão ser truncados como resultado desse backup.

    A restauração de um backup completo requer apenas uma única imagem de backup.

-   Diferencial (**VSS \_ BT \_ DIFFERENTIAL**). A API do VSS é usada para garantir que somente os arquivos que foram alterados ou adicionados desde o último backup completo sejam copiados para uma mídia de armazenamento; todas as informações de backup intermediárias são ignoradas. Isso pode incluir arquivos inteiros ou intervalos específicos dentro de arquivos. Um backup diferencial é associado a um backup completo e geralmente não pode ser restaurado até que o backup completo seja restaurado. Se houver arquivos de log, eles geralmente não serão truncados como resultado desse backup.

    A restauração de um backup diferencial requer a imagem de backup original e a imagem de backup diferencial mais recente feita desde o último backup completo.

-   Incremental (**VSS \_ BT \_ INCREMENTAL**). A API do VSS é usada para garantir que somente os arquivos que foram alterados ou adicionados desde o último backup completo ou incremental sejam copiados para uma mídia de armazenamento. Isso pode incluir arquivos inteiros ou intervalos específicos dentro de arquivos. Alguns autores não permitem que backups incrementais sejam mistos com backups diferenciais. Se houver arquivos de log, eles poderão ser truncados como resultado desse backup.

    A restauração de um backup incremental requer a imagem de backup original e todas as imagens de backup incrementais feitas desde o backup inicial.

-   Backup de log (**VSS \_ BT \_ LOG**). Somente os arquivos de log de um autor (arquivos adicionados a um componente com o método [**IVssCreateWriterMetadata::AddDataBaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) e recuperados por uma chamada para [**IVssWMComponent::GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile)) terão o backup feito. Esse tipo de backup é específico do VSS. Os backups de log tendem a ser feitos com muita frequência. Normalmente, o arquivo de log será truncado como resultado desse backup.
-   Copiar backup (**VSS \_ BT \_ COPY**). Assim como o tipo de backup FULL DO VSS \_ \_ BT, os arquivos terão o backup feito independentemente da data do último backup. No entanto, o histórico de backup de cada arquivo não será atualizado e esse tipo de backup não pode ser usado como base de um backup incremental ou diferencial. Os arquivos de log nunca devem ser truncados como resultado de um backup de cópia.

<dl> <dt>

<span id="Partial_File_Support"></span><span id="partial_file_support"></span><span id="PARTIAL_FILE_SUPPORT"></span>Suporte parcial a arquivos
</dt> <dd>

Alguns autores suportam a restauração de arquivos por meio da substituição de partes dos arquivos que eles gerenciam. Um solicitante pode ser projetado para tirar proveito disso e, nesse caso, ele indica isso definindo as informações em [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate).

</dd> </dl>

O solicitante especifica que tipo de backup está sendo executado por meio do parâmetro *backupType* de [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate). Diferentes autores darão suporte a diferentes tipos de backup. Depois [**que IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) for chamado, o solicitante poderá determinar quais tipos de backup um determinado autor dá suporte chamando [**IVssExamineWriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema). O valor retornado é uma máscara de bits que indica suporte para diferentes tipos de backup. **VSS \_ BS \_ DIFFERENTIAL** indica suporte para backups diferenciais, **\_ VSS BS \_ INCREMENTAL** para backups incrementais, **LOG do VSS \_ BS \_ para** backups de log e **\_ VSS BS \_ COPY** para backups de cópia; todos os autores devem dar suporte a backups completos. Se um writer não dá suporte à combinação de backups incrementais com backups diferenciais, o sinalizador DIFERENCIAL INCREMENTAL EXCLUSIVO DO **\_ VSS BS \_ \_ \_** também será adicionado. Se o solicitante estiver executando um backup incremental ou diferencial e um determinado autor não dá suporte a esse tipo de backup, um backup completo deverá ser executado nesse autor.

## <a name="backup-stamps"></a>Carimbos de backup

Backups incrementais e diferenciais estão sempre vinculados a um backup anterior. Há duas maneiras de fazer backups. Para armazenamentos de dados simples, o solicitante pode acompanhar a correlação entre backups. No entanto, para armazenamentos de dados mais complexos, o autor precisará manter seu próprio timestamp com o backup; esse timestamp pode manter o controle da posição do log, das informações de ponto de verificação e assim por diante. O solicitante pode determinar se um determinado autor precisa armazenar seu próprio data/hora verificando o bit **\_ \_ TIMESTAMPED do VSS BS** no valor retornado por [**IVssExamineWriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema).

Os autores que armazenam um timestamp em um backup adicionarão o timestamp ao processar [**IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) ou ao processar [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). O solicitante pode obter esse timestamp chamando [**IVssComponent::GetBackupStamp.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp) Ao executar um backup incremental ou diferencial, o solicitante precisa ligar o backup atual a algum backup anterior. Isso é feito obtendo o timestamp do backup anterior de um componente específico e passando-o para a função [**IVssBackupComponents::SetPreviousBackupStamp;**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) isso precisa ser feito para cada componente que foi feito backup no backup anterior.

## <a name="backing-up-files"></a>Fazer o back-up de arquivos

### <a name="backing-up-files-reported-by-writer"></a>Fazer o back-up de arquivos relatados pelo writer

Cada especificação de arquivo que um autor adiciona aos seus metadados durante a fase GatherWriterMetadata contém uma máscara de tipo de backup que especifica quando o arquivo deve ser feito backup. O solicitante determina o que é essa máscara chamando [**IVssWMFiledesc::GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask). Os valores nessa máscara são usados para determinar para quais tipos de backup a especificação de arquivo precisa ser feito backup. A máscara pode conter um ou mais dos seguintes valores de bit:

<dl> <dt>

<span id="VSS_FSBT_FULL_BACKUP_REQUIRED"></span><span id="vss_fsbt_full_backup_required"></span>**BACKUP COMPLETO DO VSS \_ FSBT \_ \_ \_ NECESSÁRIO**
</dt> <dd>

Necessário para backups completos.

</dd> <dt>

<span id="VSS_FSBT_DIFFERENTIAL_BACKUP_REQUIRED"></span><span id="vss_fsbt_differential_backup_required"></span>**BACKUP \_ DIFERENCIAL DO VSS FSBT \_ \_ \_ NECESSÁRIO**
</dt> <dd>

Necessário para backups diferenciais.

</dd> <dt>

<span id="VSS_FSBT_INCREMENTAL_BACKUP_REQUIRED"></span><span id="vss_fsbt_incremental_backup_required"></span>**BACKUP INCREMENTAL DO VSS \_ FSBT \_ \_ \_ NECESSÁRIO**
</dt> <dd>

Necessário para backups incrementais.

</dd> <dt>

<span id="VSS_FSBT_LOG_BACKUP_REQUIRED"></span><span id="vss_fsbt_log_backup_required"></span>**BACKUP DE LOG DO VSS \_ FSBT \_ \_ \_ NECESSÁRIO**
</dt> <dd>

Necessário para backups de log.

</dd> <dt>

<span id="VSS_FSBT_ALL_BACKUP_REQUIRED"></span><span id="vss_fsbt_all_backup_required"></span>**VSS \_ FSBT \_ TODO O BACKUP \_ \_ NECESSÁRIO**
</dt> <dd>

Necessário para todos os tipos de backup; esse é o padrão.

</dd> </dl>

Essa especificação substitui a especificação de seletividade do componente. Por exemplo, considere um componente cujos arquivos estão marcados com BACKUP DE LOG DO **\_ VSS \_ \_ \_ FSBT** OBRIGATÓRIO, mas não com **\_ VSS FSBT \_ FULL BACKUP \_ \_ REQUIRED.** Suponha que esse componente não seja selecionável para backup (*bSelectable* era false quando [**IVssCreateWriterMetadata::AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent) foi chamado). No caso de um backup de log, isso significa que todos os arquivos neste componente sempre devem ser armazenados em backup. No entanto, no caso de um backup completo, nenhum dos arquivos precisa ser feito backup, apesar do fato de que a seletividade do componente implica que ele deve ser feito backup.

### <a name="backup-by-last-modify-time"></a>Backup por Hora da Última Modificação

As informações de especificação de arquivo especificadas na fase [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) não dão ao solicitante informações sobre o que mudou desde o último backup. Uma maneira de um autor indicar alterações no solicitante é usando o mecanismo de arquivo diferente. Um autor pode especificar que determinados arquivos em um componente devem ser armazenados em backup somente se eles foram modificados desde um determinado momento; O autor pode especificar esses arquivos em [**IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) ou em [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). Um solicitante pode determinar esses arquivos chamando [**IVssComponent::GetDifferencedFilesCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount) e [**IVssComponent::GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile). Se a especificação de arquivo corresponde a um conjunto em **IVssBackupComponents::GatherWriterMetadata** (que atualmente é válido com base na máscara de tipo de backup), as informações de arquivo diferença substituem as informações anteriores; ou seja, os arquivos correspondentes a essa especificação de arquivo agora terão o backup feito somente se eles foram modificados desde o horário especificado. A hora da última modificação é comunicada usando uma [**estrutura FILETIME.**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) Se o valor dessa estrutura for zero, isso implica que a hora da última modificação deve ser determinada com base no registro do solicitante da hora do último backup.

### <a name="partial-file-backup"></a>Backup parcial de arquivo

Outra maneira de um autor indicar alterações no solicitante é usando o mecanismo de arquivo parcial. Um autor pode especificar intervalos de byte em arquivos de componente que precisam ser armazenados em backup; O autor pode especificar esses intervalos de arquivos [**em IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) ou em [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). Um solicitante pode determinar esses arquivos chamando [**IVssComponent::GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount) e [**IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile). **IVssComponent::GetPartialFile** retornará um caminho e um nome de arquivo apontando para o arquivo e uma cadeia de caracteres de intervalos que indica o que precisa ser feito backup no arquivo. Assim como acontece com arquivos de diferença, se o caminho e o nome do arquivo corresponde a uma especificação de arquivo definida pelo autor em [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), as informações de arquivo parcial substituem a configuração anterior. A cadeia de caracteres de intervalos pode ter dois formatos: pode especificar os intervalos diretamente ou pode especificar um arquivo que contém informações de intervalos. Se especificar intervalos diretamente, a sintaxe será uma lista separada por vírgulas do formulário offset1:length1, offset2:length2, em que cada deslocamento e comprimento é um inteiro sem sinal de 64 bits. Se especificar um arquivo de intervalos, a cadeia de caracteres de intervalos deverá ser definida como File= *filename*, em que *filename* é o caminho completo para o arquivo de intervalos. O próprio arquivo de intervalos é um arquivo binário formatado como uma lista de inteiros sem sinal de 64 bits. O primeiro inteiro indica quantos intervalos são representados no arquivo. Cada par subsequente de inteiros representa o deslocamento e o comprimento de um intervalo. O solicitante deve tomar cuidado para fazer backup e restaurar esse arquivo de intervalos também.

### <a name="file-specification-rules"></a>Regras de especificação de arquivo

As especificações de arquivo adicionadas por meio do arquivo diferente e dos mecanismos de arquivo parcial modificarão as especificações de arquivo definidas em [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) ou adicionarão arquivos completamente novos. Se modificar as especificações de arquivos definidas em **IVssBackupComponents::GatherWriterMetadata** usando o mecanismo de arquivo parcial, um solicitante poderá esperar que a especificação do arquivo corresponder exatamente a uma das especificações de arquivo definidas no componente **em IVssBackupComponents::GatherWriterMetadata**. A especificação de arquivo não se sobrepõe parcialmente a outra especificação de arquivo e não corresponderá a nenhuma especificação de arquivo em nenhum outro dos componentes desse autor. As especificações de arquivo adicionadas usando o mecanismo de arquivo parcial podem, no entanto, sobrepor parcialmente outra especificação de arquivo. Quando isso for verdadeiro, a especificação de arquivo diferenciado ou de arquivo parcial substituirá a especificação definida em **IVssBackupComponents:: GatherWriterMetadata**. As especificações de arquivo geral podem ter um valor de local alternativo (retornado por [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation)) que indica um local alternativo para obter o arquivo no momento do backup. Se as especificações de arquivo definidas por meio dos mecanismos de arquivo diferenciado ou de arquivo parcial corresponderem a uma especificação de arquivos existente que tenha um local alternativo, os dados deverão ser coletados nesse local alternativo. Se as especificações de arquivo definidas por meio dos mecanismos diferenciados-arquivo ou arquivo parcial não corresponderem a nenhuma especificação existente para o componente, então, esses intervalos de arquivos agora devem ser adicionados ao backup. O solicitante pode esperar que somente os arquivos em volumes que já foram incluídos no conjunto de cópias de sombra serão adicionados usando um desses mecanismos.

### <a name="backup-without-a-shadow-copy"></a>Backup sem uma cópia de sombra

É possível que certos tipos de arquivos não precisem ser submetidos a backup de um volume de cópia de sombra. Por exemplo, isso geralmente será verdadeiro para arquivos de log de banco de dados. Como os arquivos de log crescem de forma monotônico, e um gravador pode especificar exatamente quais partes do arquivo fazer backup usando arquivos parciais, muitas vezes será possível fazer backup do volume original. Como uma otimização, um gravador pode marcar quais arquivos exigem cópias de sombra para tipos de backup diferentes usando a máscara de tipo de backup. O valor retornado de [**IVssWMFiledesc:: GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask) pode conter um ou mais dos seguintes valores de bits:

<dl> <dt>

<span id="VSS_FSBT_FULL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_full_snapshot_required"></span>**\_instantâneo completo do VSS FSBT \_ \_ \_ necessário**
</dt> <dd>

Cópia de sombra necessária para backups completos.

</dd> <dt>

<span id="VSS_FSBT_DIFFERENTIAL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_differential_snapshot_required"></span>**\_ \_ instantâneo diferencial do VSS FSBT \_ \_ necessário**
</dt> <dd>

Cópia de sombra necessária para backups diferenciais.

</dd> <dt>

<span id="VSS_FSBT_INCREMENTAL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_incremental_snapshot_required"></span>**\_instantâneo incremental do VSS FSBT \_ \_ \_ necessário**
</dt> <dd>

Cópia de sombra necessária para backups incrementais.

</dd> <dt>

<span id="VSS_FSBT_LOG_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_log_snapshot_required"></span>**instantâneo de log de FSBT do VSS \_ \_ \_ \_ necessário**
</dt> <dd>

Cópia de sombra necessária para backups de log.

</dd> <dt>

<span id="VSS_FSBT_ALL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_all_snapshot_required"></span>**\_FSBT VSS \_ todos os \_ instantâneos \_ necessários**
</dt> <dd>

Cópia de sombra necessária para todos os tipos de backup; Esse é o padrão.

</dd> </dl>

Se um volume específico contiver apenas componentes que não exigem uma cópia de sombra para esse backup, o solicitante poderá ignorar a etapa de criação de uma cópia de sombra para esse volume. Todos os dados nesse volume podem ser copiados para a mídia de backup diretamente do volume original.

## <a name="restoring-files"></a>Restaurando arquivos

### <a name="sequential-restores"></a>Restaurações sequenciais

Depois que o solicitante é executado executando uma operação de restauração, ele envia o evento de restauração para todos os gravadores. Em geral, os gravadores lidam com esse evento realizando recuperação ou outras operações de pós-restauração. No entanto, a restauração de backups incrementais geralmente ocorre como uma sequência de operações de restauração, uma por backup incremental. O solicitante precisa informar ao gravador que tal restauração está em andamento para evitar que a recuperação ou outras operações indesejadas ocorram até que a restauração seja concluída. Isso é feito chamando [**IVssBackupComponents:: SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores). Esse método é chamado por componente e indica para o gravador que mais restaurações são recebidas para esse componente. Para a restauração final na sequência, o sinalizador de restaurações adicionais deve ser definido como false (seu valor padrão), que indica que esta é a última restauração na sequência para esse componente.

### <a name="new-targets"></a>Novos destinos

Se houver suporte do gravador, o solicitante poderá restaurar arquivos de dados para um local diferente do local de tempo de backup original. O solicitante pode verificar esse suporte chamando [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema). O **gravador do VSS \_ BS \_ \_ dá suporte ao \_ novo \_** bit de destino será definido se o gravador oferecer suporte a esse comportamento. O solicitante informa o gravador do novo local chamando [**IVssBackupComponents:: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget) para cada especificação de arquivo realocado. O solicitante também pode optar por restaurar um arquivo de intervalos específico para um local diferente. O solicitante informa o gravador dessa alteração chamando [**IVssBackupComponents:: SetRangesFilePath**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath).

### <a name="directed-targets"></a>Destinos direcionados

Para cenários de restauração complicadas, um gravador pode querer mapear intervalos de um arquivo de backup em diferentes intervalos do mesmo arquivo ou de outro. Isso pode ser feito usando o mecanismo direcionado de destino. O solicitante pode determinar após a fase de [**Rerestauração IVssBackupComponents::P**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) que esse mecanismo está sendo usado para um componente chamando [**IVssComponent:: GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget) e verificando um retorno do **VSS \_ RT \_ direcionado**. O solicitante pode obter todas essas restaurações redirecionadas chamando [**IVssComponent:: GetDirectedTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtargetcount) e [**IVssComponent:: GetDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget). **IVssComponent:: GetDirectedTarget** retornará um caminho completo para um arquivo de origem no backup e um caminho completo para um arquivo de destino que será restaurado para o. Ele também retorna uma lista de intervalos para cada um desses arquivos. O solicitante é então responsável por restaurar os intervalos especificados no arquivo de origem para os intervalos mapeados no arquivo de destino. O formato da cadeia de caracteres de intervalos é o mesmo que em [**IVssComponent:: Getparcialfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile).

-   [Função de gravador em backups incrementais e diferenciais do VSS](writer-role-in-vss-incremental-and-differential-backups.md)
-   [Função de solicitante no VSS backups incrementais e diferenciais](requestor-role-in-vss-incremental-and-differential-backups.md)

 

 
