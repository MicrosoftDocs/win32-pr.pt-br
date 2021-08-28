---
description: O Test Writer é um utilitário que você pode usar para testar aplicativos solicitante do VSS.
ms.assetid: 02434cb9-390c-4cf0-9941-b833ace55685
title: Ferramenta de Writer de Teste do VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35c8ff5461c263754aa5771cc9db230dec795a98
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482092"
---
# <a name="vss-test-writer-tool"></a>Ferramenta de Writer de Teste do VSS

O Test Writer é um utilitário que você pode usar para testar aplicativos solicitante do VSS. Esse autor pode ser configurado para executar quase todas as ações que um vss writer pode executar. Além disso, o Test Writer executa verificações abrangentes para garantir que o solicitante tenha tratado essas ações de autor corretamente.

Cada instância do autor é inicializada com um arquivo de configuração XML que descreve exatamente em quais componentes o autor relatará e como o autor se comporta. O autor pode ser configurado para relatar vários tipos de cenários, incluindo cenários mais complicados usando interfaces incrementais e diferenciais. O autor executará verificações em vários pontos durante o processo para garantir que o solicitante está se comportando de maneira adequada. Depois que a restauração for concluída, o autor verificará se todos os arquivos necessários foram restaurados sem corrupção. O autor também pode ser configurado para executar outras operações, como eventos específicos com falha.

> [!Note]  
> Essa ferramenta está incluída no Microsoft Windows Software Development Kit (SDK) para Windows Vista e posterior. Você pode baixar o Windows SDK do [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx) .

 

Na instalação Windows SDK do Windows, a ferramenta VssSampleProvider pode ser encontrada em `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (para 64 bits Windows) e `%Program Files(x86)%\Windows Kits\8.1\bin\x86` .

## <a name="running-the-test-writer-tool"></a>Executando a Ferramenta de Autor de Teste

Para iniciar o Test Writer, digite o seguinte no prompt de comando:

**vswriter.exe** *arquivo de configuração*

em *que config-file* é o caminho para um arquivo de configuração que especifica o comportamento desse autor.

Para interromper o Test Writer, pressione CTRL+C.

Várias instâncias do Test Writer podem ser executados ao mesmo tempo. No entanto, cada instância do autor relatará a mesma ID de classe de autor (embora uma ID de instância de autor diferente), portanto, os caminhos lógicos e os nomes de componentes devem ser exclusivos em todas as instâncias em execução simultânea do autor.

Para garantir que o autor possa verificar corretamente se o solicitante recebeu as especificações do arquivo de exclusão, todos os arquivos que foram armazenados em backup devem ser excluídos do volume original antes de tentar restaurá-los. É recomendável que um modelo de cada cenário de autor seja armazenado, para que o cenário possa ser recriado facilmente.

## <a name="using-a-configuration-file"></a>Usar um Arquivo de Configuração

O arquivo de configuração de exemplo a seguir, vswriterconfig.xml, pode ser encontrado em em \_ `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\vsstools` plataformas x86 e `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\x64\vsstools` em plataformas x64.

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

O elemento raiz nesse arquivo de configuração é chamado TestWriter. Todos os outros elementos são organizados sob o elemento TestWriter.

Um dos atributos associados ao TestWriter é o atributo de uso. Esse atributo especifica o tipo de uso relatado por [**meio de IVssExamineWriterMetadata::GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity). Um dos valores possíveis para esse atributo é USER \_ DATA.

O primeiro elemento filho do elemento raiz sempre deve ser um elemento RestoreMethod. Esse elemento especifica o seguinte:

-   O método de restauração (nesse caso, RESTORE \_ IF \_ CAN BE \_ \_ REPLACED)
-   Se o autor requer eventos de restauração (nesse caso, sempre)
-   Se uma reinicialização é necessária depois que o autor é restaurado (nesse caso, não)

Opcionalmente, esse elemento pode especificar um mapeamento de localização alternativa. (Nesse caso, nenhum local alternativo é especificado.)

O segundo elemento filho é um elemento ExcludeFile. Esse elemento faz com que o autor exclua um arquivo ou um conjunto de arquivos do backup.

O terceiro elemento filho é um elemento Component. Esse elemento faz com que o autor adicione um componente aos seus metadados. Um elemento Component contém atributos para descrever o componente e os elementos filho para descrever o conteúdo do componente, como o seguinte:

-   componentType para indicar se este é um grupo de arquivos ou um banco de dados
-   logicalPath para o caminho lógico do componente
-   componentName para o nome do componente
-   selecionável para indicar o status selecionável para backup

O elemento Component também tem um elemento filho chamado ComponentFile para adicionar uma especificação de arquivo a esse componente. (Um elemento Component pode ter um número arbitrário de elementos ComponentFile que podem ser especificados para cada componente.) Esse elemento ComponentFile tem os seguintes atributos:

-   path="c: \\ writerData \\ myFilesHere"
-   filespec=" \* "
-   recursive="no"

Embora o Test Writer verifique o comportamento do solicitante, ele não verifica se o arquivo de configuração sempre mantém a semântica documentada para um autor. Há muitas operações que um autor bem-comportado não deve fazer (como relatar o mesmo arquivo em vários componentes) e é responsabilidade do autor do arquivo de configuração XML manter essa semântica.

## <a name="configuring-writer-attributes"></a>Configurando atributos de writer

O elemento raiz TestWriter contém atributos que determinam vários comportamentos do autor. Alguns dos comportamentos que podem ser alterados são os seguintes:




| Atributo | Descrição | 
|-----------|-------------|
| <span id="verbosity"></span><span id="VERBOSITY"></span>Verbosidade<br /> | O autor imprime o status no console à medida que recebe eventos e os processa. O nível de detalhabilidade exibido é especificado pelo atributo verbosity. Há três níveis de detalhes para escolher:<br /><dl><dt><span id="low"></span><span id="LOW"></span>Baixo</dt><dd> Somente falhas no autor ou comportamento incorreto do solicitante serão impressas.<br /></dd><dt><span id="medium"></span><span id="MEDIUM"></span>Médio</dt><dd> Tudo no nível de detalhes baixo é impresso, além de informações de status extras, como quando os eventos são recebidos. Este é o nível padrão.<br /></dd><dt><span id="high"></span><span id="HIGH"></span>Alta</dt><dd> Informações detalhadas de status sobre a operação do autor são relatadas.<br /></dd></dl> | 
| <span id="deleteFiles"></span><span id="deletefiles"></span><span id="DELETEFILES"></span>deleteFiles<br /> | Para executar a verificação extra, de definir esse atributo como "sim" para fazer com que o autor exclua todos os seus arquivos imediatamente após a criação da cópia de sombra do volume. O solicitante deve copiar os arquivos da cópia de sombra, pois eles não existem mais no volume original. <br /><blockquote>[!Note]<br />No caso de autores de sempre, os arquivos são excluídos do local original após o acidente, mas antes que a cópia de sombra seja criada. Depois que a cópia de sombra é criada, os arquivos são excluídos do diretório de diretórios.</blockquote><br /> | 
| <span id="deletePartialFiles"></span><span id="deletepartialfiles"></span><span id="DELETEPARTIALFILES"></span>deletePartialFiles<br /> | Para excluir arquivos parciais, de definir esse atributo como "sim".<br /> | 
| <span id="deleteDifferencedFiles"></span><span id="deletedifferencedfiles"></span><span id="DELETEDIFFERENCEDFILES"></span>deleteDifferencedFiles<br /> | Para excluir arquivos de diferença, de definir esse atributo como "sim".<br /> | 
| <span id="checkIncludes"></span><span id="checkincludes"></span><span id="CHECKINCLUDES"></span>checkIncludes<br /> | De definir esse atributo como "sim" para fazer com que o autor verifique se cada arquivo que foi feito backup foi restaurado em um local apropriado e se o arquivo não foi corrompido. Arquivos parciais e arquivos de diferença também são tratados corretamente.<br /> | 
| <span id="checkExcludes"></span><span id="checkexcludes"></span><span id="CHECKEXCLUDES"></span>checkExcludes<br /> | De definir esse atributo como "sim" para fazer com que o autor verifique se os arquivos correspondentes a uma especificação de arquivo na lista de exclusão não são restaurados. Para que isso funcione corretamente, os diretórios de restauração devem ser esvaziados antes da restauração.<br /> | 




 

## <a name="specifying-alternate-location-mappings"></a>Especificando mapeamentos de localização alternativos

Um mapeamento de local alternativo especifica um local para o que restaurar se o método de restauração for VSS WRE RESTORE TO ALTERNATE LOCATION ou \_ se a restauração normal de um componente \_ \_ \_ \_ falhar. Um autor pode relatar seus mapeamentos de localização alternativos ao solicitante usando o método [**IVssExamineWriterMetadata::GetAlternateLocationMapping.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) Você pode adicionar mapeamentos de localização alternativos ao arquivo de configuração do Test Writer adicionando subelementos AlternateLocationMapping ao elemento RestoreMethod.

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

Este exemplo especifica que o solicitante deve primeiro tentar restaurar todos os arquivos correspondentes a c: arquivos.txt para o \\ \\ \* diretório de arquivos \\ c:. Se um desses arquivos não puder ser substituído, o solicitante deverá restaurar todos os arquivos para o diretório c: \\ altfiles. O solicitante deve salvar esse mapeamento de local alternativo usando o [**método IVssBackupComponents::AddAlternativeLocationMapping.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping) Se o Test Writer estiver configurado para verificar se os arquivos foram restaurados, ele também verificará se o solicitante chamou **AddAlternativeLocationMapping.**

## <a name="specifying-files-to-be-excluded"></a>Especificando arquivos a serem excluídos

Cada autor pode especificar uma lista de especificações de arquivo que especificam arquivos para o solicitante excluir do backup. Você pode adicionar essas especificações de arquivo ao arquivo de configuração do Test Writer adicionando subelementos ExcludeFile ao elemento raiz TestWriter.

Aqui está um exemplo de um subelemento ExcludeFile que exclui todos os arquivos no diretório C: arquivos que \\ corresponderem a C: \\ temp \* \* .

``` syntax
    <ExcludeFile path="c:\files" 
                 filespec="temp*.*" 
                 recursive="no"/>
```

## <a name="backing-up-spit-writers"></a>Fazer o back-up de autores de filme

Muitos autores atuam como "autores de filme". Um autor de sempre cria arquivos intermediários, ou "arquivos de arquivos de arquivos", com base em um conjunto original de arquivos e coloca os arquivos de arquivos em um local alternativo no momento do backup. O autor usa o método [**IVssWMFiledesc::GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) para notificar o solicitante de que ele deve fazer o back-up desses arquivos do local alternativo. No entanto, esses arquivos ainda devem ser restaurados para o local ativo dos arquivos originais. O Test Writer pode ser configurado para atuar como um autor de técnicas para uma especificação de arquivo específica.

O seguinte elemento ComponentFile contém um atributo alternatePath:

``` syntax
    <ComponentFile path="c:\files"
                   filespec="*.txt"
                   recursive="no"
                   alternatePath="c:\files\spit" />
```

Este exemplo configura o Test Writer para copiar todos os arquivos correspondentes a c: arquivos.txt diretório c: arquivos imediatamente antes da criação da cópia de \\ \\ \* sombra do \\ \\ volume. O solicitante deve fazer o back-up dos arquivos do diretório c: \\ files \\ directory. Se o Test Writer estiver configurado para excluir arquivos, ele excluirá os arquivos originais antes que a cópia de sombra seja criada, para que eles não apareçam no diretório de arquivos c: no volume de cópia \\ de sombra. Nesse caso, os arquivos em c: arquivos são excluídos depois que a cópia de sombra é criada, portanto, eles devem ser copiados em backup do diretório de arquivos c: no volume de cópia \\ \\ de \\ \\ sombra.

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

Somente arquivos parciais que corresponderem parcialmente a um ComponentFile existente (como no primeiro arquivo parcial no exemplo) ou novos arquivos parciais que estão no mesmo volume que um ComponentFile existente (como no segundo arquivo parcial) devem ser especificados dessa maneira. Para esse componente, o solicitante deve fazer todo o back-up de todos os arquivos correspondentes a c: arquivos \\ \\ \*.txt exceto para partial.txt. Em seguida, o solicitante deve fazer o back-up dos intervalos especificados (em que um intervalo é um deslocamento seguido por um comprimento) para os arquivos c: arquivospartial.txt e \\ \\ c: \\ files2 \\partial.txt.

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

Ao contrário dos arquivos parciais, os arquivos diferentes nunca devem corresponder parcialmente a uma especificação ComponentFile. A especificação de arquivo em um elemento DifferencedFile deve corresponder exatamente a um ComponentFile (como no primeiro arquivo diferente no exemplo) ou não deve corresponder a ele, mas estar em um volume referenciado em um ComponentFile (como no segundo arquivo diferente). Os valores de data e hora devem ser relativos ao fuso horário local, mas serão convertidos em GMT antes de serem relatados ao solicitante. No exemplo, somente arquivos correspondentes a c: arquivos.txt ou c: arquivos2.txt que foram modificados desde \\ \\ \* \\ \\ \* 22/01/2003:12:44:17 serão armazenados em backup.

Se o Test Writer estiver configurado para verificar restaurações de arquivo, somente os arquivos modificados serão verificados para restauração. Se o atributo deleteDifferencedFiles do elemento raiz TestWriter estiver definido, os arquivos diferentes serão excluídos do volume original imediatamente após a criação da cópia de sombra.

## <a name="new-targets"></a>Novos destinos

Determinados autores permitem que o solicitante informe que um novo local foi escolhido para restaurar determinados arquivos. O autor indica que ele dá suporte a esse modo como parte do bitmask retornado por [**IVssExamineWriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema). Por padrão, o Test Writer sempre dá suporte a novos destinos. Esse suporte pode ser desabilitado definindo o atributo supportsNewTarget no elemento raiz TestWriter como "não".

Se um autor dá suporte a novos destinos, o solicitante pode informar o autor de novos destinos chamando [**IVssBackupComponents::AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget). Em seguida, o autor verificará o novo local de destino para verificar a restauração em vez do local original.

## <a name="more-information"></a>Mais informações

O Test Writer dá suporte a mais opções de configuração que não são descritas aqui. O esquema completo para todos os recursos de configuração do Test Writer é especificado no swriter.xml no (para Windows de `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\x64\vsstools` 64 bits) e `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\vsstools` (para 32 bits Windows). Esse arquivo contém um esquema XML que descreve completamente todos os elementos e atributos que comem um arquivo de configuração. Cada elemento e cada atributo nesse arquivo é comentado com uma descrição que documenta o uso desse elemento ou atributo.

 

 




