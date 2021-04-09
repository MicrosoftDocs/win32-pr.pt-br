---
description: 'O documento de metadados do gravador contém três conjuntos de dados: informações de identificação e classificação do gravador, especificações de nível de gravador e dados de componentes.'
ms.assetid: 1a84790a-8f46-4e1b-8e45-5036830e8fee
title: Conteúdo do documento de metadados do gravador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f222977f1c8d785e6f69613f219545dc3402af7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010500"
---
# <a name="writer-metadata-document-contents"></a>Conteúdo do documento de metadados do gravador

O documento de metadados do gravador contém três conjuntos de dados: informações de identificação e classificação do gravador, especificações de nível de gravador e dados de componentes.

## <a name="writer-identification-information"></a>Informações de identificação do gravador

As informações de identificação e classificação do gravador incluem o seguinte:

-   Nome do gravador
-   [*ID da classe do gravador*](vssgloss-w.md)
-   [*Instância do gravador*](vssgloss-w.md)
-   Como os dados gerenciados pelo gravador são usados no sistema host (consulte [**tipo de \_ uso \_ do VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type))
-   O tipo de dados gerenciados pelo gravador (consulte [**\_ \_ tipo de origem VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type))

Com exceção da instância do Writer, que é exclusiva e é gerada pelo sistema quando um objeto [**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) é inicializado, todos esses valores são definidos por um gravador quando ele chama [**CVssWriter:: Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize) e estão disponíveis para um solicitante chamando [**IVssExamineWriterMetadata:: getidentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity).

Como a instância do gravador é gerada exclusivamente, uma instância de gravador armazenada recuperada de um documento de metadados do gravador armazenado provavelmente não será útil.

Ao verificar [**o \_ \_ tipo de uso do VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type), um aplicativo pode determinar se um gravador está gerenciando dados gerais do aplicativo ou se os arquivos com os quais ele trabalha fazem parte do estado de inicialização do sistema ou são usados por um serviço do sistema. Os aplicativos de backup e restauração precisam respeitar os tipos de uso para ajudar a manter a estabilidade do sistema.

O sinalizador de [**\_ \_ tipo de origem do VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type) indica que tipo de aplicativo o qual o gravador está gerenciando os dados é executado durante a operação normal.

Atualmente, a distinção é limitada à especificação de se o gravador produz arquivos como parte de operações de banco de dados transacionais ou não transações, ou se os arquivos são o resultado de um tipo de atividade mais geral. Essa lista pode crescer ao longo do tempo. Essas informações podem ser úteis para determinar o nível comum de atividade esperado nos arquivos de um gravador.

## <a name="writer-level-specification"></a>Especificação de Writer-Level

As especificações de nível de gravador contêm informações que são o gravador em seu escopo, aplicando-se a todos os dados independentes dos quais um componente o gerencia.

Um gravador sempre deve especificar [*métodos de restauração*](vssgloss-r.md).

Opcionalmente, ele pode especificar o seguinte:

-   Excluir lista de arquivos
-   [*Mapeamentos alternativos de local*](vssgloss-a.md) para restauração

As listas de arquivos include e Exclude contêm informações de arquivo além daquelas nos componentes, e sua especificação substitui a especificação de componente.

## <a name="restore-method-specification"></a>Especificação do método de restauração

O [*método Restore*](vssgloss-r.md) é definido no documento de metadados do gravador por [**IVssCreateWriterMetadata:: SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod) e recuperado por um solicitante com [**IVssExamineWriterMetadata:: GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod).

Ao definir um método de restauração, um gravador indica a maneira preferida de restauração de arquivos, também conhecido como destino de restauração original, para todos os arquivos gerenciados por um gravador. Por exemplo, o método Restore especifica se todos os arquivos gerenciados por um gravador devem ter permissão para substituir os arquivos atualmente no disco. (Consulte [configurações de restauração do VSS](vss-restore-configurations.md) e [**enumeração do VSS \_ RESTOREMETHOD \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) para obter mais informações.)

## <a name="exclude-file-list-specification"></a>Excluir especificação de lista de arquivos

A lista de exclusões permite o ajuste fino das especificações de curinga em componentes, impedindo explicitamente a inclusão de determinados arquivos em um conjunto de backup.

Por exemplo, um componente pode ter um [*conjunto de arquivos*](vssgloss-f.md) contendo uma especificação de arquivo de c: \\ Database \\ \* . \* Embora essa seja uma definição conveniente, ocasionalmente pode haver arquivos temporários gerados (talvez no formato \* . tmp) e o gravador sempre quer impedir seu backup.

Nesse caso, um gravador adicionaria \* . tmp à sua lista de exclusões usando [**IVssCreateWriterMetadata:: AddExcludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles). Essa especificação pode ser recursiva.

Um solicitante consulta essas informações usando [**IVssExamineWriterMetadata::**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getexcludefile)getdelet.

A lista de arquivos de exclusão tem precedência sobre listas de arquivos de componentes.

Assim, a lista de arquivos especificados para backup em um documento de metadados do gravador consistia em todos os arquivos especificados nos componentes [*explicitamente incluídos*](vssgloss-e.md) e nos componentes [*implicitamente incluídos*](vssgloss-i.md) , menos todos os arquivos excluídos.

## <a name="alternate-location-mappings-specification"></a>Especificação de mapeamentos de local alternativo

Mapeamentos de local alternativos são inicialmente definidos durante a criação de um documento de metadados do gravador e indicam um local no disco para o qual os arquivos podem ser restaurados se a restauração de um arquivo no local original não for possível.

As informações são adicionadas como uma cadeia de caracteres larga terminada em nulo com [**IVssCreateWriterMetadata:: AddAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping) e recuperadas como um objeto [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) por [**IVssExamineWriterMetadata:: GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping).

Apesar do fato de que mapeamentos de local alternativos são especificados e examinados usando as interfaces de nível de gravador ([**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) e [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)), eles são especificados em termos de [*conjuntos de arquivos*](vssgloss-f.md). O conjunto de arquivos usado na especificação de um mapeamento de local alternativo (caminho, especificação de arquivo e sinalizador de recursão) deve corresponder a um dos conjuntos de arquivos já adicionados a um dos componentes do gravador (consulte [Adicionando arquivos aos componentes](definition-of-components-by-writers.md)).

Para obter mais informações, consulte [locais de backup e restauração não padrão](non-default-backup-and-restore-locations.md).

## <a name="component-level-information"></a>Informações de Component-Level

Os [*componentes*](vssgloss-c.md) são coleções de arquivos que formam uma unidade lógica para fins de backup e restauração. Todos os arquivos em um componente (exceto aqueles explicitamente excluídos) devem ser armazenados em backup e restaurados como uma unidade.

Os gravadores adicionam componentes usando o [**componente IVssCreateWriterMetadata::**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent)Add, especificando as seguintes informações de componente:

-   Tipo
-   Nome
-   Caminho lógico (se houver)
-   Recurso com suporte
-   [*Seleção*](vssgloss-s.md)
-   Metadados a serem usados pelo gravador durante a restauração
-   Exibir informações
-   Informações de notificação

A [*seleção de backup*](vssgloss-s.md) e a [*seleção de restauração*](vssgloss-s.md) são completamente independentes umas das outras, e um gravador as usa em conjunto com caminhos lógicos para indicar as relações entre os vários componentes que ele gerencia. Os gravadores podem indicar quais componentes são necessários para [*inclusão explícita*](vssgloss-e.md) (aqueles que podem ser incluídos explicitamente no critério de um solicitante) e aqueles que só podem ser [*incluídos implicitamente*](vssgloss-i.md). (Consulte [trabalhando com a seleção e os caminhos lógicos](working-with-selectability-and-logical-paths.md).)

Os arquivos são adicionados a um determinado componente usando [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)ou [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles). (Consulte [Adicionando arquivos aos componentes](definition-of-components-by-writers.md).)

Ao adicionar arquivos a um componente durante o backup, um gravador deve especificar um conjunto de arquivos (um caminho, uma especificação de arquivo e um sinalizador de recursão) que define os arquivos cujo backup será feito.

Os gravadores também podem especificar um [*caminho alternativo*](vssgloss-a.md) para backup, o que não deve ser confundido com [*mapeamentos de local alternativos*](vssgloss-a.md) mencionados anteriormente. Esse caminho alternativo indica um local não padrão do qual os arquivos devem ser copiados quando um volume é submetido a backup.

As informações sobre um determinado componente no documento de metadados do gravador podem ser obtidas por meio de uma interface [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) retornada por [**IVssExamineWriterMetadata:: GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent).

Os arquivos e caminhos são retornados em [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) como objetos [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) .

As informações de componente do gravador são discutidas em detalhes em [definição de componentes por gravadores](definition-of-components-by-writers.md).

 

 



