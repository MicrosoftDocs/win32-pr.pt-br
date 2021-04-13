---
description: 'A participação de um gravador em backups incrementais e diferenciais normalmente ocorre durante o tratamento de eventos de identificação (CVssWriter:: onidentification), PrepareForBackup (CVssWriter: OnPrepareBackup) e de upsnapshot (CVssWriter: OnPostSnapshot).'
ms.assetid: 85c4e003-b531-4283-83aa-dd5cc53f35b1
title: Função de gravador em backups incrementais e diferenciais do VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2cda57d907bed4572f0c0f71f9ee829bee18299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501723"
---
# <a name="writer-role-in-vss-incremental-and-differential-backups"></a>Função de gravador em backups incrementais e diferenciais do VSS

A participação de um gravador em backups incrementais e diferenciais normalmente ocorre durante o tratamento de eventos de [*identificação*](vssgloss-i.md) ([**CVssWriter:: onidentification**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)), [*PrepareForBackup*](vssgloss-p.md) ([**CVssWriter: OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup)) e de *upsnapshot* ([**CVssWriter: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)). A forma como um gravador participa é moldado se ele dá suporte a carimbos de backup e horários da última modificação e se o solicitante que executa o backup dá suporte a [*operações parciais de arquivo*](vssgloss-p.md).

## <a name="handling-identify-events-during-incremental-and-differential-backups"></a>Tratamento de eventos de identificação durante backups incrementais e diferenciais

Ao manipular o evento de identificação, os gravadores estabelecem sua arquitetura básica para a operação de backup incremental e diferencial por meio do esquema de backup ([**\_ \_ esquema de backup do VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)) e de tipos de backup de especificação de arquivo (tipo de backup de especificação de [**\_ arquivo \_ \_ \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)).

Um gravador indica a quais operações ele dá suporte em seu documento de metadados do gravador criando uma máscara de bits de valores de [**\_ \_ esquema de backup do VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) e passando-a para o método [**IVssCreateWriterMetadata:: SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema) . Com isso, um gravador pode indicar se ele oferece suporte ao seguinte:

-   Backups incrementais (**\_ \_ incremental do VSS BS**)
-   Backups diferenciais (**\_ \_ diferencial do VSS BS**)
-   Backups incrementais e diferenciais não podem ser misturados (**\_ \_ \_ \_ diferenciais incrementais exclusivos do VSS BS**)
-   Backups incrementais e diferenciais usando carimbos de backup (**\_ carimbo de data/ \_ hora VSS BS**)
-   Backups incrementais e diferenciais com base nas informações sobre a última modificação de um arquivo (o **VSS \_ BS \_ última \_** modificação)

Os gravadores usam a máscara de tipo de backup de especificação de arquivo para fornecer informações de nível de conjunto de arquivos aos solicitantes sobre como incluir arquivos em um backup incremental ou diferencial.

Um gravador pode definir uma máscara de tipo de backup de especificação de arquivo de um conjunto de arquivos ao adicionar o conjunto de arquivos a um componente criando uma máscara de bits de valores de [**\_ \_ \_ \_ tipo de backup**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) de especificação de arquivo do VSS e passando-o para [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)ou [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup).

Há três valores de "backup necessário" da enumeração [**de \_ \_ tipo de \_ backup \_ de especificação de arquivo do VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) que afetam os backups diferenciais e incrementais:

-   **BACKUP do VSS \_ FSBT \_ todo \_ \_ necessário**
-   **\_backup incremental do VSS FSBT \_ \_ \_ necessário**
-   **\_ \_ backup diferencial do VSS FSBT \_ \_ necessário**

Há três valores de "cópia de sombra obrigatórias":

-   **\_FSBT VSS \_ todos os \_ instantâneos \_ necessários**
-   **\_instantâneo incremental do VSS FSBT \_ \_ \_ necessário**
-   **\_ \_ instantâneo diferencial do VSS FSBT \_ \_ necessário**

Conjuntos de arquivos marcados com um tipo de backup de especificação de arquivo de "cópia de sombra necessária" indicam se um solicitante precisa copiar dados de uma cópia de sombra ao executar as operações de backup INCREMENTAL, DIFERENCIAl ou tudo (que inclui operações incrementais e diferenciais).

O sinalizador "backup necessário", aplicado a operações INCREMENTAis, DIFERENCIAis ou de backup, indica que o gravador espera que uma cópia da versão atual do conjunto de arquivos esteja disponível após a restauração de qualquer operação de backup. Normalmente, isso significa que, se um conjunto de arquivos for marcado com "backup necessário", todos os seus membros serão copiados para a mídia de backup durante um backup incremental ou diferencial, independentemente de quando o backup ou a modificação tiver ocorrido pela última vez.

Por padrão, os conjuntos de arquivos são adicionados aos componentes com um tipo de backup de especificação de arquivo de **VSS \_ FSBT \_ todos os \_ backups \_ necessários** \| **VSS \_ FSBT \_ todo o \_ instantâneo \_ necessário**. Portanto, a menos que um desenvolvedor de escritor decida não usar o padrão (escolhendo outro tipo de backup de especificação de arquivo, usando operações parciais de arquivo ou usando arquivos diferenciados), os arquivos na maioria dos conjuntos de arquivos serão normalmente copiados em sua totalidade para mídia de backup.

Neste ponto, o documento de metadados do gravador do gravador é totalmente preenchido com a maioria das informações que um solicitante precisará para iniciar um backup diferencial ou incremental. A especificação de adição do conjunto de arquivos ou das informações de nível de arquivo para dar suporte ao backup será tratada durante o evento [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) .

## <a name="handling-prepareforbackup-events-during-incremental-and-differential-backups"></a>Manipulando eventos PrepareForBackup durante backups incrementais e diferenciais

Antes que o solicitante continue com a operação de backup real, os gravadores podem modificar a especificação de um backup [*incremental*](vssgloss-i.md) ou [*diferencial*](vssgloss-d.md) alterando o documento de componentes de backup do solicitante por meio da interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) .

Como os gravadores usam a interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) , normalmente executam essas preparações ao manipular o evento [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) .

Em [**CVssWriter: OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup), os gravadores podem especificar com mais precisão como alguns arquivos serão avaliados para backup, especificar quais mecanismos devem ser usados para fazer backup deles e possivelmente definir carimbos de backup.

<dl> <dt>

<span id="Partial_Files"></span><span id="partial_files"></span><span id="PARTIAL_FILES"></span>Arquivos parciais
</dt> <dd>

Se um solicitante oferecer suporte a eles, um gravador poderá optar por ter um backup incremental ou diferencial implementado usando operações de arquivo parcial. (Os gravadores podem determinar se um solicitante dá suporte a operações parciais de arquivo chamando [**CVssWriter:: IsPartialFileSupportEnabled**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispartialfilesupportenabled).)

Os gravadores usam [**IVssComponent:: Addparcialfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) para indicar as partes dos arquivos selecionados cujo backup será feito durante a operação incremental ou diferencial. Os solicitantes devem respeitar essa especificação e sempre devem fazer backup das seções especificadas dos arquivos. (Consulte [trabalhando com arquivos parciais](working-with-partial-files.md) para obter mais informações sobre operações de arquivo parcial.)

Usando [**IVssComponent:: Addparcialfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile), um gravador pode adicionar um arquivo ao backup que não foi adicionado anteriormente a um de seus conjuntos de componentes (por [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)ou [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)) como um arquivo parcial. Todos os novos arquivos adicionados ao backup dessa maneira devem estar em um volume que já esteja sendo copiado por sombra para esse backup.

Se um arquivo estiver envolvido com operações parciais de arquivo, isso substituirá qualquer tipo de backup de especificação de arquivo, que será ignorado.

</dd> <dt>

<span id="Differenced_Files"></span><span id="differenced_files"></span><span id="DIFFERENCED_FILES"></span>Arquivos diferenciados
</dt> <dd>

Os gravadores que dão suporte a um esquema de backup modificado pela última vez (**\_ \_ esquema de BS VSS**) podem adicionar [*arquivos diferenciados*](vssgloss-d.md) a um backup incremental ou diferencial.

Ao especificar um arquivo diferenciado, um gravador usa [**IVssComponent:: AddDifferencedFileByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) e especifica um caminho, um nome de arquivo e um sinalizador recursivo — no entanto, eles não precisam corresponder a um conjunto de arquivos incluído em qualquer componente.

Na verdade, um gravador pode adicionar um arquivo não adicionado anteriormente a um de seus conjuntos de componentes (por [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)ou [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)) ao backup como um arquivo diferenciado. Todos os novos arquivos adicionados ao backup dessa maneira devem estar em um volume que já esteja sendo copiado por sombra para esse backup.

Normalmente, um gravador também especificará uma hora da última modificação ao adicionar um arquivo diferenciado, com base no mecanismo de histórico próprio do gravador. Essa última hora de modificação, se especificada, deve sempre ser usada por solicitantes para determinar se um arquivo precisa ser incluído em um backup incremental ou diferencial.

Um gravador pode optar por não especificar uma hora da última modificação ao adicionar um arquivo diferenciado a um conjunto de backup incremental ou diferencial. Se esse for o caso, os solicitantes são livres para usar seus próprios mecanismos — por exemplo, logs de backups anteriores ou informações do sistema de arquivos — para determinar se o arquivo diferenciado deve ser incluído em um backup incremental ou diferencial.

O tipo de backup de especificação de arquivo de qualquer arquivo diferenciado é ignorado.

</dd> <dt>

<span id="Backup_Stamps"></span><span id="backup_stamps"></span><span id="BACKUP_STAMPS"></span>Carimbos de backup
</dt> <dd>

Os gravadores que dão suporte a carimbos de backup (**\_ carimbo de \_ data/hora VSS BS**) têm seu próprio formato privado para armazenar informações sobre quando um backup ocorreu pela última vez. Essas informações são geradas pelo gravador durante o backup.

O carimbo de backup é armazenado no documento componentes de backup como uma cadeia de caracteres pelo método [**IVssComponent:: SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp) . O carimbo de backup se aplica a todos os conjuntos de arquivos no componente (ou conjunto de componentes) correspondente à instância do [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent).

Se um solicitante tiver acesso ao carimbo de backup de um backup anterior, ele o terá disponibilizado para o gravador chamando [**IVssBackupComponents:: SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp).

Em seguida, um gravador pode examinar esse carimbo de data/hora usando [**IVssComponent:: GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp).

Observe que o solicitante simplesmente armazena e retorna a cadeia de caracteres que contém o carimbo de backup. Ele não sabe nada sobre o formato da cadeia de caracteres ou como usá-lo; somente o gravador tem essas informações.

Um gravador pode optar por atualizar o carimbo de backup atual usando [**IVssComponent:: SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp) depois de chamar [**IVssComponent:: GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp), gravando, dessa forma, a data da operação de backup incremental ou diferencial atual.

</dd> </dl>

 

 



