---
description: O BETest é um solicitante do VSS que testa operações avançadas de backup e restauração.
ms.assetid: a6cc7308-a9fa-4a84-9e7c-4d0adda28db5
title: Ferramenta BETest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7559c304532b337214108435b740595897694f7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837264"
---
# <a name="betest-tool"></a>Ferramenta BETest

O BETest é um solicitante do VSS que testa operações avançadas de backup e restauração. Essa ferramenta pode ser usada para testar o uso de recursos VSS complexos de um aplicativo, como o seguinte:

-   Backup incremental e diferencial
-   Opções de restauração complexas, como restauração autoritativa
-   Opções de avanço

> [!Note]  
> O BETest está incluído no SDK (Software Development Kit) do Microsoft Windows para Windows Vista e posterior. O SDK 7,2 do VSS inclui uma versão de BETest que é executada somente no Windows Server 2003. Este tópico descreve a versão SDK do Windows do BETest, não a versão 2003 do Windows Server incluída no SDK do VSS 7,2. Para obter informações sobre como baixar o SDK do Windows e o SDK 7,2 do VSS, consulte [serviço de cópias de sombra de volume](volume-shadow-copy-service-portal.md).

 

Na instalação do SDK do Windows, a ferramenta BETest pode ser encontrada em `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (para Windows de 64 bits) e `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (para windows de 32 bits).

## <a name="running-the-betest-tool"></a>Executando a ferramenta BETest

Para executar a ferramenta BETest na linha de comando, use a seguinte sintaxe:

*Opções de linha de comando* do **BETest**

O exemplo de uso a seguir mostra como usar a ferramenta BETest junto com a [ferramenta de gravador de teste do VSS](vss-test-writer-tool.md), que é um gravador VSS.

**Exemplo de uso da ferramenta BETest**

1.  Crie um diretório de teste chamado C: \\ BETest. Copie os seguintes arquivos para este diretório:
    -   betest.exe
    -   vswriter.exe
    -   [BetestSample.xml](#sample-xml-configuration-file-betestsamplexml)
    -   [VswriterSample.xml](#sample-xml-configuration-file-vswritersamplexml)
2.  Crie um diretório chamado C: \\ TestPath. Coloque alguns arquivos de dados de teste nesse diretório.
3.  Crie um diretório chamado C: \\ BackupDestination. Deixe esse diretório vazio.
4.  Abra duas janelas de comando elevadas e defina o diretório de trabalho em cada para C: \\ BETest.
5.  Na primeira janela de comando, inicie a [ferramenta gravador de teste do VSS](vss-test-writer-tool.md) da seguinte maneira:

    **vswriter.exe VswriterSample.xml**

    O arquivo vswriterSample.xml configura a ferramenta de gravador de teste do VSS (vswriter) para relatar o conteúdo do diretório c: \\ TestPath em preparação para uma operação de backup. Observe que a ferramenta de gravador de teste do VSS não produzirá saída até detectar a atividade de um solicitante, como o BETest. Para interromper a ferramenta gravador de teste do VSS, pressione CTRL + C.

6.  Na segunda janela de comando, use a ferramenta BETest para executar uma operação de backup da seguinte maneira:

    **betest.exe/B/S backup.xml/D C: \\ BackupDestination/x BetestSample.xml**

    O BETest fará o backup dos arquivos do diretório C: \\ TestPath para o diretório c: \\ BackupDestination. Ele salvará o documento do componente de backup em C: \\ BETest \\backup.xml.

7.  Se a operação de backup for bem-sucedida, exclua o conteúdo do diretório C: \\ TestPath e use a ferramenta BETest para executar uma operação de restauração da seguinte maneira:

    **betest.exe/R/S backup.xml/D C: \\ BackupDestination/x BetestSample.xml**

## <a name="betest-tool-command-line-options"></a>Opções de Command-Line da ferramenta BETest

A ferramenta BETest usa as seguintes opções de linha de comando para identificar o trabalho a ser executado.

<dl> <dt>

<span id="_Auth"></span><span id="_auth"></span><span id="_AUTH"></span>**/Auth**
</dt> <dd>

Executa uma operação de restauração autoritativa para Active Directory ou Active Directory modo de aplicativo.

**Windows Server 2003:** Não há suporte para essa opção de linha de comando.

</dd> <dt>

<span id="_B"></span><span id="_b"></span>**/B.**
</dt> <dd>

Executa uma operação de backup, mas não executa uma restauração.

</dd> <dt>

<span id="_BC"></span><span id="_bc"></span>**/BC**
</dt> <dd>

Executa apenas a operação backup concluído.

**Windows Server 2003:** Não há suporte para essa opção de linha de comando.

</dd> <dt>

<span id="_C_Filename"></span><span id="_c_filename"></span><span id="_C_FILENAME"></span>**/C** *nome do arquivo*
</dt> <dd>

> [!Note]  
> Essa opção de linha de comando é fornecida somente para compatibilidade com versões anteriores. Em vez disso, a opção de linha de comando **/x** deve ser usada.

 

Seleciona os componentes dos quais será feito backup ou restaurados com base no conteúdo do arquivo de configuração especificado por *filename*. Esse arquivo deve conter apenas caracteres ANSI no intervalo de 0 a 127, e não deve ter mais de 1 MB. Cada linha no arquivo deve usar o seguinte formato:

*WriterId* : *ComponentName*;

Em que *WriterId* é a ID do gravador e *ComponentName* é o nome de um dos componentes do gravador. A ID do gravador e os nomes de componentes devem estar entre aspas, e deve haver espaços antes e depois dos dois-pontos (:). Se dois ou mais componentes forem especificados, eles deverão ser separados por vírgulas. Por exemplo:

"5affb034-969f-4919-8875-88f830d0ef89" : "TestFiles1", "TestFiles2", "TestFiles3";

</dd> <dt>

<span id="_D_Path"></span><span id="_d_path"></span><span id="_D_PATH"></span>**/D** *caminho*
</dt> <dd>

Salve os arquivos dos quais foi feito backup ou restaure-os a partir do diretório de backup especificado pelo *caminho*.

</dd> <dt>

<span id="_NBC"></span><span id="_nbc"></span>**/NBC**
</dt> <dd>

Omite a operação de backup concluído.

**Windows Server 2003:** Não há suporte para essa opção de linha de comando.

</dd> <dt>

<span id="_O"></span><span id="_o"></span>**/O**
</dt> <dd>

Especifica que o backup inclui um estado de sistema inicializável.

</dd> <dt>

<span id="_P"></span><span id="_p"></span>**/P**
</dt> <dd>

Cria uma cópia de sombra persistente.

**Windows Server 2003:** Não há suporte para essa opção de linha de comando.

</dd> <dt>

<span id="_Pre_Filename"></span><span id="_pre_filename"></span><span id="_PRE_FILENAME"></span> *Nome de arquivo* /pre
</dt> <dd>

Se o tipo de backup especificado na opção de linha de comando **/t** for incremental ou diferencial, defina o documento de backup para o arquivo especificado por *filename* para backup completo ou incremental anterior.

**Windows Server 2003 e Windows XP:** Não há suporte para essa opção de linha de comando.

</dd> <dt>

<span id="_R"></span><span id="_r"></span>**/R**
</dt> <dd>

Executa a restauração, mas não executa o backup. Deve ser usado junto com a opção de linha de comando **/s** .

</dd> <dt>

<span id="_Rollback"></span><span id="_rollback"></span><span id="_ROLLBACK"></span>**/Rollback**
</dt> <dd>

Cria uma cópia de sombra que pode ser usada para reversão do aplicativo.

**Windows Server 2003:** Não há suporte para essa opção de linha de comando.

</dd> <dt>

<span id="_S_Filename"></span><span id="_s_filename"></span><span id="_S_FILENAME"></span>**/S** *nome do arquivo*
</dt> <dd>

No caso do backup, o salva o documento de backup no arquivo especificado por *filename*. No caso de somente restauração, o carrega o documento de backup desse arquivo.

</dd> <dt>

<span id="_Snapshot"></span><span id="_snapshot"></span><span id="_SNAPSHOT"></span>**/Snapshot**
</dt> <dd>

Cria uma cópia de sombra de volume, mas não executa backup ou restauração.

**Windows Server 2003:** Não há suporte para essa opção de linha de comando.

</dd> <dt>

<span id="_StopError"></span><span id="_stoperror"></span><span id="_STOPERROR"></span>**/StopError**
</dt> <dd>

Interrompe o teste quando o primeiro erro do gravador é encontrado.

**Windows Server 2003:** Não há suporte para essa opção de linha de comando.

</dd> <dt>

<span id="_T_BackupType"></span><span id="_t_backuptype"></span><span id="_T_BACKUPTYPE"></span>**/T** *backuptype*
</dt> <dd>

Especifica o tipo de backup. O *backuptype* pode ser completo, de log, de cópia, incremental ou diferencial. Para obter mais informações sobre tipos de backup, consulte [**VSS \_ backup \_ Type**](/windows/desktop/api/Vss/ne-vss-vss_backup_type).

</dd> <dt>

<span id="_V"></span><span id="_v"></span>**/V**
</dt> <dd>

Gera uma saída detalhada que pode ser usada para solução de problemas.

**Windows Server 2003:** Não há suporte para essa opção de linha de comando.

</dd> <dt>

<span id="_X_Filename"></span><span id="_x_filename"></span><span id="_X_FILENAME"></span> *Nome do arquivo* /x
</dt> <dd>

Seleciona os componentes cujo backup será feito ou restaurado com base no conteúdo do arquivo de configuração XML especificado por *filename*. Esse arquivo deve conter apenas caracteres ANSI no intervalo de 0 a 127. O formato do arquivo XML é definido pelo esquema no arquivo de BETest.xml. Para obter um arquivo de configuração de exemplo, consulte BetestSample.xml. Ambos os arquivos estão no diretório vsstools.

> [!Note]  
> Você pode exibir o arquivo de BETest.xml no Internet Explorer. Antes de abrir esse arquivo, verifique se o arquivo XDR-Schema. xsl está no mesmo diretório que BETest.xml. O arquivo XDR-Schema. xsl contém instruções de renderização que tornam o arquivo BETest.xml mais legível.

 

**Windows Server 2003:** Não há suporte para essa opção de linha de comando.

</dd> </dl>

## <a name="sample-xml-configuration-file-betestsamplexml"></a>Arquivo de configuração XML de exemplo: BetestSample.xml

O arquivo de configuração de exemplo a seguir, BetestSample.xml, pode ser encontrado no diretório Vsstools

``` syntax
<BETest>
    <Writer writerid="5affb034-969f-4919-8875-88f830d0ef89">
        <Component componentName="TestFiles">
        </Component>
    </Writer>
</BETest>
```

Este exemplo de um arquivo de configuração simples seleciona um componente do qual será feito backup ou restaurado.

## <a name="sample-xml-configuration-file-vswritersamplexml"></a>Arquivo de configuração XML de exemplo: VswriterSample.xml

O arquivo de configuração de exemplo a seguir, VswriterSample.xml, pode ser encontrado no diretório Vsstools

``` syntax
<TestWriter   usage="USER_DATA"
                    deleteFiles="no">

    <RestoreMethod method="RESTORE_IF_CAN_BE_REPLACED" 
                   writerRestore="always"
                   rebootRequired="no" />
    
    <Component componentType="filegroup" 
               componentName="TestFiles">
               <ComponentFile path="c:\TestPath" filespec="*" recursive="no" />
    </Component>

</TestWriter>
```

O elemento raiz nesse arquivo de configuração é denominado TestWriter. Todos os outros elementos são organizados sob o elemento TestWriter.

O primeiro atributo associado a TestWriter é o atributo Usage. Esse atributo especifica o tipo de uso relatado por meio do método [**IVssExamineWriterMetadata:: getidentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity) . Um dos valores possíveis para esse atributo são \_ os dados do usuário.

O segundo atributo é o atributo deleteFiles. Esse atributo é descrito em [Configurando atributos do gravador](vss-test-writer-tool.md).

O primeiro elemento filho do elemento raiz é um elemento RestoreMethod. Esse elemento Especifica o seguinte:

-   O método Restore (nesse caso, RESTOre \_ If \_ pode \_ ser \_ substituído)
-   Se o gravador requer eventos de restauração (neste caso, sempre)
-   Se uma reinicialização é necessária após a restauração do gravador (neste caso, não)

Esse elemento pode, opcionalmente, especificar um mapeamento de local alternativo. (Nesse caso, nenhum local alternativo é especificado.) Para obter mais informações, consulte [especificando mapeamentos alternativos de local](vss-test-writer-tool.md).

O segundo elemento filho é um elemento de componente. Esse elemento faz com que o gravador adicione um componente a seus metadados. Um elemento de componente contém atributos para descrever o componente e os elementos filho para descrever o conteúdo do componente, como o seguinte:

-   ComponentType para indicar se este é um grupo de arquivos ou um banco de dados (neste caso, um grupo de arquivos)
-   logicalPath para o caminho lógico do componente (nesse caso, nenhum é especificado)
-   ComponentName para o nome do componente (nesse caso, "TestFiles")
-   selecionável para indicar o status de selecionável para backup

O elemento Component também tem um elemento filho chamado Componentfile para adicionar uma especificação de arquivo a esse componente. (Um elemento de componente pode ter um número arbitrário de elementos Componentfile que podem ser especificados para cada componente.) Este elemento Componentfile tem os seguintes atributos:

-   caminho = "c: \\ TestPath"
-   filespec = " \* "
-   recursivo = "não"

 

 



