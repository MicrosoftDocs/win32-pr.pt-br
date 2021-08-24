---
description: O servidor de origem permite que um cliente recupere a versão exata dos arquivos de origem que foram usados para criar um aplicativo.
ms.assetid: c7bf51ce-7fb4-49aa-ad33-e551b2c8362b
title: Servidor de Origem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1938a617cd6c8f613df2a1113288a27f6593336f819cde2f5380a8420c329d45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815506"
---
# <a name="source-server"></a>Servidor de Origem

O servidor de origem permite que um cliente recupere a versão exata dos arquivos de origem que foram usados para criar um aplicativo. Como o código-fonte de um módulo pode mudar entre versões e ao longo de um curso de anos, é importante ver o código-fonte como ele existia quando a versão do módulo em questão foi criada.

O servidor de origem recupera os arquivos apropriados do controle do código-fonte. Para usar o servidor de origem, o aplicativo deve ter sido indexado de origem.

## <a name="source-indexing"></a>Indexação de origem

O sistema de indexação de origem é uma coleção de arquivos executáveis e scripts Perl. Os scripts Perl exigem Perl 5.6 ou superior.

Em geral, os binários são indexados de origem durante o processo de build depois que o aplicativo é criado. As informações necessárias para o servidor de origem são armazenadas nos arquivos PDB.

Atualmente, o servidor de origem é acompanhado de scripts que devem funcionar com os seguintes sistemas de controle do código-fonte.

-   Team Foundation Server
-   Forçosamente
-   Visual SourceSafe
-   Cvs
-   Subversion

Você também pode criar um script personalizado para indexar seu código para um sistema de controle do código-fonte diferente.

A tabela a seguir lista as ferramentas do servidor de origem.



| Ferramenta        | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Srcsrv.ini  | Esse arquivo é a lista mestra de todos os servidores de controle do código-fonte. Cada entrada tem o seguinte formato:*MYSERVER* = *serverinfo*<br/> Ao usar o Perforce, as informações do servidor consistem no caminho de rede completo para o servidor, seguido por dois-pontos, seguido pelo número da porta que ele usa. Por exemplo:<br/> MYSERVER=machine.corp.company.com:1666<br/> Esse arquivo pode ser instalado no computador que executa o depurador. Quando o servidor de origem é iniciado, ele procura Srcsrv.ini valores; esses valores substituirão as informações contidas no arquivo PDB. Isso permite que os usuários configurem um depurador para usar um servidor de controle do código-fonte alternativo no momento da depuração.<br/> Para obter mais informações, consulte o exemplo Srcsrv.ini instalado com as ferramentas do servidor de origem.<br/> |
| Ssindex.cmd | Esse script cria a lista de arquivos verificados no controle do código-fonte junto com as informações de versão de cada arquivo. Ele armazena um subconjunto dessas informações nos arquivos .pdb gerados quando você criou o aplicativo. O script usa um dos seguintes módulos Perl para fazer interface com o controle do código-fonte: P4.pm (Perforce) ou Vss.pm (Visual Source Cofre). Para obter mais informações, execute o script com o -? ou -?? Opção (ajuda detalhada) ou examine o script.<br/>                                                                                                                                                                                                                                                                                                             |
| Srctool.exe | Esse utilitário lista todos os arquivos indexados em um arquivo .pdb. Para cada arquivo, ele lista o caminho completo, o servidor de controle do código-fonte e o número de versão do arquivo. Você pode usar essas informações para recuperar arquivos sem usar o servidor de origem. Para obter mais informações, execute o utilitário com o /? opção.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Pdbstr.exe  | Esse utilitário é usado pelos scripts de indexação para inserir as informações de controle de versão no fluxo alternativo "srcsrv" do arquivo .pdb de destino. Ele também pode ler qualquer fluxo de um arquivo .pdb. Você pode usar essas informações para verificar se os scripts de indexação estão funcionando corretamente. Para obter mais informações, execute o utilitário com o /? opção.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="retrieving-the-source-file"></a>Recuperando o arquivo de origem

A API dbgHelp fornece acesso à funcionalidade do servidor de origem por meio [**da função SymGetSourceFile.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) Para recuperar o nome do arquivo de origem a ser recuperado, chame a função [**SymEnumSourceFiles**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcefiles) ou [**SymGetLineFromAddr64.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr)

## <a name="using-source-server-with-a-debugger"></a>Usando o servidor de origem com um depurador

Para usar o servidor de origem com WinDbg, KD, NTSD ou CDB, verifique se você instalou uma versão recente das Ferramentas de Depuração para o pacote Windows (versão 6.3 ou posterior). Em seguida, inclua srv \* no comando .srcpath da seguinte maneira:

**\. srcpath srv \* ;** _c: \\ mysource_

Observe que este exemplo também inclui um caminho de origem tradicional. Se o depurador não puder recuperar o arquivo do servidor de origem, ele pesquisa o caminho especificado.

Se um arquivo de origem for recuperado pelo servidor de origem, ele permanecerá no disco rígido após o fim da sessão de depuração. Os arquivos de origem são armazenados localmente no subdiretório src das Ferramentas de Depuração para Windows de instalação.

## <a name="source-server-data-blocks"></a>Blocos de dados do servidor de origem

O servidor de origem se baseia em dois blocos de dados dentro do arquivo PDB.

-   Lista de arquivos de origem. A criação de um módulo cria automaticamente uma lista de caminhos totalmente qualificados para os arquivos de origem usados para criar o módulo.
-   Bloco de dados. Indexar a origem, conforme descrito anteriormente, adiciona um fluxo alternativo ao arquivo PDB chamado "srcsrv". O script que insere esses dados depende do processo de build específico e do sistema de controle do código-fonte em uso.

Na especificação de linguagem versão 1, o bloco de dados é dividido em três seções: ini, variáveis e arquivos de origem. Ele tem a sintaxe a seguir.

``` syntax
SRCSRV: ini ------------------------------------------------ 
VERSION=1
VERCTRL=<source_control_str>
DATETIME=<date_time_str>
SRCSRV: variables ------------------------------------------ 
SRCSRVTRG=%sdtrg% 
SRCSRVCMD=%sdcmd% 
SRCSRVENV=var1=string1\bvar2=string2 
DEPOT=//depot 
SDCMD=sd.exe -p %fnvar%(%var2%) print -o %srcsrvtrg% -q %depot%/%var3%#%var4%
SDTRG=%targ%\%var2%\%fnbksl%(%var3%)\%var4%\%fnfile%(%var1%) 
WIN_SDKTOOLS= sserver.microsoft.com:4444 
SRCSRV: source files --------------------------------------- 
<path1>*<var2>*<var3>*<var4> 
<path2>*<var2>*<var3>*<var4> 
<path3>*<var2>*<var3>*<var4> 
<path4>*<var2>*<var3>*<var4> 
SRCSRV: end ------------------------------------------------
```

Todo o texto é interpretado literalmente, exceto pelo texto entre sinais de porcentagem (%). O texto entre sinais de porcentagem é tratado como um nome de variável a ser resolvido recursivamente, a menos que seja uma das seguintes funções:

<dl> <dt>

<span id="_fnvar___"></span><span id="_FNVAR___"></span>%fnvar%()
</dt> <dd>

O texto do parâmetro deve ser incluído em sinais de porcentagem e tratado como uma variável a ser expandida.

</dd> <dt>

<span id="_fnbksl___"></span><span id="_FNBKSL___"></span>%fnbksl%()
</dt> <dd>

Todas as barras (/) no texto do parâmetro devem ser substituídas por barras para trás ( \\ ).

</dd> <dt>

<span id="_fnfile___"></span><span id="_FNFILE___"></span>%fnfile%()
</dt> <dd>

Todas as informações de caminho no texto do parâmetro devem ser retiradas, deixando apenas o nome do arquivo.

</dd> </dl>

A seção ini contém variáveis que descrevem os requisitos. O script de indexação pode adicionar qualquer número de variáveis a esta seção. Os exemplos são os seguintes:

<dl> <dt>

<span id="VERSION"></span><span id="version"></span>Versão
</dt> <dd>

A versão de especificação de linguagem. Esta variável é obrigatória.

</dd> <dt>

<span id="VERCTL"></span><span id="verctl"></span>VERCTL
</dt> <dd>

Uma cadeia de caracteres que descreve o produto de controle do código-fonte. Essa variável é opcional.

</dd> <dt>

<span id="DATETIME"></span><span id="datetime"></span>Datetime
</dt> <dd>

Uma cadeia de caracteres que indica a data e a hora em que o arquivo PDB foi processado. Essa variável é opcional.

</dd> </dl>

A seção de variáveis contém variáveis que descrevem como extrair um arquivo do controle do código-fonte. Ele também pode ser usado para definir texto comumente usado como variáveis para reduzir o tamanho do bloco de dados.

<dl> <dt>

<span id="SRCSRVTRG"></span><span id="srcsrvtrg"></span>SRCSRVTRG
</dt> <dd>

Descreve como criar o caminho de destino para o arquivo extraído. Essa é uma variável necessária.

</dd> <dt>

<span id="SRCSRVCMD"></span><span id="srcsrvcmd"></span>SRCSRVCMD
</dt> <dd>

Descreve como criar o comando para extrair o arquivo do controle do código-fonte. Isso inclui o nome do arquivo executável e seus parâmetros de linha de comando. Essa é uma variável necessária.

</dd> <dt>

<span id="SRCSRVENV"></span><span id="srcsrvenv"></span>SRCSRVENV
</dt> <dd>

Uma cadeia de caracteres que lista as variáveis de ambiente a serem criadas durante a extração de arquivo. Separe várias entradas com um caractere de backspace ( \\ b). Essa é uma variável opcional.

</dd> </dl>

A seção arquivos de origem contém uma entrada para cada arquivo de origem que foi indexado. O conteúdo de cada linha é interpretado como variáveis com os nomes VAR1, VAR2, VAR3 e assim por diante até VAR10. As variáveis são separadas por asteriscos. VAR1 deve especificar o caminho totalmente qualificado para o arquivo de origem conforme listado em outro lugar no arquivo PDB. Por exemplo, a seguinte linha:

``` syntax
c:\proj\src\file.cpp*TOOLS_PRJ*tools/mytool/src/file.cpp*3
```

é interpretado da seguinte maneira:

``` syntax
VAR1=c:\proj\src\file.cpp
VAR2=TOOLS_PRJ
VAR3=tools/mytool/src/file.cpp
VAR4=3
```

Neste exemplo, VAR4 é um número de versão. No entanto, a maioria dos sistemas de controle do código-fonte dá suporte à rotulagem de arquivos de forma que o estado de origem de um determinado build possa ser restaurado. Portanto, você pode usar o rótulo para o build. O bloco de dados de exemplo pode ser modificado para conter uma variável como a seguinte:

``` syntax
LABEL=BUILD47
```

Em seguida, supondo que o sistema de controle do código-fonte usa o sinal de ata (@) para indicar um rótulo, você pode modificar a variável SRCSRVCMD da seguinte forma:

**sd.exe -p %fnvar%(%var2%) print -o %srcsrvtrg% -q %depot%/%var3%@%label%**

## <a name="how-source-server-works"></a>Como funciona o servidor de origem

O cliente do servidor de origem é implementado Symsrv.dll. O cliente não extrai informações diretamente do arquivo PDB; ele usa um manipulador de símbolos, como aquele implementado no Dbghelp.dll. É essencialmente um mecanismo de substituição de variável recursiva que cria uma linha de comando que pode ser usada para extrair o arquivo de origem adequado do sistema de controle do código-fonte. Seu código não deve chamar Symsrv.dll diretamente. Para integrar sua funcionalidade ao seu aplicativo, use a [**função SymGetSourceFile.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile)

A primeira versão do servidor de origem funciona da seguinte forma. Esse comportamento pode mudar em versões futuras.

-   O cliente chama a **função SrcSrvInit** com o caminho de destino a ser usado como base para todas as extrações de arquivo de origem. Ele armazena esse caminho na variável TARG.
-   O cliente extrai o fluxo Srcsrv do PDB quando o módulo PDB é carregado e chama a função **SrcSrvLoadModule** para passar o bloco de dados para o servidor de origem.
-   Quando Dbghelp recupera um arquivo de origem, o cliente chama a **função SrcSrvGetFile** para recuperar os arquivos de origem do controle do código-fonte.
-   O servidor de origem pesquisa as entradas de arquivo de origem no bloco de dados para uma entrada que corresponde ao arquivo solicitado. Ele preenche VAR1 para VAR *n* com o conteúdo da entrada do arquivo de origem. Em seguida, ele expande a variável SRCSRVTRG usando VAR1 para VAR *n*. Se o arquivo já estiver nesse local, ele retornará o local para o chamador. Caso contrário, ele expandirá a variável SRCSRVCMD para criar o comando necessário para recuperar o arquivo do controle do código-fonte e copiá-lo para o local de destino. Por fim, ele executa este comando.

## <a name="creating-a-source-control-provider-module"></a>Criando um módulo do provedor de controle do código-fonte

O servidor de origem inclui módulos de provedor para P4.pm (Perforce) e Visual Source Cofre (vss.pm). Para criar seu próprio módulo de provedor, você deve implementar o seguinte conjunto de interfaces.

<dl> <dt>

<span id="_module__SimpleUsage__"></span><span id="_module__simpleusage__"></span><span id="_MODULE__SIMPLEUSAGE__"></span>**$module::SimpleUsage()**
</dt> <dd>

Finalidade: exibe informações de uso de módulo simples para STDOUT.

Parâmetros: nenhum

Valor de retorno: Nenhum

</dd> <dt>

<span id="_module__VerboseUsage__"></span><span id="_module__verboseusage__"></span><span id="_MODULE__VERBOSEUSAGE__"></span>**$module::VerboseUsage()**
</dt> <dd>

Finalidade: exibe informações detalhadas de uso do módulo para STDOUT.

Parâmetros: nenhum

Valor de retorno: Nenhum

</dd> <dt>

<span id="_objref____module__new__CommandArguments_"></span><span id="_objref____module__new__commandarguments_"></span><span id="_OBJREF____MODULE__NEW__COMMANDARGUMENTS_"></span>**$objref = $module::new( \@ CommandArguments)**
</dt> <dd>

Finalidade: inicializa uma instância do módulo do provedor.

Parâmetros: todos @ARGV os argumentos que não foram reconhecidos pelo SSIndex.cmd como sendo argumentos gerais.

Valor de retorno: uma referência que pode ser usada em operações posteriores.

</dd> <dt>

<span id="_objref-_GatherFileInformation__SourcePath___ServerHashReference_"></span><span id="_objref-_gatherfileinformation__sourcepath___serverhashreference_"></span><span id="_OBJREF-_GATHERFILEINFORMATION__SOURCEPATH___SERVERHASHREFERENCE_"></span>**$objref->GatherFileInformation($SourcePath, $ServerHashReference)**
</dt> <dd>

Finalidade: permite que o módulo reúna as informações de indexação de origem necessárias para o diretório especificado pelo parâmetro $SourcePath. O módulo não deve pressupor que essa entrada será chamada apenas uma vez para cada instância de objeto, pois SSIndex.cmd pode chamá-la várias vezes para caminhos diferentes.

Parâmetros: (1) O diretório local que contém a origem a ser indexada. (2) Uma referência a um hash que contém todas as entradas do arquivo Srcsrv.ini especificado.

Valor de retorno: Nenhum

</dd> <dt>

<span id="__VariableHashReference___FileEntry_____objref-_GetFileInfo__LocalFile_"></span><span id="__variablehashreference___fileentry_____objref-_getfileinfo__localfile_"></span><span id="__VARIABLEHASHREFERENCE___FILEENTRY_____OBJREF-_GETFILEINFO__LOCALFILE_"></span>**($VariableHashReference, $FileEntry) = $objref->GetFileInfo($LocalFile)**
</dt> <dd>

Finalidade: fornece as informações necessárias para extrair um único arquivo específico do sistema de controle do código-fonte.

Parâmetros: um nome de arquivo totalmente qualificado

Valor retornado: (1) Uma referência de hash das variáveis necessárias para interpretar o valor retornado $FileEntry. O SSIndex.cmd armazena essas variáveis em cache para cada arquivo de origem usado por um único arquivo de depuração para reduzir a quantidade de informações escritas no fluxo de índice de origem. (2) A entrada de arquivo a ser gravado no fluxo de índice de origem para permitir que SrcSrv.dll extraia esse arquivo do controle do código-fonte. O formato exato dessa linha é específico para o sistema de controle do código-fonte.

</dd> <dt>

<span id="_TextString____objref-_LongName__"></span><span id="_textstring____objref-_longname__"></span><span id="_TEXTSTRING____OBJREF-_LONGNAME__"></span>**$TextString = $objref->LongName()**
</dt> <dd>

Finalidade: fornece uma cadeia de caracteres descritiva para identificar o provedor de controle do código-fonte para o usuário final.

Parâmetros: nenhum

Valor de retorno: o nome descritivo do sistema de controle do código-fonte.

</dd> <dt>

<span id="_StreamVariableLines____objref-_SourceStreamVariables__"></span><span id="_streamvariablelines____objref-_sourcestreamvariables__"></span><span id="_STREAMVARIABLELINES____OBJREF-_SOURCESTREAMVARIABLES__"></span>**@StreamVariableLines = $objref->SourceStreamVariables()**
</dt> <dd>

Finalidade: permite que o provedor de controle do código-fonte adicione variáveis específicas do controle do código-fonte ao fluxo de origem para cada arquivo de depuração. Os módulos de exemplo usam esse método para escrever as variáveis EXTRACT CMD e \_ EXTRACT TARGET \_ necessárias.

Parâmetros: nenhum

Valor de retorno: a lista de entradas para as variáveis de fluxo de origem.

</dd> </dl>

 

 




