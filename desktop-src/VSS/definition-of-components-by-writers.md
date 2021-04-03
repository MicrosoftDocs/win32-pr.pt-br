---
description: Os componentes são definidos por e instanciados por gravadores no documento de metadados do gravador em resposta a um evento de identificação no início de uma operação de backup (consulte Visão geral da inicialização do backup) quando o documento de metadados do gravador é preenchido.
ms.assetid: 5e1c3f9b-ca83-4e70-963b-0a237c6f4b0d
title: Definição de componentes por gravadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa5383e9bc87620f23bb2a3ab067c1913a323782
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837261"
---
# <a name="definition-of-components-by-writers"></a>Definição de componentes por gravadores

Os componentes são definidos por e instanciados por gravadores no documento de metadados do gravador em resposta a um [*evento de identificação*](vssgloss-i.md) no início de uma operação de backup (consulte [visão geral da inicialização do backup](overview-of-backup-initialization.md)) quando o documento de metadados do gravador é preenchido.

Ao criar um componente em seu documento de metadados do gravador, usando [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) e [**IVssCreateWriterMetadata:: addcomponente**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent), um gravador deve especificar:

-   Se o componente é [ *selecionável para backup*](vssgloss-s.md)
-   Um tipo de componente
-   Um nome de componente (que deve ser exclusivo não apenas em uma determinada [*instância do gravador*](vssgloss-w.md) , mas em todas as instâncias do gravador)
-   Se o componente tem quaisquer metadados específicos do gravador associados a ele
-   Se o gravador requer uma notificação após um backup bem-sucedido

Os gravadores podem especificar opcionalmente:

-   Um [*caminho lógico*](vssgloss-l.md) do componente (que deve ser exclusivo não apenas dentro de uma determinada instância do gravador, mas em todas as instâncias do gravador)
-   Uma descrição do componente (ou legenda)
-   Um ícone a ser usado com GUIs para indicar o componente

Não é necessário que um componente contenha realmente qualquer arquivo. Esse tipo de componente vazio ou "fictício" pode ser útil para organizar componentes. Esse componente pode ser usado para definir um [*conjunto de componentes*](vssgloss-c.md) e um componente do gravador (consulte o [caminho lógico de componentes](logical-pathing-of-components.md)).

## <a name="setting-up-component-organization"></a>Configurando a organização do componente

Definir a [*seleção*](vssgloss-s.md) de um componente (sua [*seleção de backup*](vssgloss-s.md)e sua [*seleção de restauração*](/windows)) e seus [*caminhos lógicos*](vssgloss-l.md) permite que um gravador exija ou faça opcional a inclusão de determinados componentes em uma operação de backup ou restauração e agrupe componentes em [*conjuntos de componentes*](vssgloss-c.md) com um componente selecionável atuando como um ponto de entrada para todo o grupo.

A associação nesses agrupamentos determina quais componentes serão usados durante as operações de backup e restauração. Usando "selecionável" para significar a selecionável para voltar para operação de backup e selecionável para restauração para a operação de restauração, os desenvolvedores devem entender que:

-   Se for feito backup de qualquer componente gerenciado por um determinado gravador, um solicitante deverá [*incluir explicitamente*](vssgloss-e.md) todos os [*componentes*](vssgloss-c.md) não selecionáveis sem os ancestrais selecionáveis em seu [*caminho lógico*](vssgloss-l.md) para o documento de componentes de backup e fazer backup e restaurar esses componentes como um grupo.
-   Um solicitante tem a opção de adicionar explicitamente componentes selecionáveis ao documento de componentes de backup durante as operações de backup e restauração; Depois de adicionado, o backup do componente deve ser feito ou restaurado.
-   Se um componente for selecionável, o componente e todos os seus [*Subcomponentes*](vssgloss-s.md) (conforme definido por caminhos lógicos) formam um conjunto de componentes, que pode ser tratado como uma única unidade que pode, opcionalmente, participar de operações de backup e restauração.
-   Um solicitante nunca adiciona explicitamente um componente não selecionável com ancestrais selecionáveis, um subcomponente em um conjunto de componentes, ao documento de componentes de backup durante as operações de backup e restauração. Esses componentes devem ser [*incluídos implicitamente*](/windows) se seu ancestral selecionável for explicitamente adicionado, caso em que eles devem ser armazenados em backup ou restaurados (consulte [uso de componentes pelo solicitante](use-of-components-by-the-requestor.md)).
-   Um componente selecionável com um ancestral selecionável ainda é um [*subcomponente*](vssgloss-s.md) (um membro de um conjunto de componentes) e pode ser incluído implicitamente se seu ancestral selecionável está explicitamente incluído na operação. Nesse caso, suas informações não são adicionadas ao documento de componentes de backup. Se seu ancestral selecionável não estiver incluído na operação, o componente poderá ser explicitamente selecionado para inclusão na operação, caso em que suas informações estão incluídas no documento de componentes de backup.
-   Um subcomponente incluído implicitamente em um backup pode ser incluído explicitamente em uma operação de restauração, independentemente do status de qualquer ancestral selecionável, se for selecionável para restauração. Qualquer selecionável para o subcomponente de restauração incluído durante uma operação de restauração deve ter suas informações adicionadas ao documento de componentes de backup.
-   Um gravador que não tinha nenhum componente adicionado explicitamente ao documento de componentes de backup antes da geração de eventos [*PrepareForBackup*](vssgloss-p.md) e [*prerestore*](vssgloss-p.md) não receberá nenhum outro evento do VSS.

Para obter mais informações, consulte [trabalhando com a seleção e os caminhos lógicos](working-with-selectability-and-logical-paths.md).

## <a name="adding-files-to-a-component"></a>Adicionando arquivos a um componente

Um componente contém informações de arquivo na forma de um [*conjunto de arquivos*](vssgloss-f.md) que contém:

-   Um diretório raiz dos arquivos no componente.
-   Uma especificação de arquivo para os arquivos no componente.
-   Um sinalizador que indica se a especificação do componente é recursiva.

Dependendo do tipo de componente, que pode ser um banco de dados ou um grupo de arquivos, e (no caso de componentes de banco de dado) se os arquivos a serem carregados são arquivos de log ou data, um gravador chama [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)ou [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) para adicionar um conjunto de arquivos.

Ao usar essas funções, você deve especificar os arquivos a serem adicionados ao conjunto de arquivos da seguinte maneira:

-   *wszPath*: esse é o caminho para o diretório que contém os arquivos a serem adicionados ao conjunto de arquivos. Se o parâmetro *bRecursive* for definido como **true**, o parâmetro *wszPath* especificará uma hierarquia de diretórios a serem atravessados recursivamente e todos os diretórios deverão ser recriados, incluindo diretórios vazios.
-   *wszFilespec*: essa cadeia de caracteres especifica os arquivos em cada diretório a ser adicionado ao conjunto de arquivos.

Por exemplo, suponha que exista a seguinte estrutura de diretório:

<dl> C: \\ Directory1 \\File1.txt  
C: \\ Directory1 \\File2.txt  
C: \\ directory1 \\ Directory2 \\File1.txt  
C: \\ directory1 \\ Directory2 \\File2.txt  
C: \\ directory1 \\ Directory3\\  
</dl>

Se o gravador especificar "C: \\ directory1" para *wszPath*, "arquivo1. \* " para *wszFilespec* e **true** para *bRecursive*, o solicitante deverá incluir estes arquivos:

<dl> C: \\ Directory1 \\File1.txt  
C: \\ directory1 \\ Directory2 \\File1.txt  
</dl>

Em vez disso, o gravador especifica "C: \\ directory1" para *wszPath*, " \* " para *wszFilespec* e **true** para *bRecursive*, o solicitante deve incluir estes arquivos:

<dl> C: \\ Directory1 \\File1.txt  
C: \\ Directory1 \\File2.txt  
C: \\ directory1 \\ Directory2 \\File1.txt  
C: \\ directory1 \\ Directory2 \\File2.txt  
</dl>

Se o gravador especificar "C: \\ directory1" para *wszPath*, " \* " para *wszFilespec* e **false** para *bRecursive*, o solicitante deverá incluir estes arquivos:

<dl> C: \\ Directory1 \\File1.txt  
C: \\ Directory1 \\File2.txt  
</dl>

Em todos os exemplos anteriores, sempre que o gravador especifica **true** para *bRecursive*, o diretório vazio C: \\ directory1 \\ Directory3 \\ deve ser recriado.

Para um conjunto de arquivos adicionado a um componente de grupo de arquivos, nos casos em que os arquivos atualmente em disco não estão no que o gravador consideraria o local apropriado ou padrão, um gravador tem a opção de adicionar um caminho alternativo. Nesses casos, a definição do conjunto de arquivos do caminho contém o local normal dos arquivos e para onde os arquivos devem ser restaurados, enquanto o caminho alternativo contém o local atual dos arquivos cujo backup será feito.

Todos os arquivos no conjunto de arquivos devem existir no momento do backup. Os solicitantes devem assumir que todos os arquivos listados no conjunto de arquivos são necessários para o backup e irão falhar o backup se algum arquivo estiver ausente. Observe que quando " \* " é especificado para o parâmetro *wszFilespec* , ele pode corresponder a zero ou mais arquivos.

Observe que esses atributos de documento de metadados do gravador como mapeamentos de local alternativo, arquivos explicitamente incluídos e excluídos, e métodos de restauração são definidos no nível do gravador, não no nível do componente. (Para obter mais informações, consulte [trabalhando com o documento de metadados do gravador](working-with-the-writer-metadata-document.md).)

## <a name="component-definition-for-backup-and-restore-operations"></a>Definição de componente para operações de backup e restauração

As operações de restauração e de backup geram, necessariamente, um [*evento de identificação*](vssgloss-i.md)e, para backups e restaurações, elas serão tratadas pelo mesmo método [**CVssWriter:: onidentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) .

Durante as operações de backup, os solicitantes usam as informações retornadas pelos métodos [**CVssWriter:: Onidentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) de um gravador para determinar quais gravadores estão presentes no sistema e, em seguida, para determinar em quais arquivos fazer backup.

Durante as operações de restauração, as informações retornadas pelo evento [**CVssWriter:: Onidentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) de um gravador são usadas somente para estabelecer a identidade e o status dos gravadores atualmente presentes no sistema; as informações de especificação de arquivo geradas durante uma restauração não são usadas. Em vez disso, os documentos de metadados do gravador armazenados no momento do backup são usados para obter esses dados.

Depois de gerada durante uma operação de backup, as informações de componente do gravador, juntamente com as informações do gravador, são salvas para serem recuperadas para dar suporte a operações de restauração. Normalmente, é responsabilidade do solicitante armazenar essas informações.

 

 
