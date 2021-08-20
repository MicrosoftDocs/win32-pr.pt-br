---
description: 'Para dar suporte a uma operação de backup incremental ou diferencial, um solicitante deve fazer o seguinte:'
ms.assetid: a77700e3-8217-460e-bec9-1041d03eec41
title: Função de solicitante no VSS backups incrementais e diferenciais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 637d4bf97b97d484080c85a2345599a05e4bbd89f88a0c1786b5bda911a83331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122001"
---
# <a name="requester-role-in-vss-incremental-and-differential-backups"></a>Função de solicitante no VSS backups incrementais e diferenciais

Para dar suporte a uma operação de backup [*incremental*](vssgloss-i.md) ou [*diferencial*](vssgloss-d.md) , um solicitante deve fazer o seguinte:

1.  Determine qual grau de suporte do gravador está disponível (usando [**IVssBackupComponents:: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) para obter acesso às informações em documentos de metadados do gravador) — em particular, determine qual esquema de backup tem suporte ([**esquema de \_ backup \_ do VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)).
2.  Defina um estado de backup apropriado.
3.  Obtenha especificações de nível de conjunto de arquivos e arquivos para um backup incremental ou diferencial.
4.  Execute o backup.

## <a name="requester-determination-of-incremental-and-differential-support-and-configuration"></a>Determinação do solicitante de suporte e configuração incremental e diferencial

Um solicitante precisa obter informações sobre o suporte do gravador antes de selecionar os componentes para inclusão em um backup incremental ou diferencial ou definir seu próprio estado.

<dl> <dt>

<span id="Determining_Writer_Support"></span><span id="determining_writer_support"></span><span id="DETERMINING_WRITER_SUPPORT"></span>Determinando o suporte do gravador
</dt> <dd>

Um solicitante determina se um determinado gravador dá suporte a backups incrementais ou diferenciais do VSS recuperando a máscara de esquema de backup do gravador usando o método [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema) .

A máscara de esquema de backup de um gravador com suporte a técnicas incrementais ou diferenciais do VSS conterá o **\_ \_ diferencial** **VSS \_ BS \_ incremental** ou do VSS BS ou ambos. Os gravadores também podem indicar restrições de sua participação com o sinalizador **\_ \_ \_ \_ diferencial incremental exclusivo do VSS BS** . (Consulte [**\_ \_ esquema de backup do VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) para obter mais informações sobre esquemas de backup).

</dd> <dt>

<span id="Setting_Requester_Backup_State"></span><span id="setting_requester_backup_state"></span><span id="SETTING_REQUESTER_BACKUP_STATE"></span>Definindo o estado do backup do solicitante
</dt> <dd>

Um solicitante indica que um backup é um backup incremental ou diferencial, definindo um tipo de backup como o **VSS \_ BT \_ incremental** ou **\_ \_ diferencial VSS BT** usando o método [**IVssBackupComponents:: setbackupstate**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) antes de gerar um evento [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) .

O método [**IVssBackupComponents:: Setbackupstate**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) também é usado para indicar se o solicitante fornece [*suporte parcial a arquivos*](vssgloss-p.md), que é frequentemente usado para implementar determinadas operações de backup e restauração incrementais.

</dd> </dl>

## <a name="getting-writer-specifications-for-incremental-and-differential-backups"></a>Obtendo especificações de gravador para backups incrementais e diferenciais

As informações de especificação de backup de arquivo de nível de conjunto de arquivos ([**tipo de backup de \_ especificação de arquivo \_ \_ \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)) contidas no documento de metadados do gravador de cada gravador estão disponíveis para exame após o retorno bem-sucedido de [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).

No entanto, um gravador pode adicionar [*arquivos diferenciados*](vssgloss-d.md) ou solicitar [*suporte parcial a arquivos*](vssgloss-p.md) até o tratamento bem-sucedido do evento de [*instantâneo*](vssgloss-p.md) .

O arquivo diferenciado e a especificação de suporte de arquivo parcial podem substituir o tipo de backup de especificação de arquivo, de modo que os solicitantes podem querer adiar uma análise completa de todas as especificações de gravador sobre backups incrementais e diferenciais até o retorno bem-sucedido de [**IVssBackupComponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup).

<dl> <dt>

<span id="Getting_File_Backup_Specification_Information"></span><span id="getting_file_backup_specification_information"></span><span id="GETTING_FILE_BACKUP_SPECIFICATION_INFORMATION"></span>Obtendo informações de especificação de backup de arquivo
</dt> <dd>

As informações de especificação de backup de arquivo no nível do conjunto de arquivos ([**tipo de backup de \_ especificação do arquivo \_ \_ \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)) estão contidas no documento de metadados do gravador de cada gravador e podem ser examinadas imediatamente após o retorno bem-sucedido de [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).

Os solicitantes devem obter máscaras de especificação de backup de arquivo ([**tipo de backup de \_ especificação de arquivo \_ \_ \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)) para cada conjunto de arquivos de cada um dos componentes do gravador a serem incluídos no backup incremental ou diferencial, independentemente de o componente ter sido [*explicitamente*](vssgloss-e.md) ou [*implicitamente*](vssgloss-i.md) incluído.

Um solicitante pode determinar quais documentos de metadados do gravador do gravador devem ser consultados usando [**IVssBackupComponents:: GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) e [**IVssBackupComponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents). A instância da interface [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) retornada por **IVssBackupComponents:: GetWriterComponents** fornece informações de gravador por meio do método [**IVssWriterComponentsExt:: GetWriterInfo**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getwriterinfo) .

O solicitante Obtém informações de componente por meio de instâncias da interface [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) correspondente a um componente incluído gerenciado por um determinado gravador usando [**IVssExamineWriterMetadata:: GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent).

As informações sobre conjuntos de arquivos gerenciados pelo componente correspondente à interface [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) são obtidas por chamadas para [**IVssWMComponent:: GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile), [**IVssWMComponent:: getdatabasefile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabasefile)ou [**IVssWMComponent:: GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile) (conforme apropriado).

Essas chamadas podem retornar instâncias da interface [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) para cada um dos conjuntos de arquivos de um componente.

Um tipo de backup de especificação de arquivo de um conjunto de arquivos é obtido chamando [**IVssWMFiledesc:: GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask).

</dd> <dt>

<span id="Getting_Partial_File_and_Differenced_File_Information"></span><span id="getting_partial_file_and_differenced_file_information"></span><span id="GETTING_PARTIAL_FILE_AND_DIFFERENCED_FILE_INFORMATION"></span>Obtendo informações parciais de arquivo e arquivo diferenciado
</dt> <dd>

Um solicitante Obtém o arquivo parcial e as informações de arquivo diferenciado por meio da interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) .

Um solicitante pode iterar em todos os gravadores incluídos em um backup usando [**IVssBackupComponents:: GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) e [**IVssBackupComponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents).

A instância de uma interface [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) retornada por [**IVssBackupComponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents) fornece acesso a todas as instâncias da interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondente a determinados componentes [*incluídos explicitamente*](vssgloss-e.md) de um gravador por meio dos métodos [**IVssWriterComponentsExt:: GetComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent) e [**IVssWriterComponentsExt:: GetComponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponentcount) .

Um solicitante precisará passar por todas as instâncias de [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) para todos os gravadores cujo esquema dê suporte ao backup incremental ou diferencial, ou seja, gravadores cuja máscara de esquema de backup, conforme retornado por [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema), inclui o **VSS \_ BS \_ incremental** quando o tipo de **backup for \_ \_** **VSS \_ BT \_ incremental** ou **\_ \_ diferencial do VSS**

As informações parciais do arquivo são obtidas chamando [**IVssComponent:: GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount) e [**IVssComponent:: getparcialfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile) (consulte [trabalhando com arquivos parciais](working-with-partial-files.md)).

Para gravadores que dão suporte a operações de backup com base nos dados da última modificação de um arquivo (gravadores cuja máscara de esquema de backup, conforme retornado por [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema), inclui o **VSS \_ BS \_ última \_ modificação**), as informações de arquivo diferenciado são obtidas chamando [**IVssComponent:: GetDifferencedFilesCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount) e [**IVssComponent:: GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile).

Observe que os arquivos diferenciados podem ser arquivos novos, ou seja, arquivos que não são membros de qualquer conjunto de arquivos atualmente em um documento de metadados do gravador específico.

Os solicitantes não devem localizar arquivos incluídos para operações de arquivo parcial e como arquivos diferenciados. Se um solicitante encontrar tal circunstância, ele deverá retornar e registrar um erro do gravador.

Um solicitante ainda pode optar por prosseguir com o backup dos arquivos do gravador problemáticos, mas, nesse caso, deve fazer isso de acordo com a especificação encontrada nas informações do arquivo diferenciado.

</dd> </dl>

## <a name="implementing-incremental-or-differential-backups"></a>Implementando backups incrementais ou diferenciais

Antes de implementar um backup, os solicitantes devem ter informações sobre quais gravadores dão suporte a um backup [*incremental*](vssgloss-i.md) ou [*diferencial*](vssgloss-d.md) , todas as operações de arquivo parcial solicitadas, todos os arquivos diferenciados e o tipo de backup de especificação de arquivo de todos os outros arquivos.

<dl> <dt>

<span id="Nonsupporting_Writers"></span><span id="nonsupporting_writers"></span><span id="NONSUPPORTING_WRITERS"></span>Gravadores sem suporte
</dt> <dd>

Os gravadores cujo esquema não dão suporte ao backup incremental ou diferencial (gravadores cuja máscara de esquema de backup, conforme retornado por [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema), inclui o **VSS \_ BS \_ incremental** quando o tipo de backup é **\_ \_ incremental do VSS BT** ou não inclui o **\_ \_ diferencial do VSS BS** quando o tipo de backup é **\_ \_ diferencial do VSS**

Isso não significa necessariamente que os dados dos gravadores não estarão envolvidos em uma operação de backup incremental ou diferencial. No entanto, a escolha do que fazer é a critério do solicitante. O solicitante pode fazer o seguinte:

-   Fazer backup de nenhum arquivo pertencente aos gravadores sem suporte (indique claramente isso para o usuário)
-   Fazer backup de todos os arquivos de gravadores sem suporte
-   Execute um backup incremental usando dados do sistema de arquivos e os próprios logs de histórico do solicitante.

A última alternativa deve ser usada com muito cuidado e somente se o solicitante entender se os gravadores envolvidos podem dar suporte a backup incremental ou diferencial e à restauração de dados independentemente do mecanismo VSS.

</dd> <dt>

<span id="Supporting_Writers"></span><span id="supporting_writers"></span><span id="SUPPORTING_WRITERS"></span>Escritores de suporte
</dt> <dd>

Um solicitante precisa processar (em ordem) todos os [*arquivos diferenciados*](vssgloss-d.md)do gravador, manipular todas as solicitações de [*arquivo parcial*](vssgloss-p.md) e, em seguida, fazer backup dos arquivos restantes de acordo com seu tipo de backup de especificação de arquivo ([**\_ \_ \_ \_ tipo de backup**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)de especificação de arquivo VSS).

1.  **Fazendo backup de arquivos diferenciados:**

    Para gravadores que dão suporte a operações de backup com base nos últimos dados de modificação (gravadores cuja máscara de esquema de backup, conforme retornado por [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema), inclui o **VSS \_ BS \_ última \_ modificação**), um solicitante usa as informações de caminho, especificação de arquivo e sinalizador de recursão retornada por [**IVssComponent:: GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile) para gerar uma lista de arquivos como candidatos para backup ou restauração incremental

    [**IVssComponent:: GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile) também pode retornar uma hora da última modificação (expressa como uma estrutura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) ).

    Se a hora da última modificação fornecida pelo gravador for diferente de zero, o solicitante a usará como base (em vez de informações do sistema de arquivos ou dos próprios dados armazenados do solicitante) para determinar se o arquivo deve ser incluído no backup [*incremental*](vssgloss-i.md) ou [*diferencial*](vssgloss-d.md) .

    Por exemplo, se a hora da última modificação do arquivo, conforme retornado pelo gravador foi:

    -   Após o último backup completo, o arquivo deve ser incluído nos backups incrementais e diferenciais.
    -   Após o último backup completo, mas antes do último backup incremental, o arquivo deve ser incluído em operações de backup incremental, mas não em backups diferenciais.

    Se a hora da última modificação fornecida pelo gravador for zero, o solicitante deverá usar informações do sistema de arquivos e seus próprios dados armazenados para determinar a hora da modificação do arquivo diferenciado.

2.  **Usando operações de arquivo parcial:**

    Se um gravador solicitou o backup de um arquivo usando uma operação de arquivo parcial, o solicitante usará as informações de deslocamento do arquivo para salvar os segmentos de arquivo indicados na mídia de backup. (Consulte [trabalhando com arquivos parciais](working-with-partial-files.md) para obter mais informações sobre operações de arquivo parcial).

    Como observado acima, um gravador não deve designar um arquivo como um arquivo diferenciado e como um participante em uma operação de arquivo parcial. Se um solicitante encontrar tal circunstância, ele deverá retornar e registrar um erro do gravador.

    Um solicitante ainda pode optar por prosseguir com o backup dos arquivos do gravador problemáticos, mas, nesse caso, deve fazer isso de acordo com a especificação encontrada nas informações do arquivo diferenciado.

3.  **Trabalhando com o tipo de backup de especificação de arquivo:**

    Depois de processar todos os arquivos e operações de arquivo parciais, o solicitante agora processa todos os arquivos restantes em seu conjunto de backup com base em seu tipo de backup de especificação de arquivo ([**\_ \_ \_ \_ tipo de backup spec de arquivo VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)).

    Há três valores de "backup necessário" da enumeração [**de \_ \_ tipo de \_ backup \_ de especificação de arquivo do VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) que afetam os backups diferenciais e incrementais:

    -   BACKUP do VSS \_ FSBT \_ todo \_ \_ necessário
    -   \_backup incremental do VSS FSBT \_ \_ \_ necessário
    -   \_ \_ backup diferencial do VSS FSBT \_ \_ necessário

    Há três valores de "cópia de sombra obrigatórias":

    -   \_FSBT VSS \_ todos os \_ instantâneos \_ necessários
    -   \_instantâneo incremental do VSS FSBT \_ \_ \_ necessário
    -   \_ \_ instantâneo diferencial do VSS FSBT \_ \_ necessário

    Conjuntos de arquivos marcados com um tipo de backup de especificação de arquivo de "cópia de sombra necessária" indicam que um solicitante precisa copiar dados de uma cópia de sombra ao executar as operações de backup INCREMENTAL, DIFERENCIAl ou todas (que inclui operações incrementais e diferenciais).

    O sinalizador "backup necessário", aplicado a operações INCREMENTAis, DIFERENCIAis ou de backup, indica que o gravador espera que uma cópia da versão atual do conjunto de arquivos esteja disponível após a restauração de qualquer operação de backup. Normalmente, isso significa que, se um conjunto de arquivos for marcado com "backup necessário", um solicitante copiará todos os seus membros para mídia de backup durante um backup incremental ou diferencial, independentemente de quando o backup ou a modificação tiver ocorrido pela última vez.

    Por padrão, os conjuntos de arquivos são adicionados aos componentes com um tipo de backup de especificação de arquivo de VSS \_ FSBT \_ todos os \_ backups \_ necessários \| VSS \_ FSBT \_ todo o \_ instantâneo \_ necessário. Portanto, a menos que um gravador defina explicitamente o tipo de backup de especificação de arquivo de outra forma, os solicitantes precisarão copiar os arquivos não tratados por operações de arquivo parcial ou os arquivos diferenciados designados na maioria dos conjuntos de arquivos serão normalmente copiados em sua totalidade para mídia de backup.

</dd> <dt>

<span id="Backup_Stamps"></span><span id="backup_stamps"></span><span id="BACKUP_STAMPS"></span>Carimbos de backup
</dt> <dd>

Os gravadores que dão suporte a carimbos de backup ( \_ \_ carimbo de data/hora VSS BS) podem optar por gerar informações de carimbo de backup a serem usadas para dar suporte a operações futuras de backup e restauração diferenciais

O formato e as informações contidas em cadeias de caracteres que contêm informações de carimbo de backup são particulares ao gravador que os gera; o solicitante não sabe como processar essas informações.

Os gravadores de suporte armazenam o carimbo de backup no documento componentes de backup como uma cadeia de caracteres usando o método [**IVssComponent:: SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp) .

A função do solicitante no tratamento de informações de carimbo de backup é (se existir) para disponibilizá-la ao gravador chamando [**IVssBackupComponents:: SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) em uma operação futura de backup ou restauração.

</dd> </dl>

 

 
