---
description: Trabalhar com componentes selecionados implicitamente requer acesso aos documentos de metadados do documento e do gravador dos componentes de backup.
ms.assetid: ede51931-be50-4286-818b-0e6122247bdd
title: Seleção e trabalho com propriedades de componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a735481d4bd0d7fdaa4102026b74ca78be947afbab24858d88d9210dd7bd4e6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751648"
---
# <a name="selectability-and-working-with-component-properties"></a>Seleção e trabalho com propriedades de componente

Trabalhar com componentes selecionados implicitamente requer acesso aos documentos de metadados do documento e do gravador dos componentes de backup.

Há dois motivos para isso:

-   Os dados do componente armazenados no documento componentes de backup (representado pela interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) ) não têm acesso às informações do conjunto de arquivos de componentes — especificação de arquivo, caminho e sinalizador de recursão. (Consulte [trabalhando com o documento componentes de backup](working-with-the-backup-components-document.md).)
-   Somente os componentes [*incluídos explicitamente*](vssgloss-e.md) no documento componentes de backup durante o backup têm suas informações armazenadas diretamente no documento componentes de backup. Os solicitantes e os gravadores devem usar as informações disponíveis por meio da interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) , em conjunto com as informações de [*caminho lógico*](vssgloss-l.md) e documentos de metadados do gravador para obter informações e definir propriedades de, componentes [*incluídos implicitamente*](vssgloss-i.md) .

O caso "myWriter" abordado em [um caminho lógico de componentes](logical-pathing-of-components.md) pode ser usado para ilustrar a seleção de backup.



| Nome do Componente | Caminho lógico            | Selecionável para backup | Selecionável para restauração | Incluído explicitamente |
|----------------|-------------------------|-----------------------|------------------------|---------------------|
| Executáveis  | ""                      | N                     | N                      | Y                   |
| "ConfigFiles"  | Executáveis           | N                     | N                      | Y                   |
| "LicenseInfo"  | ""                      | Y                     | N                      | Y                   |
| “Segurança”     | ""                      | Y                     | N                      | Y                   |
| UserInfo     | “Segurança”              | N                     | N                      | N                   |
| Certificado | “Segurança”              | N                     | N                      | N                   |
| "writerData"   | ""                      | Y                     | Y                      | Y                   |
| Conjunto1         | "writerData"            | N                     | Y                      | N                   |
| Janeiro          | "writerData \\ conjunto1"      | N                     | N                      | N                   |
| Dez          | "writerData \\ conjunto1"      | N                     | N                      | N                   |
| Conjunto2         | "writerData"            | N                     | Y                      | N                   |
| Janeiro          | "writerData \\ conjunto2"      | N                     | N                      | N                   |
| Dez          | "writerData \\ conjunto2"      | N                     | N                      | N                   |
| Consultá        | "writerData \\ QueryLogs" | N                     | N                      | N                   |
| Usos        | "writerData"            | Y                     | Y                      | N                   |
| Janeiro          | "uso de writerData \\ "     | N                     | N                      | N                   |
| Dez          | "uso de writerData \\ "     | N                     | N                      | N                   |



 

## <a name="implicitly-included-components-in-the-backup-set"></a>Componentes incluídos implicitamente no conjunto de backup

Ao examinar o documento de metadados do gravador do gravador (consulte [**IVssBackupComponents:: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata)) durante o backup, um solicitante deve armazenar uma lista de todos os componentes, seus [*caminhos lógicos*](vssgloss-l.md)e suas informações de conjunto de arquivos.

As informações de conjunto de arquivos e arquivo excluído serão necessárias para determinar uma lista de arquivos para qualquer componente incluído (explícita ou implicitamente).

Para não selecionável para componentes de backup sem seleção para os ancestrais de backup e selecionáveis para os componentes de backup que não definem um [*conjunto de componentes*](vssgloss-c.md), somente as informações de conjunto de arquivos e arquivo excluído serão necessárias para identificar todos os candidatos do componente para backup, pois esses componentes não definem subcomponentes.

Para componentes selecionáveis explicitamente incluídos para componentes de backup que definem um conjunto de componentes, os conjuntos de arquivos e excluem informações de arquivo para o componente de definição e todos os [*subcomponentes*](vssgloss-s.md) precisam ser usados para selecionar arquivos para backup.

Isso significa que os conjuntos de backup para os componentes "Executáveis", "ConfigFiles" e "LicenseInfo" só podem ser encontrados examinando os metadados do autor apenas para esses componentes usando suas instâncias da interface [**IVssWMComponent.**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)

No entanto, se writerData estiver explicitamente incluído no backup, você deverá examinar sua instância da interface [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) e aquelas de "Set1", "Jan" (com o caminho lógico "writerData \\ Set1"), "Dec" (com o caminho lógico "writerData \\ Set1"), "Set2", "Jan" (com o caminho lógico "writerData \\ Set2"), "Dec" (com o caminho lógico "writerData \\ Set2"), "Query", "Usage", "Jan" (com o caminho lógico "writerData Usage") e "Dec" (com o caminho lógico \\ "writerData \\ Usage").

Para fazer isso, um solicitante terá que primeiro identificar que o componente "writerData" (caminho lógico "") é selecionável. Em seguida, ele terá que verificar todos os outros componentes gerenciados pelo autor para determinar se o primeiro elemento em seu caminho lógico é "writerData". Esses componentes que têm "writerData" como os membros principais de seu caminho lógico são identificados como subcomponentes de "writerData" e são selecionados implicitamente quando ele é selecionado explicitamente.

Na verdade, uma verificação semelhante precisará ser feita para determinar que nenhum componente tem "LicenseInfo" como o membro à frente de seu caminho lógico e, portanto, que "LicenseInfo" não tem subcomponentes.

Devido à complexidade desse mecanismo no VSS, muitos autores de solicitantes podem achar útil criar suas próprias estruturas para armazenar informações de componente e conjunto de backup para componentes adicionados explicitamente e implicitamente.

## <a name="properties-of-implicitly-included-components"></a>Propriedades de componentes incluídos implicitamente

Durante as operações de restauração e backup, as instâncias das interfaces [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) e [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) são usadas para recuperar informações sobre componentes e para definir ou alterar as propriedades do componente. No entanto, somente os componentes explicitamente incluídos terão instâncias da interface **IVssComponent** ou estarão acessíveis à interface **IVssBackupComponents.**

Algumas propriedades têm escopo de todo o conjunto de componentes. Essas propriedades incluem o seguinte:

-   Status de backup e restauração: <dl>

[**IVssBackupComponents::SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)  
    [**IVssComponent::GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded)  
    [**IVssBackupComponents::SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus)  
    [**IVssComponent::GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus)  
    </dl>
-   Opções de backup e restauração: <dl>

[**IVssBackupComponents::SetBackupOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupoptions)  
    [**IVssComponent::GetBackupOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupoptions)  
    [**IVssBackupComponents::SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions)  
    [**IVssComponent::GetRestoreOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoreoptions)  
    </dl>
-   Mensagens de falha: <dl>

[**IVssComponent::SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg)  
    [**IVssComponent::SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg)  
    [**IVssComponent::SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg)  
    [**IVssComponent::SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg)  
    </dl>
-   Destinos de restauração: <dl>

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

Portanto, você usa a instância da interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) do membro de definição de um conjunto de componentes ou usa o nome, o tipo e o caminho lógico do membro definido com um método [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) para definir ou recuperar propriedades para todos os membros do conjunto de componentes.

Por esse motivo, os conjuntos de componentes são tratados como unidades. Por exemplo, um backup de um conjunto de componentes só será bem-sucedido se o backup de todos os conjuntos de arquivos de todos os seus componentes for bem-sucedido.

No exemplo anterior, suponha que um arquivo no componente "Jan" (com o caminho lógico "writerData Set2") seja membro do conjunto de componentes definido \\ por "writerData". Se um dos arquivos de "Jan" não tiver feito o back-up, um solicitante usará as informações de "writerData" (seu nome "writerData", seu caminho "" e seu tipo de componente) como argumentos ao definir [**IVssBackupComponents::SetBackupSucceeded com**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded) **false** para indicar a falha do conjunto de componentes.

Da mesma forma, o estado retornado por [**IVssComponent::GetBackupSucceededed para**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded) a instância de "writerData" da interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) se aplica não apenas a "writerData", mas a todos os seus subcomponentes também.

Além disso, se um autor optar por alterar o destino de restauração usando [**IVssComponent::SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget) da instância de "writerData" de [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent), isso alterará o destino de restauração de todos os conjuntos de arquivos de todos os subcomponentes de "writerData".

As propriedades a seguir se aplicam não a todo o componente, mas a arquivos ou conjuntos de arquivos específicos:

-   Mapeamentos de localização alternativos: <dl>

[**IVssBackupComponents::AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping)  
    [**IVssComponent::GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping)  
    [**IVssComponent::GetAlternateLocationMappingCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmappingcount)  
    </dl>
-   Arquivos com diferenças: <dl>

[**IVssComponent::AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime)  
    [**IVssComponent::GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile)  
    [**IVssComponent::GetDifferencedFilesCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount)  
    </dl>
-   Arquivos parciais: <dl>

[**IVssComponent::AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile)  
    [**IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)  
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

Quando um solicitante acessa esses recursos para um subcomponente usando a interface [**IVssBackupComponents,**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) ele usa as informações de componente para o componente de definição do conjunto de componentes, mas as informações de arquivo ou conjunto de arquivos para o subcomponente.

Da mesma forma, se a propriedade estiver acessível por meio da interface [**IVssComponent,**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) a instância correspondente ao subcomponente de definição será usada, mas os argumentos do arquivo ou do conjunto de arquivos serão retirados do subcomponente.

Por exemplo, suponha que o subcomponente "Jan" (com o caminho lógico "writerData Set2") tinha um arquivo definido com um caminho de "c: fred", uma especificação de arquivo de " .dat" e um sinalizador \\ \\ \* recursivo de **true** talvez tenha que ser restaurado para um local alternativo.

Se esse fosse o caso, um solicitante chamaria [**IVssBackupComponents::AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping)usando as informações de "writerData" (tipo de componente, um nome de componente de "writeData" e um caminho lógico de "") juntamente com as informações do conjunto de arquivos de "Jan" (caminho "c: set", especificação de arquivo \\ " \* .dat" e recursão igual a **true**).

Observe que, nesse caso, as informações do conjunto de arquivos devem corresponder exatamente às informações do conjunto de arquivos usadas por [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)ou [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) para adicionar arquivos a Jan.

Da mesma forma, se um autor quisesse adicionar um destino direcionado a um arquivo com um caminho de "c: file" e o nome "ltd.dat" gerenciado por "Jan" (com o caminho lógico "writerData Set2"), ele usaria a instância \\ \\ [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondente a "writerData", mas as informações de arquivo de "Jan".

## <a name="implicitly-included-components-in-the-restore-set"></a>Componentes incluídos implicitamente no conjunto de restauração

Os componentes que foram incluídos implicitamente em um backup poderão ser incluídos explicitamente em uma restauração se eles puderem ser restaurados. Conforme registrado em Trabalhando com a seleção para restauração e [subcomponentes,](working-with-selectability-for-restore-and-subcomponents.md)esses componentes são adicionados ao Documento de Componentes de Backup usando o método [**IVssBackupComponents::AddRestoreSubcomponent.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent)

No entanto, isso não cria uma nova instância da interface [**IVssComponent,**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) nem o componente está diretamente acessível por meio da interface [**IVssBackupComponents.**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)

Em vez disso, um componente explicitamente incluído para restauração, mas implicitamente incluído para backup, deve ser acessado por meio de uma instância da interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondente ao componente que definiu o conjunto de componentes do qual ele era membro no backup.

Por exemplo, para incluir explicitamente para a restauração "Set1", um subcomponente do selecionável para o componente de backup "writerData", você obteria informações sobre isso chamando o método [**IVssComponent::GetRestoreSubcomponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponent) da instância de "writerData" da interface [**IVssComponent.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)

 

 



