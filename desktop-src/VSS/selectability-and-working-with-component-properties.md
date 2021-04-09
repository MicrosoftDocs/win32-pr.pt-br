---
description: Trabalhar com componentes selecionados implicitamente requer acesso aos documentos de metadados do documento e do gravador dos componentes de backup.
ms.assetid: ede51931-be50-4286-818b-0e6122247bdd
title: Seleção e trabalho com propriedades de componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83d06683bafb02802d84f152f1ceb662eb7491f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091425"
---
# <a name="selectability-and-working-with-component-properties"></a>Seleção e trabalho com propriedades de componente

Trabalhar com componentes selecionados implicitamente requer acesso aos documentos de metadados do documento e do gravador dos componentes de backup.

Há dois motivos para isso:

-   Os dados do componente armazenados no documento componentes de backup (representado pela interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) ) não têm acesso às informações do conjunto de arquivos de componentes — especificação de arquivo, caminho e sinalizador de recursão. (Consulte [trabalhando com o documento componentes de backup](working-with-the-backup-components-document.md).)
-   Somente os componentes [*incluídos explicitamente*](vssgloss-e.md) no documento componentes de backup durante o backup têm suas informações armazenadas diretamente no documento componentes de backup. Os solicitantes e os gravadores devem usar as informações disponíveis por meio da interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) , em conjunto com as informações de [*caminho lógico*](vssgloss-l.md) e documentos de metadados do gravador para obter informações e definir propriedades de, componentes [*incluídos implicitamente*](vssgloss-i.md) .

O caso "myWriter" abordado em [um caminho lógico de componentes](logical-pathing-of-components.md) pode ser usado para ilustrar a seleção de backup.



| Nome do Componente | Caminho lógico            | Selecionável para backup | Selecionável para restauração | Incluído explicitamente |
|----------------|-------------------------|-----------------------|------------------------|---------------------|
| Executáveis  | ""                      | N                     | N                      | S                   |
| "ConfigFiles"  | Executáveis           | N                     | N                      | S                   |
| "LicenseInfo"  | ""                      | S                     | N                      | S                   |
| “Segurança”     | ""                      | S                     | N                      | S                   |
| UserInfo     | “Segurança”              | N                     | N                      | N                   |
| Certificado | “Segurança”              | N                     | N                      | N                   |
| "writerData"   | ""                      | S                     | S                      | S                   |
| Conjunto1         | "writerData"            | N                     | S                      | N                   |
| Janeiro          | "writerData \\ conjunto1"      | N                     | N                      | N                   |
| Dez          | "writerData \\ conjunto1"      | N                     | N                      | N                   |
| Conjunto2         | "writerData"            | N                     | S                      | N                   |
| Janeiro          | "writerData \\ conjunto2"      | N                     | N                      | N                   |
| Dez          | "writerData \\ conjunto2"      | N                     | N                      | N                   |
| Consultá        | "writerData \\ QueryLogs" | N                     | N                      | N                   |
| Usos        | "writerData"            | S                     | S                      | N                   |
| Janeiro          | "uso de writerData \\ "     | N                     | N                      | N                   |
| Dez          | "uso de writerData \\ "     | N                     | N                      | N                   |



 

## <a name="implicitly-included-components-in-the-backup-set"></a>Componentes incluídos implicitamente no conjunto de backup

Ao examinar o documento de metadados do gravador do gravador (consulte [**IVssBackupComponents:: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata)) durante o backup, um solicitante deve armazenar uma lista de todos os componentes, seus [*caminhos lógicos*](vssgloss-l.md)e suas informações de conjunto de arquivos.

As informações de conjunto de arquivos e arquivo excluído serão necessárias para determinar uma lista de arquivos para qualquer componente incluído (explícita ou implicitamente).

Para não selecionável para componentes de backup sem seleção para os ancestrais de backup e selecionáveis para os componentes de backup que não definem um [*conjunto de componentes*](vssgloss-c.md), somente as informações de conjunto de arquivos e arquivo excluído serão necessárias para identificar todos os candidatos do componente para backup, pois esses componentes não definem subcomponentes.

Para selecionáveis explicitamente incluídos para componentes de backup que definem um conjunto de componentes, o arquivo define e exclui informações de arquivo para o componente de definição e todos os [*Subcomponentes*](vssgloss-s.md) precisam ser usados para selecionar arquivos para backup.

Isso significa que os conjuntos de backup para os componentes "executáveis", "ConfigFiles" e "LicenseInfo" podem ser encontrados apenas examinando os metadados do gravador apenas para esses componentes usando suas instâncias da interface [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) .

No entanto, se writerData for incluído explicitamente no backup, você deverá examinar sua instância da interface [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) e as de "conjunto1", "Jan" (com o caminho lógico "writerData \\ conjunto1"), "DEC" (com caminho lógico "writerData \\ conjunto1"), "Conjunto2", "Jan" (com caminho lógico "writerData \\ Conjunto2"), "DEC" (com o caminho lógico "writerData \\ conjunto2"), "Query", "Usage", "Jan" (com o caminho lógico "WriterData Usage" \\ ) e "DEC" (com o caminho lógico "writerData Usage" \\ ).

Para fazer isso, um solicitante precisará primeiro identificar que o componente "writerData" (caminho lógico "") é selecionável. Em seguida, será necessário verificar todos os outros componentes gerenciados pelo gravador para determinar se o primeiro elemento em seu caminho lógico é "writerData". Os componentes que têm "writerData" como os membros à esquerda de seu caminho lógico são identificados como subcomponentes de "writerData" e são selecionados implicitamente quando são selecionados explicitamente.

Na verdade, será necessário fazer uma verificação semelhante para determinar que nenhum componente tenha "LicenseInfo" como o membro à esquerda de seu caminho lógico e, portanto, "LicenseInfo" não tenha subcomponentes.

Devido à complexidade desse mecanismo no VSS, muitos gravadores de solicitação podem achar útil criar suas próprias estruturas para armazenar as informações de componente e conjunto de backup para componentes explicitamente e implicitamente adicionados.

## <a name="properties-of-implicitly-included-components"></a>Propriedades de componentes incluídos implicitamente

Durante as operações de restauração e backup, as instâncias das interfaces [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) e [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) são usadas para recuperar informações sobre componentes e para definir ou alterar as propriedades do componente. No entanto, somente os componentes explicitamente incluídos terão instâncias da interface **IVssComponent** ou poderão ser acessados para a interface **IVssBackupComponents** .

Algumas propriedades são do conjunto de componentes em todo o escopo. Essas propriedades incluem o seguinte:

-   Status de backup e restauração: <dl>

[**IVssBackupComponents::SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)  
    [**IVssComponent::GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded)  
    [**IVssBackupComponents::SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus)  
    [**IVssComponent::GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus)  
    </dl>
-   Opções de backup e restauração: <dl>

[**IVssBackupComponents:: setbackupoptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupoptions)  
    [**IVssComponent:: getbackupoptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupoptions)  
    [**IVssBackupComponents:: setrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions)  
    [**IVssComponent:: getrestore**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoreoptions)  
    </dl>
-   Mensagens de falha: <dl>

[**IVssComponent::SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg)  
    [**IVssComponent::SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg)  
    [**IVssComponent::SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg)  
    [**IVssComponent::SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg)  
    </dl>
-   Restaurar destinos: <dl>

[**IVssComponent::SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget)  
    [**IVssComponent::GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget)  
    </dl>
-   Carimbos de backup: <dl>

[**IVssComponent::SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)  
    [**IVssComponent::GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp)  
    </dl>
-   Metadados adicionais: <dl>

[**IVssComponent::SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata)  
    [**IVssComponent::GetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata)  
    [**IVssComponent::SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata)  
    [**IVssComponent::GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)  
    </dl>

Portanto, você usa a instância da interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) de um conjunto de componentes que define um membro ou usa o nome, o tipo e o caminho lógico da definição do membro com um método [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) para definir ou recuperar propriedades para todos os membros do conjunto de componentes.

Por esse motivo, os conjuntos de componentes são tratados como unidades. Por exemplo, um backup de um conjunto de componentes será bem-sucedido somente se o backup de todos os conjuntos de arquivos de todos os seus componentes for bem-sucedido.

No exemplo anterior, suponha que um arquivo no componente "Jan" (com o caminho lógico "writerData \\ conjunto2") seja um membro do conjunto de componentes definido por "writerData". Se um dos arquivos de "Jan" não for feito backup, um solicitante usará as informações de "writerData" (seu nome "writerData", seu caminho "" e seu tipo de componente) como argumentos ao definir [**IVssBackupComponents:: SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded) com **false** para indicar a falha do conjunto de componentes.

Da mesma forma, o estado retornado por [**IVssComponent:: GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded) para a instância de "writerData" da interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) se aplica não apenas a "writerData", mas também a todos os seus subcomponentes.

Além disso, se um gravador optar por alterar o destino de restauração usando [**IVssComponent:: SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget) da instância de [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)do "writerData", isso alteraria o destino de restauração para todos os conjuntos de arquivos de todos os subcomponentes de "writerData".

As propriedades a seguir se aplicam não a todo o componente, mas a arquivos ou conjuntos de arquivos específicos:

-   Mapeamentos de local alternativos: <dl>

[**IVssBackupComponents::AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping)  
    [**IVssComponent::GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping)  
    [**IVssComponent::GetAlternateLocationMappingCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmappingcount)  
    </dl>
-   Arquivos diferenciados: <dl>

[**IVssComponent::AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime)  
    [**IVssComponent::GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile)  
    [**IVssComponent::GetDifferencedFilesCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount)  
    </dl>
-   Arquivos parciais: <dl>

[**IVssComponent:: addparcialfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile)  
    [**IVssComponent:: getparcialfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)  
    [**IVssComponent::GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount)  
    </dl>
-   Destinos direcionados: <dl>

[**IVssComponent::AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget)  
    [**IVssComponent::GetDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget)  
    [**IVssComponent::GetDirectedTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtargetcount)  
    </dl>
-   Novos destinos: <dl>

[**IVssBackupComponents::AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)  
    [**IVssComponent::GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)  
    [**IVssComponent::GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount)  
    </dl>

Quando um solicitante acessa esses recursos para um subcomponente usando a interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) , ele usa as informações de componente para o componente de definição do conjunto de componentes, mas as informações de arquivo ou de conjunto de arquivos para o subcomponente.

Da mesma forma, se a propriedade puder ser acessada por meio da interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) , a instância correspondente ao subcomponente de definição será usada, mas os argumentos de arquivo ou de conjunto de arquivos serão extraídos do subcomponente.

Por exemplo, suponha que o subcomponente "Jan" (com o caminho lógico "writerData \\ conjunto2") tivesse um conjunto de arquivos com um caminho de "c: \\ Fred", uma especificação de arquivo de " \* . dat", e um sinalizador recursivo de **true** pode precisar ser restaurado para um local alternativo.

Se esse for o caso, um solicitante chamaria [**IVssBackupComponents:: AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping), usando informações de "writerData" (tipo de componente, um nome de componente de "writeData" e um caminho lógico de "") junto com as informações de conjunto de arquivos de "Jan" (caminho "c: \\ Fred", especificação de arquivo " \* . dat" e recursão é igual a **true**).

Observe que, nesse caso, as informações do conjunto de arquivos devem corresponder exatamente às informações do conjunto de arquivos usadas por [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)ou [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) para adicionar arquivos a Jan.

Da mesma forma, se um escritor quisesse adicionar um destino direcionado a um arquivo com o caminho "c: \\ Ethel" e o nome "Lucy. dat" gerenciado por "Jan" (com o caminho lógico "writerData \\ conjunto2"), ele usará a instância [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondente a "writerData", mas as informações de arquivo de "Jan".

## <a name="implicitly-included-components-in-the-restore-set"></a>Componentes incluídos implicitamente no conjunto de restauração

Os componentes que foram incluídos implicitamente em um backup podem ser incluídos explicitamente em uma restauração se forem selecionáveis para restauração. Conforme observado em [trabalhando com a seleção para a restauração e subcomponentes](working-with-selectability-for-restore-and-subcomponents.md), esses componentes são adicionados ao documento de componentes de backup usando o método [**IVssBackupComponents:: AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) .

No entanto, isso não cria uma nova instância da interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) , nem o componente é diretamente acessível por meio da interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) .

Em vez disso, um componente explicitamente incluído para restauração, mas incluído implicitamente para backup, deve ser acessado por meio de uma instância da interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondente ao componente que definiu o conjunto de componentes do qual ele era um membro no backup.

Por exemplo, para incluir explicitamente para Restore "Conjunto1", um subcomponente do selecionável para o componente de backup "writerData", você obteria informações sobre ele chamando o método [**IVssComponent:: GetRestoreSubcomponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponent) da instância de "writerData" da interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) .

 

 



