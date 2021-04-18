---
description: O gravador de teste é um utilitário que você pode usar para testar aplicativos do solicitante do VSS.
ms.assetid: 02434cb9-390c-4cf0-9941-b833ace55685
title: Ferramenta de gravador de teste do VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61ffdbb513697a701866be5ceeb40168e8c28368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763409"
---
# <a name="vss-test-writer-tool"></a>Ferramenta de gravador de teste do VSS

O gravador de teste é um utilitário que você pode usar para testar aplicativos do solicitante do VSS. Esse gravador pode ser configurado para executar quase todas as ações que um gravador VSS pode executar. Além disso, o gravador de teste executa verificações extensivas para garantir que o solicitante tenha tratado corretamente essas ações de gravador.

Cada instância do gravador é inicializada com um arquivo de configuração XML que descreve exatamente quais componentes serão relatados pelo gravador e como o gravador se comporta. O gravador pode ser configurado para relatar vários tipos de cenários, incluindo cenários mais complicados usando as interfaces incrementais e diferenciais. O gravador executará verificações em vários pontos durante o processo para garantir que o solicitante esteja se comportando de maneira adequada. Depois que a restauração for concluída, o gravador verificará se todos os arquivos necessários foram restaurados sem corrupção. O gravador também pode ser configurado para executar outras operações, como eventos específicos com falha.

> [!Note]  
> Essa ferramenta está incluída no SDK (Software Development Kit) do Microsoft Windows para Windows Vista e posterior. Você pode baixar o SDK do Windows do [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx) .

 

Na instalação do SDK do Windows, a ferramenta VssSampleProvider pode ser encontrada em `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (para o Windows de 64 bits) e `%Program Files(x86)%\Windows Kits\8.1\bin\x86` .

## <a name="running-the-test-writer-tool"></a>Executando a ferramenta de gravador de teste

Para iniciar o gravador de teste, digite o seguinte no prompt de comando:

 *Arquivo config-* vswriter.exe

em que *config-file* é o caminho para um arquivo de configuração que especifica o comportamento desse gravador.

Para interromper o gravador de teste, pressione CTRL + C.

Várias instâncias do gravador de teste podem ser executadas ao mesmo tempo. No entanto, cada instância do gravador relatará a mesma ID de classe de gravador (embora uma ID de instância de gravador diferente), portanto, os caminhos lógicos e os nomes de componentes devem ser exclusivos em todas as instâncias em execução simultaneamente do gravador.

Para garantir que o gravador possa verificar corretamente se o solicitante cumpriu as especificações de arquivo de exclusão, todos os arquivos dos quais foi feito backup devem ser excluídos do volume original antes de tentar restaurá-los. É recomendável que um modelo de cada cenário de gravador seja armazenado, para que o cenário possa ser facilmente recriado.

## <a name="using-a-configuration-file"></a>Usar um Arquivo de Configuração

O arquivo de configuração de exemplo a seguir, vswriter \_config.xml, pode ser encontrado em `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\vsstools` plataformas x86 e `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\x64\vsstools` em plataformas x64.

``` syntax
<TestWriter usage="USER_DATA">

    <RestoreMethod method="RESTORE_IF_CAN_BE_REPLACED"
                   writerRestore="always"
                   rebootRequired="no" />

    <ExcludeFile path="c:\writerData\notTheseFiles" 
                 filespec="excludeThisFile.txt" 
                 recursive="no"/>

    <Component componentType="filegroup"
               componentName="TestFiles">
        <ComponentFile path="c:\writerData\myFilesHere" 
                       filespec="*"
                       recursive="no" />
    </Component>

</TestWriter>
```

O elemento raiz nesse arquivo de configuração é denominado TestWriter. Todos os outros elementos são organizados sob o elemento TestWriter.

Um dos atributos associados a TestWriter é o atributo Usage. Esse atributo especifica o tipo de uso relatado por meio de [**IVssExamineWriterMetadata:: getidentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity). Um dos valores possíveis para esse atributo são \_ os dados do usuário.

O primeiro elemento filho do elemento raiz sempre deve ser um elemento RestoreMethod. Esse elemento Especifica o seguinte:

-   O método Restore (nesse caso, RESTOre \_ If \_ pode \_ ser \_ substituído)
-   Se o gravador requer eventos de restauração (neste caso, sempre)
-   Se uma reinicialização é necessária após a restauração do gravador (neste caso, não)

Esse elemento pode, opcionalmente, especificar um mapeamento de local alternativo. (Nesse caso, nenhum local alternativo é especificado.)

O segundo elemento filho é um elemento excludefile. Esse elemento faz com que o gravador exclua um arquivo ou um conjunto de arquivos do backup.

O terceiro elemento filho é um elemento de componente. Esse elemento faz com que o gravador adicione um componente a seus metadados. Um elemento de componente contém atributos para descrever o componente e os elementos filho para descrever o conteúdo do componente, como o seguinte:

-   ComponentType para indicar se este é um grupo de arquivos ou um banco de dados
-   logicalPath para o caminho lógico do componente
-   ComponentName para o nome do componente
-   selecionável para indicar o status de selecionável para backup

O elemento Component também tem um elemento filho chamado Componentfile para adicionar uma especificação de arquivo a esse componente. (Um elemento de componente pode ter um número arbitrário de elementos Componentfile que podem ser especificados para cada componente.) Este elemento Componentfile tem os seguintes atributos:

-   Path = "c: \\ writerData \\ myFilesHere"
-   filespec = " \* "
-   recursivo = "não"

Embora o gravador de teste Verifique o comportamento do solicitante, ele não verifica se o arquivo de configuração sempre mantém a semântica documentada para um gravador. Há muitas operações que um gravador bem comportado não deve fazer (como relatar o mesmo arquivo em vários componentes), e cabe ao autor do arquivo de configuração XML manter essas semânticas.

## <a name="configuring-writer-attributes"></a>Configurando atributos do gravador

O elemento raiz TestWriter contém atributos que determinam vários comportamentos do gravador. Alguns dos comportamentos que podem ser alterados são os seguintes:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="verbosity"></span><span id="VERBOSITY"></span>detalhamento<br/></td>
<td>O gravador imprime o status no console do à medida que recebe eventos e os processa. O nível de detalhamento exibido é especificado pelo atributo de detalhes. Há três níveis de detalhamento a serem escolhidos:<br/> <dl> <dt><span id="low"></span><span id="LOW"></span>pequena</dt> <dd> Somente as falhas no gravador ou comportamento incorreto do solicitante serão impressas.<br/> </dd> <dt><span id="medium"></span><span id="MEDIUM"></span>médio</dt> <dd> Tudo no nível de detalhe baixo é impresso, além das informações de status extras, como quando os eventos são recebidos. Este é o nível padrão.<br/> </dd> <dt><span id="high"></span><span id="HIGH"></span>elevada</dt> <dd> Informações detalhadas de status sobre a operação do gravador são relatadas.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="deleteFiles"></span><span id="deletefiles"></span><span id="DELETEFILES"></span>deleteFiles<br/></td>
<td>Para executar a verificação extra, defina esse atributo como &quot; Sim &quot; para fazer com que o gravador exclua todos os seus arquivos imediatamente após a criação da cópia de sombra de volume. O solicitante deve copiar os arquivos da cópia de sombra, pois eles não existem mais no volume original. <br/>
<blockquote>
[!Note]<br />
No caso de gravadores saliva, os arquivos são excluídos do local original após o saliva, mas antes da cópia de sombra ser criada. Depois que a cópia de sombra é criada, os arquivos são excluídos do diretório saliva.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="deletePartialFiles"></span><span id="deletepartialfiles"></span><span id="DELETEPARTIALFILES"></span>deletePartialFiles<br/></td>
<td>Para excluir arquivos parciais, defina este atributo como &quot; Sim &quot; .<br/></td>
</tr>
<tr class="even">
<td><span id="deleteDifferencedFiles"></span><span id="deletedifferencedfiles"></span><span id="DELETEDIFFERENCEDFILES"></span>deleteDifferencedFiles<br/></td>
<td>Para excluir arquivos diferenciados, defina este atributo como &quot; Sim &quot; .<br/></td>
</tr>
<tr class="odd">
<td><span id="checkIncludes"></span><span id="checkincludes"></span><span id="CHECKINCLUDES"></span>checkIncludes<br/></td>
<td>Defina esse atributo como &quot; Sim &quot; para fazer com que o gravador Verifique se todos os arquivos cujo backup foi feito foi restaurado em um local apropriado e se o arquivo não foi corrompido. Arquivos parciais e arquivos diferenciados também são tratados corretamente.<br/></td>
</tr>
<tr class="even">
<td><span id="checkExcludes"></span><span id="checkexcludes"></span><span id="CHECKEXCLUDES"></span>checkExcludes<br/></td>
<td>Defina esse atributo como &quot; Sim &quot; para fazer com que o gravador Verifique se os arquivos que correspondem a uma especificação de arquivo na lista de exclusões não são restaurados. Para que isso funcione corretamente, os diretórios de restauração devem ser esvaziados antes da restauração.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="specifying-alternate-location-mappings"></a>Especificando mapeamentos de local alternativos

Um mapeamento de local alternativo especifica um local para restaurar se o método de restauração for o VSS \_ WRE \_ restaurar \_ para um \_ \_ local alternativo ou se a restauração normal de um componente falhar. Um gravador pode relatar seus mapeamentos de local alternativos para o solicitante usando o método [**IVssExamineWriterMetadata:: GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) . Você pode adicionar mapeamentos de local alternativos ao arquivo de configuração do gravador de teste adicionando subelementos AlternateLocationMapping ao elemento RestoreMethod.

O elemento RestoreMethod a seguir contém um subelemento AlternateLocationMapping.

``` syntax
<RestoreMethod method="RESTORE_IF_CAN_REPLACE"
              writerRestore="always"
              rebootRequired="no">
    <AlternateLocationMapping path="c:\files"
                              filespec="*.txt"
                              recursive="no"
                              alternatePath="c:\altfiles"/>
</RestoreMethod>
```

Este exemplo especifica que o solicitante deve primeiro tentar restaurar todos os arquivos que correspondem a c: \\ files \\ \* . txt para o diretório c: \\ files. Se um desses arquivos não puder ser substituído, o solicitante deverá restaurar todos os arquivos para o diretório c: \\ altfiles. O solicitante deve salvar esse mapeamento de local alternativo usando o método [**IVssBackupComponents:: AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping) . Se o gravador de teste estiver configurado para verificar se os arquivos foram restaurados, ele também verificará se o solicitante chamou **AddAlternativeLocationMapping**.

## <a name="specifying-files-to-be-excluded"></a>Especificando os arquivos a serem excluídos

Cada gravador pode especificar uma lista de especificações de arquivo que especificam arquivos para o solicitante excluir do backup. Você pode adicionar essas especificações de arquivo ao arquivo de configuração do gravador de teste adicionando subelementos de excludefile ao elemento raiz TestWriter.

Aqui está um exemplo de um subelemento excludefile que exclui todos os arquivos no diretório C: \\ files que correspondem a C: \\ temp \* . \*

``` syntax
    <ExcludeFile path="c:\files" 
                 filespec="temp*.*" 
                 recursive="no"/>
```

## <a name="backing-up-spit-writers"></a>Fazendo backup de gravadores saliva

Muitos gravadores atuam como "saliva gravadores". Um gravador saliva cria arquivos intermediários, ou "arquivos saliva", com base em um conjunto original de arquivos e coloca os arquivos saliva em um local alternativo no momento do backup. O gravador usa o método [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) para notificar o solicitante de que ele deve fazer backup desses arquivos a partir do local alternativo. No entanto, esses arquivos ainda devem ser restaurados para o local ativo dos arquivos originais. O gravador de teste pode ser configurado para atuar como um gravador saliva para uma determinada especificação de arquivo.

O elemento Componentfile a seguir contém um atributo alternatePath:

``` syntax
    <ComponentFile path="c:\files"
                   filespec="*.txt"
                   recursive="no"
                   alternatePath="c:\files\spit" />
```

Este exemplo configura o gravador de teste para copiar todos os arquivos que correspondem a c: \\ files \\ \* . txt para o diretório c: \\ files \\ saliva imediatamente antes da criação da cópia de sombra de volume. O solicitante deve fazer backup dos arquivos do diretório c: \\ files \\ saliva Se o gravador de teste estiver configurado para excluir arquivos, ele excluirá os arquivos originais antes da criação da cópia de sombra, para que eles não apareçam no diretório c: \\ files no volume da cópia de sombra. Nesse caso, os arquivos em c: \\ files \\ saliva são excluídos após a criação da cópia de sombra, para que seja necessário fazer backup do diretório c: \\ files \\ saliva no volume da cópia de sombra.

## <a name="reporting-component-dependencies"></a>Dependências de componente de relatório

Os gravadores podem especificar uma dependência entre um componente local e um componente existente em outro gravador. Essas dependências são relatadas ao solicitante usando [**IVssWMComponent:: getdependency**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdependency). O gravador de teste pode ser configurado para relatar essas dependências adicionando um ou mais subelementos de dependência ao elemento de componente.

O elemento de componente a seguir contém um subelemento de dependência:

``` syntax
    <Component componentType="filegroup"
               logicalPath=""
               componentName="WriterComponent"
               selectable="yes">
         <Dependency writerId="<GUID of target writer>"
                     logicalPath="ComponentPath"
                     componentName="Writer2Component" />
    </Component>
```

A dependência é especificada como atributos do elemento Dependency. WriterId é a ID de classe do gravador que contém o destino da dependência, logicalPath é o caminho lógico para o componente nesse gravador e ComponentName é o nome do componente. Nesse caso, se o solicitante estiver fazendo backup de "WriterComponent" no gravador atual, ele também deverá fazer backup do componente "ComponentPath \\ Writer2Component" no gravador de destino.

> [!Note]  
> O gravador de teste não executa nenhuma verificação para garantir que as dependências sejam respeitadas.

 

## <a name="failing-events"></a>Eventos com falha

O gravador de teste pode ser configurado para falhar em qualquer um dos eventos normais que um gravador recebe. Esses eventos são os seguintes:



| Evento                                                                                                                                    | Descrição                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Identify"></span><span id="identify"></span><span id="IDENTIFY"></span>Identificar<br/>                                     | Recebido como uma resposta a uma chamada [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) . A falha aqui fará com que o gravador não seja relatado.<br/>                                                                 |
| <span id="PrepareForBackup"></span><span id="prepareforbackup"></span><span id="PREPAREFORBACKUP"></span>PrepareForBackup<br/>     | Recebido como uma resposta ao solicitante chamando [**IVssBackupComponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup).<br/>                                                                                                                 |
| <span id="PrepareForSnapsot"></span><span id="prepareforsnapsot"></span><span id="PREPAREFORSNAPSOT"></span>PrepareForSnapsot<br/> | Recebido quando o solicitante chama [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), mas antes da cópia de sombra ser criada.<br/>                                                                                              |
| <span id="Freeze"></span><span id="freeze"></span><span id="FREEZE"></span>Trave<br/>                                             | Recebido imediatamente após [*PrepareForSnapshot*](vssgloss-p.md), mas ainda antes da criação da cópia de sombra.<br/>                                                                                                      |
| <span id="Thaw"></span><span id="thaw"></span><span id="THAW"></span>Congelar<br/>                                                     | Recebido após a conclusão da criação da cópia de sombra.<br/>                                                                                                                                                                                                     |
| <span id="PostSnapshot"></span><span id="postsnapshot"></span><span id="POSTSNAPSHOT"></span>Pós-instantâneo<br/>                     | Recebido após o descongelamento ser concluído, mas antes de [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) é concluído.<br/>                                                                                                                   |
| <span id="Abort"></span><span id="abort"></span><span id="ABORT"></span>Anular<br/>                                                 | Recebido se houver muito tempo decorrido entre [*congelar*](vssgloss-f.md) e [*descongelar*](vssgloss-t.md) ou se o solicitante chamar [**IVssBackupComponents:: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup).<br/> |
| <span id="BackupComplete"></span><span id="backupcomplete"></span><span id="BACKUPCOMPLETE"></span>BackupComplete<br/>             | Recebido quando o solicitante é encerrado. As falhas aqui nunca serão relatadas.<br/>                                                                                                                                                                                 |
| <span id="PreRestore"></span><span id="prerestore"></span><span id="PRERESTORE"></span>Prerestore<br/>                             | Recebido quando o solicitante chama [**IVssBackupComponents::P Rerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore).<br/>                                                                                                                                           |
| <span id="PostRestore"></span><span id="postrestore"></span><span id="POSTRESTORE"></span>Restauração<br/>                         | Recebido quando o solicitante chama [**IVssBackupComponents::P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore).<br/>                                                                                                                                         |



 

Essas falhas são configuradas adicionando um ou mais subelementos FailEvent ao elemento raiz TestWriter. Há duas classes de falhas que podem ser definidas: retryável e sem nova tentativa. Erros com nova tentativa são erros que podem desaparecer se todo o processo de backup for repetido, enquanto erros sem nova tentativa não serão desaparecedos. O tipo de falha do evento é escolhido com base no atributo com nova tentativa.

Aqui está um exemplo de uma falha básica sem nova tentativa:

``` syntax
    <FailEvent writerEvent="Freeze"
               retryable="no" />
```

Este exemplo fará com que o gravador falhe durante o evento [*Freeze*](vssgloss-f.md) . [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) reportará a falha do gravador para ser VSS \_ E \_ WRITERERROR sem \_ nova tentativa.

Aqui está um exemplo de um erro básico com nova tentativa:

``` syntax
    <FailEvent writerEvent="Freeze"
               retryable="yes"
               numFailures="2"/>
```

Este exemplo fará com que o gravador falhe nas duas primeiras vezes que receber um evento [*Freeze*](vssgloss-f.md) . Após as duas primeiras vezes, o gravador sempre terá sucesso. A falha do gravador relatada por meio de [**GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) será um código de erro com nova tentativa aleatória.

## <a name="declaring-supported-backup-types"></a>Declarando tipos de backup com suporte

Os gravadores comunicam quais tipos de backup têm suporte por meio da chamada de [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)do solicitante. O elemento raiz TestWriter contém atributos para cada tipo de backup para indicar suporte. Esses atributos são supportsCopy, supportsDifferential, supportsIncremental e supportsLog. Para indicar o suporte para um tipo de backup específico, defina o atributo correspondente como "Sim".

Se o solicitante definir o tipo de backup para um tipo de backup sem suporte pelo gravador, o gravador notará esse fato durante o [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup), mas, caso contrário, funcionará corretamente.

## <a name="indicating-the-file-backup-type"></a>Indicando o tipo de backup de arquivo

O método [**IVssWMFiledesc:: GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask) retorna um bitmask para o solicitante que indica como deve ser feito o backup de um arquivo. Isso indicará se um arquivo é necessário ou não é necessário durante tipos específicos de backup e também se uma cópia de sombra é necessária durante tipos específicos de backup. Os tipos de backup nesse bitmask são explicados em um comprimento maior na [função de solicitante de documento no backup de repositórios complexos](requestor-role-in-backing-up-complex-stores.md).

No gravador de teste, os elementos dessa bitmask são especificados pela definição de atributos em cada elemento Componentfile. Os atributos fullBackupRequired, diffBackupRequired, incBackupRequired e logBackupRequired especificam quando é necessário fazer backup de um arquivo. Os atributos fullSnapshotRequired, diffSnapshotRequired, incSnapshotRequired e logSnapshotRequired especificam quando é necessário fazer backup de um arquivo de uma cópia de sombra de um volume (e nunca do volume original). O padrão para todos esses valores é "Sim", indicando que um arquivo deve sempre ser copiado em backup e deve ser submetido a backup de uma cópia de sombra de um volume.

## <a name="adding-partial-files"></a>Adicionando arquivos parciais

Durante o processamento de [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), um gravador tem a chance de adicionar arquivos parciais a cada componente. Esses arquivos parciais são relatados usando [**IVssComponent:: Getpartialfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile). O gravador de teste pode ser configurado para adicionar arquivos parciais especificando subelementos parciais em um elemento de componente.

Aqui está um exemplo de um elemento de componente que tem dois subelementos parciais:

``` syntax
    <Component componentType="filegroup"
               logicalPath=""
               componentName="WriterComponent"
               selectable="yes">
        <ComponentFile path="c:\files"
                       filespec="*.txt"
                       recursive="no"/>
        <PartialFile path="c:\files"
                     filespec="partial.txt"
                     ranges="0:5,100:20" />
        <PartialFile path="c:\files2"
                     filespec="partial.txt"
                     ranges="0:5,100:20" />
    </Component>
```

Somente arquivos parciais que correspondem parcialmente a um Componentfile existente (como no primeiro arquivo parcial no exemplo) ou novos arquivos parciais que estão no mesmo volume que um Componentfile existente (como no segundo arquivo parcial) devem ser especificados dessa maneira. Para esse componente, o solicitante deve fazer backup completo de todos os arquivos que correspondem a c: \\ files \\ \* . txt, exceto pelo partial.txt. O solicitante deve então fazer backup dos intervalos especificados (onde um intervalo é um deslocamento seguido por um comprimento) para os arquivos c: \\ files \\partial.txt e c: \\ files2 \\partial.txt.

Se o gravador estiver configurado para verificar restaurações de arquivo, somente os intervalos de backup do arquivo parcial serão verificados no momento da restauração. As modificações em outras partes do arquivo vão despercebidas. Se o atributo deletePartialFiles do elemento raiz TestWriter for definido, os arquivos parciais serão excluídos do volume original imediatamente após a cópia de sombra ser criada.

## <a name="adding-differenced-files"></a>Adicionando arquivos diferenciados

Durante o processamento de [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), um gravador pode adicionar arquivos diferenciados a cada componente. Esses arquivos diferenciados são relatados usando [**IVssComponent:: GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile). O gravador de teste pode ser configurado para adicionar arquivos diferenciados especificando subelementos DifferencedFile em um elemento de componente.

Aqui está um exemplo de um elemento de componente que tem dois subelementos DifferencedFile:

``` syntax
    <Component componentType="filegroup"
               logicalPath=""
               componentName="WriterComponent"
               selectable="yes">
        <ComponentFile path="c:\files"
                       filespec="*.txt"
                       recursive="no"/>
        <DifferencedFile path="c:\files"
                         filespec="*.txt"
                         year="2007"
                         month="1"
                         day="22"
                         hour="12"
                         minute="44"
                         second="17" />
        <DifferencedFile path="c:\files2"
                         filespec="*.txt"
                         year="2007"
                         month="1"
                         day="22"
                         hour="12"
                         minute="44"
                         second="17" />
    </Component>
```

Diferentemente dos arquivos parciais, os arquivos diferenciados nunca devem corresponder parcialmente a uma especificação de Componentfile. A especificação de arquivo em um elemento DifferencedFile deve corresponder exatamente a um Componentfile (como no primeiro arquivo de diferença no exemplo) ou não deve corresponder a ele, mas estar em um volume referenciado em um Componentfile (como no segundo arquivo de diferença). Os valores de data e hora devem ser relativos ao fuso horário local, mas eles serão convertidos em GMT antes de serem relatados ao solicitante. No exemplo, somente os arquivos que correspondem a c: \\ files \\ \* . txt ou c: \\ files2 \\ \* . txt que foram modificados desde 1/22/2003:12:44:17 serão submetidos a backup.

Se o gravador de teste estiver configurado para verificar restaurações de arquivo, somente os arquivos modificados serão verificados quanto à restauração. Se o atributo deleteDifferencedFiles do elemento raiz TestWriter for definido, os arquivos diferenciados serão excluídos do volume original imediatamente após a cópia de sombra ser criada.

## <a name="new-targets"></a>Novos destinos

Determinados gravadores permitem que o solicitante informe que um novo local foi escolhido para restaurar determinados arquivos. O gravador indica que ele dá suporte a esse modo como parte do bitmask retornado por [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema). Por padrão, o gravador de teste sempre dá suporte a novos destinos. Esse suporte pode ser desabilitado definindo o atributo supportsNewTarget no elemento raiz TestWriter como "no".

Se um gravador oferecer suporte a novos destinos, o solicitante poderá informar o gravador de novos destinos chamando [**IVssBackupComponents:: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget). O gravador verificará o novo local de destino para verificar a restauração em vez do local original.

## <a name="more-information"></a>Mais informações

O gravador de teste dá suporte a mais opções de configuração que não são descritas aqui. O esquema completo para todos os recursos de configuração do gravador de teste é especificado no swriter.xml in `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\x64\vsstools` (para Windows de 64 bits) e `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\vsstools` (para windows de 32 bits). Esse arquivo contém um esquema XML que descreve completamente todos os elementos e atributos que compõem um arquivo de configuração. Cada elemento e cada atributo nesse arquivo é comentado com uma descrição que documenta o uso do elemento ou do atributo.

 

 




