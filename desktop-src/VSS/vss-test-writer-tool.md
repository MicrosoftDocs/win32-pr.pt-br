---
description: O gravador de teste é um utilitário que você pode usar para testar aplicativos do solicitante do VSS.
ms.assetid: 02434cb9-390c-4cf0-9941-b833ace55685
title: Ferramenta de gravador de teste do VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93f0b81bd5e27db9fdfb70ca52e6f43bbb1e853af87bc12e1d76f01d7966ef3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344228"
---
# <a name="vss-test-writer-tool"></a>Ferramenta de gravador de teste do VSS

O gravador de teste é um utilitário que você pode usar para testar aplicativos do solicitante do VSS. Esse gravador pode ser configurado para executar quase todas as ações que um gravador VSS pode executar. Além disso, o gravador de teste executa verificações extensivas para garantir que o solicitante tenha tratado corretamente essas ações de gravador.

Cada instância do gravador é inicializada com um arquivo de configuração XML que descreve exatamente quais componentes serão relatados pelo gravador e como o gravador se comporta. O gravador pode ser configurado para relatar vários tipos de cenários, incluindo cenários mais complicados usando as interfaces incrementais e diferenciais. O gravador executará verificações em vários pontos durante o processo para garantir que o solicitante esteja se comportando de maneira adequada. Depois que a restauração for concluída, o gravador verificará se todos os arquivos necessários foram restaurados sem corrupção. O gravador também pode ser configurado para executar outras operações, como eventos específicos com falha.

> [!Note]  
> essa ferramenta está incluída no SDK (Software Development Kit) do Microsoft Windows para Windows Vista e posterior. você pode baixar o SDK do Windows do [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx) .

 

na instalação do SDK do Windows, a ferramenta VssSampleProvider pode ser encontrada em `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (para a Windows de 64 bits) e `%Program Files(x86)%\Windows Kits\8.1\bin\x86` .

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

Este exemplo especifica que o solicitante deve primeiro tentar restaurar todos os arquivos que correspondem a c: \\ files \\ \*.txt para o diretório c: \\ files. Se um desses arquivos não puder ser substituído, o solicitante deverá restaurar todos os arquivos para o diretório c: \\ altfiles. O solicitante deve salvar esse mapeamento de local alternativo usando o método [**IVssBackupComponents:: AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping) . Se o gravador de teste estiver configurado para verificar se os arquivos foram restaurados, ele também verificará se o solicitante chamou **AddAlternativeLocationMapping**.

## <a name="specifying-files-to-be-excluded"></a>Especificando os arquivos a serem excluídos

Cada gravador pode especificar uma lista de especificações de arquivo que especificam arquivos para o solicitante excluir do backup. Você pode adicionar essas especificações de arquivo ao arquivo de configuração do gravador de teste adicionando subelementos de excludefile ao elemento raiz TestWriter.

Aqui está um exemplo de um subelemento excludefile que exclui todos os arquivos no diretório C: \\ files que correspondem a C: \\ temp \* . \*

``` syntax
    <ExcludeFile path="c:\files" 
                 filespec="temp*.*" 
                 recursive="no"/>
```

## <a name="backing-up-spit-writers"></a>Fazendo backup de gravadores saliva

Muitos gravadores atuam como "saliva gravadores". Um gravador saliva cria arquivos intermediários, ou "arquivos saliva", com base em um conjunto original de arquivos e coloca os arquivos saliva em um local alternativo no momento do backup. O autor usa o método [**IVssWMFiledesc::GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) para notificar o solicitante de que ele deve fazer o back-up desses arquivos do local alternativo. No entanto, esses arquivos ainda devem ser restaurados para o local ativo dos arquivos originais. O Test Writer pode ser configurado para atuar como um autor de técnicas para uma especificação de arquivo específica.

O seguinte elemento ComponentFile contém um atributo alternatePath:

``` syntax
    <ComponentFile path="c:\files"
                   filespec="*.txt"
                   recursive="no"
                   alternatePath="c:\files\spit" />
```

Este exemplo configura o Test Writer para copiar todos os arquivos correspondentes a arquivos c: arquivos.txt diretório c: arquivos imediatamente antes da criação da cópia de \\ \\ \* sombra de \\ \\ volume. O solicitante deve fazer o back-up dos arquivos do diretório c: \\ files \\ directory. Se o Test Writer estiver configurado para excluir arquivos, ele excluirá os arquivos originais antes que a cópia de sombra seja criada, para que eles não apareçam no diretório de arquivos c: no volume de cópia \\ de sombra. Nesse caso, os arquivos em c: arquivos são excluídos depois que a cópia de sombra é criada, portanto, eles devem ser copiados em backup do diretório de arquivos c: no volume de cópia \\ \\ de \\ \\ sombra.

## <a name="reporting-component-dependencies"></a>Dependências do componente de relatório

Os autores podem especificar uma dependência entre um componente local e um componente que existe em outro autor. Essas dependências são relatadas ao solicitante usando [**IVssWMComponent::GetDependency**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdependency). O Test Writer pode ser configurado para relatar essas dependências adicionando um ou mais subelementos de Dependência ao elemento Component.

O seguinte elemento Component contém um subelemento Dependency:

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

A dependência é especificada como atributos do elemento Dependency. writerId é a ID de classe do autor que contém o destino da dependência, logicalPath é o caminho lógico para o componente nesse autor e componentName é o nome do componente. Nesse caso, se o solicitante estiver fazer o back-up de "WriterComponent" no autor atual, ele também deverá fazer o back-up do componente "ComponentPath Writer2Component" no autor de \\ destino.

> [!Note]  
> O Test Writer não executa nenhuma verificação para garantir que as dependências sejam adida.

 

## <a name="failing-events"></a>Eventos com falha

O Test Writer pode ser configurado para falhar em qualquer um dos eventos normais recebidos por um autor. Esses eventos são os seguinte:



| Evento                                                                                                                                    | Descrição                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Identify"></span><span id="identify"></span><span id="IDENTIFY"></span>Identificar<br/>                                     | Recebido como uma resposta a [**uma chamada IVssBackupComponents::GatherWriterMetadata.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) A falha aqui fará com que o autor não seja relatado.<br/>                                                                 |
| <span id="PrepareForBackup"></span><span id="prepareforbackup"></span><span id="PREPAREFORBACKUP"></span>PrepareForBackup<br/>     | Recebido como uma resposta ao solicitante chamando [**IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup).<br/>                                                                                                                 |
| <span id="PrepareForSnapsot"></span><span id="prepareforsnapsot"></span><span id="PREPAREFORSNAPSOT"></span>PrepareForSnapsot<br/> | Recebido quando o solicitante chama [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), mas antes que a cópia de sombra seja criada.<br/>                                                                                              |
| <span id="Freeze"></span><span id="freeze"></span><span id="FREEZE"></span>Congelar<br/>                                             | Recebido imediatamente após [*PrepareForSnapshot*](vssgloss-p.md), mas ainda antes da criação da cópia de sombra.<br/>                                                                                                      |
| <span id="Thaw"></span><span id="thaw"></span><span id="THAW"></span>Descongelar<br/>                                                     | Recebido após a criação da cópia de sombra ser concluída.<br/>                                                                                                                                                                                                     |
| <span id="PostSnapshot"></span><span id="postsnapshot"></span><span id="POSTSNAPSHOT"></span>PostSnapshot<br/>                     | Recebido após a conclusão do Thaw, mas antes da conclusão [**de IVssBackupComponents::D oSnapshotSet.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)<br/>                                                                                                                   |
| <span id="Abort"></span><span id="abort"></span><span id="ABORT"></span>Abortar<br/>                                                 | Recebido se passar muito tempo [](vssgloss-f.md) entre [](vssgloss-t.md) Congelamento e Descongelamento ou se o solicitante chamar [**IVssBackupComponents::AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup).<br/> |
| <span id="BackupComplete"></span><span id="backupcomplete"></span><span id="BACKUPCOMPLETE"></span>BackupComplete<br/>             | Recebido quando o solicitante sai. Falhas aqui nunca serão relatadas.<br/>                                                                                                                                                                                 |
| <span id="PreRestore"></span><span id="prerestore"></span><span id="PRERESTORE"></span>Pré-repositório<br/>                             | Recebido quando o solicitante chama [**IVssBackupComponents::P reRestore.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)<br/>                                                                                                                                           |
| <span id="PostRestore"></span><span id="postrestore"></span><span id="POSTRESTORE"></span>PostRestore<br/>                         | Recebido quando o solicitante chama [**IVssBackupComponents::P ostRestore.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)<br/>                                                                                                                                         |



 

Essas falhas são configuradas adicionando um ou mais subelementos FailEvent ao elemento raiz TestWriter. Há duas classes de falhas que podem ser definidas: retryable e non-retryable. Erros que podem ser repetir são erros que podem desaparecer se todo o processo de backup for novamente, enquanto erros não retriáveis provavelmente desaparecerão. O tipo de falha para o evento é escolhido com base no atributo que pode ser tentar novamente.

Aqui está um exemplo de uma falha básica não retriável:

``` syntax
    <FailEvent writerEvent="Freeze"
               retryable="no" />
```

Este exemplo fará com que o autor falhe durante o [*evento Freeze.*](vssgloss-f.md) [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) relatará a falha do autor como VSS \_ E \_ WRITERERROR \_ NONRETRYABLE.

Aqui está um exemplo de um erro básico que pode ser tentar novamente:

``` syntax
    <FailEvent writerEvent="Freeze"
               retryable="yes"
               numFailures="2"/>
```

Este exemplo fará com que o autor falhe nas duas primeiras vezes em que receber um [*evento Freeze.*](vssgloss-f.md) Após as duas primeiras vezes, o autor sempre terá êxito. A falha do autor relatada [**por meio de GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) será um código de erro aleatório que pode ser tentar novamente.

## <a name="declaring-supported-backup-types"></a>Declarando tipos de backup com suporte

Os autores comunicam quais tipos de backup têm suporte por meio da chamada do solicitante [**IVssExamineWriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema). O elemento raiz TestWriter contém atributos para cada tipo de backup para indicar suporte. Esses atributos são supportsCopy, supportsDifferential, supportsIncremental e supportsLog. Para indicar o suporte para um tipo de backup específico, de definido o atributo correspondente como "sim".

Se o solicitante define o tipo de backup como um tipo de backup que não é suportado pelo autor, o autor observará esse fato durante [**PrepareForBackup,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)mas, de outra forma, funcionará corretamente.

## <a name="indicating-the-file-backup-type"></a>Indicando o tipo de backup de arquivo

O [**método IVssWMFiledesc::GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask) retorna um bitmask para o solicitante indicando como um arquivo deve ser feito backup. Isso indicará se um arquivo é necessário ou não durante tipos específicos de backup e também se uma cópia de sombra é necessária durante tipos específicos de backup. Os tipos de backup nesta máscara de bits são explicados com maior comprimento no documento Função de Solicitante em [Backup de Armazenamentos Complexos](requestor-role-in-backing-up-complex-stores.md).

No Test Writer, os elementos dessa máscara de bits são especificados definindo atributos em cada elemento ComponentFile. Os atributos fullBackupRequired, diffBackupRequired, incBackupRequired e logBackupRequired especificam quando um arquivo precisa ser feito backup. Os atributos fullSnapshotRequired, diffSnapshotRequired, incSnapshotRequired e logSnapshotRequired especificam quando um arquivo deve ser copiado em backup de uma cópia de sombra de um volume (e nunca do volume original). O padrão para todos esses valores é "sim", indicando que um arquivo sempre deve ser copiado em backup e deve ser feito backup de uma cópia de sombra de um volume.

## <a name="adding-partial-files"></a>Adicionando arquivos parciais

Durante o processamento de [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), um autor tem a oportunidade de adicionar arquivos parciais a cada componente. Esses arquivos parciais são [**relatados usando IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile). O Test Writer pode ser configurado para adicionar arquivos parciais especificando subelementos PartialFile em um elemento Component.

Aqui está um exemplo de um elemento Component que tem dois subelementos PartialFile:

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

Somente arquivos parciais que corresponderem parcialmente a um ComponentFile existente (como no primeiro arquivo parcial no exemplo) ou novos arquivos parciais que estão no mesmo volume que um ComponentFile existente (como no segundo arquivo parcial) devem ser especificados dessa maneira. Para esse componente, o solicitante deve fazer todo o back-up de todos os arquivos correspondentes a c: arquivos \\ \\ \*.txt exceto partial.txt. Em seguida, o solicitante deve fazer o back-up dos intervalos especificados (em que um intervalo é um deslocamento seguido por um comprimento) para os arquivos c: arquivospartial.txt e \\ \\ c: \\ files2 \\partial.txt.

Se o writer estiver configurado para verificar restaurações de arquivo, somente os intervalos de backup do arquivo parcial serão verificados no momento da restauração. As modificações em outras partes do arquivo passarão despercebidas. Se o atributo deletePartialFiles do elemento raiz TestWriter estiver definido, os arquivos parciais serão excluídos do volume original imediatamente após a criação da cópia de sombra.

## <a name="adding-differenced-files"></a>Adicionando arquivos com diferença

Durante o processamento de [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), um autor pode adicionar arquivos de diferença a cada componente. Esses arquivos diferentes são relatados usando [**IVssComponent::GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile). O Test Writer pode ser configurado para adicionar arquivos diferenciados especificando subelementos DifferencedFile em um elemento Component.

Aqui está um exemplo de um elemento Component que tem dois subelementos DifferencedFile:

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

Ao contrário dos arquivos parciais, os arquivos diferentes nunca devem corresponder parcialmente a uma especificação ComponentFile. A especificação de arquivo em um elemento DifferencedFile deve corresponder exatamente a um ComponentFile (como no primeiro arquivo diferente no exemplo) ou não deve corresponder a ele, mas estar em um volume referenciado em um ComponentFile (como no segundo arquivo diferente). Os valores de data e hora devem ser relativos ao fuso horário local, mas serão convertidos em GMT antes de serem relatados ao solicitante. No exemplo, somente arquivos correspondentes a c: arquivos.txt ou c: arquivos2.txt que foram modificados desde \\ \\ \* \\ \\ \* 22/1/2003:12:44:17 serão armazenados em backup.

Se o Test Writer estiver configurado para verificar restaurações de arquivo, somente os arquivos modificados serão verificados para restauração. Se o atributo deleteDifferencedFiles do elemento raiz TestWriter estiver definido, os arquivos diferentes serão excluídos do volume original imediatamente após a criação da cópia de sombra.

## <a name="new-targets"></a>Novos destinos

Determinados autores permitem que o solicitante informe que um novo local foi escolhido para restaurar determinados arquivos. O autor indica que ele dá suporte a esse modo como parte do bitmask retornado por [**IVssExamineWriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema). Por padrão, o Test Writer sempre dá suporte a novos destinos. Esse suporte pode ser desabilitado definindo o atributo supportsNewTarget no elemento raiz TestWriter como "não".

Se um autor dá suporte a novos destinos, o solicitante pode informar o autor de novos destinos chamando [**IVssBackupComponents::AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget). Em seguida, o autor verificará o novo local de destino para verificar a restauração em vez do local original.

## <a name="more-information"></a>Mais informações

O Test Writer dá suporte a mais opções de configuração que não são descritas aqui. O esquema completo para todos os recursos de configuração do Test Writer é especificado no swriter.xml no (para Windows de `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\x64\vsstools` 64 bits) e `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\vsstools` (para 32 bits Windows). Esse arquivo contém um esquema XML que descreve completamente todos os elementos e atributos que comem um arquivo de configuração. Cada elemento e cada atributo nesse arquivo é comentado com uma descrição que documenta o uso desse elemento ou atributo.

 

 




