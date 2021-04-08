---
description: Assim como acontece com todas as operações importantes no VSS, os backups incrementais e diferenciais exigem uma cooperação próxima entre os solicitantes e os gravadores.
ms.assetid: 00391a49-8c81-4518-88a2-741ad5ee4ac3
title: Função solicitante no backup de repositórios complexos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 197351e76b6861ee9b9d1e0589ef028c911430ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010850"
---
# <a name="requester-role-in-backing-up-complex-stores"></a>Função solicitante no backup de repositórios complexos

Assim como acontece com todas as operações importantes no VSS, os backups [*incrementais*](vssgloss-i.md) e [*diferenciais*](vssgloss-d.md) exigem uma cooperação próxima entre os solicitantes e os gravadores.

## <a name="backup-type"></a>Tipo de backup

A infraestrutura fornece suporte especial para cinco tipos de backup. Elas são descritas da seguinte maneira:

-   Completo (**VSS \_ BT \_ completa**). O backup dos arquivos será feito independentemente da data do último backup. O histórico de backup de cada arquivo será atualizado e esse tipo de backup poderá ser usado como a base de um backup incremental ou diferencial. Se houver arquivos de log, eles poderão ser truncados como resultado desse backup.

    A restauração de um backup completo requer apenas uma única imagem de backup.

-   Diferencial **( \_ \_ diferencial do VSS BT**). A API do VSS é usada para garantir que apenas os arquivos que foram alterados ou adicionados desde o último backup completo sejam copiados para um meio de armazenamento; todas as informações de backup intermediários são ignoradas. Isso pode incluir arquivos inteiros ou intervalos específicos em arquivos. Um backup diferencial é associado a um backup completo e geralmente não pode ser restaurado até que o backup completo tenha sido restaurado. Se houver arquivos de log, eles normalmente não serão truncados como resultado desse backup.

    A restauração de um backup diferencial requer a imagem de backup original e a imagem de backup diferencial mais recente feita desde o último backup completo.

-   Incremental (**VSS \_ BT \_ incremental**). A API do VSS é usada para garantir que apenas os arquivos que foram alterados ou adicionados desde o último backup completo ou incremental sejam copiados para um meio de armazenamento. Isso pode incluir arquivos inteiros ou intervalos específicos em arquivos. Alguns gravadores não permitem que backups incrementais sejam misturados com backups diferenciais. Se houver arquivos de log, eles poderão ser truncados como resultado desse backup.

    A restauração de um backup incremental requer a imagem de backup original e todas as imagens de backup incremental feitas desde o backup inicial.

-   Backup de log **( \_ \_ log de BT VSS**). Somente os arquivos de log de um gravador (arquivos adicionados a um componente com o método [**IVssCreateWriterMetadata:: AddDataBaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) e recuperados por uma chamada para [**IVssWMComponent:: GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile)) serão submetidos a backup. Esse tipo de backup é específico do VSS. Backups de log tendem a ser usados com muita frequência. Normalmente, o arquivo de log será truncado como resultado desse backup.
-   Copiar backup (**\_ \_ cópia do VSS BT**). Assim como o \_ tipo de backup completo do VSS BT \_ , será feito backup dos arquivos, independentemente da data do último backup. No entanto, o histórico de backup de cada arquivo não será atualizado e esse tipo de backup não poderá ser usado como a base de um backup incremental ou diferencial. Os arquivos de log nunca devem ser truncados como resultado de um backup de cópia.

<dl> <dt>

<span id="Partial_File_Support"></span><span id="partial_file_support"></span><span id="PARTIAL_FILE_SUPPORT"></span>Suporte a arquivos parciais
</dt> <dd>

Alguns gravadores dão suporte à restauração de arquivos por meio da substituição de partes dos arquivos que eles gerenciam. Um solicitante pode ser projetado para tirar proveito disso e, se for, ele indicará isso definindo as informações em [**IVssBackupComponents:: Setbackupstate**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate).

</dd> </dl>

O solicitante especifica que tipo de backup está sendo executado por meio do parâmetro *backuptype* de [**IVssBackupComponents:: setbackupstate**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate). Gravadores diferentes terão suporte para diferentes tipos de backup. Após a chamada de [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) , o solicitante pode determinar a quais tipos de backup um determinado gravador dá suporte chamando [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema). O valor retornado é uma máscara de bits que indica suporte para tipos de backup diferentes. **VSS \_ \_Diferencial de BS** indica suporte para backups diferenciais, **VSS \_ BS \_ incremental** para backups incrementais, **log de \_ BS \_ do VSS** para backups de log e **\_ \_ cópia de BS VSS** para backups de cópia; todos os gravadores devem oferecer suporte a backups completos Se um gravador não der suporte à combinação de backups incrementais com backups diferenciais, o sinalizador **\_ \_ \_ \_ diferencial incremental do VSS BS exclusivo** também será adicionado. Se o solicitante estiver executando um backup incremental ou diferencial e um determinado gravador não oferecer suporte a esse tipo de backup, um backup completo deverá ser executado nesse gravador.

## <a name="backup-stamps"></a>Carimbos de backup

Backups incrementais e diferenciais sempre estão associados a um backup anterior. Há duas maneiras de unir os backups. Para armazenamentos de dados simples, o solicitante pode controlar a correlação entre backups. No entanto, para armazenamentos de dados mais complexos, o gravador precisará manter seu próprio carimbo de data/hora com o backup; esse carimbo de data/hora pode manter o controle da posição do log, das informações do ponto de verificação e assim por diante. O solicitante pode determinar se um determinado gravador precisa armazenar seu próprio carimbo de data/hora verificando o bit de marca de data/ **\_ \_ hora do VSS BS** no valor retornado por [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema).

Os gravadores que armazenam um carimbo de data/hora em um backup adicionarão o carimbo de data/hora ao processar [**IVssBackupComponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) ou ao processar [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). O solicitante pode obter esse carimbo de data/hora chamando [**IVssComponent:: GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp). Ao executar um backup incremental ou diferencial, o solicitante precisa vincular o backup atual a algum backup anterior. Isso é feito obtendo o carimbo de data/hora do backup anterior de um componente específico e passando-o para a função [**IVssBackupComponents:: SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) ; Isso precisa ser feito para cada componente que foi submetido a backup no backup anterior.

## <a name="backing-up-files"></a>Fazendo backup de arquivos

### <a name="backing-up-files-reported-by-writer"></a>Fazendo backup de arquivos relatados pelo gravador

Cada especificação de arquivo que um gravador adiciona a seus metadados durante a fase GatherWriterMetadata contém uma máscara de tipo de backup que especifica quando deve ser feito o backup do arquivo. O solicitante determina o que é essa máscara chamando [**IVssWMFiledesc:: GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask). Os valores nessa máscara são usados para determinar para quais tipos de backup a especificação do arquivo precisa ser submetida a backup. A máscara pode conter um ou mais dos seguintes valores de bits:

<dl> <dt>

<span id="VSS_FSBT_FULL_BACKUP_REQUIRED"></span><span id="vss_fsbt_full_backup_required"></span>**\_backup completo do VSS FSBT \_ \_ \_ necessário**
</dt> <dd>

Necessário para backups completos.

</dd> <dt>

<span id="VSS_FSBT_DIFFERENTIAL_BACKUP_REQUIRED"></span><span id="vss_fsbt_differential_backup_required"></span>**\_ \_ backup diferencial do VSS FSBT \_ \_ necessário**
</dt> <dd>

Necessário para backups diferenciais.

</dd> <dt>

<span id="VSS_FSBT_INCREMENTAL_BACKUP_REQUIRED"></span><span id="vss_fsbt_incremental_backup_required"></span>**\_backup incremental do VSS FSBT \_ \_ \_ necessário**
</dt> <dd>

Necessário para backups incrementais.

</dd> <dt>

<span id="VSS_FSBT_LOG_BACKUP_REQUIRED"></span><span id="vss_fsbt_log_backup_required"></span>**\_backup de log FSBT do VSS \_ \_ \_ necessário**
</dt> <dd>

Necessário para backups de log.

</dd> <dt>

<span id="VSS_FSBT_ALL_BACKUP_REQUIRED"></span><span id="vss_fsbt_all_backup_required"></span>**BACKUP do VSS \_ FSBT \_ todo \_ \_ necessário**
</dt> <dd>

Necessário para todos os tipos de backup; Esse é o padrão.

</dd> </dl>

Essa especificação substitui a especificação de seletividade do componente. Por exemplo, considere um componente cujos arquivos são todos marcados com **o \_ backup de log FSBT do VSS \_ \_ \_ necessário** , mas não com o **\_ backup completo do VSS FSBT \_ \_ \_ necessário**. Suponha que esse componente não seja selecionável para backup (*bSelectable* foi falso quando [**IVssCreateWriterMetadata:: addComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent) foi chamado). No caso de um backup de log, isso significa que sempre é necessário fazer backup de todos os arquivos nesse componente. No entanto, no caso de um backup completo, nenhum dos arquivos precisa ser submetido a backup, apesar do fato de que a seletividade do componente implica que deve ser feito o backup.

### <a name="backup-by-last-modify-time"></a>Backup por hora da última modificação

As informações de especificação de arquivo especificadas na fase [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) não fornecem as informações do solicitante sobre o que foi alterado desde o último backup. Uma maneira de um gravador indicar alterações no solicitante é usando o mecanismo de arquivo diferenciado. Um gravador pode especificar que determinados arquivos em um componente devem ser copiados em backup somente se tiverem sido modificados desde um certo tempo; o gravador pode especificar esses arquivos em [**IVssBackupComponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) ou em [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). Um solicitante pode determinar esses arquivos chamando [**IVssComponent:: GetDifferencedFilesCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount) e [**IVssComponent:: GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile). Se a especificação do arquivo corresponder a um conjunto em **IVssBackupComponents:: GatherWriterMetadata** (que é atualmente válido com base na máscara de tipo de backup), as informações do arquivo diferenciado substituirão as informações anteriores; ou seja, os arquivos que correspondem a essa especificação de arquivo agora serão copiados somente se tiverem sido modificados desde o tempo especificado. A hora da última modificação é comunicada usando uma estrutura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) . Se o valor dessa estrutura for zero, isso significa que a hora da última modificação deve ser determinada com base no registro do solicitante da hora do último backup.

### <a name="partial-file-backup"></a>Backup de arquivo parcial

Outra maneira de um gravador indicar alterações no solicitante é usando o mecanismo de arquivo parcial. Um gravador pode especificar intervalos de bytes em arquivos de componentes que precisam ser copiados em backup; o gravador pode especificar esses intervalos de arquivos em [**IVssBackupComponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) ou em [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). Um solicitante pode determinar esses arquivos chamando [**IVssComponent:: GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount) e [**IVssComponent:: getparcialfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile). **IVssComponent:: Getparcialfile** retornará um caminho e um nome de arquivo apontando para o arquivo e uma cadeia de caracteres de intervalos indicando o backup que precisa ser feito no arquivo. Assim como ocorre com arquivos diferenciados, se o caminho e o nome do arquivo corresponderem a uma especificação de arquivo definida pelo gravador em [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), as informações de arquivo parcial substituirão a configuração anterior. A cadeia de caracteres de intervalos pode ter dois formatos: ele pode especificar os intervalos diretamente ou pode especificar um arquivo contendo informações de intervalos. Se especificar intervalos diretamente, a sintaxe será uma lista separada por vírgulas do formato offset1: length1, offset2: length2, em que cada offset e length será um inteiro sem sinal de 64 bits. Se especificar um arquivo de intervalos, a cadeia de caracteres de intervalos deverá ser definida como File = *filename*, em que *filename* é o caminho completo para o arquivo de intervalos. O próprio arquivo de intervalos é um arquivo binário que é formatado como uma lista de inteiros sem sinal de 64 bits. O primeiro inteiro indica quantos intervalos são representados no arquivo. Cada par subsequente de inteiros representa o deslocamento e o comprimento de um intervalo. O solicitante deve tomar cuidado para fazer backup e restaurar esse arquivo de intervalos também.

### <a name="file-specification-rules"></a>Regras de especificação de arquivo

As especificações de arquivo adicionadas por meio dos mecanismos de arquivo diferenciado e de arquivo parcial modificarão as especificações de arquivo definidas em [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) ou adicionarão arquivos completamente novos. Se a modificação das especificações de arquivos estiver definida em **IVssBackupComponents:: GatherWriterMetadata** usando o mecanismo de arquivo parcial, um solicitante poderá esperar que a especificação de arquivo corresponda exatamente a uma das especificações de arquivo definidas no componente em **IVssBackupComponents:: GatherWriterMetadata**. A especificação do arquivo não se sobreporá parcialmente a outra especificação de arquivo, e não corresponderá a quaisquer especificações de arquivo em nenhum dos componentes do escritor. No entanto, as especificações de arquivo adicionadas usando o mecanismo de arquivo parcial podem se sobrepor parcialmente a outra especificação de arquivo. Quando isso for verdadeiro, a especificação de arquivo diferenciado ou de arquivo parcial substituirá a especificação definida em **IVssBackupComponents:: GatherWriterMetadata**. As especificações de arquivo geral podem ter um valor de local alternativo (retornado por [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation)) que indica um local alternativo para obter o arquivo no momento do backup. Se as especificações de arquivo definidas por meio dos mecanismos de arquivo diferenciado ou de arquivo parcial corresponderem a uma especificação de arquivos existente que tenha um local alternativo, os dados deverão ser coletados nesse local alternativo. Se as especificações de arquivo definidas por meio dos mecanismos diferenciados-arquivo ou arquivo parcial não corresponderem a nenhuma especificação existente para o componente, então, esses intervalos de arquivos agora devem ser adicionados ao backup. O solicitante pode esperar que somente os arquivos em volumes que já foram incluídos no conjunto de cópias de sombra serão adicionados usando um desses mecanismos.

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

 

 
