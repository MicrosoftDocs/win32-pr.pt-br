---
description: Assim como acontece com todas as operações importantes no VSS, os backups incrementais e diferenciais exigem uma cooperação próxima entre os solicitantes e os gravadores.
ms.assetid: 3cf5dd1f-dc58-42bc-925f-fee7d34053c5
title: Função de gravador no backup de repositórios complexos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80864256b9a19c25a2f0dce0d0c929ed19fd7269
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090430"
---
# <a name="writer-role-in-backing-up-complex-stores"></a>Função de gravador no backup de repositórios complexos

Assim como acontece com todas as operações importantes no VSS, os backups [*incrementais*](vssgloss-i.md) e [*diferenciais*](vssgloss-d.md) exigem uma cooperação próxima entre os solicitantes e os gravadores.

## <a name="backup-types"></a>Tipos de backup

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

Os gravadores indicam que tipo de backups têm suporte chamando [**IVssCreateWriterMetadata:: SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema) ao processar o evento de [*identificação*](vssgloss-i.md) . O parâmetro *dsSchemaMask* para o método **IVssCreateWriterMetadata:: SetBackupSchema** é uma máscara de bits que indica quais tipos de backup têm suporte. Todos os gravadores devem oferecer suporte a backups completos.

<dl> <dt>

<span id="VSS_BS_DIFFERENTIAL"></span><span id="vss_bs_differential"></span>**\_diferencial do VSS BS \_**
</dt> <dd>

Indica suporte para backups diferenciais.

</dd> <dt>

<span id="VSS_BS_INCREMENTAL"></span><span id="vss_bs_incremental"></span>**INCREMENTAL do VSS \_ BS \_**
</dt> <dd>

Indica suporte para backups incrementais.

</dd> <dt>

<span id="VSS_BS_LOG"></span><span id="vss_bs_log"></span>**\_log de BS do VSS \_**
</dt> <dd>

Indica suporte para backups de log.

</dd> <dt>

<span id="VSS_BS_COPY"></span><span id="vss_bs_copy"></span>**cópia do VSS \_ BS \_**
</dt> <dd>

Indica suporte para backups de cópia.

</dd> <dt>

<span id="VSS_BS_EXCLUSIVE_INCREMENTAL_DIFFERENTIAL"></span><span id="vss_bs_exclusive_incremental_differential"></span>**\_ \_ \_ diferencial incremental exclusivo do VSS BS \_**
</dt> <dd>

Indica que um gravador não dá suporte à combinação de backups incrementais com backups diferenciais.

</dd> </dl>

O gravador pode determinar que tipo de backup está sendo executado chamando [**CVssWriter:: Getbackuptype**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getbackuptype). O ponto mais antigo quando isso pode ser executado é durante o processamento do evento PrepareForBackup. **CVssWriter:: Getbackuptype** retornará um membro da enumeração de [**\_ \_ tipo de backup do VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_type) . Se o gravador não oferecer suporte ao tipo de backup, o gravador deverá tratar o backup como um backup completo.

## <a name="backup-stamps"></a>Carimbos de backup

Backups incrementais e diferenciais sempre estão associados a um backup anterior. Há duas maneiras de unir os backups. Para armazenamentos de dados simples, o solicitante pode controlar a correlação entre backups. No entanto, para armazenamentos de dados mais complexos, o gravador precisará manter seu próprio carimbo de data/hora com o backup; esse carimbo de data/hora pode manter o controle da posição do log, das informações do ponto de verificação e assim por diante. Um gravador indica que ele precisa de seus próprios carimbos de data/hora Configurando o bit de **\_ \_ marca** de e/ou/ou-ou-ou-ou-ou- [**IVssCreateWriterMetadata:: SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema)

Um gravador pode armazenar um carimbo de data/hora com cada componente que está sendo submetido a backup. O gravador armazena o carimbo de data/hora chamando [**IVssComponent:: SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)e passando uma representação de cadeia de caracteres do carimbo para o parâmetro *wszBackupStamp* . Em geral, um gravador chamará esse método durante o processamento do evento de [*instantâneo*](vssgloss-p.md) . No entanto, para backups que não envolvem uma cópia de sombra, o evento de pós-instantâneo não será enviado. Nesse caso, **IVssComponent:: SetBackupStamp** deve ser chamado durante o processamento do evento [*PrepareForBackup*](vssgloss-p.md) .

Quando um backup incremental ou diferencial estiver sendo executado, o solicitante indicará ao gravador o carimbo de backup do backup anterior que está servindo como base para esse backup. O gravador pode acessar este carimbo de backup anterior ao processar o evento PrepareForBackup ou pós-instantâneo, chamando [**IVssComponent:: GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp). O gravador pode usar o carimbo retornado para determinar o que precisa ser feito backup.

## <a name="backup-strategies"></a>Estratégias de backup

### <a name="file-backup-files-strategies"></a>Estratégias de arquivos de backup de arquivo

Geralmente, determinados arquivos relatados nos metadados do gravador precisam apenas de backup ao executar determinados tipos de backup. Alguns arquivos só podem ser necessários ao executar um backup completo. Outros arquivos só podem ser necessários ao executar um backup incremental ou diferencial. O VSS fornece um método para que os gravadores indiquem essas informações para o solicitante. Ao adicionar arquivos a componentes usando [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)ou [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), o parâmetro *dwBackupTypeMask* indica para quais tipos de backup esses arquivos devem ser submetidos a backup. A máscara pode conter um ou mais dos seguintes valores:

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

Uma maneira de um gravador indicar quais arquivos foram alterados é usando o mecanismo de arquivo diferenciado. Um gravador pode especificar que determinados arquivos em um componente só devem ser submetidos a backup se tiverem sido modificados desde um determinado momento. O gravador chama [**IVssComponent:: AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) com uma especificação de arquivo e uma hora da última modificação. **IVssComponent:: AddDifferencedFilesByLastModifyTime** normalmente é chamado durante o processamento do evento de pós-instantâneo, embora possa ser chamado durante o processamento do evento PrepareForBackup. O solicitante deve fazer backup de todos os arquivos que correspondem à especificação de arquivo que foi alterada desde o tempo especificado. Se o gravador estiver usando o mecanismo de carimbo de backup, essa última hora de modificação será determinada com base no carimbo de backup anterior no documento de backup. O gravador também pode passar zero para a hora da última modificação, o que indica que o solicitante é responsável por determinar o tempo do último backup e que os arquivos foram alterados desde o momento.

### <a name="partial-file-backup"></a>Backup de arquivo parcial

Outra maneira de um gravador indicar alterações no solicitante é usando o mecanismo de arquivo parcial. Um gravador pode especificar intervalos de bytes em arquivos de componentes que precisam ser copiados em backup; o gravador pode especificar esses intervalos de arquivos durante o processamento do evento de PrepareForBackup ou do instantâneo. O gravador chama [**IVssComponent:: Addparcialfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) para adicionar especificações de arquivo parcial ao backup. Uma especificação de arquivo parcial consiste em um caminho e um nome de arquivo juntamente com informações sobre quais intervalos no arquivo precisam ser copiados em backup.

### <a name="file-specification-rules"></a>Regras de especificação de arquivo

[**IVssComponent:: AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) ou [**IVssComponent:: addpartialfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) pode ser usado para modificar as especificações de arquivo fornecidas durante o evento de identificação ou para adicionar arquivos completamente novos à especificação. Se o gravador estiver modificando as informações definidas durante o evento de identificação usando **IVssComponent:: AddDifferencedFilesByLastModifyTime**, a especificação de arquivo deverá corresponder exatamente a uma das especificações de arquivo no componente atual. A especificação do arquivo não deve sobrepor parcialmente os arquivos no componente atual e não deve corresponder a arquivos em nenhum outro componente. Os arquivos especificados usando **IVssComponent:: Addparcialfile** podem, no entanto, sobrepor parcialmente outra especificação de arquivo. As informações definidas por **IVssComponent:: AddDifferencedFilesByLastModifyTime** ou **IVssComponent:: addpartialfile** substitui o conjunto de informações anteriormente usando a interface [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) em resposta ao evento de identificação.

As especificações de arquivo geral podem ter um valor de local alternativo (definido pelo parâmetro *wszAlternateLocation* de [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)) que indica um local alternativo para obter o arquivo no momento do backup. Se a especificação de arquivo definida por meio dos mecanismos diferenciados-arquivo ou arquivo parcial corresponder a uma especificação de arquivo existente que tenha um local alternativo, o aplicativo de backup obterá os dados desse local alternativo.

Se a especificação de arquivo definida em [**IVssComponent:: AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) ou em [**IVssComponent:: addpartialfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) não corresponder e arquivos no componente que estão sendo submetidos a backup, todos os arquivos correspondentes agora serão adicionados ao backup. Deve-se ter cuidado para que o gravador só adicione arquivos que existam em um volume que já esteja sendo copiado em sombra ao fazer isso; caso contrário, o solicitante pode falhar ao fazer backup desses arquivos. Se essas funções forem chamadas durante o processamento do evento de pós-instantâneo, isso poderá ser determinado usando o método [**CVssWriter:: IsPathAffected**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispathaffected) . Se chamado ao manipular o evento PrepareForBackup, o gravador deve fazer essa determinação usando outro método.

### <a name="backup-without-a-shadow-copy"></a>Backup sem uma cópia de sombra

É possível que certos tipos de arquivos não precisem ser submetidos a backup de um volume de cópia de sombra. Por exemplo, isso geralmente será verdadeiro para arquivos de log de banco de dados. Como os arquivos de log crescem de forma monotônico, e um gravador pode especificar exatamente quais partes do arquivo fazer backup usando arquivos parciais, muitas vezes será possível fazer backup do volume original. Como uma otimização, um gravador pode marcar quais arquivos exigem cópias de sombra para diferentes tipos de backup usando os sinalizadores definidos no parâmetro *dwBackupTypeMask* de [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)ou [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup). Os sinalizadores com suporte incluem o seguinte:

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

## <a name="backup-cleanup"></a>Limpeza de backup

Se o gravador precisar executar truncamento de log ou outra limpeza posterior ao backup, o local apropriado para fazer isso é durante o processamento do evento [*BackupComplete*](vssgloss-b.md) . O evento [*BackupShutdown*](vssgloss-b.md) será enviado algum tempo após BackupComplete, portanto, algumas limpeza também podem ser feitas no manipulador de eventos BackupShutdown.

O evento BackupShutdown é sempre enviado após o encerramento de um backup. Se o solicitante terminar de forma anormal durante a execução de um backup, o BackupShutdown será enviado imediatamente, sem primeiro enviar BackupComplete. Se o gravador precisar limpar qualquer Estado, isso pode ser feito aqui; no entanto, o truncamento de log não deve acontecer nesse evento porque o backup não foi concluído.

## <a name="restore-strategies"></a>Estratégias de restauração

As tarefas básicas de gravadores na restauração são verificar se a restauração pode acontecer na manipulação do evento de prerestore e se a restauração aconteceu ao manipular o evento de restauração. Armazenamentos mais complexos também executarão um processo de recuperação no manipulador de restauração. Se a restauração fizer parte de uma restauração incremental ou diferencial, o gravador geralmente desejará atrasar esse processo de recuperação até que todas as restaurações incrementais ou diferenciais tenham sido concluídas. [**IVssComponent:: GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) indicará se esta é a restauração final deste componente ou se há mais restaurações a serem fornecidas. Se **IVssComponent:: GetAdditionalRestores** retornar **true**, o gravador não deverá executar seu procedimento de recuperação nesse componente.

## <a name="new-targets"></a>Novos destinos

Se houver suporte do gravador, o solicitante poderá restaurar arquivos de dados para um local diferente do local de tempo de backup original. Um gravador indica suporte para esse modo de restauração, definindo que o **\_ gravador BS VSS \_ \_ dá suporte ao \_ novo \_** bit de destino no parâmetro *dsSchemaMask* ao chamar [**IVssCreateWriterMetadata:: SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema). Um gravador Obtém os novos locais para os arquivos de componente no momento da restauração chamando [**IVssComponent:: GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount) e [**IVssComponent:: GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget).

## <a name="directed-targets"></a>Destinos direcionados

Para cenários de restauração complicadas, um gravador pode querer mapear intervalos de um arquivo de backup em diferentes intervalos do mesmo arquivo ou de outro. Isso pode ser feito usando o mecanismo de destino direcionado. Para fazer isso, um gravador deve primeiro indicar que isso está acontecendo chamando [**IVssComponent:: SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget), passando o **VSS \_ RT \_ direcionado** para o parâmetro de *destino* . Em seguida, para cada mapeamento, o gravador chama [**IVssComponent:: AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget). Esse método usa um caminho completo para um arquivo de origem no backup e um caminho completo para um arquivo de destino que será restaurado para o. Ele também usa uma lista de intervalos para cada um desses arquivos. O gravador chama essas funções enquanto manipula o evento de prerestore, e o solicitante é responsável por restaurar os intervalos especificados no arquivo de origem para os intervalos mapeados no arquivo de destino. O formato da cadeia de caracteres de intervalos é o mesmo que em [ **IVssComponent:: addparcialfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile)

## <a name="private-writer-metadata"></a>Metadados do gravador privado

Geralmente, é útil que um gravador mantenha metadados privados com um backup para executar corretamente uma restauração incremental ou diferencial. Um gravador pode chamar [**IVssComponent:: SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata) ao manipular o PrepareForBackup ou o pós-instantâneo para armazenar metadados. Esses metadados podem ser acessados pelo gravador durante a prerestore ou a restauração chamando [**IVssComponent:: GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata). Os metadados também podem ser armazenados com a especificação de arquivo parcial usando o parâmetro *wszMetadata* de [**IVssComponent:: addparcialfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile); esses metadados são acessados por meio do parâmetro *pbstrMetadata* de [**IVssComponent:: getparcialfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile). O gravador também pode passar metadados para si mesmo entre [**CVssWriter:: OnPreRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore) e [**CVssWriter:: OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore). Em **CVssWriter:: OnPreRestore**, os metadados são definidos chamando [**IVssComponent:: SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata). Em **CVssWriter:: OnPostRestore**, os metadados são recuperados chamando [**IVssComponent:: GetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata).

-   [Função de gravador em backups incrementais e diferenciais do VSS](writer-role-in-vss-incremental-and-differential-backups.md)
-   [Função de solicitante no VSS backups incrementais e diferenciais](requestor-role-in-vss-incremental-and-differential-backups.md)

 

 



