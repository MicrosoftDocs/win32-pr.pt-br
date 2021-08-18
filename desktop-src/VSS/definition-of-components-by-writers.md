---
description: Os componentes são definidos por e instautados por autores em seu Documento de Metadados do Writer em resposta a um evento Identificar no início de uma operação de backup (consulte Visão geral da inicialização de backup) quando o Documento de Metadados do Writer é populado.
ms.assetid: 5e1c3f9b-ca83-4e70-963b-0a237c6f4b0d
title: Definição de componentes por autores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82fa08acba3c49cd99e83a5dcc901d4a12108a9dc6dde9891add93bcc54e3566
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136370"
---
# <a name="definition-of-components-by-writers"></a>Definição de componentes por autores

Os componentes são definidos por e instautados por [](vssgloss-i.md) autores em seu Documento de Metadados do Writer em resposta a um evento Identificar no início de uma operação de backup (consulte Visão geral da inicialização de [backup](overview-of-backup-initialization.md)) quando o Documento de Metadados do Writer é populado.

Ao criar um componente em seu Documento de Metadados do Writer, usando [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) e [**IVssCreateWriterMetadata::AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent), um autor deve especificar:

-   Se o componente é [ *selecionável para backup*](vssgloss-s.md)
-   Um tipo de componente
-   Um nome de componente (que deve ser exclusivo não apenas em uma determinada instância [*de writer,*](vssgloss-w.md) mas em todas as instâncias de writer)
-   Se o componente tem metadados específicos do autor associados a ele
-   Se o autor requer notificação após um backup bem-sucedido

Opcionalmente, os autores podem especificar:

-   O caminho lógico de [*um componente*](vssgloss-l.md) (que deve ser exclusivo não apenas em uma determinada instância de writer, mas em todas as instâncias de autor)
-   Uma descrição do componente (ou legenda)
-   Um ícone a ser usado com GUIs para indicar o componente

Não é necessário que um componente realmente contenha arquivos. Esse tipo de componente vazio ou "fictício" pode ser útil na organização de componentes. Esse componente pode ser usado [](vssgloss-c.md) para definir um conjunto de componentes e um componente de um autor (consulte [Caminho lógico de componentes](logical-pathing-of-components.md)).

## <a name="setting-up-component-organization"></a>Configurando a organização do componente

Definir a selecionabilidade de um componente (sua selecionável [](vssgloss-l.md) para [*backup*](vssgloss-s.md)e sua selecionável para restauração [*)*](/windows)e seus caminhos lógicos [](vssgloss-c.md) permitem que um autor imigure ou torna opcional a inclusão de determinados componentes em uma operação de backup ou restauração e para agrupar componentes em conjuntos de componentes com um componente selecionável atuando como um ponto de entrada para todo o grupo. [](vssgloss-s.md)

A associação nesses grupos determina quais componentes serão usados durante operações de backup e restauração. Usando "selecionável" para significar voltar para a operação de backup e selecionável para restauração para a operação de restauração, os desenvolvedores devem entender que:

-   Se algum componente gerenciado por um determinado autor for [](vssgloss-e.md) feito backup, um [](vssgloss-c.md) solicitante deverá incluir explicitamente todos os componentes não selecionáveis sem ancestrais selecionáveis em seu caminho lógico para o Documento de Componentes de Backup e fazer backup e restaurar esses componentes como um grupo. [](vssgloss-l.md)
-   Um solicitante tem a opção de adicionar explicitamente componentes selecionáveis ao Documento de Componentes de Backup durante operações de backup e restauração; depois de adicionado, o componente deve ser feito backup ou restaurado.
-   Se um componente for selecionável, o componente e todos os [*seus subcomponentes*](vssgloss-s.md) (conforme definido por caminhos lógicos) formarão um conjunto de componentes, que pode ser tratado como uma única unidade que pode, opcionalmente, participar de operações de backup e restauração.
-   Um solicitante nunca adiciona explicitamente um componente não selecionável com ancestrais selecionáveis, um subcomponente em um conjunto de componentes, ao seu Documento de Componentes de Backup durante operações de backup e restauração. Esses componentes deverão ser [*incluídos implicitamente*](/windows) se seu ancestral selecionável for adicionado explicitamente; nesse caso, eles deverão ser incluídos em backup ou restaurados (consulte Uso de componentes pelo [solicitante).](use-of-components-by-the-requestor.md)
-   Um componente selecionável com um ancestral selecionável ainda é [*um subcomponente*](vssgloss-s.md) (um membro de um conjunto de componentes) e pode ser incluído implicitamente se seu ancestral selecionável for incluído explicitamente na operação. Nesse caso, suas informações não são adicionadas ao Documento de Componentes de Backup. Se seu ancestral selecionável não estiver incluído na operação, o componente poderá ser selecionado explicitamente para inclusão na operação, caso em que suas informações serão incluídas no Documento de Componentes de Backup.
-   Um subcomponente incluído implicitamente em um backup pode ser incluído explicitamente em uma operação de restauração, independentemente do status de qualquer ancestral selecionável, se for selecionável para restauração. Qualquer subcomponente selecionável para restauração incluído durante uma operação de restauração deve ter suas informações adicionadas ao Documento de Componentes de Backup.
-   Um autor que não teve nenhum componente adicionado explicitamente ao Documento de Componentes de Backup antes da geração de [*eventos PrepareForBackup*](vssgloss-p.md) e [*PreRestore*](vssgloss-p.md) não receberá mais eventos vss.

Para obter mais informações, consulte [Trabalhando com selecionabilidade e caminhos lógicos.](working-with-selectability-and-logical-paths.md)

## <a name="adding-files-to-a-component"></a>Adicionando arquivos a um componente

Um componente contém informações de arquivo na forma de um conjunto [*de arquivos*](vssgloss-f.md) que contém:

-   Um diretório raiz dos arquivos no componente.
-   Uma especificação de arquivo para os arquivos no componente.
-   Um sinalizador que indica se a especificação do componente é recursiva.

Dependendo do tipo de componente, que pode ser um banco de dados ou um grupo de arquivos e (no caso de componentes de banco de dados) se os arquivos a serem carregados são arquivos de dados ou de log, um autor chama [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)ou [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) para adicionar um conjunto de arquivos.

Ao usar essas funções, você deve especificar os arquivos a serem adicionados ao conjunto de arquivos da seguinte forma:

-   *wszPath:* esse é o caminho para o diretório que contém os arquivos a serem adicionados ao conjunto de arquivos. Se o *parâmetro bRecursive* for definido como **true**, o parâmetro *wszPath* especificará uma hierarquia de diretórios a serem percorridos recursivamente e todos os diretórios deverão ser recriados, incluindo diretórios vazios.
-   *wszFilespec:* essa cadeia de caracteres especifica os arquivos em cada diretório a serem adicionados ao conjunto de arquivos.

Por exemplo, suponha que a seguinte estrutura de diretório exista:

<dl> C: \\ Directory1 \\File1.txt  
C: \\ Directory1 \\File2.txt  
C: \\ Directory1 \\ Directory2 \\File1.txt  
C: \\ Directory1 \\ Directory2 \\File2.txt  
C: \\ Directory1 \\ Directory3\\  
</dl>

Se o autor especificar "C: \\ Directory1" para *wszPath*, "File1. \* " para *wszFilespec* e **true** para *bRecursive*, o solicitante deverá incluir estes arquivos:

<dl> C: \\ Directory1 \\File1.txt  
C: \\ Directory1 \\ Directory2 \\File1.txt  
</dl>

Se o autor especificar "C: \\ Directory1" para *wszPath*, " \* " para *wszFilespec* e **true** para *bRecursive*, o solicitante deverá incluir estes arquivos:

<dl> C: \\ Directory1 \\File1.txt  
C: \\ Directory1 \\File2.txt  
C: \\ Directory1 \\ Directory2 \\File1.txt  
C: \\ Directory1 \\ Directory2 \\File2.txt  
</dl>

Se o autor especificar "C: \\ Directory1" para *wszPath*, " \* " para *wszFilespec* e **false** para *bRecursive*, o solicitante deverá incluir estes arquivos:

<dl> C: \\ Directory1 \\File1.txt  
C: \\ Directory1 \\File2.txt  
</dl>

Em todos os exemplos anteriores, sempre que o autor especifica **true** para *bRecursive,* o diretório vazio C: \\ Directory1 Directory3 deve ser \\ \\ recriado.

Para um conjunto de arquivos adicionado a um componente de grupo de arquivos, em casos em que os arquivos atualmente em disco não estão no que o autor consideraria o local apropriado ou padrão, um autor tem a opção de adicionar um caminho alternativo. Nesses casos, a definição do caminho do conjunto de arquivos contém o local normal dos arquivos e para onde os arquivos devem ser restaurados, enquanto o caminho alternativo contém o local atual dos arquivos a serem armazenados em backup.

Todos os arquivos no conjunto de arquivos devem existir no momento do backup. Os solicitantes devem assumir que todos os arquivos listados no conjunto de arquivos são necessários para o backup e falharão no backup se algum arquivo estiver ausente. Observe que quando " \* " é especificado para o parâmetro *wszFilespec,* ele pode corresponder a zero ou mais arquivos.

Observe que esses atributos do Documento de Metadados de Autor como mapeamentos de localização alternativos, arquivos explicitamente incluídos e excluídos e métodos de restauração são definidos no nível do autor, não no nível do componente. (Para obter mais informações, consulte [Trabalhando com o documento de metadados do autor](working-with-the-writer-metadata-document.md).)

## <a name="component-definition-for-backup-and-restore-operations"></a>Definição de componente para operações de backup e restauração

As operações de restauração [](vssgloss-i.md)e backup necessariamente geram um evento Identify e, para backups e restaurações, ele será tratado pelo mesmo [**método CVssWriter::OnIdentify.**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)

Durante as operações de backup, os solicitantes usam as informações retornadas pelos métodos [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) de um autor para determinar quais autores estão presentes no sistema e, em seguida, determinar qual dos seus arquivos fazer backup.

Durante as operações de restauração, as informações retornadas pelo evento [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) de um autor são usadas apenas para estabelecer a identidade e o status dos autores atualmente presentes no sistema; as informações de especificação de arquivo geradas durante uma restauração não são usadas. Em vez disso, os Documentos de Metadados do Writer armazenados em tempo de backup são usados para obter esses dados.

Depois de geradas durante uma operação de backup, as informações do componente de writer, juntamente com o restante das informações do autor, são salvas para serem recuperadas para dar suporte a operações de restauração. Normalmente, é responsabilidade do solicitante armazenar essas informações.

 

 
